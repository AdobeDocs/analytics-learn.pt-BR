---
title: Como entender o painel de atribuição do Adobe Analytics e as janelas de pesquisa
description: Saiba como usar o painel de atribuição e a janela de pesquisa para entender o comportamento do cliente e personalizar como os itens de dimensão recebem crédito por eventos bem-sucedidos.
feature: Attribution
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-06-20T00:00:00Z
jira: KT-13181
thumbnail: KT-13181.jpeg
exl-id: 1da9334b-0edb-4237-b7ca-57640865208c
source-git-commit: f1bb981a83eb698f4185a22c367346a9ddd0c755
workflow-type: tm+mt
source-wordcount: '1659'
ht-degree: 1%

---

# Como entender o painel de atribuição do Adobe Analytics e as janelas de pesquisa

Quando eu pensei pela primeira vez sobre o [painel de atribuição](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=pt-BR) e a **janela de retrospectiva**, lembrei-me imediatamente do conceito de &#39;*viagem no tempo&#39;*; então, é claro, também lembrei-me da resposta típica a muitas ferramentas novas como essas que é simplesmente parar de tentar usá-lo, porque elas parecem tão complicadas.

Quero dizer, honestamente, basta olhar para todas essas opções, interruptores, painéis, leituras, e botões.  E sério, vamos falar sobre essas complicadas luzes piscando, mangueiras, medidores... ESPERE!  Não é hora de distrair falando de máquinas do tempo, só não temos tempo... ou temos?

Vou admitir que o **painel de atribuição** é uma ferramenta bastante complexa; no entanto, nosso trabalho típico como analistas, dia após dia, é usar outra de nossas ferramentas favoritas e altamente complexas para também observar o que aconteceu no passado. Esta ferramenta chama-se ***Adobe Analytics***!  Então sim, para responder a nossa pergunta muito relevante, eu acredito que estas duas coisas dizem que temos muito tempo.

Portanto, por que devemos permitir que algo como um pouco de medo interfira com ferramentas tão surpreendentes, sofisticadas e poderosas como essas que literalmente nos permitem olhar *para trás* no tempo, todos os dias?

Afinal - esta é a VIAGEM NO TEMPO, pessoal!!  Somos todos sobre esse tipo de coisa.  Certo???!!

Então, o que estamos esperando - um carro de metal brilhante, uma caixa de polícia, ou uma cabine telefônica vintage usando a fiação de um guarda-chuva velho como sua antena para aparecer em nossa porta?

Não!  Temos algo ainda melhor, então vamos nos amarrar e esperar!

Bem... você entendeu a ideia.


Agora que estamos todos entusiasmados com a viagem no tempo, vamos respirar fundo, voltar um pouco, estabelecer o que é o **painel de atribuição** *realmente* e detalhar um pouco:

![Atribuição](assets/attribution.png)

*Figura 1 - Os números exibidos estão alinhados com o texto abaixo*

Em **attribution**, considere apenas como eventos/ações podem ser causados por um indivíduo, por vários indivíduos ou por um de vários eventos diferentes ao longo do tempo.

De acordo com o [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=pt-BR), a *atribuição* oferece aos analistas a capacidade de personalizar como os itens do *Dimension* recebem crédito por *eventos bem-sucedidos*.


>[!WARNING]
>
>**Os modelos de atribuição** são tão frequentemente associados a **canais de marketing** que eu *risquei* ❷ o CANAL na imagem acima para ilustrar que é possível executar a análise de **atribuição** comparando-a com a maioria das outras ***dimensões***.


Na verdade, raramente uma determinada jornada de cliente é realmente linear e menos previsível.  Além disso, cada cliente continuará em seu próprio ritmo; com frequência, ele pode voltar, parar, sair ou adotar outros comportamentos não lineares. Essas ações orgânicas dificultam ou são praticamente impossíveis de saber o impacto dos esforços de marketing na jornada do cliente. Também dificultam os esforços para unir vários canais de dados.

Isso mesmo.  Deixe suas analogias &quot;dominó&quot; na porta e abra suas mentes para conceitos mais nos moldes do efeito borboleta e da teoria das cordas - mas como tudo o mais, precisamos começar com alguns dos fundamentos.

