---
title: Um guia abrangente para a transição do Google Analytics para o Adobe Analytics
description: Um dos maiores desafios na transição entre quaisquer ferramentas é saber onde encontrar a funcionalidade equivalente e aprender a usá-la com eficiência. Esta discussão faz parte de um guia maior, cujo objetivo é ajudar os usuários a fazerem a transição para o Adobe Analytics.
feature: Third-party Integration
role: User
level: Beginner
doc-type: feature video
thumbnail: 34749.jpg
kt: 9830
exl-id: b2be6081-a1c0-4435-affb-454ed5a74662
source-git-commit: de78868e07b0fa59a7babc092c463bbe4d8e2da7
workflow-type: ht
source-wordcount: '3690'
ht-degree: 100%

---

# Um guia abrangente para a transição do Google Analytics para o Adobe Analytics

## 1. Introdução

Um dos maiores desafios na transição entre quaisquer ferramentas é saber onde encontrar a funcionalidade equivalente e aprender a usá-la com eficiência. Esta discussão faz parte de um guia maior, cujo objetivo é ajudar os usuários a fazerem a transição para o Adobe Analytics (seja como um novo usuário ou como usuário do Google Analytics) com mais facilidade. Uma comparação aprofundada com o GA, que possivelmente é a ferramenta com a qual a maioria dos usuários está familiarizada, será fornecida para ajudar os usuários a correlacionar o conhecimento existente com o novo conjunto de ferramentas. Embora nada substitua prática, este artigo ajudará você a começar, e esperamos que também diminua as frustrações que talvez você encontre durante esse período (ou mesmo como um lembrete depois de começar a entrar no ritmo das coisas).

Também devemos fazer uma rápida comparação de terminologia:

| **Descrição** | **Adobe Analytics** | **Google Analytics** |
|--------------------------------------------------------------------------------------------------------------------------------|---------------------|----------------------|
| Uma métrica de evento que representa que uma página (ou tela em um aplicativo) foi visualizada | Exibição de página | Pageview |
| Uma métrica que representa um grupo de interações no site ou aplicativo que ocorrem no mesmo intervalo de tempo | Visita | Sessão |
| Uma métrica que define um dispositivo identificado (com base em vários critérios, incluindo cookies e outros padrões de comportamento para unir informações do usuário) | Visitante único | Usuário |

## 2. As interfaces

Uma das coisas que vejo com mais frequência quando as pessoas comparam o Adobe Analytics com o Google Analytics é que o Adobe Analytics tem muitas informações, o que é um tanto intimidador para as pessoas. Embora isso seja verdade, isso é também uma força, não uma fraqueza. O Adobe Analytics oferece uma grande variedade de ferramentas e flexibilidade na visualização de dados, permitindo que você tenha muito mais liberdade para criar o que precisa.

Vamos começar observando os relatórios &quot;no site&quot;.

### 2.1. Relatórios no site

#### 2.1.1. Tela inicial

Tanto o Adobe Analytics quanto o Google Analytics fornecem uma maneira de personalizar a primeira visualização que um usuário vê ao fazer logon.

##### 2.1.1.1. Espaço de trabalho / Configuração personalizada da tela inicial (Adobe Analytics)

O Adobe Analytics não apresenta um relatório pré-construído para todos os usuários visualizarem ao fazer logon. A página inicial padrão leva o usuário para a tela inicial do Espaço de trabalho, que mostrará a cada usuário todos os relatórios do espaço de trabalho que ele criou ou que foram compartilhados com ele. Além disso, cada usuário tem a capacidade de definir qualquer um desses relatórios como sua tela inicial, se desejar.

![image1](assets/ga-to-aa_1.png)

Detalhes sobre o espaço de trabalho serão apresentados mais adiante neste guia. Consulte a Seção 2.1.2.1

>[!TIP]
>
>Crie alguns relatórios padrão e compartilhe com os outros da sua organização para que eles tenham um ponto de partida e vejam as informações sem que precisem criar os próprios relatórios imediatamente.



