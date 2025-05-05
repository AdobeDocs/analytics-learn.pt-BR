---
title: Um guia abrangente para a transição do Google Analytics para o Adobe Analytics
description: Saiba mais sobre a localização de funcionalidades equivalentes e como usá-las com eficiência na transição do Google Analytics para o Adobe Analytics
feature: Third-party Integration
role: User
level: Beginner
kt: 9830
thumbnail: 34749.jpg
exl-id: b2be6081-a1c0-4435-affb-454ed5a74662
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '3413'
ht-degree: 100%

---

# Um guia abrangente para a transição do Google Analytics para o Adobe Analytics{#comprehensive-guide-for-transitioning-to-Adobe-Analytics}

## 1. Introdução

Um dos maiores desafios na transição entre quaisquer ferramentas é saber onde encontrar a funcionalidade equivalente e aprender a usá-la com eficiência. Esta discussão faz parte de um guia maior, cujo objetivo é ajudar os usuários a fazerem a transição para o Adobe Analytics (seja como um novo usuário ou como usuário do Google Analytics) com mais facilidade. Uma comparação aprofundada com o GA (que possivelmente é a ferramenta similar com a qual a maioria dos usuários está familiarizada) será fornecida para ajudar os usuários a correlacionar o conhecimento existente com o novo conjunto de ferramentas. Quando não há substituto para a prática, isso ajuda a começar e a reduzir as frustrações que você pode encontrar durante esse período.

Também devemos fazer uma rápida comparação de terminologia:

| **Descrição** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Uma métrica de evento que representa que uma página (ou tela em um aplicativo) foi visualizada | Exibição de página | Pageview |
| Uma métrica que representa um grupo de interações no site ou aplicativo que ocorrem no mesmo intervalo de tempo | Visita | Sessão |
| Uma métrica que define um dispositivo identificado (com base em vários critérios, incluindo cookies e outros padrões de comportamento para unir informações do usuário) | Visitante único | Usuário |

## 2. As interfaces

Quando as pessoas comparam o Google Analytics com o Adobe Analytics, elas comentam que, inicialmente, a interface da Adobe é intimidadora. Embora isso seja verdade, isso é também uma força, não uma fraqueza. O Adobe Analytics oferece uma grande variedade de ferramentas e flexibilidade na visualização de dados, permitindo que você tenha muito mais liberdade para criar o que precisa.

Vamos começar observando os relatórios &quot;no site&quot;.

### 2.1. Relatórios no site

#### 2.1.1. Tela inicial

Tanto o Adobe Analytics quanto o Google Analytics fornecem uma maneira de personalizar a primeira visualização que um usuário vê ao fazer logon.

##### 2.1.1.1. Espaço de trabalho / Configuração personalizada da tela inicial (Adobe Analytics)

O Adobe Analytics não apresenta um relatório pré-construído para todos os usuários visualizarem ao fazer logon. A página inicial padrão leva o usuário para a tela inicial do Espaço de trabalho, que mostra a cada usuário todos os relatórios do espaço de trabalho que ele criou ou que foram compartilhados com ele. Além disso, cada usuário tem a capacidade de definir qualquer um desses relatórios como sua tela inicial, se desejar.

![workspace-create-project](assets/ga-to-aa_1.png)

Detalhes sobre o espaço de trabalho serão apresentados mais adiante neste guia. Consulte a Seção 2.1.2.1

>[!TIP]
>
>Crie alguns relatórios padrão e compartilhe com os outros da sua organização para que eles tenham um ponto de partida e vejam as informações sem que precisem criar os próprios relatórios imediatamente.



##### 2.1.1.2. Insights da Tela inicial (Google Analytics)

* A tela inicial do Google Analytics tem algumas visualizações pré-construídas para você. Elas abrangem, por exemplo:
* Usuários, Sessões, Taxa de rejeição e Duração da sessão nos últimos sete dias
* Usuários por hora do dia nos últimos 30 dias
* Usuários atuais agora e Principais páginas ativas
* Canal de tráfego, Origem/Meio e Referências nos últimos sete dias
* Sessões por país nos últimos sete dias
* Principais páginas dos últimos sete dias
* Tendência de usuários ativos nos últimos 30 dias
* e mais

