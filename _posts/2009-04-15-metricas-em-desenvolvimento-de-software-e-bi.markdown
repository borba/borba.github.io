---
layout: post
title:  Métricas em Desenvolvimento de Software e BI
date:   2009-04-15 23:26:00
categories: Palestras
tags: [bi, data mart, kettle, Métricas, pentaho]
permalink: /2009/04/metricas-em-desenvolvimento-de-software-e-bi
---

![metrics](/assets/images/2009/fita-metrica.jpg){: .image_on_center}Estou participando aqui no trabalho do ajuste do data mart de projetos. Esse trabalho me fez lembrar de uma apresentação que fiz no Developer's World 2004: "Métricas em Fábricas de Software" ou "Tudo o que você sempre quis saber sobre o seu projeto mas tinha medo de perguntar".

Tudo evolui tão rápido na nossa área, que normalmente essas apresentações antigas ficam facilmente obsoletas, mas dando uma olhada nessa, achei que as perguntas ainda são bem relevantes e interessantes. Cá pra nós eu odeio mesmo o título oficial, não suporto o termo "Fábrica de Software". Fábrica dá uma conotação próxima a manufatura, que não representa de forma alguma o conceito de desenvolvimento de software.

De qualquer forma, estou querendo chamar a atenção para as ferramentas que estamos usando para implementar nosso data mart de projetos. Estamos usando uma suite open source chamada [Pentaho][pentaho]{:target="_blank"}. Plataformas de BI normalmente são complexas e muito caras, mas a ferramenta de ETL do pentaho (Kettle ou Pentaho Data Integration) é muito boa. Tem seus pequenos problemas de interface mas em termos de funcionalidades é bastante poderosa. Me irrita bastante quando as pessoas precisam fazer um trabalho específico e não usam a ferramenta adequada, por isso quando precisar criar um data warehouse ou mesmo quando for fazer uma migração de um banco para outro, utilize uma ferramenta de ETL, e em especial considere utilizar o Kettle. Você vai ganhar muito tempo...

Para curtir um pouco a nostalgia, aqui está a apresentação de 2004.

{% raw %}
<center>
<iframe src="//www.slideshare.net/slideshow/embed_code/key/bjWSccvdWlz38O" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%; text-align: center;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/lborba/mtricas-em-fabricas-de-software" title="Métricas Em Fabricas De Software" target="_blank">Métricas Em Fabricas De Software</a> </strong> de <strong><a target="_blank" href="//www.slideshare.net/lborba">Luiz Borba</a></strong> </div>
</center>
{% endraw %}

[pentaho]: http://www.pentaho.org/