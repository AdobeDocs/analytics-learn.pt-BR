---
title: Eleve suas análises de dados a um novo patamar com as Métricas calculadas
description: Saiba como um especialista ponto a ponto usa métricas calculadas para criar novas métricas sem alterar sua implementação e usar os dados já coletados para ajudar a responder a perguntas comerciais complexas.
feature: Calculated Metrics
role: User
level: Beginner
doc-type: Article
last-substantial-update: 2023-05-16T00:00:00Z
jira: KT-13266
thumbnail: KT-13266.jpeg
exl-id: 74793149-9967-4765-832c-c65e578ee34b
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1582'
ht-degree: 3%

---

# Eleve suas análises de dados a um novo patamar com as Métricas calculadas

A maioria dos novos usuários do Adobe Analytics está familiarizada com os Segmentos como uma maneira de cortar e dividir seus dados. Hoje, quero apresentar a vocês as métricas calculadas, a próxima melhor ferramenta da sua caixa de ferramentas de analistas.

Como um recurso avançado do Adobe Analytics, as métricas calculadas permitem criar novas métricas sem alterar a implementação usando os dados já coletados. O Construtor de métricas calculadas pode usar várias funções matemáticas e estatísticas diferentes, para que você possa criar métricas que respondam até mesmo às perguntas comerciais mais complexas.

## Introdução às métricas calculadas

Para começar a usar métricas calculadas, vejamos um exemplo simples. Imagine que você queira entender se os usuários de autoatendimento online têm um valor médio de pedido (AOV) mais alto do que os usuários assistidos por chamada. Para criar uma métrica calculada para responder a essa pergunta, faça o seguinte:

Para abrir o Construtor de métricas calculadas, use a navegação superior para clicar em → **Componentes** → **Métricas calculadas** → **+ Adicionar.** Ou clique no sinal de **+** acima de **Métricas** no painel Componentes.


![Calc 01](assets/calc01.png) ![Calc 02](assets/calc03.png) ![Calc 03](assets/calc02.png)

![Calc 04](assets/calc04.png)

*Descrições abaixo para itens de interface do usuário*

Depois que o Construtor de métricas calculadas for aberto, adicione e/ou faça o seguinte:

**A.** Um nome para a métrica calculada. Este nome é exibido na lista de componentes de métricas, portanto, torne-o algo que ficará claro para você mesmo e para outras pessoas, como *Call Center AOV*.

**B.** Uma descrição da métrica calculada. Esta descrição aparece quando os usuários clicam em &#39;**i**&#39; ao lado da métrica na lista de componentes; portanto, verifique se ela é informativa. Por exemplo, para o AOV da central de atendimento, podemos adicionar *Calcula o AOV para Pedidos assistidos da central de atendimento*.

**C.** O formato da métrica: escolha decimal, hora, porcentagem ou moeda, e adicione casas decimais e polaridade. Aqui, vamos escolher *Moeda para o Formato, 0 para o número de decimais e* ⬆ *Bom (Verde) para a polaridade.*

**D**. Se você estiver usando tags, que permitem aplicar tópicos e localizar rapidamente métricas calculadas, adicione aqui as tags que se aplicam. Adicionamos as marcas *AOV* e *Call Center*.

**E.** Esta seção é para exibição - à medida que você cria sua métrica calculada na seção F, a fórmula será exibida aqui.

**F.** Aqui, você arrastará e soltará dimensões (H), métricas (I) ou segmentos (J) para criar sua métrica calculada, bem como os operadores da fórmula. Para cada métrica, se você clicar no botão de rolagem, será possível alterar o Tipo de métrica (Padrão/Total) e o Modelo de atribuição. *Arrastaremos e soltaremos a Receita da Central de Atendimento e, abaixo dela, vamos**. Aceitaremos o tipo de métrica padrão e o modelo de atribuição.*

**G**. Use esta opção **+Adicionar** para adicionar condições ou números estáticos adicionais, que não são necessários aqui.

