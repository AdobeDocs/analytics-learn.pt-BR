---
title: Adeus Excel, olá métricas calculadas
description: Saiba mais sobre os benefícios de usar métricas calculadas no Adobe Analytics e como elas podem fornecer uma visualização dinâmica e contínua dos dados neste artigo.
feature: Calculated Metrics
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13178
thumbnail: KT-13178.jpeg
exl-id: d4f69244-6614-41f3-ac48-70adabb8a8e7
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1286'
ht-degree: 2%

---

# Adeus Excel, olá métricas calculadas

Saiba mais sobre os benefícios de usar métricas calculadas no Adobe Analytics e como elas podem fornecer uma visualização dinâmica e contínua dos dados neste artigo.

Ei! Por que você está no Excel agora? Quero dizer, eu sei por quê. Você tem relatórios para chegar às pessoas certas. Você está ocupado inserindo dados do Adobe Analytics e calculando taxas de conversão, traçando-as e se preparando para colocá-las em um PowerPoint que está se encaminhando para os tomadores de decisão. Realmente espero que você esteja pelo menos usando o Report Builder para fazer isso, mas sei que alguns de vocês estão copiando e colando dados manualmente de um Workspace para o Excel.

Por quê?

Por que passar por um processo manual todo mês? Por que apresentar uma visualização estática uma vez por mês em vez de uma visualização dinâmica e contínua? Por que copiar isso para o PowerPoint? Por que não criar métricas calculadas diretamente no Adobe Analytics?

## As métricas calculadas são poderosas

Métricas calculadas são poderosas, mas até mesmo as funções matemáticas básicas são realmente úteis e melhorias sérias sobre fazer a matemática no Excel. Vamos analisar alguns dos benefícios e alguns casos de uso:

1. **As métricas calculadas são atuais e dinâmicas**

   Quando você exporta números do Adobe Analytics, eles são bloqueados em um ponto no tempo. Você realmente precisa saber o desempenho de seu site ou aplicativo no mês anterior, mas como os tomadores de decisão acompanham o andamento da metade do mês? Se seu índice de conversão cair por um dia e, em seguida, reverter para a média até o final do mês, você sabe? Esse mergulho pode ser um dado valioso que revela uma importante questão de telemetria, ou ainda mais vital, uma mudança no comportamento do visitante. Com uma métrica calculada, você pode fazer um gráfico e vê-lo no dia em que ocorre, deixando você pronto para responder.

1. **As Métricas Calculadas Economizam Seu Tempo**

   Eu estive lá. Copiar/colar. Insira a fórmula ou arraste a célula acima dela para baixo. Clique no gráfico e altere o intervalo para que você tenha os últimos doze ou treze meses. Agora copie o gráfico. Agora faça de novo. E de novo. E de novo. Envie o PowerPoint. É tedioso e demorado e parece que você tem que fazer isso todos os meses para sempre.

   Em vez disso, você pode criar uma Workspace que use sua métrica calculada, tenha Doze ou Treze últimos meses completos como intervalo de datas e fazer com que os dados e o gráfico sejam atualizados automaticamente no traço da meia-noite no primeiro dia de cada mês. Os recipients podem ter acesso direto à Workspace. Eles podem ter uma cópia do PDF enviada automaticamente por email a eles no primeiro dia do mês ou após o uso de Visualizações de texto para adicionar comentários sobre os dados (você sabe, a parte divertida dos relatórios).

1. **Métricas calculadas podem ser aplicadas a grandes conjuntos de dados**

   Você poderia exportar todos os nomes de produtos para o Excel e começar a calcular taxas de conversão e receita por visitante, mas isso se torna um incômodo quando se tem cerca de 100.000. Não é um problema com as métricas calculadas. Solte sua dimensão em uma tabela como de costume e use suas Métricas calculadas como as métricas. Agora você tem uma tabela classificável dinâmica que será atualizada automaticamente à medida que os produtos ou qualquer dimensão que você estiver usando forem adicionados ao catálogo.

1. **Métricas calculadas evitam erros**

   Ocorrem erros do Excel. Todos nós já estivemos lá. Puxa, toda a economia da Grécia e a reputação de dois acadêmicos estimados foram arruinados por causa de um erro de fórmula Excel. Você provavelmente não tem uma economia europeia baseada em suas habilidades no Excel, mas definitivamente há alguma decisão sobre os orçamentos que mudarão com base em seus números. Usar métricas calculadas significa criar uma métrica, mantê-la para controle de qualidade e não se preocupar com ela novamente.

