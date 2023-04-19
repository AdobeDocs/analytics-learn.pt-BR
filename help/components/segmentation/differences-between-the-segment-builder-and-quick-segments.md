---
title: Diferenças entre o construtor de segmentos e os segmentos rápidos no Analysis Workspace
description: Os segmentos podem ser uma das ferramentas mais eficientes em seu kit de ferramentas de análise de dados. Conheça as diferenças entre usar o construtor de segmentos e os segmentos rápidos no Analysis Workspace para obter eficiência.
feature: Segmentation
role: User
level: Beginner
doc-type: article
kt: KT-13118
source-git-commit: 9484b2e981d78be59b6ea16eeae2cf6f212c81ab
workflow-type: tm+mt
source-wordcount: '1264'
ht-degree: 1%

---


# Diferenças entre o construtor de segmentos e os segmentos rápidos no Analysis Workspace

Os segmentos podem ser uma das ferramentas mais eficientes em seu kit de ferramentas de análise de dados. Conheça as diferenças entre usar o construtor de segmentos e os segmentos rápidos no Analysis Workspace para obter eficiência.

>[!TIP]
>
> Clique na imagem na parte inferior da página para baixar um lembrete útil sobre quando usar cada ferramenta no Analysis Workspace.

Os segmentos podem ser uma das ferramentas mais eficientes em seu kit de ferramentas de análise de dados. Quando você quiser ver grupos específicos de tráfego, seções do site ou jornadas do cliente, usar segmentos pode ser uma ótima maneira de concentrar sua análise em um subconjunto específico de tráfego do site. Vindo de um ambiente de varejo, alguns dos segmentos mais úteis que fiz são para diferentes tipos de grupos de clientes, por exemplo clientes novos vs. existentes, clientes conectados a uma conta vs. convidados e assim por diante. Mas você também pode criá-los para diferentes seções do site, clientes que executam ações específicas ou qualquer outra coisa que você possa imaginar!

**Há duas maneiras principais de criar segmentos:**

* Uso do construtor de segmentos no menu Componentes
* Uso dos segmentos rápidos na parte superior de um painel

Se você criar seu segmento usando o construtor de segmentos, poderá salvá-lo para reutilização em outros projetos. Essa é uma ótima maneira de se concentrar em grupos específicos de clientes, por exemplo, pessoas que visitam determinadas seções do site e fazem uma compra. Por outro lado, se você estiver fazendo uma análise exploratória e quiser testar diferentes configurações de segmento, o construtor de segmento rápido pode ser uma ótima ajuda. Vejamos alguns dos principais benefícios de cada método.

## Segmentos rápidos

Na parte superior de cada painel, você pode clicar no ícone de segmento rápido (um funil com o símbolo +) para abrir o construtor. Isso permitirá criar um segmento em qualquer nível (ocorrência, visita ou visitante) com até três condições. Semelhante ao construtor de segmento principal, isso fornece uma indicação no lado direito que observa se o segmento está retornando dados e a % da população de tráfego geral incluída no segmento, embora seja uma versão mais simplificada do que a exibição de volume de segmento completo exibida no construtor de segmentos. Ao adicionar mais de uma condição, você pode usar os operadores &#39;and&#39; e &#39;or&#39;. Infelizmente, não há a opção &quot;then&quot; para segmentos rápidos, portanto, se você precisar de segmentos sequenciais, será necessário usar o construtor de segmentos completo. Também há um limite de um contêiner em um segmento rápido. Como ele deve ser usado para segmentos básicos que podem ser criados e editados rapidamente. Depois que um segmento rápido é aplicado a um painel ou salvo, ele não pode mais ser editado no painel.

Ao fazer uma análise exploratória e testar diferentes tipos de segmentos para ver como diferentes grupos de clientes reagem ou o desempenho de diferentes categorias - o uso de segmentos rápidos é muito mais rápido do que o uso do construtor de segmentos. Além disso, esses segmentos só estão disponíveis no projeto em que foram criados. Dessa forma, se não fornecer os resultados desejados, não será necessário se preocupar em excluir o segmento salvo da lista principal. Se, depois de testar os segmentos, você perceber que isso será útil em outros projetos, sempre poderá clicar no botão &quot;abrir construtor&quot; para abrir o segmento no construtor de segmentos completo para salvá-lo como um segmento regular. No entanto, depois de fazer isso, não será mais possível editá-lo no construtor de segmentos rápidos.

