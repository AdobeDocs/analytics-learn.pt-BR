---
title: 'Utilizar práticas recomendadas ao rastrear aplicativos de página única (SPA) no Adobe Analytics '
description: Neste documento, descreveremos várias práticas recomendadas às quais você deve seguir e estar ciente ao usar o Adobe Analytics para rastrear aplicativos de página única (SPA). Este documento se concentrará no uso do Experience Platform Launch, que é o método de implementação recomendado.
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
source-git-commit: 32424f3f2b05952fe4df9ea91dcbe51684cee905
workflow-type: ht
source-wordcount: '1669'
ht-degree: 100%

---

# Utilizar práticas recomendadas ao rastrear aplicativos de página única (SPA) no Adobe Analytics {#using-best-practices-when-tracking-spa-in-adobe-analytics}

Neste documento, descreveremos várias práticas recomendadas às quais você deve seguir e estar ciente ao usar o Adobe Analytics para rastrear aplicativos de página única (SPA). Este documento se concentrará no uso do Adobe [!DNL Experience Platform Launch], que é o método de implementação recomendado.

OBSERVAÇÕES INICIAIS:

* Os itens abaixo assumirão que você está usando o [!DNL Experience Platform Launch] para implementar no seu site. As considerações ainda existiriam se você não estivesse usando o [!DNL Experience Platform Launch], mas seria necessário adaptá-las ao seu método de implementação.
* Todos os SPAs são diferentes, portanto, talvez seja necessário ajustar alguns dos itens a seguir para atender melhor a sua necessidade, mas queremos compartilhar algumas práticas recomendadas com você; itens que precisam ser considerados ao implementar o Adobe Analytics em páginas SPA.

## Diagrama simples do trabalho com SPA no [!DNL Experience Platform Launch] {#simple-diagram-of-working-with-spas-in-launch}

![SPA para o Analytics no Launch](assets/spa_for_analyticsinlaunch.png)

**OBSERVAÇÃO:** Conforme dito, este é um diagrama simplificado de como as páginas de SPA são tratadas em uma implementação do Adobe Analytics usando o [!DNL Experience Platform Launch]. Nas seções a seguir desta página, discutiremos as etapas e problemas os quais você deve considerar ou agir com cuidado.

## Definir a camada de dados {#setting-the-data-layer}

Quando o novo conteúdo é carregado em uma página de SPA ou quando uma ação ocorre em uma página de SPA, uma das primeiras coisas que você deve fazer é atualizar a camada de dados. Isso precisa ocorrer ANTES que o evento personalizado seja disparado e acione as regras no [!DNL Experience Platform Launch], para que o [!DNL Experience Platform Launch] possa coletar os novos valores da camada de dados e enviá-los para o Adobe Analytics.

A seguir, há uma amostra de camada de dados cujos elementos podem ser modificados na alteração de exibição ou na ação em seu SPA. Por exemplo, em uma alteração de tela inteira/maior parte, seria comum alterar um elemento &quot;[!DNL pageName]&quot; para que o novo pudesse ser capturado no [!DNL Experience Platform Launch] e enviado para o Adobe Analytics.

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

## Configuração de eventos personalizados e acompanhamento no [!DNL Experience Platform Launch] {#setting-custom-events-and-listening-in-launch}

Quando o novo conteúdo for carregado na página ou quando uma ação ocorrer no site, você deverá informar o [!DNL Experience Platform Launch] para que possa executar uma regra e enviar dados para o [!DNL Analytics]. Há algumas maneiras diferentes de fazer isso: [!UICONTROL Regras] de [!UICONTROL chamada direta] ou Eventos personalizados.

* [!UICONTROL Regras] de [!UICONTROL chamada direta]: no [!DNL Experience Platform Launch], você pode configurar uma [!UICONTROL regra] de [!UICONTROL chamada direta] que é executada ao ser chamada diretamente da página. Se o carregamento da página ou a ação no site for muito simples, ou se for exclusivo e puder executar um conjunto específico de instruções todas as vezes (definir [!DNL eVar4] como X e acionar [!DNL event2] toda vez), você pode usar uma [!UICONTROL regra] de [!UICONTROL chamada direta]. Consulte a documentação do [!DNL Experience Platform Launch] sobre criação de [!UICONTROL regras] de [!UICONTROL chamada direta].
* Eventos personalizados: Para obter mais funcionalidades e a capacidade de anexar dinamicamente uma carga com valores diferentes, você deve definir eventos JavaScript personalizados e acompanhá-los no [!DNL Experience Platform Launch], onde é possível usar a carga para definir variáveis e enviar os dados para o Adobe Analytics. É mais provável que você precisará dessa funcionalidade e, portanto, essa opção é considerada a prática recomendada. No entanto, cada função no seu site pode determinar qual método será mais apropriado. Vamos avançar neste documento supondo que você precisará usar esse método de eventos personalizados.

