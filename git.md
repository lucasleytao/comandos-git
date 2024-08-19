## COMANDOS

## Inicializar repositório Git (Git Bash)

Dentro da pasta do projeto (Botão direito) Open Git Bash here (abre uma linha de comando Git)

## Criando um arquivo git	

	git init               
Cria um arquivo git (somente na primeira vez)

	git status              
## Relatório de atualizacao de status 

No Visual Studio Code (VS Code), o controle de versão Git é integrado, e as letras que aparecem ao lado dos arquivos indicam o status deles em relação ao Git. Aqui estão as principais letras e seus significados:

### 1. **U** - **Untracked**
   - **Significado:** O arquivo é novo e não está sendo rastreado pelo Git.
   - **Exemplo:** `U  new-file.js`

### 2. **M** - **Modified**
   - **Significado:** O arquivo foi modificado em relação ao último commit, mas ainda não foi adicionado à área de staging.
   - **Exemplo:** `M  modified-file.js`

### 3. **A** - **Added**
   - **Significado:** O arquivo foi adicionado à área de staging, ou seja, foi incluído para o próximo commit.
   - **Exemplo:** `A  added-file.js`

### 4. **D** - **Deleted**
   - **Significado:** O arquivo foi deletado e essa exclusão foi adicionada à área de staging.
   - **Exemplo:** `D  deleted-file.js`

### 5. **R** - **Renamed**
   - **Significado:** O arquivo foi renomeado, e essa renomeação foi adicionada à área de staging.
   - **Exemplo:** `R  renamed-file.js -> new-name.js`

### 6. **C** - **Copied**
   - **Significado:** O arquivo foi copiado de outro arquivo e essa cópia foi adicionada à área de staging.
   - **Exemplo:** `C  copied-file.js`

### 7. **??** - **Untracked**
   - **Significado:** Similar ao "U", indica que o arquivo é novo e não está sendo rastreado pelo Git.
   - **Exemplo:** `?? new-file.js`

### 8. **AM** - **Added and Modified**
   - **Significado:** O arquivo foi adicionado e modificado antes do commit.
   - **Exemplo:** `AM added-and-modified-file.js`

### 9. **MM** - **Modified in both Staging and Working Directory**
   - **Significado:** O arquivo foi modificado e adicionado à área de staging, e depois foi modificado novamente na working directory.
   - **Exemplo:** `MM modified-file.js`

### 10. **UU** - **Unmerged**
   - **Significado:** Indica um conflito de merge que não foi resolvido.
   - **Exemplo:** `UU conflicting-file.js`

Essas letras ajudam a identificar rapidamente o estado de cada arquivo no repositório Git dentro do VS Code.

## OCULTAR ARQUIVOS

## Git ignore (Ocultar uma pasta ou arquivo do controle de versao)

Cria um arquivo .gitignore (botao direito - abrir com bloco de notas e especificar o arquivo que deseja ocultar [salvar])

	touch .gitignore

* pasta/
* arquivo.jpg

## ESTADOS

* Modificado (modified);
* Preparado (staged/index);
* Consolidado (comitted);

## Adicionando arquivos ao controle de versão (não enviados)

### Adiciona um arquivo específico ao controle de versão

	git add "arquivo.ext" 
Adiciona todos os arquivos e pastas ao controle de versao

	git add .             

Remove um arquivo específico

	git rm --cached "arquivo.ext" 


## Criando versões do código (commits)

	git commit -m "mensagem da versao"

## Configurando usuário do git (somente na primeira vez)

## Boa prática
Define o email para os commits

	git config --global user.email "email-github"

Define o nome do usuario para os commits

	git config --global user.name"nome-identificador-atrelado-a-versao"  

## Enviar alterações usando git push

* Criar novo repositório no GitHub 
* New repository (copia link)

## Código no Git 
Define para onde o código será enviado

	git remote add origin (cola link - botao direito - paste)

[enter] 

	git push (pede para copiar link <branch>) 
Divisões ou versões diferentes de código (galho)

Selecionar branch

	git push --set-upstream origin master 

## Sucesso!  
Código enviado para o GitHub (repositório remoto)

## VERSÕES

## Histórico de atualizações do código

	git reflog   

## Voltar para uma versão anterior

	git reset --hard 1658aa4 (id da versao que deseja recuperar)

## BRANCHS

## Criando uma branch (galho)
Mostra a branch atual

	git branch     

Cria uma nova branch

	git branch beta  

Mostra a lista de branchs

	git branch   

Muda para a branch desejada
	
	git checkout beta  

MODO CURTO!

