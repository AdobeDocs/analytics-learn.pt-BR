---
title: Hacks simples para maior eficiência e autoatendimento - parte 1
description: Conheça os principais desafios que as equipes de análise enfrentam hoje e nossas recomendações para superá-las usando estratégias fora da interface do usuário do Adobe Analytics.
solution: Analytics
exl-id: 5d1077fd-d006-4a85-bf1c-54f6b2d31934
source-git-commit: dad200fdb5c5d15c00254d693fb47bbcec80afaf
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 0%

---

# Adobe Analytics: Hacks simples para maior eficiência e autoatendimento

**Parte 1: Fora da interface do usuário**

Este artigo descreve os principais desafios que as equipes de análise enfrentam hoje, e nossas recomendações para superá-las usando estratégias fora da interface do Adobe Analytics.

## Principais desafios para as equipes do Analytics

Muitas equipes do Analytics se encontram com uma distribuição desequilibrada do trabalho. Em vez de uma combinação de 80% de análise e 20% de implementação, muitas organizações se encontram no inverso disso. Eles veem a maior parte dos esforços gastos na configuração, criação de relatórios e fornecimento de suporte, em vez de produzir análises que impulsionam insights de alto valor.

As equipes do Analytics estão encontrando sua produtividade e eficiência esgotadas por vários motivos. Isso inclui as implementações em constante mudança e em evolução, tentando manter a confiança organizacional nos dados e reduzindo o volume de negócios dos analistas. A redução do volume de negócios evita o longo processo de treinamento de novos membros da equipe em ferramentas de implementação personalizadas desconhecidas.

Outros desafios principais que os analistas enfrentam:

* **Concorrência:** As empresas de varejo online e de vários canais tornam-se mais competitivas.
* **Expectativas do cliente:** As experiências do cliente e as estratégias de marketing se tornam mais complexas.
* **Valor dos dados:** O valor de dados e insights precisos para impulsionar uma vantagem competitiva torna-se mais importante.
* **Expectativas das partes interessadas:** Parceiros comerciais, participantes e executivos solicitam cada vez mais dados antes da aprovação.
* **Gestão de projetos:** A equipe de análise recebe solicitações para implementar a coleta de dados para um fluxo interminável de novos recursos, além de produzir relatórios precisos, integrar novos analistas e descobrir o próximo novo insight.

## Chaves para a eficiência: Fora da interface do usuário

1. Mantenha seu [Referência de design da solução](/help/implementation/implementation-basics/creating-and-maintaining-an-sdr.md) (DSE) atualizado:

   * O SDR é a principal fonte de verdade para a definição e o uso pretendido de todas as variáveis na implementação do Analytics.
   * O SDR é a principal referência que os usuários devem conhecer para obter valor da interface do usuário do Adobe Analytics.
   * É importante mantê-la atualizada e com controle de versão (um formato de data simples pode ser usado).

1. Documentação e governança da coleta de dados - especificações técnicas:

   A especificação técnica tem um público-alvo mais limitado do que o SDR, mas é tão importante, se não mais, para uma implementação totalmente funcional. Uma boa especificação técnica deve ser todos os recursos de desenvolvimento, controle de qualidade e gerenciamento de tags necessários para implementar a solução. Certifique-se de manter quantos documentos forem necessários para acomodar arquiteturas de implementação exclusivas.

   **Especificações técnicas**

   _Caso de uso:_ Instruções que descrevem como criar scripts para coleta de dados

   _Usuários principais:_ Desenvolvedores

   _Outras observações:_

   * Documento altamente técnico criado especificamente para seus ambientes de implantação
   * Útil tanto para a implementação inicial como para a manutenção/referência subsequente
   * Organizado por tipo de solução (por exemplo, rastreamento de campanha, metadados de página e assim por diante).
   * O documento principal precisa ser atualizado e mantido à medida que as alterações de SDR são feitas
   * Repositório central
   * Números de versão sincronizados para SDR e especificação técnica

1. Comunicar e documentar o propósito de design da solução na inicialização:

   * Comunique-se com o usuário em mente
   * Ao lançar ou aprimorar a coleta de dados, crie resumos simples que podem ser compartilhados com as partes interessadas
   * Reforçar o uso adequado da variável para fora da porta
   * Envie um email de lançamento de resumo para as principais partes interessadas e analistas
   * Crie uma biblioteca que possa ser usada para oferecer suporte ao horário comercial, às sessões de capacitação de equipe ou para integração específica da equipe

1. Documentação, governança e higiene dos dados da coleta de dados - AHD:

   O Analytics Health Dashboard (AHD) aprofunda um _individual_ e fornece uma visualização dos dados coletados em cada componente (eVar, propriedade e evento). Isso pode ajudar a apontar se os dados pararam de coletar em um componente para que você possa tomar medidas para corrigir o problema. Você pode executar esse painel a qualquer momento no futuro para qualquer conjunto de relatórios.

   Painel de integridade do Analytics (AHD):

   _Caso de uso:_ Instantâneo de cada métrica e dimensão capturada por um único conjunto de relatórios

   _Usuários principais:_ PME e/ou desenvolvimento líder do Analytics

   _Outras observações:_
   * Entregue por meio do Excel usando uma integração personalizada da API de relatórios do Adobe
   * Os usuários devem ter acesso à API dos serviços da Web do Analytics
   * Existem opções para a semiautomatização

1. Ganhe com o alargamento do mundo dos peritos em matéria de assuntos (PME):

   * Criar PME nas várias equipes da organização
   * Construa sua presença ajudando a socializar versões e vitórias
   * Usar horários regulares para ajudar a treinar os formadores e reduzir as tarefas ad hoc

Saiba mais sobre estratégia e liderança de pensamento no [Sucesso do cliente](https://experienceleague.corp.adobe.com/docs/customer-success/customer-success/overview.html) cubo.