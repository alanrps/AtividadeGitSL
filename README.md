# AtividadeGitSL

# Git Assignment

**INDIVIDUAL**

**Entrega**: 18-Mar-21

## Como entregar
Copie o arquivo em um repositorio que seja seu e coloque as respostas nas caixas abaixo

Abra uma issue nesse repositório aqui indicando o link para o arquivo no seu repo.

### Entenda o repositorio
Baixe o arquivo [handson.zip] (handson.zip) e descompacte-o
A pasta handson é um repositório git. Usando a linha de comando, altere o diretório para "handson/"

As caixas vazias
```,                                

```
representam o conteúdo que você precisa preencher e postar em seu repositório privado

1. Descreva qual é a saída dos seguintes comandos
    -  `git branch` 
    -  `git checkout BRANCH_NAME` (USE THE NAME OF AN EXISTING BRANCH)
    -  `git log --decorate`

```
Git branch: Lista simples das branches atuais.
Git checkout feature-foo: Altera a branch atual para a selecionada.
Git log --decorate: Lista o histórico de commits na branch atual.
```

2. Tente usar `git log --graph --all`. O que acontece?
```
Retorna o histórico de commits em todas as branchs, isto com a representação gráfica das branchs no lado esquerdo.
```

3. Use `git diff BRANCH_NAME`  para ver as diferenças de um ramo e do ramo atual.
   Sumarize as diferenças do master e do outro ramo.

```
diff --git a/A.java b/A.java
index 3ea227e..674b8ce 100644
--- a/A.java
+++ b/A.java
@@ -1,4 +1,7 @@
 public class A {
-
+   
+   public void foo() {
+   
+   }
 
 }
diff --git a/B.java b/B.java
index ae64e6b..e69de29 100644
--- a/B.java
+++ b/B.java
@@ -1,4 +0,0 @@
-public class B {
-
-
-}

Acima é possível visualizar as diferenças que foram retornadas no terminal, 
os que possuem "-" significa que são ausências e o "+" significa que possue aquele dado a mais.
```

4. Escreva uma sequencia de comandos para mesclar o ramo não-master no `master`

```
git checkout master
git merge feature-foo
```


5. Escreva um comando (ou sequência) para (i) criar um novo ramo chamado `math` (do` master`)
e (ii) mudar para este ramo

```
git checkout -b math -> Cria nova branch e já altera para ela.
```
   
6. Edite B.java adicionando o código abaixo ao conteúdo do arquivo
```java
System.out.println("I know math, look:")
System.out.println(2+2)
```

7. Escreva o comando (ou sequencia) para realizar o commit de suas mudanças
```
git add B.java
git commit -m "Alter file B.java feature-foo"
```

8. Volte para o branch `master` e mude B.java adicionando o seguinte código-fonte (confirme sua mudança para` master`):
```java
System.out.println("Hello World")
```
```
git checkout master
vim B.java
git add B.java
git commit -m "Alter file B.java master"
```

9. Escreva uma sequência de comando para mesclar o branch `math` em` master` e descreva o que aconteceu
```
git merge math
O terminal retornou que ocorreu um conflito entre as branchs.
```
   
10. Escreva um conjunto de comandos para abortar a mesclagem
```
git merge --abort
```
   
11. Agora repita o item 9, mas prossiga com a mesclagem manual (Editando B.java). Todas as funções implementadas são necessárias. Explique o seu procedimento
```
Quando ocorrer conflitos o GitHub realiza marcações, assim é só apagar as marcações, ou seja, os conflitos e deixar o conteúdo que quer que permaneça.
```

12. Escreva um comando (ou conjunto de comandos) para prosseguir com a mesclagem e atualizar o branch `master`
```
git add *
git commit -m "resolve conflicts"

Para atualizar a branch após a resolução dos merge conflicts é necessário adicionar as modificações e após isso fazer o commit. 
```
