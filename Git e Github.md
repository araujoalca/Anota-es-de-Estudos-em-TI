# GIT E GITHUB



**Duastecnologias diferentes, mas complementares, para: **  

- Controle de Versão (versionamento)
- Armazenamento em nuvem (GitHub)
- Trabalho em equipe (colaborativo)
- Melhoramento de código (colaborativo)
- Reconhecimento (visibilidade)



## Resumo para comandos no Git Bash  





| Comando     | Descrição                                |
| :---------- | :--------------------------------------- |
| cd <br>cd / | Navega entre diretóros <br>Vai para o diretório Raiz |
|             |                                          |
|             |                                          |
|             |                                          |



|             **Unix (bash)**              | **Descrição**                            |
| :--------------------------------------: | ---------------------------------------- |
| cd<br>cd /<br>cd NomeDiretório<br>cd ..  | Navega entre  os diretórios <br>Vai pra o  diretório raiz<br>Vai para o  diretório especificado<br>Retrocede um  nível |
|              clear (ctrl l)              | Limpa a tela                             |
|           rm -rf meuDiretorio/           | Deleta o diretório meuDiretorio e todo o seu conteúdo<br>r = recursivo (todas as pastas/arquivos dentro)<br>f = force, para não pedir confirmação se quer apagar  mesmo |
|               ls<br>ls -a                | Lista o  conteúdo de um diretório<br>Mostra arquivos  e pastas ocultos |
| echo > NovoArquivo.txt<br>echo "Meu texto aqui"<br>echo "1 2 3" > NovoArquivo.txt | Cria o arquivo NovoArquivo.txt (deleta o que já existir)<br>Cria o hello.txt (deleta se já existir) – contendo o texto “1 2 3”<br>Escreve “Meu texto aqui” na tela |
|           mkdir NovoDiretorio            | Cria o diretório NovoDiretorio           |
|         mv arquivo.md ./meudir/          | Move arquivo.md para o diretório  meudir |
|                   pwd                    | Mostra o  caminho de diretórios onde vc está (path) |
| ....................................................... | ...............   COMANDOS DO GIT ............... |
|                 git init                 | inicializa  um repositório no diretório atual |
| git add * ou git add .<br>git add strogonoff.md receitas | Passa todas  as modificações para a staging area<br>Põe strogonoff.md na staging area (pronto para receber commit) |
|   git commit -m “meu primeiro commit”    | Envelopa os arquivos em staging, criando o objeto  commit no repositório local |
|                git status                | Mostra o  estado dos arquivos            |
|            git config --list             | Lista os dados de configuração do GIT    |
| ***Trocando nome e email***<br>git config –list<br>git config --global --unset  user.name<br>git config --global --unset  user.email<br>git config --global user.name  "araujoalca"<br>git config --global user.email  "araujoalca@id.uff.br" | <br>// Lista as configurações do GIT, como email, nome, etc...<br>// Deleta o nome atual<br><br>// Deleta o email atual<br><br>// Adiciona o novo nome às configurações o GIT<br><br>// Adiciona o novo email às configurações o GIT<br> |
| ***Linkando o repositório local com o GitHub***<br>git remote add origin url-copiada-no-github<br>  git remote -v<br>git status<br><br>git push origin master | <br><br>// Mostra ao GIT onde o repositório será 'empurrado' (push). Antes, copie  a URL na página do repositório no GitHub<br>// Lista as referências do repositório local no servidor<br>// Certifique-se de que não há pendências no repositório  local (de que não há nada para ser 'add' ou 'commit'<br>// ‘Empurra’ o  repositório local para o servidor |
| ***Resolvendo Conflitos***<br><br><br><br>git status<br><br>git add<br>git status<br><br>git commit -m “alteração  do README”<br>git push origin master<br><br><br><br><br>git pull origin master<br><br><br><br><br><br><br><br>git status<br><br><br><br>git add<br><br>git commit -m “resolve  conflitos do README<br>git push origin master | * Edite o  arquivo **README.md** lá do servidor GitHub<br>* E edite também, mas de  forma diferente, a mesma linha do arquivo **README.md** do seu GIT local.<br><br>// Mostrará que há um arquivo **modified** e ainda não  está “*staged for commit*”<br>// Adiciona o README para o **staging**<br>// Mostrará  agora que as mudanças (*modified*) estão prontas para serem **commitadas**<br>// Agora o estado atual está **unmodified** na máquina local (pronto  para o push no servidor)<br>// Vai tentar empurrar o seu repositório local para o  GitHub, mas vai dar **conflito** porque o repositório do servidor tem alterações  que vc ainda não incorporou ao seu git local. Primeiro vc deve trazer, **puxar**  os arquivos de lá e fazer um merge com o seu, e só depois de resolver este  conflito, dar um **push** novamente.<br>// **Puxará** (*pull*) os  arquivos do servidor e o GIT tentará fazer a junção, o **merge**, dos dois  conteúdos, mas como as mesmas linhas foram alteradas com conteúdo diferente,  **o merge falhará**: “*automatic merge failed*”<br>Para resolver  o conflito, abra o arquivo **README.md** de seu GIT local (que estará com  conteúdo diferente, pois conterá a tentativa de merge com o novo conteúdo  que estava no servidor) e reedite-o para a forma final como ele deve ficar.  Salve-o.<br>// Mostrará que *há uma resolução de conflito* e **merge** em  andamento entre dois arquivos – e está no estado **modified** -  e faz a sugestão  para fazer o **merge** ao **adicioná-lo** e **commitá-lo** e assim resolver o conflito<br>// Resolve o conflito com o **merge** e *torna o arquivo pronto  para ser commitado* (na área de **staging**)<br>// Resolve a alteração *no repositório local* (falta  *empurrar* para o servidor)<br>// **Empurra** o objeto *commitado* para o repositório  do servidor |