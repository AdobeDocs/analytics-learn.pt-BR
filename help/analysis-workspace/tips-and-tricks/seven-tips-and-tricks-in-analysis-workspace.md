---
title: 7 dicas e truques que tornam a criação de projetos personalizados do Analytics mais rápida e fácil
description: O Analysis Workspace é uma ferramenta poderosa no Adobe Analytics que pode ajudá-lo a criar projetos de análise mais impactantes. Ele tem um vasto conjunto de recursos que permite que você faça qualquer tipo de análise de forma livre, mas uma experiência simples do usuário que torna esse poder e a escala acessíveis.
feature: Fundamentos do Workspace
topics: topics
activity: use
doc-type: feature video
team: Technical Marketing
kt: 3945
role: User, Developer, Data Engineer, Architect, Data Architect, Admin, Leader
level: Beginner
exl-id: af0e66cb-4e74-4ce0-9429-4a461fd54263
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: tm+mt
source-wordcount: '1056'
ht-degree: 0%

---

# 7 dicas e truques que tornam a criação de projetos personalizados do Analytics mais rápida e fácil

**Expanda o seu conjunto de habilidades do Analysis Workspace!**
O Analysis Workspace é uma ferramenta poderosa no Adobe Analytics que pode ajudá-lo a criar projetos de análise mais impactantes. Ele tem um vasto conjunto de recursos que permite que você faça qualquer tipo de análise de forma livre, mas uma experiência simples do usuário que torna esse poder e a escala acessíveis.

## Build: Fazendo drill-down para os pontos de dados corretos

### ***Dica 1: Solte qualquer  [!UICONTROL dimensão], intervalo de  [!UICONTROL datas],  [!UICONTROL segmento] ou   métrica em qualquer parte do seu projeto***

Basta arrastar e soltar um [!UICONTROL segment] ou qualquer outro componente para a área [!UICONTROL segment] soltar na parte superior de qualquer painel e você pode segmentar rapidamente esse painel até determinados pontos de dados. Por exemplo, você pode segmentar seu painel para mostrar somente ocorrências em que os pedidos existem, soltando as [!UICONTROL metric] &quot;orders&quot; na área suspensa [!UICONTROL segment]. Você ainda pode segmentar por dados que não existem em um componente (para ver ocorrências sem pedidos, por exemplo) soltando o item de dimensão &quot;não especificado&quot; ou &quot;nenhum&quot; na zona.

