---
title: Uso do Report Builder para saber mais sobre a API do Adobe Analytics
description: Report Builder é algo que todos conhecemos e amamos. E se eu dissesse a vocês que poderiam usar o que vocês sabem sobre a Report Builder para avançar ainda mais sua habilidade com o Adobe Analytics? Neste vídeo, iremos acompanhar como fazer as solicitações do Report Builder de depuração e usá-las para aprender como criar seus próprios query da API do Analytics.
feature: report builder
topics: null
audience: analyst
activity: use
doc-type: feature video
team: Technical Marketing
kt: 2345
translation-type: tm+mt
source-git-commit: 24ad92b0ccdf1112e3ed4a0968cd47db757598c3
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%

---


# Usar o [!UICONTROL Report Builder] para saber mais sobre a API do Adobe Analytics {#using-report-builder-to-learn-the-adobe-analytics-api}

[!UICONTROL Report Builder] é algo que todos conhecemos e amamos. E se eu dissesse a vocês que poderiam usar o que vocês sabem sobre [!UICONTROL Report Builder] para avançar ainda mais na sua habilidade com o Adobe Analytics? Neste vídeo, iremos acompanhar como responder às solicitações do [!UICONTROL Report Builder] de depuração e usá-las para aprender como criar seus próprios query de [!DNL Analytics] API.

>[!VIDEO](https://video.tv.adobe.com/v/25442/?quality=12)

**ATUALIZAÇÃO**: [!UICONTROL O Report Builder] atualizou ligeiramente a forma como solicita os dados. Você ainda pode usar a abordagem deste vídeo, mas as informações serão um pouco diferentes em um depurador.

Em um depurador:

1 - Procure api5.omniture.com. O número pode variar de 1 a 5, dependendo do data center.

2 - Go to the [!UICONTROL Request] tab

3 - Procure &quot;[!DNL Report.Queue]&quot; na solicitação.

Também há um método alternativo para depurar solicitações como essa, e ele funciona tão bem quanto isso. Você pode ativar o registro de [!UICONTROL Report Builder] no menu [!UICONTROL Opções] e isso gravará as mesmas informações que um depurador faria. Os registros podem ser encontrados em [!UICONTROL Documentos] > [!UICONTROL ReportBuilderLogs]e serão organizados por dia. Você pode pesquisar no arquivo por &quot;Report.Queue&quot; para localizar cada solicitação. Os registros também ajudam na solução de problemas.

Para obter mais informações sobre esse recurso, visite a [documentação](https://www.adobe.io/).
