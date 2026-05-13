---
title: Criar modelos de código padronizados
description: Para uma implementação de linha de base (ou seja, o que sua empresa considera ser os KPIs obrigatórios para todos os sites do Adobe Analytics), sua organização deve ter um único método de implementação, quando possível.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10532.jpg
kt: 10532
exl-id: be00c8c0-a4bc-4380-98da-d1e2a3d31ec5
TQID: https://experienceleague.adobe.com/rmLhZbO6hYtpj1P0q0ZVwXglHVBC-KaHIkxyAF-7i-U
product_v2: id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
feature_v2: id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 677e5a22dab92be7ff021c8410525b9091975aef
workflow-type: tm+mt
source-wordcount: 366
ht-degree: 87%

---

# Criar modelos de código padronizados

**O QUE:** para uma implementação de “linha de base” (ou seja, o que sua empresa considera ser os KPIs obrigatórios para todos os sites do Adobe Analytics), sua organização deve ter um único método de implementação, quando possível. Por exemplo, use a mesma estrutura de camada de dados entre os sites e a mesma regra/código personalizado do gerenciador de tags para capturar dados, como pesquisas internas ou informações de perfil do visitante.

**POR QUE:** ter uma implementação de linha de base repetível e escalável torna a adição de novos elementos ou novos sites/aplicativos uma tarefa simplificada e de baixo esforço, além de manter sua implementação limpa e fácil de solucionar problemas. Usar um método uniforme também facilita que novos administradores/desenvolvedores fiquem online e entendam com o que estão trabalhando.

**COMO:** adote um modelo de formato único para entregar aos desenvolvedores quando um novo site ou aprimoramento de marcação ficar online. Normalmente, um documento do Word funciona bem, em que você pode destacar os seguintes itens:

* Variáveis que estão sendo implementadas, a finalidade dessas variáveis e quando devem ser definidas. Por exemplo:

| Variável do AA | Descrição | Quando/Onde definir | Como definir |
|--- |--- |--- |--- |
| eVar8 | Palavras-chave de pesquisa interna | Na aterrissagem da página de resultados da pesquisa interna | camada de dados |
| event8 | Contagem de pesquisas internas | Na aterrissagem da página de resultados da pesquisa interna | Regra de inicialização |

* Detalhe sobre como definir. É aqui que você pode especificar quaisquer objetos de camada de dados necessários e sua sintaxe, bem como quaisquer regras TMS que precisam ser configuradas e os detalhes da configuração da regra.
* Casos de teste para garantir que sejam abordados no controle de qualidade e em todas as variáveis que você espera ver em um caso de teste bem-sucedido. Descreva o que uma implementação bem-sucedida deve incluir quando o desenvolvedor testar esse aprimoramento.

Idealmente, esse documento só precisará ser aprimorado para o próximo site, em que você atualiza as noções básicas como nome da propriedade, convenção de nomenclatura da página etc. Não é necessário reinventar a roda a cada vez, e você pode economizar mais tempo.

## Autores(as)

Este documento foi coescrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, gerente de plataforma de análise digital da NortonLifeLock
Especialista em Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sênior da Adobe
