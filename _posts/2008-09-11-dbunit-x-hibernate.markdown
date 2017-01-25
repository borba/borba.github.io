---
layout: post
title:  "DbUnit x Hibernate"
date:   2008-09-11 15:47:37
categories: Programação
tags: [dbunit, ejb, hibernate, junit, princípio dry, tdd, yaml]
permalink: 2008/09/dbunit-x-hibernate
---

Aqui na empresa, temos clientes que apenas mandam executar um projeto segundo a arquitetura definida por eles. Algumas vezes é frustante trabalhar neste tipo de projeto, afinal, nem sempre conseguimos seguir nossas convicções e utilizar plenamente nossos conhecimentos e experiência na definição da melhor solução para o problema. Em um desses projetos, fui convocado para auxiliar a equipe que estava consumindo muito tempo na implementação dos testes.

### O Cenário:

O sistema utiliza [EJB][ejb]{:target="_blank"} 2 e [Hibernate][hibernate]{:target="_blank"} 2. O cliente exige implementação de testes dos métodos da [fachada][fachada]{:target="_blank"} utilizando [JUnit][junit]{:target="_blank"} e [DBUnit][dbunit]{:target="_blank"}.

### Problemas:

A montagem dos cenários é complexa. O DBUnit entende apenas o modelo relacional, isto significa que o engenheiro tem que fazer um “desmapeamento hibernate” na cabeça dele para montar as tabelas e colunas com os valores necessários.

Veja um exemplo:

{% highlight xml %}
<?xml version='1.0' encoding='UTF-8'?>
<dataset>
    <employee start_date="2001-01-01"
              first_name="Drew"
              ssn="333-29-9999"
              last_name="Smith" />

    <employee start_date="2002-04-04"
              first_name="Nick"
              ssn="222-90-1111"
              last_name="Marquiss" />

    <employee start_date="2003-06-03"
              first_name="Jose"
              ssn="111-67-2222"
              last_name="Whitson" />
</dataset>
{% endhighlight %}

Claro que esse é um modelo relacional simples, agora imagine modelos de classes complexos, com heranças, relacionamentos, etc. Neste caso, dá bastante trabalho.

Além da dificuldade em produzir a massa de dados, existe um problema muito grave. Dentro das classes de teste é necessário fazer validações contra os valores do arquivo xml (por exemplo em métodos de consulta). Neste caso podemos fazer as validações com valores hard coded, como neste exemplo:

{% highlight java %}
assertEquals(employee.getFirstName(), "Jose");
{% endhighlight %}

Que é uma péssima idéia, pois viola o [princípio DRY][dry]{:target="_blank"} (Don’t Repeat Yourself). Outra saída é obter os valores do xml através da API do DBUnit, que vai dar uma trabalheira danada, ainda mais se você quiser montar o objeto para fazer comparações deste tipo:

{% highlight java %}
assertEquals(employeeActual, employeeExpected);
{% endhighlight %}

Já imaginou? Vai ter que construir outro hibernate só para pegar cada valor das tabelas e colunas do arquivo XML e remontar os objetos novamente.

### Como Resolver?

O grande problema dessa abordagem é o fato do DBUnit entender apenas de tabelas e colunas. E se existisse um HibernateUnit? No hipotético HibernateUnit eu poderia especificar meus dados na forma de objetos. Além disso, poderia utilizar um formato mais legível e que pudesse ser transformado diretamente para objetos dentro do seu código. Esse formato pode ser o [YAML][yaml]{:target="_blank"}. Veja como ficaria:

{% highlight yaml %}
departaments:
    - &engineering
      id          : 1
      name        : Engineering
      employees:
    - id          : 1
      startDate   : 2001-01-01
      firstName   : Drew
      lastName    : Smith
      ssn         : 333-29-9999
      departament : *engineering
    - id          : 2
      startDate   : 2002-04-04
      firstName   : Nick
      lastName    : Marquiss
      ssn         : 222-90-1111
      departament : *engineering
    - id          : 3
      startDate   : 2003-06-03
      firstName   : Jose
      lastName    : Whitson
      ssn         : 111-67-2222
      departament : *engineering
{% endhighlight %}

Inclui um relacionamento para employee só para ficar um pouco mais rico. A vantagem dessa abordagem é que além de ficar mais legível, existem frameworks que serializam e deserializam esse formato para objetos. Com esse recurso, seria possível obter os objetos diretamente do arquivo e em seguida fazer comparações com objetos obtidos no banco. Legal, hein?

Acho que uma solução deste tipo poderia trazer muitos benefícios para o nosso problema. Estou fazendo uma pesquisa e se não existir nada semelhante, devo implementar essa solução como um projeto open source.

Pena que nosso cliente **EXIGE** que usemos o DBUnit.

[ejb]: http://java.sun.com/products/ejb
[hibernate]: http://www.hibernate.org
[fachada]: http://c2.com/cgi/wiki?FacadePattern
[junit]: http://www.junit.org
[dbunit]: http://dbunit.sourceforge.net
[dry]: http://c2.com/cgi/wiki?DontRepeatYourself
[yaml]: http://www.yaml.org
