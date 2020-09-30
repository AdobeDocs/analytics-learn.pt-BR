---
title: 'Usando práticas recomendadas ao rastrear aplicativos de página única (SPA) no Adobe Analytics '
description: Neste documento, descreveremos várias práticas recomendadas que você deve seguir e estar ciente ao usar o Adobe Analytics para rastrear aplicativos de página única (SPA). Este documento se concentrará em usar o Experience Platform Launch, que é o método de implementação recomendado.
feature: implementation basics
topics: spa
audience: implementer
activity: implement
doc-type: technical video
team: Technical Marketing
kt: 1389
translation-type: tm+mt
source-git-commit: 548ac75589383dfd4da4ae02412de91a0a3b28d6
workflow-type: tm+mt
source-wordcount: '1669'
ht-degree: 0%

---


# Usando práticas recomendadas ao rastrear aplicativos de página única (SPA) no Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

Neste documento, descreveremos várias práticas recomendadas que você deve seguir e estar ciente ao usar o Adobe Analytics para rastrear aplicativos de página única (SPA). Este documento se concentrará em usar o Adobe [!DNL Experience Platform Launch], que é o método de implementação recomendado.

NOTAS INICIAIS:

* Os itens abaixo assumirão que você está usando [!DNL Experience Platform Launch] para implementar em seu site. As considerações ainda existirão se você não estiver usando [!DNL Experience Platform Launch], mas precisaria adaptá-las ao seu método de implementação.
* Todos os SPAs são diferentes, portanto, talvez seja necessário ajustar alguns dos itens a seguir para melhor atender às suas necessidades, mas queríamos compartilhar algumas práticas recomendadas com você. itens que você precisa considerar ao implementar o Adobe Analytics em páginas SPA.

## Diagrama simples de como trabalhar com SPAs em [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![spa para análise na inicialização](assets/spa_for_analyticsinlaunch.png)

**NOTA:** Como mencionado, este é um diagrama simplificado de como as páginas SPA são tratadas em uma implementação do Adobe Analytics usando [!DNL Experience Platform Launch]. Nas seções a seguir desta página, discutiremos as etapas e quaisquer problemas que você deve considerar ou agir com cuidado.

## Configuração da camada de dados {#setting-the-data-layer}

Quando novo conteúdo é carregado em uma página SPA, ou quando uma ação ocorre em uma página SPA, uma das primeiras coisas que você deve fazer é atualizar a camada de dados. Isso precisa acontecer ANTES que o evento personalizado dispare e regras no [!DNL Experience Platform Launch], para que [!DNL Experience Platform Launch] possa coletar os novos valores da camada de dados e enviá-los para o Adobe Analytics.

A seguir, há uma amostra de camada de dados, cujos elementos podem ser alterados na alteração ou ação da visualização em seu SPA. Por exemplo, em uma alteração de tela cheia/maioria, seria comum alterar um elemento &quot;[!DNL pageName]&quot;, para que o novo pudesse ser capturado [!DNL Experience Platform Launch] e enviado para o Adobe Analytics.

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

## Configuração de Eventos personalizados e acompanhamento em [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Quando o novo conteúdo é carregado na página ou quando uma ação acontece no site, você deve informar [!DNL Experience Platform Launch] para que possa executar uma regra e enviar dados para [!DNL Analytics]. Há algumas maneiras diferentes de fazer isso: [!UICONTROL Regras] de chamada  direta ou Eventos personalizados.

* [!UICONTROL Regras de chamada] direta [!UICONTROL para]: no [!DNL Experience Platform Launch], você pode configurar uma [!UICONTROL regra] de chamada  direta que é executada quando é chamada diretamente da página. Se o carregamento de sua página ou a ação no site for muito simples, ou se for exclusiva e puder executar um conjunto específico de instruções toda vez (definido [!DNL eVar4] como X e acionado [!DNL event2] toda vez), você poderá usar uma [!UICONTROL regra] de chamada direta. Consulte [!DNL Experience Platform Launch] a documentação referente à criação de [!UICONTROL regras] de chamada direta.
* Eventos personalizados: Para obter mais funcionalidade e para a capacidade de anexar dinamicamente uma carga com valores diferentes, você deve definir eventos JavaScript personalizados e ouvi-los no, onde você pode usar a carga para definir variáveis e enviar os dados para o Adobe Analytics. [!DNL Experience Platform Launch] É mais provável que você precise dessa funcionalidade e, portanto, essa opção é considerada a prática recomendada. No entanto, cada função em seu site pode determinar qual método será mais apropriado. Vamos avançar neste documento, assumindo que você precisará usar esse método de eventos personalizados.

