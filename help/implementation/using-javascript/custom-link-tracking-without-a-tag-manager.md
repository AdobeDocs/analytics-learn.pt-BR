---
title: Rastreamento de link personalizado sem um gerenciador de tags
description: Para muitas ações na página, o rastreamento não deve ser tratado como uma exibição de página. Neste vídeo, você aprenderá a codificar um beacon de rastreamento de link no Analytics, se não estiver usando um gerenciador de tags (como o Experience Platform Launch). Consulte o código, bem como aprenda uma dica importante.
feature: Implementação Do Appmeasurement
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1845
role: '"Desenvolvedor, engenheiro de dados"'
level: Intermediário
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 4%

---


# Rastreamento de link personalizado sem um Gerenciador de tags {#custom-link-tracking-without-a-tag-manager}

Para muitas ações na página, o rastreamento não deve ser tratado como uma exibição de página. Neste vídeo, você aprenderá a codificar um beacon de rastreamento de link no Analytics, se não estiver usando um gerenciador de tags (como Adobe [!DNL Experience Platform Launch]). Consulte o código, bem como aprenda uma dica importante.

## Envio de um s.tl() Beacon {#sending-an-s-tl-beacon}

Há duas funções que enviam dados para o Adobe Analytics:

1. s.t() - Um sinal de &quot;rastreamento&quot;, que é uma ocorrência de exibição de página, incrementando exibições de página para o nome de página fornecido, bem como definindo outras variáveis
1. s.tl() - um beacon de &quot;rastreamento de link&quot;, que geralmente é chamado de hit/beacon de &quot;link personalizado&quot;, que não incrementa as exibições de página e ignora a variável pageName . Isso é comumente usado para rastrear ações menores na página que não carregam uma nova página/tela ou outras ações que não resultam em um novo carregamento da página.

>[!NOTE]
>
>Neste vídeo, mostramos como codificar uma ocorrência de link personalizado quando VOCÊ NÃO está usando um gerenciador de tags como o Adobe [!DNL Experience Platform Launch]. Recomendamos que você use [!DNL Experience Platform Launch], nossa recomendação de práticas recomendadas para implementação. No entanto, se precisar codificar em um `s.tl()`, veja a seguir como fazer isso.

>[!VIDEO](https://video.tv.adobe.com/v/25832/?quality=12)

## Código de exemplo {#sample-code}

Este é o código de amostra usado no link personalizado do vídeo:

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