---
title: Como entender o painel de atribuição e as janelas de pesquisa do Adobe Analytics
description: Saiba como usar o Painel de atribuição e a Janela de pesquisa para entender o comportamento do cliente e personalizar como os itens de dimensão recebem crédito por eventos bem-sucedidos.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
source-git-commit: 48dbac6921a69dbdba1e98bf412ff55ceb27baf5
workflow-type: tm+mt
source-wordcount: '1881'
ht-degree: 2%

---


# Como entender o painel de atribuição e as janelas de pesquisa do Adobe Analytics

Saiba como usar o Painel de atribuição e a Janela de pesquisa para entender o comportamento do cliente e personalizar como os itens de dimensão recebem crédito por eventos bem-sucedidos.

## Utilização do painel Attribution 

![Deloreano](assets/delorean.png)

&#39;Excelente Scott!&#39;

Assim que pensei no [Painel de atribuição](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html) e **Janela de pesquisa**, lembrei-me da canção &quot;Back in Time&quot;, de Huey Lewis e da News; então, é claro, eu também fui lembrado que nossa resposta típica a muitas ferramentas novas como estas é simplesmente deixar de tentar usá-las, porque elas parecem tão complicadas.

Na verdade, veja todas essas opções, switches, painéis, leituras e nós.  E sério, vamos falar sobre esse condensador de fluxo.  Esperem, eu disse condensador de fluxo?

Ok, eu admito o **Painel de atribuição** é um instrumento bastante complexo; no entanto, nosso trabalho típico como analistas, dia após dia, é usar uma ferramenta altamente complexa para ver o que aconteceu no passado.  Essa ferramenta é chamada de **Adobe Analytics**!

Portanto, por que devemos deixar algo como um pouco de medo ficar no caminho de uma ferramenta tão legal e poderosa que nos permite literalmente olhar para trás no tempo todos os dias?

Estamos a falar disso, certo?  CERTO???! (Quero dizer, vamos, tenho certeza de que ainda está tudo bem e politicamente correto nos chamar de geeks?)

Ah, quem se importa?  Prepare-se, Geeks, Nerds, Goobers, Dwebs e Techies (sim até mesmo os Trekkies), eu posso ouvir o estéreo do carro agora:

&quot;Então me leve embora, não me importo!  Mas é melhor você me prometer... VOU VOLTAR A TEMPO!&quot;

Eu tenho a sua atenção agora, certo?  Ótimo!


Vamos dividir um pouco as coisas.  Agora que estamos todos entusiasmados **viagem no tempo**, vamos dar um passo para trás e estabelecer quais **Painel de atribuição** realmente é:

![Controle de tempo](assets/time-control.gif)

Não, não, não, não!  Não vamos nos distrair ainda.  Talvez, vamos tentar de novo:

![Janela de atribuição](assets/attribution-window.png)

Em **Atribuição**, considere apenas como os eventos/ações podem ser causados por um indivíduo, vários indivíduos ou uma ou várias coisas diferentes ao longo do tempo.

De acordo com [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-dataviews/component-settings/attribution.html), a atribuição oferece aos analistas a capacidade de personalizar como os itens de dimensão recebem crédito por eventos bem-sucedidos.  Na verdade, nenhuma jornada do cliente é realmente linear e é menos previsível.  Além disso, cada cliente continuará a seu próprio ritmo; muitas vezes, elas podem voltar, parar, sair ou se envolver em outros comportamentos não lineares. Essas ações orgânicas tornam difícil ou praticamente impossível saber o impacto dos esforços de marketing na jornada do cliente. Também dificultam os esforços para unir vários canais de dados.

Algum desses soa familiar a você?  Pense nisso no contexto da jornada de Marty McFly:

![Voltar ao Futuro 1](assets/back-to-the-future1.png)![Voltar ao Futuro 2](assets/back-to-the-future2.png)

Desde o momento em que ele fugiu do estacionamento do shopping Twin Pines até quando ele literalmente se jogou para fora do DeLorean antes de ser obliterado por uma locomotiva de 210 toneladas parece longe de ser linear, e não é nada que ninguém pudesse prever.

No entanto, através do poder da mágica cinematográfica, seguimos o caminho de Marty ao longo do tempo e compreendemos todos os seus pontos de contato, suas bancas, dorsos duplos e dropouts.

## Modelos de atribuição

Na vida real, podemos usar o **Painel de atribuição** para ver várias coisas diferentes.  Por exemplo, a variável **Modelos de atribuição** mostre-nos como **conversões** são distribuídos por **hits** em qualquer grupo específico.

