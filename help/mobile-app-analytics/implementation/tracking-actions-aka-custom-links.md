---
title: Rastreamento de ações (também conhecido como Links personalizados) em um aplicativo móvel com o SDK da Experience Platform
description: 'Ações são eventos que ocorrem no aplicativo móvel. Neste vídeo, saiba como usar a API trackAction para rastrear e medir uma ação. '
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
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: ht
source-wordcount: '174'
ht-degree: 100%

---

# Rastreamento de ações (também conhecido como Links personalizados) em um aplicativo móvel com o SDK da Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Ações são eventos que ocorrem no aplicativo móvel. Neste vídeo, saiba como usar a API trackAction para rastrear e medir uma ação.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12)

Esta é a API que você deve usar para rastrear todas as ações que não são carregadas na tela do seu site. Se a tela estiver aparecendo, use trackState, que aciona um hit de exibição de página. Caso contrário, use trackAction para enviar variáveis associadas à ação que está ocorrendo.

Esses dados entram como `contextData`, o que também significa que você precisará usar [!UICONTROL Regras de processamento] para obter os dados móveis dessas variáveis `contextData` e mapeá-los para [!DNL eVars], [!DNL Props], Eventos etc. no Adobe Analytics.

Para obter mais informações sobre trackAction, consulte a [documentação](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/configuration-reference/mobile-core-api-reference).
