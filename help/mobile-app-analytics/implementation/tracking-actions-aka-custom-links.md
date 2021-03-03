---
title: Rastreamento de ações (links personalizados do AKA) em um aplicativo móvel com o SDK da Experience Platform
description: 'As ações são eventos que ocorrem no aplicativo móvel. Neste vídeo, saiba como usar a API trackAction para rastrear e medir uma ação. '
feature: SDK móvel
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Dispositivo móvel
role: '"Desenvolvedor, engenheiro de dados"'
level: Experienciado
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---


# Rastreamento de ações (links personalizados do AKA) em um aplicativo móvel com o SDK da Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

As ações são eventos que ocorrem no aplicativo móvel. Neste vídeo, saiba como usar a API trackAction para rastrear e medir uma ação.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Essa é a API que você deve usar para rastrear todas as ações que não são de carregamento de tela no site. Se a tela estiver chegando, use trackState, que aciona uma ocorrência de exibição de página. Caso contrário, use trackAction para enviar variáveis associadas à ação que está acontecendo.

Esses dados vêm como `contextData`, o que também significa que você precisará usar [!UICONTROL Regras de processamento] para obter os dados móveis dessas variáveis `contextData` e mapeá-los para [!DNL eVars], [!DNL Props], Eventos etc. no Adobe Analytics.

Para obter mais informações sobre trackAction, consulte a [documentação](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
