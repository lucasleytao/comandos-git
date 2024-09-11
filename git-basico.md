## Git#GitHub
### Git version
    git --version
### User list (lista de identificação)
    git config --global --list
### User
    git config --global user.name 'nome'
    git config --global user.email 'email'
### List (lista de arquivos e diretórios)
    ls
### Arquivos ocultos (lista arquivos ocultos)
    ls -a
### Change Directory (mudar diretório)
    cd nome_diretorio
### Change Directory (diretório anterior)
    cd ..
### Touch (criar arquivo)
    touch nome_arquivo.txt
### Make (criar diretório)
    mkdir nome_diretorio
### Clear (limpar)
    clear
### Histórico de comandos
* Up (pra cima)
* Down (pra baixo)
### Excluir arquivo (remove)
    git rm nome_arquivo.txt
### Excluir diretório (local)
    rm -rf nome_diretorio
### Excluir diretório
    git rm -r nome_diretorio
### Nano (editor de texto para terminal)
    nano nome_aquivo.txt (se não existir, será criado)
##
* Control + O (Output) 'Gravar e Sair'
* Confirmar nome do arquivo 'Enter'
* Control + X 'Sair do nano'
### Cat (exibe conteúdo de um arquivo)
    cat nome_arquivo.txt
### Mover ou Renomear
    mv nome_arquivo nome_arquivo1 
## Comandos especiais
### Repositório específico (sai do atual e entra no específico)
    cd ../nome_repositorio
### Log de envios (sair > q)
    git log
### Histórico de envios de um determinado autor
    git log --author=nome_usuario
### Log de envios condensado (sair > q)
    git log --oneline
### Reverter envio (checkout) Verde
### Não altera histórico do Git (Marco histórico)
    git log --oneline (copia id_envio)
    git checkout id_envio (verifica versao)
    git checkout main (retorna a ultima versao)
### Reverter envio (Revert) [ :q ] Amarelo
### Altera histórico do Git
    git log --oneline (copia id_envio)
    git revert id_envio (desfaz e altera historico)
### Reverter envio (Reset) [ :q ] Vermelho
### Apaga histórico do Git
    git log --oneline (copia id_envio)
    git reset id_envio (apaga historico)
    git reset id_envio --hard (apaga tudo)
### Unir comandos (&&)
    git add . && git commit -m "mensagem"
### Git ignore (Ocultar uma pasta ou arquivo do controle de versão)
    touch .gitignore
* pasta/
* arquivo.jpg
### Branch
    git branch (lista branchs)
    git branch nome_branch (cria uma nova branch)
    git branch -b nome_branch (cria e seleciona)
    git checkout nome_branch (escolhe branch)
    git branch -D nome_branch (hard delete branch)
### Push da branch
    git push origin nome_branch
### Merge (Fundir branchs)
* Seleciona Branch de destino
##
    git merge nome-branch
## #GitHub
    Serviço de host para repositórios Git 
    > Servidor remoto
##
* Push (Empurrar): Subir
* Pull: Baixar
### #Push (Empurrar) (forma verbosa)
    git push link_repositorio nome_branch(origem)
### Adicionar Alias (Apelido) para o repositório
    git remote add origin(apelido) link_repositorio
### Verificar configurações do apelido (fletch e push)
    git remote -v
### Push (forma reduzida)
    git push origin nome_branch
### #Pull (Baixar)
* Verifica se há atualizações e faz o MERGE no diretório principal
##
    git pull origin diretorio_principal
### #Clone (Clonar repositório)
* Copia link do repositório que deseja clonar (Code)
##
    git clone link_projeto
* Clone de projeto com nome próprio
##
    git clone link_projeto nome_proprio
* Excluir uma pasta clonada (hard reset)
##
    rm -rf nome-do-projeto
### #Pull Request (Abre um pedido de fusão)
* entrar no projeto
### [ Compare & pull request ]
* cria um pull request para o seu tech lead analisar, ou seja, abre um pedido de fusão com a branch principal (em produção)
### #Fork
* Contribuição com outros projetos OpenSource no GitHub











