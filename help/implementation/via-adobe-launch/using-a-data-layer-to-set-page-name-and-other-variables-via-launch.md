---
title: Use uma camada de dados para definir variáveis do Analytics por meio de tags
description: Saiba como usar uma camada de dados para fornecer dados do Analytics e outras soluções da Experience Cloud.
feature: Launch Implementation
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: 7224af1bd798d447f1b14c61e836f8e5c8af7ea4
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 96%

---

# Use uma camada de dados para definir variáveis do Analytics por meio de [!DNL Tags] {#use-a-data-layer-to-set-analytics-variables-in-adobe-analytics-via-tags}

O uso de uma camada de dados para o [!DNL Analytics] e outras soluções da Experience Cloud é uma prática recomendada. Neste vídeo, você verá como obter valores da camada de dados e usá-los no [!DNL Experience Platform Tags] para preencher variáveis no Adobe Analytics.

## Camadas de dados {#data-layers}

Uma _camada de dados_ é uma estrutura de objetos JavaScript que os desenvolvedores adicionam às páginas da Web digitais. As soluções do Analytics usam a camada de dados para preencher relatórios. Sistemas de gerenciamento de tags, incluindo [!DNL Experience Platform Tags]) são os intermediários que leem a camada de dados, mapeiam os valores para variáveis e enviam esses dados para soluções de experiência digital.

Revisar informações adicionais sobre camadas de dados no [Documentação do Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=pt-BR).

## Camadas de dados, [!DNL Experience Platform Tags] e Adobe Analytics{#data-layers-launch-and-adobe-analytics}

1. Defina ou identifique um padrão de camada de dados a ser usado no site.

   1. Posicione a camada de dados na parte superior possível do cabeçalho da página e antes da chamada para [!DNL Experience Platform Tags]. Isso garante que os valores sejam acessados imediatamente pelo [!DNL Tags] e por soluções da Adobe que precisam estar no topo da página, como o Adobe Target.

1. Preencha os dados na camada de dados.
1. No [!DNL Experience Platform Tags], crie “[!UICONTROL elementos de dados]” que mapeiam os pontos de dados na camada de dados. Esses elementos de dados são usados no [!DNL Experience Platform Tags] em [!UICONTROL regras] e [!UICONTROL extensões].
1. Na seção de variáveis globais de extensão do [!DNL Analytics] ou em um [!DNL Tags rule], atribua os valores em [!UICONTROL elementos de dados] para [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] e outras variáveis [!DNL Analytics].
1. Acionar um sinal que envia os dados para o [!DNL Analytics].

O vídeo a seguir o orienta pelo processo.

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>A camada de dados específica usada neste vídeo pode não ser considerada uma “prática recomendada” para sua organização. O conceito de usar uma camada de dados para encontrar dados importantes em suas soluções de marketing digital é uma prática recomendada.