**Exemplos:** [NESTE](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html?lang=pt-BR) documento de ajuda, há links para exemplos de sites SPA que implementaram o [!DNL Analytics] (e outras soluções da Experience Cloud), além de documentos que descrevem o que foi implementado. Nessas amostras de SPA, os seguintes eventos personalizados foram usados:

* [!DNL event-view-start]: Esse evento deve ser disparado no início da exibição/estado que está sendo carregado.
* [!DNL event-view-end]: Esse evento deve ser disparado mesmo quando uma alteração de exibição/estado ocorrer e todos os componentes de SPA na página tiverem sido carregados. Normalmente, esse é o evento que aciona uma chamada no Adobe Analytics.
* [!DNL event-action-trigger]: Esse evento deve ser disparado quando qualquer evento ocorrer na página, exceto o carregamento de exibição/estado. Esse pode ser um evento de clique ou uma alteração de conteúdo menor sem modificar a exibição.

Consulte as páginas/documentos mencionados acima para obter mais informações sobre como/quando eles são disparados. Você não precisa usar esses mesmos nomes de evento, mas a funcionalidade listada aqui é a prática recomendada. O vídeo a seguir mostrará um site de exemplo e de onde no [!DNL Experience Platform Launch] é possível acompanhar os eventos personalizados.