### Agora que já falamos sobre os benefícios de usar métricas calculadas, vamos ver como colocá-las em prática

**Caso de Uso 1: Taxas de Conversão**

A maioria das taxas de conversão é apenas uma simples divisão. Divida o número de conversões pelo número de visitantes ou visitas. Divida o número de exibições de página para a página final de uma funnel pelo número de exibições de páginas para a primeira página de uma funnel. Divida o número de cliques internos na campanha pelo número de impressões. Tudo isso pode ser facilmente feito como métricas calculadas e colocado em um painel, aproveitando a baixa latência de dados, a atualização de visualizações e uma maior capacidade de compartilhamento.

**Caso de Uso 2: Pesquisa Interna**

A pesquisa interna é uma das ferramentas mais importantes para entender seu site. Os resultados da pesquisa do site informam em que seus visitantes estão interessados e se eles podem encontrá-lo facilmente por meio da navegação ou não. Você tem que ser capaz de dizer se sua pesquisa de site está funcionando bem e usar um pouco de adição e divisão básica pode dar-lhe essa resposta.

Vamos começar com os resultados da pesquisa. Você quer saber se um termo de pesquisa obtém resultados ou não traz nada. Normalmente, são eventos separados. Você deseja passar pelo problema de obter um terceiro evento para todas as pesquisas internas de sites adicionadas? Em vez disso, dê uma pausa aos desenvolvedores e use Métricas calculadas para adicionar Pesquisa interna: Resultados e Pesquisa interna: Nenhum resultado juntos para obter o Total de pesquisas internas.

Qual porcentagem das pesquisas não retorna resultados? Dividir pesquisa interna: Nenhum resultado pela nova Métrica calculada do Total de pesquisas internas. Agora você sabe se criar novo conteúdo para corresponder a esses termos de pesquisa é urgente ou se talvez sua equipe de conteúdo pode lidar com prioridades mais altas.

Queremos saber quantas dessas pesquisas com resultados obtêm cliques e geralmente têm uma métrica separada para isso também. Use Métricas calculadas para dividir o número de cliques pelo número de vezes que o termo apresentou resultados de pesquisa e exibi-lo como uma porcentagem. Agora você tem a taxa de cliques para cada termo de pesquisa interna em seu site. Você pode isolar os termos de pesquisa que estão trazendo resultados inúteis. Ele tem todos os dados históricos disponíveis para você poder mapeá-los e, à medida que você faz melhorias, você pode ver facilmente se eles estão trabalhando, observando essa taxa subir ou descer.

Divida o número de pesquisas internas pelo número de visitantes de pesquisa. Você tem pesquisas por visitante para cada termo. Se esse número for alto (quanto mais próximo de 1,0 melhor), você terá um de dois problemas possíveis. Os resultados clicados são ruins e seus visitantes estão fazendo várias pesquisas para encontrar os melhores resultados, ou não conseguem encontrar as páginas que estão procurando por meio da navegação.

Como você pode medir se essas páginas principais podem ser encontradas por meio da sua navegação? Crie uma métrica calculada para exibições de página que se seguiram a uma exibição de página de resultados da pesquisa. Divida isso pelo total de exibições da página. Agora você sabe a porcentagem de exibições de página que vêm dos resultados da pesquisa. Se você tiver uma alta porcentagem, provavelmente terá trabalho a fazer em navegação.

### As Métricas Calculadas São Poderosas

Espero que isso tenha mostrado a vocês algumas das possibilidades de usar funções matemáticas básicas em Métricas calculadas e que vocês mesmos comecem a construir algumas. Isso só começa a descrever as possibilidades matemáticas que você pode fazer em Métricas calculadas, mesmo com quatro funções simples. As métricas calculadas podem ajudar você a entender o comportamento do visitante em um nível totalmente novo e, uma vez que tenha o jeito certo, você abriu as portas para usar funções mais complexas que também estão disponíveis para você.

## Autora

Este documento foi escrito por:

![Captura de cabeça do Gittai](assets/gittai.png)

**Gitai Ben-Ammi**, Consultor principal do Concentrix Catalyst

Especialista no Adobe Analytics
