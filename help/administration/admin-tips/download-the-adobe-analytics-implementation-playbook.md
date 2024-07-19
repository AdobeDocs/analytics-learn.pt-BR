---
title: Baixar o manual de implementação do Adobe Analytics
description: Um Documento de requisitos comerciais (geralmente chamado de BRD) é uma documentação muito importante na qual os principais interessados, usuários empresariais e de tecnologia desejam colaborar. É um local para documentar todos os KPIs desejados, requisitos de relatórios e qualquer ponto de dados que você deseje ver quando a implementação do AA estiver concluída.
feature: Implementation Basics
topic: Administration
role: Admin
level: Beginner
doc-type: article
thumbnail: 10530.jpg
kt: 10530
exl-id: aab53a12-3f11-49c9-aba4-dc926bcf776b
source-git-commit: df00d4fb8cc5093903ed4628dfe12f152294123a
workflow-type: tm+mt
source-wordcount: '1802'
ht-degree: 99%

---

# Baixar o manual de implementação do Adobe Analytics

Antes de começar, [baixe o manual](assets/aa-implementation-playbook.xlsx).

## Guia Requisitos comerciais

**O QUE:** um Documento de requisitos comerciais (geralmente chamado de BRD) é uma documentação muito importante na qual os principais interessados, usuários empresariais e de tecnologia desejam colaborar. É um local para documentar todos os KPIs, requisitos de relatórios e qualquer ponto de dados desejado que você deseja ver quando a implementação do Adobe Analytics (AA) for concluída.

**POR QUE:** isso serve como um ponto de partida para a documentação a seguir (SDR, especificação técnica etc.) e é uma fonte comum de verdade para um estado final acordado do AA. Este documento organiza o raciocínio entre as equipes da organização para formar uma direção orientadora e avançar com a criação ou o aprimoramento da implementação.

**COMO:** a documentação dos requisitos de negócios é comumente feita pelos usuários empresariais finais do AA, mas é importante obter feedback dos usuários de tecnologia, pois pode haver desafios técnicos a serem observados e alguns pontos de dados podem exigir mais esforço do que outros, o que faz parte da priorização.

Pergunte a si mesmo, “o que queremos rastrear em nosso site”, “que pontos de dados serão importantes para mim no uso de relatórios” e, mais importante, “como esses pontos de dados informarão as decisões”. É importante garantir que cada um dos requisitos comerciais esteja relacionado a um ponto de dados que possa ser usado para informar as decisões de negócios. Por exemplo, pode ser tentador rastrear todos os cliques no site; mas, no final das contas, que insights você está obtendo com esses relatórios?

Comece preenchendo a coluna C na captura de tela abaixo (Requisito comercial). Isso deve ser algo como “Quantas pesquisas internas são concluídas em nosso site” ou “Qual ponto de campanha interno é mais eficaz em termos de impressões”. Após preencher esse nível de detalhes, você pode voltar e preencher a coluna B (categoria) e agrupar os requisitos em categorias como “Pesquisa” ou “Promoção interna”, que devem corresponder perfeitamente às seções de especificação técnica.

Você também indicará se acha que usar um eVar, evento, prop ou combinação alcançará o que deseja rastrear.

Por fim, a coluna Status da implementação servirá como uma verificação de status quando você começar a adicionar itens ao seu site.

![Documento de requisitos comerciais](assets/brd-template.png)

## Guia Mapa de variáveis (marcação de doc/SDR)

**O QUE:** um documento de marcação (comumente conhecido como SDR) é uma parte essencial da documentação, valiosa para os usuários de tecnologia e negócios do AA. Ela lista cada variável em uso pelos conjuntos de relatórios, juntamente com todos os detalhes relevantes para as configurações da variável, como a variável é implementada e qual é sua finalidade nos relatórios. Como o seu documento de propriedades, isso deve ser um documento dinâmico e bem governado do Excel com uma pessoa responsável por mantê-lo atualizado, à medida que são introduzidos aprimoramentos de marcação ou alterações de implementação.

**POR QUE:** este documento terá muitos propósitos, mas os mais importantes são:

