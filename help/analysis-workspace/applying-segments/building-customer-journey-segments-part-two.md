---
title: Criação de segmentos de jornada do cliente - parte dois
description: Na segunda parte, saiba como criar segmentos de intenção de visita de compra e retenção para entender a jornada de compra dos clientes e personalizar o conteúdo. Usando sinais como cliques ou logins de "Reserve agora", identificamos a intenção de compra e retenção para uma análise eficiente e marketing direcionado.
feature: Segmentation
role: User
level: Experienced
last-substantial-update: 2023-07-21T00:00:00Z
jira: KT-13476
thumbnail: KT-13476.jpeg
exl-id: 2db73010-5cd0-4454-a4ba-fc1667a50cba
source-git-commit: d95136a21c08312a81baba7673cb7135270af4bd
workflow-type: tm+mt
source-wordcount: '1997'
ht-degree: 0%

---

# Criação de segmentos de jornada do cliente - parte dois

Na segunda parte, saiba como criar segmentos de intenção de visita de compra e retenção para entender a jornada de compra dos clientes e personalizar o conteúdo. Usando sinais como cliques ou logins de &quot;Reserve agora&quot;, identificamos a intenção de compra e retenção para uma análise eficiente e marketing direcionado.

## Criação de segmentos de intenção de visita de compra e retenção

Em nossa última publicação, descrevemos o processo de criação de segmentos de intenção de visita e criamos nosso primeiro segmento de intenção de visita, Maravilhas de uma única ocorrência. Hoje criaremos nossos segmentos de compra e retenção. Segmentamos cerca de 23% de nossas visitas e criamos espaços reservados para os segmentos restantes de Intenção de visita.

![Imagem 1](assets/Image-1.png)

Os segmentos de intenção de visita que estamos criando agora são a base para criar segmentos de jornada do cliente com base em visitantes. Criaremos esses segmentos de jornada com base em visitantes depois de criar nossos segmentos de intenção de visita.

Lembre-se de que a criação de segmentos de intenção de visita é um processo de eliminação. Portanto, não estamos construindo esses segmentos em ordem cronológica. Estamos criando nossos segmentos de intenção de visita na ordem de mais fácil de definir a mais difícil de definir:

1. Intenção: 0 - Maravilhas de uma ocorrência
1. Intenção: 3 - Compra
1. Intenção: 4 - Retenção
1. Propósito: 2 - Consideração
1. Propósito: 1 - Percepção

Em nossa última publicação, eu chamei o segmento &quot;Compra&quot; de &quot;Reserva&quot;, já que estou no ramo de viagens. Mas daqui para frente vamos chamá-lo de segmento de Compra para facilitar a aplicação a vários setores.

Quanto mais claro o sinal, mais fácil será criar o segmento. Em nossa última publicação, criamos nosso segmento Maravilhas de uma ocorrência, que era o mais fácil de definir, pois é apenas tráfego rejeitado. Você descobrirá que os segmentos de intenção de Compra e Retenção também são muito fáceis de definir, pois se baseiam em sinais muito claros.

## A Jornada do cliente é diferente da propensão para compra

Conforme analisamos a criação de nosso segmento de intenção de compra, é importante lembrar que identificar onde um cliente está em sua jornada é diferente de propensão. Você pode ter alguns modelos de propensão de compra que pontuam visitantes da Web para prever a probabilidade de eles fazerem uma compra. Esses modelos são muito úteis, mas são diferentes do segmento de Intenção de compra que criaremos hoje.

Embora um modelo de propensão busque prever se um visitante comprará, nossos segmentos de Intenção de visita buscam entender onde uma pessoa está em sua jornada de compra. Usar segmentos de intenção para entender o estado de espírito de um cliente nos ajuda a personalizar o conteúdo e adaptar o marketing para direcionar o tráfego certo e alimentar nosso pipeline de vendas. Portanto, nosso segmento Intenção de compra busca sinais comportamentais explícitos que indicam que um visitante está procurando fazer uma compra.

## Criação do segmento de intenção de visita de compra

O segmento Intenção de visita de compra é fácil de definir. No meu caso, qualquer um que clicar no botão &quot;Reservar Agora&quot; está indicando algum tipo de intenção de reservar um cruzeiro. É semelhante a clicar em &quot;Check-out&quot; para um varejista online ou em um link &quot;Assinar&quot; em um contexto de mídia.

Você precisará ter algum discernimento ao decidir qual sinal usar para inferir a intenção de compra. Queremos que o segmento Intenção de compra contenha todas as compras, mas a taxa de conversão não deve ser de 100%. Portanto, não queremos usar a página Confirmação de compra ou Agradecimento para este segmento.

Da mesma forma, a página Revisar sua compra (ou o que quer que seja imediatamente antes da confirmação da compra) provavelmente fica muito longe do funil para ser útil para análise e direcionamento.

