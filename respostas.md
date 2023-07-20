## Exercícios de Git - Nível Básico:


1. Como inicializar um repositório Git em um diretório local?
***Resposta***: Use o comando `git init` para inicializar um repositório Git em um diretório local.

2. Quais comandos você usaria para adicionar todos os arquivos modificados ao índice (staging area)?
***Resposta***: Use o comando `git add .` para adicionar todos os arquivos modificados ao índice.

3. Como confirmar (commit) as mudanças no repositório local?
***Resposta***: Use o comando `git commit -m "mensagem do commit"` para confirmar as mudanças no repositório local.

4. Explique a diferença entre "git pull" e "git push".
***Resposta***: `git pull` é usado para obter as mudanças do repositório remoto e incorporá-las ao repositório local, enquanto `git push` é usado para enviar as mudanças do repositório local para o repositório remoto.

5. Como verificar o status atual do seu repositório local?
***Resposta***: Use o comando `git status` para verificar o status atual do repositório local.

6. Como desfazer as mudanças em um arquivo antes de confirmá-las (commit)?
***Resposta***: Use o comando `git checkout -- nome-do-arquivo` para desfazer as mudanças em um arquivo específico antes de confirmá-las.

7. Como visualizar o histórico de commits do repositório local?
***Resposta***: Use o comando `git log` para visualizar o histórico de commits do repositório local.

8. Como criar e alternar entre branches (ramificações)?
***Resposta***: Use o comando `git branch nome-do-branch` para criar um novo branch e `git checkout nome-do-branch` para alternar entre branches.

9. Como mesclar (merge) uma branch com a branch principal (main)?
***Resposta***: Primeiro, alterne para a branch principal usando `git checkout main` e, em seguida, use o comando `git merge nome-da-branch` para mesclar a branch com a principal.

10. Como clonar um repositório remoto para o seu computador?
***Resposta***: Use o comando `git clone URL-do-repositorio` para clonar um repositório remoto para o seu computador.

  

## Exercícios de Git - Nível Intermediário:

  

1. Explique o que é um conflito de merge e como resolvê-lo.
***Resposta***: Um conflito de merge ocorre quando dois branches têm alterações conflitantes no mesmo trecho de código. Para resolvê-lo, é necessário abrir o arquivo em conflito, resolver as diferenças manualmente e, em seguida, adicionar e confirmar as mudanças novamente.

2. Como reverter um commit específico no histórico?
***Resposta***: Use o comando `git revert hash-do-commit` para reverter um commit específico no histórico. Isso criará um novo commit que desfaz as mudanças do commit original.

3. Descreva o que são as ações "git rebase" e quando elas são usadas.
***Resposta***: O comando `git rebase` é usado para reaplicar uma sequência de commits em um branch diferente. Ele é frequentemente usado para manter o histórico de commits limpo e linear, evitando o uso de merges. Ele é útil quando você deseja trazer as alterações de uma branch para a outra.

4. Como remover um arquivo do repositório e mantê-lo em versões anteriores?
***Resposta***: Use o comando `git rm nome-do-arquivo` para remover o arquivo do repositório e, em seguida, confirme a mudança. O arquivo será removido nas versões futuras, mas ainda estará disponível nas versões anteriores do histórico.

5. Como usar o comando "git cherry-pick" para aplicar um commit específico em outra branch?
***Resposta***: Use o comando `git cherry-pick hash-do-commit` para aplicar um commit específico em outra branch. Isso criará um novo commit na branch atual, aplicando as alterações do commit especificado.

6. Como renomear um branch local e remoto?
***Resposta***: Para renomear um branch local, use o comando `git branch -m novo-nome-do-branch` enquanto estiver em outro branch. Para renomear um branch remoto, use `git push origin :nome-do-branch-antigo novo-nome-do-branch` e, em seguida, `git push origin novo-nome-do-branch`.

7. Como criar e aplicar um patch no Git?
***Resposta***: Use o comando `git format-patch branch` para criar um arquivo de patch a partir das diferenças entre a branch atual e a especificada. Para aplicar um patch, use o comando `git apply nome-do-patch`.

8. Explique a diferença entre "git reset" e "git revert".
***Resposta***: O comando `git reset` é usado para desfazer commits, removendo-os do histórico, enquanto `git revert` é usado para criar um novo commit que desfaz as mudanças de um commit específico, mantendo-o no histórico.

9. Como usar tags no Git para marcar versões importantes do código?
***Resposta***: Use o comando `git tag nome-da-tag` para criar uma nova tag. Para marcar um commit específico, use `git tag nome-da-tag hash-do-commit`. Use `git push origin nome-da-tag` para enviar a tag para o repositório remoto.

10. Descreva o fluxo de trabalho básico para contribuir para um projeto de código aberto usando forks e pull requests.
***Resposta***: O fluxo de trabalho básico envolve: fazer um fork do repositório do projeto de código aberto, clonar o fork para o seu computador, criar uma nova branch para suas alterações, fazer as alterações, confirmá-las, enviar a branch para o repositório remoto no seu fork, e finalmente, criar um Pull Request para solicitar que suas alterações sejam incorporadas ao projeto principal.
