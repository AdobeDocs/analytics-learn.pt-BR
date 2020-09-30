---
title: Como identificar o servidor de rastreamento do Analytics e os conjuntos de relatórios
description: Ao configurar o Adobe Analytics ou ao referenciá-lo em outras soluções de Experience Cloud, geralmente é útil ou até necessário conhecer o "Servidor de rastreamento" do Analytics que você está usando, ou também o "Conjunto de relatórios" para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado o Adobe Analytics.
feature: implementation basics
topics: null
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
translation-type: tm+mt
source-git-commit: 60f4ce4f563a990576b3331b01cd87c29d424f43
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 2%

---


# Como identificar o Analytics [!DNL Tracking Server] e os conjuntos de [!UICONTROL relatórios] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Ao configurar o Adobe Analytics, ou ao referenciá-lo em outras soluções de Experience Cloud, geralmente é útil ou até necessário saber o [!DNL Analytics] &quot;[!DNL Tracking Server]&quot; que você está usando, ou também o &quot;Conjunto[!UICONTROL de]relatórios&quot; para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado o Adobe Analytics.

## Após a implementação {#after-implementation}

Depois de implementar [!DNL Analytics] em um site, você pode encontrar o [!DNL tracking server] e a [!DNL report suite ID] direita no beacon de rastreamento. O nome do host [!DNL tracking server] está no beacon, portanto, é fácil de encontrar. As IDs do conjunto [!UICONTROL de] relatórios são uma lista separada por vírgulas logo após &quot;/b/ss/&quot; no nome do caminho do beacon.

Para ver o beacon, bem como todas as outras informações recebidas [!DNL Analytics] e outras soluções de Experience Cloud, instale a Extensão [do Chrome](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=pt)&quot;Experience Cloud Debugger&quot;.

## Antes da implementação {#before-implementation}

**[!DNL Tracking Server]** - Se você ainda não começou com sua implementação do Adobe Analytics, você escolherá um subdomínio para &quot;.sc.omtrdc.net&quot; [!DNL tracking server]. Por exemplo, vamos dizer que tenho uma loja de chapéus online chamada &quot;Jim’s Brims&quot;. Posso simplesmente definir [!DNL tracking server] para:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Conjunto]** de relatórios - Para localizar uma lista dos conjuntos [!UICONTROL de] relatórios criados, faça logon [!DNL Analytics] e vá até [!UICONTROL Admin] > Conjuntos [!UICONTROL de] relatórios no menu superior para ver uma lista dos conjuntos [!UICONTROL de]relatórios, incluindo sua ID e título.

Veja o vídeo abaixo para obter mais informações.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