**Exemplos:** No documento de ajuda [THIS](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html) , há links para exemplos de sites SPA que foram implementados [!DNL Analytics] (e outras soluções de Experience Cloud), bem como documentos que descrevem o que foi implementado. Nesses exemplos de SPA, os seguintes eventos personalizados foram usados:

* [!DNL event-view-start]: Este evento deve ser acionado na start da visualização da visualização/estado que está sendo carregado.
* [!DNL event-view-end]: Esse evento deve ser acionado mesmo quando ocorrer uma alteração de visualização/estado e todos os componentes SPA da página tiverem terminado de ser carregados. Esse é o evento que normalmente aciona uma chamada para o Adobe Analytics.
* [!DNL event-action-trigger]: Esse evento deve ser acionado quando qualquer evento ocorrer na página, exceto carregamento de visualização/estado. Pode ser um evento click ou uma alteração de conteúdo menor sem uma alteração de visualização.

Consulte as páginas/documentos acima mencionados para obter mais informações sobre como/quando são disparados. Você não precisa usar esses mesmos nomes de eventos, mas a funcionalidade listada aqui é uma prática recomendada. O vídeo a seguir mostrará um site de amostra e onde [!DNL Experience Platform Launch] ouvir os eventos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Execução de s.t() ou s.tl() na [!DNL Experience Platform Launch] [!UICONTROL Regra] {#running-s-t-or-s-tl-in-the-launch-rule}

Uma das coisas mais importantes para entender ao [!DNL Analytics] trabalhar com um SPA é a diferença entre `s.t()` e `s.tl()`. Você acionará um desses métodos para enviar dados [!DNL Experience Platform Launch] para o [!DNL Analytics], mas precisa saber quando enviar cada um.

* **s.t()** - O &quot;t&quot; significa &quot;track&quot; e é uma visualização de página normal. Mesmo que o URL não mude, a visualização muda o suficiente para *considerá* -la uma nova &quot;página&quot;? Em caso afirmativo, defina a função s.[!DNL pageName] e usar `s.t()` para enviar a chamada para [!DNL Analytics]

* **s.tl()** - &quot;tl&quot; significa &quot;link de rastreamento&quot; e é normalmente usado para rastrear cliques ou pequenas alterações de conteúdo na página, em vez de uma alteração de tela cheia. Se a alteração na sua página for pequena, para que você não considere uma &quot;página&quot; totalmente nova, use `s.tl()` e não se preocupe em configurar a variável s.pageName, como [!DNL Analytics] a ignorará.

**DICA:** Algumas pessoas usam uma diretriz geral de que, se a tela mudar mais de 50%, ela deve ser considerada uma visualização de página e uso `s.t()`. Se houver menos de 50% de alteração na tela, use `s.tl()`. No entanto, depende totalmente de você e do que você considera uma nova &quot;página&quot; e como você gostaria de rastrear seu site no Adobe Analytics.

O vídeo a seguir mostra onde/como acionar `s.t()` ou `s.tl()` no Launch by Adobe.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Limpando variáveis {#clearing-variables}

Ao rastrear seu site com o Adobe Analytics, é claro que você só deseja enviar os dados certos para o site [!DNL Analytics] na hora certa. Em um ambiente SPA, um valor rastreado em uma [!DNL Analytics] variável pode persistir e ser reenviado para [!DNL Analytics], potencialmente, quando não queremos mais. Por esse motivo, há uma função na [!DNL Analytics] extensão para limpar as variáveis, de modo que você tenha uma nova página ao executar a próxima solicitação de imagem e enviar dados para [!DNL Launch] [!DNL Analytics].

No diagrama acima, nós o listamos no final do processo, apagando as variáveis *depois* que você envia a ocorrência. Na realidade, pode ser feito antes OU depois que a ocorrência é enviada, mas deve ser consistente em suas [!DNL Experience Platform Launch] regras, para que você sempre limpe as variáveis antes ou depois de configurá-las e enviá-las. Lembre-se, se você vai apagar as variáveis *antes* de executar `s.t()`, certifique-se de apagar as variáveis primeiro, depois definir as novas variáveis e, em seguida, enviar os novos dados para [!DNL Analytics].

**NOTA:** A limpeza de variáveis nem sempre é necessária durante a execução, pois `s.tl()`exige o uso da `s.tl()` variável ao lado dela sempre para informar [!DNL linkTrackVars] quais variáveis serão definidas (adicionadas automaticamente nos bastidores em [!DNL Analytics] [!DNL Experience Platform Launch]). Isso significa que as variáveis errantes geralmente não entram quando são usadas `s.tl()`, mas é muito recomendado quando são usadas `s.t()` em um ambiente SPA. Dito isto, gostaria de recomendar como prática recomendada a utilização da função Limpar variáveis tanto para `s.t()` como `s.tl()` em um ambiente SPA, apenas para garantir a qualidade da coleta de dados.

O vídeo a seguir mostra onde/como apagar as variáveis em [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Considerações adicionais {#additional-considerations}

### Janelas de código personalizado em [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

Na [!DNL Launch] [!DNL Analytics] extensão, há dois locais onde você pode inserir o código personalizado: A seção de gerenciamento [!UICONTROL da] biblioteca e a seção &quot;[!UICONTROL Configurar rastreador usando código]personalizado&quot;.

![Iniciar janelas de código personalizadas do Analytics](assets/launch_analyticscustomcodewindows.png)

É importante saber que qualquer um desses locais só executará o código neles uma vez, quando o carregamento da página inicial ocorrer na página do SPA. Se você precisar que o código seja executado em uma alteração de visualização ou em uma ação do site, adicione uma Ação adicional à **[!UICONTROL regra]** apropriada (por exemplo, em &quot;carregamento de página: &quot;evento-visualização-fim&quot; [!UICONTROL regra]), para que o código seja executado sempre que a [!UICONTROL regra] for executada. Ao criar essa ação na [!UICONTROL regra], defina *Extensão = Principal* e Tipo de *ação = Código* personalizado.

### SPA/Sites regulares &quot;híbridos&quot; {#hybrid-spa-regular-sites}

Alguns sites são uma combinação de páginas &quot;regulares&quot; e páginas SPA. Nessa instância, será necessário usar uma estratégia que funcione para ambos os tipos de página. Ao configurar seus eventos personalizados no site e acionar as regras no [!DNL Experience Platform Launch], tenha cuidado para que não haja ocorrências [!DNL Analytics] de duplos entrando na página, com base em alterações de hash etc. (se foi assim que você optou por acionar a [!DNL Experience Platform Launch] regra). Nesse caso, você precisará suprimir uma das visualizações de página para que não forneça dados defeituosos no Adobe Analytics.

Se você decidir dividir a funcionalidade em [!UICONTROL regras] separadas para ter mais controle sobre ela, lembre-se/documento de que fez isso, para que quaisquer alterações em uma [!UICONTROL regra] possam ser feitas também na outra [!UICONTROL regra] , protegendo a integridade dos [!DNL Analytics] dados.

### Integração com [!DNL Target] via A4T {#integration-with-target-via-a4t}

Só uma rápida chamada aqui. Se você estiver integrando com [!DNL Target] o uso de A4T, verifique se a [!DNL Target] solicitação e a [!DNL Analytics] solicitação na mesma alteração de visualização têm o mesmo SDID. Isso garantirá que seus dados sejam sincronizados corretamente nas soluções.

Para ver as ocorrências, use um depurador ou um programa sniffer de pacote. Você também pode usar o Experience Cloud Debugger, uma extensão do Chrome que pode ser baixada [AQUI](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). [!DNL Target] deve ser acionado primeiro na página, portanto, você também pode verificar isso no JavaScript Console ou no depurador.

## Recursos adicionais {#additional-resources}

* [Discussão sobre a SPA nos fóruns do Adobe](https://forums.adobe.com/thread/2451022)
* [Sites de arquitetura de referência para mostrar como implementar o SPA no Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html)