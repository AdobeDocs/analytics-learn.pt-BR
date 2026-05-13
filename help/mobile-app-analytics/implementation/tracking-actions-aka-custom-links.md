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
role: Developer
level: Experienced
exl-id: 541c51b8-638e-43b4-90ac-0ce94290a141
TQID: https://experienceleague.adobe.com/msvft7mQiNGjLqGEezPIbwruvSbsunPGUIFF1q7vlT0
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b3f03848-ae12-48b2-8aab-cad18567eb32id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: f1f1a2d4-0976-4881-b091-c2bb8de7ffac
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 73%

---

# Rastreamento de ações (também conhecido como Links personalizados) em um aplicativo móvel com o SDK da Experience Platform {#tracking-actions-aka-custom-links-in-a-mobile-app-with-the-experience-platform-sdk}

Ações são eventos que ocorrem no aplicativo móvel. Neste vídeo, saiba como usar a API trackAction para rastrear e medir uma ação.

>[!VIDEO](https://video.tv.adobe.com/v/26268/?quality=12&learn=on)

Esta é a API que você deve usar para rastrear todas as ações que não são carregadas na tela do seu site. Se a tela estiver aparecendo, use trackState, que aciona um hit de exibição de página. Caso contrário, use trackAction para enviar variáveis associadas à ação que está ocorrendo.

Esses dados entram como `contextData`, o que também significa que você precisará usar [!UICONTROL Regras de processamento] para obter os dados móveis dessas `contextData` variáveis e mapeá-los para [!DNL eVars], [!DNL Props], Eventos etc. no Adobe Analytics.

Para obter mais informações sobre trackAction, consulte a [documentação](https://developer.adobe.com/client-sdks/documentation/getting-started/track-events/#track-user-actions-for-adobe-analytics).
