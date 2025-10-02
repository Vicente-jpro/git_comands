# git_comands

Aqui estão os comandos mais importantes do Git para usar no terminal, com uma breve descrição de cada um:

### 1. **Configuração inicial**
- **`git config --global user.name "Seu Nome"`**  
  Define o nome de usuário para o Git.

- **`git config --global user.email "seuemail@dominio.com"`**  
  Define o email para o Git.

- **`git config --global init.defaultBranch master`**  
  Define o nome da tua branch que serão criadas inicialmente como master.


- **`git config --global alias.co checkout`**  

- **`git config --global push.default matching`**  
  Define o push para todas as branches locais que tem o mesmo nome com a remota.
  
- **`git config --list`**  
  Lista todas as configurações do Git.


### 2. **Criação e clonagem de repositórios**
- **`git init`**  
  Inicializa um novo repositório Git no diretório atual.

- **`git clone <url-do-repositorio>`**  
  Clona um repositório remoto para o diretório local.

### 3. **Verificação do status**
- **`git status`**  
  Mostra o estado atual do repositório (arquivos modificados, adicionados, etc.).

### 4. **Adicionando e confirmando alterações**
- **`git add <arquivo>`**  
  Adiciona um arquivo específico à área de preparação (staging area).

- **`git add .`**  
  Adiciona todos os arquivos modificados à área de preparação.

- **`git commit -m "Mensagem do commit"`**  
  Cria um novo commit com os arquivos adicionados e a mensagem fornecida.

- **`git commit -a`**  
  Comita todos os arquivos modificados e rastreados, sem precisar usar `git add`.

### 5. **Visualizando históricos e diferenças**
- **`git log`**  
  Exibe o histórico de commits.

- **`git log --oneline`**  
  Exibe o histórico de commits em uma linha.

- **`git diff`**  
  Exibe as diferenças entre os arquivos modificados e a última versão commitada.

- **`git diff --staged`**  
  Exibe as diferenças dos arquivos que foram adicionados à área de preparação (staged).

### 6. **Gerenciamento de branches**
- **`git branch`**  
  Lista os branches locais no repositório.

- **`git branch <nome-do-branch>`**  
  Cria um novo branch.

- **`git checkout <nome-do-branch>`**  
  Muda para o branch especificado.

- **`git checkout -b <nome-do-branch>`**  
  Cria e muda para o novo branch.

- **`git merge <nome-do-branch>`**  
  Mescla o branch especificado com o branch atual.

- **`git branch -d <nome-do-branch>`**  
  Deleta o branch localmente.

### 7. **Sincronização com repositórios remotos**
- **`git remote add origin <url-do-repositorio>`**  
  Adiciona um repositório remoto.

- **`  git remote -v`**  
  Verificar se o repositório remoto foi adicionado.

- **`git push origin <nome-do-branch>`**  
  Envia as alterações locais para o repositório remoto no branch especificado.

- **`git pull origin <nome-do-branch>`**  
  Faz o pull (atualiza) o branch local com as mudanças do remoto.

- **`git fetch`**  
  Baixa as mudanças do repositório remoto, mas não as mescla automaticamente.

- **`git push`**  
  Envia as alterações para o repositório remoto.

- **`git pull`**  
  Atualiza o branch local com as mudanças do repositório remoto.

### 8. **Resolução de conflitos**
- **`git merge --abort`**  
  Desfaz um merge em caso de conflito.

- **`git rebase`**  
  Reaplica commits a partir de um branch base diferente, muitas vezes usado para evitar merges desnecessários.

- **`git rebase <branch-name>`**  
  Aplica seus commits no topo da `branch-name` atualizada.
  Caso de uso:
  Estas a trabalhar na branch `sprint-30` e fizeste um marge request para `main`.
  A branch `main` tem varios commites adiantado. Entao, queremos atualizar a nossa branch `sprint-30`
  e colocar o nosso commit no top de todos os commits.
  
    

- **`git rebase --continue`**  
  Continua o processo de rebase após resolver conflitos.

### 9. **Outros comandos úteis**
- **`git stash`**  
  Guarda temporariamente mudanças não comitadas (útil para mudar de branch sem perder alterações).

- **`git stash pop`**  
  Restaura as alterações que estavam guardadas com `git stash`.

- **`git reset <commit>`**  
  Reverte o repositório para um estado anterior, descartando ou mantendo as alterações.

- **`git reset --hard`**  
  Reverte para o último commit, descartando todas as mudanças não comitadas.

- **`git rm <arquivo>`**  
  Remove um arquivo do repositório e da área de preparação.

- **`git clean -fd`**  
  Remove arquivos não rastreados do diretório de trabalho (arquivos não versionados).

# Criação de ssh key
Neste tutorial ensinarei como criar uma key `ssh` para o teu repositório remoto.

Cria uma masta para 
```sh
  mkdir ~/ssh
```
Navega para o diretório `~/ssh` possivelmente o nome do diretório será `.ssh`. 
Executa o comando abaixo.

```sh
  ssh-keygen.exe
```

Após executar o comandos `ssh-keygen.exe` vai pedir-te a password, clica duas vezes `Enter` ou coloca a password e clica `Enter`. 
Automaticamente vai criar dois ficheiros com os nomes: `id_ed25519` e `id_ed25519.pub`
vamos usar o ficheiro  `id_ed25519.pub`
```sh
cat id_ed25519.pub
```
Este comando vai permitir ver o conteúdo da key pública. cópia e cola no teu `Github/GitLab`.
Você é inteligente. Vais descobrir onde deves colar
