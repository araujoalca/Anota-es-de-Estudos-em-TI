# GIT E GITHUB

**Duas tecnologias diferentes, mas complementares, para:**
- Controle de Versão (versionamento)
- Armazenamento em nuvem (GitHub)
- Trabalho em equipe (colaborativo)
- Melhoramento de código (colaborativo)
- Reconhecimento (visibilidade)


## Resumo para comandos no Git Bash  


|        **Unix (Bash)**         | **Descrição**                            |
| :----------------------------: | ---------------------------------------- |
|               cd               | Navega entre os diretórios               |
|              cd /              | Vai pra o diretório raiz                 |
|        cd NomeDiretório        | Vai para o diretório NomeDiretório       |
|             cd ..              | Retrocede um nível                       |
|         clear (ctrl l)         | Limpa a tela                             |
|      rm -rf meuDiretorio/      | Deleta o diretório meuDiretorio e todo o seu conteúdo<br>r = recursivo (todas as pastas/arquivos dentro)<br>f = force, para não pedir confirmação se quer apagar mesmo |
|               ls               | Lista o conteúdo de um diretório         |
|             ls -a              | Mostra arquivos  e pastas ocultos        |
|     echo > NovoArquivo.txt     | Cria o arquivo NovoArquivo.txt (deleta o que já existir) |
|     echo "Meu texto aqui"      | Escreve "Meu texto aqui" na tela         |
| echo "1 2 3" > NovoArquivo.txt | Cria o NovoArquivo.txt (deleta se já existir) – contendo o texto "1 2 3" |
|      mkdir NovoDiretorio       | Cria o diretório NovoDiretorio           |
|    mv arquivo.md ./meudir/     | Move o arquivo.md para o diretório meudir |
|              pwd               | Mostra o  caminho de diretórios onde vc está (path) |


**COMANDOS DO GIT**

|           **Unix (Bash)**           | **Descrição**                            |
| :---------------------------------: | ---------------------------------------- |
|              git init               | inicializa um repositório no diretório atual |
|      git add * <br> git add .       | Transfere todas as modificações para a staging area  (as habilita para receber commit) |
|   git add strogonoff.md receitas    | Transfere strogonoff.md para a staging area |
| git commit -m "meu primeiro commit" | Envelopa os arquivos em staging area, criando o objeto commit no repositório local |
|             git status              | Mostra o  estado dos arquivos            |
|          git config --list          | Lista os dados de configuração do GIT    |

***Trocando nome e email***

|             **Unix (Bash)**              | **Descrição**                            |
| :--------------------------------------: | ---------------------------------------- |
|             git config –list             | Lista as configurações do GIT, como email, nome, etc... |
|  git config --global --unset  user.name  | Deleta o nome atual                      |
| git config --global --unset  user.email  | Deleta o email atual                     |
| git config --global user.name  "araujoalca" | Adiciona o novo nome às configurações o GIT |
| git config --global user.email "araujoalca@id.uff.br" | Adiciona o novo email às configurações o GIT |

***Linkando o repositório local e "empurrando-o" para o GitHub***

|             **Unix (Bash)**              | **Descrição**                            |
| :--------------------------------------: | ---------------------------------------- |
| git remote add origin url-copiada-no-github | Configura no GIT onde o repositório será 'empurrado' (push). Antes, copie a URL na página do repositório no GitHub |
|              git remote -v               | Lista as referências do repositório local no servidor |
|                git status                | Certifique-se de que não há pendências no repositório  local (de que não há nada para ser 'add' ou 'commit' |
|          git push origin master          | ‘Empurra’ o repositório local para o servidor |

***Resolvendo Conflitos***

|             **Unix (Bash)**              | **Descrição**                            |
| :--------------------------------------: | ---------------------------------------- |
|                  Obs 1:                  | * Edite o  arquivo **README.md** lá do servidor GitHub |
|                  Obs 2:                  | * E edite também, mas de  forma diferente, a mesma linha do arquivo **README.md** do seu GIT local |
|                git status                | Mostrará que há um arquivo **modified** e ainda não  está "*staged for commit*" |
|                 git add                  | Adiciona o README para o **staging**     |
|                git status                | Mostrará agora que as mudanças (*modified*) estão prontas para serem **commitadas** |
|   git commit -m "alteração  do README"   | Agora, o estado atual está **unmodified** na máquina local (objeto *commit* pronto para o *push* no servidor) |
|          git push origin master          | Vai tentar empurrar o seu repositório local para o  GitHub, mas vai dar **conflito** porque o repositório do servidor tem alterações  que vc não havia incorporado ao seu git local. Primeiro vc deve **puxar**  os arquivos de lá (*pull*) e fazer um merge com o seu GIT, e só depois de resolver este conflito em sua máquina, dar um **push** novamente |
|          git pull origin master          | **Puxará** (*pull*) os  arquivos do servidor e o GIT tentará fazer a junção, o **merge**, dos dois  conteúdos, mas como as mesmas linhas foram alteradas com conteúdo diferente,  **o merge falhará**: "*automatic merge failed*"<br><br>Para resolver  o conflito, abra o arquivo **README.md** de seu GIT local (que estará com  conteúdo diferente, pois conterá a tentativa de merge com o novo conteúdo  que estava no servidor) e reedite-o para a forma final como ele deve ficar.  Salve-o. |
|                git status                | Mostrará que *há uma resolução de conflito* e **merge** em  andamento entre dois arquivos – e está no estado **modified** - e sugere fazer o **merge** ao **adicioná-lo** e **commitá-lo**, e assim resolver o conflito |
|                 git add                  | Finaliza o conflito com o **merge** e *torna o arquivo pronto  para ser commitado* |
| git commit -m "resolve  conflitos do README" | Resolve a alteração *no repositório local* (ainda falta *empurrar* para o servidor) |
|          git push origin master          | **Empurra** o objeto *commitado* para o repositório  do servidor |
