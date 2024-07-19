---
title: Utilização de análises de coorte para entender o comportamento do cliente
description: Para melhorar a experiência e a receita do cliente, as empresas devem entender o comportamento do cliente. A análise de coorte pode ajudar a compreender o engajamento e a retenção, resultando em ações como a melhoria da criação de contas e a criação de campanhas para meses de alto volume.
feature: Cohort Analysis
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13213
thumbnail: KT-13213.jpeg
exl-id: 23dd43c5-47e4-46c7-88ee-66c7f62ca9cf
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1146'
ht-degree: 13%

---

# Utilização de análises de coorte para entender o comportamento do cliente

Para melhorar a experiência e a receita do cliente, as empresas devem entender o comportamento do cliente. A análise de coorte pode ajudar a compreender o engajamento e a retenção, resultando em ações como a melhoria da criação de contas e a criação de campanhas para meses de alto volume.

A análise do desempenho digital é fundamental para entender como os clientes interagem com uma empresa e quais ações podem ser tomadas para melhorar sua experiência. Nesta publicação do blog, exploraremos como usar a análise de coorte para entender melhor o comportamento do cliente.

## Parte 1: Comparação de desempenho digital entre visitas de primeira e de retorno

### Configuração do preparo

Um cliente pretende entender o desempenho digital nos últimos dois anos e está considerando desenvolver um programa de fidelidade para impulsionar o desempenho digital. Para começar, podemos observar a combinação atual de sites entre usuários novos e repetidos para entender como os dois grupos de visitantes se comportam hoje.

Desempenho digital atual

1. Em 2022, 62 % dos pedidos foram provenientes de visitas iniciais, em comparação com 38 % dos pedidos provenientes de visitas de regresso (sujeitos a cookies, vários dispositivos).
1. A conversão de visitas de primeira vez é feita em uma taxa ligeiramente maior do que as visitas de retorno para ambos, 11,6% vs. 11,4%.
1. Em comparação com 2021, as taxas de conversão diminuíram em ambos os segmentos.

![Tabela de visitas](assets/cohort1.png)

## Parte 2: Análise de coorte — Visitas, arranjos comestíveis, produção global

Para entender a aderência do canal Digital e a oportunidade de direcionar compradores recorrentes, a próxima pergunta a ser respondida é: Qual é o volume de visitantes que retornam ao site todos os meses em 2022?

### Introdução à análise de coorte

A análise de coorte é uma ferramenta útil para entender como as coortes interagem com uma marca ao longo do tempo. Para começar, determinamos quais perguntas responder:

1. Em um determinado ano, qual é o período médio de retenção por mês?
1. Qual volume de visitantes do site retorna todos os meses em um determinado ano?
1. Qual é o impacto dos logons na retenção?
1. Existem produtos específicos que geraram maior retenção?

Como configurar a Tabela de coorte

1. Definir intervalo de datas de janeiro a dezembro de 2022
1. **Critérios de inclusão:** Visitas
1. **Critérios de retorno:** visitas
1. **Granularidade:** Mês
1. **Configurações:** Cálculo contínuo
\*\*Permite calcular a retenção com base na coluna anterior, não na coluna incluída. Portanto, isso significa que um usuário é incluído em cada um dos meses\*\*
1. **Segmentos:** você pode selecionar segmentos específicos para aprofundar esta análise
   1. Páginas de destino específicas
   1. Tipo de dispositivo
   1. Canais de marketing
   1. Etc.

### Interpretação dos resultados

**Em 2022:**

1) Os meses com as taxas de retenção mais altas +1 mês incluem janeiro, abril e novembro
1) Os meses com mais volume incluem fevereiro e maio
1) Há ~1.000 visitantes que retornam ao site todos os meses

![tabela de retenção 2022](assets/cohort2.png)

**Em 2021:**

1) Os meses com as taxas de retenção mais altas +1 mês incluem abril, janeiro e março
1) Os meses com mais volume incluem fevereiro e maio

![Tabela de retenção de 2021](assets/cohort3.png)

**Itens de ação:**

Crie um segmento com base nos ~1.000 visitantes e saiba mais sobre eles:

- Onde eles estão localizados?
- Quais produtos eles compram ao longo do ano?
- De que lojas elas estão comprando?

Os principais meses destacam a oportunidade de direcionar a retenção com base no volume:

- Existem táticas específicas que podem gerar aderência adicional durante fevereiro e maio para aproveitar o volume?

Repetir análise para pedidos para compreender compradores repetidos

