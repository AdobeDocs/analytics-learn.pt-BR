---
title: Uso de uma camada de dados para definir o Nome da página e Outras variáveis no Adobe Analytics por meio do Launch
description: O uso de uma camada de dados para o Analytics e outras soluções da Experience Cloud é considerado uma prática recomendada. Neste vídeo, você verá como extrair seus valores da camada de dados e usá-los no Launch para preencher variáveis no Adobe Analytics.
feature: Implementação do Launch
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1852
role: '"Desenvolvedor, engenheiro de dados"'
level: Iniciante
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 4%

---


# Uso de uma camada de dados para definir o Nome da página e Outras variáveis via [!DNL Experience Platform Launch] {#using-a-data-layer-to-set-page-name-and-other-variables-in-adobe-analytics-via-launch}

O uso de uma camada de dados para [!DNL Analytics] e outras soluções da Experience Cloud é considerado uma prática recomendada. Neste vídeo, você verá como extrair seus valores da camada de dados e usá-los em [!DNL Experience Platform Launch] para preencher variáveis no Adobe Analytics.

## Camadas de dados {#data-layers}

É uma prática recomendada usar uma camada de dados ao trabalhar com dados no seu site e nas soluções da Adobe Experience Cloud, especialmente com o Adobe Analytics. Uma _camada de dados_ é uma estrutura de objetos JavaScript que os desenvolvedores inserem nas páginas. As camadas de dados podem ser usadas pelas ferramentas de rastreamento (incluindo sistemas de Tag Management como [!DNL Experience Platform Launch]) para preencher relatórios. Encontre informações adicionais sobre camadas de dados na [documentação da Experience Cloud](https://marketing.adobe.com/resources/help/en_US/sc/implement/ref-data-layer.html) ou no [site W3C](https://www.w3.org/).

Além disso, consulte o blog [Camadas de dados: De chavão a práticas recomendadas,](https://theblog.adobe.com/data-layers-buzzword-best-practice/), que fornece algumas informações importantes sobre camadas de dados, bem como alguns exemplos.

## Camadas de dados, [!DNL Experience Platform Launch] e Adobe Analytics (oh my?){#data-layers-launch-and-adobe-analytics-oh-my}

1. Crie uma camada de dados padrão para usar no site, que pode ser referenciada por [!DNL Experience Platform Launch].

   1. Coloque essa camada de dados a mais alta possível no cabeçalho da página, antes da chamada para [!DNL Experience Platform Launch], para que os valores possam ser usados imediatamente por [!DNL Launch] e pelas soluções da Adobe que precisam estar em alta na página, como o Adobe Target.

1. Preencha os dados na camada de dados.
1. Em [!DNL Experience Platform Launch], crie &quot;[!UICONTROL elementos de dados]&quot; que façam referência aos pontos de dados na camada de dados e que possam ser usados em [!DNL Experience Platform Launch] em [!UICONTROL rules], [!UICONTROL extensions], e assim por diante.
1. Use os [!UICONTROL elementos de dados] nas variáveis globais da extensão [!DNL Analytics] ou em uma regra, atribuindo os valores em [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] ou outras variáveis [!DNL Analytics].
1. Acione um sinal que envie os dados para [!DNL Analytics].

O vídeo a seguir o orienta pelo processo.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12)
