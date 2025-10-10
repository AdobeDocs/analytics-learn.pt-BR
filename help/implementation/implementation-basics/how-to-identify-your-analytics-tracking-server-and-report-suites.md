---
title: Como identificar o servidor de rastreamento da análise e a ID de conjunto de relatórios
description: Ao configurar o Adobe Analytics ou referenciá-lo em outras soluções da Experience Cloud, muitas vezes é útil (ou até necessário) saber qual “servidor de rastreamento” do Analytics você está usando, bem como o “conjunto de relatórios” para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado o Adobe Analytics ou não.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer, Data Engineer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 42bf16df9585d1f41206b81bf509a72c10f1d7f2
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 100%

---

# Como identificar o [!DNL tracking server] da análise e a [!UICONTROL ID de conjunto de relatórios] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Ao configurar o Adobe Analytics ou referenciá-lo em outras soluções da Experience Cloud, muitas vezes é útil (ou até necessário) saber qual “servidor de rastreamento” do Analytics você está usando, bem como o “[!UICONTROL conjunto de relatórios]” para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado o Adobe Analytics ou não.

>[!IMPORTANT]
>
>Este artigo e vídeo se aplicam a uma implementação de “AppMeasurement” do Adobe Analytics, e não a uma implementação que utiliza o SDK da web.

## Após a implementação {#after-implementation}

Depois de implementar o Analytics em um site, você pode encontrar o [!DNL tracking server] e a [!DNL report suite ID] à direita no beacon de rastreamento. O [!DNL tracking server] é o nome do host no beacon, portanto, é fácil encontrá-lo. As IDs de [!UICONTROL conjunto de relatórios] são uma lista separada por vírgulas logo após “/b/ss/” no nome do caminho do beacon.

Para ver o beacon, bem como todas as outras informações que chegam ao Analytics e outras soluções da Experience Cloud, instale a [extensão do Chrome “Experience Cloud Debugger”](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=pt-BR).

## Antes da implementação {#before-implementation}

**[!DNL Tracking server]**: se ainda não tiver começado a implementação do Adobe Analytics, você deve escolher um subdomínio para o [!DNL tracking server] “.sc.omtrdc.net”. Por exemplo, digamos que eu possua uma loja de chapéus online chamada “Jim’s Brims”. Posso simplesmente definir meu [!DNL tracking server] como:

“jimsbrims.sc.omtrdc.net”.

**[!UICONTROL Conjunto de relatórios]**: para encontrar uma lista dos [!UICONTROL conjuntos de relatórios] criados, faça logon no [!DNL Analytics] e acesse [!UICONTROL Admin] > [!UICONTROL Conjuntos de relatórios] no menu superior para ver uma lista de [!UICONTROL conjuntos de relatórios], incluindo sua ID e título.

Veja o vídeo abaixo para obter mais informações.

>[!VIDEO](https://video.tv.adobe.com/v/40899/?quality=12&learn=on&captions=por_br)
