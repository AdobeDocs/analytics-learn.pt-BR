---
title: Práticas recomendadas de implementação para aplicativos de página única (SPAs)
description: Conheça algumas práticas recomendadas para implementar o Adobe Analytics em aplicativos de página única (SPAs). Isso inclui o uso de tags da Experience Platform, que é o método de implementação recomendado.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: Developer, Data Engineer
level: Intermediate
exl-id: 8fe63dd1-9629-437f-ae07-fe1c5a05fa42
source-git-commit: 8fc641743bc9e07b838a22ca64ccc15344d52764
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 100%

---

# Práticas recomendadas de implementação para aplicativos de página única (SPAs) {#implementation-best-practices-for-single-page-appliations}

Aprenda algumas práticas recomendadas para implementação do [!DNL Adobe Analytics] em aplicativos de página única (SPAs). Isso inclui o uso do [!DNL Experience Platform Tags], que é o método de implementação recomendado.

OBSERVAÇÕES INICIAIS:

* O conteúdo abaixo faz referência ao uso do [!DNL Experience Platform Tags] para implementar o Adobe Analytics em seu site. Essas considerações se aplicam se o [!DNL Experience Platform Tags] não for usado, portanto, é necessário adaptá-las ao seu método de implementação.
* Há diferenças nos SPAs, portanto, você deve ajustar sua abordagem de acordo com suas necessidades.

## Diagrama simples do trabalho com SPA no [!DNL Experience Platform Tags] {#simple-diagram-of-working-with-spas-in-tags}

![SPA para o Analytics em tags](assets/spa_for_analyticsinlaunch.png)

**NOTA:** este é um diagrama simplificado de como as páginas do SPA são tratadas em uma implementação do Adobe Analytics usando o [!DNL Experience Platform Tags]. As seções a seguir identificam etapas e problemas a serem considerados.

## Definir a camada de dados {#set-the-data-layer}

Quando o novo conteúdo for carregado ou quando uma ação ocorrer em uma página do SPA, *atualize a camada de dados primeiro*. Isto tem de acontecer **antes** de um evento personalizado que aciona uma regra ser executado no [!DNL Experience Platform Tags]. Isso garante que os valores corretos da camada de dados sejam enviados às tags e, em seguida, para o Adobe Analytics.

Veja a seguir um exemplo de camada de dados. Qualquer um desses elementos pode ser alterado com base na exibição inicial ou na alteração subsequente da exibição, considerando uma ação realizada na página do SPA. Por exemplo, em uma alteração de exibição completa ou majoritária, é um requisito comum transmitir um valor “[!DNL pageName]” exclusivo para diferenciar as exibições nos relatórios do Adobe Analytics.

```JavaScript
<script>
    digitalData = {
        pageInstanceID: "Launch Demo Site",
        page:{
            pageInfo:{
                pageID: '2745374',
                pageName: 'acs demo - product listing page'
            },
            attributes:{
                project: "Experience Platform Launch Project"
            }
        },
        user : [ {
          "profile" : [ {
            "attributes" : {
              "gender" : "male",
              "age" : "35"
            }
          } ]
        }],
        libraries : {
          adobe : {
            launch : {
              state : 0, // 0 = not loaded , 1 = loaded
              domain : "assets.adobedtm.com"
            }
          }
        }

     };
    </script>
```

## Defina eventos personalizados e acompanhe esses eventos no [!DNL Experience Platform Tags] {#setting-custom-events-and-listening-in-tags}

Quando um novo conteúdo é carregado ou quando uma ação ocorre na página do SPA, as tags da Experience Platform precisam ser orientadas a executar uma regra que envia dados para o [!DNL Analytics]. Há algumas abordagens para isso: [!UICONTROL Regras de chamada direta] ou Eventos personalizados.

