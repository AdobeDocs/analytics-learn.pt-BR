---
title: Criar convenções de nomenclatura padronizadas
description: As convenções de nomenclatura padronizadas se aplicam ao próprio nome da variável quando habilitadas na interface do administrador do AA e aos valores transmitidos para a dimensão.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
exl-id: 0fe3b981-0d9b-4f12-a6ca-63a4140f4baf
TQID: 'https://experienceleague.adobe.com/nnAluH2AvqNbWEPk3lbthk-xDl-tnqyW8uHg4Beurq0'
product_v2:
  - id: e55547f1-a1ff-40c6-8978-026e40ab7fa4
    internal-label: Analytics
feature_v2:
  - id: b069d60e-95f3-44d6-95a8-ddc862a4bc38
    internal-label: Reports
  - id: a421fb65-2c82-457a-921c-28c46b697a39
    internal-label: Analytics basics
subfeature_v2:
  - id: c24fe15a-643a-47bd-8278-5e027df49785
    internal-label: Implementation basics
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 3e00cf9416ba2c6886e5a7efb952cac8ce370930
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 78%
---
# Criar convenções de nomenclatura padronizadas

**O QUE:** as convenções de nomenclatura padronizadas se aplicam ao próprio nome da variável quando habilitadas na interface do administrador do Adobe Analytics (AA) e aos valores transmitidos para a dimensão. (ou seja, usaríamos “page name (v1)” como o nome da variável e, para os valores de nome de página que serão transmitidos, uma estrutura/hierarquia uniforme e específica, como “sitename|homepage” ou “sitename|search|searchresults”).

**POR QUE:** as convenções de nomenclatura são uma ótima maneira de manter a uniformidade e uma interface fácil de entender para seus usuários. Se você criá-las desde o início e aplicá-las na plataforma e no código, será mais fácil dimensioná-las.

**COMO:** a interface e o documento de marcação devem corresponder ao &quot;Nome&quot; e à &quot;Descrição&quot; - isso evita que os usuários precisem buscar um documento do Excel e permite que eles entendam seus dados diretamente na interface. Também é recomendável manter tudo em letras minúsculas por questões de uniformidade.

É sempre melhor manter os nomes de página consistentes em toda a plataforma (ou nomes de tela para aplicativos). Por exemplo, você pode definir `property:section:sub section:sub sub section:unique page name` em uma variável/dimensão. Se todos esses campos forem separados em sua camada de dados, você poderá criar o nome da página diretamente no arquivo JS/Launch. Ter todos esses elementos definidos em suas próprias dimensões também pode ajudar você a detalhar propriedades ou áreas específicas do site/aplicativo com mais facilidade e entender melhor o tráfego e os fluxos.

Qualquer coisa que facilite a compreensão e descoberta de dados para os usuários, incluindo algo tão simples quanto as convenções de nomenclatura, aumentará o uso do Adobe Analytics e fornecerá melhores insights para os negócios.

## Autores(as)

Este documento foi coescrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, gerente de plataforma de análise digital da NortonLifeLock
Especialista em Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sênior da Adobe
