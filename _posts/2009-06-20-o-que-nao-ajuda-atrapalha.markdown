---
layout: post
title:  O que não ajuda, atrapalha...
date:   2009-06-20 11:42:00
categories: Programação
tags: [c, nhibernate]
permalink: /2009/06/o-que-nao-ajuda-atrapalha
---

Trabalhei esses últimos dias fazendo uma otimização de uma rotina escrita em C# e que usava NHibernate. Uma das mudanças que fiz foi fazer um bulk delete de uma certa entidade. Quis o destino que eu encontrasse um método delete com uma assinatura que recebia uma query. Perfeito!

Fiz a minha parte:

{% highlight csharp %}
sessao.Delete("FROM Ocorrencia WHERE ...");
{% endhighlight %}

Não é que o maldito NHibernate ao invés de simplesmente criar a query de remoção, executa uma query de consulta, monta todos as entidades (no caso, Ocorrencia) e depois dá delete de um por um?

Por que diabos alguém em seu juízo perfeito escreveria um método tão estúpido quanto esse? Se eu já quero apagar esses objetos porque carrega-los na memória, consumindo o meu já escasso tempo de processamento?

Fica a lição: **NÃO PROGRAME POR COINCIDÊNCIA**. Não é apenas porque um método tem a assinatura perfeita que ele vai ser a solução do seu problema. **LEIA A DOCUMENTAÇÃO**. Certifique-se que está fazendo a coisa certa, ou caso contrário você vai se dar muito mal.