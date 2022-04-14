# Repositório do Desafio de Projeto Git/GitHub da DIO
Repositório criado para pesafio de projeto sobre Git/GitHub para o bootcamp **Spread Fullstack Developer**.  

Reforce seu conhecimento em Git com um desafio de projeto totalmente prático, onde você executará todos os passos para a criação, atualização e sincronização de um repositório no GitHub. Para isso, tenha em mente todas as dicas e direcionamentos apresentados pelo expert nas aulas. Dessa forma, você poderá compartilhar suas anotações e exercícios em seu próprio repositório. Criando assim, o primeiro (de muitos) projetos do seu portfólio ;-)

## Links Úteis
[Sintaxe Básica Markdown](https://www.markdownguide.org/)

## Comandos Cobertos Neste Curso
### git clone
Para clonar um repositório que ja tenha sido publicado no GitHub. Exemplo  
```
  git clone git@github.com:wfbraga/dio-desafio-github-primeiro-repositorio.git
```

### git status
Mostra a branch na qual estamos, se est'a atualizada com _origin/main_ e se existe algo que falta "commitar"
```
$ git status
No ramo main
Your branch is up-to-date with 'origin/main'.

nothing to commit, working tree clean
```
### git add
Depois de criar novos arquivos ou pastas e’ necessário adicioná-los  a lista de arquivos que estao prontos para serem “commitados”.  
Podemos usar: 
```
$git add <nome-do-arquivo-ou-pasta> 
```
Ou passar flag “.” indicando que queremos adicionar todos os arquivos novos a lista de arquivos a serem “commitados”
```
$git add .
```
Esse comando não produz um output no terminal, mas se dermos um _git status_ teremos uma saída diferente da primeira vez.
```
$ git status
No ramo main
Your branch is up-to-date with 'origin/main'.

Mudanças a serem submetidas:
  (use "git restore --staged <file>..." to unstage)
        new file:   lista_repositorios/links.html
```
### git commit
Depois de _git add_, usamos _git commit_ para indicar que realmente queremos que as últimas alterações façam parte do histórico do repositório. Usamos flas –m para indicar que queremos passar uma mensagem que deve ser uma breve explicação sobre as alterações feitas nos arquivos.
```
$ git commit -m "Inclindo primeira pasta e arquivo com lista de links para os repos"
[main 0818a64] Inclindo primeira pasta e arquivo com lista de links para os repos
 1 file changed, 23 insertions(+)
 create mode 100644 lista_repositorios/links.html
```
### git push
Depois de trabalhar no repositório na nossa maquina e hora de publicar nossas alterações no GItHub. Para isso usamos o comando _git push_ (do ingles “empurrar”). Devemos indicar para onde queremos “empurrar” essas alterações. No nosso caro usamos _origin_, que se refere a origem remota do repositório, ou seja, no GitHub e logo informamos a branch, que no nosso caso e’ a _main_.
```
$ git push origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (4/4), 725 bytes | 181.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0)
To github.com:wfbraga/dio-desafio-github-primeiro-repositorio.git
   447dc41..0818a64  main -> main
```
### Bonus: git pull
'git pull' irá buscar no repo remoto e atualizar seu repo local. Muitas vezes, a branch padrão no Git é uma branch _master_ ou _main_ e continua sendo atualizada com frequência. Um usuário pode usar qualquer nome de branch para extrair essa ramificação do repo remoto. No usaremos _git pull origin main_ para atualizar nosso repo local.
```
$ git pull origin main
From github.com:wfbraga/dio-desafio-github-primeiro-repositorio
 * branch            main       -> FETCH_HEAD
Already up-to-date.
```
O output do nosso comando indica que não há nenhuma alteração no repositório remoto para ser puxada. Casou houvesse, produziria um output similar à mostrada abaixo. 

```
$ git pull origin main
From github.com:wfbraga/dio-desafio-github-primeiro-repositorio
 * branch            main       -> FETCH_HEAD
Updating 0818a64..2a116d8
Fast-forward
 README.md | 74 +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++-
 1 file changed, 73 insertions(+), 1 deletion(-)
```
## Considerações Finais
Esses são os comandos primordiais que um iniciante deve conhecer mais ainda muito por cobrir no futuro. Meu conselho e’ que pesquise como criar novas _branchs_ e usar _git reset_ que não foram cobertos nesse breve repositório.  