Simplificando, se 10 pessoas pressionarem um botão para atravessar uma porta, nossos Modelos de Atribuição vão nos dizer qual dessas 10 pessoas nós queremos dar o crédito de apertar esse botão.  Pensando nisso, veja alguns exemplos de como os modelos de atribuição podem afetar essas 10 pessoas:
* **Primeiro contato**: Este é exatamente como parece.  Nesse caso, dá 100% de crédito à primeira pessoa que atravessou a porta.  Para isso, os profissionais de marketing têm mais probabilidade de usá-lo em táticas como Social ou Exibição, mas geralmente é uma ótima tática para a eficácia da recomendação de produtos no site.
* **Último contato**: Também é exatamente como soa.   Este modelo dá 100% de crédito à última pessoa que entrou na porta.  Esse modelo geralmente é usado para analisar coisas como Pesquisar e campanhas de ciclo de marketing de curto prazo.
* **Linear**: Isto dá crédito igual a todas as pessoas que atravessaram a porta.  Isso mesmo - Você pega um DeLorean, e você pega um DeLorean, e você pega um DeLorean.  TODO MUNDO TEM UM DELOREANO!!!
* **Forma de U**: Este dá 40% do crédito ao primeiro na porta, espalha 20% do crédito para todos no meio e depois dá 40% ao último.  Pense em uma situação em que você deseja reconhecer a maioria das conversões tanto na frente quanto no back-end, mas também quer borrifar uma pequena parte do crédito através de algumas das interações que contribuem no meio.
* **Declínio de tempo**: Eu ficaria em falta se não compartilhasse este com vocês antes de enviá-los para a documentação oficial para revisar os modelos restantes.  Tal como o plutônio de Doc Brown, este modelo tem literalmente uma meia-vida que decai exponencialmente!  Nesse caso, o parâmetro padrão para a meia-vida desse modelo é de 7 dias.  A maneira como funciona é aplicar peso a cada Canal de marketing, com base na quantidade de tempo que passa após o ponto de contato inicial e quando o cliente converte.

Para obter mais informações sobre isso e o restante **Modelos de atribuição**, [clique aqui](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=pt-BR).

Para tornar isso ainda mais interessante, vamos falar sobre o **Janelas de pesquisa**.

Sim, aqui vamos nós... nos leve de volta a tempo!!  Porque é aqui que começa a diversão!

Adobe define **Janelas de pesquisa** como &quot;a quantidade de tempo que uma conversão deve retroceder para incluir pontos de contato. Os modelos de atribuição que dão mais crédito às primeiras interações veem diferenças maiores ao exibir diferentes janelas de retrospectiva.&quot;

* **Janela de retrospectiva de visita**: Retorna ao início de uma visita quando ocorreu uma conversão.
* **Janela de retrospectiva do visitante**: Verifica todas as visitas até o primeiro dia do mês do intervalo de datas atual.
* **Janela de pesquisa personalizada**: Permite expandir a Janela de atribuição além do intervalo de datas do relatório até um máximo de **90 dias**.

Se vocês viram TODOS os filmes de Volta para o Futuro, então vocês sabem que Marty McFly voltou no tempo mais de uma vez, e vocês também sabem que ele voltou para 1955 mais de uma vez.  Se dependermos da aquisição do &quot;Gray&#39;s Sports Almanac&quot; como nosso evento de conversão, considere o seguinte:

![Esportes - Almanaque](assets/sports-almanac.png)

