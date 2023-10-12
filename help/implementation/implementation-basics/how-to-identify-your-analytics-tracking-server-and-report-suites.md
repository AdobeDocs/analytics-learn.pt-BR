---
title: Como identificar o servidor de rastreamento de análise e a ID do conjunto de relatórios
description: Ao configurar o Adobe Analytics ou ao referenciá-lo em outras soluções de Experience Cloud, geralmente é útil ou até necessário conhecer o "Servidor de rastreamento" do Analytics que você está usando, ou também o "Conjunto de relatórios" para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado o Adobe Analytics ou não.
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
source-wordcount: '330'
ht-degree: 18%

---

# Como identificar sua análise [!DNL tracking server] e [!UICONTROL ID do conjunto de relatórios] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Ao configurar o Adobe Analytics ou ao referenciá-lo em outras soluções de Experience Cloud, geralmente é útil ou até necessário conhecer o &quot;servidor de rastreamento&quot; do Analytics que você está usando, ou também o &quot;[!UICONTROL conjunto de relatórios]&quot; para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado o Adobe Analytics ou não.

>[!IMPORTANT]
>
>Este artigo e vídeo se aplicam a uma implementação &quot;AppMeasurement&quot; do Adobe Analytics, e não a uma implementação usando o SDK da Web.

## Após a implementação {#after-implementation}

Depois de implementar o Analytics em um site, você pode encontrar a [!DNL tracking server] e a variável [!DNL report suite ID] diretamente no beacon de rastreamento. A variável [!DNL tracking server] O é o nome do host no beacon, portanto, é fácil encontrá-lo. A variável [!UICONTROL conjunto de relatórios] As IDs são uma lista separada por vírgulas logo após &quot;/b/ss/&quot; no nome do caminho do beacon.

Para ver o beacon, bem como todas as outras informações que chegam ao Analytics e outras soluções Experience Cloud, instale o [Extensão &quot;Experience Cloud Debugger&quot; do Chrome](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=pt-BR).

## Antes da implementação {#before-implementation}

**[!DNL Tracking server]** - Se ainda não tiver começado a implementação do Adobe Analytics, você escolherá um subdomínio para &quot;.sc.omtrdc.net&quot; [!DNL tracking server]. Por exemplo, digamos que eu tenha uma loja de chapéus online chamada &quot;Jim&#39;s Brims&quot;. Posso simplesmente definir meu [!DNL tracking server] como:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Conjunto de relatórios]** - Para encontrar uma lista de seus [!UICONTROL conjuntos de relatórios] que foram criadas, faça logon no [!DNL Analytics] e vá para [!UICONTROL Admin] > [!UICONTROL Conjuntos de relatórios] no menu superior para ver uma lista de [!UICONTROL conjuntos de relatórios], incluindo a ID e o título.

Veja o vídeo abaixo para obter mais informações.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