* Para qualquer pessoa nova na sua implementação (nova contratação, proprietário de negócios procurando entender melhor os relatórios disponíveis etc.), este documento fornece a melhor visualização de todas as variáveis implementadas e a finalidade delas para que os indivíduos possam realizar um autoatendimento em termos de aprendizado da configuração do AA.
* Para o proprietário/usuário técnico de um produto do AA, este documento servirá como um lembrete de como outras variáveis são configuradas e quais variáveis estão disponíveis para uso ao adicionar uma nova dimensão.

**COMO:** comece listando todas as variáveis prontas para uso da Adobe (página, produto, geo etc.), bem como eVars, props, eventos e variáveis de lista em um documento do Excel. Isso deve ter uma guia por site/conjunto de relatórios.
Para cada uma dessas dimensões, adiciono as seguintes colunas:
* **Nome:** forneça um nome simples e curto que possa ser entendido pela maioria das pessoas. Ele deve ser intuitivo o suficiente para que um novo usuário possa vê-lo e entender o que a variável deve capturar.
* **Descrição:** mais detalhes sobre o uso da variável e quais dados ela rastreia. Eu mantenho isso curto e simples e faço corresponder à descrição usada na interface. Idealmente, não quero que meus usuários precisem consultar o documento de marcação. Assim, quando uma nova dimensão é configurada no back-end do administrador, eu adiciono a mesma descrição lá. Dessa forma, o usuário pode clicar no ícone de informações diretamente no espaço de trabalho para entender o que é uma dimensão. Não é necessário abrir um documento do Excel.

![URL da página simplificado](assets/page-url-simplified.png)

* **Código:** o código do back-end que define o valor. Pode ser o campo da camada de dados na página, ou você pode informar que isso é feito com uma regra de inicialização, uma regra de processamento etc.
* **Relatórios de classificação:** informe quaisquer relatórios de classificação que estão sendo feitos com o Importador de classificação ou o Construtor de regras de classificação
* **Escopo da solução:** é útil listar todas as propriedades (pelo menos as que usam mais do que as variáveis padrão) em pequenas colunas e adicionar uma marca de seleção para cada dimensão que está sendo definida nessa propriedade. Isso permitirá filtrar facilmente por uma propriedade específica, bem como ver rapidamente onde uma determinada dimensão está sendo definida.
* **Configuração:** configurações da interface do administrador para cada variável (ou seja, para eVars — expiração, alocação, merchandising etc.)

Captura de tela do SDR de amostra:
![SDR de exemplo](assets/sample-sdr.png)

Também é recomendável usar este documento de marcação para rastrear qualquer variável livre e qualquer variável “inútil”. Quando uma dimensão não é mais útil, o desenvolvimento geralmente precisará de um tempo para excluí-la. Mesmo depois disso, o armazenamento em cache pode ocorrer, ou você pode perceber que a dimensão também estava sendo definida em outro lugar. Limpar dimensões não é uma tarefa fácil e pode exigir paciência. Veja algumas dicas para manter seu lixo escondido para que seus usuários não fiquem confusos enquanto o acompanham.

* Todas as dimensões/eventos que não estão sendo usados estão “livres” ou “sendo excluídos”
   * Se a dimensão tiver valores que não foram usados nos últimos 90 dias, ela “será excluída”
   * Se a dimensão estiver livre e limpa por pelo menos 90 dias, estará “livre”
   * Marque esses itens de maneira apropriada em “Nome”, no documento de marcação, para que você possa filtrá-los facilmente. Mantenha-os desmarcados no documento de marcação (filtro de dados do Excel) para que os usuários não os vejam
   * Marque-os com o nome do eVar na interface para que os usuários não os encontrem em uma pesquisa (ou seja, “(v6)”) e remova a descrição na interface
* Ao fazer isso, quando uma nova dimensão é necessária, você pode filtrar facilmente por “livre” na coluna “Nome” para encontrar uma dimensão limpa para usar
* Para as dimensões e eventos que estão “sendo excluídos”, é recomendado que você acompanhe esses itens usando o espaço de trabalho:
   * Crie um projeto visível para administradores somente com 3 tabelas: eVars, propriedades e eventos. Use “instâncias” para eVars específicas e, para propriedades, crie segmentos de HIT com “prop5 existe”, por exemplo.
   * Definir data como Últimos 90 dias
   * Use-as como linhas nas 3 tabelas, juntamente com as ocorrências
   * Assim que um item chegar a “0”, marque-o como “livre” no documento de marcação e remova-o do projeto do espaço de trabalho

