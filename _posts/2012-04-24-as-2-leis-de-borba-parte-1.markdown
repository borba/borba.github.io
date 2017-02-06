---
layout: post
title:  As 2 Leis de Borba - Parte 1
date:   2012-04-24 10:24:59
categories: Metodologias Ágeis Opinião Programação
tags: [arquitetura, continuous deployment, evolução, leis de borba, mudança]
permalink: /2012/04/as-2-leis-de-borba-parte-1
---

No ano passado preparei uma [aula][blog-arquitetura-pragmatica]{:target="_blank"} sobre Arquitetura de Software para a turma de mestrado do CIN/UFPE. O fio condutor da aula era a desmistificação do conceito de arquitetura, oferecendo uma abordagem mais pragmática. Ao invés de uma arquitetura torre de marfim, cheio de diagramas e regras, apresentei uma opção evolutiva, incremental e flexível. Durante a preparação do material tive um *insight* interessante, que se transformou nas 2 Leis de Borba para Arquitetura de Software.

![leis de newton](/assets/images/2012/leis-de-newton.jpg){: .image_on_center}

Primeira Lei de Borba para Arquitetura de Software: 


> **"Toda a Arquitetura definida está errada."**

Uma arquitetura definida não vale nada enquanto não construimos um sistema em cima dela. Somente um sistema rodando em produção pode provar o valor da arquitetura. Não adianta passar meses elaborando a arquitetura mais maravilhosa do mundo, implementando apenas código de infraestrutura, porque enquanto não existir um sistema rodando e sendo usado por usuários de verdade, você ainda estará na estaca zero.

Agora digamos que eu tenha lançado o meu produto, baseado em uma arquitetura definida e tenho pessoas usando de forma satisfatória o meu sistema. Consegui finalmente provar que minha arquitetura funciona, porém neste caso se aplica a segunda lei...

Segunda Lei de Borba de Arquitetura de Software:

> **"Toda Arquitetura definida e que comprovadamente funciona, estará errada em breve"**

Tudo muda o tempo todo. Pessoas mudam, negócios mudam e consequentemente empresas mudam e requisitos mudam. Lembre-se que depois de lançado seu [produto não é mais seu][blog-produto-seu]{:target="_blank"}, é de seus usuários. Se você não conseguir adaptar seu sistemas às mudanças do ambiente, será extinto. A seleção natural de Darwin funciona aqui também.

A melhor forma de enfrentar esse tipo de situação é adotar uma abordagem evolutiva. Defina e construa sua arquitetura/infraestrutura a medida que for construindo seu sistema. Instale seu sistema o mais rápido possível e aprenda com seus usuários.

Dicas:

* Crie uma solução de baixo acoplamento e alta coesão, para facilitar as mudanças
* Use TDD para poder integrar o novo código de forma mais rápida e econômica
* Utilize *design* incremental
* *Refactoring* sempre
* Crie uma estrutura para fazer (ou desfazer) *deployments* na maior frequencia possível (Facebook [faz 5 vezes por semana][facebook-deploy]{:target="_blank"}
* Colete [métricas][metricas]{:target="_blank"} para aprender com seus usuários e tomar decisões baseadas em dados reais

Esteja disposto e preparado a mudar sempre. Não seja um [Dodô][dodo]{:target="_blank"}.

O mais importante é que a aplicabilidade dessas leis não se limitam ao contexto de Arquitetura de Software. mas isso é assunto para o próximo post desta série.

[blog-arquitetura-pragmatica]: /2011/04/arquitetura-pragmatica
[blog-produto-seu]: /2012/01/um-produto-pra-chamar-de-seu
[facebook-deploy]: https://www.facebook.com/photo.php?v=10100259101684977
[metricas]: http://www.fourhourworkweek.com/blog/2009/05/19/vanity-metrics-vs-actionable-metrics/
[dodo]: http://pt.wikipedia.org/wiki/Dod%C3%B3


