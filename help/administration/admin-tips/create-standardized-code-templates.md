---
title: Criar modelos de código padronizados
description: 'Para uma implementação de linha de base (ou seja, o que sua empresa considera os KPIs obrigatórios para todos os sites da Adobe Analytics), sua organização deve ter um único método de implementação, quando possível. '
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 2%

---


# Criar modelos de código padronizados

**O QUE:** Para uma implementação de &quot;linha de base&quot; (ou seja, o que sua empresa considera os KPIs obrigatórios para todos os sites da Adobe Analytics), sua organização deve ter um único método de implementação, quando possível. Por exemplo, use a mesma estrutura de camada de dados entre sites e a mesma regra/código personalizado do gerenciador de tags para capturar coisas como pesquisas internas ou informações de perfil do visitante.

**POR QUE:** Ter uma implementação de linha de base repetível e escalável torna a adição de novos elementos ou novos sites/aplicativos um esforço simplificado e de baixo esforço, além de manter sua implementação limpa e fácil de solucionar problemas. Usar um método uniforme também facilita que novos administradores/desenvolvedores fiquem online e entendam com o que estão trabalhando.

**COMO:** Adote um modelo de formato único para entregar aos desenvolvedores quando um novo site ou aprimoramento de marcação entrar online. Normalmente, um documento de palavras funciona bem, onde você pode destacar os seguintes itens:

* Variáveis que estão sendo implementadas, sua finalidade e quando devem ser definidas. Por exemplo:

| Variável AA | Descrição | Quando/Onde definir | Como definir |
|--- |--- |--- |--- |
| eVar8 | Palavras-chave de pesquisa interna | Na aterrissagem da página de resultados da pesquisa interna | camada de dados |
| event8 | Contagem de pesquisas internas | Na aterrissagem da página de resultados da pesquisa interna | Iniciar regra |

* Detalhe sobre como definir. É aqui que você pode especificar quaisquer objetos de camada de dados necessários e sua sintaxe, bem como quaisquer regras TMS que precisam ser configuradas e os detalhes da configuração da regra.
* Casos de teste para garantir que sejam abordados no controle de qualidade e em todas as variáveis que você espera ver em um caso de teste bem-sucedido. Descreva o que uma implementação bem-sucedida deve incluir quando o desenvolvedor testar esse aprimoramento.

Idealmente, esse documento só precisará ser aprimorado para o próximo site, onde você atualiza as noções básicas, como nome da propriedade, convenção de nomenclatura da página etc. Não é necessário reinventar a roda de cada vez, e você pode economizar mais tempo.

## Autores

Este documento foi co-escrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, gerente de plataforma de análise digital do NortonLifeLock Adobe Analytics Campeion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Consultor Sênior na Adobe
