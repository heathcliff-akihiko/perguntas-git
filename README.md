# Responda cada pergunta abaixo com suas palavras.
## As respostas estão [aqui](https://github.com/heathcliff-akihiko/perguntas-git/blob/main/respostas.md)

# **NÃO ESQUEÇA**
#### VOCÊ PODE OLHAR AS RESPOSTAS A QUALQUER MOMENTO MAS SE VOCÊ DESEJA REALMENTE TESTAR SEUS CONHECIMENTOS RESPONDA COM SUAS PALAVRAS
#### CASO NÃO SAIBA RESPONDER UMA DAS PERGUNTAS PESQUISE, REVEJA SUAS ANOTAÇÕES, TESTE NO SEU CONSOLE, CONSULTE A DOCUMENTAÇÃO, SEMPRE BUSCANDO APRENDER E NÃO DECORAR
#### LEMBRANDO QUE O QUE IMPORTA É QUE AS REPOSTA ESTEJA CERTA, NÃO COM AS MESMAS PALAVRAS.

# BOA SORTE

# Introdução ao Git

O Git é um sistema de controle de versão distribuído, amplamente utilizado para o gerenciamento de projetos de software. Ele permite que várias pessoas trabalhem em um projeto simultaneamente, rastreando as mudanças feitas ao longo do tempo.

## Principais Conceitos do Git

- **Repositório:**
  - Um repositório é um local onde o Git armazena todas as versões de um projeto.

- **Commit:**
  - Um commit é uma alteração feita no código. Cada commit tem uma mensagem descritiva que ajuda a entender as alterações feitas.

- **Branch (ramo):**
  - Um branch é uma ramificação do código principal. Ele permite que você trabalhe em novas funcionalidades sem afetar diretamente o código principal.

## Principais Comandos do Git

1. `git init` - Inicia um novo repositório Git em um diretório existente.

2. `git clone <URL do repositório>` - Clona um repositório existente para um novo diretório local.

3. `git add <nome do arquivo>` - Adiciona mudanças ao índice para preparação do commit.

4. `git commit -m "Mensagem do commit"` - Grava as mudanças no repositório.

5. `git pull origin <nome do branch>` - Atualiza o repositório local com as alterações remotas.

6. `git push origin <nome do branch>` - Envia as alterações locais para o repositório remoto.

7. `git branch` - Lista, cria ou exclui branches.

8. `git merge <nome do branch>` - Combina as alterações de um branch em outro.

9. `git log` - Exibe o histórico de commits.

## Conclusão

O Git é uma ferramenta poderosa para o gerenciamento de código-fonte, permitindo colaboração eficiente e rastreamento de alterações. A compreensão desses comandos básicos é essencial para utilizar o Git de maneira eficaz.

## Exercícios de Git - Nível Básico:

 1. Como inicializar um repositório Git em um diretório local?
   ***O comando utilizado é o git init***

 2. Quais comandos você usaria para adicionar todos os arquivos
    modificados ao índice (staging area)?
    ***git add .***

 3. Como confirmar (commit) as mudanças no repositório local?
   ***git commit -m "mensagem"***

 4. Explique a diferença entre "git pull" e "git push".
   ***O git push serve para subir os arquivos para o github e o git pull serve para atualizar as alterações realizadas por outros em meu repositório local.***

 5. Como verificar o status atual do seu repositório local?
   ***git status***

 6. Como desfazer as mudanças em um arquivo antes de confirmá-las
    (commit)?
    ***Para desfazer um commit que possa ter tido, por exemplo algum erro no arquivo é fazer o oposto do que é o commit basicamente, usamos o comando git revert mais a hash do commit que será revertido, se quiser reverter especificamente o último commit usamos git revert HEAD. Nada mais é do que um novo commit com as alterações inversas que haviam sido feitas anteriormente. Os arquivos retornam ao mesmo estado como se o commit atual nunca tivesse existido. O git revert é um commit só que ao contrário.***

 7. Como visualizar o histórico de commits do repositório local?
   ***usar o comando git log***

 8. Como criar e alternar entre branches (ramificações)?
   ***Para criar uma branch o comando é git checkout -b nome da branch, fazemos a alteração que desejamos no código pelo vscode, nesse momento quando damos o comando git status no terminal ele vai mostrar que temos uma modificação que foi feita no código que ainda não foi comitada, realizamos o commit com add . e git commit -m "mensagem do commit", em seguida git push nome da branch que foi criada, desta forma as alterações comitadas só foram feitas dentro da nova ramificação que criamos e para alternar entre as branchs é git checkout nome da branch.***

 9. Como mesclar (merge) uma branch com a branch principal (main)?
   ***Para fazer um merge no terminal temos que ir até a branch principal (main), através do comando git checkout main estando dentro da main damos o comando git merge nome da nova branch, agora é preciso comitar novamente para subir as alterações no github com add . e git commit -m "mensagem do commit", em seguida git push origin main, pois queremos fazer o commit para a branch principal.***

 10. Como clonar um repositório remoto para o seu computador?
    ***git clone url do repositório***

