---
title: Utilização do Report Builder para saber mais sobre a API do Adobe Analytics
description: O Report Builder é algo que todos conhecemos e gostamos. E se disséssemos que você poderia usar o que sabe sobre o Report Builder para melhorar ainda mais o seu conjunto de habilidades do Adobe Analytics? Neste vídeo, abordaremos como responder às solicitações do Report Builder de depuração e usá-las para aprender a criar as suas próprias consultas de API do Analytics.
feature: Report Builder
topics: null
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
role: User
level: Intermediate
exl-id: 8b8e0dac-2498-4fba-ba4b-585b309ae1fd
source-git-commit: 8fc641743bc9e07b838a22ca64ccc15344d52764
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 100%

---

# Utilização do [!UICONTROL Report Builder] para saber mais sobre a API do Adobe Analytics {#using-report-builder-to-learn-the-adobe-analytics-api}

O [!UICONTROL Report Builder] é algo que todos conhecemos e gostamos. E se disséssemos que você poderia usar o que sabe sobre o [!UICONTROL Report Builder] para melhorar ainda mais o seu conjunto de habilidades do Adobe Analytics? Neste vídeo, abordaremos como responder às solicitações do [!UICONTROL Report Builder] de depuração e usá-las para aprender a criar as suas próprias consultas de API do [!DNL Analytics].

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12&learn=on)

**ATUALIZAÇÃO**: O [!UICONTROL Report Builder] atualizou ligeiramente a maneira como os dados são solicitados. Você ainda pode usar a abordagem deste vídeo, mas as informações serão ligeiramente diferentes em um depurador.

Em um depurador:

1 - Pesquise por api5.omniture.com. O número pode variar de 1 a 5, dependendo do data center.

2 - Acesse a guia [!UICONTROL Solicitação]

3 - Procure por “[!DNL Report.Queue]” na solicitação.

Também há um método alternativo para depurar solicitações como essa que funciona muito bem. Você pode ativar o log do [!UICONTROL Report Builder] no menu [!UICONTROL Opções] que registrará as mesmas informações que um depurador registraria. Os logs podem ser encontrados em [!UICONTROL Documentos] > [!UICONTROL ReportBuilderLogs] e serão organizados por dia. Você pode pesquisar por “Report.Queue” no arquivo para encontrar cada solicitação. Os logs também ajudam na solução de diversos problemas.

Para obter mais informações sobre esse recurso, consulte a [documentação](https://www.adobe.io/).
