# exercicio01

a) No working dir comando "echo 01 > arquivo.txt"
b) Adicionando o arquivo no staging e conferir o status com os comandos "git add arquivo.txt" e "git status", resultado:
On branch main
Your branch is up to date with 'origin/main'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   arquivo.txt

c) comando  git commit -m "git add example - arquivo.txt"
[main dc8c8c4] git add example - arquivo.txt
 1 file changed, 1 insertion(+)
 create mode 100644 arquivo.txt

d) Comando "echo 02 > arquivo.txt"
e) Comando "git diff arquivo.txt", resultado:
diff --git a/arquivo.txt b/arquivo.txt
index 8a0f05e..9e22bcb 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-01
+02

f) Comando "git add arquivo.txt" e "git status", resultado:
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   arquivo.txt

g) Comando "git diff arquivo.txt"
h) Comando "echo 03 > arquivo.txt"
i) Comando "git diff arquivo.txt", resultado:
diff --git a/arquivo.txt b/arquivo.txt
index 9e22bcb..75016ea 100644
--- a/arquivo.txt
+++ b/arquivo.txt
@@ -1 +1 @@
-02
+03

j) Comando "git restore --staged arquivo.txt" e "git status", resultado:
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   arquivo.txt

no changes added to commit (use "git add" and/or "git commit -a")

k) Realização do commit e verificar log "git add arquivo.txt", "git commit -m "arquivo restaurado"", resultado do commit:
[main e5a00c6] arquivo restaurado
 1 file changed, 1 insertion(+), 1 deletion(-)

continuação k) Comando "git log", resultado:
commit e5a00c6e522e40f7b96aca91f4c0c0c96efe941b (HEAD -> main)
Author: Eduardo Abreu <edu.abreu09@hotmail.com>
Date:   Fri Aug 2 01:32:16 2024 +0000

    arquivo restaurado

commit dc8c8c42d468ddcca4846f520a0aec8ac0e0a385
Author: Eduardo Abreu <edu.abreu09@hotmail.com>
Date:   Fri Aug 2 01:30:03 2024 +0000

    git add example - arquivo.txt

commit f8de9cceacde071db3bdc0806271e01f25e4d51d (origin/main, origin/HEAD)
Author: Eduhkbr <47605719+Eduhkbr@users.noreply.github.com>
Date:   Thu Aug 1 18:09:49 2024 -0300

    Initial commit
i) Adicionar um arquivo gitignore "nano .gitignore"
m) Criar um arquivo novo.txt e verificar o status "echo "novo conteudo" > teste.txt"
"git status"
On branch main
Your branch is ahead of 'origin/main' by 2 commits.
  (use "git push" to publish your local commits)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .gitignore

nothing added to commit but untracked files present (use "git add" to track)