**K.** E, finalmente, ao criar seu cálculo, você pode visualizar os dados dos últimos 90 dias aqui.

Agora que criamos o AOV da Central de Atendimento, também precisamos de uma métrica calculada para o AOV Online. Fazíamos isso seguindo as mesmas etapas descritas acima.

Em seguida, podemos criar uma terceira métrica calculada, usando o Construtor de métricas calculadas ou dinamicamente na tabela de forma livre, para comparar a Central de atendimento e o AOV online, de modo que tenhamos algo como isso:

![Calc 05](assets/calc05.png)

Em nosso exemplo, vemos um aumento significativo quando os compradores usam a central de atendimento para ajudá-los a fazer uma compra. Esses dados podem informar nossas decisões sobre como ajudar os clientes a obter assistência com suas compras por meio de, por exemplo, ofertas pop-up ou outras experiências guiadas.

## Utilização de segmentos em métricas calculadas

Agora, vejamos como podemos usar segmentos em métricas calculadas para obter mais insight sobre comportamento, preferências e motivações do cliente. Com segmentos e métricas calculadas, podemos aprender o suficiente sobre os clientes para melhorar sua experiência, aumentar a receita e melhorar a satisfação e a fidelidade do cliente.

Já sabemos pelos exemplos de AOV acima que as compras assistidas pela central de atendimento normalmente têm uma AOV mais alta. No entanto, outras métricas nos informam que a maioria dos usuários não usa a central de atendimento para compras.

Então, quais categorias de varejo - e caminhos de usuário por meio dessas categorias - resultam no AOV mais alto?  Podemos descobrir ao combinar segmentos com métricas calculadas.

Para fazer isso, primeiro precisamos criar segmentos *include* e *exclude* no nível da visita para cada categoria de produto. Incluir ou excluir é determinado ao clicar na engrenagem **Opções** no canto direito do contêiner. O padrão é Incluir.

![Calc 06](assets/calc06.png) ![Calc 07](assets/calc07.png)

Após criar esses segmentos, podemos criar uma métrica calculada para responder à sua pergunta. Abrimos o Criador de métricas calculadas e fazemos o seguinte:

1. Procure os segmentos recém-criados e arraste e solte os que queremos usar na área cinza na parte superior da caixa **Definição**. Por exemplo, se queremos criar uma AOV para usuários que visitaram categorias Femininas e Masculinas, mas não Infantis, podemos arrastar e soltar esses três segmentos nessa área: *Incluir Femininos*, *Incluir Masculinos* e *Excluir Infantis*. Chamamos isso de *segmentos de empilhamento*.

   ![Calc 09](assets/calc09.png) ![Calc 08](assets/calc08.png)

1. Em seguida, arrastamos e soltamos a métrica **Receita online** no mesmo contêiner e depois **Pedidos online**. Como os contêineres funcionam como expressões matemáticas para determinar a ordem das operações, os itens nos contêineres são processados antes dos processos subsequentes, embora não tenhamos vários contêineres ou processos nesse cálculo.
1. Alteramos o operador entre as duas métricas para divisão ().
1. Selecionamos **Moeda** como formato, **0** casas decimais e **UP** para polaridade.
1. Nomeie a métrica calculada e forneça uma descrição.
1. Salvar.

Quando terminarmos, nossa métrica calculada ficará assim:

![Calc 10](assets/calc10.png)

Depois de criarmos métricas calculadas usando segmentos empilhados para cada combinação da jornada de categoria do visitante e analisarmos os dados, veremos o que aprendemos! Os usuários que visitam as categorias Feminino e Masculino durante sua visita têm o AOV mais alto e, quando comparado aos visitantes de uma única categoria, o aumento é significativo:

![Calc 11](assets/calc11.png) ![Calc 12](assets/calc12.png)

Sabendo disso, podemos otimizar o layout da página, as disposições do produto e as mensagens promocionais para inserir mais pessoas nessas categorias antes de concluir a compra.

## Valioso, mas não disponível em todos os lugares

