---
title: Práticas recomendadas de implementação para aplicativos de página única (SPA)
description: Conheça algumas práticas recomendadas para implementar o Adobe Analytics em aplicativos de página única (SPA). Isso inclui o uso de Tags de Experience Platform, o método de implementação recomendado.
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
source-git-commit: d78c3351d2a98704396ceb8f84d123dd463befe5
workflow-type: tm+mt
source-wordcount: '1313'
ht-degree: 2%

---

# Práticas recomendadas de implementação para aplicativos de página única (SPA) {#implementation-best-practices-for-single-page-appliations}

Saiba mais sobre algumas práticas recomendadas para implementação [!DNL Adobe Analytics] em Aplicativos de página única (SPA). Isso inclui o uso de [!DNL Experience Platform Tags], o método de implementação recomendado.

OBSERVAÇÕES INICIAIS:

* O conteúdo abaixo faz referência ao uso de [!DNL Experience Platform Tags] para implementar o Adobe Analytics em seu site. Essas considerações se aplicam se [!DNL Experience Platform Tags] não é usada, portanto, é necessário adaptá-las ao seu método de implementação.
* Há diferenças no SPA, portanto, você deve ajustar sua abordagem de acordo com as necessidades.

## Diagrama simples do trabalho com SPA no [!DNL Experience Platform Tags] {#simple-diagram-of-working-with-spas-in-tags}

![SPA do analytics em tags](assets/spa_for_analyticsinlaunch.png)

**OBSERVAÇÃO:** Este é um diagrama simplificado de como as páginas de SPA são tratadas em uma implementação do Adobe Analytics usando [!DNL Experience Platform Tags]. As seções a seguir identificam etapas e problemas a serem considerados.

## Definir a camada de dados {#set-the-data-layer}

Quando o novo conteúdo é carregado ou quando uma ação ocorre em uma página de SPA, *atualizar a camada de dados primeiro*. Isto tem de acontecer **before** um evento personalizado que aciona uma regra é executado em [!DNL Experience Platform Tags]. Isso garante que os valores corretos da camada de dados sejam colocados em Tags e, em seguida, no Adobe Analytics.

Veja a seguir uma amostra de camada de dados. Qualquer um desses elementos pode ser alterado com base na exibição inicial ou na alteração subsequente da exibição, considerando uma ação realizada na página de SPA. Por exemplo, em uma alteração de exibição completa ou maioritária, é um requisito comum transmitir um &quot;[!DNL pageName]&quot; para diferenciar as exibições nos relatórios do Adobe Analytics.

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

## Defina eventos personalizados e acompanhe esses eventos em [!DNL Experience Platform Tags] {#setting-custom-events-and-listening-in-tags}

Quando novo conteúdo é carregado ou quando uma ação ocorre na página SPA, as Tags do Experience Platform precisam ser informadas para executar uma regra que envia dados para o [!DNL Analytics]. Há algumas abordagens para isso: [!UICONTROL Regras de chamada direta] ou Eventos personalizados.

* [!UICONTROL Regras de chamada direta]: Configure um [!UICONTROL regra de chamada direta] que é executado quando é chamado diretamente da página. Se o carregamento ou a ação da página for simples ou exclusiva, e puder executar um conjunto específico de instruções todas as vezes (por exemplo, defina [!DNL eVar4] para X e acionar [!DNL event2] toda vez), essa abordagem é adequada. Consulte [!DNL Experience Platform Tags] documentação para obter mais detalhes sobre como criar [!UICONTROL regras de chamada direta].
* Eventos personalizados: Se você precisar anexar dinamicamente uma carga com valores exclusivos para eventos que ocorrem em páginas SPA, use eventos JavaScript personalizados e ouça-os em [!DNL Experience Platform Tags]. Use a carga para definir elementos de dados e variáveis do Analytics em Tags. Esse método é considerado a prática recomendada, pois essa necessidade geralmente prevalece para a SPA. Nossos exemplos abaixo usam o método de eventos personalizados.

**Exemplos:** [Neste](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html) documento de ajuda, há links para exemplos SPA sites que implementam [!DNL Analytics] e outras soluções Experience Cloud. Nesses exemplos, os seguintes eventos personalizados são usados:

* **[!DNL Event-view-start]**: Execute no início da exibição/estado carregado.
* **[!DNL Event-view-end]**: Executar quando ocorrer uma alteração de exibição/estado e todos os componentes SPA na página terminarem de ser carregados. Normalmente, esse é o evento que envia dados para o Adobe Analytics.
* **[!DNL Event-action-trigger]**: Executar quando qualquer evento ocorrer na página, exceto o carregamento de visualização/estado. Exemplos disso incluem um evento de clique ou uma alteração de conteúdo menor sem uma alteração de exibição.

