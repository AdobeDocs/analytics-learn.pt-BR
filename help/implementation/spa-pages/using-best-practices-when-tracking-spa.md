---
title: 'Uso das práticas recomendadas ao rastrear aplicativos de página única (SPA) no Adobe Analytics '
description: Neste documento, descreveremos várias práticas recomendadas que você deve seguir e estar ciente ao usar o Adobe Analytics para rastrear Aplicativos de página única (SPA). Este documento se concentrará no uso do Experience Platform Launch, que é o método de implementação recomendado.
feature: Implementation Basics
topics: spa
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
topic: SPA
role: "Developer, Data Engineer"
level: Intermediate
translation-type: tm+mt
source-git-commit: f3b3fa7d91b0cb21005b57768ca23ed6700fcc03
workflow-type: tm+mt
source-wordcount: '1676'
ht-degree: 0%

---


# Usar as práticas recomendadas ao rastrear aplicativos de página única (SPA) no Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

Neste documento, descreveremos várias práticas recomendadas que você deve seguir e estar ciente ao usar o Adobe Analytics para rastrear Aplicativos de página única (SPA). Este documento se concentrará no uso da Adobe [!DNL Experience Platform Launch], que é o método de implementação recomendado.

NOTAS INICIAIS:

* Os itens abaixo presumirão que você está usando [!DNL Experience Platform Launch] para implementar o em seu site. As considerações ainda existiriam se você não estivesse usando [!DNL Experience Platform Launch], mas precisaria adaptá-las ao seu método de implementação.
* Todos os SPAs são diferentes, portanto, talvez seja necessário ajustar alguns dos itens a seguir para melhor atender às suas necessidades, mas queremos compartilhar algumas práticas recomendadas com você; itens que você precisa considerar ao implementar o Adobe Analytics em páginas SPA.

## Diagrama simples de como trabalhar com SPAs em [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa para analytics no launch](assets/spa_for_analyticsinlaunch.png)

**OBSERVAÇÃO:** conforme declarado, este é um diagrama simplificado de como as páginas de SPA são tratadas em uma implementação do Adobe Analytics usando o  [!DNL Experience Platform Launch]. Nas seções a seguir desta página, discutiremos as etapas e quaisquer problemas que você deve considerar ou agir com cuidado.

## Configuração da camada de dados {#setting-the-data-layer}

Quando o novo conteúdo é carregado em uma página de SPA, ou quando uma ação ocorre em uma página de SPA, uma das primeiras coisas que você deve fazer é atualizar a camada de dados. Isso precisa ocorrer ANTES que o evento personalizado seja acionado e dispare regras em [!DNL Experience Platform Launch], para que [!DNL Experience Platform Launch] possa coletar os novos valores da camada de dados e enviá-los para o Adobe Analytics.

A seguir, há uma amostra de camada de dados, cujos elementos podem ser alterados na alteração da exibição ou na ação em seu SPA. Por exemplo, em uma alteração de tela cheia/maioria, seria comum alterar um elemento &quot;[!DNL pageName]&quot;, para que o novo pudesse ser capturado em [!DNL Experience Platform Launch] e enviado para o Adobe Analytics.

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

## Definir eventos personalizados e escuta em [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Quando o novo conteúdo é carregado na página ou quando uma ação ocorre no site, você deve informar [!DNL Experience Platform Launch] para que ele possa executar uma regra e enviar dados para [!DNL Analytics]. Há algumas maneiras diferentes de fazer isso: [!UICONTROL Chamada direta] [!UICONTROL regras] ou Eventos personalizados.

* [!UICONTROL Regras ] [!UICONTROL de chamada direta]: no  [!DNL Experience Platform Launch], você pode configurar uma regra de chamada    direta que é executada quando é chamada diretamente da página. Se o carregamento da página ou a ação no site for muito simples, ou se for exclusiva e puder executar um conjunto específico de instruções todas as vezes (defina [!DNL eVar4] como X e acione [!DNL event2] sempre), você poderá usar uma [!UICONTROL chamada direta] [!UICONTROL rule]. Consulte a documentação [!DNL Experience Platform Launch] sobre como criar [!UICONTROL chamada direta] [!UICONTROL regras].
* Eventos personalizados: Para obter mais funcionalidades e a capacidade de anexar dinamicamente uma carga com valores diferentes, você deve definir eventos JavaScript personalizados e ouvi-los em [!DNL Experience Platform Launch], onde é possível usar a carga para definir variáveis e enviar os dados para o Adobe Analytics. É mais provável que você precise dessa funcionalidade e, portanto, essa opção é considerada a prática recomendada. No entanto, cada função no site pode determinar qual método será mais apropriado. Vamos avançar neste documento, supondo que você precisará usar esse método de eventos personalizados.