No GA4, os usuários têm mais opções para personalizar e adicionar seus próprios relatórios à tela inicial.

![google-analytics-interfaces](assets/ga-to-aa_2.png)

Isso é provavelmente o que você mais sente falta no Adobe Analytics. Não há uma tela inicial pré-construída para você. No entanto, você pode facilmente configurar um espaço de trabalho personalizado para replicar o que precisa da lista acima e configurá-lo como sua tela de destino. Mais informações sobre isso serão apresentadas mais adiante (ou consulte a Seção 2.1.2.1, sobre o Adobe Workspace).

#### 2.1.2. Report Builders no local

Além de fornecer relatórios simples, as ferramentas de análise fornecem ferramentas mais eficientes para criar seus próprios relatórios personalizados.

##### 2.1.2.1. Adobe Analytics Workspace

É o carro-chefe do Adobe Analytics. Desde que estreou, em 2017, ele se tornou o local de referência para análise no Analytics e o principal motivo pelo qual a seção Relatórios está prestes a ser encerrada.

Essa ferramenta permite criar relatórios com liberdade quase total.

O relatório pode ser dividido em painéis que podem conter diversas visualizações. Os painéis podem ser configurados com informações comuns, como intervalos de datas e filtros de segmentos comuns.

Tanto os painéis quanto as visualizações dentro deles podem ser redimensionados e arrastados para mostrar os itens lado a lado ou empilhados. Assim, se você quiser comparar dois conjuntos de dados diferentes lado a lado, você pode criar painéis divididos ao meio, mostrando os dois sites lado a lado, para facilitar a comparação.

Há uma variedade de visualizações disponíveis para os usuários:

* Tabela de forma livre
* Tabela de coorte
* Fallout
* Fluxo
* Gráficos
   * Área (empilhada e não empilhada)
   * Linha
   * Dispersão
   * Barra (empilhada e não empilhada)
   * Marcador
   * Rosca
   * Histograma
   * Barra horizontal (empilhada e não empilhada)
* Mapa
* Blocos de resumo
   * Mudança de resumo
   * Texto de resumo
   * Texto (campo de texto livre para inserir informações extras para fornecer contexto)
* Venn

Cada painel e visualização podem ser intitulados e ter uma descrição aplicada para ajudar a contextualizar o que as informações estão mostrando.
No Adobe Analytics, os segmentos (essencialmente filtros de dados) se aplicam retroativamente e podem ser colocados em colunas das tabelas de forma livre para comparar os dados lado a lado. Por exemplo, se um usuário quiser comparar duas categorias diferentes em seu site para tráfego, ele pode criar um segmento para a &quot;Categoria A&quot; e um segmento diferente para a &quot;Categoria B&quot;.

![analytics-page-views-report](assets/ga-to-aa_3.png)

As tabelas de forma livre permitem ter várias colunas e segmentação, conforme necessário, para visualizar os dados da maneira que você desejar.

Se não quiser ver um detalhamento por data, basta arrastar e soltar outra dimensão ou segmento para ver os dados de uma maneira diferente. Por exemplo, use segmentos para o Tipo de dispositivo e adicione um detalhamento por sistema operacional para seus usuários de dispositivo móvel/tablet:

![analytics-compare-page-views-report](assets/ga-to-aa_4.png)

O Espaço de trabalho permite que sua criatividade flua, você não fica limitado a detalhamentos &quot;padrão&quot;. Você pode criar as visualizações necessárias para aprofundar as comparações que precisam ser executadas.

>[!TIP]
>
>Não tenha medo de experimentar e explorar. Há várias maneiras de pensar fora da caixa. Além disso, validar o que você construiu mostra a sua opinião. A experiência ajuda.

Você pode criar métricas calculadas dinamicamente ou segmentos que vivem somente dentro do relatório para evitar a inundação do segmento e do repositório de cálculos. Isso permite criar itens focados que são necessários para relatórios específicos sem confundir sua organização com itens que não podem ser usados em outros contextos.

