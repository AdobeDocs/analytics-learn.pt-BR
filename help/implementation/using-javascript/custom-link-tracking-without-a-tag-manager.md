---
title: Rastreamento de link personalizado sem um Gerenciador de tags
description: Para muitas ações na página, o rastreamento não deve ser tratado como uma visualização de página. Neste vídeo, você aprenderá a codificar um beacon de rastreamento de link no Analytics, se não estiver usando um gerenciador de tags (como o Experience Platform Launch). Consulte o código, bem como aprenda uma dica importante.
feature: appmeasurement implementation
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
translation-type: tm+mt
source-git-commit: 8276828e9e759a1964ca5ea89bb1395e5e78b500
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 4%

---


# Rastreamento de link personalizado sem um Gerenciador de tags {#custom-link-tracking-without-a-tag-manager}

Para muitas ações na página, o rastreamento não deve ser tratado como uma visualização de página. Neste vídeo, você aprenderá a codificar um beacon de rastreamento de link no Analytics, se não estiver usando um gerenciador de tags (como o Adobe [!DNL Experience Platform Launch]). Consulte o código, bem como aprenda uma dica importante.

## Envio de um beacon s.tl() {#sending-an-s-tl-beacon}

Há duas funções que enviam dados para o Adobe Analytics:

1. s.t() - Um beacon &quot;track&quot;, que é uma ocorrência de visualização de página, que aumenta as visualizações de página para o nome de página fornecido, bem como define outras variáveis
1. s.tl() - um beacon de &quot;link de rastreamento&quot;, frequentemente chamado de hit/beacon de &quot;link personalizado&quot;, que não incrementa visualizações de página, e ignora a variável pageName. Normalmente, isso é usado para rastrear ações menores na página que não carregam uma nova página/tela ou outras ações que não resultam em um novo carregamento de página.

>[!NOTE]
>
>Neste vídeo, mostramos como codificar uma ocorrência de link personalizado quando VOCÊ NÃO está usando um gerenciador de tags como Adobe [!DNL Experience Platform Launch]. Recomendamos que você use [!DNL Experience Platform Launch], nossa recomendação de práticas recomendadas para implementação. No entanto, se você precisar codificar em um `s.tl()`, veja como fazer isso.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12)

## Código de exemplo {#sample-code}

Este é o exemplo de código usado no link personalizado no vídeo:

```JavaScript
<a href="#" onclick="
    s.linkTrackVars='events,eVar2,prop2';
    s.linkTrackEvents=s.events='event2';
    s.eVar2='facebook share';
    s.prop2='facebook share';
    s.tl(this,'o','Social Share');
    s.manageVars('clearVars',s.linkTrackVars,1);">
    Click here to share on FaceBook
</a>
```

Para obter mais informações sobre links personalizados, consulte a [documentação](https://marketing.adobe.com/resources/help/pt_BR/sc/implement/function_tl.html).