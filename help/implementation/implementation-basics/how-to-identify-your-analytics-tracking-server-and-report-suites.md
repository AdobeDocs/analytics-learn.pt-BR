---
title: Como identificar o servidor de rastreamento da análise e a ID de conjunto de relatórios
description: Ao configurar o Adobe Analytics ou referenciá-lo em outras soluções da Experience Cloud, muitas vezes é útil (ou até necessário) saber qual “servidor de rastreamento” do Analytics você está usando, bem como o “conjunto de relatórios” para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado o Adobe Analytics ou não.
feature: Implementation Basics
topics:
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
TQID: 'https://experienceleague.adobe.com/DRy-lxNuEQR9Tb-nIoev0Mu1OzSiCcLcqve1eDf7p6Q'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
    internal-label: Measurement
source-git-commit: 3e00cf9416ba2c6886e5a7efb952cac8ce370930
workflow-type: tm+mt
source-wordcount: '334'
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

>[!VIDEO](https://video.tv.adobe.com/v/40899/?captions=por_br&quality=12&learn=on)