Esta discussão é apenas uma introdução a esta ferramenta; há outros guias abrangentes para começar. Depois de revisar esses guias, você criará relatórios abrangentes, como os seguintes:

![workspace-dashboard](assets/ga-to-aa_5.png)

Os espaços de trabalho não são salvos automaticamente, portanto, é mais fácil criar um relatório ad-hoc único sem encher seu repositório de relatórios.

Outro recurso eficiente dos espaços de trabalho é a capacidade de aplicar modificadores interativos a seus relatórios na forma de menus suspensos. Esses menus suspensos não funcionam em arquivos CSV ou PDF exportados dos relatórios. No entanto, no relatório em tempo real, eles permitem atualizar todas as visualizações em um painel para mostrar o mesmo relatório em condições diferentes. Vários menus suspensos podem ser usados e, desde que as opções não sejam mutuamente exclusivas, os itens selecionados serão empilhados para apresentar informações de maneira clara.

>[!IMPORTANT]
>
>Para saber mais sobre o uso de menus suspensos e detalhamentos de forma livre, consulte <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680?profile.language=pt>

##### 2.1.2.2. Google Analytics: painéis, relatórios personalizados e relatórios salvos

O Google tem algumas ferramentas para criar relatórios na interface, mas seguem a mesma exibição e limitações da seção de relatórios.

Ao ler isto, os versados em Google Analytics podem pensar: &quot;Mas o Google Data Studio não é um equivalente melhor em relação ao Espaço de trabalho, da Adobe&quot;? Sim, mas o Data Studio tecnicamente não faz parte da ferramenta do Analytics e permite conexões com diferentes fontes de dados. Essa ferramenta é abordada posteriormente na seção “Acesso estendido a relatórios”, mais especificamente na Seção 2.2.3.

Os painés do Google e os relatórios personalizados permitem que você reúna várias visualizações em um único relatório, mas ao contrário do Espaço de trabalho, você ainda fica limitado a correlações simples e a quais dados podem ser colocados em quais colunas.

Nos relatórios personalizados, um dos maiores desafios é que, ao criar um filtro, ele se aplica a todas as guias do relatório. Não há uma maneira de comparar dois filtros diferentes no mesmo relatório.

Ele funciona para comparações simples. Todos são semelhantes aos painéis herdados, aos relatórios personalizados e aos marcadores da Adobe. São ferramentas básicas fornecidas para atender às suas necessidades, que estão no conjunto de relatórios.

#### 2.1.3 Relatórios

O Google e a Adobe têm alguns relatórios navegáveis que são tabelas pré-construídas e gráficos de linha do tempo básicos baseados em uma dimensão.

##### 2.1.3.1. Relatórios do Adobe Analytics

O Adobe Analytics também tem uma seção de relatórios, mas ela será removida para dar lugar ao Analysis Workspace. Na verdade, o fim da vida útil foi anunciado para essa interface, já que o Espaço de trabalho é uma ferramenta mais eficiente. A maioria dessas tabelas pode ser criada e modificada com mais facilidade. As seções da Adobe são muito mais detalhadas, e isso pode ser intimidante:

![analytics-site-metrics](assets/ga-to-aa_6.png)

Como a maioria dos itens acima são acessíveis por meio de espaços de trabalho, ofereço uma breve visão geral dessas seções e como elas se relacionam com o Google Analytics e destaco os relatórios que ainda são relevantes.

As métricas do site são algo que já conhecemos. Aqui abrangeremos as métricas padrão (exibições de página, visitantes únicos, visitas e eventos personalizados que você configurou). É semelhante ao Relatório de comportamentos do GA, mas também inclui parte do que você encontraria no Audience (já que a Adobe não divide os tipos de métrica).

