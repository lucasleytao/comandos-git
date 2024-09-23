## Git#GitHub
* Diretório: Pasta de arquivos
* Repositório: Rastreador de arquivos
### #Git
* Ferramenta que rastreia alterações de código, auxiliando desenvolvedores que trabalham de forma colaborativa. Os objetivos incluem velocidade e integridade de dados e suporte para fluxos de trabalho não lineares distribuidos.
### #GitHub
* É um provedor (servidor) de hospedagem remoto para desenvolvimento de software e controle de versão utilizando o Git. Ele oferece o controle de versão distribuida e a funcionalidade de gerenciamento de código no Git, além de seus próprios recursos.
### #Pontos importantes
* Commit: Funciona como um marco histórico de alterações importantes.
## Comandos
### Criando um arquivo git
* Cria um arquivo git (somente na primeira vez)
##	
	git init   
##            
	git status              
### Relatório de atualização de status 

* No Visual Studio Code (VS Code), o controle de versão Git é integrado, e as letras que aparecem ao lado dos arquivos indicam o status deles em relação ao Git. Aqui estão as principais letras e seus significados:

### 1. **U** - Untracked
   - **Significado:** O arquivo é novo e não está sendo rastreado pelo Git.
   - **Exemplo:** `U  new-file.js`

### 2. **M** - Modified
   - **Significado:** O arquivo foi modificado em relação ao último commit, mas ainda não foi adicionado à área de staging.
   - **Exemplo:** `M  modified-file.js`

### 3. **A** - Added
   - **Significado:** O arquivo foi adicionado à área de staging, ou seja, foi incluído para o próximo commit.
   - **Exemplo:** `A  added-file.js`

### 4. **D** - Deleted
   - **Significado:** O arquivo foi deletado e essa exclusão foi adicionada à área de staging.
   - **Exemplo:** `D  deleted-file.js`

### 5. **R** - Renamed
   - **Significado:** O arquivo foi renomeado, e essa renomeação foi adicionada à área de staging.
   - **Exemplo:** `R  renamed-file.js -> new-name.js`

### 6. **C** - Copied
   - **Significado:** O arquivo foi copiado de outro arquivo e essa cópia foi adicionada à área de staging.
   - **Exemplo:** `C  copied-file.js`
### Git version
    git --version
### Listando Usuários
### User list (lista de identificação)
    git config --global --list
### User
    git config --global user.name 'nome'
    git config --global user.email 'email'
### Listando Arquivos
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
### Reverter envio (checkout) (Sem riscos)
### Não altera histórico do Git (Marco histórico)
    git log --oneline (copia id_envio)
    git checkout id_envio (verifica versao)
    git checkout main (retorna a ultima versao)
### Reverter envio (Revert) [ :q ] (Cuidado)
### Altera histórico do Git
    git log --oneline (copia id_envio)
    git revert id_envio (desfaz e altera historico)
### Reverter envio (Reset) [ :q ] (Alto risco)
### Apaga histórico do Git
    git log --oneline (copia id_envio)
    git reset id_envio (apaga historico)
    git reset id_envio --hard (apaga tudo)
### Unir comandos (&&)
    git add . && git commit -m "mensagem"
### Alterar mensagem de commit
    git commit --amend
* Isso abrirá o editor de texto Vim
* Edite > Esc > Digite :wq > Enter
### Estágios do Commit
    M - Modified (Modificado): Arquivos alterados
    A - Staging (Área de palco): Arquivos prontos para envio
    Committed: Arquivos enviados
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

## Trabalhando com equipes

## Passo a passo de segurança que garante que o código não seja quebrado

* 1 git pull da branch principal
* 2 gerar uma nova branch a partir da branch principal
* 3 trabalhar e adicionar novas funcionalidades na nova branch criada
* 4 finalizar o trabalho na branch temporaria
* 5 git checkout na branch principal
* 6 git pull
* 7 mergear (unir) o código da branch temporária com a branch principal (depois de testar)
* 8 git push da branch principal

## Solicitar Pull Request

Avalição (aprovação ou reprovação) do código por um membro da equipe de desenvolvimento

Fluxo básico de trabalho no Git para clonar um repositório no qual você é colaborador, fazer alterações e submetê-las para revisão em um Pull Request.

1. **Configurar Git**:
   Certifique-se de que o Git está instalado no seu computador. Você pode verificar isso abrindo o terminal ou prompt de comando e digitando `git --version`. Se o Git não estiver instalado, você pode baixá-lo e instalá-lo do [site oficial do Git](https://git-scm.com/).

2. **Configurar suas credenciais no Git**:
   Antes de clonar o repositório, é uma boa prática configurar seu nome de usuário e email no Git, que serão usados nas suas contribuições. Você pode fazer isso com os seguintes comandos:
   ```bash
   git config --global user.name "Seu Nome"
   git config --global user.email "seu.email@exemplo.com"
   ```

3. **Clonar o repositório**:
   - Encontre o URL do repositório no GitHub. Isso pode ser encontrado na página principal do repositório, geralmente sob o botão "Clone or download".
   - Abra o terminal ou prompt de comando e digite o seguinte comando para clonar o repositório:
     ```bash
     git clone URL_DO_REPOSITÓRIO
     ```
4. **Navegar até o diretório do repositório**:
   Após clonar, um novo diretório com o nome do repositório será criado. Navegue até este diretório com o comando:
   ```bash
   cd nome_do_repositório
   ```

5. **Criar uma nova branch**:
   É uma boa prática não trabalhar diretamente na branch principal (geralmente chamada de `main` ou `master`). Crie uma nova branch para suas alterações:
   ```bash
   git checkout -b nome_da_nova_branch
   ```

6. **Fazer suas alterações**:
   Abra os arquivos no seu editor de código de preferência e faça as alterações necessárias.

7. **Adicionar as alterações para o próximo commit**:
   Depois de fazer suas alterações, você precisa adicionar essas alterações ao índice do Git usando:
   ```bash
   git add .
   ```
   Ou, se preferir adicionar arquivos específicos:
   ```bash
   git add caminho_para_arquivo
   ```

8. **Fazer o commit das alterações**:
   Commitar suas alterações armazena um snapshot das alterações no histórico do Git. Faça isso com:
   ```bash
   git commit -m "Descreva as alterações feitas"
   ```

9. **Enviar as alterações para o repositório remoto**:
   Após fazer o commit das suas alterações localmente, você precisa enviá-las para o repositório remoto (GitHub) para que todos os colaboradores possam vê-las. Faça isso com:
   ```bash
   git push origin nome_da_nova_branch
   ```

10. **Criar um Pull Request**:
    - Vá até a página do GitHub do repositório e você geralmente verá um prompt para "Comparar & pull request" na nova branch que você enviou. Clique nisso.
    - Revise as mudanças e, se estiver tudo certo, crie o Pull Request para a branch principal. Você pode adicionar descrições adicionais e discutir as alterações com outros colaboradores antes de suas alterações serem mescladas.