Consulte as páginas e os documentos referenciados acima para obter mais informações sobre como e quando esses eventos são acionados. Não é necessário usar os mesmos nomes de evento na implementação. O caso de uso funcional do método usado é essencial para entender como a prática recomendada para cada um. O vídeo a seguir demonstra um exemplo de página de SPA e código de amostra em [!DNL Experience Platform Tags] que escuta os eventos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Execute s.t() ou s.tl() no [!DNL Experience Platform Tags] {#running-s-t-or-s-tl-in-the-launch-rule}

Um conceito importante para compreender [!DNL Analytics] ao trabalhar com um SPA é a diferença entre `s.t()` e `s.tl()`. Seu código aciona um ou outro desses métodos em [!DNL Experience Platform Tags] para enviar dados para [!DNL Analytics].

* **s.t()** - O &quot;t&quot; significa &quot;track&quot;, e isso representa uma exibição de página. Se a exibição for alterada o suficiente para que você  *considere* é uma nova &quot;página&quot;, use esta chamada. Defina um valor exclusivo para [!DNL s.pageName] e use `s.t()` para enviar os dados para o [!DNL Analytics].

* **s.tl()** - O &quot;tl&quot; significa &quot;rastrear link&quot; e representa um clique em link ou uma pequena alteração de conteúdo. Se a mudança de exibição for mínima, use `s.tl()` para transmitir um valor exclusivo sobre a interação para o [!DNL Analytics]. Essa variável transmitida não é [!DNL s.pageName], pois isso é ignorado no Analytics quando `s.tl()` chamadas são recebidas.

**DICA:** Como diretriz geral, se a tela mudar em mais de 50%, use a `s.t()` chamada de exibição de página. Caso contrário, use `s.tl()`. No entanto, utilize seu julgamento ao considerar ações que constituem uma nova &quot;página&quot; e como elas devem ser apresentadas nos relatórios do Adobe Analytics.

O vídeo a seguir mostra onde e como acionar `s.t()` ou `s.tl()` em Tags.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Limpar variáveis {#clear-variables}

Envie os dados corretos para [!DNL Analytics] na hora certa. Em um ambiente SPA, um valor armazenado em um [!DNL Analytics] A variável persiste e é reenviada para [!DNL Analytics], possivelmente quando não desejar mais. Existe uma função no [!DNL Analytics] [!DNL Tags] para limpar as variáveis, para garantir que a próxima chamada não envie dados erroneamente para [!DNL Analytics].

O diagrama acima mostra as variáveis limpas *after* você envia dados. Na realidade, isso pode acontecer antes OU depois da chamada , no entanto, seja consistente em seu [!DNL Experience Platform Tags] regras para uma implementação mais limpa. Se você limpar variáveis *before* você executa `s.t()`, defina as novas variáveis imediatamente após a chamada e continue para enviar os novos dados para o [!DNL Analytics].

**OBSERVAÇÃO:** Limpar variáveis nem sempre é necessário ao executar `s.tl()`. Esta chamada requer o uso da variável [!DNL linkTrackVars] variável para instruir [!DNL Analytics] quais variáveis devem ser definidas. Isso acontece automaticamente [!DNL Experience Platform Tags] por meio da configuração. Impede que variáveis errantes sejam configuradas em contraste com o comportamento com `s.t()` em um ambiente SPA. Para garantir a implementação mais limpa e confiável, é provavelmente mais fácil usar a função clear variables para ambas as chamadas em um ambiente SPA.

O vídeo a seguir mostra onde e como limpar variáveis em [!DNL Tags].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Considerações adicionais {#additional-considerations}

### Janelas de código personalizado em [!DNL Experience Platform Tags] {#custom-code-windows-in-tags}

No [!DNL Tags] [!DNL Analytics] , há dois lugares onde o código personalizado pode ser inserido: O &quot;[!UICONTROL gerenciamento de bibliotecas]&quot; e &quot;[!UICONTROL Configurar rastreador usando código personalizado]&quot;.

![Tags Janelas de código personalizado do Analytics](assets/launch_analyticscustomcodewindows.png)

Qualquer um desses locais executa o código contido neles uma vez para a página inicial carregar sua página de SPA. Se o código deve ser executado em uma exibição ou alteração de ação, implemente-o no **[!UICONTROL regra]** (por exemplo, o &quot;carregamento de página: &quot;event-view-end&quot;), para garantir que o código seja executado sempre que a função [!UICONTROL regra] é executado. Ao criar a ação no [!UICONTROL regra], definir *Extensão = Principal* e *Tipo de ação = Código personalizado*.

### SPA &quot;Híbrido&quot; e locais tradicionais {#hybrid-spa-and-traditional-sites}

Alguns sites são compostos de uma combinação de páginas tradicionais e SPA. Nesta instância, use uma estratégia que funcione para ambos os tipos de página. Ao configurar seus eventos personalizados no site e acionar as regras em [!DNL Experience Platform Tags], certifique-se de que as ocorrências duplas não sejam enviadas para o [!DNL Analytics] com base em alterações de hash e assim por diante. Nesse caso, suprima uma das exibições de página para impedir que dados duplicados sejam passados para o Adobe Analytics.

Se você decidir separar a funcionalidade em um único [!UICONTROL regras] para ter mais controle, lembre-se de documentar que você fez isso. Se você alterar um [!UICONTROL regra], efetuar a mesma alteração à outra [!UICONTROL regra].

### Integração com [!DNL Target] uso do A4T {#integration-with-target-using-a4t}

Ao integrar com [!DNL Target] usando o A4T, confirme se a variável [!DNL Target] e [!DNL Analytics] as solicitações enviadas na mesma exibição ou ação passam o mesmo valor do parâmetro SDID. Isso garante que seus dados sejam sincronizados corretamente no back-end.

Para exibir essas ocorrências, use um depurador ou ferramenta de monitoramento de pacotes. O Adobe fornece um Experience Platform Debugger para essa finalidade. É uma extensão do Chrome que pode ser [baixado aqui](https://chrome.google.com/webstore/detail/adobe-experience-platform/bfnnokhpnncpkdmbokanobigaccjkpob?hl=en). [!DNL Target] O deve ser executado primeiro na página. Isso também pode ser verificado no depurador.

## Recursos adicionais {#additional-resources}

* [Discussão sobre SPA nos fóruns da Adobe](https://experienceleaguecommunities.adobe.com:443/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940)
* [Sites de arquitetura de referência para mostrar como implementar SPA no Experience Platform Launch](https://experienceleague.adobe.com/docs/experience-manager-learn/sites/spa-editor/spa-editor-framework-feature-video-use.html)
