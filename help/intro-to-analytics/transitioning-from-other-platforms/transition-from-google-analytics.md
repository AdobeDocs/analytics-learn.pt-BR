---
title: Um guia abrangente para a transição do Google Analytics para o Adobe Analytics
description: Um dos maiores desafios na transição entre qualquer ferramenta é saber onde encontrar funcionalidade equivalente e aprender a usá-la com eficiência. Essa discussão faz parte de um guia maior para ajudar os usuários a fazerem a transição para o Adobe Analytics.
feature: Third-party Integration
role: User
level: Beginner
doc-type: feature video
thumbnail: 34749.jpg
kt: 9830
exl-id: b2be6081-a1c0-4435-affb-454ed5a74662
source-git-commit: de78868e07b0fa59a7babc092c463bbe4d8e2da7
workflow-type: tm+mt
source-wordcount: '3690'
ht-degree: 1%

---

# Um guia abrangente para a transição do Google Analytics para o Adobe Analytics

## 1. Introdução

Um dos maiores desafios na transição entre qualquer ferramenta é saber onde encontrar funcionalidade equivalente e aprender a usá-la com eficiência. Essa discussão faz parte de um guia maior para ajudar os usuários a fazerem a transição para o Adobe Analytics (como um novo usuário ou proveniente do Google Analytics) com mais facilidade. Uma comparação aprofundada com a GA; como a ferramenta comparativa mais provável com a qual a maioria dos usuários estará familiarizada; é fornecido para ajudar os usuários a correlacionar o conhecimento existente com o novo conjunto de ferramentas. Embora não haja substitutos para a prática; isso ajudará você a começar e, esperemos, reduzirá as frustrações que poderá encontrar durante esse período (ou mesmo como um refrescante depois de começar a entrar no giro das coisas).

Também devemos ter uma rápida comparação de terminologia:

| **Descrição** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Uma métrica de evento que representa uma página (ou tela em um aplicativo) foi visualizada | Exibição da Página | Pageview. |
| Uma métrica que representa um grupo de interações no seu site ou aplicativo que ocorrem no mesmo período | Visita | Sessão |
| Uma métrica que define um dispositivo identificado (com base em vários critérios, incluindo cookies e outros padrões de comportamento para unir informações do usuário) | Visitante único | Usuário |

## 2. As interfaces

Uma das coisas que vejo com mais frequência quando as pessoas comparam o Adobe Analytics com o Google Analytics é que o Adobe tem muita coisa acontecendo - é assustador para as pessoas. Isso é verdade, mas também é. Acreditem ou não; uma força, não uma fraqueza. O Adobe oferece uma grande variedade de ferramentas e flexibilidade na visualização de dados, permitindo que você tenha muito mais liberdade para criar o que precisa.

Vamos começar observando os relatórios &quot;no site&quot;.

### 2.1. Relatórios no local

#### 2.1.1. Tela inicial

O Adobe Analytics e o Google Analytics fornecem uma maneira de personalizar a primeira visualização que um usuário vê ao fazer logon.

##### 2.1.1.1. Área de trabalho / Tela inicial do conjunto personalizado (Adobe Analytics)

A Adobe Analytics não presume criar um relatório pré-criado para todos os usuários visualizarem no logon. A página inicial padrão leva o usuário para a tela inicial do Workspace, que mostrará a cada usuário todos os relatórios do espaço de trabalho que ele criou ou que foram compartilhados com ele. Além disso, cada usuário tem a capacidade de definir qualquer um desses relatórios como sua tela inicial, se desejar.

![image1](assets/ga-to-aa_1.png)

Mais detalhes sobre o espaço de trabalho serão apresentados abaixo mais adiante neste guia. Ver Seção 2.1.2.1

>[!TIP]
>
>Crie/compartilhe alguns relatórios padrão para sua organização para que ela tenha um ponto de partida para ver as informações sem precisar mergulhar na criação de seus próprios relatórios imediatamente.



##### 2.1.1.2. Insights da tela inicial (Google Analytics)

