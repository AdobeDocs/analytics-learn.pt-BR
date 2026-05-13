---
title: Truques simples para obter maior eficiência e autoatendimento — parte 1
description: Conheça os principais desafios que as equipes de análise enfrentam hoje e nossas recomendações para superá-los usando estratégias fora da interface do Adobe Analytics.
feature: Analytics Basics
role: Admin, Leader
level: Intermediate
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
TQID: https://experienceleague.adobe.com/tavjm7si5M73xvfMYmKLLCk6-c3Epjgv2oUtZiklnGE
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: a421fb65-2c82-457a-921c-28c46b697a39id: b069d60e-95f3-44d6-95a8-ddc862a4bc38id: e9dbdbc5-3e52-40f0-a7bc-e18542967b7aid: fd307ce7-56f5-4ee3-af68-a7833ff6e85e
subfeature_v2: id: e7d92df1-c5ba-4e93-85df-f83171b889be
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: d3cdead0-685a-4489-9250-4bb709942f66id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 727
ht-degree: 94%

---

# Adobe Analytics: Truques simples para maior eficiência e autoatendimento

**Parte 1: fora da interface**

Este artigo descreve os principais desafios que as equipes de análise enfrentam hoje e nossas recomendações para superá-los usando estratégias fora da interface do Adobe Analytics.

## Principais desafios para as equipes do Analytics

Muitas equipes do Analytics possuem uma distribuição de trabalho desequilibrada. Em vez de uma combinação de 80% de análise e 20% de implementação, muitas organizações fazem o inverso disso. A maior parte dos esforços é gasta na configuração, criação de relatórios e fornecimento de suporte, não na produção de análises que tragam insights de alto valor.

As equipes do Analytics esgotam sua produtividade e eficiência por vários motivos. Isso inclui implementações em constante mudança e em evolução, tentando manter a confiança organizacional nos dados e reduzindo o volume de negócios dos analistas. A redução do volume de negócios evita o longo processo de treinamento de novos membros da equipe em ferramentas de implementação personalizadas e desconhecidas.

Outros desafios principais que os analistas enfrentam:

* **Concorrência:** as empresas de varejo online e de vários canais tornam-se mais competitivas.
* **Expectativas do cliente:** as experiências do cliente e as estratégias de marketing tornam-se mais complexas.
* **Valor dos dados:** o valor de dados e insights precisos para impulsionar uma vantagem competitiva torna-se mais importante.
* **Expectativas das partes interessadas:** parceiros comerciais, participantes e executivos solicitam cada vez mais dados antes da aprovação.
* **Gestão de projetos:** a equipe de análise recebe muitas solicitações para implementar a coleta de dados de um fluxo interminável de novos recursos, além de produzir relatórios precisos, integrar novos analistas e descobrir o próximo novo insight.

## Chaves para a eficiência: fora da interface

1. Mantenha sua [Referência de design de solução](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (SDR) atualizada:

   * O SDR é a principal fonte da verdade para a definição e o uso pretendido de todas as variáveis na implementação da análise.
   * O SDR é a principal referência que os usuários devem conhecer para obter valor da interface do Adobe Analytics.
   * É importante mantê-la atualizada e fazer controle de versão (um formato de data simples pode ser usado).

1. Documentação e governança da coleta de dados — especificações técnicas:

   A especificação técnica tem um público-alvo mais limitado do que o SDR, mas é tão importante quanto, se não mais, para uma implementação totalmente funcional. Uma boa especificação técnica deve conter todos os recursos de desenvolvimento, controle de qualidade e gerenciamento de tags necessários para implementar a solução. Certifique-se de manter quantos documentos forem necessários para acomodar arquiteturas de implementação exclusivas.

   **Especificações técnicas**

   _Caso de Uso :_Instruções que descrevem como criar scripts para a coleta de dados

   _Usuários Primários :_Desenvolvedores

   _Outras Anotações :_

   * Documento altamente técnico criado especificamente para seus ambientes de implantação
   * Útil para a implementação inicial e manutenção/referência subsequentes
   * Organizado por tipo de solução (por exemplo, rastreamento de campanha, metadados de página e assim por diante).
   * O documento principal precisa ser atualizado e mantido à medida que as alterações de SDR são feitas
   * Repositório central
   * Números de versão sincronizados para o SDR e a especificação técnica

1. Comunicar e documentar o propósito de design da solução no lançamento:

   * Comunique-se mantendo o usuário em mente
   * Ao lançar ou aprimorar a coleta de dados, crie resumos simples que possam ser compartilhados com as partes interessadas
   * Reforce o uso adequado de variáveis desde o início
   * Envie um email de anúncio de lançamento resumido para as principais partes interessadas e analistas
   * Crie uma biblioteca que possa ser usada em apoio ao horário comercial, às sessões de capacitação de equipe ou para integração específica da equipe

1. Documentação de coleta dos dados, governança e higiene dos dados — AHD:

   O Painel de integridade do Analytics (AHD) detalha um conjunto de relatórios _individual_ e fornece uma visualização dos dados coletados em cada componente (eVar, propriedade e evento). Isso pode ajudar a apontar se os dados pararam de coletar em um componente para que você possa tomar medidas para corrigir o problema. Você pode executar esse painel a qualquer momento no futuro, para qualquer conjunto de relatórios.

   Painel de integridade do Analytics (AHD):

   _Instantâneo de Caso de Uso :_de cada métrica e dimensão capturada por um único conjunto de relatórios

   _Usuários Primários :_Líderes de Análise SME e/ou Desenvolvimento

   _Outras Anotações :_
   * Entregue por meio do Excel usando uma integração personalizada da API de relatórios da Adobe
   * Os usuários devem ter acesso à API dos serviços web do Analytics
   * Existem opções para semiautomatizar

1. Ganhe por meio da expansão do mundo dos especialistas no assunto (SMEs):

   * Estabeleça SMEs nas várias equipes da organização
   * Construa a presença deles ajudando a divulgar versões e vitórias
   * Use o horário comercial para ajudar a capacitar os treinadores e reduzir as solicitações ad hoc

Saiba mais sobre estratégia e liderança de pensamento na central de [Sucesso do cliente](https://experienceleague.adobe.com/docs/customer-success/customer-success/overview.html?lang=pt-BR).