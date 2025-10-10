---
title: Diferenças entre o construtor de segmentos e os segmentos rápidos do Analysis Workspace
description: Os segmentos podem ser uma das ferramentas mais eficientes do seu kit de ferramentas de análise de dados. Conheça as diferenças entre o uso do construtor de segmentos e dos segmentos rápidos do Analysis Workspace para obter eficiência.
feature: Segmentation
role: User
level: Beginner
doc-type: article
kt: KT-13118
exl-id: 144e71fd-8d42-4d20-b55e-3d81ad992a79
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1266'
ht-degree: 100%

---

# Diferenças entre o construtor de segmentos e os segmentos rápidos do Analysis Workspace

Os segmentos podem ser uma das ferramentas mais eficientes do seu kit de ferramentas de análise de dados. Conheça as diferenças entre o uso do construtor de segmentos e dos segmentos rápidos do Analysis Workspace para obter eficiência.

>[!TIP]
>
> Clique na imagem na parte inferior da página para baixar um lembrete útil sobre quando usar cada ferramenta no Analysis Workspace.

Os segmentos podem ser uma das ferramentas mais eficientes do seu kit de ferramentas de análise de dados. Caso deseje ver grupos específicos de tráfego, seções do site ou jornadas do cliente, o uso de segmentos pode ser uma ótima maneira de concentrar sua análise em um subconjunto específico de tráfego do site. Vindo de um ambiente de varejo, alguns dos segmentos mais úteis que criei são para diferentes grupos de clientes, por exemplo, clientes novos vs. existentes, clientes conectados a uma conta vs. convidados e assim por diante. Mas você também pode criá-los para diferentes seções do site, clientes que executam ações específicas ou qualquer outra coisa que possa imaginar.

**Há duas maneiras principais de criar segmentos:**

* Usar o construtor de segmentos do menu de componentes
* Usar os segmentos rápidos na parte superior de um painel

Se você criar seu segmento usando o construtor de segmentos, poderá salvá-lo para reutilização em outros projetos. Essa é uma ótima maneira de se concentrar em grupos específicos de clientes, por exemplo, pessoas que visitam determinadas seções do site e fazem uma compra. Por outro lado, se estiver fazendo uma análise exploratória e quiser testar diferentes configurações de segmento, o construtor de segmentos rápidos pode ser uma ótima ajuda. Vejamos alguns dos principais benefícios de cada método.

## Segmentos rápidos

Na parte superior de cada painel, você pode clicar no ícone de segmento rápido (um funil com o símbolo +) para abrir o construtor. Isso permitirá criar um segmento em qualquer nível (ocorrência, visita ou visitante) com até três condições. Semelhante ao construtor de segmento principal, esse fornece uma indicação no lado direito que informa se o segmento está retornando dados e a porcentagem da população de tráfego geral incluída no segmento, embora seja uma versão mais simplificada do que a visualização completa do volume do segmento que é exibida no construtor de segmentos. Ao adicionar mais de uma condição, você pode usar os operadores “and” e “or”. Infelizmente, a opção “then” não está disponível para segmentos rápidos, portanto, se você precisar de segmentos sequenciais, será necessário usar o construtor de segmentos completo. Os segmentos rápidos também são limitados ao uso de um único container. Isso se deve ao fato de que eles são usados para segmentos básicos que podem ser criados e editados rapidamente. Depois que um segmento rápido é aplicado a um painel ou salvo, ele não pode mais ser editado no painel.

Em uma análise exploratória, quando você deseja testar diferentes tipos de segmentos para ver como diferentes grupos de clientes reagem ou como se dá o desempenho de diferentes categorias, usar segmentos rápidos é bem mais prático do que usar o construtor de segmentos. Além disso, esses segmentos só estão disponíveis no projeto em que foram criados. Sendo assim, se os resultados desejados não forem fornecidos, não será necessário se preocupar em excluir o segmento salvo da lista principal. Se depois de testar os segmentos, você perceber que serão úteis em outros projetos, poderá clicar no botão “Abrir construtor” para abrir o segmento no construtor de segmentos completo e salvá-lo como um segmento regular. No entanto, depois de fazer isso, não será mais possível editá-lo no construtor de segmentos rápidos.