**Exemplos:** neste documento de  [](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) ajuda, há links para exemplos de sites de SPA que foram implementados  [!DNL Analytics] (e outras soluções da Experience Cloud), bem como documentos que descrevem o que foi implementado. Nesses exemplos de SPA, os seguintes eventos personalizados foram usados:

* [!DNL event-view-start]: Esse evento deve ser acionado no início da exibição/estado que está sendo carregado.
* [!DNL event-view-end]: Esse evento deve ser acionado mesmo quando uma alteração de exibição/estado ocorrer e todos os componentes de SPA na página tiverem terminado de ser carregados. Normalmente, esse é o evento que aciona uma chamada para o Adobe Analytics.
* [!DNL event-action-trigger]: Esse evento deve ser acionado quando qualquer evento ocorrer na página, exceto o carregamento de visualização/estado. Pode ser um evento de clique ou uma alteração de conteúdo menor sem uma alteração de exibição.

Consulte as páginas/documentos referenciados acima para obter mais informações sobre como/quando são acionados. Você não precisa usar esses mesmos nomes de evento, mas a funcionalidade listada aqui é uma prática recomendada. O vídeo a seguir mostrará um site de exemplo e onde em [!DNL Experience Platform Launch] para acompanhar os eventos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Execução de s.t() ou s.tl() no [!DNL Experience Platform Launch] [!UICONTROL Regra] {#running-s-t-or-s-tl-in-the-launch-rule}

Uma das coisas mais importantes a se entender para [!DNL Analytics] ao trabalhar com um SPA é a diferença entre `s.t()` e `s.tl()`. Você acionará um desses métodos em [!DNL Experience Platform Launch] para enviar dados em [!DNL Analytics], mas precisa saber quando enviar cada um.

* **s.t()**  - O &quot;t&quot; representa &quot;track&quot; e é uma exibição de página normal. Mesmo que o URL não seja alterado, a exibição muda o suficiente para *considerar* como uma nova &quot;página&quot;? Em caso positivo, defina a variável s.[!DNL pageName] e use `s.t()` para enviar a chamada para [!DNL Analytics]

* **s.tl()**  - O &quot;tl&quot; significa &quot;rastrear link&quot; e é usado normalmente para rastrear cliques ou pequenas alterações de conteúdo na página, em vez de uma alteração de tela cheia. Se a alteração na sua página for pequena, para que você não a considere uma &quot;página&quot; totalmente nova, use `s.tl()` e não se preocupe em definir a variável s.pageName , pois [!DNL Analytics] a ignorará.

**DICA:** Algumas pessoas usam uma diretriz geral de que, se a tela mudar mais de 50%, ela deverá ser considerada uma exibição de página e usada  `s.t()`. Se for menor que 50% de alteração na tela, use `s.tl()`. No entanto, depende totalmente de você e do que você considera uma nova &quot;página&quot; e como gostaria de rastrear seu site no Adobe Analytics.

O vídeo a seguir mostra onde/como acionar `s.t()` ou `s.tl()` no Launch da Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Limpando variáveis {#clearing-variables}

Ao rastrear seu site com o Adobe Analytics, é claro que você só deseja enviar os dados corretos para [!DNL Analytics] na hora certa. Em um ambiente SPA, um valor rastreado em uma variável [!DNL Analytics] pode persistir e ser reenviado para [!DNL Analytics], possivelmente quando não queremos mais. Por isso, há uma função na extensão [!DNL Analytics] [!DNL Launch] para apagar as variáveis, de modo que você tenha uma nova tabulação ao executar a próxima solicitação de imagem e enviar dados para [!DNL Analytics].

No diagrama acima, listamos no final do processo, limpando as variáveis *depois de* que você enviou na ocorrência. Na realidade, isso pode ser feito antes OU depois que a ocorrência é enviada, mas deve ser consistente em suas regras [!DNL Experience Platform Launch], de modo que você sempre limpe antes ou depois de definir variáveis e enviá-las. Lembre-se de que, se você for apagar as variáveis *antes de* executar `s.t()`, certifique-se de apagar as variáveis primeiro, em seguida, definir as novas variáveis e, finalmente, enviar os novos dados para [!DNL Analytics].

**OBSERVAÇÃO:** a limpeza de variáveis nem sempre é necessária durante a execução  `s.tl()`, pois  `s.tl()` requer o uso da  [!DNL linkTrackVars] variável ao lado dela de cada vez para informar  [!DNL Analytics] quais variáveis serão definidas (adicionadas automaticamente nos bastidores em  [!DNL Experience Platform Launch]). Isso significa que as variáveis errantes geralmente não aparecem ao usar `s.tl()`, mas é muito recomendado usar `s.t()` em um ambiente SPA. Dito isso, gostaria de recomendar como prática recomendada o uso da função Limpar variáveis para `s.t()` e `s.tl()` em um ambiente SPA, apenas para garantir a coleta de dados de qualidade.

O vídeo a seguir mostra onde/como apagar as variáveis em [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Considerações adicionais {#additional-considerations}

### Janelas de código personalizado em [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

Na extensão [!DNL Launch] [!DNL Analytics], há dois lugares onde você pode inserir o código personalizado: A seção [!UICONTROL gerenciamento de biblioteca] e a seção extra &quot;[!UICONTROL Configurar rastreador usando código personalizado]&quot;.

![Iniciar janelas de código personalizado do Analytics](assets/launch_analyticscustomcodewindows.png)

É importante saber que qualquer um desses locais realmente só executará o código neles uma vez, quando o carregamento da página inicial ocorrer em sua página de SPA. Se você precisar que o código seja executado em uma alteração de exibição ou em uma ação no site, deverá adicionar uma Ação adicional ao **[!UICONTROL rule]** apropriado (por exemplo, no &quot;carregamento de página: event-view-end&quot; [!UICONTROL rule]), para que o código seja executado sempre que [!UICONTROL rule] for executado. Ao criar essa Ação no [!UICONTROL rule], defina *Extension = Core* e *Action Type = Custom Code*.

### SPA/Sites regulares &quot;Híbrido&quot; {#hybrid-spa-regular-sites}

Alguns sites são uma combinação de páginas &quot;regulares&quot; e páginas de SPA. Nesta instância, será necessário usar uma estratégia que funcione para ambos os tipos de página. Ao configurar seus eventos personalizados no site e acionar as regras em [!DNL Experience Platform Launch], tenha cuidado para não haver ocorrências duplas entrando em [!DNL Analytics] da página, com base em alterações de hash etc. (se foi assim que você optou por acionar a regra [!DNL Experience Platform Launch]). Nesse caso, será necessário suprimir uma das exibições de página para que ela não forneça dados defeituosos no Adobe Analytics.

Se você decidir dividir a funcionalidade em [!UICONTROL rules] separadas para ter mais controle sobre ela, lembre-se/documente que fez isso, para que todas as alterações em uma [!UICONTROL rule] possam ser feitas em outra [!UICONTROL rule] também, protegendo sua integridade de dados [!DNL Analytics].

### Integração com [!DNL Target] via A4T {#integration-with-target-via-a4t}

Só um rápido chamado aqui. Se estiver integrando com [!DNL Target] usando A4T, verifique se a solicitação [!DNL Target] e a solicitação [!DNL Analytics] na mesma alteração de exibição têm a mesma SDID. Isso garantirá que seus dados sejam sincronizados corretamente nas soluções.

Para ver as ocorrências, use um programa de depurador ou analisador de pacotes. Você também pode usar o Experience Cloud Debugger, uma extensão do Chrome que pode ser baixada [HERE](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] O deve ser acionado primeiro na página, para que você também possa verificar isso no console ou no depurador do JavaScript.

## Recursos adicionais {#additional-resources}

* [Discussão sobre o SPA nos fóruns da Adobe](https://forums.adobe.com/thread/2451022)
* [Sites de arquitetura de referência para mostrar como implementar o SPA no Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)