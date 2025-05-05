---
title: Agora aguarde um segmento... Usando a segmentação para descobrir novos insights no Analysis Workspace
description: Saiba como usar segmentos no Adobe Analytics para descobrir novos insights das visualizações e tabelas de forma livre do Analysis Workspace.
feature: Segmentation
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13268
thumbnail: KT-13268.jpeg
exl-id: 7743debd-57d8-4c79-a332-187180fc9701
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '812'
ht-degree: 1%

---

# Agora aguarde um segmento... Usando segmentos para descobrir novos insights no Analysis Workspace

Se você for um novo usuário do Adobe Analytics ou um profissional experiente, aproveitará os segmentos bastante nos projetos do Analysis Workspace. Como [Adobe Experience League](https://experienceleague.adobe.com/docs/analytics/components/segmentation/seg-overview.html?lang=pt-BR) descreve, &quot;os segmentos permitem identificar subconjuntos de visitantes com base em características ou interações de site.&quot; Embora o resultado básico desse recurso signifique isolar grupos de usuários, visitas ou ocorrências em seu site, um analista perspicaz como você pode se tornar criativo com essa ferramenta e encontrar novas maneiras de obter insights sobre a atividade do site. A lista de opções possíveis é ampla, portanto, não hesite em criar a sua própria e compartilhá-la com outras pessoas na sua organização ou online em comunidades como a [Comunidade Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?profile.language=pt) no Experience League ou a comunidade [#Measure Slack](https://www.measure.chat/).

Se você precisar de uma atualização rápida sobre como criar um segmento, consulte a documentação do Experience League sobre como usar o [Construtor de segmentos](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html?lang=pt-BR) no Analysis Workspace.

## Comparação e contraste de segmentos

No Analysis Workspace, você pode comparar dois segmentos usando &quot;[Comparação de segmentos](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/panels/segment-comparison/segment-comparison.html?lang=pt-BR)&quot;. A comparação de segmentos pode ser encontrada na seção Painéis da barra de navegação à esquerda:

![Seg 01](assets/seg01.png)

No entanto, às vezes, você não precisa de um painel completo de comparação para transmitir os principais insights para os usuários finais. Felizmente, alguns recursos também podem ser comparados em um painel padrão.

A [visualização do diagrama de Venn](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/visualizations/venn.html?lang=pt-BR) pode ajudar a criar uma comparação rápida, permitindo que você passe o mouse e veja as sessões, pedidos, usuários sobrepostos, etc. que se sobrepõem. entre 2 e 3 segmentos personalizados. Você também pode criar segmentos rapidamente clicando com o botão direito do mouse em qualquer uma das seções sobrepostas:

![Seg 02](assets/s02.png)

Às vezes, as informações importantes não estão nos dados sobrepostos, mas nos dados que não se sobrepõem. Uma maneira rápida de visualizar isso é criar uma cópia de um segmento e torná-la um segmento &quot;Excluir&quot;:

![Seg 03](assets/s03.png)

Ao empilhar o segmento &quot;excluir&quot; com o outro segmento na comparação, agora é possível calcular rapidamente quantas visitas acessam a página de menu sem exibir a página inicial na mesma sessão:

![Seg 04](assets/s04.png)

## Empilhar Ataque

Da mesma forma, é possível criar os dados de interseção de um diagrama de Venn simplesmente empilhando os segmentos. Não há limite para quantos segmentos ou dimensões individuais você empilha. Por exemplo, se eu quisesse descobrir rapidamente quais Dias da Semana no mês passado meu site tinha uma visita em um celular, especificamente um Samsung Galaxy A52s, que viu meu menu e páginas de nutrição, mas NÃO viu minha página inicial, posso criá-lo rapidamente assim:

![Seg 05](assets/s05.png)

Mas ainda melhor, uma vez que encontre esse subconjunto perfeito de meu usuário ou base de visitas, posso selecionar todos esses valores, clicar com o botão direito do mouse e criar um segmento instantaneamente:

![Seg 06](assets/s06.png)

![Seg 07](assets/s07.png)

![Seg 08](assets/s08.png)

Isso é muito poder em um segmento.

## Um segmento de números para um número de segmentos

Muitos usuários geralmente observam valores nominais, ordinais ou de intervalo ao criar segmentos, como uma página visitada, um intervalo de idade de usuários ou o número de visitas que um usuário fez no passado. No entanto, você também pode usar os dados de proporção ao criar um segmento, classificando esses valores, sejam eles dimensões padrão, métricas padrão ou variáveis e métricas personalizadas para sua organização.

Por exemplo, Tempo gasto na página ou Tempo gasto por visita tem compartimentos pré-criados disponíveis:

![Seg 09](assets/s09.png)

No entanto, elas nem sempre se encaixam nas necessidades da organização. Talvez a maioria das visitas do site seja executada por menos de 10 minutos. Você pode usar a medição granular para criar compartimentos de tamanhos diferentes. Este é um criado para analisar visitas que duram entre 1 minuto, 1 segundo e 1 minuto, 30 segundos:

![Seg 10](assets/s10.png)

Depois de criado, agora posso ver minhas visitas, pedidos e outros eventos pelos diferentes grupos de tempo segmentados que personalizei:

![Seg 11](assets/s11.png)

Você pode até começar a examinar como os Indicadores-chave de desempenho (KPIs) mudam como um fator do tempo que um usuário gasta, quantas páginas ele acessou em uma visita, quantas vezes eles visitaram no passado ou qualquer outro valor numérico - basicamente, permitindo que você veja uma métrica como um fator de outra métrica:

![Seg 12](assets/s12.png)

As possibilidades de usar segmentos para encontrar novos insights são infinitas! Isto é simplesmente um ponto de partida. Experimente alguns por conta própria e informe à comunidade o que você descobriu: [Comunidade do Adobe Analytics](https://experienceleaguecommunities.adobe.com/t5/adobe-analytics/ct-p/adobe-analytics-community?profile.language=pt) no Experience League ou na comunidade [#Measure Slack](https://www.measure.chat/).

Segmentação feliz!

## Autora

Este documento foi escrito por:

![Dan Cummings](assets/seg13.png)

**Dan Cummings**, Gerente sênior de análise de engenharia de produtos na McDonald&#39;s Corporation

Especialista no Adobe Analytics