- As taxas de retenção de mais de um mês são as mais altas para os mesmos meses?
- Os meses mais altos de visitas são os mesmos para pedidos?

## Parte 3: Adicionar duas métricas aos critérios de inclusão

### Noções básicas sobre o impacto do logon

Como esse cliente deseja entender o valor de um programa de fidelidade, a próxima etapa da análise incluiu a adição do evento de sucesso de Logon como uma métrica de Inclusão ao Coorte.

Advertência: a análise de coorte não pode ser usada para métricas calculadas (como Taxa de conversão) ou métricas não inteiras (como Receita). Somente as métricas que podem ser usadas em segmentos podem ser usadas em Análises de coorte, e só podem ser aumentadas >1 por vez.

O site tem mais probabilidade de reter usuários que estão fazendo logon?

Qual seria o impacto se pudéssemos fazer com que mais usuários fizessem logon? É uma experiência mais grudenta?

### Configuração da tabela de coorte

1. **Definir intervalo de datas:** de janeiro a dezembro de 2022
1. **Critérios de inclusão:** Visitas + evento de sucesso de logon
1. **Critérios de retorno:** visitas
1. **Granularidade:** Mês
1. **Configurações:** Cálculo contínuo
\*\*Permite calcular a retenção com base na coluna anterior, não na coluna incluída. Portanto, isso significa que um usuário é incluído em cada um dos meses\*\*

### Interpretação dos resultados

**Em 2022:**

1) Os meses com as taxas de retenção mais altas +1 mês incluem janeiro, abril e novembro (mesmos meses que a primeira tabela de coorte)
1) Os meses com mais volume incluem fevereiro, maio e dezembro
1) Há aproximadamente 2500 visitantes que retornam a cada mês \*\*mais do que duplo\*\*

**Itens de ação:**

Investigar a experiência do usuário do site para fazer com que os usuários criem uma conta durante o Check-out

![Tabela de coorte 4](assets/cohort4.png)

## Parte 4: Coorte de Dimension personalizado

Coorte de Dimension personalizada: crie coortes com base na dimensão selecionada, em vez de coortes com base no tempo (padrão). Muitos usuários desejam analisar suas coortes segundo critérios que não sejam o tempo, por isso o novo recurso de Coorte de dimensão personalizada permite ter flexibilidade para criar coortes com base nas dimensões desejadas. Use dimensões como canal de marketing, campanha, produto, página, região ou qualquer outra dimensão no Adobe Analytics para mostrar como a retenção é alterada com base nos diferentes valores dessas dimensões. O

A definição de segmento de coorte de Dimension personalizada aplica o item de dimensão somente como parte do período de inclusão, não como parte da definição de retorno.

Depois de escolher a opção Coorte de Dimension personalizado, você pode arrastar e soltar qualquer dimensão que desejar na área designada. Isso permite comparar itens de dimensão similares entre o mesmo período de tempo. Por exemplo, você pode comparar o desempenho de cidades lado a lado

lado, produtos, campanhas etc. Ele retornará seus 14 principais itens de dimensão. Entretanto, você pode usar um filtro (acesse-o passando o mouse sobre o lado direito da dimensão que foi arrastada) para exibir somente os itens de dimensão desejados. Um Coorte de dimensão personalizado não pode ser usado com o recurso de Tabela de latência.

### Quais produtos estão causando aderência no site?

A tabela de coorte de Dimension personalizada destaca os produtos que estão impulsionando taxas de retenção mais altas do que a média.  Esta tabela ajuda a identificar os principais produtos para impulsionar campanhas de marketing internas e externas com os principais produtos dignos de atenção.

**Em fevereiro:** 3 produtos se destacam com taxas de retenção mais altas

1) Product 1
1) Product 2
1) Product 3

**Em março:**

1) Product 1
1) Product 2
1) Produto 3 — frequentemente supera o desempenho com uma taxa de retenção mais alta em comparação à retenção média.

![Tabela de coorte 5](assets/cohort5.png)

## Conclusão

A análise de coorte e o Coorte de Dimension personalizado são ferramentas eficientes para entender o comportamento do cliente e melhorar o desempenho digital. Analisando taxas de retenção, taxas de logon e o impacto de produtos específicos, as empresas podem tomar decisões orientadas por dados para melhorar a experiência do cliente e impulsionar o crescimento.

## Autora

Este documento foi escrito por:

![Jennifer Yacenda](assets/jennifer-yacenda.png)

**Jennifer Yacenda**, Director sênior da Marriott

Especialista no Adobe Analytics
