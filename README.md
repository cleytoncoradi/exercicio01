# exercicio01
Exercícios da aula 2

Cleyton Coradi de Freitas - RA 2402492
@cleytoncoradi ➜ /workspaces/codespaces-blank $ ls
@cleytoncoradi ➜ /workspaces/codespaces-blank $ git config --global cleyton.coradi "Cleyton Coradi"
@cleytoncoradi ➜ /workspaces/codespaces-blank $ git config --global user.name "Cleyton Coradi"
@cleytoncoradi ➜ /workspaces/codespaces-blank $ git config --global user.email "cleyton.coradi@aluno.faculdadeimpacta.com.br"
@cleytoncoradi ➜ /workspaces/codespaces-blank $ mkdir aula
@cleytoncoradi ➜ /workspaces/codespaces-blank $ ls -latr
total 12
drwxr-xrwx+ 5 codespace root      4096 Aug  7 14:52 ..
drwxrwxrwx+ 2 codespace codespace 4096 Aug  7 14:59 aula
drwxrwxrwx+ 3 codespace root      4096 Aug  7 14:59 .
@cleytoncoradi ➜ /workspaces/codespaces-blank $ git init
Initialized empty Git repository in /workspaces/codespaces-blank/.git/
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ ls -latr
total 16
drwxr-xrwx+ 5 codespace root      4096 Aug  7 14:52 ..
drwxrwxrwx+ 2 codespace codespace 4096 Aug  7 14:59 aula
drwxrwxrwx+ 4 codespace root      4096 Aug  7 14:59 .
drwxrwxrwx+ 7 codespace codespace 4096 Aug  7 14:59 .git
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ cd .git
@cleytoncoradi ➜ /workspaces/codespaces-blank/.git (main) $ ls
HEAD  branches  config  description  hooks  info  objects  refs
@cleytoncoradi ➜ /workspaces/codespaces-blank/.git (main) $ git status
fatal: this operation must be run in a work tree
@cleytoncoradi ➜ /workspaces/codespaces-blank/.git (main) $ cd ..
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git status
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)

- Item A
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ echo 01 > arquivo.txt

- Item B
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git add arquivo.txt
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   arquivo.txt

- Item C
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git commit -m "git ad example - aquivo.txt"
[main (root-commit) c6daf8b] git ad example - aquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt
 
 Item D
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ echo 02 > arquivo.txt 
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")

Item E
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

Item F
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git restore --staged arquivo.txt
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

Item F
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff --staged arquivo.txt
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff --staged 
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ 
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff --staged 
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")

Item G
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff .
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git add arquivo.txt 
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff arquivo.txt
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff --staged arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

Item H
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ echo 03 > arquivo.txt

Item I
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

Item J
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git restore --staged arquivo.txt
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git diff arquivo.txt
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+03

Item K
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git commimt -m "Tarefa K"
git: 'commimt' is not a git command. See 'git --help'.

The most similar command is
        commit
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git commit -m "Tarefa K"
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git log
commit c6daf8be42e242ea7aff2d981af6934914b57261 (HEAD -> main)
Author: Cleyton Coradi <cleyton.coradi@aluno.faculdadeimpacta.com.br>
Date:   Wed Aug 7 15:07:19 2024 +0000

    git ad example - aquivo.txt

Item L
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ echo "*.txt" > .gitignore
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ ls -latr
total 24
drwxr-xrwx+ 5 codespace root      4096 Aug  7 14:52 ..
drwxrwxrwx+ 2 codespace codespace 4096 Aug  7 14:59 aula
-rw-rw-rw-  1 codespace codespace    3 Aug  7 15:17 arquivo.txt
drwxrwxrwx+ 8 codespace codespace 4096 Aug  7 15:20 .git
-rw-rw-rw-  1 codespace codespace    6 Aug  7 15:27 .gitignore
drwxrwxrwx+ 4 codespace root      4096 Aug  7 15:27 .
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ cat .git
.git/       .gitignore  
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ cat .git
.git/       .gitignore  
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ cat .git
.git/       .gitignore  
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ cat .gitignore 
*.txt
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git add .gitignore
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git commit -m "Adicionando arquivo gitignore"
[main bc204a5] Adicionando arquivo gitignore
 1 file changed, 1 insertion(+)
 create mode 100644 .gitignore
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ ls
arquivo.txt  aula
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ ls -latr
total 24
drwxr-xrwx+ 5 codespace root      4096 Aug  7 14:52 ..
drwxrwxrwx+ 2 codespace codespace 4096 Aug  7 14:59 aula
-rw-rw-rw-  1 codespace codespace    3 Aug  7 15:17 arquivo.txt
-rw-rw-rw-  1 codespace codespace    6 Aug  7 15:27 .gitignore
drwxrwxrwx+ 4 codespace root      4096 Aug  7 15:27 .
drwxrwxrwx+ 8 codespace codespace 4096 Aug  7 15:31 .git

Item M
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ echo Novo > novo.txt
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ ls -latr
total 28
drwxr-xrwx+ 5 codespace root      4096 Aug  7 14:52 ..
drwxrwxrwx+ 2 codespace codespace 4096 Aug  7 14:59 aula
-rw-rw-rw-  1 codespace codespace    3 Aug  7 15:17 arquivo.txt
-rw-rw-rw-  1 codespace codespace    6 Aug  7 15:27 .gitignore
drwxrwxrwx+ 8 codespace codespace 4096 Aug  7 15:31 .git
-rw-rw-rw-  1 codespace codespace    5 Aug  7 15:33 novo.txt
drwxrwxrwx+ 4 codespace root      4096 Aug  7 15:33 .
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git status
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")
@cleytoncoradi ➜ /workspaces/codespaces-blank (main) $ git add novo.txt 
The following paths are ignored by one of your .gitignore files:
novo.txt
hint: Use -f if you really want to add them.
hint: Disable this message with "git config advice.addIgnoredFile false"
