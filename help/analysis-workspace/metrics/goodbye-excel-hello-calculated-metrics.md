---
title: Adeus Excel, olá métricas calculadas
description: Saiba mais sobre os benefícios do uso de métricas calculadas no Adobe Analytics e como elas podem fornecer uma exibição dinâmica e contínua dos seus dados neste artigo.
feature: Calculated Metrics
role: User
level: Experienced
doc-type: Article
last-substantial-update: 2023-05-02T00:00:00Z
jira: KT-13178
thumbnail: KT-13178.jpeg
source-git-commit: 28db96c38e5318942ddc9f39ec0a2d561e14200c
workflow-type: tm+mt
source-wordcount: '1282'
ht-degree: 0%

---


# Adeus Excel, olá métricas calculadas

Saiba mais sobre os benefícios do uso de métricas calculadas no Adobe Analytics e como elas podem fornecer uma exibição dinâmica e contínua dos seus dados neste artigo.

Ei! Por que você está no Excel agora? Quero dizer, eu sei por quê. Você tem relatórios para chegar às pessoas certas. Você está ocupado inserindo dados do Adobe Analytics e calculando taxas de conversão, fazendo gráficos e preparando para colocar todos em um PowerPoint que está indo para os tomadores de decisão. Espero que você esteja usando o Report Builder para fazer isso, mas sei que alguns de vocês estão copiando e colando dados manualmente de um espaço de trabalho para o Excel.

Por quê?

Por que passar por um processo manual todo mês? Por que apresentar uma visualização estática uma vez por mês em vez de uma visualização dinâmica contínua? Por que copiar isso para o PowerPoint? Por que não criar métricas calculadas diretamente no Adobe Analytics?

## As métricas calculadas são poderosas

Métricas calculadas são poderosas, mas até mesmo as funções matemáticas básicas são realmente úteis e melhorias sérias em relação à execução da matemática no Excel. Vamos analisar alguns dos benefícios e alguns casos de uso:

1. **As métricas calculadas são atuais e dinâmicas**

   Quando você exporta números do Adobe Analytics, eles são bloqueados em um momento. É absolutamente necessário saber o desempenho de seu site ou aplicativo no mês anterior, mas como os tomadores de decisão controlam o ritmo das coisas no meio do mês? Se a taxa de conversão cair por um dia e, em seguida, reverter para a média até o final do mês, você sabe? Esse mergulho pode ser dados valiosos que revelam um importante problema de telemetria, ou ainda mais vital, uma mudança no comportamento do visitante. Com uma métrica calculada, é possível fazer um gráfico e visualizá-lo no dia em que ocorre, deixando você pronto para responder.

1. **Métricas calculadas economizam tempo**

   Estive lá. Copiar/colar. Insira a fórmula ou arraste a célula acima dela para baixo. Clique no gráfico e altere o intervalo para que você tenha os últimos doze ou treze meses. Agora, copie o gráfico. Agora faça de novo. E novamente. E novamente. Envie o PowerPoint. É entediante e demorado e parece que você tem que fazer isso todo mês para sempre.

   Em vez disso, você pode criar um espaço de trabalho que use sua métrica calculada, ter os Últimos 12 ou Treze Meses Completos como intervalo de datas e fazer com que os dados e o gráfico sejam atualizados automaticamente no traço da meia-noite do primeiro dia de cada mês. Os recipients podem ter acesso direto ao Workspace. Eles podem ter uma cópia de PDF automaticamente enviada por email para eles no primeiro dia do mês ou depois que você usar Visualizações de texto para adicionar seu comentário sobre os dados (você sabe, a parte divertida dos relatórios).

1. **Métricas calculadas podem ser aplicadas a grandes conjuntos de dados**

   Você poderia exportar todos os nomes de produtos para o Excel e começar a calcular taxas de conversão e receita por visitante, mas isso se torna um problema quando você tem cerca de 100.000. Não é um problema com Métricas calculadas. Solte sua dimensão em uma tabela como de costume e use suas Métricas calculadas como as métricas. Agora você tem uma tabela classificável dinâmica que será atualizada automaticamente como produtos ou qualquer dimensão que você esteja usando será adicionada ao seu catálogo.

