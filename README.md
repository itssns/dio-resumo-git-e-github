
## RESUMOS GIT E GITHUB

Repositório para armazenar resumos sobre Git e Github do curso de código Git e Github [Digital Inovation Onne](https://www.dio.me/)

## 📔 Documentação
- [Documentação Git] (https://git-scm.com/doc)
- [Documentação GitHub] (https://docs.github.com/pt)

## 💻 Resumos das Aulas

| Aulas | Resumos |
|------|---------|
|Gravando alterações do Repositório Local | Resumos

## Git
O que é Git?
Git é um sistema distribuído opensource de controle de versão 
– o mais popular do mundo, diga-se de passagem. 
O objetivo do Git é registrar todas as mudanças feitas no código-fonte de um projeto, 
evitando que algo importante se perca no meio do caminho.
- [Qual a importancia dos comandos fo git?] (https://www.atlassian.com/br/git/tutorials/)

## Comandos mais usados ⬇️

##  Git Init

O que é?
É um comando único que você usa durante a configuração inicial de um novo repositório.
```
git init
```
## Git Clone

O que é?
O Git clone é um comando para baixar o código-fonte existente de um repositório remoto (como o Github, por exemplo).
```
git clone <https://url-do-link>
```
## Git branch

O que é?
Funciona basicamente da seguinte forma: a cada alteração realizada no código, 
seja para adicionar um novo recurso ou até mesmo corrigir um erro, 
cria-se um novo ponto de ramificação que consolida essas mudanças, 
sem interferir nos arquivos originais.
Este comando é usado para criar, listas e excluir ramificações, exemplos abaixo.
Para criar uma nova branch local:

```
git branch <nome-da-branch>

```
Para upar a nova branch para o repositório remoto, você precisa usar o seguinte comando:

```
git push -u <remote> <nome-da-branch>
```
Para ver as ramificações, use:
```
git branch
```
ou
```
git branch --list

```
Por último para deletar, use:
``` 
git branch -d <nome-da-branch>

```
## Git checkout
O que é? Permite navegar entre ramificações criadas pelo git branch . A verificação de uma ramificação atualiza os arquivos no diretório atual para que fique igual à versão armazenada nessa ramificação e diz ao Git para gravar todos os novos commits nessa ramificação.

O principal objetivo do git checkout é ajudar você a mudar de uma branch para outra ou então verificar arquivos e commits:
```
git checkout <nome-da-ramificação>
```
Existe ainda um comando de atalho que te permite criar e ir para um branch de uma vez só:
```
git checkout -b <nome-da-branch>
```
## Git status
O que é? serve para fornecer algumas informações importantes sobre a branch em que você estiver no momento, incluindo se ela está atualizada em relação à master e quais arquivos foram alterados.
``` 
git status

```
## Git diff
Para que serve? Caso você queira, por exemplo, saber exatamente o que você alterou (e não apenas quais arquivos foram alterados). Basicamente, sua execução realiza uma função de comparação nas fontes de dados Git e mostra quais linhas foram adicionadas e removidas, utilize o comando:

```
git diff

```
## Git add

Para que serve? Quando criamos, modificamos ou excluímos um arquivo, essas alterações ocorrerão em nosso ambiente local e não serão incluídas no próximo commit (a menos que alteremos as configurações). Para incluir as alterações de um arquivo em nosso próximo commit, será preciso usar o comando git add.
```
git add <arquivo>

```
Para adicionar, de uma vez, todos os arquivos modificados:

```
git add -A
```
## Git commit
Para que serve? Esse comando visa definir um ponto de verificação no processo de desenvolvimento, para o qual você pode voltar mais tarde, se necessário.
```
git commit -m "mensagem explicando a mudança no código"

```
## Git push
Para que serve?
Após confirmar as alterações, a próxima coisa que você deseja fazer é enviar as alterações para o servidor remoto usando o comando git push:
```
git push <remote> <nome-do-branch>
```
No entanto, se seu branch for criado recentemente, você também precisará fazer upload do branch com o seguinte comando:
```
git push -u origin <nome-do-branch>
```
## Git pull
Para que serve? O git pull é usado para obter atualizações do repositório remoto. 

Trata-se de um comando que depende do referencial de onde ele foi feito, ou seja, um git pull feito da sua máquina vai puxar informações do repositório original para ela. Mas um git pull feito a partir do repositório original vai puxar as informações da sua máquina. Percebe?

Este comando é uma combinação de git fetch (baixa as alterações do repositório remoto, mas não as mescla com o seu) e git merge (que mescla tudo junto).

Isso significa que, quando usamos o git pull, ele recebe as atualizações do repositório remoto (git fetch) e aplica imediatamente as alterações mais recentes no seu local (git merge).
```
git pull <remote>
```
## Git revert
Para que serve? Existem várias maneiras de desfazer nossas alterações local ou remotamente (dependendo da necessidade), mas devemos usar esses comandos com cuidado para evitar problemas.

Uma maneira segura de desfazer os commits é usando git revert.

```
git revert 'número do hash'
```
O número do hash pode ser conseguido pelo comando:
```
git log -- oneline
```
## Git merge
Para que serve? Quando você conclui o desenvolvimento em sua branch e tudo funciona bem, sem conflitos, a etapa final é mesclar as branches, isso é feito com o comando git merge.

Como falamos no tópico sobre git pull, esse comando vai mesclar, no seu repositório local, todas as alterações feitas.
```
git merge <nome-da-branch>
```
## Git stash
Para que serve? Sabe quando você está trabalhando em uma parte do projeto que não está fluindo como deveria e, então, decide mudar de branch por um tempo para trabalhar em outra coisa?

Bom, quando isso acontece não é preciso necessariamente fazer o commit. Com o comando git stash, existe a possibilidade de apenas arquivar as alterações que você fez na cópia de trabalho durante um determinado período para que seja possível retornar a ela mais tarde.

Para salvar as alterações sem commit, basta executar:
```
git stash
```
Já para ver todas as stashes que você guardou, use:
```
git stash list
```
Por último, você também pode aplicar stashes antigos, especificando:
``` 
it stash apply stash@{2}.
```
## 🔍 Referências
- [Geekhunter] (https://blog.geekhunter.com.br/comandos-git-mais-utilizados/)