À medida que você sobe o funil, pode ficar menos claro se o sinal é útil ou não para indicar que um cliente pretende fazer uma compra. No meu caso, &quot;Reservar agora&quot; é semelhante a um link &quot;Check-out&quot; de varejo e esse é o sinal que usei. Mas em um contexto de varejo, o Check-out pode ainda estar muito longe do funil e a opção Exibir carrinho ou até mesmo Adicionar ao carrinho pode ser melhor.

Podemos pensar nisso como uma mercearia. Se alguém pegar um produto da prateleira isso não significa que pretende comprá-lo. Mesmo que o coloquem no carrinho, eles podem imediatamente colocá-lo de volta na prateleira. Mas se eles colocarem o produto em seus carrinhos e começarem a andar por aí com ele, há uma boa chance de que eles queiram comprá-lo. E se eles entrarem na fila de check-out com aquele produto é uma boa aposta que eles comprarão.

Sugiro o uso de páginas visitadas ou outros sinais explícitos de intenção de compra e evitar outros sinais menos diretos para identificar a intenção de compra. Por exemplo, eu não usaria o número de sessões ou o número de páginas em uma sessão ou similar. Esses sinais indiretos indicam Consideração, não Intenção de compra. Lembre-se, a finalidade desse segmento é inferir a intenção do visitante para a visita, não sua propensão.

### Utilização do Analytics Workspace para identificar sinais de intenção de compra

O relatório de Fallout é muito útil para identificar um bom sinal que indica a intenção de compra. Procure um local que indique logicamente a intenção. Você pode confirmar que a etapa indica intenção ao visualizar um fallout notável indo para essa etapa, geralmente seguido por um fallout menor para a etapa imediatamente após.

![Imagem 2](assets/Image-2.png)

Também é útil observar as taxas de conversão associadas às várias páginas do site. Isso é especialmente útil para identificar páginas que indicam a intenção de compra, mas que podem não ser necessárias para fazer uma compra (como páginas financeiras, páginas de configuração de compra etc.).

![Imagem 3](assets/Image-3.png)

Por fim, é importante incluir todas as páginas entre o início da compra e a confirmação da compra em seu segmento. Os visitantes podem dar voltas e entrar novamente no fluxo de compra em pontos diferentes.

### Excluir outros segmentos

Lembre-se da nossa primeira publicação que os nossos segmentos de Intenção de visita precisam ser mutuamente exclusivos e completamente exaustivos. Este é um refrão que vocês ouvirão muito nesta série.

Certifique-se de que o segmento Intenção de compra exclui o segmento Uma e Concluída. Você só deve precisar excluir o segmento Um e Concluído porque os sinais que usamos para a Intenção de compra são muito específicos.

Observe que excluir o segmento Um e Concluído pode excluir alguém que entra novamente em seu site em uma página de check-out. Isso está certo. A própria definição de Um e Concluído é uma exibição de página, o que significa que mesmo se um visitante entrar ou for atualizado em uma página de check-out, sua visita não avançou, portanto, não há expressão de intenção de compra.

### O segmento de intenção de compra no Construtor de segmentos

A definição de segmento para Intenção de compra é muito simples.

Usando o contêiner de visita, inclua as páginas ou outras ações que indicam explicitamente a intenção de fazer uma compra. Se você tiver várias condições de inclusão, coloque-as em um container unido pela condição &quot;And&quot;.

Adicione um container Excluir ao segmento unido pela condição &quot;And&quot;. Adicione sua definição de segmento Maravilhas de uma ocorrência (Exibições de página é igual a 1) ao contêiner Excluir.

![Imagem 4](assets/Image-4.png)

Como prática recomendada, certifique-se de rotular os containers. Você ficará feliz em fazer isso, especialmente quando nossas definições de segmento se tornarem mais complexas.

Agora que criamos o segmento de intenção de compra, podemos usar o Workspace de qualidade de dados de intenção de visita para ver que nosso segmento de intenção de compra é mutuamente exclusivo com nosso segmento Um e Concluído.

![Imagem 5](assets/Image-5.png)

## Criação do segmento de intenção de visita de retenção

No negócio de cruzeiros, muitos hóspedes vêm ao nosso site para gerenciar uma reserva, mas não necessariamente para fazer uma compra. Eles podem vir ao site para inserir informações de viagem, revisar seu itinerário, fazer reservas de jantar ou várias outras coisas, sem fazer compras para um cruzeiro. Os nossos hóspedes também podem adquirir excursões em terra ou outras melhorias à sua experiência. Consideramos esses aprimoramentos como parte da retenção, portanto, os mantemos separados do nosso segmento de reserva (que chamamos de &quot;Compra&quot; nesta série de blogs).