Assim, seus dados estarão sempre limpos e você terá uma visão clara do seu lixo.

![Visão geral de variáveis e eventos](assets/variables-and-events-overview.png)

## Guia Propriedades

**O QUE:** um documento de propriedades deve listar todas as suas propriedades digitais: sites, aplicativos móveis, outras ferramentas (bate-papo, feedback etc.), quer essas propriedades estejam marcadas com o Adobe Analytics ou não. Isso deve servir como um documento centralizado e dinâmico para todos os usuários de negócios e de tecnologia.

**POR QUE:** isso fornecerá uma visão clara da jornada do usuário em todas as suas propriedades digitais e do que o Adobe Analytics cobre ou não, para que você possa priorizar a adição de marcações a qualquer propriedade que não as possua. Ao definir seu ecossistema digital dessa maneira, você pode identificar oportunidades potenciais na estratégia de marcação para obter uma visão completa da jornada do usuário. Por exemplo, você precisa de um conjunto de relatórios global para rastrear vários domínios/sites? É necessária uma transferência da ID de visitante entre domínios ou um aplicativo de experiência híbrida? Os filtros de URL internos precisam ser atualizados para o rastreamento entre domínios?

**COMO:** identifique um proprietário do documento para fornecer governança e uma única fonte de responsabilidade para o gerenciamento de atualizações.
Liste o seguinte na guia de propriedades:
* **Nome da propriedade:** pode ser um domínio, subdomínio, nome do aplicativo etc. Mesmo no mesmo domínio, se algumas partes dele forem gerenciadas separadamente (por uma equipe ou tecnologia diferentes), elas devem ser separadas.
* **Link (URL)** para a propriedade, quando disponível
* **Proprietário e contatos:** liste o proprietário ou os contatos principais da propriedade
* **Método de marcação:** muitos de nós têm diferentes métodos de código e implementações em vigor (Launch, arquivos JS, AEP etc.). Você pode detalhar isso ainda mais se necessário (como por versão de código ou um sistema de gerenciamento de tags), mas isso tem o objetivo de rastrear todos os seus diferentes métodos e versões de código, onde o código precisa ser atualizado e como ele precisa ser mantido. Se estiver usando o Adobe Launch, liste o nome da propriedade do Launch.

Lembre-se de incluir todas as propriedades digitais, mesmo que elas não estejam marcadas com o Adobe Analytics. Isso ajudará você a entender o cenário digital e como os usuários interagem com todas as suas propriedades.

É recomendável manter esse documento o mais simples possível e não sobrecarregá-lo de informações, para que seja fácil de interpretar por diferentes partes da organização. As equipes do Analytics geralmente compreendem o cenário digital melhor do que qualquer outra equipe, portanto, esse documento é usado com frequência por outras equipes e executivos para fornecer uma visão geral completa.

>[!TIP]
>
>Crie uma dimensão de nome de site/propriedade no Adobe Analytics. Ter uma dimensão dedicada (geralmente um eVar) no Adobe Analytics, que identifica o nome do site/nome do aplicativo, permitirá segmentar, solucionar problemas, criar conjuntos de relatórios virtuais etc. Os benefícios são infinitos, especialmente ao combinar vários sites em um conjunto de relatórios (global). O segredo é garantir que suas equipes de desenvolvimento sempre definam esse valor na dimensão de propriedades, incluindo todos os carregamentos de página (s.t calls/trackState) e todos os eventos personalizados (s.tl calls/trackAction). As regras de processamento podem ser uma ferramenta valiosa para ajudar você a definir esses valores de maneira adequada e consistente.

[Assista a este vídeo de Doug Moore](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/implementation/implementation-basics/creating-a-business-requirements-document.html?lang=pt-BR){target="_blank"} para obter mais informações sobre como preencher o manual de implementação.

## Autores(as)

Este documento foi coescrito por:

![Christel Guidon](assets/Christel-Headshot-150.png)

Christel Guidon, gerente de plataforma de análise digital do NortonLifeLock 
Especialista em Adobe Analytics

![Rachel Fenwick](assets/Rachel-Fenwick-150.png)

Rachel Fenwick, consultora sênior da Adobe
