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