Os clientes de varejo podem fazer devoluções ou gerenciar seu programa de fidelidade. Os assinantes de mídia ou tecnologia podem estar usando o produto. Se seu convidado está em seu site para gerenciar o relacionamento dele com você, essa é uma Visita de retenção e devemos observar esses sinais. E se você fornecer um produto on-line, como Mídia, Tecnologia, Bancos on-line ou outros, provavelmente há muitos outros tipos de segmentos de intenção de visitas que não discutiremos nesta série.

Assim como no segmento Intenção de compra, estamos procurando por indicações muito explícitas de intenção. Para mim, temos uma seção inteira do site dedicada a gerenciar um cruzeiro, então é fácil identificar essas páginas. Isso pode ser mais complexo para outras empresas. Procure sinais como logons, gerenciamento de conta, visitas a páginas de suporte e semelhantes.

Devo observar que &quot;Retenção&quot; é um nome meio estranho para essa intenção de visita, já que o visitante não está em nosso site, &quot;para que eu possa ser mantido como cliente&quot;. A retenção é a nossa intenção para essa visita. Lembre-se de ter empatia com nossos clientes e manter um foco de cliente em primeiro lugar!

### Utilização do Analytics Workspace para identificar sinais de intenção de retenção

Novamente, o Analytics Workspace nos ajuda a identificar a intenção de retenção. É possível usar as dimensões de páginas, seção do site ou segmento personalizado para categorizar suas páginas. Procure páginas com baixas taxas de conversão de compra. Em nosso caso, descobrimos que as páginas de Check-in Online e Excursão pela Costa (Shorex) têm taxas de conversão relativamente mais baixas do que outras páginas que estão mais logicamente associadas a compras e compras.

![Imagem 6](assets/Image-6.png)

Também é uma boa ideia procurar páginas de alto tráfego no Workspace. Digitalize a lista de páginas de alto tráfego e decida se elas indicam uma intenção de retenção.

## Excluir outros segmentos

Novamente, nossos segmentos de Intenção de visita precisam ser mutuamente exclusivos e completamente exaustivos. Se você ainda não estiver cansado de ler isso, você vai ficar! Para nosso segmento de intenção de retenção, é extremamente importante excluir os comportamentos de intenção de compra.

Para a maioria de nós, a intenção de compra e a intenção de retenção não são comportamentos mutuamente exclusivos. Temos convidados que vêm ao site para gerenciar seu próximo cruzeiro, mas também para reservar sua próxima viagem (obrigado!). Se você é um restaurante, um visitante pode verificar seus pontos de fidelidade e, em seguida, fazer um pedido on-line.

Mesmo que o comportamento não seja mutuamente exclusivo, nossos segmentos devem ser para análise de Jornada do cliente. Podemos criar outros segmentos muito interessantes para analisar a sobreposição entre os comportamentos de compra e fidelidade. Mas para nossos propósitos atuais, precisamos que esses segmentos sejam mutuamente exclusivos.

Como a geração de demanda é um dos principais objetivos do marketing, nosso segmento de intenção de retenção excluirá a intenção de compra. Em outras palavras, se alguém vier ao nosso site para gerenciar um cruzeiro, mas também indicar a intenção de reservar um novo cruzeiro, essa visita será direcionada ao segmento Intenção de compra.

### O segmento de intenção de retenção no Construtor de segmentos

Nossas definições de segmento estão se tornando um pouco mais claras. Incluir visitas no seu segmento. Adicione os sinais de intenção de retenção. Para mim, isso foi simples. Se o nome da página começa com &quot;bge:&quot; (nossas páginas de convidados reservadas), você está no segmento. Adicionei que as exibições de página são maiores que uma para medição extra (mas ainda excluiremos uma das maravilhas de ocorrência abaixo).

Em seguida, adicione os contêineres de exclusão para suas Maravilhas de uma ocorrência e Visitas de intenção de compra. Verifique se os contêineres estão unidos com a condição &quot;And&quot;.

![Imagem 7](assets/Image-7.png)

Mais uma vez, examine sua Workspace de qualidade de dados de intenção de visita para garantir que seus segmentos sejam mutuamente exclusivos. Nossos segmentos de Intenção de visita estão tomando forma muito bem!

![Imagem 8](assets/Image-8.png)

Neste ponto, configuramos três dos nossos cinco segmentos de Intenção de visita. Vemos que esses segmentos são mutuamente exclusivos. Na próxima publicação, criaremos os segmentos finais de Intenção de visita, Consideração e Percepção, e nossos segmentos serão completamente exaustivos. Depois que nossos segmentos de Intenção de visita forem configurados, nós os reuniremos em segmentos baseados em visitantes que você achará muito úteis para análise e personalização.

## Autora

Este documento foi escrito por:

![Aaron Fossum](assets/aaron-headshot.png)

**Aaron Fossum**, Director, Análise Digital

Especialista no Adobe Analytics
