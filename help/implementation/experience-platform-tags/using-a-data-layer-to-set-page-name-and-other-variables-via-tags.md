---
title: Use uma camada de dados para definir variáveis do Analytics no Experience Platform [!DNL tags]
description: Saiba como usar uma camada de dados para fornecer dados do Analytics e outras soluções de Experience Cloud.
feature: Tags
topics: Development
role: Developer, Data Engineer
level: Beginner
kt: 1852
thumbnail: 25899.jpg
exl-id: 408ceb47-df05-4456-85bb-0ef2798a05a5
source-git-commit: a45667a8d7ccb46b9e33bd11a78fac9714a61df5
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 50%

---

# Use uma camada de dados para definir variáveis do Analytics no Experience Platform [!DNL tags]

O uso de uma camada de dados para o [!DNL Analytics] e outras soluções da Experience Cloud é uma prática recomendada. Neste vídeo, saiba como obter valores da camada de dados e usá-los no Experience Platform [!DNL tags] para preencher variáveis no Adobe Analytics.

## Camadas de dados

Uma _camada de dados_ é uma estrutura de objetos JavaScript que os desenvolvedores adicionam às páginas da Web digitais. As soluções do Analytics usam a camada de dados para preencher relatórios. Sistemas de gerenciamento de tags, incluindo o Experience Platform [!DNL tags]) são os intermediários que leem a camada de dados, mapeiam os valores para variáveis e enviam esses dados para soluções de experiência digital.

Revisar informações adicionais sobre camadas de dados no [Documentação do Experience Cloud](https://experienceleague.adobe.com/docs/analytics/implementation/prepare/data-layer.html?lang=pt-BR).

## Camadas de dados, Experience Platform [!DNL tags], e ADOBE ANALYTICS

1. Defina ou identifique um padrão de camada de dados a ser usado no site.

   1. Posicione a camada de dados na parte superior possível do cabeçalho da página e antes da chamada para o Experience Platform [!DNL tags]. Isso garante que os valores sejam acessados imediatamente pelo [!DNL tags] e por soluções da Adobe que precisam estar no topo da página, como o Adobe Target.

1. Preencha os dados na camada de dados.
1. No Experience Platform [!DNL tags], criar &quot;[!UICONTROL elementos de dados]&quot; que mapeiam os pontos de dados na camada de dados. Esses elementos de dados são usados no Experience Platform [!DNL tags] in [!UICONTROL regras] e [!UICONTROL extensões].
1. Na seção de variáveis globais de extensão do [!DNL Analytics] ou em um [!DNL Tags rule], atribua os valores em [!UICONTROL elementos de dados] para [!UICONTROL props], [!UICONTROL eVars], [!UICONTROL pageName] e outras variáveis [!DNL Analytics].
1. Acionar um sinal que envia os dados para o [!DNL Analytics].

O vídeo a seguir o orienta pelo processo.

>[!NOTE]
>
> O Launch agora está **[!DNL tags]**

>[!VIDEO](https://video.tv.adobe.com/v/25899/?quality=12&learn=on)

>[!NOTE]
>
>A camada de dados específica usada neste vídeo pode não ser considerada uma “prática recomendada” para sua organização. O conceito de usar uma camada de dados para encontrar dados importantes em suas soluções de marketing digital é uma prática recomendada.