* [!UICONTROL Regras de chamada direta]: configure uma [!UICONTROL regra de chamada direta] que é executada ao ser chamada diretamente da página. Se o carregamento ou a ação da página for simples ou exclusivo, e puder executar um conjunto específico de instruções todas as vezes (por exemplo, definir [!DNL eVar4] para X e acionar [!DNL event2] todas as vezes), essa abordagem será adequada. Consulte a documentação do [!DNL Experience Platform Tags] para obter mais detalhes sobre como criar [!UICONTROL regras de chamada direta].
* Eventos personalizados: se você precisar anexar dinamicamente um conteúdo com valores exclusivos para eventos que ocorrem em páginas do SPA, use eventos JavaScript personalizados e acompanhe-os no [!DNL Experience Platform Tags]. Use o conteúdo para definir elementos de dados e variáveis do Analytics em tags. Esse método é considerado a prática recomendada, pois essa é uma necessidade predominante nos SPAs. Os exemplos abaixo usam o método de eventos personalizados.

**Exemplos:** [Neste](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) documento de ajuda, há links para exemplos de sites de SPA que implementam o [!DNL Analytics] e outras soluções da Experience Cloud. Nesses exemplos, os seguintes eventos personalizados foram usados:

* **[!DNL Event-view-start]**: executa no início da exibição/estado carregado.
* **[!DNL Event-view-end]**: executa quando ocorrer uma alteração de exibição/estado e todos os componentes do SPA na página terminarem de ser carregados. Normalmente, esse é o evento que envia dados para o Adobe Analytics.
* **[!DNL Event-action-trigger]**: executa quando qualquer evento ocorre na página, exceto o carregamento de visualização/estado. Exemplos disso são um evento de clique ou uma alteração de conteúdo menor que não altera a visualização.

Consulte as páginas e os documentos referenciados acima para obter mais informações sobre como e quando esses eventos são acionados. Não é necessário usar os mesmos nomes de evento na implementação. O caso de uso funcional do método usado é essencial para entender a prática recomendada para cada um. O vídeo a seguir demonstra um exemplo de página de SPA e um código de amostra no [!DNL Experience Platform Tags] que acompanha os eventos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12&learn=on)

## Execute s.t() ou s.tl() no [!DNL Experience Platform Tags] {#running-s-t-or-s-tl-in-the-launch-rule}

Um conceito importante para compreender o [!DNL Analytics] ao trabalhar com um SPA é a diferença entre `s.t()` e `s.tl()`. Seu código aciona um desses métodos no [!DNL Experience Platform Tags] para enviar dados ao [!DNL Analytics].

* **s.t()** - O “t” significa “track” e representa uma exibição de página Se a visualização for alterada o suficiente para você a *considerar* uma nova “página”, use esta chamada. Defina um valor exclusivo para a variável [!DNL s.pageName] e use `s.t()` para enviar os dados ao [!DNL Analytics].

* **s.tl()** - O “tl” significa “track link” e representa um clique em um link ou uma pequena alteração de conteúdo. Se a mudança de exibição for mínima, use `s.tl()` para transmitir um valor exclusivo sobre a interação para o [!DNL Analytics]. Essa variável transmitida não é [!DNL s.pageName], pois isso é ignorado no Analytics quando chamadas `s.tl()` são recebidas.

**DICA:** Como diretriz geral, se a tela for alterada em mais de 50%, use a chamada de exibição de página `s.t()`. Caso contrário, use `s.tl()`. No entanto, tome sua própria decisão ao considerar quais ações constituem uma nova “página” e como elas devem ser apresentadas nos relatórios do Adobe Analytics.

O vídeo a seguir mostra onde e como acionar `s.t()` ou `s.tl()` em tags.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12&learn=on)

## Limpar variáveis {#clear-variables}

Envie os dados corretos para o [!DNL Analytics] na hora certa. Em um ambiente de SPA, um valor armazenado em uma variável [!DNL Analytics] persiste e é reenviado para o [!DNL Analytics], possivelmente quando você não o desejar mais. Existe uma função na extensão [!DNL Analytics] [!DNL Tags] para limpar as variáveis, garantindo que a próxima chamada não envie dados erroneamente para o [!DNL Analytics].