Aqui, você encontra os relatórios de “Bot”. O tráfego de bots é excluído de todos os seus relatórios padrão. No entanto, há dois relatórios que fornecem insight sobre o que está acontecendo e quais bots estão chegando ao seu site. Isso é especialmente bom se você configurar regras de bot personalizadas para excluir bots de spam conhecidos que acessam frequentemente seu site. Você pode obter alguns insights sobre o que esses bots estão fazendo sem que seus relatórios principais sejam inundados por esse tráfego. Os relatórios de bot estão indisponíveis no Espaço de trabalho, mas em breve, os novos recursos de relatório também permitirão que os usuários obtenham essas informações por lá.

O Conteúdo do site é um agrupamento de dimensões padrão da Adobe: Nome da página, Seções do site, Hierarquias, Servidores e muito mais. Todas essas dimensões estão disponíveis no Espaço de trabalho.

Os “Móveis” são um agrupamento de dados específicos de dispositivos móveis, incluindo dispositivos, tipos de dispositivos e muito mais. Eles estão disponíveis no Espaço de trabalho.

Os caminhos não estão disponíveis no Espaço de trabalho. O Espaço de trabalho tem um diagrama de fluxo onde é possível ver os fluxos de entrada e saída para uma única página/valor. Por outro lado, os Caminhos permitem que você veja os caminhos mais comuns usados no site. Por padrão, Páginas é o primeiro relatório de caminho configurado para você. No entanto, é possível ativá-lo para propriedades personalizadas, como um valor de “Tipo de página”. Você pode ver a definição de caminho dentro dos tipos de página. A outra coisa interessante em Caminhos é a maneira simples como as informações são apresentadas. O diagrama de fluxo no espaço de trabalho (dependendo da quantidade que você está tentando ver) pode ficar grande. Recomendo experimentar ambos. Cada um tem seu uso e valor, dependendo do que você está tentando fazer. Observe que qualquer dimensão pode ser usada em Fluxos, enquanto a Definição de caminho deve ser configurada em uma propriedade no painel administrativo.

Os relatórios de Fontes de tráfego, Campanhas e Canais de marketing são semelhantes ao relatório de Aquisição no Google. As Fontes de tráfego se concentram nos Referenciadores reais e as Campanhas se concentram nos Códigos de Campanha. Os Canais de marketing também se concentram nos Códigos de campanha, mas aplicam uma lógica extra, determinada por você, sobre como processar as informações. A Adobe oferece mais liberdade sobre como configurar suas regras. Por outro lado, o Google faz várias coisas para você, e isso traz uma mudança de pensamento. Por padrão, a atribuição do Google para Códigos de campanha é de seis meses. Por padrão, a atribuição da Adobe é definida como uma semana. Isso pode ser alterado nas configurações de administrador, mas no Espaço de trabalho é possível aplicar uma atribuição personalizada sobre qualquer dimensão, proporcionando muito mais flexibilidade &quot;instantânea&quot;.

Os relatórios de Retenção de visitante e Perfil do visitante são semelhantes aos relatórios de Público-alvo no Google Analytics. O foco da Retenção está mais na frequência de retorno, enquanto o foco do Perfil do visitante está mais na geografia e tecnologia dos usuários.

Os relatórios de Conversão personalizada e Tráfego personalizado são relatórios de dimensão personalizados. As conversões são eVars. Você pode definir uma expiração personalizada para o valor como, por exemplo, ocorrência, visita, mês e ano. Esse valor permanece consistente para um usuário no intervalo de tempo configurado, a menos que seja substituído. As variáveis de tráfego são propriedades. Você também pode configurá-las para Relatórios de definição de caminho ou como itens de lista, que detalharão vários valores com base em um delimitador de sua escolha.

A Mídia é para coisas como vídeos ou arquivos de áudio, onde você configurou um rastreamento de mídia especial.

Relatórios personalizados é uma seção na qual um usuário pode personalizar as colunas e os detalhamentos criados na interface dos relatórios e salvá-los como um relatório personalizado. No entanto, como mencionado acima, visto que o Espaço de trabalho permite detalhamentos e correlações muito mais avançados, qualquer personalização deve ser realizada lá. Essa era uma boa solução antes de o Espaço de trabalho existir.

A seção Marcadores é semelhante aos Relatórios personalizados, onde os relatórios usados com frequência podem ser marcados na interface dos relatórios para facilitar sua localização.