## **Modelos de atribuição**

Quando usamos o **painel de atribuição**, podemos começar a observar várias coisas diferentes.  Por exemplo, os **modelos de atribuição** demonstram como nossas *conversões* (ou seja, ❶ **métricas de sucesso**) podem ser distribuídas entre *ocorrências* em qualquer grupo específico.

Simplificando, se **10 pessoas** pressionarem um **BOTÃO VERMELHO GRANDE** para passarem pela porta, nossos **modelos de atribuição** nos dirão quais **10 pessoas** queremos atribuir &quot;crédito&quot; - ou melhor, quanto *muito* &quot;crédito&quot; queremos atribuir - para pressionar o botão dito.

![Botão](assets/button.png)

Tendo isso em mente, aqui estão alguns exemplos de como os ❸ **modelos de atribuição** podem afetar essas **10 pessoas**:

- **Primeiro contato**: este modelo funciona exatamente como parece dando **100% de crédito** à pessoa *primeira* que entrou pela porta.  Os profissionais de marketing têm mais probabilidade de usar essa abordagem para táticas como ***mídia social*** ou ***exibição***; no entanto, também é uma ótima tática para usar com frequência na eficácia das recomendações de produtos no site.
- **Último contato**: esta tática também funciona exatamente como parece, mas oferece **100% de crédito** à ÚLTIMA pessoa que entrou pela porta.  Normalmente, esse modelo é usado para analisar coisas como a ***pesquisa natural (orgânica)*** e outras *campanhas de curto prazo* do ciclo de marketing.
- **Linear**: este modelo distribui crédito igual para TODAS AS PESSOAS que passaram pela porta.

  >[!CAUTION]
  >
  >No entanto, recomenda-se cautela aqui, porque você tem o potencial de espalhar seus resultados muito rapidamente ao aplicar essa tática, considerando quanto mais longa ela é executada e quanto maior o público em que ela é atingida.

- **Forma de U**: esta abordagem atribui **40%** do crédito à *primeira pessoa* na porta, distribui **20%** do crédito entre *todos entre* e dá **40%** ao **último**. Este modelo será usado com mais frequência em situações em que você tem um **longo ciclo de conversão/vendas** contendo *vários pontos de contato* ao longo do caminho.  Nesse caso, seu objetivo é destacar principalmente as táticas de marketing do ***first*** e do ***last*** que contribuíram para a conversão do cliente.
- **J**-**Formatado** e **J Inverso**:
   - Pense em **Forma de U**, mas este modelo atribui crédito de **60%** à *última pessoa* que anda pela porta, **20%** à *primeira* e, em seguida, *divide* os **20%** restantes em *todas as outras pessoas* no meio.  **J invertido** faz exatamente o oposto.

     O objetivo aqui é colocar a maior parte de sua ênfase, seja no *início* ou no *fim* de sua campanha. No entanto, você ainda deseja atribuir uma certa quantidade de crédito ao item de contribuição na extremidade oposta, reconhecendo os &quot;carinhas&quot; ao longo do caminho.

- **Declínio de tempo**: agora, eu seria negligente se não compartilhasse este. Esse modelo tem literalmente uma meia-vida que decai exponencialmente - com o tempo!  Neste caso, o parâmetro *padrão* para a meia-vida deste modelo é **7 dias**.  Funciona da seguinte maneira: aplicar *peso* a cada **canal de marketing**, *com base no tempo* decorrido após o *ponto de contato inicial* e quando o cliente se converter.

  **Declínio de tempo** e **Modelos de atribuição em forma de U** normalmente são usados para medir campanhas de longo prazo, mas, como você pode ver, eles têm metas um pouco diferentes, com base em como eles *pesam* o valor do resultado.

- **Personalizado**: você escolhe quem vai receber crédito.  É a sua campanha!

Para obter informações adicionais sobre estes e outros modelos de atribuição, [clique aqui](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=pt-BR)

Para tornar isso ainda mais interessante, vamos falar sobre como retroceder o relógio!

