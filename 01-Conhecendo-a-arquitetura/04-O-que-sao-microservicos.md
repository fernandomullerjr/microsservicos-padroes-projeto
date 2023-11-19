


# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# push

git status
git add .
git commit -m "Aula 04 O que são microsserviços?."
eval $(ssh-agent -s)
ssh-add /home/fernando/.ssh/chave-debian10-github
git push
git status




# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# 04 O que são microsserviços?

## Transcrição

[00:00] Então já entendemos como funciona a web, o que é uma aplicação monolítica e alguns dos problemas dessa abordagem. Agora vamos falar sobre a arquitetura de microsserviços.

[00:14] Vamos entender o que é isso, o que é esse tal de microsserviço. Então imagina aquele mesmo exemplo que vimos de uma aplicação monolítica, onde nós temos uma loja e aí temos o serviço de catálogo, temos pedidos, temos pagamento e podemos ter várias outras coisas.

[00:27] Em uma arquitetura de microsserviços, o que nós temos é cada uma dessas partes, cada pedaço desse nosso sistema de loja vai ser uma aplicação diferente e essa aplicação diferente, essa pequena aplicação é o que chamamos de um serviço. E a ideia de microsserviços é ter vários microsserviços.

[00:50] Ou seja, vários desses serviços muito pequenos, que tenham uma responsabilidade muito bem definida, que saibamos exatamente o que cada um dos serviços vai fazer.

[01:00] Então de novo, naquele exemplo da loja, ela vai ter um serviço de catálogo, que vai lidar com produtos, vai ter toda a lógica de cadastro, de exibição de produtos, como um produto é organizado, tudo isso vai ter o próprio banco de dados. Um banco de dados de catálogo que lida com produtos, categorias, taxonomia de produtos.

[01:24] Então toda a lógica de produtos está nessa aplicação separada. Já a parte de realizar um pedido, por exemplo, vamos ter um serviço específico de pedido. E os pedidos estarão armazenados em um banco de dados diferente do de produtos. Então os produtos estão nesse banco de dados e os pedidos estão em outro.

[01:46] Se por algum motivo o sistema de pedidos sair do ar, eu ainda consigo ver o meu catálogo de produtos, navegar nas páginas e ver o que eu quero comprar. Eu não vou conseguir efetivar a compra, mas eu consigo ir navegando.

[01:59] Então nesse meio tempo inclusive eu tenho tempo da pessoa continuar navegando sem perceber que há um problema e eu tenho tempo de reparar esse outro serviço. Às vezes o meu serviço de carrinho não está funcionando, mas a pessoa consegue finalizar, já realizar um pagamento direto sem adicionar no carrinho.

[02:16] Então eu posso pular essa etapa se o meu serviço estiver fora do ar, enfim, temos mais flexibilidade dessa forma e esse é o ponto.

[02:25] E a definição formal, caso você me conheça e já tenha ouvido falar de alguma aula minha, a definição formal é algo que eu gosto de trazer e depois desmembrar. Mas essa definição é até interessante e faz sentido. Então eu vou ler para você:

[02:41] "Microsserviços são uma abordagem arquitetônica e organizacional do desenvolvimento de software na qual o software consiste em pequenos serviços independentes que se comunicam usando APIs bem definidas. Esses serviços pertencem a pequenas equipes autossuficientes".

[02:59] Então já temos algumas coisas interessantes para pensar. Primeiro, você já provavelmente estava pensando: “Vinícius, como eu vou fazer um pedido e armazenar no banco de dados, se eu não sei os detalhes do produto que estão sendo comprados?” Então esse que é o ponto.

[03:14] Os microsserviços, para gerarem uma aplicação completa, eles precisam se comunicar. Então o meu microsserviço pedido vai conhecer o de catálogo, o de produto.

[03:25] Ele vai conhecer o banco de dados, ele vai saber como funciona a lógica, toda a taxonomia de produtos? Não. Mas ele vai conhecer o endpoint, por exemplo, vai saber como acessar os detalhes de um produto ou alguma coisa assim, pegar pelo menos uma identificação de um produto para conseguir armazenar e quando eu quiser buscar os dados desse pedido, eu pego ele e tenho os detalhes do produto para depois conseguir consultar no catálogo.

[03:50] Então os serviços vão se comunicar e essa comunicação pode ser feita de diversas formas. Por exemplo, através de HTTP. Um serviço pode realizar requisições para outro através de HTTP, utilizando APIs rest, ou até protocolos um pouco mais complexos, específicos para esse tipo de coisa, como GRPC ou alguma coisa do tipo.

[04:11] Então a comunicação entre microsserviços é algo muito importante e comum, acontece bastante e precisamos nos comunicar.

[04:19] E um outro ponto falado nessa definição formal, é que esses serviços pertencem a pequenas equipes autossuficientes.

[04:26] O que isso quer dizer é que eu posso muito bem, de forma muito tranquila, ter uma equipe inteira cuidando desse serviço de produto, com uma tecnologia, uma stack, uma equipe de gestão, ou uma metodologia ágil sendo aplicada e outra equipe completamente diferente cuidando do projeto de pagamentos, com outra stack, com outra metodologia de desenvolvimento.

[04:48] Então por isso microsseviços trazem tanta flexibilidade para o nosso projeto. Mas precisamos falar de vantagens e desvantagens, e isso vamos falar no próximo vídeo.







# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# 04 O que são microsserviços?