##### 2.1.1.2. Insights da Tela inicial (Google Analytics)

* A Tela inicial do Google Analytics tem algumas visualizações pré-construídas para você.  Elas abrangem, por exemplo:
* Usuários, Sessões, Taxa de rejeição e Duração da sessão nos últimos sete dias
* Usuários por hora do dia nos últimos 30 dias
* Usuários atuais agora e Principais páginas ativas
* Canal de tráfego, Origem/Meio e Referências nos últimos sete dias
* Sessões por país nos últimos sete dias
* Principais páginas dos últimos sete dias
* Tendência de usuários ativos nos últimos 30 dias
* e mais

No GA4, os usuários têm mais opções para personalizar e adicionar seus próprios relatórios à tela inicial.

![image2](assets/ga-to-aa_2.png)

Esse provavelmente é o item que fará mais falta ao vir para a Adobe. Não há uma tela inicial pré-construída para você, mas é possível configurar facilmente um espaço de trabalho personalizado para replicar o que você precisa acima e, se desejar, defini-lo como tela de aterrissagem. Mais informações sobre isso posteriormente (ou consulte a Seção 2.1.2.1, sobre o Espaço de trabalho da Adobe).

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

![image3](assets/ga-to-aa_3.png)

As tabelas de forma livre permitem ter várias colunas e segmentação, conforme necessário, para visualizar os dados da maneira que você desejar.

A partir da tabela acima, gostaria de visualizar um detalhamento por data? Arraste e solte outra dimensão ou segmento ali para ver os dados de uma maneira diferente. Talvez usando segmentos para o Tipo de dispositivo e, em seguida, adicionando um detalhamento por SO para seus usuários de celular/tablet:

![image3](assets/ga-to-aa_4.png)

O Espaço de trabalho permite que sua criatividade flua, você não fica limitado a detalhamentos &quot;padrão&quot;. Você pode criar as visualizações necessárias para aprofundar as comparações que precisam ser executadas.

>[!TIP]
>
>Não tenha medo de experimentar e explorar. Há muitas maneiras de aproveitar essa ferramenta e ver o que você pode fazer. Apenas certifique-se de tentar validar se o que você criou está realmente mostrando o que você acha que está. Sua experiência contará muito nessa hora.

Você pode até criar métricas calculadas dinamicamente ou segmentos localizados somente dentro do relatório. Isso evita que seu segmento e repositório de cálculos fiquem cheios, mas também garante que você crie itens focalizados necessários para relatórios específicos sem confundir sua organização com itens que não sejam muito úteis em outros contextos.

Esta discussão é apenas uma apresentação a esta ferramenta. Haverá outros guias mais abrangentes para começar, mas quando você fizer isso, poderá criar relatórios mais completos como:

![image3](assets/ga-to-aa_5.png)

Observe também que os espaços de trabalho não são salvos automaticamente, portanto, é mais fácil fazer um relatório ad-hoc único sem obstruir o repositório de relatórios.

Outro recurso poderoso dos espaços de trabalho é a capacidade de aplicar modificadores interativos a seus relatórios na forma de menus suspensos. Embora esses menus suspensos não funcionem em arquivos CSV ou PDF exportados de seus relatórios, no relatório em tempo real eles permitem atualizar todas as visualizações em um painel para mostrar o mesmo relatório em condições diferentes. Vários menus suspensos podem ser usados e, desde que as opções não sejam mutuamente exclusivas, os itens selecionados serão empilhados para apresentar informações de maneira clara.

>[!IMPORTANT]
>
>Para saber mais sobre o uso de menus suspensos e detalhamentos de forma livre, consulte <https://experienceleaguecommunities.adobe.com/t5/adobe-analytics-discussions/the-power-of-dropdown-filters-and-dimension-breakdowns-in-adobe/td-p/434680>

##### 2.1.2.2. Google Analytics: painéis, relatórios personalizados e relatórios salvos

O Google tem algumas ferramentas para criar relatórios na interface, mas seguem a mesma exibição e limitações da seção de relatórios.

