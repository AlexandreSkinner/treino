
# Realizar um push destino(origin) origem(master)
  $ git push origin master

## Comandos git
 Workspace => Seu ambiente de desenvolvimento, o código que trabalhamos. Você já deve ter instalado o Git em sua máquina e feito as configurações necessárias como e-mail, senha, nome de usuário, SSH Keys Private Public, etc.


Local Repository => Local onde ficam salvos os códigos criados na sua máquina.


Remote Repository => Local onde ficam salvos os códigos criados por você ou uma equipe na qual você fará parte, e que todos terão acesso, pois localiza-se  na nuvem/servidor geralmente, o GitHub é um exemplo de Remote Repository. Você já deve ter feito o cadastro necessário no Github como e-mail senha nome de usuário SSH Keys Private Public, etc. 


$ git init 
 -Inicia um repositório, o git começa a monitorar suas ações neste diretório,  qualquer ação que você fizer(criar/editar arquivo) você terá um Status de Untracked  em seu Workspace.


$ git clone <urlDoProjetoHospedadoRemotamente>
 -Você fará do download para seu Workspace, do projeto hospedado remotamente, que já  estará integrado automaticamente com o Git.


$ git remote -v 
 -Listará todos os repositóriso remotos dispostos em sua máquina, (todos que vocÊ clonou).


$ git remote add origin <urlDoRepositórioHospedadoRemotamente> 
 -Adicionará o seu repositório Local à um repositório remoto(criado no Github), o  git remote add significa que você adicionará um repositório local ao remoto, o comando origin é como um apelido que você usará para o seu repositório, e a urlDoRepositórioHospedadoRemotamente é o endereço do seu repositóro hospedado no Github


$ git config --list
 -Lista todas as configurações relacionadas ao seu Git, estas configurações possuem 03 níveis: 
         Configuração do Sistema - servirá para qualquer projeto seu e qualquer usuário desta máquina. 
         Configuração do Usuário - servirá para qualqure projeto do seu usuário naquela máquina.
         Configuração do seu Projeto - servirá apenas para o determinado projeto.


$ git config --system --edit
 -Servirá para abrir o seu arquivo de configuração do Sistema a fim de poder editá-lo.


$ git config --global --edit 
 -Servirá para abrir o seu arquivo de configuração do Seu Usuário a fim de poder 
editá-lo, para você abri-lo no VSCode use o seguinte comando: git config --global core.editor code


$ git config --local --edit
 -Servirá para abrir o seu arquivo de configuração do git relacionado ao seu projeto.