**Portanto, as métricas calculadas simples e complexas são super valiosas para analistas!**

No entanto, essas métricas não estão disponíveis em todas as áreas do Adobe Analytics. Não é possível usar métricas calculadas em:

- Fallout na Analysis Workspace
- Análise de coorte no Analysis Workspace
- Data Warehouse
- Relatórios em tempo real
- Relatórios de Dados atuais
- Analytics for Target
- Report Builder

## Práticas recomendadas de métricas calculadas

Agora que você sabe o quanto as métricas calculadas podem ser valiosas, vamos dar uma olhada nas práticas recomendadas para criá-las.

1. **Verifique a sintaxe da fórmula.** Verifique se a sintaxe da fórmula está correta e se segue a sintaxe do Adobe Analytics para obter informações relevantes.
1. **Verifique a ordem das operações.** Certifique-se de usar os contêineres com cuidado e colocar as coisas em ordem matemática adequada de operações.
1. **Não conte dados duas vezes**. É possível evitar a contagem dupla de dados, garantindo que a fórmula usada na métrica calculada não conte os mesmos dados várias vezes. Geralmente, isso é feito combinando as condições *Incluir* e *Excluir* na métrica calculada ou por meio do uso de segmentos.
1. **Verifique a granularidade de tempo.** Verifique se a métrica calculada tem a mesma granularidade de tempo que as métricas de origem usadas na fórmula.
1. **Usar dados precisos:** você só obterá resultados valiosos se usar dados precisos e confiáveis no cálculo.

## Práticas recomendadas do segmento personalizado

Ao criar segmentos no Adobe Analytics, lembre-se destas práticas recomendadas:

1. **Mantenha simples.** Evite complicar o segmento em excesso. Mantenha o mais simples possível e use apenas as condições necessárias para garantir a precisão.
1. **Usar os tipos de contêiner corretos**. Use o tipo correto de contêiner (visitante, visita ou ocorrência) na definição do segmento para evitar resultados incorretos.
1. **Não conte dados duas vezes**. Assim como com as métricas calculadas, verifique se o segmento não conta os mesmos dados várias vezes. Os contêineres Incluir e Excluir podem ajudar.
   1. Quando um contêiner de inclusão é usado, ele *inclui* *todo o conteúdo da visita* se qualquer ocorrência corresponder à condição na visita.
   1. Quando um container de exclusão é usado, ele *exclui todo o conteúdo da visita* se qualquer ocorrência corresponder à condição na visita.
1. **Aninhe corretamente os contêineres**. Determine quais dados são incluídos usando o contêiner mais externo e aplique regras aninhadas aos dados restantes. À medida que regras aninhadas são aplicadas, o fluxo de segmento atua como uma funnel e as regras subsequentes não se aplicam a nenhuma ocorrência excluída pela primeira regra.
1. **Verifique se seus dados estão atualizados.** Certifique-se de usar dados precisos e atualizados na definição do segmento para obter resultados precisos.
1. **Testar o segmento.** Sempre teste o segmento para verificar se ele está funcionando como pretendido antes de liberá-lo para outras pessoas.
1. **Considere o desempenho.** Segmentos podem retardar o processamento de relatórios, portanto, considere esse impacto ao criá-los.

## Principais aprendizados

A combinação de segmentos e métricas calculadas no Adobe Analytics pode resultar em uma análise de dados mais robusta e eficaz. Ao cortar e cortar seus dados e criar cálculos para comparação, você pode obter insights mais profundos sobre o comportamento do cliente que pode usar para otimizar suas campanhas de marketing e criar painéis e relatórios personalizados. No entanto, lembre-se de que as métricas calculadas não estão disponíveis em todas as áreas do Adobe Analytics e siga as práticas recomendadas para garantir que você esteja obtendo dados precisos e úteis.


## Autora

Este documento foi escrito por:

![Debbie Kern](assets/calc13.jpeg)

**Debbie Kern**, gerente sênior do Adobe Analytics na Adobe

![Resposta](assets/calc14.png)
