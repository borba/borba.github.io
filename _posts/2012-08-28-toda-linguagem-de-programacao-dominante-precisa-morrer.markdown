---
layout: post
title:  Toda linguagem de programação dominante precisa morrer?
date:   2012-08-28 01:50:51
categories: Opinião Programação
tags: [cobol, java, linguagens, programação, scala]
permalink: /2012/08/toda-linguagem-de-programacao-dominante-precisa-morrer
---

![linguagens de programação](/assets/images/2012/prog-lang.jpg){: .image_on_center}

[Fernando Castor][castor]{:target="_blank"}, professor do [Centro de Informática da UFPE][cin]{:target="_blank"}, esteve no [CESAR][cesar]{:target="_blank"} para apresentar a palestra "[As próximas cinco linguagens para você aprender... e por quê?][5-linguagens]{:target="_blank"}". Gostei muito da palestra, que me deu a oportunidade de refletir sobre 2 *posts* que tinha escrito há algum tempo.

O primeiro deles é "[Aprenda C][blog-aprenda-c]{:target="_blank"}", de 2008, onde eu indicava que C deveria ser a primeira linguagem a ser aprendida. A lógica da minha sugestão é que as linguagens são abstrações imperfeitas sobre o funcionamento da máquina. Imperfeitas porque muitas vezes a escolha da melhor solução depende do conhecimento do programador de como aquelas instruções são compiladas ou interpretadas. O aprendizado de C lhe permite obter este tipo de conhecimento, dando uma base de conhecimentos sólidos para ser um bom programador em outras linguagens.

Castor no entanto, indica que [Python][python]{:target="_blank"} deveria ser a primeira linguagem a ser aprendida, dada a sua facilidade e simplicidade. A ideia dele é dar os primeiros passos em uma linguagem amigável e fácil de desenvolver os primeiros programas para só então partir para o C. Curiosamente um dos comentários feitos no post dizia o mesmo. Só quero dizer que após refletir sobre esses argumentos, cheguei a conclusão que concordo com ambos. **Aprenda Python primeiro**, mas não demore para** aprender C também**.

O segundo post é "[Será o Java o novo COBOL?][blog-java-cobol]{:target="_blank"}", de 2011, onde eu conto um pouco da história de Java, de como esta linguagem se tornou a mais popular para a criação de aplicações *enterprise* e como atravessa um período de decadência, em função das raras e decepcionantes novas versões. Por conta disso, comparo com Java com COBOL, que durante cerca de 40 anos foi um padrão para aplicações neste mercado até ser superado por Java e ficar relegado ao legado (um baita legado na verdade).

Em sua apresentação Fernando diz que Java envelheceu mal, mas que não há como desprezar o monte de coisas desenvolvidas nesta plataforma. Segundo ele, precisamos de uma linguagem pós-java, que incorpore novos e modernos recursos, mas que esteja integrada ao ecossistema Java. Ele elege [Scala][scala]{:target="_blank"} como sendo essa linguagem.

Sobre o evelhecimento do Java, fico imaginando que pode ser efeito comum a toda linguagem que seja dominante para essa categoria de sistemas. Depois de ser utilizada em uma quantidade muito grande de empresas, o compromisso com compatibilidade com o legado e a pressão conservadora do mercado impõe restrições que novos *players* não tem. Sempre será mais fácil incorporar inovações disruptivas em novas linguagens do que em atualizações de linguagens existentes. Esta situação sempre vai gerar a visão de que a linguagem dominante envelheceu. **Aconteceu com COBOL e está acontecendo com Java.**

Sobre Scala como sucessor de Java, aí eu tenho minhas dúvidas... Apesar da [empolgação da mídia][java-scala]{:target="_blank"}, dos [investimentos recentes][typesafe]{:target="_blank"} e até da [minha própria animação][blog-funcionais]{:target="_blank"} com Scala, cheguei a conclusão que está ela sendo conduzida de forma muito acadêmica e gerando muita complexidade. Acredito que esta complexidade vai impedir a adoção de Scala nos mercados empresariais, aumentando a vida útil da linguagem Java. Neste caso, continuo acreditando que **a linguagem que vai substituir Java ainda não foi inventada**, ou pelo menos ainda não foi divulgada propriamente.


[castor]: https://sites.google.com/a/cin.ufpe.br/castor/
[cin]: http://www2.cin.ufpe.br/site/index.php
[cesar]: http://www.cesar.org.br
[5-linguagens]: http://www.youtube.com/watch?v=MsWmSCCVj5Y
[blog-aprenda-c]: /2008/09/aprenda-c/
[python]: http://www.python.org/
[blog-java-cobol]: /2011/02/sera-o-java-o-novo-cobol/
[scala]: http://www.scala-lang.org/
[java-scala]: http://www.theserverside.com/feature/Disruptive-forces-in-Java-Is-Scala-the-new-Spring-framework
[typesafe]: http://www.eweek.com/c/a/Application-Development/Typesafe-Scala-Software-Maker-Gets-14M-to-Boost-Stack-826474/
[blog-funcionais]: /2010/04/porque-linguagens-funcionais-sao-importantes/