Cria uma nova branch a partir da branch atual e muda automaticamente para a branch criada

	git checkout -b beta-feature master  

Excluir uma branch remota específica

	git push origin --delete <nome da branch>

## Git merge (unir branches)

* passo 1 - Entrar na branch que irá receber as atualizacoes

git checkout branchdestino

* passo 2 - Informar a branch que estará fornecendo as atualizacoes

IMPORTANTE!!! CUIDADO PARA NÃO QUEBRAR A BRANCH PRINCIPAL!

ANTES DE EXECUTAR O MERGE, DEVE-SE VERIFICAR A ATUALIZAÇÃO MAIS RECENTE DO SERVIDOR

Mostra a versao mais recente da branch principal do codigo

	git pull (puxar)       

Branch que fornece as atualizacoes

	git merge branchorigem   

Branch principal

	git push (empurrar)    

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

## Pull Request (solicitar) 

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

## Remover repositório

Para alterar o repositório remoto que já está configurado, você pode usar os seguintes comandos do Git:

## Remover o repositório remoto existente:

	git remote remove origin

## Adicionar o novo repositório remoto:

	git remote add origin https://repositorio_escolhido

## Verificar se o novo repositório remoto foi configurado corretamente

	git remote -v

## PRINCIPAIS COMANDOS

Inicializa um novo repositório git de um diretório já existente

    git init

Verifica o status atual dos repositórios git

    git status

Clona um repositório hospedado na nuvem

    git clone url-endereco-do-repositorio-remoto

Cria um arquivo `.gitignore` (oculta `arquivo.jpg` ou `pasta/`)

    touch .gitignore

A branch atual será renomeada para `main` (padrão)

    git branch -m main

Adiciona um arquivo ao estado de pronto para commit (stage)

    git add "arquivo.ext"

Adiciona todos os arquivos ao estado de pronto para commit (stage)

    git add .

Desfaz uma ou mais alterações feitas depois de usar o `git add`

    git restore --staged "arquivo.ext"

Remove um arquivo do estado de pronto para commit (stage)

    git rm --cached "arquivo.ext"

Mostra o que foi alterado antes de adicionar o arquivo para stage

    git diff

Compara alterações do stage com o commit anterior

    git diff --staged

Registra no commit as alterações com uma mensagem curta (checkpoint)

    git commit -m "mensagem de versao"

Envia as atualizações para a nuvem na branch ativa (atual)

    git push

Permite listar e ver qual branch está ativa atualmente

    git branch

Permite criar uma nova branch (galho)

    git branch nomebranch

Excluir uma branch

    git branch -d nomebranch

Permite mudar para uma nova branch

    git checkout nomebranch

Cria uma nova branch a partir da branch atual e muda para a branch criada

    git checkout -b nomenovabranch branchatual

Mostra a versão mais recente da branch principal do código

    git pull branchmain

Branch que fornece as atualizações

    git merge branchorigem

## AJUDA

##### Geral
	git help
	
##### Comando específico
	git help add
	git help commit
	git help <qualquer_comando_git>
	

## Configuração

### Geral

As configurações do GIT são armazenadas no arquivo **.gitconfig** localizado dentro do diretório do usuário do Sistema Operacional (Ex.: Windows: C:\Users\Documents and Settings\Leonardo ou *nix /home/leonardo).

As configurações realizadas através dos comandos abaixo serão incluídas no arquivo citado acima.

##### Setar usuário
	git config --global user.name "Leonardo Comelli"

##### Setar email
	git config --global user.email leonardo@software-ltda.com.br
	
##### Setar editor
	git config --global core.editor vim
	
##### Setar ferramenta de merge
	git config --global merge.tool vimdiff

##### Setar arquivos a serem ignorados
	git config --global core.excludesfile ~/.gitignore

##### Listar configurações
	git config --list

### Ignorar Arquivos

Os nomes de arquivos/diretórios ou extensões de arquivos listados no arquivo **.gitignore** não serão adicionados em um repositório. Existem dois arquivos .gitignore, são eles:

* Geral: Normalmente armazenado no diretório do usuário do Sistema Operacional. O arquivo que possui a lista dos arquivos/diretórios a serem ignorados por **todos os repositórios** deverá ser declarado conforme citado acima. O arquivo não precisa ter o nome de **.gitignore**.

* Por repositório: Deve ser armazenado no diretório do repositório e deve conter a lista dos arquivos/diretórios que devem ser ignorados apenas para o repositório específico.

## Repositório Local

### Criar novo repositório

	git init

### Verificar estado dos arquivos/diretórios

	git status

### Adicionar arquivo/diretório (staged area)