Ao ler isto, os versados em Google Analytics podem pensar: &quot;Mas o Google Data Studio não é um equivalente melhor em relação ao Espaço de trabalho, da Adobe&quot;? Isso até estaria correto, mas como o Data Studio tecnicamente não faz parte da ferramenta do Analytics e permite conexões com diferentes fontes de dados, ela será abordada posteriormente na seção &quot;Acesso a relatórios estendidos&quot; desta discussão (especificamente, na Seção 2.2.3)

Os painés do Google e os relatórios personalizados permitem que você reúna várias visualizações em um único relatório, mas ao contrário do Espaço de trabalho, você ainda fica limitado a correlações simples e a quais dados podem ser colocados em quais colunas.

Nos relatórios personalizados, um dos maiores desafios é o fato de que, ao criar um filtro, ele é aplicado a todas as guias do relatório. Logo, não há como comparar dois filtros diferentes no mesmo relatório.

Ele funciona para comparações simples. Todos são semelhantes aos Painéis herdados, aos Relatórios personalizados e aos Marcadores da Adobe. São ferramentas básicas fornecidas para atender às suas necessidades, que estão no conjunto de relatórios.

#### 2.1.3 Relatórios

O Google e a Adobe têm alguns relatórios navegáveis que são tabelas pré-construídas e gráficos de linha do tempo básicos baseados em uma dimensão.

##### 2.1.3.1. Relatórios do Adobe Analytics

O Adobe Analytics também apresenta uma seção Relatórios, embora boa parte dela esteja sendo removida em favor do Analysis Workspace (na verdade, o fim da vida útil foi anunciado para essa interface, uma vez que o Espaço de trabalho [Seção 2.1.2.1] é uma ferramenta muito mais poderosa). Nele, a maioria dessas tabelas pode ser criada e modificada com mais facilidade. As seções da Adobe são muito mais detalhadas, e isso pode ser intimidante:

![image3](assets/ga-to-aa_6.png)

Com a maior parte das informações acima acessíveis por meio dos Espaços de trabalho, darei uma breve visão geral dessas seções e como elas se relacionam com o Google Analytics, destacando também os relatórios que ainda são relevantes.

Métricas do site é algo que já conhecemos. Abrange as métricas padrão (exibições de página, visitantes únicos, visitas, bem como eventos personalizados configurados). É semelhante ao Relatório de comportamentos do GA, mas também inclui parte do que você encontraria no Audience (já que a Adobe não divide os tipos de métrica).

Aqui, você também encontrará os relatórios de &quot;Bot&quot;. O tráfego de bots é excluído de todos os seus relatórios padrão, no entanto, há dois relatórios que permitem que você veja alguns insights sobre o que está acontecendo e quais bots estão chegando ao seu site. Isso é especialmente bom se você configurar regras de bot personalizadas para excluir bots de spam conhecidos que acessam frequentemente seu site. Você pode obter alguns insights sobre o que esses bots estão fazendo sem que seus relatórios principais sejam inundados por esse tráfego. Os relatórios de bot estão indisponíveis no Espaço de trabalho (mas os novos recursos de relatório em breve também permitirão que os usuários obtenham essas informações lá).

O conteúdo do site é um agrupamento de dimensões padrão da Adobe: Nome da página, Seções do site (Canais), Hierarquias (uma maneira de criar relatórios detalhados personalizados de organização em seu site), Servidores (particularmente útil se você tem vários subdomínios no site ou está marcando vários sites juntos em um conjunto de rastreamento) etc. Todos estão disponíveis no Espaço de trabalho.

A seção Dispositivos móveis é um agrupamento de dados específicos de dispositivos móveis, como dispositivos, tipos de dispositivos etc. Todos estão disponíveis no Espaço de trabalho.

