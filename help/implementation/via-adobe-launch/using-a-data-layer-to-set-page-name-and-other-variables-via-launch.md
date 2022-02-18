---
title: Utilização de uma camada de dados para definir o nome da página e outras variáveis no Adobe Analytics por meio do Launch
description: O uso de uma camada de dados para o Analytics e outras soluções da Experience Cloud é considerado uma prática recomendada. Neste vídeo, você verá como obter seus valores da camada de dados e usá-los no Launch para preencher variáveis no Adobe Analytics.
feature: Launch Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: Developer, Data Engineer
level: Beginner
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: fe861dfd541c1b9cb3b233fa3f56d55054305fd9
workflow-type: ht
source-wordcount: '365'
ht-degree: 100%

---

# Utilização de uma camada de dados para definir o nome da página e outras variáveis por meio do [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

O uso de uma camada de dados para o [!DNL Analytics] e outras soluções da Experience Cloud é considerado uma prática recomendada. Neste vídeo, você verá como obter seus valores da camada de dados e usá-los no [!DNL Experience Platform Launch] para preencher variáveis no Adobe Analytics.

## Camadas de dados {#data-layers}

É uma prática recomendada usar uma camada de dados ao trabalhar com dados no site e nas soluções da Adobe Experience Cloud, especialmente com o Adobe Analytics. Uma _camada de dados_ é uma estrutura de objetos JavaScript que os desenvolvedores inserem nas páginas. As camadas de dados podem ser usadas pelas ferramentas de rastreamento (incluindo sistemas de gerenciamento de tags, como [!DNL Experience Platform Launch]) para preencher relatórios. Encontre informações adicionais sobre camadas de dados na [documentação da Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=pt-BR) ou no [site da W3C](https://www.w3.org/).

Além disso, consulte o blog [Camadas de dados: de tendência a prática recomendada,](https://theblog.adobe.com/data-layers-buzzword-best-practice/), que fornece informações excelentes sobre camadas de dados, bem como alguns exemplos.

## Camadas de dados, [!DNL Experience Platform Launch] e Adobe Analytics {#data-layers-launch-and-adobe-analytics-oh-my}

1. Crie uma camada de dados padrão para usar no site, que pode ser referenciada pelo [!DNL Experience Platform Launch].

   1. Coloque essa camada de dados o mais alto possível no cabeçalho da página, antes da chamada para o [!DNL Experience Platform Launch], para que os valores possam ser usados imediatamente pelo [!DNL Launch] e pelas soluções da Adobe que precisam estar no topo da página, como o Adobe Target.

1. Preencha os dados na camada de dados.
1. No [!DNL Experience Platform Launch], crie &quot;[!UICONTROL elementos de dados]&quot; que fazem referência aos pontos de dados na camada de dados e que podem ser usados no [!DNL Experience Platform Launch] nas [!UICONTROL regras], [!UICONTROL extensões] e assim por diante.
1. Use os [!UICONTROL elementos de dados] em qualquer uma das variáveis globais de extensão do [!DNL Analytics] ou em uma regra, atribuindo os valores a [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] ou outras variáveis do [!DNL Analytics].
1. Acionar um sinal que envia os dados para o [!DNL Analytics].

O vídeo a seguir o orienta pelo processo.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