##### Adicionar um arquivo em específico

	git add meu_arquivo.txt

##### Adicionar um diretório em específico

	git add meu_diretorio

##### Adicionar todos os arquivos/diretórios
	
	git add .	
	
##### Adicionar um arquivo que esta listado no .gitignore (geral ou do repositório)
	
	git add -f arquivo_no_gitignore.txt
	
### Comitar arquivo/diretório

##### Comitar um arquivo
	
	git commit meu_arquivo.txt

##### Comitar vários arquivos

	git commit meu_arquivo.txt meu_outro_arquivo.txt
	
##### Comitar informando mensagem

	git commit meuarquivo.txt -m "minha mensagem de commit"

### Remover arquivo/diretório

##### Remover arquivo

	git rm meu_arquivo.txt

##### Remover diretório

	git rm -r diretorio

### Visualizar histórico

##### Exibir histórico
	
	git log
	
##### Exibir histórico com diff das duas últimas alterações

	git log -p -2
	
##### Exibir resumo do histórico (hash completa, autor, data, comentário e qtde de alterações (+/-))

	git log --stat
	
##### Exibir informações resumidas em uma linha (hash completa e comentário)

	git log --pretty=oneline
	
##### Exibir histórico com formatação específica (hash abreviada, autor, data e comentário)

	git log --pretty=format:"%h - %an, %ar : %s"
	
* %h: Abreviação do hash;
* %an: Nome do autor;
* %ar: Data;
* %s: Comentário.

