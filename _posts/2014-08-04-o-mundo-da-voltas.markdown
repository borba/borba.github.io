---
layout: post
title:  O Mundo dá Voltas
date:   2014-08-04 15:12:44
categories: Memória Opinião Programação
tags: [assembly, c, lisp, ms dos, programação concorrente]
permalink: /2014/08/o-mundo-da-voltas
---

[![Planeta Terra](http://borba.blog.br/wordpress/wp-content/uploads/2014/08/terra.jpg "")](http://borba.blog.br/2013/11/uma-licao-para-nao-ser-aprendida/ "Uma Lição para não ser Aprendida")

Como já falei [aqui](http://borba.blog.br/2013/11/uma-licao-para-nao-ser-aprendida/ "Uma Lição para não ser Aprendida"), comecei a minha vida profissional trabalhando com [C](http://pt.wikipedia.org/wiki/C_(linguagem_de_programa%C3%A7%C3%A3o) "C") e [Assembly](http://pt.wikipedia.org/wiki/Assembly "Assembly"), o que me deu uma base de conhecimento muito boa sobre como o computador funciona. Recentemente participei de uma discussão sobre a elaboração de um treinamento sobre programação concorrente. Uma das minha sugestões foi que fizesse parte do escopo do treinamento a criação de um escalonador de tarefas não preemptivo escrito em C para [MS-DOS](http://pt.wikipedia.org/wiki/MS-DOS "MS-DOS"). Pode até parecer loucura e perda de tempo o investimento nessas tecnologias obsoletas, mas me deixe defender essa posição.

Eu acho que a maioria dos novos engenheiros hoje em dia tem dificuldade de dominar certos conceitos porque nunca desenvolveram programas de baixo nível, mais próximos da máquina. Trabalhar exclusivamente em um nível de abstração muito alto dificulta o entendimento do que acontece por baixo dos panos (já falei sobre isso [aqui](http://borba.blog.br/2008/09/aprenda-c/ "Aprenda C")). Criar uma aplicação multitasking em um sistema operacional que não dá suporte multitasking, nos obriga a dominar uma série de conceitos mais próximos da máquina (como interrupções e chaveamento de contexo) para superar esse desafio. Além disso, quero chamar a atenção para outro aspecto.

O [NodeJS](http://nodejs.org/ "NodeJS") é uma ferramenta moderna que ganhou bastante popularidade nos últimos anos. O maior apelo dela é a facilidade na criação de aplicações rápidas e escaláveis em [Javascript](http://pt.wikipedia.org/wiki/Javascript "Javascript"). O pulo do gato do NodeJS é a utilização de uma única thread com um loop de eventos executando [fibers](http://en.wikipedia.org/wiki/Fiber_(computer_science) "Fibers"). Fiber nada mais é do que um processo de excução não preemptivo. Exatamente a mesma solução que usávamos no MS-DOS em 1990.

O mundo dá voltas, e não é só neste caso. O modelo de programação concorrente com [actors](http://en.wikipedia.org/wiki/Actor_model "Actors Model") foi criado em 1973 e o conceito de [map reduce](http://en.wikipedia.org/wiki/Lisp_(programming_language) "LISP") também já existia antes de eu nascer.

Fazer um curso hoje usando tecnologias tão antigas e obsoletas pode nos ajudar a sempre ter um olho atento ao que já passou, porque lá do passado podemos encontrar as soluções para os nossos problemas atuais. De quebra, ia ser bastante divertido fazer o contraste entre as ferramentas antigas e as atuais. Acho que depois de uma experiência dessa eu nunca mais ia reclamar do Java.