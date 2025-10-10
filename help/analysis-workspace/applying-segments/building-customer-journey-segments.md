---
title: Criação de segmentos de jornada do cliente
description: Saiba como criar segmentos de jornada do cliente com base no comportamento no Adobe Analytics e melhorar a experiência do cliente com o Adobe Experience Cloud seguindo este guia passo a passo.
feature: Segmentation
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13180
thumbnail: KT-13180.jpeg
exl-id: c06afc7b-e997-404d-82a4-e7ec5d5ba44d
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 1%

---

# Criação de segmentos de jornada do cliente

Saiba como criar segmentos de jornada do cliente com base no comportamento no Adobe Analytics e melhorar a experiência do cliente com o Adobe Experience Cloud seguindo este guia passo a passo.

Vamos criar melhores segmentos de jornada do cliente! Nesta série, usaremos o Adobe Analytics para definir segmentos comportamentais, estimar tamanhos de público-alvo e rastrear o movimento do usuário. Ao final, você poderá personalizar a mídia e melhorar a experiência dos clientes com o Adobe Experience Cloud. Lembre-se de que esses segmentos estão ativos e devem ser atualizados conforme você aprende mais sobre os clientes. Embora os relatórios possam apresentar alguns desafios, não se preocupe, eu vou guiá-lo através dele! Vamos começar criando nosso primeiro conjunto de segmentos de Jornada de clientes, começando com o segmento &quot;Maravilhas de uma ocorrência&quot;.

Hoje, criaremos espaços reservados para nosso primeiro conjunto de segmentos de Jornada de clientes, criaremos um Adobe Analytics Workspace para nos ajudar a definir nossos segmentos e nosso primeiro segmento, &quot;Maravilhas de uma só ocorrência&quot;.

No final desta série, você poderá criar segmentos de jornada do cliente no Adobe Analytics com base em sinais comportamentais. Você poderá estimar o tamanho de cada público-alvo em cada estágio da jornada e entender em que taxa os usuários se movem entre esses estágios. E você poderá exportar esses públicos-alvo de jornadas do cliente para o Adobe Experience Cloud para permitir a personalização e o direcionamento de mídia.

Cada negócio é diferente, o que significa que os segmentos de jornada de seus clientes serão diferentes dos meus. Portanto, em vez de receitar fórmulas específicas para seus segmentos, sugira algumas coisas a serem observadas e um processo geral para criá-las.

Também é importante observar que os segmentos de jornada do cliente serão segmentos ativos. Este não é um exercício isolado. À medida que você aprende mais sobre os clientes, atualizará esses segmentos. Isso apresenta alguns desafios para os relatórios. As pessoas querem consistência em seus relatórios e, se as definições de segmento mudarem, os números nos relatórios também mudarão.

## Introdução aos segmentos de intenção de visita

A primeira etapa para criar segmentos de jornada do cliente é inferir por que um convidado está em seu site usando sinais de comportamento e, se disponível, dados de Voz do cliente. Criaremos um conjunto de segmentos de Intenção de visita para categorizar todas as visitas no site. Neste ponto, nossos segmentos de Intenção de visita precisam ser mutuamente exclusivos e completamente exaustivos. Cada visita deve pertencer a um, e somente a um, segmento de Intenção de visita.

Os segmentos de Intenção de visita descrevem uma visita, portanto, usaremos o contêiner de Visitas na definição do segmento.

Meu conjunto inicial de segmentos de Intenção de visita incluía:

* Maravilhas de uma ocorrência
* Percepção
* Consideração
* Reserva (Compra)
* Retenção (gerenciar uma reserva/compra)

Para facilitar o uso dos meus segmentos de intenção de visita, adicionei &quot;intenção&quot; aos nomes dos segmentos, dei a eles um número para ativar a classificação e marquei-os como &quot;intenção&quot;. Meus segmentos pareciam com a figura abaixo.

![segmentos de intenção](assets/intent-segments.png)

**Crie os Segmentos de Intenção de Visita usando o contêiner Visitas com uma definição de espaço reservado de Exibições de Página >= 1.**

Como veremos, a criação desses segmentos é um processo interativo e interconectado. Eu descreverei o processo de construção desses segmentos em uma publicação futura.

## Workspace de qualidade de dados do segmento de intenção de visita

![espaço de trabalho de intenção de visita](assets/visit-intent-workspace.png)

Usei um espaço de trabalho simples para garantir que estava definindo bem meus segmentos de Intenção de visita. Lembre-se de que cada visita precisa pertencer a um, e somente a um, segmento de Intenção de visita. O espaço de trabalho que eu configuro garante que todas as visitas sejam contabilizadas e que não haja sobreposição entre os segmentos.

