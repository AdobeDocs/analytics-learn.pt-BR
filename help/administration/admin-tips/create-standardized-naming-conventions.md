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
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 100%

---

# Criar convenções de nomenclatura padronizadas

**O QUE:** as convenções de nomenclatura padronizadas se aplicam ao próprio nome da variável quando habilitadas na interface do administrador do Adobe Analytics (AA) e aos valores transmitidos para a dimensão. (ou seja, usaríamos “page name (v1)” como o nome da variável e, para os valores de nome de página que serão transmitidos, uma estrutura/hierarquia uniforme e específica, como “sitename|homepage” ou “sitename|search|searchresults”).

**POR QUE:** as convenções de nomenclatura são uma ótima maneira de manter a uniformidade e uma interface fácil de entender para seus usuários. Se você criá-las desde o início e aplicá-las na plataforma e no código, será mais fácil dimensioná-las.

**COMO:** a interface e o documento de marcação devem corresponder ao “Nome” e à “Descrição”; isso evita que os usuários precisem buscar um documento do Excel e permite que eles entendam seus dados diretamente na interface. Também é recomendável manter tudo em letras minúsculas por questões de uniformidade.

É sempre melhor manter os nomes de página uniformes em toda a plataforma (ou nomes de tela para aplicativos). Por exemplo, você pode definir “property:section:sub section:sub sub section:unique page name” em uma variável/dimensão. Se todos esses campos forem separados em sua camada de dados, você poderá criar o nome da página diretamente no arquivo JS/Launch. Ter todos esses elementos definidos em suas próprias dimensões também pode ajudar você a detalhar propriedades ou áreas específicas do site/aplicativo com mais facilidade e entender melhor o tráfego e os fluxos.

Qualquer coisa que facilite a compreensão e descoberta de dados para os usuários, incluindo algo tão simples quanto as convenções de nomenclatura, aumentará o uso do Adobe Analytics e fornecerá melhores insights para os negócios.

## Autores(as)

Este documento foi coescrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, gerente de plataforma de análise digital do NortonLifeLock 
Especialista em Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sênior da Adobe
