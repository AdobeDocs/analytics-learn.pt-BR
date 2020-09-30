---
title: Uso de uma camada de dados para definir o Nome da página e Outras variáveis no Adobe Analytics por meio do Launch
description: O uso de uma camada de dados para o Analytics e outras soluções de Experience Cloud é considerado uma prática recomendada. Neste vídeo, você verá como extrair seus valores da camada de dados e usá-los no Launch para preencher variáveis no Adobe Analytics.
feature: launch implementation
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
translation-type: tm+mt
source-git-commit: ee6c03cff5b051d9293d75965e9fd98f151d7fce
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 4%

---


# Usando uma camada de dados para definir o Nome da página e Outras variáveis por meio de [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

O uso de uma camada de dados para [!DNL Analytics] e outras soluções de Experience Cloud é considerado uma prática recomendada. Neste vídeo, você verá como extrair seus valores da camada de dados e usá-los para preencher variáveis no Adobe Analytics [!DNL Experience Platform Launch] .

## Camadas de dados {#data-layers}

É uma prática recomendada usar uma camada de dados ao trabalhar com dados em seu site e com soluções Adobe Experience Cloud, especialmente com a Adobe Analytics. Uma _camada de dados_ é uma estrutura de objetos JavaScript que os desenvolvedores inserem nas páginas. The data layers can be used by tracking tools (including tag management systems like [!DNL Experience Platform Launch]) to populate reports. Encontre informações adicionais sobre camadas de dados na documentação [do](https://marketing.adobe.com/resources/help/en_US/sc/implement/ref-data-layer.html) Experience Cloud ou no site [](https://www.w3.org/)W3C.

Além disso, consulte o blog Camadas [de dados: Do Buzzword à Prática recomendada,](https://theblog.adobe.com/data-layers-buzzword-best-practice/)o que fornece algumas excelentes informações sobre camadas de dados, bem como alguns exemplos.

## Camadas de dados [!DNL Experience Platform Launch]e Adobe Analytics (oh my?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Crie um padrão de camada de dados para usar em seu site, que pode ser referenciado por [!DNL Experience Platform Launch].

   1. Coloque essa camada de dados o mais alto possível no cabeçalho da página, antes da chamada para [!DNL Experience Platform Launch], para que os valores possam ser usados imediatamente por [!DNL Launch]e por soluções de Adobe que precisam estar em alta na página, como a Adobe Target.

1. Preencha os dados na camada de dados.
1. Em [!DNL Experience Platform Launch], crie &quot;elementos[!UICONTROL de]dados&quot; que façam referência aos pontos de dados na camada de dados e que possam ser usados [!DNL Experience Platform Launch] em [!UICONTROL regras], [!UICONTROL extensões]e assim por diante.
1. Use os elementos [!UICONTROL de] dados nas variáveis globais de [!DNL Analytics] extensão ou em uma regra, atribuindo os valores a [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName]ou outras [!DNL Analytics] variáveis.
1. Acione um sinal que envie os dados para [!DNL Analytics].

O vídeo a seguir o orienta pelo processo.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