Verifique as demais opções de formatação no [Git Book](http://git-scm.com/book/en/Git-Basics-Viewing-the-Commit-History)

##### Exibir histório de um arquivo específico

	git log -- <caminho_do_arquivo>

##### Exibir histórico de um arquivo específico que contêm uma determinada palavra

	git log --summary -S<palavra> [<caminho_do_arquivo>]

##### Exibir histórico modificação de um arquivo

	git log --diff-filter=M -- <caminho_do_arquivo>

* O <M> pode ser substituido por: Adicionado (A), Copiado (C), Apagado (D), Modificado (M), Renomeado (R), entre outros.

##### Exibir histório de um determinado autor

	git log --author=usuario

##### Exibir revisão e autor da última modificação de uma bloco de linhas

	git blame -L 12,22 meu_arquivo.txt 

### Desfazendo operações

##### Desfazendo alteração local (working directory)
Este comando deve ser utilizando enquanto o arquivo não foi adicionado na **staged area**. 

	git checkout -- meu_arquivo.txt

##### Desfazendo alteração local (staging area)
Este comando deve ser utilizando quando o arquivo já foi adicionado na **staged area**.

	git reset HEAD meu_arquivo.txt

Se o resultado abaixo for exibido, o comando reset *não* alterou o diretório de trabalho. 

	Unstaged changes after reset:
	M	meu_arquivo.txt

A alteração do diretório pode ser realizada através do comando abaixo:
	
	git checkout meu_arquivo.txt

## Repositório Remoto

### Exibir os repositórios remotos

	git remote
	
	git remote -v

### Vincular repositório local com um repositório remoto

	git remote add origin link-do-repositorio-remoto
	
### Exibir informações dos repositórios remotos

	git remote show origin
	
### Renomear um repositório remoto 

	git remote rename origin curso-git
	
### Desvincular um repositório remoto
	
	git remote rm curso-git

### Enviar arquivos/diretórios para o repositório remoto

O primeiro **push** de um repositório deve conter o nome do repositório remoto e o branch.

	git push -u origin master
	
Os demais **pushes** não precisam dessa informação

	git push
	

### Atualizar repositório local de acordo com o repositório remoto

##### Atualizar os arquivos no branch atual

	git pull
	
##### Buscar as alterações, mas não aplica-las no branch atual

	git fetch
	
### Clonar um repositório remoto já existente

	git clone git@github.com:leocomelli/curso-git.git
	
### Tags

##### Criando uma tag leve

	git tag vs-1.1

##### Criando uma tag anotada

	git tag -a vs-1.1 -m "Minha versão 1.1"

##### Criando uma tag assinada
Para criar uma tag assinada é necessário uma chave privada (GNU Privacy Guard - GPG).

	git tag -s vs-1.1 -m "Minha tag assinada 1.1"

##### Criando tag a partir de um commit (hash)

	git tag -a vs-1.2 9fceb02
	
##### Criando tags no repositório remoto

	git push origin vs-1.2
	
##### Criando todas as tags locais no repositório remoto

	git push origin --tags
	
### Branches

O **master** é o branch principal do GIT.

O **HEAD** é um ponteiro *especial* que indica qual é o branch atual. Por padrão, o **HEAD** aponta para o branch principal, o **master**.

##### Criando um novo branch

	git branch bug-123
	
##### Trocando para um branch existente

	git checkout bug-123
	
Neste caso, o ponteiro principal **HEAD** esta apontando para o branch chamado bug-123.

##### Criar um novo branch e trocar 

	git checkout -b bug-456
	
##### Voltar para o branch principal (master)

	git checkout master
	
##### Resolver merge entre os branches

	git merge bug-123
	
Para realizar o *merge*, é necessário estar no branch que deverá receber as alterações. O *merge* pode automático ou manual. O merge automático será feito em arquivos textos que não sofreram alterações nas mesmas linhas, já o merge manual será feito em arquivos textos que sofreram alterações nas mesmas linhas.

A mensagem indicando um *merge* manual será:

	Automerging meu_arquivo.txt
	CONFLICT (content): Merge conflict in meu_arquivo.txt
	Automatic merge failed; fix conflicts and then commit the result.


##### Apagando um branch

	git branch -d bug-123

##### Listar branches 

###### Listar branches

	git branch

###### Listar branches com informações dos últimos commits

	git branch -v

###### Listar branches que já foram fundidos (merged) com o **master**

	git branch --merged

###### Listar branches que não foram fundidos (merged) com o **master**

	git branch --no-merged

##### Criando branches no repositório remoto

###### Criando um branch remoto com o mesmo nome

	git push origin bug-123

###### Criando um branch remoto com nome diferente

	git push origin bug-123:new-branch

##### Baixar um branch remoto para edição

	git checkout -b bug-123 origin/bug-123


##### Apagar branch remoto

	git push origin:bug-123

### Rebasing

Fazendo o **rebase** entre um o branch bug-123 e o master.

	git checkout experiment
	
	git rebase master
	

Mais informações e explicações sobre o [Rebasing](http://git-scm.com/book/en/Git-Branching-Rebasing)

### Stash

Para alternar entre um branch e outro é necessário fazer o commit das alterações atuais para depois trocar para um outro branch. Se existir a necessidade de realizar a troca sem fazer o commit é possível criar um **stash**. O Stash como se fosse um branch temporário que contem apenas as alterações ainda não commitadas.

##### Criar um stash
	
	git stash
	
##### Listar stashes

	git stash list

##### Voltar para o último stash

	git stash apply

##### Voltar para um stash específico
	
	git stash apply stash@{2}
	
Onde **2** é o indíce do stash desejado.

##### Criar um branch a partir de um stash

	git stash branch meu_branch

### Reescrevendo o histórico

##### Alterando mensagens de commit

	git commit --amend -m "Minha nova mensagem"

##### Alterar últimos commits
Alterando os três últimos commits

	git rebase -i HEAD~3

O editor de texto será aberto com as linhas representando os três últimos commits.

	pick f7f3f6d changed my name a bit
	pick 310154e updated README formatting and added blame
	pick a5f4a0d added catfile

Altere para edit os commits que deseja realizar alterações.

	edit f7f3f6d changed my name a bit
	pick 310154e updated README formatting and added blame
	pick a5f4a0d added catfile

Feche o editor de texto.

Digite o comando para alterar a mensagem do commit que foi marcado como *edit*.

	git commit –amend -m “Nova mensagem”

Aplique a alteração

	git rebase --continue

**Atenção:** É possível alterar a ordem dos commits ou remover um commit apenas
mudando as linhas ou removendo.


##### Juntando vários commits
Seguir os mesmos passos acima, porém marcar os commtis que devem ser juntados com **squash*
	
##### Remover todo histórico de um arquivo

	git filter-branch --tree-filter 'rm -f passwords.txt' HEAD
	
	
### Bisect
O bisect (pesquisa binária) é útil para encontrar um commit que esta gerando um bug ou uma inconsistência entre uma sequência de commits.

##### Iniciar pequinsa binária

	git bisect start
	
##### Marcar o commit atual como ruim

	git bisect bad

##### Marcar o commit de uma tag que esta sem o bug/inconsistência

	git bisect good vs-1.1

##### Marcar o commit como bom
O GIT irá navegar entre os commits para ajudar a indentificar o commit que esta com o problema. Se o commit atual não estiver quebrado, então é necessário marca-lo como **bom**.

	git bisect good

##### Marcar o commit como ruim
Se o commit estiver com o problema, então ele deverá ser marcado como **ruim**.

 	git bisect bad
 
##### Finalizar a pesquisa binária
Depois de encontrar o commit com problema, para retornar para o *HEAD* utilize:
	
	git bisect reset