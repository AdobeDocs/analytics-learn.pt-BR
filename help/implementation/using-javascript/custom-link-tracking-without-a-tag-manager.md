---
title: Rastreamento de link personalizado sem um Gerenciador de tags
description: Para muitas ações na página, o rastreamento não deve ser tratado como uma exibição de página. Neste vídeo, você aprenderá a codificar um beacon de rastreamento de link no Analytics, se não estiver usando um gerenciador de tag (como o Experience Platform Launch). Consulte o código e aprenda uma dica importante.
feature: Appmeasurement Implementation
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: Developer
level: Intermediate
exl-id: e4567b1c-414e-44ad-982f-52b0150e7eda
TQID: https://experienceleague.adobe.com/BU98KM1JAq3v6Gd7SRU0FNT3qW-4a9UvP0M-ffFqJIA
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 100%

---

# Rastreamento de link personalizado sem um Gerenciador de tags {#custom-link-tracking-without-a-tag-manager}

Para muitas ações na página, o rastreamento não deve ser tratado como uma exibição de página. Neste vídeo, você aprenderá a codificar um beacon de rastreamento de link no Analytics, se não estiver usando um gerenciador de tag (como o Adobe [!DNL Experience Platform Launch]). Consulte o código e aprenda uma dica importante.

## Envio de um beacon s.tl() {#sending-an-s-tl-beacon}

Há duas funções que enviam dados para o Adobe Analytics:

1. s.t() - Um beacon “track” que é uma ocorrência de exibição de página que incrementa exibições de página para o nome de página fornecido e define outras variáveis
1. s.tl() - um beacon “track link”, geralmente chamado de ocorrência/beacon de “link personalizado”, que não incrementa as exibições de página e ignora a variável pageName. Isso é comumente usado para rastrear ações menores na página que não carregam uma nova página/tela ou outras ações que não resultam em um novo carregamento da página.

>[!NOTE]
>
>Neste vídeo, mostramos como codificar uma ocorrência de link personalizado quando você NÃO está usando um gerenciador de tag como o Adobe [!DNL Experience Platform Launch]. Recomendamos que você use o [!DNL Experience Platform Launch], nossa sugestão de práticas recomendadas para implementação. No entanto, se você precisar codificar em um `s.tl()`, veja como fazer isso.

>[!VIDEO](https://video.tv.adobe.com/v/34662/?captions=por_br&quality=12&learn=on)

## Código de exemplo {#sample-code}

Este é o código de exemplo usado no link personalizado do vídeo:

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
