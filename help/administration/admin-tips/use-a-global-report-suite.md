---
title: Usar um conjunto de relatórios global
description: Ter um único conjunto de relatórios global pode ajudar de várias maneiras e realmente simplificar sua implementação.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10536.jpg
kt: 10536
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 0%

---


# Usar um conjunto de relatórios global

**O QUE:** É tentador criar conjuntos de relatórios para cada um de seus sites, mas isso pode se tornar rapidamente seu pior pesadelo - tanto em termos de complicar seus relatórios quanto em sua implementação. Ter um único conjunto de relatórios global pode ajudar de várias maneiras e realmente simplificar sua implementação.

**POR QUE:** Criar um conjunto de relatórios global é a única opção para ter uma exibição unificada das propriedades digitais e das jornadas dos usuários em cada propriedade. Se você tiver um aplicativo para dispositivos móveis e um site, deve sempre combinar os dados do aplicativo e os dados da Web em um conjunto de relatórios para aproveitar as jornadas entre dispositivos e rastrear aqueles que visitam ambas as propriedades como um único visitante vs. com conjuntos de relatórios separados, onde você teria um conjunto de dados desarticulado mostrando 2 visitantes - 1 para cada propriedade - sem saber o cruzamento.

Estas são as vantagens/desvantagens de ter um único conjunto de relatórios para ajudá-lo a pesar suas opções:

* PROS:
   * Ser capaz de entender facilmente todo o seu cenário digital. Se você implementou a dimensão &quot;propriedades&quot; (eVar) referenciada em outras dicas, será muito fácil obter uma única visualização de todos os sites e aplicativos, tráfego e conversões. Ter essa visão geral é fundamental para entender sua empresa em geral.
   * No mesmo sentido, agora você pode ver como os usuários fluem em todas as suas propriedades e compreender a jornada deles em todo o seu cenário digital.
   * Facilidade de administração. Ao usar vários conjuntos de relatórios, será necessário manter a interface em vários locais, bem como vários documentos de marcação (ou um mais complicado). Manter tudo em um só lugar significa que só há um lugar para fazer atualizações. Também facilita muito a concessão de acesso.
   * Melhor usabilidade na interface. Se os usuários tiverem apenas um local para acessar, eles não precisarão pensar em qual conjunto de relatórios selecionar. Lembre-se de que não é possível usar vários conjuntos de relatórios no mesmo painel do espaço de trabalho, e ter vários deles pode confundir os usuários.
   * Menos chamadas de servidor = menos custos. Se você fizer chamadas para vários conjuntos de relatórios, aumentará seus custos. Manter a implementação simples também manterá os custos baixos.
   * Você pode simplesmente aproveitar os conjuntos de relatórios virtuais (VRS) para dividir dados específicos do site no conjunto de relatórios global e restringir as permissões do usuário com base em um VRS, se necessário. Depois que os dados são separados em conjuntos de relatórios individuais, não é possível acumulá-los, mas se já estiverem unidos em um conjunto de dados (RS global), eles serão facilmente divididos.
* CONS:
   * Se você tiver propriedades muito separadas, nas quais os usuários não fazem cortes de um para o outro e nunca devem fazê-lo, convém manter conjuntos de relatórios separados.
   * Se suas propriedades tiverem necessidades de marcação e relatórios muito diferentes, pode ser interessante configurar conjuntos de relatórios separados para aumentar a eficiência das variáveis. Ter conjuntos de relatórios separados proporcionará mais flexibilidade ao usar variáveis personalizadas (mais eVars).
   * Únicos excedidos: A interface do Adobe Analytics permite visualizar apenas 500.000 valores únicos em uma única dimensão em um determinado período de tempo. Após exceder isso, os valores serão agrupados como &quot;únicos excedidos&quot; ou &quot;tráfego baixo&quot; na interface. Esses valores permanecem disponíveis para você no back-end (ou seja, Data Warehouse, Feeds de dados), mas não podem ser visualizados na interface. Se você tiver dados muito granulares (como ID de usuário, PSN etc.), é fácil alcançar esse nível. Ter conjuntos de relatórios separados pode ajudar nesse problema.

**COMO:** Começar com uma nova implementação AA e usar um conjunto de relatórios global é simples e direto. Você só precisaria criar o conjunto de relatórios global (um para Dev e um para Prod) na interface de administração AA e aplicar os mesmos valores de ID de conjunto de relatórios (RSID) em todas as suas propriedades.

A migração de uma estratégia de multitags com um conjunto de relatórios exclusivo por propriedade requer mais estratégia e planejamento. Algumas das considerações que você precisará ter em mente:

* Alinhamento de suas variáveis (ou seja, eVar1 na Propriedade A precisa capturar o mesmo ponto de dados que o eVar1 na Propriedade B)
* Consolidação de quaisquer regras de processamento, regras de canal de marketing, classificações (SAINT e Construtor de regras)
* Migração de feeds de dados e fontes de dados
* Escolha de uma data limite e comunicação com todos os usuários empresariais

## Autores

Este documento foi co-escrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, gerente de plataforma de análise digital do NortonLifeLock Adobe Analytics Campeion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Consultor Sênior na Adobe
