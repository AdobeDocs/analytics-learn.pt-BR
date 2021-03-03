---
title: Como identificar o servidor de rastreamento do Analytics e os conjuntos de relatórios
description: Ao configurar o Adobe Analytics, ou ao referenciá-lo em outras soluções da Experience Cloud, geralmente é útil ou até necessário conhecer o "Servidor de rastreamento" do Analytics que você está usando, ou também o "Conjunto de relatórios" para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado ou não o Adobe Analytics.
feature: Noções básicas da implementação
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: '"Desenvolvedor, engenheiro de dados"'
level: Iniciante
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 2%

---


# Como identificar seu Analytics [!DNL Tracking Server] e [!UICONTROL Report Suites] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Ao configurar o Adobe Analytics, ou ao referenciá-lo em outras soluções da Experience Cloud, geralmente é útil ou até necessário saber o [!DNL Analytics] &quot;[!DNL Tracking Server]&quot; que você está usando, ou também o &quot;[!UICONTROL Report Suite]&quot; para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado ou não o Adobe Analytics.

## Após a implementação {#after-implementation}

Depois de implementar [!DNL Analytics] em um site, você pode encontrar o [!DNL tracking server] e o [!DNL report suite ID] direito no beacon de rastreamento. O [!DNL tracking server] é o nome do host no beacon, então é fácil de localizar. As IDs [!UICONTROL do conjunto de relatórios] são uma lista separada por vírgulas logo após &quot;/b/ss/&quot; no nome do caminho do sinal.

Para ver o beacon, bem como todas as outras informações que vêm para [!DNL Analytics] e outras soluções da Experience Cloud, instale o [&quot;Experience Cloud Debugger&quot; Extensão do Chrome](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=pt).

## Antes da implementação {#before-implementation}

**[!DNL Tracking Server]** - Se ainda não tiver iniciado a implementação do Adobe Analytics, você escolherá um subdomínio para o &quot;.sc.omtrdc.net&quot;  [!DNL tracking server]. Por exemplo, digamos que eu tenha uma loja de chapéus online chamada &quot;Jim’s Brims&quot;. Posso simplesmente definir meu [!DNL tracking server] como:

&quot;jimsbrims.sc.omtrdc.net&quot;.

**[!UICONTROL Conjunto de relatórios]**  - Para encontrar uma lista dos conjuntos de  [!UICONTROL relatórios ] que foram criados, faça logon  [!DNL Analytics] e vá até  [!UICONTROL Administrador]  >  [!UICONTROL Conjuntos de relatórios ] no menu superior para ver uma lista de conjuntos de  [!UICONTROL relatórios], incluindo a ID e o título.

Veja o vídeo abaixo para obter mais informações.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12)