Caminhos é outro desses itens &quot;não totalmente disponíveis no Espaço de trabalho&quot;. Embora o Espaço de trabalho tenha um diagrama de Fluxo, você só pode ver os fluxos de entrada e saída para uma única página/valor, enquanto Caminhos permite que você veja os caminhos mais comuns usados no site. Por padrão, Páginas é o primeiro relatório de caminho configurado para você, mas você pode ativá-lo para propriedades personalizadas (por exemplo, para rastrear um valor de &quot;tipo de página&quot; você pode ver a definição de caminho dentro dos tipos de página). A outra coisa interessante em Caminhos é a maneira simples como as informações são apresentadas. O diagrama de fluxo no espaço de trabalho (dependendo da quantidade que você está tentando ver) pode ficar grande. Recomendo experimentar ambos. Cada um tem seu uso e valor, dependendo do que você está tentando fazer. Observe que qualquer dimensão pode ser usada em Fluxos, enquanto a Definição de caminho deve ser configurada em uma propriedade no painel administrativo.

Os relatórios de Fontes de tráfego, Campanhas e Canais de marketing são semelhantes ao relatório de Aquisição no Google. As Fontes de tráfego se concentram nos Referenciadores reais e as Campanhas se concentram nos Códigos de Campanha. Os Canais de marketing também se concentram nos Códigos de campanha, mas aplicam uma lógica extra, determinada por você, sobre como processar as informações. Acho que a Adobe oferece muito mais liberdade em como configurar suas regras. O Google faz muitas coisas para você, e isso será uma mudança na mentalidade. Também deve ser observado que, por padrão, a atribuição do Google nos Códigos de campanha é de seis meses, e a da Adobe é definida por padrão como uma semana. Isso pode ser alterado nas configurações de administrador, mas no Espaço de trabalho é possível aplicar uma atribuição personalizada sobre qualquer dimensão, proporcionando muito mais flexibilidade &quot;instantânea&quot;.

Os relatórios de Retenção de visitante e Perfil do visitante são semelhantes aos relatórios de Público-alvo no Google Analytics. O foco da Retenção está mais na frequência de retorno, enquanto o foco do Perfil do visitante está mais na geografia e tecnologia dos usuários.

Conversão personalizada e Tráfego personalizado são relatórios de dimensão personalizados. Conversões são seus eVars (em que você pode definir um termo personalizado para o valor, ou seja, ocorrência, visita, mês, ano etc., e esse valor permanecerá para esse usuário pelo tempo especificado, a menos que seja substituído). As Variáveis de tráfego são as suas propriedades, mas você também pode configurá-las para Relatórios de definição de caminho ou como itens de lista (que detalharão vários valores com base em um delimitador de sua escolha).

A Mídia é para coisas como vídeos ou arquivos de áudio, onde você configurou um rastreamento de mídia especial.

Relatórios personalizados é uma seção na qual um usuário pode personalizar as colunas e os detalhamentos criados na interface dos relatórios e salvá-los como um relatório personalizado. No entanto, como mencionado acima, como o Espaço de trabalho permite detalhamentos e correlações muito mais poderosas, qualquer item personalizado deve ser feito lá. Essa era uma boa solução antes de o Espaço de trabalho existir.

A seção Marcadores é semelhante aos Relatórios personalizados, onde os relatórios usados com frequência podem ser marcados na interface dos relatórios para facilitar sua localização.

O Painel era um produto herdado que permitia às pessoas combinarem reportlets de dados em uma visualização. No entanto, a funcionalidade no Espaço de trabalho (Seção 2.1.2.1) é tão mais fácil de usar, que só existe como um ponto de acesso para relatórios herdados que devem ser recriados antes que esse recurso seja descontinuado.

Metas é uma área de relatório especial que permite às pessoas criar um relatório com base em uma meta em um determinado período para que as equipes possam monitorar coisas, como campanhas, e ver se estavam no caminho para atingir suas metas de tráfego.

Todos os relatórios aqui permitiam várias colunas de métrica e detalhamentos de dimensão, mas a simplicidade das visualizações e parte da lógica por trás de quais elementos podiam ser correlacionados poderia ser frustrante às vezes.

##### 2.1.3.2. Relatórios do Google Analytics

