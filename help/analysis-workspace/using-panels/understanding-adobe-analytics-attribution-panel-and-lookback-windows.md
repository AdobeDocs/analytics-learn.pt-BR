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
source-wordcount: '1664'
ht-degree: 1%

---

# Como entender o painel de atribuição do Adobe Analytics e as janelas de pesquisa

Quando eu pensei pela primeira vez sobre o [painel de atribuição](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/panels/attribution.html?lang=en) e **janela de retrospectiva**, eu fui imediatamente lembrado do conceito de &quot;*viagem no tempo&#39;*; então, é claro, também me lembraram que nossa resposta típica a muitas novas ferramentas como essas é simplesmente parar de tentar usá-las, porque elas parecem tão complicadas.

Quero dizer, honestamente, basta olhar para todas essas opções, interruptores, painéis, leituras, e botões.  E sério, vamos falar sobre essas complicadas luzes piscando, mangueiras, medidores... ESPERE!  Não é hora de distrair falando de máquinas do tempo, só não temos tempo... ou temos?

Eu vou admitir o **painel de atribuição** é uma ferramenta bastante complexa; no entanto, nosso trabalho típico como analistas, dia após dia, é usar outra de nossas ferramentas favoritas e altamente complexas para também dar uma olhada no que aconteceu no passado. Essa ferramenta é chamada de ***Adobe Analytics***!  Então sim, para responder a nossa pergunta muito relevante, eu acredito que estas duas coisas dizem que temos muito tempo.

Portanto, por que devemos permitir que algo como um pouco de medo interfira com ferramentas tão surpreendentes, sofisticadas e poderosas como essas que literalmente nos permitem olhar *voltar* a tempo, todos os dias?

Afinal - esta é a VIAGEM NO TEMPO, pessoal!!  Somos todos sobre esse tipo de coisa.  Certo???!!

Então, o que estamos esperando - um carro de metal brilhante, uma caixa de polícia, ou uma cabine telefônica vintage usando a fiação de um guarda-chuva velho como sua antena para aparecer em nossa porta?

Não!  Temos algo ainda melhor, então vamos nos amarrar e esperar!

Bem... você entendeu a ideia.


Agora que estamos todos entusiasmados com a viagem no tempo, vamos respirar fundo, dar um passo para trás, estabelecer o que **painel de atribuição** *realmente* é e detalhar um pouco:

![Atribuição](assets/attribution.png)

*Figura 1: Os números exibidos estão alinhados com o texto mais abaixo*

Entrada **atribuição**, basta considerar como os eventos/ações podem ser causados por um indivíduo, por vários indivíduos ou por um dentre vários eventos diferentes ao longo do tempo.

De acordo [Adobe](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/overview.html?lang=en), *atribuição* oferece aos analistas a capacidade de personalizar como *Dimension* os itens recebem crédito por *eventos de sucesso*.


>[!WARNING]
>
>**Modelos de atribuição** são frequentemente associados a **canais de marketing** que eu propositalmente *riscado* ❷ CANAL na imagem acima para ilustrar que é possível executar **atribuição** análise em relação à maioria das outras ***dimension***.


Na verdade, raramente uma determinada jornada de cliente é realmente linear e menos previsível.  Além disso, cada cliente continuará em seu próprio ritmo; com frequência, ele pode voltar, parar, sair ou adotar outros comportamentos não lineares. Essas ações orgânicas dificultam ou são praticamente impossíveis de saber o impacto dos esforços de marketing na jornada do cliente. Também dificultam os esforços para unir vários canais de dados.

Isso mesmo.  Deixe suas analogias &quot;dominó&quot; na porta e abra suas mentes para conceitos mais nos moldes do efeito borboleta e da teoria das cordas - mas como tudo o mais, precisamos começar com alguns dos fundamentos.

## **Modelos de atribuição**

Quando usamos o **painel de atribuição** No entanto, podemos começar a observar várias coisas diferentes.  Por exemplo, a variável **modelos de atribuição** demonstrar para nós como nossas *conversões* (ou seja, ❶ **métricas de sucesso**) podem ser distribuídos entre *ocorrências* em qualquer grupo específico.

