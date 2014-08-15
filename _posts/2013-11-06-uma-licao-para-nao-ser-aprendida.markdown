---
layout: post
title:  Uma Lição para não ser Aprendida
date:   2013-11-06 13:13:04
categories: Memória Tecnologia
tags: [bugs, c, corisco, dos, lições aprendidas, microterminal, mt100, tecnologia, twr, z80]
permalink: /2013/11/uma-licao-para-nao-ser-aprendida
---

No começo da década de 90 eu trabalhava em uma empresa chamada TWR Informática. Lá, eu programava para o MT100, um microterminal para entrada de dados.

O MT100 era um pequeno dispositivo com um teclado numérico e um display de 2 linhas de 16 caracteres, controlado por um processador Z80. O software que comandava este equipamento rodava em um computador PC, onde os terminais eram ligados através de sua interface paralela.
[![z80](http://borba.blog.br/wordpress/wp-content/uploads/2013/11/z80.jpg "")](http://borba.blog.br/wordpress/wp-content/uploads/2013/11/z80.jpg "")

O programa que controlava o que aparecia na tela dos microterminais e processava os inputs dos usuários, rodava de forma [residente](http://en.wikipedia.org/wiki/Terminate_and_Stay_Resident "") no DOS. O programa era "acordado" de tempos em tempos por uma interrupção do sistema (minha memória não é suficientemente boa para lembrar qual interrupçãao usávamos), fazia o polling dos dispositivos e executava a lógica necessária.

Depois de algumas versões, resolvemos enfrentar o desafio de fazer com que os programas do MT100 fizessem acesso a arquivos de dados. Nossa primeira abordagem foi criar um formato proprietário para armazenar os dados necessários, mas rapidamente nos deparamos com o problema de que precisaríamos criar arquivos de índices para acesso mais eficiente aos dados.

Rildo Pragana, conhecido por ter criado o Corisco (o legítimo computador pernambucano), era nosso líder técnico. Um belo dia, Rildo trouxe um disquete com uma biblioteca que implementava a estrutura B-Tree, escolha lógica para implementar a solução dos índices. No dia seguinte ele viajou, deixando essa nobre tarefa para a sua jovem equipe.

[![corisco](http://borba.blog.br/wordpress/wp-content/uploads/2013/11/corisco-295x300.gif "")](http://borba.blog.br/wordpress/wp-content/uploads/2013/11/corisco.gif "")

Começamos a tentar colocar a biblioteca para funcionar, mas por mais tentássemos, o bagulho não funcionava. Depois de quebrar a cabeça por um bom tempo chegamos a conclusão que a biblioteca estava irremediavelmente bugada. Como o uso desta biblioteca se provou ser um beco sem saída, passamos para o plano b, vamos escrever nossa própria implementação de B-Tree.

Pense em um desafio tesão. Corremos imediatamente para a Livro 7 e compramos um livro que mostrava como funcionava essa estrutura de dados. Eu sei que a essas alturas você deve estar se perguntando por que não procuramos no Google ou no Wikipedia, mas naquele tempo não existia nada disso. Internet pra mim era o e-mail que eu tinha na faculdade e lamba os beiços.

Aquela semana de trabalho, onde todo mundo chegava pra trabalhar já de pau duro (não literal, por favor) é uma das lembranças mais legais que eu tenho da minha carreira. O trabalho valeu a pena. Após alguns dias, os sistemas feitos para o MT100 finalmente podiam fazer consultas a dados de forma eficiente. Agora, era só esperar a chegada de Rildo para coroar aquele trabalho maravilhoso.

Rildo chega, a equipe toda reunida conta o que aconteceu, de como ele nos atrapalhou nos dando uma biblioteca quebrada e como nós salvamos o dia criando a nossa própria solução. Sabe qual foi o resultado?

ESPORRO MONUMENTAL! ESPORRO 8.5 na escala Richter.

"Eu não disse que era pra usar essa biblioteca?", Rildo esbravejava.

"Mas não funciona. Tentamos de tudo, não tem jeito", a gente se defendia, ainda perplexos com a reação de Rildo.

"Me dê essa porra de disquete aqui", Rildo disse, pegando o disquete e saindo para casa.

No dia seguinte, ainda confusos com o acontecido, esperamos a chegada de Rildo para saber o que fazer em seguida. Rildo finalmente chega com um sorriso que ia de orelha a orelha. Senta esparramado na cadeira joga o disquete na mesa e diz: "Era um bug da biblioteca padrão do Turbo C 1.5, já corrigi, esta aí. Podem usar a biblioteca agora".

Como é? Um bug no C? Ele corrigiu? Como esse gênio filho de uma puta conseguiu descobrir?

[![velho oeste](http://borba.blog.br/wordpress/wp-content/uploads/2013/11/once-upon-a-time-in-the-west1-1024x805.jpg "")](http://borba.blog.br/wordpress/wp-content/uploads/2013/11/once-upon-a-time-in-the-west1.jpg "")

Deste episódio, tirei várias lições, mas quero falar sobre uma lição que não deve ser aprendida. Não estamos mais nos tempos do velho oeste. Nossos sistemas operacionais, nossos compiladores, nossas bibliotecas, nossas ferramentas estão muito mais maduras e estáveis do que naquele tempo. A quantidade de desenvolvedores que usam essas tecnologias se multiplicou, criando massa crítica para que essas bibliotecas atinjam a maturidade mais rapidamente. Se você se deparar hoje em dia com um bug fantasmagórico o mais provável é que o erro seja realmente seu. Culpar o compilador, a biblioteca ou o sistema operacional só faz você perder tempo e se distanciar da solução.