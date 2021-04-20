---
title: Usar o Report Builder para saber mais sobre a API do Adobe Analytics
description: Report Builder é algo que todos conhecemos e adoramos. Então, e se eu disser que você pode usar o que sabe sobre o Report Builder para avançar ainda mais seu skillset do Adobe Analytics? Neste vídeo, abordaremos como depurar solicitações do Report Builder e usá-las para saber como criar suas próprias consultas de API do Analytics.
feature: Report Builder
topics: null
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
role: Business Practitioner
level: Intermediate
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 1%

---


# Usar o [!UICONTROL Report Builder] para saber mais sobre a API do Adobe Analytics {#using-report-builder-to-learn-the-adobe-analytics-api}

[!UICONTROL Report ] Builder é algo que todos conhecemos e amamos. Então, e se eu disser que você pode usar o que sabe sobre o [!UICONTROL Report Builder] para avançar ainda mais seu conjunto de habilidades do Adobe Analytics? Neste vídeo, abordaremos como obter as solicitações de depuração do [!UICONTROL Report Builder] e usá-las para saber como criar suas próprias consultas de API do [!DNL Analytics].

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12)

**ATUALIZAÇÃO**:  [!UICONTROL O ] Construtor de relatórios atualizou ligeiramente a forma como solicita os dados. Você ainda pode usar a abordagem deste vídeo, mas as informações serão um pouco diferentes em um depurador.

Em um depurador:

1 - Pesquise por api5.omniture.com. O número pode variar de 1 a 5, dependendo do data center.

2 - Vá para a guia [!UICONTROL Request]

3 - Procure por &#39;[!DNL Report.Queue]&#39; na solicitação.

Também há um método alternativo para depurar solicitações como essa, e ele também funciona. Você pode ativar o registro do [!UICONTROL Report Builder] no menu [!UICONTROL Options] e isso registrará as mesmas informações que um depurador registraria. Os logs podem ser encontrados em [!UICONTROL Documents] > [!UICONTROL ReportBuilderLogs], e serão organizados por dia. Você pode pesquisar o arquivo para &#39;Report.Queue&#39; para encontrar cada solicitação. Os registros também ajudam na solução de problemas de qualquer problema.

Para obter mais informações sobre esse recurso, visite a [documentação](https://www.adobe.io/).