Nomeei esse espaço de trabalho como &quot;QUALIDADE DE DADOS: segmentos de intenção de visita&quot; com as tags &quot;qualidade dos dados&quot;, &quot;intenção de visita&quot; e &quot;jornada do cliente&quot;. Posteriormente, criaremos um &quot;Painel de intenções de visita&quot;, de modo que o prefixo &quot;QUALIDADE DOS DADOS&quot; indique que esse espaço de trabalho serve para configurar e manter os segmentos. É um painel administrativo que tem relativamente pouco insight de negócios, mas é importante para garantir que os segmentos sejam mantidos. É uma boa ideia voltar rotineiramente a esse painel ou configurar alertas para garantir que seus segmentos permaneçam definidos corretamente.

A visualização mais importante deste espaço de trabalho é a de forma livre Sobreposição de segmento, no meio à esquerda. Usando a métrica Visitas, crie filtros de coluna para cada segmento de Intenção de visita, além do segmento Todas as visitas na coluna mais à direita. Crie linhas para cada segmento de Intenção de visita à esquerda. Agora você terá uma visualização entre guias. Quando seus segmentos estiverem configurados corretamente, haverá dados em apenas uma coluna e uma linha, na interseção de cada segmento de intenção de visita consigo mesmo.

As próximas visualizações mais importantes são as métricas de resumo na parte superior esquerda. O resumo de Visitas segmentadas obtém seu valor da coluna Todas as visitas na visualização Sobreposição de segmento imediatamente abaixo. O resumo de Todas as visitas tem sua própria tabela oculta.

![todas as visitas](assets/all-visits.png)

Na parte superior direita, adicionei métricas a cada um dos segmentos para atribuir um certo &quot;sabor&quot; à forma como os segmentos estão se formando. Em particular, como esses segmentos são mutuamente exclusivos, só espero ver reservas para o segmento de Intenção de reserva (não se preocupe, chegaremos às taxas de conversão quando fizermos esses segmentos de Intenção de visita com base no visitante.

Lembre-se de que acabamos de criar segmentos de espaço reservado. Inicialmente, seu espaço de trabalho ficará escancarado. Todos os segmentos de intenção de visita se sobreporão 100% porque têm a mesma definição. Isso está correto e é exatamente o que você deseja ver nesse ponto do processo. À medida que construímos as definições de segmento, você começará a ver esses segmentos começarem a tomar forma.

![Definições de segmento de intenção de visita](assets/visit-intent-segment-defs.png)

## Criação do segmento de primeira intenção de visita

Definir segmentos de intenção de visita é um processo de eliminação e há muita interdependência entre eles. Portanto, não construí esses segmentos na ordem da jornada, construí-os na ordem do mais facilmente definido para o mais desafiador. Isso me deu esta ordem:

1. Intenção: 0 - Maravilhas de uma ocorrência
1. Intenção: 3 - Reserva
1. Intenção: 4 - Retenção
1. Propósito: 2 - Consideração
1. Propósito: 1 - Percepção

Muito aleatório, hein? A definição desses segmentos de Intenção de visita era um processo iterativo, indireto, e geralmente um ajuste a um segmento exigia atualizações para outros segmentos. Isso ficará mais claro à medida que descrevo como defini cada um desses segmentos.

Hoje, vamos definir nosso primeiro, e mais fácil, segmento, One Hit Wonders

## Criação do segmento One Hit Wonders

Meu primeiro segmento, &quot;One Hit Wonders&quot;, foi fácil de definir. É qualquer visita com apenas uma exibição de página. Realmente não sabemos por que esse usuário estava no site, porque ele rejeitou. Suponho que pudéssemos adivinhar uma intenção com base em sua página de entrada, mas com apenas uma visualização de página, simplesmente não há informações suficientes para fazer uma suposição informada sobre a intenção.

![Definição de segmento](assets/segment-def.png)

Depois de definir esse segmento, você começará a ver sua Workspace de intenção de visita tomando forma.

![Mais definições de segmento](assets/more-segment-defs.png)

A criação de segmentos de jornada do cliente usando o Adobe Analytics é um processo desafiador, mas gratificante. Ao criar segmentos comportamentais, estimar o tamanho do público e rastrear os movimentos do usuário, as empresas podem personalizar a mídia e melhorar a experiência do cliente. Cada empresa é única e não há fórmulas específicas para criar segmentos, mas diretrizes e um processo a ser seguido. Os segmentos devem ser atualizados à medida que as empresas aprendem mais sobre seus clientes, o que apresenta desafios de geração de relatórios. Ao seguir o processo de criação de segmentos de Intenção de visita, as empresas podem melhorar a experiência geral do cliente.

## Autora

Este documento foi escrito por:

![Aaron Fossum](assets/aaron-headshot.png)

**Aaron Fossum**, Diretor, Digital Analytics

Especialista no Adobe Analytics
