---
title: Rastreamento de ações (também conhecido como Links personalizados) em um aplicativo móvel com o SDK da Experience Platform
description: Ações são eventos que ocorrem no aplicativo móvel. Neste vídeo, saiba como usar a API trackAction para rastrear e medir uma ação.
feature: Mobile SDK
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
topic: Mobile
role: Developer, Data Engineer
level: Experienced
exl-id: 541c51b8-638e-43b4-90ac-0ce94290a141
source-git-commit: 4d467928756950074620388645523021b21fb0d5
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 99%

---

# Rastreamento de ações (também conhecido como Links personalizados) em um aplicativo móvel com o SDK da Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Ações são eventos que ocorrem no aplicativo móvel. Neste vídeo, saiba como usar a API trackAction para rastrear e medir uma ação.

>[!VIDEO](https://video.tv.adobe.com/v/328310/?quality=12&learn=on&captions=por_br)

Esta é a API que você deve usar para rastrear todas as ações que não são carregadas na tela do seu site. Se a tela estiver aparecendo, use trackState, que aciona um hit de exibição de página. Caso contrário, use trackAction para enviar variáveis associadas à ação que está ocorrendo.

Esses dados entram como `contextData`, o que também significa que você precisará usar [!UICONTROL Regras de processamento] para obter os dados móveis dessas variáveis `contextData` e mapeá-los para [!DNL eVars], [!DNL Props], Eventos etc. no Adobe Analytics.

Para obter mais informações sobre trackAction, consulte a [documentação](https://developer.adobe.com/client-sdks/documentation/getting-started/track-events/#track-user-actions-for-adobe-analytics).
