---
title: Criar convenções de nomenclatura padronizadas
description: As convenções de nomenclatura padronizadas se aplicam ao próprio nome da variável quando habilitado na interface do usuário do administrador AA e aos valores passados para a dimensão.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10531.jpg
kt: 10531
source-git-commit: 160df6c23acb67f1b07f2fcd25f1eca96eb6dee7
workflow-type: tm+mt
source-wordcount: '339'
ht-degree: 0%

---


# Criar convenções de nomenclatura padronizadas

**O QUE:** As convenções de nomenclatura padronizadas se aplicam ao próprio nome da variável quando ativadas na interface do usuário do administrador do Adobe Analytics (AA) e aos valores passados para a dimensão. (ou seja, os nomes de página seriam &quot;nome de página (v1)&quot; como um nome de variável e os valores de nome de página passados devem ser uniformes e seguir uma estrutura/hierarquia específica como &quot;sitename|homepage&quot; ou &quot;sitename|search|searchresults&quot;).

**POR QUE:** As convenções de nomenclatura são uma ótima maneira de manter tudo uniforme e manter a interface fácil de entender para seus usuários. Se você criá-los desde o início e aplicá-los na plataforma e no código, será mais fácil dimensioná-los.

**COMO:** A interface e o documento de marcação devem corresponder ao &quot;Nome&quot; e à &quot;Descrição&quot;; isso evitará que os usuários precisem buscar um documento do Excel e permitirá que entendam seus dados diretamente na interface. Também é recomendável manter tudo em minúsculas por questões de consistência.

É sempre melhor manter os nomes de página consistentes em toda a plataforma também (ou nomes de tela para aplicativos). Por exemplo, você pode definir &quot;propriedade:section:subseção:subseção:nome da página único&quot; em uma variável/dimensão. Se todos esses forem campos separados na camada de dados, você pode até mesmo criar o nome da página diretamente no arquivo JS/Launch. Ter todos esses elementos definidos em suas próprias dimensões também pode ajudar você a detalhar propriedades ou áreas específicas do site/aplicativo com mais facilidade e entender melhor o tráfego e os fluxos.

Qualquer coisa que torne mais fácil para os usuários encontrar e entender os dados, incluindo algo tão simples quanto as convenções de nomenclatura, aumentará o uso do Adobe Analytics e fornecerá melhores insights para os negócios.

## Autores

Este documento foi co-escrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, gerente de plataforma de análise digital do NortonLifeLock Adobe Analytics Campeion

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, Consultor Sênior na Adobe
