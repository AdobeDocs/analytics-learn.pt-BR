---
title: Noções básicas e uso do IQ da jornada - Análise entre dispositivos
description: Quando os usuários interagem com sua marca, fazem isso de muitas maneiras e em vários dispositivos. A Análise entre dispositivos é integrada ao Adobe Experience Platform Identity Service para identificar como os dispositivos são mapeados para pessoas. Em seguida, ele usa essa inteligência para criar uma visualização entre dispositivos do comportamento do usuário. Isso resulta na capacidade de fazer análise em pessoas, não em dispositivos.
feature: CDA
topics: null
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
role: Profissional
level: Intermediário
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1667'
ht-degree: 6%

---


# Entendendo e usando [!DNL Journey IQ] - Análise entre dispositivos

Quando os usuários interagem com sua marca, fazem isso de muitas maneiras e em vários dispositivos. O Cross-Device Analytics integra-se ao [!DNL Adobe Experience Platform Identity Service] para identificar como os dispositivos são mapeados para pessoas. Em seguida, ele usa essa inteligência para criar uma visualização entre dispositivos do comportamento do usuário. Isso resulta na capacidade de fazer análise em pessoas, não em dispositivos.

## Visão geral da Análise entre dispositivos

### Eu Não Sou Meus Dispositivos

Quando os usuários interagem com sua marca, fazem isso de muitas formas e em várias &quot;superfícies&quot; ou &quot;dispositivos&quot;. Eles podem usar um navegador da Web em um PC ou dispositivo móvel, ou podem usar um aplicativo móvel. Na análise digital tradicional, que cresceu na coleta de dados com base em cookies, cada uma dessas superfícies é representada como um &quot;visitante&quot; exclusivo. Isso significa que cada um dos usuários humanos é representado como um múltiplo de visitantes únicos.

Veja um exemplo. Suponha que Isabelle interagiu com sua marca da seguinte maneira:

*Isabelle é três*
![visitantesJornada tradicional do Analytics](assets/cda-isabelle-journey-traditional-analytics.png)

Usando análises tradicionais, a jornada de Isabelle é fraturada em três partes. Ela é representada como três visitantes únicos, cada um usando um dispositivo diferente para executar tarefas isoladas. O que é necessário é uma visão unificada, em vários dispositivos, das interações de Isabelle. [!DNL Journey IQ: Cross-Device Analytics] fornece essa visualização.

*Isabelle é uma*
![pessoa: jornada de análise entre dispositivos](assets/cda-isabelle-journey-cross-device-analytics.png)

### Uma visualização entre dispositivos fornece análises melhores

Ter uma visão centrada em pessoas e entre dispositivos do comportamento de Isabelle pode fazer uma diferença significativa na sua análise. Por exemplo, a abordagem tradicional baseada em visitantes não fornece a visão completa da eficácia do canal de marketing. Vamos olhar a jornada de Isabelle mais uma vez, focando em qual canal recebe crédito pela exibição de produto e pela compra dela. Usaremos a atribuição [!UICONTROL last-touch] para simplificar, mas o mesmo problema ocorre usando qualquer modelo de atribuição quando você divide o comportamento de Isabelle em visitantes separados. Usar a visão tradicional do mundo baseada em visitantes dá resultados muito diferentes, até mesmo enganosos:

*Atribuição tradicional de canal de análise e*
![análise entre dispositivos](assets/channel-attribution.png)

Observe que, com a visualização entre dispositivos, o canal de email recebe crédito pela exibição do produto e pela compra, o que representa com mais precisão a experiência real de Isabelle.

Continue lendo para saber mais sobre:

* Como o [!DNL Cross-Device Analytics] funciona
* Pré-requisitos para [!DNL Cross-Device Analytics]
* Interpretação de dados entre dispositivos
* Análise de dados entre dispositivos no Analysis Workspace

## Como o [!DNL Cross-Device Analytics] funciona

[!DNL Journey IQ: Cross-Device Analytics (CDA)] integra-se ao  [!DNL Adobe Experience Platform Identity Service], utilizando o  [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/pt-BR/device-co-op/using/home.html) ou  [!DNL Private Graph] para identificar como os dispositivos são mapeados para pessoas. Em seguida, ele usa essa inteligência para criar uma visualização entre dispositivos do comportamento do usuário. O CDA inclui recursos e ferramentas imbatíveis para ajudar sua empresa a entender o uso de vários dispositivos e a experiência do cliente nesses dispositivos em suas interações com sua marca. Ele é uma camada abaixo da Analysis Workspace para fornecer um profundo insight sobre a análise de público-alvo com base em pessoas e a atribuição entre dispositivos, a segmentação e a análise de jornada usando ferramentas poderosas como [!UICONTROL Fallout], [!DNL Flow], [!DNL Cohort], [!DNL Segment IQ] e [!DNL Attribution IQ].

### O [!DNL Cross-Device Virtual Report Suite]

