---
title: Construção de segmentos de Jornada do cliente
description: Saiba como criar segmentos de jornada de clientes baseados em comportamento no Adobe Analytics e melhorar a experiência de seus clientes com o Adobe Experience Cloud seguindo este guia passo a passo.
feature: Segmentation
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13180
thumbnail: KT-13180.jpeg
source-git-commit: d7b1fac5c98080f9ca786ea21a3700d2937c7ebc
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---


# Construção de segmentos de Jornada do cliente

Saiba como criar segmentos de jornada de clientes baseados em comportamento no Adobe Analytics e melhorar a experiência de seus clientes com o Adobe Experience Cloud seguindo este guia passo a passo.

Vamos criar melhores segmentos de jornada do cliente! Nesta série, usaremos o Adobe Analytics para definir segmentos baseados em comportamento, estimar os tamanhos do público-alvo e rastrear o movimento do usuário. No final, você poderá personalizar a mídia e melhorar a experiência dos clientes com o Adobe Experience Cloud. Lembre-se de que esses segmentos estão vivendo e devem ser atualizados à medida que você aprende mais sobre seus clientes. Embora os relatórios possam apresentar alguns desafios, não se preocupe, eu vou guiá-lo! Vamos começar criando nosso primeiro conjunto de segmentos de Jornada do cliente, começando com o segmento &quot;One Hit Wonders&quot;.

Hoje, criaremos espaços reservados para nosso primeiro conjunto de segmentos da Jornada do cliente, criaremos um espaço de trabalho do Adobe Analytics para nos ajudar a definir nossos segmentos e definir nosso primeiro segmento, &quot;One Hit Wonders&quot;.

No final desta série, você poderá criar segmentos de jornada do cliente no Adobe Analytics com base em sinais comportamentais. Você poderá estimar o tamanho de cada público-alvo em cada estágio da jornada e entender a que taxa os usuários se movem entre esses estágios. Além disso, você poderá exportar esses públicos-alvo de jornada do cliente para o Adobe Experience Cloud para permitir a personalização e o direcionamento de mídia.

Cada negócio é diferente, o que significa que os segmentos de jornada do cliente terão uma aparência diferente da minha. Portanto, em vez de prescrever fórmulas específicas para seus segmentos, sugerir algumas coisas para observar e um processo geral para criá-las.

Também é importante observar que seus segmentos de jornada do cliente serão segmentos vivos. Não se trata de um exercício unilateral. À medida que você aprende mais sobre seus clientes, atualizará esses segmentos. Isso apresenta alguns desafios para os relatórios. As pessoas desejam consistência em seus relatórios e, se as definições de segmento forem alteradas, os números nos relatórios também serão alterados.

## Introdução aos segmentos de intenção de visita

A primeira etapa para criar segmentos de jornada do cliente é descobrir por que um convidado está em seu site usando sinais de comportamento e, se disponível, dados de Voz do cliente. Criaremos um conjunto de segmentos de intenção de visita para categorizar todas as visitas no site. Neste ponto, nossos segmentos de intenção de visita precisam ser mutuamente exclusivos e completamente exaustivos. Cada visita deve pertencer a um segmento de Intenção de visita e a apenas um.

Os segmentos de intenção de visita descrevem uma visita, de modo que usaremos o contêiner de Visitas na definição do segmento.

Meu conjunto inicial de segmentos de intenção de visita inclui:

* Martelos de uma ocorrência
* Consciência
* Consideração
* Reserva (Compra)
* Retenção (gerencie uma reserva/compra)

Para facilitar o uso dos meus segmentos de Intenção de visita, prefixei os nomes de segmento com &quot;Intenção:&quot;, dei a eles um número para ativar a classificação e marcei-os como &quot;intenção&quot;. Meus segmentos pareciam com a figura abaixo.

![segmentos de intenção](assets/intent-segments.png)

**Vá em frente e crie seus Segmentos de intenção de visita usando o contêiner Visitas com uma definição de espaço reservado de Exibições de página >= 1.**

Como veremos, construir esses segmentos é um processo iterativo e interconectado. Descreverei o processo de construção desses segmentos em uma publicação futura.

## Espaço de trabalho de qualidade dos dados do segmento de intenção de visita

![espaço de trabalho de intenção de visita](assets/visit-intent-workspace.png)

Usei um espaço de trabalho simples para garantir que estava definindo bem meus segmentos de intenção de visita. Lembre-se de que cada visita precisa pertencer a um e somente a um segmento de Intenção de visita . O espaço de trabalho que eu configuro garante que todas as visitas sejam contabilizadas e que não haja sobreposição entre os segmentos.