>[!VIDEO](https://video.tv.adobe.com/v/23024/?quality=12)

## Execução de s.t() ou s.tl() na [!UICONTROL Regra] do [!DNL Experience Platform Launch] {#running-s-t-or-s-tl-in-the-launch-rule}

Uma das coisas mais importantes para entender sobre o [!DNL Analytics] ao trabalhar com um SPA é a diferença entre `s.t()` e `s.tl()`. Você acionará um desses métodos no [!DNL Experience Platform Launch] para enviar dados para o [!DNL Analytics], mas você precisa saber quando enviar cada um deles.

* **s.t()** - O “t” significa “track” e é uma exibição de página normal. Mesmo que a URL não mude, a exibição muda o suficiente para você *considerá-la* uma nova “página”? Se sim, defina a variável s.[!DNL pageName] e use `s.t()` para enviar a chamada para o [!DNL Analytics]

* **s.tl()** - O “tl” significa “track link” e é usado normalmente para rastrear cliques ou pequenas alterações de conteúdo na página, em vez de uma alteração de tela inteira. Se a alteração na sua página for pequena, a ponto de você não considerá-la uma “página” totalmente nova, use `s.tl()` e não se preocupe em definir a variável s.pageName, pois ela será ignorada pelo [!DNL Analytics].

**DICA:** Algumas pessoas usam uma diretriz geral de que, se a tela for alterada em mais de 50%, ela deverá ser considerada uma exibição de página, portanto usa-se `s.t()`. Se a tela for alterada em menos de 50%, usa-se `s.tl()`. No entanto, depende totalmente de você e do que você considera uma nova “página” e como gostaria de rastrear o seu site no Adobe Analytics.

O vídeo a seguir mostra onde/como acionar o `s.t()` ou o `s.tl()` no Experience Platform Launch.

>[!VIDEO](https://video.tv.adobe.com/v/23048/?quality=12)

## Limpar variáveis {#clearing-variables}

Ao rastrear o seu site com o Adobe Analytics, é claro que você só deseja enviar os dados certos para o [!DNL Analytics] na hora certa. Em um ambiente de SPA, um valor rastreado em uma variável do [!DNL Analytics] pode persistir e ser reenviado para o [!DNL Analytics], possivelmente quando não o queremos mais. Por isso, há uma função na extensão [!DNL Analytics] [!DNL Launch] para limpar as variáveis, de modo que você possa começar do zero ao executar a próxima solicitação de imagem e enviar os dados para o [!DNL Analytics].

No diagrama acima, ela está listada no final do processo, limpando as variáveis *depois* que você envia a ocorrência. Na realidade, isso pode ser feito antes OU depois que a ocorrência é enviada, mas deve ser consistente nas suas regras do [!DNL Experience Platform Launch], para que você sempre limpe antes ou depois de definir as variáveis e enviá-las. Lembre-se, se você for limpar as variáveis *antes* de executar o `s.t()`, certifique-se de limpá-las primeiro, depois definir as novas variáveis e, em seguida, enviar os novos dados para o [!DNL Analytics].

**OBSERVAÇÃO:** Limpar as variáveis nem sempre é necessário ao executar o `s.tl()`, porque `s.tl()` exige o uso da variável [!DNL linkTrackVars] ao lado dele a cada vez para que o [!DNL Analytics] saiba quais variáveis serão definidas (adicionadas automaticamente em segundo plano no [!DNL Experience Platform Launch]). Isso significa que as variáveis errantes geralmente não aparecem ao usar `s.tl()`, mas isso é bastante recomendado ao usar `s.t()` em um ambiente SPA. Dito isto, gostaria de propor como prática recomendada o uso da função Limpar variáveis para ambos `s.t()` e `s.tl()` em um ambiente SPA, apenas para garantir uma coleta de dados de qualidade.

O vídeo a seguir mostra onde/como limpar as variáveis no [!DNL Launch].

>[!VIDEO](https://video.tv.adobe.com/v/23049/?quality=12)

## Considerações adicionais {#additional-considerations}

### Janelas de código personalizado no [!DNL Experience Platform Launch] {#custom-code-windows-in-launch}

Na extensão [!DNL Launch] [!DNL Analytics] há dois lugares onde você pode inserir o código personalizado: na seção de [!UICONTROL gerenciamento da biblioteca] e na seção extra “[!UICONTROL Configurar o rastreador usando um código personalizado]”.

![Janelas de código personalizado no Launch Analytics](assets/launch_analyticscustomcodewindows.png)

É importante saber que qualquer um desses locais só executará o código uma vez, quando o carregamento da página inicial ocorrer em sua página de SPA. Se precisar que o código seja executado em uma alteração de visualização ou em uma ação no seu site, insira uma ação adicional na **[!UICONTROL regra]** apropriada (Por exemplo, na [!UICONTROL regra] &quot;page load: event-view-end&quot;), para que o código seja executado toda vez que a [!UICONTROL regra] for executada. Ao criar essa ação na [!UICONTROL regra], defina a *Extensão = Principal* e o *Tipo de ação = Código personalizado*.

### “Híbrido” de SPA/Sites normais {#hybrid-spa-regular-sites}

Alguns sites são uma combinação de páginas “normais” e páginas de SPA. Nesta instância, será necessário usar uma estratégia que funcione para ambos os tipos de página. Ao configurar os seus eventos personalizados no site e acionar as regras no [!DNL Experience Platform Launch], tenha cuidado para que não haja ocorrências duplas da página entrando no [!DNL Analytics], por conta de alterações de hash etc. (se foi assim que você optou por acionar a regra do [!DNL Experience Platform Launch]). Nesse caso, será necessário suprimir uma das exibições de página para que ela não forneça dados corrompidos no Adobe Analytics.

Se você decidir dividir a funcionalidade em [!UICONTROL regras] separadas para ter mais controle sobre ela, certifique-se de lembrar/documentar que você fez isso, para que qualquer alteração em uma [!UICONTROL regra] possa também ser feita à outra [!UICONTROL regra], protegendo a integridade dos dados do [!DNL Analytics].

### Integração com o [!DNL Target] através do A4T {#integration-with-target-via-a4t}

Só uma rápida observação. Se estiver integrando com o [!DNL Target] usando o A4T, certifique-se de que a solicitação do [!DNL Target] e a solicitação do [!DNL Analytics] na mesma alteração de exibição têm a mesma SDID. Isso garantirá que os seus dados sejam sincronizados corretamente nas soluções.

Para ver as ocorrências, use um programa de depurador ou analisador de pacotes. Você também pode usar o Experience Cloud Debugger, uma extensão do Chrome que pode ser baixada [AQUI](https://chrome.google.com/webstore/detail/adobe-experience-cloud-de/ocdmogmohccmeicdhlhhgepeaijenapj). O [!DNL Target] deve ser acionado primeiro na página, para que você também possa verificar isso no depurador ou no console do JavaScript.

## Recursos adicionais {#additional-resources}

* [Discussão sobre SPA nos fóruns da Adobe](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-platform-launch/best-practices-for-single-page-apps/m-p/267940?profile.language=pt)
* [Sites de arquitetura de referência para mostrar como implementar SPA no Experience Platform Launch](https://helpx.adobe.com/experience-manager/kt/integration/using/launch-reference-architecture-SPA-tutorial-implement.html?lang=pt-BR)