>[!VIDEO](https://video.tv.adobe.com/v/24036/?quality=12)

>[!TIP]
>
>**Experimente isto:** Há um mundo de eficiência esperando por você no menu do botão direito do mouse. Nesse menu, você pode acessar várias ferramentas e recursos diretamente no fluxo de trabalho do Analysis Workspace. Em caso de dúvida, clique com o botão direito do mouse para ver se a ferramenta ou a capacidade necessária está próxima

### ***Dica 2: Criar métricas simples sem sair do fluxo de trabalho***

Com as [!UICONTROL Métricas calculadas] rápidas, é possível criar novas [!UICONTROL métricas] diretamente no Analysis Workspace, em vez de navegar até o [!UICONTROL Construtor de métrica calculada]. Basta selecionar as colunas [!UICONTROL metric] que deseja calcular e, em seguida, no menu de contexto, selecione &quot;[!UICONTROL Criar métrica a partir da seleção]&quot;. Agora, você pode adicionar, subtrair, dividir, multiplicar e muito mais, sem deixar seu projeto e quebrar seu raciocínio.

>[!VIDEO](https://video.tv.adobe.com/v/23126/?quality=12)

>[!TIP]
>
>**Dica Útil:** até duas colunas   de métrica podem ser selecionadas ao usar as Métricas  [!UICONTROL Calculadas Rápido]. Use o Construtor de [!UICONTROL Métrica Calculada] para criar [!UICONTROL métricas] que incluam mais de duas [!UICONTROL métricas].

## Visualizar: Dando vida aos dados dentro dos projetos

### ***Dica 3: Copiar e inserir visualizações e painéis em qualquer lugar***

Copie facilmente visualizações e painéis de um local e adicione-os a outro, mesmo em um projeto diferente. Isso significa que você pode mover dados facilmente à medida que seu projeto cresce e compartilhar suas conclusões com novos usuários para que eles não precisem iniciar uma análise do zero. Basta clicar com o botão direito do mouse no painel ou na visualização que deseja copiar, selecionar &quot;[!UICONTROL Copiar visualização]&quot; e clicar com o botão direito do mouse em um painel em branco para inseri-lo.

>[!VIDEO](https://video.tv.adobe.com/v/23230/?quality=12)

>[!TIP]
>
>**Recurso altamente solicitado:** nossos clientes nos pediram para facilitar a cópia e a inserção de visualizações e painéis. Agora, eles gastam menos tempo recriando insights e mais tempo descobrindo novos.

### ***Dica 4: Alternar entre visualizações de granularidade de tempo em apenas um clique***

Altere facilmente a visualização de tempo ao trabalhar com visualizações de tendências. Em iterações anteriores do Analysis Workspace, alterar o tempo significava ocultar uma tabela de origem, arrastar uma nova [!UICONTROL dimensão] e ocultar novamente a tabela. Agora, é tão fácil quanto selecionar a granularidade de tempo que deseja demonstrar diretamente do menu suspenso &quot;[!UICONTROL Configurações de visualização]&quot; (engrenagem superior direita).

>[!VIDEO](https://video.tv.adobe.com/v/23548/?quality=12)

## Compartilhar: Facilitar o uso e o entendimento das descobertas por outros

### ***Dica 5: Criar um personalizado  [!DNL Virtual Report Suite] para unidades comerciais específicas***

O Adobe Analytics coleta grandes quantidades de dados. A preparação de componentes em [!DNL Virtual Report Suites] permite que os administradores criem um conjunto de dados para cada unidade comercial em uma organização. Isso significa que os analistas que trabalham no Analysis Workspace não precisam percorrer os dados para descobrir o que é mais importante para eles. Basta marcar a caixa &quot;[!UICONTROL Enable Customization of Virtual Report Suite Components]&quot; no construtor [!UICONTROL Virtual Report Suites] em [!UICONTROL &quot;Components]&quot; e, em seguida, selecionar os [!UICONTROL componentes] que correspondem às medidas de uma equipe específica.

>[!VIDEO](https://video.tv.adobe.com/v/23544/?quality=12)

>[!TIP]
>
>**Dica Útil:** Você também pode alterar o nome dos componentes em um Conjunto de Relatórios  [!UICONTROL Virtual ] para corresponder à nomenclatura de unidades comerciais específicas. Basta clicar no ícone de lápis ao lado do componente e digitar um novo nome.

### ***Dica 6: Link para painéis e visualizações em um projeto ou entre projetos***

Crie links que levam públicos-alvo em qualquer lugar no Analysis Workspace. Basta clicar com o botão direito do mouse no painel ao qual deseja vincular, selecionar &quot;[!UICONTROL Obter link do painel]&quot; e copiar. Em seguida, destaque o texto que deseja vincular, selecione o ícone de link no editor de texto de uma caixa de texto ou descrição e cole. Para vincular a um projeto inteiro, basta clicar na guia &quot;[!UICONTROL Compartilhar]&quot;, selecionar &quot;[!UICONTROL Obter link do projeto]&quot; e seguir as mesmas etapas descritas acima.

>[!VIDEO](https://video.tv.adobe.com/v/23724/?quality=12)

>[!TIP]
>
>**Dica Útil:** Há várias maneiras de os links melhorarem a experiência dos leitores. Você pode apontá-los para ilustrações que correspondem conclusões e recomendações em projetos. Ou permita que eles pulem de um índice diretamente para as seções em que estão interessados. Também é possível vincular aos projetos de outros usuários relacionados à sua análise

### ***Dica 7: Salvar projetos como modelos personalizados reutilizáveis***

Agora é possível transformar facilmente qualquer projeto em um modelo personalizado. Basta selecionar &quot;[!UICONTROL Salvar como modelo]&quot; no menu suspenso &quot;[!UICONTROL Projeto]&quot;, adicionar tags que facilitam a localização do modelo e clicar em &quot;[!UICONTROL Salvar projeto como modelo]&quot;. Agora, o modelo estará disponível para todos os usuários do Analysis Workspace na guia &quot;[!UICONTROL Modelos personalizados]&quot;. Isso permite que os analistas iniciem seus projetos com pontos de dados significativos, em vez de começar do quadrado.

>[!VIDEO](https://video.tv.adobe.com/v/23231/?quality=12)

>[!TIP]
>
>**Recurso altamente solicitado:** vários clientes nos pediram para tornar os projetos de salvamento possíveis como modelos personalizados. Agora, essa capacidade se tornou um dos favoritos deles.

[Clique aqui para encontrar mais dicas e truques no Experience League](https://experienceleague.adobe.com/?search=tips&amp;tag=Analysis+Workspace#recommended/solutions/analytics)

| Sobre o autor |  |
|------------|------------|
| ![Jen Lasser](assets/jlasser-headshot-s.jpg) | Jen Lasser é gerente da equipe de gerenciamento de produtos da Adobe Analytics. <br> Nessa função, ela se reúne com os clientes para entender suas necessidades de negócios,  <br>usando o que aprende a informar o roteiro de produtos do Adobe Analytics  <br>e a priorizar novos recursos do produto. Antes de sua posição atual, <br>Jen era uma consultora principal da equipe de Adobe Consulting, trabalhando como <br>especialista em assunto na visualização de dados, Analysis Workspace e [!DNL Report Builder]. <br><br>Com o benefício do seu insight real, preparamos as seguintes dicas e truques para  <br>ajudar a criar, visualizar e compartilhar seus projetos do Analysis Workspace com mais facilidade |
