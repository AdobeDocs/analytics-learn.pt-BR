---
title: Como identificar o servidor de rastreamento do Analytics e os conjuntos de relatórios
description: Ao configurar o Adobe Analytics ou ao referenciá-lo em outras soluções da Experience Cloud, geralmente é útil ou até necessário conhecer o “Servidor de rastreamento” do Analytics que você está usando, ou também o “Conjunto de relatórios” para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado o Adobe Analytics ou não.
feature: Implementation Basics
topics: null
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 2358
role: Developer, Data Engineer
level: Beginner
exl-id: 3925026f-69f1-4425-b3a9-6fef26375fed
source-git-commit: 8fc641743bc9e07b838a22ca64ccc15344d52764
workflow-type: ht
source-wordcount: '303'
ht-degree: 100%

---

# Como identificar o [!DNL Tracking Server] do Analytics e os [!UICONTROL conjuntos de relatórios] {#how-to-identify-your-analytics-tracking-server-and-report-suites}

Ao configurar o Adobe Analytics ou ao referenciá-lo em outras soluções da Experience Cloud, geralmente é útil ou até necessário conhecer o [!DNL Analytics] “[!DNL Tracking Server]” que você está usando, ou também o “[!UICONTROL Conjunto de relatórios]” para o qual você está enviando dados. Este vídeo mostra como localizar ambos os valores, independentemente de você já ter implementado o Adobe Analytics ou não.

## Após a implementação {#after-implementation}

Depois de implementar o [!DNL Analytics] em um site, você pode encontrar o [!DNL tracking server] e o [!DNL report suite ID] à direita no beacon de rastreamento. O [!DNL tracking server] é o nome do host no beacon, portanto, é fácil encontrá-lo. As IDs do [!UICONTROL conjunto de relatórios] são uma lista separada por vírgulas logo após “/b/ss/” no nome do caminho do beacon.

Para ver o beacon, bem como todas as outras informações que chegam ao [!DNL Analytics] e outras soluções da Experience Cloud, instale a [Extensão do Chrome “Experience Cloud Debugger”](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj?hl=pt-BR).

## Antes da implementação {#before-implementation}

**[!DNL Tracking Server]** — se ainda não tiver começado a implementação do Adobe Analytics, você escolherá um subdomínio para “.sc.omtrdc.net” [!DNL tracking server]. Por exemplo, digamos que eu tenha uma loja de chapéus online chamada “Jim’s Brims”. Posso simplesmente definir meu [!DNL tracking server] como:

“jimsbrims.sc.omtrdc.net”.

**[!UICONTROL Conjunto de relatórios]** — para encontrar uma lista de [!UICONTROL conjuntos de relatórios] que foram criados, faça logon no [!DNL Analytics] e acesse [!UICONTROL Administrador] > [!UICONTROL Conjuntos de relatórios ] no menu superior para ver uma lista de [!UICONTROL conjuntos de relatórios], inclusive a ID e o título.

Veja o vídeo abaixo para obter mais informações.

>[!VIDEO](https://video.tv.adobe.com/v/26061/?quality=12&learn=on)
