# dio-desafio-github-2022
Desafio de Projeto sobre Git/GitHub

## Comandos Básicos de Manipulção do Git no Linux / Windows

* Definição do escopo Global (E-mail / nome)
* Configuração do SSH (Commits sem necessidade de autenticação constantes)
* Criar estrutura base do repositório (Inicializar o diretório)
* Sincronização Diretório Git Local / GitHub Remoto


### Definição do escopo Global (E-mail / nome)

git config --global user.email "conta de e-mail"
git config --global user.name "Nome/apelido"


### Configuração do SSH (Commits sem necessidade de autenticação constantes)

**Gerar chave SSH**
ssh-keygen -t ed25519 -C *"e-mail"*

**Iniciar o Agent SSH (Linux)** - *Obs.:Em algumas distribuições Linux pode ser necessário executar com permissão de administrador*
eval $(ssh-agent -s)

**Adicionar a chave para o agente** - *(Deve ser adicionada a chave privada)*
ssh-add *caminho localização/chave criada*

**Adicionar a chave no GitHub** - *(Deve ser adicionada a chave pública)*
1. Acessar a conta do github 
2. Clicar na foto/imagem de perfil e selecionar **configurações**
3. Acessar o menu *SSH and GPG keys*. Em seguida clique em New SSH key (Nova chave SSH) ou Add SSH key (Adicionar chave SSH).
4. Definir um título (identificação) para a chave e adicione o conteúdo da chave no Key (chave)
5. Clique no botão * Add SSH key (Adicionar chave SSH).*
6. Digite a senha.


### Criar estrutura base do repositório (Inicializar o diretório)

**Criar o diretório (pasta) desejado**
mkdir projeto-git

**Acessar o diretório (pasta) criado**
cd projeto-git

**Criar estrutura inicial de um projeto Git ou clone um repositório existente**
git init
ou
git clone *URL SSH do repositório Git/GitHub*

*Crie os arquivos e pastas que desejar e depois adicione esses aquivos ao git para fazer o commit*
**Adicionar arquivos e verifique se tem alguma pendência**
git status
git add .
git commit -m "Descrição


### Sincronização Diretório Git Local / GitHub Remoto

**Verificar os repositórios sincronizados:**
git remote -v

**Adicionar repositório remoto (se for o caso)**
git remote add origin *URL do repositório GIT remoto*

**Enviar arquivos local para o remoto**. *Obs.: antes de executar o comando abaixo, confira se o repositório principal está nomeado como master ou main. Vai depender da versão do Git utilizdda. Ajuste o comando conforme configuração do Git* 
git push origin master
ou
git push origin main

**Buscar arquivos remotos para local**
git pull origin master
ou
git pull origin main
