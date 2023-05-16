---
title: Leve a análise de dados ao próximo nível com as Métricas calculadas
description: Saiba como um especialista em peer usa as Métricas calculadas para criar novas métricas sem alterar a implementação e usar os dados já coletados para ajudar a responder perguntas comerciais complexas.
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
source-git-commit: c64f2fde1b91edd9f3d6c0f87aa889ed2c613d9b
workflow-type: tm+mt
source-wordcount: '1566'
ht-degree: 1%

---


# Leve a análise de dados ao próximo nível com as Métricas calculadas

A maioria dos novos usuários do Adobe Analytics está familiarizada com Segmentos como uma maneira de destrinchar e analisar seus dados. Hoje, quero apresentar a você métricas calculadas, a melhor ferramenta a seguir na sua caixa de ferramentas de analistas.

Como um recurso avançado do Adobe Analytics, as métricas calculadas permitem criar novas métricas sem alterar a implementação usando os dados que você já coletou. O Criador de métricas calculadas pode usar diversas funções matemáticas e estatísticas, para que você possa criar métricas que respondam até mesmo às perguntas comerciais mais complexas.

## Introdução às métricas calculadas

Para começar a usar métricas calculadas, vamos ver um exemplo simples. Imagine que você queira entender se os usuários de autoatendimento online têm um valor médio de pedido (AOV) mais alto do que os usuários assistidos por chamadas. Para criar uma métrica calculada para responder a essa pergunta, faça o seguinte:

Para abrir o Criador de métricas calculadas, use a navegação superior para clicar em → **Componentes** → **Métricas calculadas** → **+ Adicionar.** Ou você pode clicar no botão **sinal +** above **Métricas** no painel Componentes.


![Calc 01](assets/calc01.png) ![Calc 02](assets/calc03.png) ![Calc 03](assets/calc02.png)

![Calc 04](assets/calc04.png)

*Descrições abaixo para itens da interface do usuário*

Quando o Criador de métricas calculadas for aberto, adicione e/ou faça o seguinte:

**A.** Um nome para a métrica calculada. Esse nome é exibido na lista de componentes da métrica, portanto, torne algo claro para você e para outros, como *Call Center AOV*.

**B.** Uma descrição da métrica calculada. Esta descrição é exibida quando os usuários clicam no botão **i** Ao lado da métrica na lista de componentes, verifique se ela é informativa. Por exemplo, para o Call Center AOV, podemos adicionar *Calcula AOV para pedidos assistidos do Call Center*.

**C.** O formato da métrica: Escolha decimal, hora, porcentagem ou moeda e adicione casas decimais e polaridade. Aqui, vamos escolher *Moeda para o Formato, 0 para o número de decimais e* ⬆ *Bom (verde) para a polaridade.*

**D**. Se você estiver usando tags, que permitem aplicar tópicos e localizar rapidamente as métricas calculadas, adicione as tags que se aplicam aqui. Adicionamos *AOV* e *Central de atendimento* tags.

**E.** Esta seção é para exibição - à medida que você cria sua métrica calculada na seção F, a fórmula será exibida aqui.

**F.** Aqui, você arrastará e soltará dimensões (H), métricas (I) ou segmentos (J) para criar sua métrica calculada, bem como os operadores para a fórmula. Para cada métrica, se você clicar no ícone de engrenagem, poderá alterar o Tipo de métrica (Padrão/Total) e o Modelo de atribuição. *Arrastaremos e soltaremos a Receita da Central de Atendimento, e logo abaixo disso, nós iremos*÷ ￼*. Aceitaremos o tipo de métrica padrão e o modelo de atribuição.*

**G**. Use este **+Adicionar** para adicionar condições adicionais ou números estáticos, que não precisamos aqui.

**K.** E finalmente, conforme você constrói o cálculo, você pode visualizar os dados dos últimos 90 dias aqui.

Agora que criamos o Call Center AOV, também precisamos de uma métrica calculada para o Online AOV. Faremos isso seguindo as mesmas etapas descritas acima.

Em seguida, podemos criar uma terceira métrica calculada, usando o Construtor de métricas calculadas ou em tempo real na tabela de forma livre, para comparar o Call Center e o Online AOV, de modo que acabamos com algo como isto:

![Calc 05](assets/calc05.png)

No nosso exemplo, vemos um aumento significativo quando os compradores usam a central de atendimento para ajudá-los a fazer uma compra. Esses dados podem então informar nossas decisões sobre como ajudar os clientes a obter assistência com suas compras, por exemplo, por meio de ofertas pop-up ou outras experiências guiadas.

## Uso de segmentos em métricas calculadas

Agora, vamos observar como podemos usar segmentos em métricas calculadas para obter mais informações sobre o comportamento, as preferências e as motivações do cliente. Com segmentos e métricas calculadas, podemos aprender o suficiente sobre os clientes para melhorar sua experiência, aumentar a receita e melhorar a satisfação e a fidelidade do cliente.

Já sabemos, com base nos exemplos acima, que as compras assistidas da central de atendimento normalmente têm um AOV mais alto. No entanto, outras métricas nos informam que a maioria dos usuários não usa a central de atendimento para compras.

Então, quais categorias de varejo - e caminhos de usuário por essas categorias - resultam no maior AOV?  Podemos descobrir ao combinar segmentos com métricas calculadas.

Para fazer isso, primeiro precisamos criar um nível de visita *incluir* e *exclude* segmentos para cada categoria de produto. Incluir ou excluir é determinado ao clicar no botão **Opções** no canto direito do contêiner. O padrão é Incluir.

![Calc 06](assets/calc06.png) ![Calc 07](assets/calc07.png)

Depois de criar esses segmentos, podemos criar uma métrica calculada para fornecer a resposta à sua pergunta. Abrimos o Criador de métricas calculadas e fazemos o seguinte:

