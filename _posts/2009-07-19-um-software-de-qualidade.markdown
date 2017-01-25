---
layout: post
title:  Um Software de Qualidade
date:   2009-07-19 16:31:00
categories: Programação
tags: [hibernate, qualidade, wordpress]
permalink: /2009/07/um-software-de-qualidade
---

![wordpress logo](/assets/images/2009/wordpress-logo.png){: .image_on_left} Eu vou falar um pouco mais sobre o [Wordpress][wordpress]{:target="_blank"} porque acho que é um bom exemplo de um software de qualidade.

Vou começar pela instalação. Para instalar o Wordpress, só é necessário verificar o "[Famous 5-Minute Install][wordpress-5-minute]{:target="_blank"}". Pronto. Funciona de verdade. Na verdade não é você que instala o Wordpress, ele se instala sozinho, você apenas manda ele se instalar. Não dá pra engolir softwares que só para instalar é preciso ler um livro cheio de procedimentos e depois acaba dando tudo errado e você ainda tem que ficar pesquisando na internet para ver ser descobre o que aconteceu.

Um dos procedimentos que ele faz na instalação é criar a estrutura do banco de dados. Hoje em dia não é difícil encontrar um framework que facilite isso (vide [Hibernate][hibernate]{:target="_blank"}), por então não fazemos isso sempre?

Outro exemplo que vi de como o Wordpress é robusto foi quando eu resolvi mudar a configuração dos permalinks. Após alterar a configuração veja o que apareceu na tela:

![tela do wordpress](/assets/images/2009/wordpress-permlink.png){: .image_on_center}

Devido a minha escolha o wordpress precisava criar um arquivo .htaccess para atender minha necessidade, como ele sozinho descobriu que não tinha permissão de escrita no diretório, mostrou na tela as instruções detalhadas do procedimento que eu precisava fazer na mão para que os permalinks pudessem funcionar. Quantas vezes você já se deparou com algum erro desconhecido e teve que fuçar logs para descobrir qual o problema?

É verdade, Software Robusto demanda mais esforço mas devemos abrir mão da preguiça. Não podemos é abrir mão da qualidade dos softwares que escrevemos. Software frágeis acabam por consumir a falsa economia no desenvolvimento porque geram um imenso custo de suporte e manutenção. Siga o exemplo do Worpress.

[wordpress]: http://www.wordpress.org 
[wordpress-5-minute]: http://codex.wordpress.org/Installing_WordPress#Famous_5-Minute_Install
[hibernate]: http://www.hibernate.org