## Exercícios de Git - Nível Intermediário:

 1. Explique o que é um conflito de merge e como resolvê-lo.
  ***É quando tentamos atualizar um código que outra pessoa já havia atualizado e para resolver usamos o git pull origin main para pegar as alterações que foram feitas, vai aparecer no vscode qual é a mudança que eu fiz e também a mudança que outra pessoa já havia feito no código, nesse caso ou escolhemos qual das mudanças será utilizada ou se serão as 2. Aí é só clicar na opção de mudança escolhida ou clicar para atualizar com as 2 mudanças e fazer o processo de commit novamente.***

 2. Como reverter um commit específico no histórico?
  ***Essa não seria a mesma resposta da pergunta 6 no Nível Básico?***

 3. Descreva o que são as ações "git rebase" e quando elas são usadas.
  ***Pelo que entendi o git rebase serve para eu incluir uma branch em outro repositório sem precisar fazer um merge pra isso.***

 4. Como remover um arquivo do repositório e mantê-lo em versões
    anteriores?
    ***Para remover é git rm nome do arquivo.***

 5. Como usar o comando "git cherry-pick" para aplicar um commit
    específico em outra branch?
  ***É quando voce quer pegar algum commit de uma outra branch, porém não quer pegar todos os commits da outra branch, nesse caso ao invés de fazer um merge ou rebase, podemos usar o git cherry-pik. Para usar primeiro damos um git log para pegar o id do commit específico que queremos, em seguida dá git cherry-pick id do commit que pegamos com o log, desta forma temos esse arquivo específico na nova branch.***

 6. Como renomear um branch local e remoto?
  ***Na branch local é preciso usar o comando branch -m nome atual da branch e o novo nome da branch.No caso da branch remote, o git não permite apenas renomear, é preciso apagar e fazer a criação de uma nova branch. Primeiramente renomear essa branch git branch nome da branch, em seguida um git push origin --delete nome da branch a ser apagada e agora enviamos a branch renomeada para o servidor git push -u origin nome atual da branch.***

 7. Como criar e aplicar um patch no Git?
  ***O patch é um arquivo que lista somente as operações que foram atualizadas em um código e ele serve para aplicar todas essas alterações de uma só vez no código principal, fazemos isso usando o comando patch --help | head dou um enter e já aparece arquivo original e o arquivo patch. Aí digito patch arquivo original e arrasto o arquivo original para o terminal, dou um enter e pronto.***
  

 8. Explique a diferença entre "git reset" e "git revert".
  ***O objetivo principal deles é refazer a linha do tempo, apagar alguns commits que não precisamos mais. O git revert serve para pegar um commit específico e reverter para seu estado anterior, criando um novo commit através dele. Basicamente ele desfaz o que foi feito e cria um commit novo na linha do tempo.O git reset ele apaga a linha do tempo, sobrescrevendo ela. Mas existem 3 forma de reset, soft, mixed, hard. Quando damos o comando hard com a url do commit, tudo que tiver daquele commit pra frente será deletado. Quando não passa nenhum argumento ele faz um mixed, ele vai apagar, mas não vai deletar de vez, ainda fica lá dentro do diretório e o soft pega o que aconteceu daquele commit pra frente e deixa em staged para vc decidir o que vai deletar e o que vai continuar.***

 9. Como usar tags no Git para marcar versões importantes do código?
  ***basta digitar git tag -a versão -m "mensagem", em seguida dou um git push origin main --tags para subir as tags e pronto.***

 10. Descreva o fluxo de trabalho básico para contribuir para um projeto
     de código aberto usando forks e pull requests.
     ***Logada no meu github acesso um projeto aberto de terceiros, a ideia é fazer um fork desse projeto para o meu github. Dentro do projeto clico em fork, no menu lateral clico em meus repositórios e pronto o projeto que fiz o fork já estará lá. Desta forma posso agora fazer modificações nesse projeto sem interferir no projeto principal da outra pessoa. Fazendo qualquer alteração no código (que agora tem uma versão no meu github), vou criar o commit, incluindo a mensagem sobre a alteração realizada, neste momento ele mostra que tem mais de um contribuidor para este projeto, no caso, eu e o dono do projeto. Para sugerir esta alteração no projeto original, preciso criar um pull request, clicando no botão pull request dentro do referido repositório, o github vai verificar se não tem nenhum conflito, mostra o detalhe da alteração realizada e clicamos em create pull request. Nesse momento o dono do projeto vai ser sinalizado sobre esta solicitação de recebimento e ele pode alterar ou não o projeto original.***