Eu nomeei este espaço de trabalho como &quot;QUALIDADE DOS DADOS: Visite Segmentos de intenção de visita&quot; com as tags &quot;qualidade de dados&quot;, &quot;intenção de visita&quot; e &quot;jornada do cliente&quot;. Posteriormente, criaremos um &quot;Painel de intenção de visita&quot; para que o prefixo &quot;QUALIDADE DE DADOS&quot; indique que esse espaço de trabalho é para configuração e manutenção dos segmentos. É um painel administrativo que tem bastante pouco conhecimento comercial, mas é importante para garantir que os segmentos sejam mantidos. Convém retornar regularmente a este painel ou configurar alertas para garantir que seus segmentos permaneçam definidos corretamente.

A visualização mais importante nesse espaço de trabalho é a visualização de forma livre de Sobreposição de segmento no meio esquerdo. Usando a métrica Visitas , crie filtros de coluna para cada um dos segmentos de Intenção de visita, além do segmento Todas as visitas na coluna mais à direita. Crie linhas para cada segmento de Intenção de visita à esquerda. Agora você terá uma visualização entre guias. Quando seus segmentos são configurados corretamente, haverá somente dados em uma coluna e uma linha, na interseção de cada segmento de intenção de visita com ela mesma.

As próximas visualizações mais importantes são as métricas de resumo na parte superior esquerda. O resumo de Visitas segmentadas obtém seu valor a partir da coluna Todas as visitas na visualização Sobreposição de segmento imediatamente abaixo. O resumo Todas as visitas tem sua própria tabela oculta.

![todas as visitas](assets/all-visits.png)

No canto superior direito, adicionei métricas adicionais a cada um dos segmentos para dar algum &quot;sabor&quot; à forma como os segmentos estão se modelando. Especificamente, como esses segmentos são mutuamente exclusivos, espero apenas ver reservas do segmento de Intenção de Reserva (receio não, chegaremos às taxas de conversão quando fizermos esses segmentos de Intenção de Visita com base em visitantes.

Lembre-se de que acabamos de criar segmentos de espaço reservado. Então, inicialmente, seu espaço de trabalho parecerá maravilhoso. Todos os segmentos de intenção de visita se sobrepõem em 100%, pois têm a mesma definição. Isso está correto e é exatamente o que você quer ver neste ponto do processo. À medida que criamos as definições de segmentos, você começará a ver esses segmentos começarem a tomar forma.

![Definições de segmento de intenção de visita](assets/visit-intent-segment-defs.png)

## Criar seu primeiro segmento de intenção de visita

Definir segmentos de intenção de visita é um pouco um processo de eliminação, e há muita interdependência entre eles. Então eu não construí esses segmentos na ordem da jornada, eu os construí em ordem dos mais facilmente definidos para os mais desafiadores. Isso me deu este pedido:

1. Intenção: 0 - Maravilhas de uma ocorrência
1. Intenção: 3 - Reserva
1. Intenção: 4 - Retenção
1. Intenção: 2 - Consideração
1. Intenção: 1 - Sensibilização

Bem aleatório, não é? A definição desses segmentos de Intenção de visita foi um processo iterativo, de ida e volta e, geralmente, um ajuste para um segmento exigia atualizações para outros segmentos. Isso ficará mais claro conforme descrevo como defini cada um desses segmentos.

Hoje, definiremos nosso primeiro, e mais fácil, segmento, Uma Maravilha de Ocorrência

## Construção do segmento de ponteiros de uma ocorrência

Meu primeiro segmento, &quot;One Hit Wonders&quot;, foi fácil de definir. É simplesmente qualquer visita com apenas uma exibição de página. Nós realmente não sabemos por que esse usuário estava no site, porque ele retornou. Suponho que poderíamos adivinhar uma intenção baseada na página de entrada, mas com apenas uma exibição de página, não há informação suficiente para fazer uma suposição informada sobre a intenção.

![Definição de segmento](assets/segment-def.png)

Após definir esse segmento, você começará a ver sua área de trabalho de intenção de visita tomando forma.

![Mais definições de segmento](assets/more-segment-defs.png)

Construir segmentos de jornada do cliente usando o Adobe Analytics é um processo desafiador, mas gratificante. Ao criar segmentos baseados em comportamento, estimar o tamanho do público-alvo e rastrear os movimentos do usuário, as empresas podem personalizar a mídia e melhorar a experiência do cliente. Cada negócio é exclusivo e não há fórmulas específicas para criar segmentos, mas diretrizes e um processo a ser seguido. Os segmentos devem ser atualizados à medida que as empresas aprendem mais sobre seus clientes, o que apresenta desafios em relação aos relatórios. Ao seguir o processo de criação de segmentos de intenção de visita, as empresas podem melhorar a experiência geral do cliente.

## Autora

Este documento foi escrito por:

![Aaron Fossum](assets/aaron-headshot.png)

**Aaron Fossum**, Director, Digital Analytics

Especialista em Adobe Analytics