1. Procure os segmentos recém-criados e arraste e solte os que queremos usar na área cinza na parte superior do **Definição** caixa. Por exemplo, se queremos criar um AOV para usuários que visitaram as categorias de Mulheres e Homens, mas não de Crianças, podemos arrastar e soltar esses três segmentos nessa área: *Incluir mulheres*, *Incluir masculino* e *Excluir Kids*. Chamamos isso *empilhamento de segmentos*.

   ![Calc 09](assets/calc09.png) ![Calc 08](assets/calc08.png)

1. Em seguida, arrastamos e soltamos o **Receita online** no mesmo contêiner, em seguida **Pedidos online**. Como os contêineres funcionam como expressões matemáticas para determinar a ordem das operações, os itens em contêineres são processados antes dos processos subsequentes, embora não tenhamos vários contêineres ou processos nesse cálculo.
1. Alteramos o operador entre as duas métricas para divisão ( igual).
1. Selecionamos **Moeda** como formato, **0** casas decimais e **UP** para polaridade.
1. Nomeie a métrica calculada e forneça uma descrição.
1. Salvar.

Quando terminamos, nossa métrica calculada fica assim:

![Calc 10](assets/calc10.png)

Depois de criar métricas calculadas usando segmentos empilhados para cada combinação da jornada de categoria do visitante e observar os dados, veja o que aprendemos! Os usuários que visitam as categorias de Mulheres e Homens durante sua visita têm o maior AOV e, em comparação com os visitantes de uma única categoria, o aumento é significativo:

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Sabendo disso, podemos otimizar o layout da página, disposições de produtos e mensagens promocionais para colocar mais pessoas nessas categorias antes de fazer check-out.

## Valioso, mas não disponível em todos os lugares

**Assim, as métricas calculadas, simples e complexas, são super valiosas para os analistas!**

No entanto, essas métricas não estão disponíveis em todas as áreas do Adobe Analytics. Não é possível usar métricas calculadas em:

- Fallout na Analysis Workspace
- Análise de coorte no Analysis Workspace
- Data warehouse
- Relatórios em tempo real
- Relatórios de Dados atuais
- Analytics for Target
- Report Builder

## Práticas recomendadas para métricas calculadas

Agora que você sabe o quão valiosas as métricas calculadas podem ser, vamos observar algumas práticas recomendadas para criá-las.

1. **Verifique a sintaxe da fórmula.** Verifique se a sintaxe da fórmula está correta e segue a sintaxe do Adobe Analytics para garantir que você obtenha informações significativas.
1. **Verifique a ordem das operações.** Use os contêineres com cuidado e coloque as coisas em uma ordem matemática adequada de operações.
1. **Não contar dados duas vezes**. Você pode evitar a dupla contagem de dados, garantindo que a fórmula usada na métrica calculada não conte os mesmos dados várias vezes. Isso é frequentemente conseguido através da combinação *Incluir* e *Excluir* condições na métrica calculada ou por meio do uso de segmentos.
1. **Verifique a granularidade de tempo.** Certifique-se de que a métrica calculada tenha a mesma granularidade de tempo que as métricas de origem usadas na fórmula.
1. **Use dados precisos:** Você só obterá resultados valiosos se usar dados precisos e confiáveis no cálculo.

## Práticas recomendadas do segmento personalizado

Ao criar segmentos no Adobe Analytics, lembre-se das práticas recomendadas a seguir:

1. **Mantenha simples.** Evite complicar demais o segmento. Mantenha-o o mais simples possível e use apenas as condições necessárias para garantir a precisão.
1. **Usar os tipos de contêiner corretos**. Certifique-se de usar o tipo de contêiner correto - visitante, visita ou ocorrência - na definição do segmento para evitar obter resultados incorretos.
1. **Não contar dados duas vezes**. Assim como com métricas calculadas, verifique se o segmento não conta os mesmos dados várias vezes. Incluir e excluir contêineres pode ajudar.
   1. Quando um contêiner de inclusão é usado, ele *inclui* *todo o conteúdo da visita* se qualquer ocorrência corresponder à condição na visita.
   1. Quando um contêiner de exclusão é usado, ele *exclui todo o conteúdo da visita* se qualquer ocorrência corresponder à condição na visita.
1. **Aninhar contêineres adequadamente**. Determine quais dados estão incluídos usando o contêiner mais externo e, em seguida, aplique regras aninhadas aos dados restantes. À medida que regras aninhadas são aplicadas, o fluxo do segmento age como um funil, e as regras subsequentes não se aplicam a quaisquer ocorrências que a primeira regra excluiu.
1. **Verifique se os dados estão atualizados.** Certifique-se de usar dados precisos e atualizados na definição do segmento para obter resultados precisos.
1. **Teste o segmento.** Sempre teste o segmento para verificar se ele está funcionando conforme o esperado antes de liberá-lo para outros.
1. **Considere o desempenho.** Os segmentos podem atrasar o processamento do relatório, portanto, considere esse impacto ao criá-los.

## Principais aprendizados

A combinação de segmentos e métricas calculadas no Adobe Analytics pode absolutamente levar a uma análise de dados mais robusta e eficaz. Ao cortar e cortar seus dados e criar cálculos para comparação, você pode obter insights mais profundos sobre o comportamento do cliente que você pode usar para otimizar suas campanhas de marketing e criar painéis e relatórios personalizados. No entanto, lembre-se de que as métricas calculadas não estão disponíveis em todas as áreas do Adobe Analytics e certifique-se de seguir as práticas recomendadas para garantir que você obtenha dados precisos e úteis.


## Autora

Este documento foi escrito por:

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, Gerente sênior da Adobe Analytics na Adswerve

![Adswerve](assets/calc14.png)