![Segmento rápido](assets/quick-segement.png)

## Construtor de segmentos

O construtor de segmentos pode ser acessado clicando no símbolo + acima da lista de segmentos no menu dos componentes à esquerda ou clicando na lista suspensa de componentes e selecionando &quot;Criar segmento..&quot; Ao contrário dos segmentos rápidos, isso tem todas as opções disponíveis. Para adicionar várias condições, é possível criar segmentos sequenciais usando o operador &quot;then&quot;. Segmentos sequenciais também permitem usar o &quot;grupo lógico&quot; como seu nível (em vez de ocorrência, visita ou visitante). O construtor de segmentos também permitirá adicionar uma descrição aos segmentos, que pode adicionar contexto sobre quem criou o segmento ou que tipo de dados ele foi criado para filtrar, ou até mesmo simplesmente adicionar &quot;tags&quot; ao segmento para fins organizacionais, os quais não são possíveis no construtor de segmentos rápidos.

O uso do construtor de segmentos é essencial quando o segmento terá mais de três condições, se precisar usar contêineres ou desejar segmentos sequenciais. O construtor de segmento completo tem muito mais opções para criar segmentos mais complexos, o que pode ajudar você a detalhar diferentes tipos de clientes, categorias, jornadas do cliente e assim por diante. Depois que esses segmentos são criados e salvos, eles são adicionados à lista principal de segmentos, o que significa que podem ser marcados, aprovados, compartilhados, usados em vários relatórios e publicados no Experience Cloud. A publicação no Experience Cloud permite utilizar o segmento em outros produtos do Adobe, como no Adobe Target para personalização do direcionamento. Os segmentos criados no construtor de segmentos não podem ser editados no painel de segmentos rápidos, é necessário abrir o construtor de segmentos para fazer qualquer alteração neles. Felizmente, a visualização à direita fornece uma análise mais detalhada do tráfego que o segmento traria nos últimos 90 dias, o que significa que é mais fácil ter certeza de que o segmento está trazendo o que você deseja antes de salvar.

![Construtor de segmentos](assets/segment-builder-quick.png)

## Casos de uso

Em diferentes setores, seus usos para a criação de segmentos personalizados podem ser diferentes. Trabalhando para a divisão de comércio eletrônico de um grande varejista, geralmente realizamos análises exploratórias para determinar quais caminhos os clientes estão tomando para comprar. Quando vemos picos ou quedas em ações como adicionar produtos ao carrinho ou fazer pedidos, é aqui que o uso dos segmentos rápidos pode ser útil. Durante uma análise, posso criar rapidamente um segmento para um tipo específico de cliente ou para uma ação/link específico em que ele clica. Ao não precisar abrir o construtor de segmentos e salvar cada segmento, eu posso adicionar as condições rapidamente e removê-las o mais rápido possível. Isso economiza muito tempo ao tentar explicar por que vemos uma mudança em nosso site.

Como alternativa, há vezes que o construtor de segmentos foi o meu passo a passo. Nem todos os clientes são iguais e, frequentemente, queremos ver tipos específicos de clientes identificados por ações ou caminhos que tomam. Ao usar o construtor de segmentos, podemos adicionar várias condições para identificar os diferentes tipos de clientes e salvar os segmentos para que eles possam ser compartilhados e usados por vários analistas. É importante que esses tipos de segmentos sejam consistentes em todos os relatórios, de modo que criar um que todos possam usar é melhor do que cada pessoa que cria sua própria versão, pois os resultados podem ser diferentes.

Em geral, os segmentos rápidos e o construtor de segmentos são ferramentas excelentes para usar em sua análise. Cada um tem seus propósitos, benefícios e desvantagens. Verifique nossas dicas e fichas de truques para download, disponíveis para uso, abaixo, para obter um guia de referência rápido.

## Autora

Este documento foi escrito por:

![Mandy George](assets/mandy-george.jpg)

**Mandy George**, Analista digital III na Best Buy Canada

Especialista em Adobe Analytics

## Baixar

[![Download de segmentos rápidos](assets/quick-segments-download-small.jpg)](assets/Adobe_Analytics_Segments_Vs_Segment_Builder_Reference_Guide.pdf)
