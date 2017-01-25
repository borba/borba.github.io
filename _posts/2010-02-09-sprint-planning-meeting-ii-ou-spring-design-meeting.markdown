---
layout: post
title:  Sprint Planning Meeting II ou Sprint Design Meeting?
date:   2010-02-09 00:20:00
categories: Metodologias Ágeis
tags: [scrum, sprint planning]
permalink: /2010/02/sprint-planning-meeting-ii-ou-spring-design-meeting
---

Qual o principal **objetivo** da reunião de Sprint Planning Meeting 2?

![design meeting](/assets/images/2010/design-meeting.jpg){: .image_on_right} Em muitos lugares você poderá encontrar uma resposta simplista para essa pergunta: O objetivo é **dividir** os itens do product backlog em tarefas de no máximo 8 horas (ou 16 em algumas fontes). Mas dividir como?

Durante a Sprint Planning Meeting 1, o time e o product owner selecionaram de comum acordo alguns itens para serem trabalhados durante o sprint em questão. Para chegar neste ponto, o time teve que discutir em mais detalhes cada item de backlog, tirar eventuais dúvidas e revisar algumas estimativas. Em função disso, podemos perceber claramente que se trata de uma reunião para discussão e esclarecimento dos **requisitos**. Até este momento estamos apenas trabalhando em cima do domínio do **problema**, ainda não entramos na solução.

No Sprint Planning Meeting 2 a cuíca muda o tom. Se pensarmos que o objetivo principal é apenas dividir os itens em tarefas, vamos estar na verdade apenas dividindo o problema, mas aqui precisamos na verdade é dividir a **solução**. Para chegar na solução o time vai ter que fazer **design** (análise &amp; projeto), que é exatamente o objetivo desta reunião.

Agora, será que faz diferença? Será que dividir o problema é diferente de dividir a solução? Vejamos alguns exemplos:

Considere o item de backlog chamado Login do Usuário. Algumas possíveis tarefas para Sprint Planning Meeting 2 sem foco em design:

* Implementar tela de login
* Implementar serviço de autenticação

Muito bom, com esse conjunto de tarefas eu posso fazer o item de backlog, o problema é que agrega muito pouco e para efeito de planejamento é desastroso, afinal o time não sabe exatamente o que vai fazer em cada uma dessas tarefas. Tudo vai ser descoberto apenas na hora H. Neste cenário observamos que é muito comum a criação de diversas novas tarefas durante o sprint.

Vamos ver agora que tarefas eu poderia criar se tivesse realizado a reunião com foco em design:

* Criar tela de login
* Selecionar lib js para chamar serviço de autenticação via ajax (supondo que é ajax e uma lib ainda não foi selecionada)
* Criar serviço de autenticação
* Criar query com login=login e senha=senha
* Criar classe de Usuario (campos: login e senha)
* Criar método para criptografar a senha (escolher método)
* e por aí vai...

O que acontece no novo cenário é que a equipe se aprofundou na solução. Neste caso o time pôde definir melhor o escopo de cada tarefa, antecipar dúvidas e eliminar riscos. Mas afinal para que serve o planejamento?

Resumindo:

* Sprint Planning Meeting 1 = Requisitos
* Sprint Planning Meeting 2 = Design

E ainda assim: Sprint Planning Meetings = **planejamento**.