O diagrama acima mostra as variáveis limpas *após* o envio dos dados. Na realidade, isso pode acontecer antes OU depois da chamada, no entanto, seja consistente em suas regras do [!DNL Experience Platform Tags] para realizar uma implementação mais limpa. Se você limpar variáveis *antes* de executar `s.t()`, defina as novas variáveis imediatamente após a chamada e, em seguida, envie os novos dados para o [!DNL Analytics].

**OBSERVAÇÃO:** Limpar variáveis nem sempre é necessário ao executar `s.tl()`. Esta chamada requer o uso da variável [!DNL linkTrackVars] para instruir o [!DNL Analytics] sobre quais variáveis devem ser definidas. Isso acontece automaticamente no [!DNL Experience Platform Tags] por meio de configuração. Isso impede que variáveis errantes sejam configuradas em contraste com o comportamento com chamadas `s.t()` em um ambiente de SPA. Para garantir uma implementação mais limpa e confiável, é provavelmente mais fácil usar a função de limpar variáveis para ambas as chamadas em um ambiente de SPA.

O vídeo a seguir mostra onde e como limpar as variáveis no [!DNL Tags].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12&learn=on)

## Considerações adicionais {#additional-considerations}

### Janelas de código personalizado no [!DNL Experience Platform Tags] {#custom-code-windows-in-tags}

Na extensão [!DNL Tags] [!DNL Analytics], há dois lugares onde o código personalizado pode ser inserido: as seções “[!UICONTROL Gerenciamento de biblioteca]” e “[!UICONTROL Configurar rastreador usando código personalizado]”.

![Janelas de código personalizado no Tags Analytics](assets/launch_analyticscustomcodewindows.png)

Qualquer um desses locais executa o código contido neles assim que a página inicial carrega sua página de SPA. Se o código deve ser executado em uma exibição ou alteração de ação, implemente-o na **[!UICONTROL regra]** apropriada (por exemplo, a regra “carregamento de página: final da visualização do evento”), para garantir que o código seja executado sempre que a [!UICONTROL regra] for executada. Ao criar essa ação na [!UICONTROL regra], defina a *Extensão = Principal* e o *Tipo de ação = Código personalizado*.

### SPA “híbrido” e sites tradicionais {#hybrid-spa-and-traditional-sites}

Alguns sites são compostos de uma combinação de páginas tradicionais e de SPA. Nesta instância, use uma estratégia que funcione para ambos os tipos de página. Ao configurar seus eventos personalizados no site e acionar as regras em no [!DNL Experience Platform Tags], certifique-se de que as ocorrências duplas não sejam enviadas para o [!DNL Analytics] com base em alterações de hash e assim por diante. Nesse caso, suprima uma das exibições de página para impedir que dados duplicados sejam enviados ao Adobe Analytics.

Se você decidir separar a funcionalidade em uma única [!UICONTROL regra] para ter mais controle, lembre-se de documentar que você fez isso. Se você alterar uma [!UICONTROL regra], efetue a mesma alteração na outra [!UICONTROL regra].

### Integração com o [!DNL Target] através do A4T {#integration-with-target-using-a4t}

Ao integrar com o [!DNL Target] usando o A4T, confirme se as solicitações do [!DNL Target] e do [!DNL Analytics] enviadas na mesma visualização ou ação passam o mesmo valor do parâmetro SDID. Isso garante que seus dados sejam sincronizados corretamente no back-end.

Para exibir essas ocorrências, use um depurador ou ferramenta de monitoramento de pacotes. A Adobe fornece o Experience Platform Debugger para essa finalidade. Essa é uma extensão do Chrome que pode ser [baixada aqui](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob?hl=pt-BR). O [!DNL Target] deve ser executado primeiro na página. Isso também pode ser verificado no depurador.

## Recursos adicionais {#additional-resources}

* [Discussão sobre SPA nos fóruns da Adobe](https://experienceleaguecommunities.adobe.com:443/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940)
* [Sites de arquitetura de referência para mostrar como implementar SPA no Experience Platform Launch](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)
