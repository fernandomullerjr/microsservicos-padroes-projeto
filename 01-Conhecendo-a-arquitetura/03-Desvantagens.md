
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# push

git status
git add .
git commit -m "Aula 03 Desvantagens."
eval $(ssh-agent -s)
ssh-add /home/fernando/.ssh/chave-debian10-github
git push
git status




# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# 03 Desvantagens

A abordagem de aplicações monolíticas, assim como qualquer abordagem no desenvolvimento de software, possui vantagens e desvantagens.

Qual das alternativas a seguir é uma desvantagem de aplicações monolíticas?
Selecione uma alternativa

    Deploys possivelmente mais perigosos

    Maior simplicidade da infra

    Base de código única







# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# ############################################################################################################
# RESPOSTA


Deploys possivelmente mais perigosos

Alternativa correta! Uma aplicação monolítica tem um único deploy, então um erro em uma parte da aplicação pode quebrar uma outra que não tem nenhuma relação.