![Segmento rápido](assets/quick-segement.png)

## Construtor de segmentos

O construtor de segmentos pode ser acessado clicando no símbolo + acima da lista de segmentos no menu de componentes à esquerda ou clicando na lista suspensa de componentes e selecionando “Criar segmento”. Ao contrário dos segmentos rápidos, esse recurso inclui todas as opções disponíveis. Para adicionar várias condições, é possível criar segmentos sequenciais usando o operador “then”. Segmentos sequenciais também permitem o uso de um “grupo lógico” como seu nível (em vez da ocorrência, visita ou visitante). O construtor de segmentos também permite adicionar uma descrição aos segmentos, a qual pode fornecer contexto sobre quem criou o segmento ou que tipo de dados ele foi criado para filtrar. Além disso, é possível adicionar “tags” ao segmento para organizá-lo. Essas opções não estão disponíveis no construtor de segmentos rápidos.

O uso do construtor de segmentos é essencial quando o segmento terá mais de três condições, precisará do uso de containers ou se você deseja segmentos sequenciais. O construtor de segmentos completo tem diversas opções para criar segmentos mais complexos, o que pode ajudar você a detalhar diferentes tipos de clientes, categorias, jornadas do cliente e assim por diante. Depois que esses segmentos são criados e salvos, eles são adicionados à lista principal de segmentos, o que significa que podem ser marcados, aprovados, compartilhados, usados em vários relatórios e publicados na Experience Cloud. A publicação na Experience Cloud permite utilizar o segmento em outros produtos da Adobe, como no Adobe Target para personalização e direcionamento. Os segmentos criados no construtor de segmentos não podem ser editados no painel de segmentos rápidos; é necessário abrir o construtor de segmentos para realizar qualquer alteração. Felizmente, a visualização à direita fornece uma análise mais detalhada do tráfego que o segmento traria nos últimos 90 dias, o que significa que é mais fácil garantir se o segmento está trazendo o que você deseja antes de salvá-lo.

![Construtor de segmentos](assets/segment-builder-quick.png)

## Casos de uso

Em diferentes setores, o uso desse recurso para a criação de segmentos personalizados pode variar. Trabalhando para a divisão de comércio eletrônico de um grande varejista, geralmente realizamos análises exploratórias para determinar quais caminhos os clientes estão tomando até o momento da compra. Quando vemos picos ou quedas em ações como adicionar produtos ao carrinho ou fazer pedidos, é aqui que o uso dos segmentos rápidos se torna útil. Durante uma análise, posso criar rapidamente um segmento para um tipo específico de cliente ou para uma ação/link específico em que ele clica. Eliminando a necessidade de abrir o construtor de segmentos e salvar cada segmento, posso adicionar as condições rapidamente e removê-las o mais rápido possível. Isso economiza muito tempo ao tentar explicar uma mudança em nosso site.

Da mesma forma, há momentos em que o construtor de segmentos se torna mais útil. Nem todos os clientes são iguais e, frequentemente, queremos observar tipos específicos de clientes que são identificados pelas ações ou caminhos que tomam. Ao usar o construtor de segmentos, podemos adicionar várias condições para identificar os diferentes tipos de clientes e salvar os segmentos para que eles possam ser compartilhados e usados por vários analistas. É importante que esses tipos de segmentos sejam consistentes em todos os relatórios, portanto, criar um segmento que todos possam usar é melhor do que cada pessoa criar sua própria versão, pois os resultados podem ser diferentes.

Em geral, tanto os segmentos rápidos quanto o construtor de segmentos são ferramentas excelentes para se usar em sua análise. Cada um tem seus propósitos, benefícios e desvantagens. Certifique-se de consultar nossa folha de dicas e truques úteis disponível para download abaixo, para obter um guia de referência rápido.

## Autora

Este documento foi escrito por:

![Mandy George](assets/mandy-george.jpg)

**Mandy George**, analista digital III na Best Buy Canada

Especialista em Adobe Analytics

## Baixar

[![Baixar segmentos rápidos](assets/quick-segments-download-small.jpg)](assets/Adobe_Analytics_Segments_Vs_Segment_Builder_Reference_Guide.pdf)