Simplificando, se **10 pessoas** pressione a **BOTÃO VERMELHO GRANDE** para entrar por uma porta, nosso **modelos de atribuição** vão nos dizer qual dessas **10 pessoas** queremos atribuir &quot;crédito&quot; - ou melhor ainda, como *muito* &quot;crédito&quot; queremos atribuí-los - por pressionar o botão dito.

![Botão](assets/button.png)

Tendo isso em mente, aqui estão alguns exemplos de como as ❸ **modelos de atribuição** podem afetar esses **10 pessoas**:

- **Primeiro contato**: esse modelo funciona exatamente como parece dando **100% de crédito** para o *primeiro* pessoa que entrou pela porta.  Os profissionais de marketing têm mais probabilidade de usar essa abordagem para táticas como ***redes sociais*** ou ***exibição***; no entanto, também é uma ótima tática para usar com frequência na eficácia das recomendações de produtos no local.
- **Último contato**: Essa tática também funciona exatamente como parece, mas em vez disso oferece **100% de crédito** à ÚLTIMA pessoa que atravessou a porta.  Normalmente, esse modelo é usado para analisar coisas como ***pesquisa natural (orgânica)*** e outros *curto prazo* campanhas do ciclo de marketing.
- **Linear**: Esse modelo distribui crédito igual para TODAS AS PESSOAS que passaram pela porta.

  >[!CAUTION]
  >
  >No entanto, recomenda-se cautela aqui, porque você tem o potencial de espalhar seus resultados muito rapidamente ao aplicar essa tática, considerando quanto mais longa ela é executada e quanto maior o público em que ela é atingida.

- **Forma de U**: essa abordagem atribui **40%** do crédito para o *primeira pessoa* na porta, espalha **20%** do crédito em *todos entre eles* e então dá **40%** para o **último** até. Esse modelo será usado com mais frequência em situações em que você tem uma **ciclo longo de conversão/vendas** contendo *vários pontos de contato* pelo caminho.  Nesse caso, seu objetivo é destacar principalmente o ***primeiro*** e ***último*** táticas de marketing que contribuíram para a conversão do cliente.
- **J**-**Em forma** e **J invertido**:
   - Pense em **Forma de U**, mas em vez disso esse modelo atribui **60%** crédito para o *última pessoa* andando pela porta, **20%** para o *primeiro* e depois *divide* o restante **20%** em *todos os outros* no meio.  **J invertido** faz exatamente o oposto.

     O objetivo aqui é colocar a maior parte de sua ênfase, seja no *início* ou o *fim* da sua campanha; no entanto, você ainda deseja atribuir uma certa quantidade de crédito ao item de contribuição na extremidade oposta, reconhecendo os &quot;carinhas&quot; ao longo do caminho.

- **Decaimento de tempo**: Agora, eu seria negligente se não compartilhasse desse. Esse modelo tem literalmente uma meia-vida que decai exponencialmente - com o tempo!  Neste caso, o *padrão* O parâmetro para a meia-vida deste modelo é **7 dias**.  A maneira como funciona é aplicar *peso* para cada **canal de marketing**, *com base na quantidade de tempo* que passa após o *ponto de contato inicial* e quando o cliente converte.

  **Decaimento de tempo** e **Modelos de atribuição em forma de U** são normalmente usados para medir campanhas de longo prazo, mas, como você pode ver, eles têm metas um pouco diferentes, com base em como elas são *peso* o valor do resultado.

- **Personalizado**: Você escolhe quem vai receber crédito.  É a sua campanha!

Para obter informações adicionais sobre esses e outros modelos de atribuição, [clique aqui](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/models.html?lang=en)

Para tornar isso ainda mais interessante, vamos falar sobre como retroceder o relógio!

## **Janelas de pesquisa**

Agora é hora de começar a levar sua mente ao próximo nível.  É aqui que literalmente adicionamos o elemento de viagem no tempo à nossa análise - e, novamente, estamos começando com as noções básicas.

