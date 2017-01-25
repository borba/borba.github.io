---
layout: post
title:  Porque linguagens funcionais são importantes
date:   2010-04-27 16:43:34
categories: Programação
tags: [funcional]
permalink: /2010/04/porque-linguagens-funcionais-sao-importantes
---

![functional programming cartoon](/assets/images/2010/fp-cartoon.png){: .image_on_left} Dos 3 principais paradigmas de programação (funcional, imperativo e orientado a objetos), o funcional é o mais antigo. A primeira linguagem de programação funcional foi criada em 1955 (IPL) e a mais popular LISP foi criada em 1958. Apesar de surgirem um pouco depois (Fortran e COBOL foram criadas respectivamentes em 1956 e 1959), as linguagens imperativas tiveram maior popularidade. Mesmo sem ter alcançado o *mainstream*, o paradigma funcional continou recebendo investimentos ano após ano até meados dos anos 90, quando a turma das linguagens imperativas se fundiu definitivamente com o pessoal de orientação a objetos (C++ e principalmente Java são exemplos) enterrando as linguagens funcionais no lixo da história. Acabaram as esperanças desse paradigma se tornar parte do *mainstream*. Será?

O tempo passou e nos últimos anos alguns sinais começaram a aparecer. Erlang (linguagem funcional proprietária criada pela Ericsson) que foi banida e distribuida de forma open-source em 98, volta a ser utilizada pela Ericsson (e por muitos outros) em 2004. A Microsoft lança o F# (linguagem funcional para a plataforma .NET). O pessoal do Twitter reescreve seu back-end em Scala (linguagem funcional e OO para a plataforma Java). C# incorpora conceitos funcionais na sua linguagem para dar suporte ao LINQ. A Google publica artigos mostrando como utiliza o paradigma funcional para armazenar e recuperar dados. Porque esse interesse no paradigma funcional foi renovado? Qual o pulo do gato?

Devido a proximidade de limites técnicos e preocupação com consumo de energia, o pessoal de hardware está focando no desenvolvimento de novos processadores em soluções de múltiplos cores. Em breve teremos processadores com centenas de cores. Para se beneficiar deste panorama, temos que escrever softwares que executem de forma paralela. A boa notícia é que é muito mais fácil escrever código concorrente em liguagens funcionais do que em linguagens imperativas.

Não existe um único paradigma que seja indicado para resolver todos os tipos de problemas. Precisamos aprender (ou reaprender) o paradigma funcional, que foi abandonado por muito tempo. Precisamos de linguagens que incluam de forma coerente vários paradigmas, para que a gente possa escolher a melhor forma de resolver um determinado problema. Por fim, precisamos aprender [Scala][scala]{:target="_blank"}, que me parece a mais promissora nas novas linguagens multi-paradigma.

[scala]: http://scala-lang.org/