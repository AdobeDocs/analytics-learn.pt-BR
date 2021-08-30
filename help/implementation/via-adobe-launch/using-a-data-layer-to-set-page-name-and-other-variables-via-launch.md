---
title: Uso de uma camada de dados para definir o Nome da página e Outras variáveis no Adobe Analytics por meio do Launch
description: O uso de uma camada de dados para o Analytics e outras soluções do Experience Cloud é considerado uma prática recomendada. Neste vídeo, você verá como extrair seus valores da camada de dados e usá-los no Launch para preencher variáveis no Adobe Analytics.
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
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 7%

---

# Utilização de uma camada de dados para definir o Nome da página e outras variáveis por meio do [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

O uso de uma camada de dados para [!DNL Analytics] e outras soluções do Experience Cloud é considerado uma prática recomendada. Neste vídeo, você verá como extrair seus valores da camada de dados e usá-los em [!DNL Experience Platform Launch] para preencher variáveis no Adobe Analytics.

## Camadas de dados {#data-layers}

É uma prática recomendada usar uma camada de dados ao trabalhar com dados no site e nas soluções da Adobe Experience Cloud, especialmente com o Adobe Analytics. Uma _camada de dados_ é uma estrutura de objetos JavaScript que os desenvolvedores inserem nas páginas. As camadas de dados podem ser usadas pelas ferramentas de rastreamento (incluindo sistemas de Tag Management como [!DNL Experience Platform Launch]) para preencher relatórios. Encontre informações adicionais sobre camadas de dados na [documentação do Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=en) ou no [site W3C](https://www.w3.org/).

Além disso, consulte o blog [Camadas de dados: De chavão a práticas recomendadas,](https://theblog.adobe.com/data-layers-buzzword-best-practice/), que fornece algumas informações importantes sobre camadas de dados, bem como alguns exemplos.

## Camadas de dados, [!DNL Experience Platform Launch] e Adobe Analytics (oh meu?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Crie uma camada de dados padrão para usar no site, que pode ser referenciada por [!DNL Experience Platform Launch].

   1. Coloque essa camada de dados a mais alta possível no cabeçalho da página, antes da chamada para [!DNL Experience Platform Launch], para que os valores possam ser usados imediatamente por [!DNL Launch] e por soluções de Adobe que precisam estar em alta na página, como o Adobe Target.

1. Preencha os dados na camada de dados.
1. Em [!DNL Experience Platform Launch], crie &quot;[!UICONTROL elementos de dados]&quot; que façam referência aos pontos de dados na camada de dados e que possam ser usados em [!DNL Experience Platform Launch] em [!UICONTROL rules], [!UICONTROL extensions], e assim por diante.
1. Use os [!UICONTROL elementos de dados] nas variáveis globais da extensão [!DNL Analytics] ou em uma regra, atribuindo os valores em [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] ou outras variáveis [!DNL Analytics].
1. Acione um sinal que envie os dados para [!DNL Analytics].

O vídeo a seguir o orienta pelo processo.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