1. Um pouco antes **1:30** on **26 de outubro de 1985** Marty McFly volta a tempo **5 de novembro de 1955**, onde ele corre pela primeira vez sobre um pínus em um DeLorean viajando o tempo.  Na semana seguinte e meia, ele interage com várias pessoas, incluindo seus pais, afetando o futuro, por influência de seu pai para se levantar para um valentão chamado Biff, de modo que seu pai pode perceber seu próprio potencial para se tornar um autor bem-sucedido de ficção científica.
1. Mais tarde na mesma manhã **26 de outubro de 1985** Então, o Doutor Emmett Brown chega na entrada de Marty McFly para informar a ele e à namorada que algo correu terrivelmente mal com seus filhos e eles devem correr para o futuro para corrigir seus problemas.  À medida que saem, a partida é testemunhada por Biff, que acha estranho ver um DeLorean voador.  Mais tarde, no futuro, como Biff testemunha novamente um DeLorean voador e, mais tarde, pega de vista &quot;duas versões&quot; de Marty, ele começa a juntar as coisas.   Quando ouve Doc Brown e Marty argumentando como a &quot;máquina do tempo&quot; nunca deve ser usada para ganhos pessoais e apenas para pesquisa (porque Marty estava se debruçando sobre levar um almanaque esportivo de volta ao passado para fazer algumas apostas pessoais), Biff rouba a máquina do tempo enquanto os dois estão distraídos em entregar o almanaque esportivo a seu próprio jovem no passado.
1. Depois de sua viagem ao futuro, Doc Brown e Marty retornam a um **26 de outubro de 1985** eles não reconhecem, e eles deduzem que a linha do tempo foi alterada por um mau Biff.  Percebendo que eles devem corrigir o que aconteceu, Doc e Marty resolvem retornar para **12 de novembro de 1955**, a fatídica noite em que tudo foi mudado por Marty quando ele visitou pela primeira vez **1955**.  Doc e Marty acabam salvando o dia roubando o almanaque esportivo que o velho Biff do futuro tinha entregue a Young Biff em **1955** Mas não sem outra reviravolta, você realmente precisa assistir a trilogia completa de filmes para realmente aproveitar e entender.

Dependendo do **Modelo de atribuição** e **Janela de pesquisa**, podemos acabar com alguns cenários interessantes:

* Usando **primeiro contato** e **janela de retrospectiva de visita**, a atribuição considera a visita de Marty, onde ocorreu a mais recente &quot;conversão&quot;, que foi quando ele e Doc conseguiram roubar o almanaque esportivo de Young Biff e mantiveram sua aversão ao estrume.

![Biff 1](assets/biff1.png)![Biff 2](assets/biff2.png)

* Acredite ou não, usando **primeiro contato** e **janela de retrospectiva de visitante**, a atribuição favoreceria a conversão em que Biff vence.
* Aplicar um **janela de pesquisa linear** resultaria em um multi-verso em que cada linha do tempo existe.  Desculpe, isso não é **Maravilha** ou **Star Trek**!

E nesse ponto, espero que vocês estejam começando a entender a ideia.

Então, o que tudo isso significa para nós como analistas?

O **Painel de atribuição** e **Janela de pesquisa** nos dê o poder de olhar além dos dados simples e de nível de superfície e mergulhe mais fundo na jornada do cliente. Ao entender quais pontos de contato tiveram maior impacto nas conversões, podemos tomar decisões informadas sobre nossas estratégias de marketing e alocar recursos com mais eficiência.

Lembre-se, depois de ter seu **Modelos de atribuição** e **Janelas de pesquisa** selecionado, você ainda tem a capacidade de manipular seus dados filtrando-os com um segmento ou qualquer outro componente que desejar.  Além disso, depois que o Painel for renderizado, você terá toda a funcionalidade de um **Workspace**, o que significa que você está oficialmente licenciado para dirigir 88 mph!

## Finalmente, pondo-a em prática

Agora que você tem os conceitos reduzidos, imagine que está realizando uma campanha de marketing e tentando determinar qual canal é mais eficaz para gerar conversões. Com a ajuda do **Painel de atribuição**, você pode ver não somente a variável **Último contato**, mas também o **Primeiro contato**, **Mesmo contato** e qualquer outro modelo que você escolher, para determinar quais canais são os mais eficazes na condução de suas conversões. Em seguida, essas informações podem ser usadas para otimizar suas campanhas e melhorar o desempenho geral.

Agora que viram o que pode fazer, não se intimidem pelas características aparentemente complexas da **Painel de atribuição**.  **Face** sim.  **Embraço** sim.  **Entender** sim.  Acima de tudo, use-o em sua vantagem. O **Painel de atribuição** e **Janela de pesquisa** são as chaves para desbloquear uma compreensão mais profunda de seus clientes e de suas jornadas com sua marca.

Agora, podemos viajar &quot;de volta no tempo&quot; com confiança e usar o poder de nossa confiável máquina do tempo (também conhecida como  **Adobe Analytics**) tomar decisões orientadas para os dados; e, o mais importante, lembre-se, &quot;Para onde vamos, não precisamos de estradas!&quot; (Apenas um condensador de fluxo e um olho forte para atribuição!)

![De volta ao futuro](assets/back-to-the-future3.png)

## Autora

Este documento foi escrito por:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, Gerente, Análise digital no Kroger Personal Finance

Especialista em Adobe Analytics