O Google Analytics divide esses relatórios nas seguintes seções: Tempo real, Público-alvo, Aquisição, Comportamento e conversas (no GA3) e Ciclo de vida (com as subseções: Aquisição, Envolvimento, Monetização, Retenção) e Usuário (com as subseções: Demografia e tecnologia).

![image3](assets/ga-to-aa_7.png)

É possível fazer pequenos ajustes nessas visualizações, adicionar um detalhamento de dimensão secundária, alterar a visualização, criar um filtro nos dados etc. Você pode salvar suas personalizações como um Relatório salvo.

Elas fornecem insights rápidos e fáceis para seus dados. No entanto, você não pode comparar itens como Usuários à exibições de página, para uma página na mesma tabela, e não pode adicionar mais de uma dimensão extra para ver dados adicionais.

São boas para dados analíticos rápidos, mas se você realmente precisa pesquisar fundo, elas sofrem com as limitações.

### 2.2. Acesso estendido ao relatório

Além do &quot;Relatório no local&quot;, a maioria das ferramentas oferece funcionalidade estendida que permite levar sua análise para fora das ferramentas e criar algo um pouco mais personalizado.

#### 2.2.1. Adobe Analytics Report Builder (Extensão do Microsoft Excel)

O Espaço de trabalho é uma ótima ferramenta, mas, às vezes, é necessário inserir seus dados em uma planilha personalizada, para que você possa unir várias fontes de dados. O Report Builder pode ajudar nessas situações.

O Report Builder é um plug-in para o Microsoft Excel que permite criar conexões com seus dados do Adobe Analytics e assim extrair dados tabulares que podem ser manipulados no Excel. Geralmente, para usar isso com eficiência, você puxaria os dados para algumas guias de dados brutos, usaria referências de células do Excel para extrair dados dessas guias em um único relatório consolidado e criaria gráficos e visualizações.

>[!NOTE]
>
>O Report Builder tem uma permissão especial que precisa ser aplicada aos usuários para acessar este plug-in. Isso provavelmente só deve ser concedido a usuários que aprenderam a usar a ferramenta corretamente.

#### 2.2.2. Conexão da API do Adobe Analytics

Se você precisar que seu Adobe Analytics seja assimilado por algo diferente do Excel, mas ainda quiser os benefícios dos dados processados (incluindo as exclusões de regras de bot), poderá usar a API da Adobe para extrair os dados diretamente e processá-los por meio de script ou adicionar a um banco de dados para uso com outro sistema.

Observe que a API ainda extrai dados de correlação aplicando os detalhamentos e segmentos conforme especificado na solicitação de envio.

O Espaço de trabalho da Adobe (Seção 2.1.2.1) usa a API para criar todos os relatórios e, se você hablitar o modo depurar, no Espaço de trabalho, ele mostrará as chamadas de API usadas. É uma maneira rápida de criar chamadas de API usando o Espaço de trabalho para criar e validar os dados que você deseja extrair e, em seguida, usar essas chamadas de API para obter os dados para seu próprio processamento.


#### 2.2.3. Google Analytics Data Studio

Se você está lendo este documento, já sabe que mencionei o Data Studio como equivalente ao Espaço de trabalho da Adobe. O Data Studio permite extrair dados do Google Analytics, e também dados de outras fontes. Isso é bom se você deseja consolidar seus dados de análise com outros dados coletados; mas quando se trata do Google Analytics, encontrei o mesmo tipo de limitação de visualização que está presente no Google Analytics. A forma como as linhas e colunas são formadas ainda limita muito o que pode ser feito.

Ainda é uma ferramenta eficiente, e eu não desaconselharia as pessoas de usá-la de forma alguma. Mas pela minha experiência pessoal de ter usado o Espaço de trabalho por tanto tempo, o comportamento rígido é bastante limitante, na minha opinião.


#### 2.2.4. Extensão das Planilhas Google

