# Configurar o git
git config --global user.name  "Fulano de Tal"
git config --global user.email "FulanoDeTal@email.com.br"

# Listar configuração
git config --global user.name
git config --global user.email
git config --list

# Criando um novo repositório local na pasta corrente e enviar para o Repositorio remoto
git init
git add README.md
git commit -m "first commit"
git branch -M master
git remote add origin https://github.com/AlexandreSkinner/Treino.git
git push -u origin master

# Inicializar um repositório remoto a partir de um repositorio local existente
git remote add origin https://github.com/AlexandreSkinner/exemplo.git
git branch -M master
git push -u origin master

# Clonando um repositório Remoto para um repositório local
git clone https://github.com/AlexandreSkinner/treino.git

# Configurar o GITHUB como repositório remoto
git remote add origin https://github.com/alexandreskinner/<repositorio>.git
git remote add origin https://github.com/anapaulatm/Treino.git

# Verificar qual o repositório remoto está configurado para um determinado repositório local
git remote -v

# Enviando modificações do repositório local para o repositório remoto
git push <destino> <origem>
git push origin master
git push -u origin master

# Atualizando seu repositorio local coma as modificações do repositorio remoto (faz merge automaticamente)
git pull

# Busca alterações que tenham sido feita no repositorio remoto para seu repositorio local (não faz merge)
git fetch <remote>
git fetch origin

# Verificar o status da working area, staging are e repository
git status

# Colocar arquivo na staging area (trackear)
git add <nome.ext>
git add -A
git add --all
git add .

# Colocar no repositório local
git commit -m "Descrição do commit" 

# Verificar os commit realizados 
git log
git log --oneline
git log --oneline --decorate --all
git log --oneline --decorate --all --graph

# Crira um novo branch 
git branch <NomeBranch>
git checkou -b <NomeBranch> (Cria a branch e ja muda para ela)

# Mudar de branch
git branch checkout <NomeBranch>

# Excluir uma branch depois que realizamos merge
git branch -d <NomeBranch>

# Merge (Mesclar) - posicionado na master
git merge <NomeBranch>

# Remover da staging area para a Working directory
git restore --stage <nomeArquivo.ext>
git restore --stage b.txt

# Deletar um arquivo do repositório local (arquivo comitado)
git rm <nomeArquivo.ext>
git rm produtos.html

# Desfazendo modificações ainda não rastreadas e não commitada (Working directory)
# serve para recuperar arquivo deletado ou desfazer uma alteração antes de commitar
git checkout -- <arquivo> ou --<commit>
git checkout -- b.txt
git ckeckout -- f45a7c9 (volta a posição até o commit selecionado)

# Mover de pasta um arquivo para já commitado
git mv principal.js js/principal.js

# Refazer o ultimo commit (alterar a mensagem)
git commit --amend -m "<nova mensagem>"


## Status de um arquivo
(??) Untraked - Arquivo que está na sua Workspace (novo) por tanto não controlado pelo git.

(M) Modified - Arquivo que está na sua Workspace, porém é uma arquivo tracked (rastreado) pelo git que foi modificado.

## Reverter um git add, ou seja, retirar um arquivo da Stage Area para a Workspace
$ git reset <nomeArquivo.ext>
$ git reset teste.js

## Reverter um commit, existem opções que indicam a extensão do comando, é necessário informar a ID do commit que ficara no HEAD 
$ git reset <HashDoCommit> --<opção>
$ git reset 8643aee --<opção> 
$ git reset HEAD~1 --<opção>

# 1) Opção --soft retorna os arquivos do commit para Stage e aponta o HEAD para o commit 8643aee ou HEAD~1 
$ git reset 8643aee --soft   ou
$ git reset HEAD~1  --soft

# 2) Opção --mixed retorna os arquivos do commit para o Workspace direto mantendo as alterações do commiit desfeito
$ git reset HEAD~1 --mixed

# 2) Opção --hard retorna os arquivos do commit para o Workspace direto sem as alterações que foram feitas
$ git reset HEAD~1 --hard


# Retira o arquivo do repositório local (comitado) para a staging are - preserva as mudanças
git reset -- <nomeArquivo.ext>
git reset -- b.txt

# Reverter o ultimo commit
git reset HEAD~1