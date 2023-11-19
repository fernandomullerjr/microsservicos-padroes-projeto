
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# push

git status
git add .
git commit -m "Aula 01 - Apresentação."
eval $(ssh-agent -s)
ssh-add /home/fernando/.ssh/chave-debian10-github
git push
git status


## Transcrição

[00:00] Olá, pessoal! Boas-vindas à Alura. Eu sou o Vinicius Dias e vou guiar vocês nesse treinamento sobre padrões de projeto quando conversamos sobre arquitetura de microsserviços. Nesse treinamento vamos começar entendendo o básico, como a web funciona? O que é o protocolo de HTTP?

[00:17] A partir disso vamos conhecer o modelo de aplicações, a arquitetura de aplicações monolíticas. E a partir disso vamos entender algumas desvantagens de aplicações monolíticas. E a partir disso que vamos começar a falar sobre o que são microsserviços, quais as vantagens de microsserviços e suas desvantagens.

[00:38] Só então, a partir dessa ideia vamos começar a falar de padrões. Vamos falar sobre como separar microsserviços, como integrar microsserviços, como microsserviços devem lidar com dados, como lidar com a operação de microsserviços. Então vamos falar de logs, métricas, vamos conversar bastante sobre a parte arquitetural de infraestrutura, de código, de operações. Então vai ser um papo bem interessante.

[01:02] Esse treinamento é conceitual, então não vamos escrever código, não é um tipo de laboratório onde criamos um projeto. Eu vou falar bastante, mostrar alguns slides para você, passar conceitos e obviamente deixar exercícios para fixarmos esse conteúdo.

[01:18] Se nesse processo ficar alguma dúvida, se algo não ficou muito claro, você não entendeu muito bem, nós temos um fórum, você pode abrir uma dúvida lá, eu tento responder pessoalmente sempre que eu consigo, mas quando eu não consigo, nós temos uma grande comunidade de alunos, moderadores, instrutores e com certeza alguém vai conseguir te ajudar. Então espero você na próxima aula para já começarmos a entender sobre esse mundo da web para começarmos a colocar o nosso pé na arquitetura de microsserviços.