* A Tela inicial do Google Analytics tem algumas visualizações pré-criadas para você.  Isso abrange coisas como:
* Usuários, sessões, taxa de rejeição e duração da sessão nos últimos 7 dias
* Usuários por hora do dia nos últimos 30 dias
* Usuários atuais agora e principais páginas ativas
* Canal de tráfego, Fonte/Médio e Referências nos últimos 7 dias
* Sessões por país nos últimos 7 dias
* Principais páginas dos últimos 7 dias
* Tendência de usuários ativos nos últimos 30 dias
* e mais

No GA4, os usuários têm mais opções para personalizar e adicionar seus próprios relatórios à tela inicial.

![image2](assets/ga-to-aa_2.png)

Essa é provavelmente a coisa que você mais vai perder ao chegar à Adobe. eles não têm uma tela inicial pré-criada para você, mas você pode configurar facilmente um espaço de trabalho personalizado para replicar o que precisa do acima e, se você optar por, configurá-lo como a tela de aterrissagem. Mais informações sobre isso posteriormente (ou consulte a Seção 2.1.2.1 Adobe Workspace).

#### 2.1.2. Report Builder no local

Além dos Relatórios simples fornecidos pelas ferramentas de análise, cada ferramenta também fornece ferramentas mais eficientes para criar seus próprios relatórios personalizados.

##### 2.1.2.1. Espaço de trabalho Adobe Analytics

Esse é o poderoso do Adobe Analytics, desde sua introdução em 2017, ele se tornou o lugar para análise do Analytics e o principal motivo pelo qual a seção Relatórios está prestes a ser encerrada.

Essa ferramenta permite criar relatórios com liberdade quase total.

O relatório pode ser dividido em Painéis e esses painéis podem conter qualquer número de visualizações. Painéis podem ser definidos com informações comuns, como intervalo de datas e filtros de segmentos comuns.

Tanto os painéis quanto as visualizações dentro deles podem ser redimensionados e arrastados para mostrar os itens lado a lado ou empilhados. Assim, se você quiser comparar dois conjuntos de dados diferentes lado a lado, você pode criar painéis que dividem 50/50 ao meio, mostrando os dois sites lado a lado, para facilitar a comparação.

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
   * Alteração de resumo
   * Texto de resumo
   * Texto (campo de texto livre para inserir informações extras para fornecer contexto)
* Venn

Cada painel e visualização podem ser intitulados e ter uma descrição aplicada para ajudar a contextualizar o que as informações estão mostrando.
No Adobe, os segmentos (essencialmente filtros de dados) se aplicam retroativamente e podem ser colocados em colunas das tabelas de forma livre para comparar os dados lado a lado. Por exemplo, se um usuário quiser comparar duas categorias diferentes em seu site para tráfego; poderiam criar um segmento para a &quot;Categoria A&quot; e um segmento diferente para a &quot;Categoria B&quot;.

![image3](assets/ga-to-aa_3.png)

As tabelas de forma livre permitem várias colunas e a segmentação, conforme necessário, para visualizar os dados da maneira que você desejar.

A partir do acima, não deseja visualizar um detalhamento por data? Arraste e solte outra dimensão ou segmento ali para ver os dados de uma maneira diferente.. como talvez usar segmentos para o Tipo de dispositivo e, em seguida, adicione um detalhamento por SO para seus usuários de Mobile/Tablet:

![image3](assets/ga-to-aa_4.png)

O Workspace permite que sua criatividade flua, você não está limitado a detalhamentos &quot;padrão&quot;. Você pode criar as visualizações necessárias para aprofundar as comparações que precisam ser executadas.

>[!TIP]
>
>Não tenha medo de brincar e explorar, há tantas maneiras de pensar fora da caixa aqui, ver o que você pode fazer! Mas também, certifique-se de tentar validar que o que você construiu está realmente mostrando o que você acha que é. Experiência aqui ajudará!

