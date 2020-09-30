---
title: Ações de rastreamento (links personalizados AKA) em um aplicativo móvel com o SDK do Experience Platform
description: 'As ações são eventos que ocorrem no aplicativo móvel. Neste vídeo, saiba como usar a API trackAction para rastrear e medir uma ação. '
feature: mobile sdk
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2563
translation-type: tm+mt
source-git-commit: a42658cfd4bae7b077ddd48b4cf5c7db54e35c98
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# Ações de rastreamento (links personalizados AKA) em um aplicativo móvel com o SDK do Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

As ações são eventos que ocorrem no aplicativo móvel. Neste vídeo, saiba como usar a API trackAction para rastrear e medir uma ação.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Esta é a API que você deve usar para rastrear todas as ações que não são carregadas na tela do seu site. Se a tela estiver aparecendo, use trackState, que dispara uma ocorrência de visualização de página. Caso contrário, use trackAction para enviar variáveis associadas à ação que está ocorrendo.

Esses dados entram como `contextData`, o que também significa que você precisará usar as Regras [!UICONTROL de] processamento para obter os dados móveis dessas `contextData` variáveis e mapeá-los para [!DNL eVars], [!DNL Props], Eventos etc. no Adobe Analytics.

Para obter mais informações sobre trackAction, consulte a [documentação](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
