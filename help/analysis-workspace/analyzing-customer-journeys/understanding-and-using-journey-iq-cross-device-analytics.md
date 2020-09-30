---
title: Entendendo e usando o QI de jornada - Análise entre dispositivos
description: Quando os usuários interagem com a sua marca, eles fazem isso de várias formas e em vários dispositivos. O Cross-Device Analytics é integrado ao Adobe Experience Platform Identity Service para identificar como os dispositivos são mapeados para pessoas. Em seguida, ele aproveita essa inteligência para criar uma visualização entre dispositivos do comportamento do usuário. Isso resulta em ser capaz de fazer análise em pessoas, não em dispositivos.
feature: cda
topics: null
audience: all
activity: use
doc-type: article
team: Technical Marketing
kt: 4138
translation-type: tm+mt
source-git-commit: 24ad92b0ccdf1112e3ed4a0968cd47db757598c3
workflow-type: tm+mt
source-wordcount: '1681'
ht-degree: 6%

---


# Compreensão e uso [!DNL Journey IQ] - Análise entre dispositivos

Quando os usuários interagem com a sua marca, eles fazem isso de várias formas e em vários dispositivos. O Cross-Device Analytics integra-se ao para identificar [!DNL Adobe Experience Platform Identity Service] como os dispositivos são mapeados para pessoas. Em seguida, ele aproveita essa inteligência para criar uma visualização entre dispositivos do comportamento do usuário. Isso resulta em ser capaz de fazer análise em pessoas, não em dispositivos.

## Visão geral da análise entre dispositivos

### Não Sou Meus Dispositivos

Quando os usuários interagem com sua marca, eles fazem isso de várias maneiras e em várias &quot;superfícies&quot; ou &quot;dispositivos&quot;. Eles podem usar um navegador da Web em um PC ou dispositivo móvel, ou podem usar um aplicativo móvel. Na análise digital tradicional, que cresceu na coleta de dados com base em cookies, cada uma dessas superfícies é representada como um &quot;visitante&quot; exclusivo. Isso significa que cada um de seus usuários humanos é representado como um visitante único e múltiplo.

Veja um exemplo. Suponha que Isabelle interagiu com sua marca da seguinte maneira:

*Isabelle é três visitantes*![da Tradicional Jornada de Análises](assets/cda-isabelle-journey-traditional-analytics.png)

Usando a análise tradicional, a jornada de Isabelle é fraturada em três pedaços. Ela é representada como três visitantes únicos, cada um dos quais usou um dispositivo diferente para executar tarefas isoladas. O que é necessário é uma visualização unificada, de dispositivo cruzado, das interações de Isabelle. [!DNL Journey IQ: Cross-Device Analytics] fornece esta visualização.

*Isabelle é uma pessoa* que faz a jornada analítica![entre dispositivos](assets/cda-isabelle-journey-cross-device-analytics.png)

### Uma Visualização Entre Dispositivos Oferece Análises Melhores

Ter uma visualização do comportamento de Isabelle centrada na pessoa e entre dispositivos pode fazer uma diferença significativa na sua análise. Por exemplo, a abordagem tradicional baseada em visitantes não fornece a você a visão completa da eficácia do canal de marketing. Vejamos a jornada de Isabelle mais uma vez, focando em qual canal recebe crédito pela visualização do produto e pela compra. Usaremos atribuição de [!UICONTROL último toque] para simplificar, mas o mesmo problema ocorre usando qualquer modelo de atribuição quando você divide o comportamento de Isabelle em visitantes separados. Usar a tradicional visualização do mundo baseada em visitantes dá resultados muito diferentes, até mesmo enganosos:

*Atribuição de* canal do Analytics tradicional vs. Analytics![de vários dispositivos](assets/channel-attribution.png)

Observe que com a visualização entre dispositivos, o canal de e-mail recebe crédito tanto pela visualização do produto quanto pela compra, o que representa com mais precisão a experiência real de Isabelle.

Continue lendo para saber mais sobre:

* How [!DNL Cross-Device Analytics] Works
* Pré-requisitos para [!DNL Cross-Device Analytics]
* Interpretação de dados entre dispositivos
* Analisando dados entre dispositivos no Analysis Workspace

## How [!DNL Cross-Device Analytics] Works

[!DNL Journey IQ: Cross-Device Analytics (CDA)] integra-se ao [!DNL Adobe Experience Platform Identity Service], utilizando o [[!DNL Co-op Graph]](https://docs.adobe.com/content/help/pt-BR/device-co-op/using/home.html) ou [!DNL Private Graph] para identificar como os dispositivos mapeiam para pessoas. Em seguida, ele aproveita essa inteligência para criar uma visualização entre dispositivos do comportamento do usuário. O CDA inclui recursos e ferramentas inigualáveis para ajudar sua empresa a entender o uso de vários dispositivos e a experiência do cliente nesses dispositivos em suas interações com a sua marca. Ele se situa como uma camada abaixo da Analysis Workspace para fornecer um profundo insight sobre a análise de audiência baseada na pessoa e atribuição entre dispositivos, segmentação e análise de viagem usando ferramentas poderosas como [!UICONTROL Fallout], [!DNL Flow], [!DNL Cohort]e [!DNL Segment IQ] [!DNL Attribution IQ].

### O [!DNL Cross-Device Virtual Report Suite]

O CDA é apresentado por meio de um tipo especial de conjunto de relatórios [[!UICONTROL virtuais entre dispositivos]](https://docs.adobe.com/content/help/pt-BR/analytics/components/virtual-report-suites/vrs-about.html). Isso permite que você continue a usar o conjunto de relatórios original baseado em dispositivos, ao introduzir análises entre dispositivos na sua organização. É fácil configurar um VRS CDA.

Na etapa um do construtor VRS, escolha o conjunto [!UICONTROL de] relatórios que foi configurado pelo Adobe como habilitado para CDA:

*Escolher um conjunto de[!UICONTROL relatórios base (origem) habilitado para CDA]* Conjunto![ de relatórios virtuais Etapa um](assets/cda-vrs-step-one.png)

Em seguida, ative o Processamento [!UICONTROL de tempo do] relatório e ative a sutura [!UICONTROL entre dispositivos]:

*Habilitar processamento[!UICONTROL em tempo de]relatório e correção[!UICONTROL entre dispositivos]* Conjunto![ de relatórios virtuais Etapa dois](assets/cda-vrs-step-two.png)

Termine a configuração do VRS e salve-a. O CDA VRS será exibido no Analysis Workspace com um ícone especial ao lado dele, como mostrado abaixo:

*Selecione o CDA VRS no Analysis Workspace*![[!UICONTROL Virtual Report Suite] Etapa três](assets/cda-vrs-step-three.png)

>[!TIP]
>
>Você pode criar quantos conjuntos [!UICONTROL de relatórios] virtuais CDA desejar sobre o conjunto [!UICONTROL de]relatórios base habilitado para CDA.

### Restaurando Histórico

Às vezes, os usuários levam algum tempo para fazer logon e para o [!DNL Co-op Graph] ou [!DNL Private Graph] para identificá-los e mapear seus dispositivos. O CDA utiliza uma janela de retrospectiva de 30 dias, permitindo que ele reitere um visitante não identificado anteriormente como uma pessoa até 30 dias no passado.

Como isso ajuda? Lembre-se da viagem de usuário de Isabelle da discussão acima:

![[!DNL Cross-Device Analytics] Jornada](assets/cda-isabelle-journey-cross-device-analytics.png)

É possível que Isabelle não tenha feito login até pouco antes de fazer a compra e que o aparelho de Isabelle [!DNL Co-op Graph] ou [!DNL Private Graph] não tenha mapeado os dispositivos de Isabelle até algum momento depois de sua compra. Mas a retrospectiva de 30 dias do CDA permite que o CDA reafirme o comportamento anterior de Isabelle a nível de pessoa, fornecendo-vos a visualização de dispositivo cruzado da sua jornada de que precisam.

>[!NOTE]
>
>Como o histórico pode ser reiniciado, isso significa que seus dados podem mudar ao longo do tempo em um conjunto [!UICONTROL de relatórios]virtuais habilitado para CDA. Lembre-se disso ao comunicar insights de uma análise baseada em CDA.

## Pré-Requisitos Para Análises [!UICONTROL Entre Dispositivos]

O CDA está incluído com [[!DNL Analytics Ultimate]](https://helpx.adobe.com/legal/product-descriptions/adobe-analytics.html). A partir de setembro de 2019, [!DNL Analytics Ultimate] os clientes que atenderem aos pré-requisitos listados abaixo estão qualificados para usar o CDA. Os pré-requisitos para o CDA são os seguintes:

* Sua empresa deve ser um membro do [!DNL Adobe Experience Platform Identity Service] [!DNL Co-op Graph] [ou usar um](https://docs.adobe.com/content/help/pt-BR/device-co-op/using/home.html)[!DNL Adobe Experience Platform Identity Service Private Graph].
* Você deve implementar tudo o que for necessário para [!DNL Co-op Graph] ou [!DNL Private Graph] incluindo a [ID (ECID)](https://docs.adobe.com/content/help/pt-BR/id-service/using/home.html) e a sincronização de ID com o gráfico. Observe que, além dos requisitos técnicos, a empresa [!DNL Co-op Graph] tem outros requisitos legais e contratuais.
* Atualmente, não é possível usar duas organizações IMS com uma única [!DNL Private Graph], portanto você deve padronizar em uma única organização IMS. Em alguns casos, é possível que um cliente com várias organizações IMS use o [!DNL Co-op Graph] em conjunto com o CDA.
* O [!DNL Co-op graph] e [!DNL Private Graph], bem como certos componentes do CDA são hospedados em [!DNL Microsoft Azure]. Isso significa que [!DNL Analytics] os dados são copiados para frente e para trás entre o centro de processamento de dados Adobe e a presença do Adobe em [!DNL Microsoft Azure]. Alguns [!DNL Analytics] dados serão armazenados em [!DNL Azure]. Sua empresa deve concordar com este acordo.
* O CDA requer um conjunto de [!UICONTROL relatórios]&quot;entre dispositivos&quot;. Ou seja, o conjunto [!UICONTROL de] relatórios que você usa para CDA deve incluir dados de vários tipos de dispositivos diferentes ou &quot;superfícies&quot;, como Web para desktop, Web móvel e aplicativo móvel. A partir de setembro de 2019, o volume de chamada do servidor para este conjunto [!UICONTROL de] relatórios deve ser de 100MM/dia ou menos. (Os limites de volume de chamadas do servidor aumentarão nos próximos meses.)
* A partir de setembro de 2019, os e [!DNL Co-op Graph] [!DNL Private Graph] estão disponíveis apenas na América do Norte. O calendário para a presença de gráficos na EMEA e na APAC será anunciado no futuro. Se você estiver nessas regiões, incentivamos você a start de ver esses pré-requisitos agora para que você esteja pronto para ir quando o gráfico estiver disponível.

## Interpretação de dados entre dispositivos

### Pessoas não Visitantes

No Conjunto [!UICONTROL de relatórios]virtuais CDA, você verá algumas alterações. Por exemplo, a métrica Visitantes  únicos é substituída por duas novas métricas: [!UICONTROL Pessoas] e dispositivos [!UICONTROL únicos]. Essas novas métricas fornecem um insight muito melhor sobre o tamanho da audiência.

*Métrica de pessoas e dispositivos*![CDA [!UICONTROL de pessoas]](assets/cda-people-metric.png)

No Construtor [[!UICONTROL de]](https://docs.adobe.com/content/help/pt-BR/analytics/components/segmentation/segmentation-workflow/seg-build.html)segmentos, o container de segmentos do [!UICONTROL Visitante] foi substituído por um container de segmento [!UICONTROL Pessoa] . Usando um CDA VRS, é possível criar segmentos entre dispositivos, como:

* Pessoas que usam mais de um dispositivo
* Pessoas que iniciam sua jornada em um dispositivo móvel e depois compram em um dispositivo desktop
* Visitas onde as pessoas usam mais de um dispositivo para realizar uma tarefa

*Container de segmentos* de nível de pessoa![[!DNL Segment Builder] [!UICONTROL de pessoa]](assets/cda-segment-builder-person-container.png)

### Persistência do Dimension

Em um VRS CDA, dimensões como [!DNL eVars] agora persistem automaticamente entre dispositivos. Por exemplo, um [!DNL eVar] que está configurado como:

* Alocação: Mais recente (último)
* Expira após: Compra

persistirá automaticamente de um dispositivo para outro até que o evento de compra seja acionado.

## Analisando dados entre dispositivos no Analysis Workspace

### Análise de Audiência baseada em pessoa

Você já se perguntou quantas pessoas estão interagindo com a sua marca? Você queria entender quantos e que tipo de dispositivos eles usam? Como o uso deles se sobrepõe? Usando um CDA VRS, você pode criar diagramas [Venn entre dispositivos e](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/visualizations/venn.html) histogramas [](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/visualizations/histogram.html)por pessoa.

*Venn e Histograma da análise* de audiência![com base em pessoa](assets/cda-venn-and-histogram.png)

### Entre dispositivos [!DNL Flow]

Com o CDA e o Analysis Workspace, você pode visualizar como as pessoas estão se movendo de um dispositivo para outro ao longo do tempo na [[!DNL Flow visualização]](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/visualizations/flow/flow.html). Você pode ver onde eles desistem em sua jornada, e onde eles continuam.

*[!DNL Flow]com CDA*
![[!DNL Flow Visualization]](assets/cda-flow-viz.png)

### Entre dispositivos [!DNL Fallout]

Você provavelmente usa várias visualizações [[!DNL Fallout]](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/visualizations/fallout/fallout-flow.html) para analisar a eficiência dos usuários em uma série de etapas antes de obter sucesso. Você sabia que sua visualização dessas [!DNL Fallout visualizations] é limitada ao usar análises tradicionais baseadas em dispositivos? Para que a etapa seguinte seja &quot;fallthrough&quot; bem-sucedida, a próxima etapa deve ocorrer no mesmo navegador ou aplicativo que a etapa anterior. Na análise baseada em dispositivos, você é cego para as pessoas que completam com êxito a próxima etapa em outro dispositivo.

Não se preocupe, CDA já cobriu. O CDA cria a visualização entre dispositivos que torna [!DNL Fallout visualizations] muito, muito mais útil. Afinal de contas, o que realmente importa é se a pessoa acabou por ser bem sucedida na sua tarefa algures.

*[!DNL Fallout]com CDA*
![[!DNL Fallout Visualization]](assets/cda-fallout-viz.png)

### [!DNL Cross-Device Attribution IQ]

Como o CDA cria uma camada de dados entre dispositivos abaixo do Analysis Workspace, toda a sua análise terá uma perspectiva entre dispositivos. Um exemplo poderoso é o [[!DNL Attribution IQ]](https://docs.adobe.com/content/help/pt-BR/analytics/analyze/analysis-workspace/attribution/models.html). [!DNL Attribution IQ] no Analysis Workspace, você pode comparar vários modelos de atribuição lado a lado. Usando esse recurso com o CDA, agora você pode comparar como diferentes dispositivos contribuem para o sucesso.

Por exemplo, suponha que você queira entender com que frequência um telefone celular é o primeiro dispositivo usado em uma interação que leva ao sucesso final. Isto representa a &quot;taxa de aquisição&quot; do telefone celular. CDA + [!DNL Attribution IQ] permite que você faça esta análise:

*[!DNL Attribution IQ]com CDA*
![[!DNL Attribution IQ]](assets/cda-attribution-iq.png)

For more information, see the [[!DNL Cross-Device Analytics] help documentation](https://docs.adobe.com/content/help/pt-BR/analytics/components/cda/cda-home.html).