***Adobe*** define ❹ **janelas de retrospectiva** como &quot;o tempo que uma conversão deve retroceder para incluir pontos de contato. Os modelos de atribuição que dão mais crédito às primeiras interações veem diferenças maiores ao exibir diferentes janelas de retrospectiva.&quot;


Em outras palavras, **janelas de retrospectiva** determinar o período durante o qual *conversões* são considerados e fornecem *contexto* à análise de atribuição. ***Adobe Analytics*** O oferece três tipos de **janelas de retrospectiva**:

- **Janela de retrospectiva de visita:** Retroage para o início de um ***visita*** quando uma conversão ocorria, fornecia insights sobre as interações imediatas que resultavam em conversões.

  Lembre-se de que normalmente é o menor **janela de retrospectiva** para usar.
- **Janela de pesquisa do visitante:** Examina tudo ***visitas*** fazer backup até o primeiro dia do mês na pasta selecionada **intervalo de datas**, oferecendo uma visão mais ampla das interações do cliente e ajudando a identificar padrões ao longo do tempo.
- **Janela de pesquisa personalizada:** Permite expandir a variável **janela de atribuição** além do relatório **intervalo de datas** até um *máximo* de **90 dias**.  Ele fornece *flexibilidade* na captura de pontos de contato que ocorreram *fora* o selecionado **intervalo de datas**, garantindo uma análise abrangente.

Ao ajustar um determinado **janela de retrospectiva** Além disso, os analistas podem examinar o impacto de um ou mais pontos de contato em intervalos de tempo específicos e obter insights maiores sobre como as diferentes durações afetam os resultados da atribuição.

## **Reunindo tudo**

Então, o que tudo isso significa para nós analistas?

A variável **painel de atribuição** e **janela de retrospectiva** dê-nos o poder de olhar além do mundano, dos dados de nível de superfície e mergulhar mais fundo na jornada do cliente. Ao compreender quais pontos de contato tiveram maior impacto no *conversões* Além disso, podemos tomar decisões conscientes sobre nossas estratégias de marketing e alocar recursos de maneira mais eficaz.

Lembre-se, depois de ter seu **modelos de atribuição** e **janelas de retrospectiva** selecionada, você ainda poderá manipular seus dados filtrando-os com um ❺ **segmento,** ou qualquer outro componente que desejar neste momento.  Além disso, após a renderização do painel, você terá toda a funcionalidade de um espaço de trabalho tradicional à sua disposição.

## **Finalmente, colocando em prática**

Agora que você concluiu os conceitos, imagine que está executando uma campanha de marketing e tentando determinar qual canal é o *mais eficaz* para gerar conversões. Com a ajuda da **painel de atribuição**, você não só pode ver a **último contato**, mas também a **primeiro contato**, **mesmo toque** e qualquer outro **modelo** você escolhe determinar qual **canais** são as *mais eficaz* na condução do seu *conversões*. Em seguida, essas informações podem ser usadas para *otimizar* suas campanhas e melhorar o desempenho geral simplesmente restaurando o relógio com o **janela de retrospectiva** de sua escolha!

Agora que você viu o que ele pode fazer, não se deixe enganar ou se intimidar pelas características aparentemente complexas do painel de atribuição.  **Encarar**.  *Adotar* o mesmo.  **Compreender** o mesmo.
MAS ACIMA DE TUDO - *Use-o em sua vantagem.* A variável **painel de atribuição** e **janela de retrospectiva** são a chave para obter uma compreensão mais profunda dos clientes e de suas jornadas com a sua marca.

Agora, podemos viajar &quot;[voltar no tempo](https://youtu.be/gVryJmZNFdU)&quot; com confiança e usar o poder de nossa confiável máquina do tempo (também conhecida como ***Adobe Analytics***) para tomar decisões orientadas por dados.

## Autora

Este documento foi escrito por:

![Jeff Bloomer](assets/jeff-headshot.png)

**Jeff Bloomer**, gerente, Digital Analytics na Kroger Personal Finance

Especialista no Adobe Analytics