O CDA é apresentado por meio de um tipo especial de [[!UICONTROL Conjunto de relatórios virtual]](https://docs.adobe.com/content/help/pt-BR/analytics/components/virtual-report-suites/vrs-about.html) entre dispositivos. Isso permite que você continue a usar o conjunto de relatórios baseado em dispositivos original ao introduzir a análise entre dispositivos na organização. Configurar um VRS do CDA é fácil.

Na etapa um do construtor de VRS, escolha o [!UICONTROL conjunto de relatórios] que foi configurado pela Adobe como habilitado para CDA:

*Escolha um  [!UICONTROL conjunto de]*
![[!UICONTROL relatórios de base (fonte) habilitado para CDAnterior ] Conjunto de relatórios virtualEtapa um](assets/cda-vrs-step-one.png)

Em seguida, ative [!UICONTROL Processamento de tempo do relatório] e ative [!UICONTROL a compilação entre dispositivos]:

*Habilitar o  [!UICONTROL processamento no tempo do relatório e a compilação ] entre dispositivos [!UICONTROL Conjunto de relatórios virtuais]*
![ Etapa dois](assets/cda-vrs-step-two.png)

Termine a configuração do VRS e salve-a. O VRS do CDA será exibido no Analysis Workspace com um ícone especial ao lado dele, como mostrado abaixo:

*Selecione o CDA VRS no Analysis*
![[!UICONTROL Workspace] Conjunto de relatórios virtual Etapa três](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Você pode criar quantos conjuntos de relatórios virtuais CDA [!UICONTROL desejar] desejar sobre o conjunto de relatórios [!UICONTROL base habilitado para CDA].

### Restaurando Histórico

Às vezes, leva um tempo para seus usuários fazerem logon e para que [!DNL Co-op Graph] ou [!DNL Private Graph] identifiquem-nos e mapeiem juntos seus dispositivos. O CDA utiliza uma janela de retrospectiva de 30 dias, permitindo que reafirme um visitante não identificado anteriormente como uma pessoa em até 30 dias no passado.

Como isso ajuda? Lembre-se da jornada de usuários de Isabelle da discussão acima:

![[!DNL Cross-Device Analytics] Jornada](assets/cda-isabelle-journey-cross-device-analytics.png)

É possível que Isabelle não tenha feito o login apenas antes de realizar a compra e que [!DNL Co-op Graph] ou [!DNL Private Graph] não tenha mapeado juntos os dispositivos de Isabelle até que algum dia depois de sua compra. Mas a retrospectiva de 30 dias do CDA permite que o CDA reafirme o comportamento de Isabelle em nível de pessoa, fornecendo a você a visão entre dispositivos de sua jornada que você precisa.

>[!NOTE]
>
>Como o histórico pode ser reafirmado, isso significa que seus dados podem mudar ao longo do tempo em um [!UICONTROL conjunto de relatórios virtual] habilitado para CDA. Lembre-se disso ao comunicar insights de uma análise baseada em CDA.

## Pré-Requisitos Para [!UICONTROL Análise Entre Dispositivos]

O CDA está incluído com [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html). A partir de setembro de 2019, [!DNL Analytics Ultimate] os clientes que atenderem aos pré-requisitos listados abaixo estarão qualificados para usar o CDA. Os pré-requisitos para o CDA são os seguintes:

* Sua empresa deve ser membro do [!DNL Adobe Experience Platform Identity Service] [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) ou usar um [!DNL Adobe Experience Platform Identity Service Private Graph].
* Você deve implementar tudo o que é necessário para [!DNL Co-op Graph] ou [!DNL Private Graph] incluindo [Experience Cloud ID (ECID)](https://docs.adobe.com/content/help/pt-BR/id-service/using/home.html) e a sincronização de ID com o gráfico. Observe que, além dos requisitos técnicos, o [!DNL Co-op Graph] tem outros requisitos legais e contratuais.
* No momento, não é possível usar duas organizações IMS com um único [!DNL Private Graph], portanto, você deve padronizar em uma única organização IMS. Em alguns casos, é possível que um cliente com várias organizações IMS use o [!DNL Co-op Graph] em conjunto com o CDA.
* Os [!DNL Co-op graph] e [!DNL Private Graph], bem como certos componentes do CDA são hospedados em [!DNL Microsoft Azure]. Isso significa que os dados [!DNL Analytics] são copiados de um lado para o outro entre o centro de processamento de dados da Adobe e a presença da Adobe em [!DNL Microsoft Azure]. Alguns dados [!DNL Analytics] serão armazenados em [!DNL Azure]. Sua empresa deve concordar com esse acordo.
* O CDA requer um &quot;entre dispositivos&quot; [!UICONTROL conjunto de relatórios]. Ou seja, o [!UICONTROL conjunto de relatórios] que você usa para CDA deve incluir dados de vários tipos de dispositivos diferentes ou &quot;superfícies&quot; como Web para desktop, Web móvel e aplicativo móvel. A partir de setembro de 2019, o volume de chamadas do servidor para este [!UICONTROL conjunto de relatórios] deve ser de 100MM de chamadas do servidor por dia ou menos. (Os limites do volume de chamadas do servidor aumentarão nos próximos meses.)
* A partir de setembro de 2019, os [!DNL Co-op Graph] e [!DNL Private Graph] estarão disponíveis somente na América do Norte. O cronograma de presença de gráficos na EMEA e APAC será anunciado em um futuro. Se você estiver nessas regiões, recomendamos que você comece a observar esses pré-requisitos agora para que esteja pronto para o lançamento quando o gráfico estiver disponível.

## Interpretação de dados entre dispositivos

### Pessoas não visitantes

No CDA [!UICONTROL Conjunto de relatórios virtuais], você verá algumas alterações. Por exemplo, a métrica [!UICONTROL Visitantes únicos] é substituída por duas novas métricas: [!UICONTROL People] e [!UICONTROL Dispositivos únicos]. Essas novas métricas fornecem um insight muito melhor sobre o tamanho do público-alvo.

*Métrica de*
![pessoas e  [!UICONTROL dispositivos únicosCDA]](assets/cda-people-metric.png)

No [[!UICONTROL Construtor de segmentos]](https://docs.adobe.com/content/help/pt-BR/analytics/components/segmentation/segmentation-workflow/seg-build.html), o contêiner do segmento [!UICONTROL Visitante] foi substituído por um contêiner de segmento [!UICONTROL Pessoa]. Usando um CDA VRS, é possível criar segmentos entre dispositivos, como:

* Pessoas que usam mais de um dispositivo
* Pessoas que iniciam sua jornada em um dispositivo móvel e depois compram em um dispositivo de desktop
* Visitas em que as pessoas usam mais de um dispositivo para realizar uma tarefa

*Segmentos de nível de pessoa*
![[!DNL Segment Builder]  PersonContainer](assets/cda-segment-builder-person-container.png)

### Persistência da dimensão

Em um CDA VRS, dimensões como [!DNL eVars] agora persistem automaticamente entre dispositivos. Por exemplo, um [!DNL eVar] que está configurado como:

* Alocação: Mais recente (último)
* Expirar após: Compra

O persistirá automaticamente de um dispositivo para outro até que o evento Purchase seja acionado.

## Análise de dados entre dispositivos no Analysis Workspace

### Análise de público-alvo com base em pessoas

Você já se perguntou quantas pessoas estão interagindo com sua marca? Você quer entender quantos e que tipo de dispositivos eles usam? Como o uso se sobrepõe? Usando um VRS CDA, você pode criar [diagramas Venn](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/visualizations/venn.html) e dispositivos por pessoa [histogramas](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/visualizations/histogram.html) entre dispositivos.

*Análise de público-alvo com base em pessoa*
![Venn e Histograma](assets/cda-venn-and-histogram.png)

### Entre dispositivos [!DNL Flow]

Com o CDA e o Analysis Workspace, você pode visualizar como as pessoas estão mudando de um dispositivo para outro ao longo do tempo no [[!DNL Flow visualization]](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/visualizations/flow/flow.html). Você pode ver onde eles desistem em sua jornada, e onde eles continuam.

*[!DNL Flow]com CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Entre dispositivos [!DNL Fallout]

Você provavelmente usa vários [[!DNL Fallout visualizations]](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) para analisar o desempenho dos usuários em uma determinada série de etapas antes de obter sucesso. Você sabia que a sua visão desses [!DNL Fallout visualizations] é limitada ao usar análises tradicionais baseadas em dispositivos? Para &quot;fallthrough&quot; com sucesso, a próxima etapa deve ocorrer no mesmo navegador ou aplicativo que a etapa anterior. Na análise baseada em dispositivos, você é cego para pessoas que concluem com sucesso a próxima etapa em outro dispositivo.

Não se preocupe, CDA já cobriu. O CDA cria a visualização entre dispositivos que torna [!DNL Fallout visualizations] muito mais útil. Afinal de contas, o que realmente importa é se a pessoa acabou por ter êxito na sua tarefa algures.

*[!DNL Fallout]com CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Como o CDA cria uma camada de dados entre dispositivos no Analysis Workspace, toda a análise será aprimorada com uma perspectiva entre dispositivos. Um exemplo poderoso é por meio de [[!DNL Attribution IQ]](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/attribution/models.html). [!DNL Attribution IQ] no Analysis Workspace permite comparar vários modelos de atribuição lado a lado. Com esse recurso no CDA, agora é possível comparar como diferentes dispositivos contribuem para o sucesso.

Por exemplo, suponha que você queira entender com que frequência um celular é o primeiro dispositivo usado em uma interação que leva ao sucesso. Representa a &quot;taxa de aquisição&quot; do celular. CDA + [!DNL Attribution IQ] permite fazer essa análise:

*[!DNL Attribution IQ]com CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

Para obter mais informações, consulte a [[!DNL Cross-Device Analytics] documentação de ajuda](https://docs.adobe.com/content/help/pt-BR/analytics/components/cda/cda-home.html).
