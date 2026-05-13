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
TQID: https://experienceleague.adobe.com/CnzT7nd58cibYkdt7hfAwgMF4kJR3clcTZYbditrsaM
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
  - id: b3f03848-ae12-48b2-8aab-cad18567eb32
  - id: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2:
  - id: ac8a38fa-dec3-4581-8f64-178fde9f64e8
  - id: f836f655-eebe-4b76-82bc-697955ec1ce3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 279
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