## **Janelas de pesquisa**

Agora é hora de começar a levar sua mente ao próximo nível.  É aqui que literalmente adicionamos o elemento de viagem no tempo à nossa análise - e, novamente, estamos começando com as noções básicas.

***O Adobe*** define ❹ **janelas de retrospectiva** como &quot;o tempo que uma conversão deve retroceder para incluir pontos de contato. Os modelos de atribuição que dão mais crédito às primeiras interações veem diferenças maiores ao exibir diferentes janelas de retrospectiva.&quot;


Em outras palavras, as **janelas de retrospectiva** determinam o período durante o qual *conversões* são consideradas e fornecem *contexto* para a análise de atribuição. O ***Adobe Analytics*** oferece três tipos de **janelas de retrospectiva**:

- **Janela de retrospectiva de visita:** retroage ao início de uma ***visita*** quando ocorreu uma conversão, fornecendo insights sobre as interações imediatas que resultaram em conversões.

  Lembre-se de que esta é normalmente a **janela de retrospectiva** mais curta a ser usada.
- **Janela de retrospectiva do visitante:** verifica todas as ***visitas*** até o primeiro dia do mês dentro do **intervalo de datas** selecionado, oferecendo uma visão muito mais ampla das interações do cliente e ajudando a identificar padrões ao longo do tempo.
- **Janela de pesquisa personalizada:** Permite expandir a **janela de atribuição** além do **intervalo de datas** do relatório até um *máximo* de **90 dias**.  Ele fornece *flexibilidade* para capturar pontos de contato que ocorreram *fora* do **intervalo de datas** selecionado, garantindo uma análise abrangente.

Ao ajustar determinada **janela de lookback**, os analistas podem examinar o impacto de um ou mais pontos de contato em intervalos de tempo específicos e obter insights adicionais sobre como as diferentes durações afetam os resultados da atribuição.

## **Reunindo tudo**

Então, o que tudo isso significa para nós analistas?

O **painel de atribuição** e a **janela de retrospectiva** permitem que olhemos além dos dados comuns e de superfície e aprofundemos na jornada do cliente. Ao entender quais pontos de contato tiveram maior impacto em *conversões*, podemos tomar decisões informadas sobre nossas estratégias de marketing e alocar recursos de maneira mais eficaz.

Lembre-se, depois de selecionar seus **modelos de atribuição** e **janelas de retrospectiva**, você ainda poderá manipular seus dados filtrando-os com um ❺ **segmento,** ou qualquer outro componente desejado neste momento.  Além disso, depois que o painel for renderizado, você terá toda a funcionalidade de um Workspace tradicional à sua disposição.

## **Finalmente, colocando em prática**

Agora que você concluiu os conceitos, imagine que está executando uma campanha de marketing e tentando determinar qual canal é o *mais eficaz* para gerar conversões. Com a ajuda do **painel de atribuição**, você não apenas poderá ver o **último contato**, mas também o **primeiro contato**, **mesmo contato** e qualquer outro **modelo** escolhido para determinar quais **canais** são os *mais eficazes* na condução de suas *conversões*. Em seguida, essas informações podem ser usadas para *otimizar* suas campanhas e melhorar o desempenho geral simplesmente restaurando o relógio com a **janela de retrospectiva** de sua escolha!

Agora que você viu o que ele pode fazer, não se deixe enganar ou se intimidar pelas características aparentemente complexas do painel de atribuição.  **Enfrente isso**.  *Adote*.  **Entenda**.
MAS ACIMA DE TUDO - *Use-o em seu benefício.* O **painel de atribuição** e a **janela de retrospectiva** são as chaves para desbloquear uma compreensão mais profunda de seus clientes e suas jornadas com sua marca.

Agora, podemos viajar &quot;[de volta no tempo](https://youtu.be/gVryJmZNFdU)&quot; com confiança e usar o poder de nossa confiável máquina do tempo (também conhecida como ***Adobe Analytics***) para tomar decisões orientadas por dados.

## Autora

Este documento foi escrito por:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, gerente, Digital Analytics na Kroger Personal Finance

Especialista no Adobe Analytics