Para uso próprio, quando preciso extrair dados de maneira estendida do Google Analytics, minha ferramenta pessoal de escolha é a extensão de planilhas do Google. Claro, preciso fazer várias conexões com minhas tabelas do GA, mas com o Report Builder da Adobe, posso fazer referência às células de dados brutos, criar os relatórios que preciso e depois visualizá-las usando os recursos gráficos do Planilhas Google.


## 3. Exportações de dados brutos

Há ocasiões em que realmente precisamos de dados brutos. Tanto a Adobe quanto o Google oferecem os recursos para obter informações nesse formato.

### 3.1. Feed de dados da Adobe

Na Seção 2.2.2, mencionei que a API do Adobe Analytics extraía de &quot;dados processados&quot;. O feed de dados brutos ainda extrairá dados processados pelas &quot;Regras de processamento&quot; que foram configuradas no painel do administrador (verifique se os dados brutos estão atrasados para garantir que todas essas regras sejam concluídas no momento em que o feed de dados brutos for extraído). Mas esses dados brutos incluirão todos os dados excluídos em todos os outros lugares.

Isso significa que todas as exclusões de bot, dados filtrados por IP interno etc., serão incluídos nos feeds de dados brutos. Caso você esteja criando um data lake, existem sinalizadores que identificam esses dados, para que sua equipe de engenharia possa criar uma lógica para processar esses dados adequadamente.

Os feeds de dados brutos podem ser personalizados para enviar todas as colunas de dados ou apenas colunas específicas se você precisar de um feed mais focado.

Os feeds podem ser enviados diretamente para FTP, SFTP, S3 etc.


### 3.2. Google Big Query

Trata-se de uma ferramenta do Google que não tenho experiência em usar, mas que deve ser semelhante ao feed de dados da Adobe. Com ela, a equipe de engenharia acessa dados brutos direto da conta do Google Analytics.

No entanto, em vez de um despejo completo de dados brutos, a ferramenta permite que os engenheiros acessem os dados por meio de consultas SQL, para que possam extrair dados brutos direcionados ou, se desejarem, extrair todas as colunas de dados brutos para assimilar em um data lake.

## 4. Conclusão

Como qualquer sistema, é necessário praticar para se familiarizar com ele. Mas espero que este guia o ajude a começar ou forneça dicas para melhorar o uso do Adobe Analytics, caso você seja iniciante.

No entanto, eu recomendaria o uso do Adobe Analytics e do Google Analytics em sua estratégia de implementação (mesmo que o Google Analytics seja apenas a versão gratuita). Isso permite ter um sistema de backup para garantir que você tenha dados, pois nenhum sistema é infalível.

Há muitos recursos disponíveis para você além deste guia que podem ajudar a melhorar sua estratégia:

* [Adobe Experience League](https://experienceleague.adobe.com/?lang=pt-BR#home) - Contém tutoriais, vídeos, documentações e fóruns da comunidade
* [Grupos de usuários da Adobe](https://analytics-augs.adobe.com/) - Um centro de eventos conduzidos pela comunidade para ajudar os usuários a se conectarem entre si e melhorarem as implementações. Como eles são baseados em um determinado fuso horário, também é recomendado verificar os eventos conduzidos por outras regiões.
* [Canal YouTube de grupos de usuários do Adobe Analytics](https://www.youtube.com/channel/UCQOHnCs7KZgsuFHVzwboQuA) - Não foi possível criar uma sessão de grupo de usuários do Adobe Analytics? Assista novamente às sessões anteriores de grupos de usuários em todo o mundo para saber mais sobre como seus colegas estão usando a ferramenta.
* [Canal de chat do Slack para medições](https://www.measure.chat/) - Conecte-se com usuários do Adobe Analytics em todo o mundo e compartilhe aprendizados do setor, faça perguntas a seus colegas e participe de grupos de interesse com foco em medição.
* e mais!

## Autora

Este documento foi escrito por:

![Jennifer Dungan](assets/Jennifer_Dungan_Headshot150.png)

Jennifer Dungan, gerente de otimização de análise da Torstar

Especialista em Adobe Analytics

