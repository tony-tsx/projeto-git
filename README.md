# Comandos linux utilizados.

* ## ls
  ```
  ls
  ```
  > lista todos os arquivos dentro da pasta atual.
  ```

  ls <caminho>
  ```
  > lista todos os arquivos dentro da pasta especificada.

* ## clear
  ```
  clear
  ```
  > limpa o terminal.

* ## rm
  ```
  rm <caminho>
  ```
  > deleta o arquivo ou pasta especificado.

  ```
  rm -rf <caminho>
  ```
  > deleta o arquivo ou pasta especificado forçando e recursivamente.

# Comandos git

* ## git init
  ```
  git init
  ```
  > inicializa o repositório git na pasta atual.

  ```
  git init -b <nome da branch>
  ```
  > inicializa o repositório git na pasta atual, declarando a branch com qual quer começar

* ## git add
  ```
  git add .
  ```
  > adiciona todos os arquivos modificados, no "stage" do git para futuros commits.

  ```
  git add <caminho> [...caminhos]
  ```
  > adiciona o arquivo especifico modificado para o "stage" do git.

  ```
  git add <caminho> [...caminhos] -p
  ```
  > adiciona os arquivos especificado e particiona eles em hunks ( blocos de alteração dentro de um arquivo ), para separação de linhas especificas que vão ser adicionadas ao "stage" do git.

* ## git commit
  ```
  git commit -m <mensagem>
  ```
  > anexa uma mensagem a todos os arquivos que estão dentro do "stage" do git.

  ```
  git commit -m <mensagem> <caminho>
  ```
  > anexa uma mensagem ao arquivo especifico que já tenha pelo menos uma vez sido adicionado ao "stage" do git.

  ```
  git commit -m <mensagem> --amend
  ```
  > modificada a mensagem do último commit para a mensagem escrita.

* ## git branch
  ```
  git branch
  ```
  > lista todas as branches que estão no repositório local.

  ```
  git branch -r
  ```
  > lista todas as branches que estão no repositório centralizado.
  
  ```
  git branch <nome da branch>
  ```
  > cria uma nova branch localmente, mas não começa a utiliza-la.

* ## git checkout
  ```
  git checkout <nome da branch>
  ```
  > começa a utilizar a branch declarada.
    >> obs: a branch tem que existir.

  ```
  git checkou -b <nome da branch>
  ```
  > cria a branch localmente e começa a utiliza-la.

* ## git remote
  ```
  git remote -v
  ```
  > lista todas as conexões que está vinculadas ao repositório local.

  * ### add
    ```
    git remote add <nome da conexão> <url>
    ```
    > adiciona uma conexão do repositório centralizado.

  * ### remove
    ```
    git remote remove <nome da conexão>
    ```
    > remove uma conexão com o repositório centralizado.

  * ### get-url
    ```
    git remote get-url <nome da conexão>
    ```
    > mostra a url da conexão salva.

  * ### set-url
    ```
    git remote ser-url <nome da conexão> <url>
    ```
    > atualiza a url da conexão.

* ## git push
  ```
  git push <nome da conexão|url> <branch>
  ```
  > sobe as alterações que foram feitas localmente para o repositório centralizado.
  ```
  git push -u <nome da conexão|url> <branch>
  ```
  > sobe as alterações que foram feitas localmente para o repositório centralizado e define como padrão para os próximos comandos de push. Assim nas próximas vezes que você quiser dar o push não precisa declarar o nome da conexão e nem a branch `git push`

* ## git fetch
  ```
  git fetch <nome da conexão|url> <branch> 
  ```
  > recebe qualquer alteração nos arquivos que estão no repositório centralizado para o repositório local mas não atualiza os arquivos.

* ## git pull
  ```
  git pull <nome da conexão|url> <branch>
  ```
  > recebe qualquer alteração nos arquivos que estão no repositório centralizado para o repositório local e atualiza os arquivos.

* ## git clone
  ```
  git clone <url>
  ```
  > clona o repositório centralizado com a branch padrão e trás toda estrutura para uma pasta local.
  
  ```
  git clone <url> <pasta|caminho>
  ```
  > clona o repositório centralizado com a branch padrão e trás toda estrutura para uma pasta local especificada.

  ```
  git clone --single-branch --branch <branch> <url>
  ```
  > clona o repositório centralizado com uma branch especifica e trás toda estrutura para uma pasta local especificada.

* ## git merge
  ```
  git merge <branch local>
  ```
  > une as alterações em uma branch local à branch atual.

* ## git notes

  * ### list
    ```
    git notes list
    ```

  * ### add
    ```
    git notes add -m <mensagem> <hash>
    ```

  * ### append
    ```
    git notes append -m <mensagem> <hash>
    ```

  * ### remove
    ```
    git notes remove <hash>
    ```

  * ### show
    ```
    git notes show <hash>
    ```

* ## git restore
  ```
  git restore <caminho>
  ```
  > restaura o arquivo especifico para o último commit indentificado.

  ```
  git restore <caminho> -s <hash>
  ```
  > restaura o arquivo especifico para o commit indentificado pelo hash.

* ## git reset
  ```
  git reset --
  ```
  > remove do "stage" todos os arquivos que foram adicionados.

  ```
  git reset --soft <hash>
  ```
  > restaura a arvore do git para certo ponto mas não altera o conteúdo dos arquivos.

  ```
  git reset --hard <hard>
  ```
  > restaura a arvore do git para certo ponto alterando o conteúdo dos arquivos.

* ## git status
  ```
  git status
  ```
  > mostra os arquivos que foram modificados e não foram adicionados no "stage", e os arquivos que foram adicionados no "stage" mas não tiveram o commit relacionado a eles.

* ## git diff
  ```
  git diff
  ```
  > mostra a diferença dos arquivos que foram modificados comparando com os arquivos do último commit.
  ```
  git diff <caminho>
  ```
  > mostra a diferença de um arquivo especifico modificado com a versão que está no último commit.

* ## git log
  ```
  git log
  ```
  > mostra a árquivo do git no terminal informando o hash do commit, mensagem, notas, author e data.

# Dicas
  Em geral todos os comandos que são utilizado tem uma opção chamada help, o git é um desses comandos. Então para auxiliar a utilização da ferramenta podemos utilizar.
  ```
  git help
  ```
  ou
  ```
  git --help
  ```
  Então ele vai mostrar alguns comandos mais utilizados e a descrição sobre eles.

  Caso queira receber ajuda de um comando especifico poderá utilizar.
  ```
  git help <comando>
  ```
  ou
  ```
  git <comando> --help
  ```
  **Exemplo:**
  ```
  git commit --help
  ```