O Painel era um produto herdado que permitia às pessoas combinarem reportlets de dados em uma visualização. No entanto, a funcionalidade no Espaço de trabalho (Seção 2.1.2.1) é tão mais fácil de usar, que só existe como um ponto de acesso para relatórios herdados que devem ser recriados antes que esse recurso seja descontinuado.

As metas permitem que as pessoas criem um relatório com base em uma meta em um determinado período. As equipes monitoram campanhas para ver se elas estão no caminho para atingir suas metas de tráfego.

Todos os relatórios aqui permitiam várias colunas de métrica e detalhamentos de dimensão. No entanto, a simplicidade das visualizações e parte da lógica por trás de quais elementos podem ser correlacionados pode ser frustrante às vezes.

##### 2.1.3.2. Relatórios do Google Analytics

O Google Analytics divide esses relatórios nas seguintes seções: Tempo real, Público-alvo, Aquisição, Comportamento, Conversas (no GA3), Ciclo de vida (com as subseções: Aquisição, Envolvimento, Monetização, Retenção) e Usuário (com as subseções: Demografia e Tecnologia).

![google-analytics-interface-compare](assets/ga-to-aa_7.png)

É possível fazer pequenos ajustes nessas visualizações, adicionar um detalhamento de dimensão secundário, alterar a visualização, criar um filtro dos dados e muito mais. Você pode salvar suas personalizações como um relatório salvo.

Esses fornecem insights rápidos e fáceis para seus dados. No entanto, você não pode comparar itens como Usuários à exibições de página, para uma página na mesma tabela, e não pode adicionar mais de uma dimensão extra para ver dados adicionais.

São boas para dados analíticos rápidos, mas se você realmente precisa pesquisar fundo, elas sofrem com as limitações.

### 2.2. Acesso estendido ao relatório

Além do “Relatório local”, a maioria das ferramentas oferece uma funcionalidade estendida que permite levar sua análise para fora das ferramentas e criar algo um pouco mais personalizado.

#### 2.2.1. Adobe Analytics Report Builder (Extensão do Microsoft® Excel)

O Espaço de trabalho é uma ótima ferramenta, mas, às vezes, é necessário inserir seus dados em uma planilha personalizada, para que você possa unir várias fontes de dados. O Report Builder pode ajudar nessas situações.

O Report Builder é um plug-in para o Microsoft® Excel que permite criar conexões com seus dados do Adobe Analytics e assim obter dados tabulares que podem ser manipulados no Excel. Geralmente, para usar isso com eficiência, você puxaria os dados para algumas guias de dados brutos, usaria referências de células do Excel para extrair dados dessas guias em um único relatório consolidado e criaria gráficos e visualizações.

>[!NOTE]
>
>O Report Builder tem uma permissão especial que precisa ser aplicada aos usuários para acessar este plug-in. Isso provavelmente só deve ser concedido a usuários que aprenderam a usar a ferramenta corretamente.

#### 2.2.2. Conexão da API do Adobe Analytics

Se você precisar que os dados do Adobe Analytics sejam processados por uma ferramenta diferente do Excel e desejar que eles incluam as exclusões de regra de bot, use a API da Adobe para obter os dados diretamente. Em seguida, processe os dados usando um script ou adicione-os a um banco de dados para uso com outro sistema.

Observe que a API ainda extrai dados de correlação aplicando os detalhamentos e segmentos conforme especificado na solicitação de obtenção.

O Espaço de trabalho da Adobe (Seção 2.1.2.1) usa a API para criar os relatórios e, se você habilitar o modo de depuração, ele mostrará as chamadas de API exatas usadas. Essa é uma maneira rápida de criar suas chamadas de API. Ao usar o espaço de trabalho para criar e validar os dados que deseja obter, você pode usar essas chamadas de API para obter os dados para seu próprio processamento.


#### 2.2.3. Google Analytics Data Studio