1. **Métricas calculadas impedem erros**

   Ocorrem erros do Excel. Todos nós estivemos lá. Toda a economia grega e a reputação de dois acadêmicos estimados foram arruinadas devido a um erro de fórmula Excel. Você provavelmente não tem uma economia europeia aproveitando suas habilidades em Excel, mas definitivamente há alguma decisão sobre orçamentos que vão mudar com base em seus números. Usar métricas calculadas significa que você pode criar uma métrica, fazer um controle de qualidade e não se preocupar com ela novamente.

### Agora que ultrapassamos os benefícios de usar métricas calculadas, vamos ver como podemos colocá-las em prática

**Caso de uso 1 : Taxas de conversão**

A maioria das taxas de conversão é apenas uma divisão simples. Divida o número de conversões pelo número de visitantes ou visitas. Divida o número de exibições de página para a página final de um funil pelo número de exibições de páginas para a primeira página de um funil. Divida o número de click-throughs internos da campanha pelo número de impressões. Tudo isso pode ser facilmente feito como métricas calculadas e colocado em um painel com baixa latência de dados, atualização de visualizações e maior compartilhamento.

**Caso de uso 2: Pesquisa interna**

A pesquisa interna é uma das ferramentas mais importantes para entender seu site. Os resultados de pesquisa do site informam o que seus visitantes estão interessados e se eles podem encontrá-los facilmente por meio da navegação ou não. É necessário saber se a pesquisa do seu site está funcionando bem e usar um pouco de adição e divisão básicas pode lhe dar essa resposta.

Vamos começar com os resultados da pesquisa. Você quer saber se um termo de pesquisa obtém resultados ou não exibe nada. Esses são normalmente eventos separados. Deseja analisar o problema de obter um terceiro evento para todas as pesquisas internas do site adicionadas? Em vez disso, interrompa seus dispositivos e use Métricas calculadas para adicionar Pesquisa interna: Resultados e pesquisa interna: Nenhum resultado junto para obter o total de pesquisas internas.

Qual porcentagem de pesquisas não retorna resultados? Dividir Pesquisa Interna: Nenhum resultado por essa nova métrica calculada total de pesquisas internas. Agora você sabe se a criação de novo conteúdo para corresponder a esses termos de pesquisa é urgente, ou se talvez sua equipe de conteúdo possa lidar com prioridades mais altas.

Queremos saber quantas dessas pesquisas com resultados obtêm click-throughs e geralmente têm uma métrica separada para isso também. Use Métricas calculadas para dividir o número de click-throughs pelo número de vezes que o termo gerou resultados de pesquisa e exibiu como uma porcentagem. Agora você tem a taxa de cliques para cada termo de pesquisa interno em seu site. Você pode isolar os termos de pesquisa que estão trazendo resultados inúteis. Ele tem todos os dados históricos disponíveis para você para que você possa fazer um gráfico, e conforme você faz melhorias, você pode ver facilmente se eles estão trabalhando ao observar essa taxa subir ou descer.

Divida o número de pesquisas internas pelo número de visitantes que pesquisaram. Você tem pesquisas por visitante para cada termo. Se esse número for alto (quanto mais próximo, melhor será 1,0), você terá um de dois possíveis problemas. Os resultados que estão sendo clicados ou seus visitantes estão fazendo várias pesquisas para encontrar os melhores resultados, ou eles não podem encontrar as páginas que estão procurando por meio da navegação.

Como você pode medir se essas páginas-chave podem ser encontradas por meio de sua navegação? Crie uma métrica calculada para exibições de página que seguiram uma exibição de página de resultados da pesquisa. Divida isso pelo total de exibições de página para essa página. Agora você sabe a porcentagem de exibições de página que vieram dos resultados de pesquisa. Se você tiver uma porcentagem alta, provavelmente terá algum trabalho a ser feito na navegação.

### As Métricas Calculadas São Poderosas

Espero que isso tenha mostrado a vocês algumas das possibilidades de usar funções matemáticas básicas em Métricas calculadas e que você comece a criar algumas sozinho. Isso só começa a descrever as possibilidades da matemática que você pode fazer em Métricas calculadas, mesmo com quatro funções simples. As Métricas calculadas podem ajudá-lo a entender o comportamento do visitante em um nível totalmente novo e, uma vez que você tenha o tipo de comportamento, abriu a porta para usar funções mais complexas que também estão disponíveis para você.

## Autora

Este documento foi escrito por:

![Captura de cabeça de Gittai](assets/gittai.png)

**Gitai Ben-Ammi**, Consultor principal na Concentrix Catalyst

Especialista em Adobe Analytics
