\# Step 2: Initial Status

On branch master

Untracked files:

&#x20; (use "git add <file>..." to include in what will be committed)

&#x09;part1/

&#x09;status\_log.md



nothing added to commit but untracked files present (use "git add" to track)

\# Step 3: Staged notes and todo

On branch master

Changes to be committed:

&#x20; (use "git restore --staged <file>..." to unstage)

&#x09;new file:   part1/notes.txt

&#x09;new file:   part1/todo.txt



Untracked files:

&#x20; (use "git add <file>..." to include in what will be committed)

&#x09;part1/draft.md

&#x09;status\_log.md

\# Step 5: Unstaged Diff

diff --git a/part1/notes.txt b/part1/notes.txt

index e69de29..5627fb9 100644

\--- a/part1/notes.txt

+++ b/part1/notes.txt

@@ -0,0 +1,3 @@

+Line 1: My first note

+Line 2: My second note

+Line 3: My third note



\# Step 5: Staged Diff

diff --git a/part1/notes.txt b/part1/notes.txt

index e69de29..5627fb9 100644

\--- a/part1/notes.txt

+++ b/part1/notes.txt

@@ -0,0 +1,3 @@

+Line 1: My first note

+Line 2: My second note

+Line 3: My third note



\# Step 6: Explanation of git commit -a

Lệnh `git commit -a` tự động đưa các thay đổi của những file đã được theo dõi (tracked files) vào staging area và thực hiện commit ngay. Nó không có tác dụng với các file mới chưa được theo dõi (untracked files) vì Git chưa lưu thông tin về chúng trong index.