Se você está lendo este documento, já sabe que mencionei o Data Studio como um recurso equivalente ao Espaço de trabalho da Adobe. O Data Studio permite extrair dados do Google Analytics, e também dados de outras fontes. Isso é bom se você quiser consolidar os dados analíticos com outros dados coletados. No entanto, com o Google Analytics, há o mesmo tipo de limitações de visualização. A forma como as linhas e colunas são formadas ainda é limitada.

Mesmo assim, essa é uma ferramenta eficiente, e eu de forma alguma desaconselharia as pessoas a usá-la. A minha experiência pessoal é que considero o comportamento rígido bastante limitante.


#### 2.2.4. Extensão das Planilhas Google

Para uso próprio, quando preciso extrair dados de maneira estendida do Google Analytics, minha ferramenta pessoal de escolha é a extensão de planilhas do Google. Embora eu precise fazer várias conexões com minhas tabelas de GA, posso fazer referência às células dos dados brutos e criar os relatórios que preciso. Em seguida, visualizo-os usando os recursos gráficos das Planilhas do Google.


## 3. Exportações de dados brutos

Há ocasiões em que realmente precisamos de dados brutos. Tanto a Adobe quanto o Google oferecem os recursos para obter informações nesse formato.

### 3.1. Feed de dados da Adobe

Na Seção 2.2.2, mencionei que a API do Adobe Analytics extraía de &quot;dados processados&quot;. O feed de dados brutos extrai dados processados pelas “Regras de processamento” que foram configuradas no painel de administração, mas esses dados brutos incluem todos os dados excluídos em qualquer outro lugar.

Isso significa que todas as exclusões de bot, dados filtrados por IP interno etc., serão incluídos nos feeds de dados brutos. Existem sinalizadores para identificar esses dados, portanto, se você criar um data lake, a equipe de engenharia poderá criar uma lógica para processar esses dados adequadamente.

Os feeds de dados brutos podem ser personalizados para enviar todas as colunas de dados ou apenas colunas específicas se você precisar de um feed mais focado.

Os feeds podem ser enviados diretamente para o FTP, SFTP ou S3. 


### 3.2. Google Big Query

Infelizmente, esta é uma ferramenta do Google com a qual não tenho nenhuma experiência de uso. Em teoria, ele deve ser semelhante ao feed de dados da Adobe, permitindo que sua equipe de engenharia acesse dados brutos da conta do Google Analytics.

No entanto, em vez de fornecer um despejo completo de dados brutos, ele permite que os engenheiros acessem os dados por meio de consultas SQL para obter dados brutos direcionados ou todas as colunas de dados brutos.

## 4. Conclusão

Como qualquer sistema, a prática é necessária para se familiarizar com a ferramenta. Esperamos que este guia o ajude a começar ou forneça dicas para melhorar o uso do Adobe Analytics.

No entanto, eu recomendaria o uso do Adobe Analytics e do Google Analytics em sua estratégia de implementação (mesmo que o Google Analytics seja apenas a versão gratuita). Isso permite ter um sistema de backup para garantir que você tenha dados, pois nenhum sistema é infalível.

Há muitos recursos disponíveis para você além deste guia que podem ajudar a melhorar sua estratégia:

* [Adobe Experience League](https://experienceleague.adobe.com/pt-br?lang=pt-BR#home) - Contém tutoriais, vídeos, documentações e fóruns da comunidade
* [Grupos de usuários da Adobe](https://analytics-augs.adobe.com/) - Um centro de eventos executados pela comunidade para ajudar os usuários a se conectarem e melhorar suas implementações.
* [Canal do YouTube para grupos de usuários do Adobe Analytics](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) - Não foi possível criar uma sessão de grupo de usuários do Adobe Analytics? Assista novamente às sessões anteriores de grupos de usuários em todo o mundo para saber mais sobre como seus colegas estão usando a ferramenta.
* [Canal de chat do Slack para medições](https://www.measure.chat/) - Conecte-se com usuários do Adobe Analytics em todo o mundo e compartilhe aprendizados do setor, faça perguntas a seus colegas e participe de grupos de interesse com foco em medição.
* e mais!

## Autora

Este documento foi escrito por:

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, gerente de otimização de análise da Torstar

Especialista em Adobe Analytics