Você pode até criar métricas calculadas dinamicamente ou segmentos que vivem somente dentro do relatório (evitando a inundação de seu segmento e do repositório de cálculos, mas também garantindo que você possa criar itens focalizados que são necessários para relatórios específicos sem confundir sua organização com itens que não são muito utilizáveis em outros contextos.

Esta discussão é apenas uma introdução a esta ferramenta, haverá outros guias mais abrangentes para começar, mas quando você fizer isso, poderá fazer relatórios abrangentes como:

![image3](assets/ga-to-aa_5.png)

Também deve ser observado que os espaços de trabalho não são salvos automaticamente, portanto, é mais fácil fazer um relatório ad-hoc único sem fazer o log-up do repositório de relatórios.

Outro recurso poderoso dos espaços de trabalho é a capacidade de aplicar modificadores interativos a seus relatórios na forma de menus suspensos. Embora esses detalhamentos não funcionem em arquivos CSV ou PDF exportados de seus relatórios, no relatório ao vivo eles permitem atualizar todas as visualizações em um painel para mostrar o mesmo relatório em condições diferentes. Vários menus suspensos podem ser usados e, desde que as opções não sejam mutuamente exclusivas, os itens selecionados serão empilhados para permitir uma maneira limpa de apresentar informações.

>[!IMPORTANT]
>
>Para ler mais sobre o uso de detalhamentos e detalhamentos de forma livre, consulte <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google Analytics: Painéis, relatórios personalizados e relatórios salvos

A Google tem algumas ferramentas para criar relatórios na interface, mas ainda segue a mesma exibição e as mesmas limitações da seção de relatórios.

Agora, para aqueles versados em Google Analytics enquanto vocês leem isso, vocês podem estar dizendo, &quot;bem, um segundo, e o Google Data Studio, não é um equivalente melhor ao Adobe Workspace?&quot; e você estaria correto, mas como o Data Studio não é tecnicamente parte da ferramenta do Analytics e permite conexões com diferentes fontes de dados, essa ferramenta é abordada posteriormente na seção &quot;Acesso a Relatório Estendido&quot; desta discussão (e, em particular, na Seção 2.2.3)

Painéis Google e Relatórios personalizados permitem que você reúna várias visualizações em um único relatório, mas ao contrário do Workspace, você ainda está bloqueado em correlações simples e quais dados podem ser colocados em quais colunas.

Nos Relatórios personalizados, um dos maiores desafios é o fato de que, ao criar um filtro, ele se aplica a todas as guias do relatório... não há como comparar dois filtros diferentes no mesmo relatório.

Para comparações de superfície, ele faz o trabalho. Todos são semelhantes aos Painéis legados do Adobe, aos Relatórios personalizados e aos Marcadores. Ferramentas básicas fornecidas para atender às suas necessidades, que estão no conjunto de relatórios.

#### 2.1.3. Relatórios

O Google e o Adobe têm alguns relatórios navegáveis que são tabelas pré-criadas e gráficos de linha do tempo básicos baseados em uma dimensão.

##### 2.1.3.1. Relatórios do Adobe Analytics

A Adobe Analytics também tem uma seção Relatórios , embora em geral isso esteja sendo removido em fases em favor da Analysis Workspace (e, na verdade, o fim da vida útil foi anunciado para essa interface, desde o Workspace [Seção 2.1.2.1] O é uma ferramenta muito mais poderosa), onde a maioria dessas tabelas pode ser criada e modificada com mais facilidade. Adobe e muito mais quebrados:

![image3](assets/ga-to-aa_6.png)

Com a maior parte das informações acima acessíveis via espaços de trabalho, vou dar uma breve visão geral dessas seções e como elas se relacionam com Google Analytics, e destacar os relatórios aqui que ainda são relevantes.

Métricas do site é o que você esperaria, que abrange as métricas padrão (exibições de página, visitantes únicos, visitas, bem como eventos personalizados que você configurou). Isso é semelhante ao relatório de Comportamento GA, mas também inclui parte do que você encontraria no Público-alvo (já que o Adobe não divide os tipos de métrica).

Aqui, você também encontrará os Relatórios de &quot;Bot&quot;, o tráfego de bots é excluído de todos os seus relatórios padrão. No entanto, há dois relatórios que permitem que você veja alguns insights sobre o que está acontecendo e quais bots estão chegando ao seu site. Isso é especialmente bom se você configurar Regras de bot personalizadas para excluir bots de spammer conhecidos que acessam frequentemente seu site. Você pode obter alguns insights sobre o que esses bots estão fazendo sem que seus relatórios principais sejam inundados, mas esse tráfego. Os relatórios de bot estão indisponíveis no Workspace (mas os novos recursos de relatório em breve também permitirão que os usuários obtenham essas informações lá).

O Conteúdo do site é um agrupamento de dimensões padrão do Adobe: Nome da página, Seções do site (Canais), Hierarquias (uma maneira de criar relatórios detalhados personalizados de organização em seu site), Servidores (isso é particularmente útil se você tem vários subdomínios no site ou está marcando vários sites juntos em um conjunto de rastreamento), etc. Todos estão disponíveis no Workspace.

O Mobile é um agrupamento de dados específicos do Dispositivo móvel , como dispositivos, tipos de dispositivos etc. Todos estão disponíveis no Workspace.

Caminhos é outro desses itens &quot;não totalmente disponíveis no Workspace&quot;... enquanto o Workspace tem um diagrama de Fluxo, você só pode ver os fluxos de Entrada e Saída para uma única página/valor... enquanto Caminhos permitem que você veja os caminhos mais comuns usados no site. Por padrão, Páginas é o primeiro relatório de caminho configurado para você, mas você pode ativá-lo para props personalizados (como se você estivesse rastreando um valor de &quot;Tipo de página&quot;). Você pode ver a definição de caminho dentro dos tipos de página. A outra coisa que eu pessoalmente gosto em Caminhos é a maneira simples como as informações são apresentadas... O diagrama de fluxo no espaço de trabalho (dependendo de quanto você está tentando ver) pode ser esmagador. Recomendo experimentar... cada um tem um uso e um valor dependendo do que você está tentando alcançar. Observe que qualquer dimensão pode ser usada em Fluxos, enquanto a Definição de caminho deve ser configurada em uma Prop no painel Admin.

Os relatórios de Fontes de tráfego, Campanhas e Canais de marketing são semelhantes ao relatório de Aquisição no Google. As Fontes de Tráfego se concentram nos Referenciadores Reais, nas Campanhas, nos Códigos de Campanha e nos Canais de Marketing também se concentram nos Códigos de Campanha, mas também aplicam uma lógica extra, conforme determinado por você sobre como processar as informações. Eu acho que o Adobe oferece muito mais liberdade em como configurar suas regras, Google faz muitas coisas para você, e isso será uma mudança no pensamento. Além disso, é de observar que, por padrão, a atribuição do Google nos Códigos de campanha é de 6 meses, o Adobe é definido por padrão como 1 semana. Isso pode ser alterado nas configurações do administrador, mas no Workspace é possível aplicar uma atribuição personalizada sobre qualquer dimensão, proporcionando muito mais flexibilidade &quot;instantânea&quot;.

Os relatórios Retenção de visitante e Perfil do visitante são semelhantes aos relatórios de Público-alvo no Google Analytics. A retenção está mais focada na frequência de retorno, enquanto o Perfil do visitante está mais focado na Geografia e Tecnologia dos usuários.

Conversão personalizada e Tráfego personalizado são relatórios de dimensão personalizados, Conversões são suas eVars (onde você pode definir uma expiração personalizada para o valor, ou seja, ocorrência, visita, mês, ano etc... e esse valor permanecerá para esse usuário pelo tempo especificado, a menos que seja substituído). As variáveis de tráfego são suas props, mas você também pode configurá-las para Relatórios de definição de caminho ou como itens de lista (que separarão vários valores com base em um delimitador de sua escolha).

A mídia é para coisas como Vídeos ou Arquivos de áudio, onde você configurou um rastreamento de mídia especial.

Relatórios personalizados é uma seção na qual um usuário pode personalizar as colunas e os detalhamentos criados na interface dos relatórios e salvá-los como um relatório personalizado. No entanto, como mencionado acima, como o Workspace permite detalhamentos e correlações muito mais poderosas, qualquer item personalizado deve ser feito lá. Essa era uma boa solução antes da Workspace existir.

A seção Marcadores é semelhante aos Relatórios personalizados, onde os relatórios usados com frequência podem ser marcados na interface dos relatórios para facilitar sua localização.

O painel era um produto herdado que permitia que as pessoas combinassem reportlets de dados em uma visualização. No entanto, a funcionalidade no Workspace (Seção 2.1.2.1) é tão mais fácil de trabalhar, que só existe como um ponto de acesso para relatórios herdados que devem ser recriados antes que esse recurso seja descontinuado.

Metas é uma área de relatório especial que permite que as pessoas criem um relatório com base em um alvo em um determinado período para que as equipes possam monitorar coisas como campanhas e ver se estavam no caminho para atingir suas metas de tráfego.

Todos os relatórios aqui permitiam várias colunas de métrica e detalhamentos de dimensão. mas a simplicidade das visualizações e parte da lógica por trás de quais elementos poderiam ser correlacionados poderia ser frustrante às vezes.

##### 2.1.3.2. Relatórios Google Analytics

O Google Analytics divide esses relatórios nas seguintes seções: Tempo real, Público-alvo, Aquisição, Comportamento e Conversas (em GA3) e Ciclo de vida (com as subseções: Aquisição, Envolvimento, Monetização, Retenção) e Usuário (com as subseções: Demografia e tecnologia).

![image3](assets/ga-to-aa_7.png)

É possível fazer alguns ajustes menores nessas visualizações, adicionar um detalhamento de dimensão secundária, alterar a visualização, criar um filtro nos dados etc. Você pode salvar suas personalizações como um Relatório salvo.

Eles fornecem insights rápidos e fáceis para seus dados. No entanto, você não pode comparar itens como Usuários às exibições de página de uma página na mesma tabela, e não pode adicionar mais de uma dimensão extra para ver dados adicionais.

Esses são bons para dados analíticos rápidos, mas se você realmente precisa pesquisar fundo, eles sofrem com as limitações.

### 2.2. Acesso estendido ao relatório

Além do &quot;Relatório no site&quot;, a maioria das ferramentas oferece funcionalidade estendida que permite que você leve sua análise para fora das ferramentas e crie algo um pouco mais personalizado.

#### 2.2.1. Adobe Analytics Report Builder (Extensão do Microsoft Excel)

O Workspace é uma ótima ferramenta, mas, às vezes, é necessário inserir seus dados em uma planilha personalizada, possivelmente para que você possa unir várias fontes de dados. É aqui que o Report Builder entra em cena.

O Report Builder é um plug-in para o Microsoft Excel que permite criar conexões com seus dados do Adobe Analytics para extrair dados tabulares que podem ser manipulados no Excel. Geralmente, para usar isso com eficiência, você puxava os dados em algumas guias de dados brutos, em seguida, usava referências de célula do excel para inserir dados dessas guias em um único relatório consolidado, em seguida, criava gráficos e visualizações.

>[!NOTE]
>
>O Report Builder tem uma permissão especial que precisa ser aplicada aos usuários para acessar este plug-in. Isso provavelmente só deve ser concedido para usuários que aprenderam a usar a ferramenta corretamente.

#### 2.2.2. Conexão da API do Adobe Analytics

Se você precisar que sua Adobe Analytics seja digerida por algo diferente do excel, mas ainda quiser os benefícios dos dados processados (incluindo as exclusões da regra de bot), poderá usar a API do Adobe para extrair dados diretamente, processá-los ou adicioná-los a um banco de dados para uso com outro sistema.

Observe que a API ainda extrai dados de correlação que aplicam os detalhamentos e segmentos conforme especificado na solicitação de pull.

O Adobe 2.1 (Seção 2.1) usa a API para criar todos os relatórios e, se você depurar o modo no Workspace, mostrará as chamadas de API usadas. Essa é uma forma rápida de criar chamadas de API usando o Workspace para criar e validar os dados que deseja obter, em seguida, use essas chamadas de API para obter os dados para seu próprio processamento.


#### 2.2.3. Google Analytics Data Studio

Se você já esteve, você já saberá de cima que eu mencionei o Data Studio como sendo um equivalente à leitura do Adobe Workspace. O Data Studio permite que você envie dados Google Analytics, mas também dados de outras fontes. Isso é bom se você quiser consolidar os dados analíticos com outros dados coletados; mas quando se trata de Google Analytics, encontrei o mesmo tipo de limitações de visualização que estão presentes no Google Analytics. A forma como as linhas e colunas são formadas ainda é muito limitada no que pode ser feito.

Ainda é uma ferramenta poderosa, e eu não desencorajaria as pessoas de usá-la de forma alguma, mas minha experiência pessoal é que por usar o Workspace por tanto tempo, eu pessoalmente acho o comportamento rígido bastante limitante.


#### 2.2.4. Extensão da planilha do Google

Para meus próprios usos, quando preciso extrair dados de maneira estendida do Google Analytics, minha ferramenta pessoal de escolha é a Extensão da planilha do Google. Claro, preciso fazer várias conexões com minhas tabelas de DG, mas como o Adobe, posso fazer referência às células de dados brutos e criar os relatórios que preciso e visualizá-las usando os recursos gráficos da Planilha do Google.


## 3. Exportações de dados brutos

Nessas ocasiões, você realmente precisa de dados brutos, tanto o Adobe quanto o Google oferecem os recursos para obter informações dessa maneira.

### 3.1. Feed de dados do Adobe

Na Seção 2.2.2, mencionei que a API do Adobe Analytics extraía de &quot;dados processados&quot;. O feed de dados brutos ainda extrairá os dados processados pelas &quot;Regras de processamento&quot; que foram configuradas no painel de administração (verifique se os dados brutos atrasados para garantir que todas essas regras tenham sido concluídas até o momento em que o feed de dados brutos for recebido), mas esses dados brutos incluirão todos os dados excluídos em qualquer outro lugar.

Isso significa que todas as exclusões de bot, dados filtrados por IP interno etc. serão incluídos nos feeds de dados brutos. Há sinalizadores para identificar esses dados, de modo que, se você estiver criando um lago de dados, sua equipe de engenharia poderá criar lógica para processar esses dados adequadamente.

Os feeds de dados brutos podem ser personalizados para enviar todas as colunas de dados, ou apenas colunas específicas se você precisar de um feed mais focado.

Os feeds podem ser enviados diretamente para FTP, SFTP, S3, etc.


### 3.2. Google Big Query

Infelizmente, essa é uma ferramenta Google que não tenho experiência em usar, mas em teoria deve ser semelhante ao Feed de dados Adobe, permitindo que sua equipe de engenharia acesse dados brutos de sua conta Google Analytics.

No entanto, acredito que em vez de um despejo completo de dados brutos, ele permite que seus engenheiros acessem os dados via queries SQL, para que possam obter dados brutos direcionados ou se quiserem que possam extrair todas as colunas de dados brutos para assimilar em um lago de dados.

## 4. Conclusão

Como qualquer sistema, é necessário praticar para se familiarizar com ele, mas espero que este guia o ajude a começar ou dê dicas para melhorar o uso do Adobe Analytics se você só arranhou a superfície.

No entanto, sublinharei que recomendaria usar tanto o Adobe Analytics quanto o Google Analytics na sua estratégia de implementação (mesmo que o Google Analytics seja apenas a versão gratuita). Isso permite ter um sistema de backup para garantir que você tenha dados, pois nenhum sistema é infalível.

Há muitos recursos disponíveis para você além deste guia que podem ajudar a melhorar sua estratégia:

* [Adobe Experience League](https://experienceleague.adobe.com/?lang=pt-BR#home) - Contém tutoriais, vídeos, documentação e fóruns da comunidade
* [Grupos de usuários do Adobe](https://analytics-augs.adobe.com/) - Um hub de eventos executados pela comunidade para ajudar os usuários a se conectarem entre si e melhorar suas implementações - porque eles são baseados em um fuso horário específico, é melhor verificar que outras regiões também estão funcionando.
* [Canal YouTube de grupos de usuários do Adobe Analytics](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) - Não foi possível criar uma sessão de grupo de usuários do Adobe Analytics? Assista novamente às sessões anteriores do grupo de usuários em todo o mundo para saber mais sobre como seus colegas estão usando a ferramenta.
* [Medir canal de Slack do Chat](https://www.measure.chat/) - Conecte-se com usuários do Adobe Analytics em todo o mundo e compartilhe aprendizados do setor, faça perguntas de seus colegas e participe de grupos de interesse com foco em medição.
* e mais!

## Autor

Este documento foi escrito por:

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, gerente de otimização do Analytics em Torstar

Adobe Analytics Campeão

