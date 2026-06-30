# Git Exercise
## Bundle 1
### Exercise 1

```bash

PS D:\documents\TheGym\Content\Git\Exercises> git branch
PS D:\documents\TheGym\Content\Git\Exercises> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

nothing added to commit but untracked files present (use "git add" to track)
PS D:\documents\TheGym\Content\Git\Exercises> git branch -M main
PS D:\documents\TheGym\Content\Git\Exercises> git status        
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        index.html

nothing added to commit but untracked files present (use "git add" to track)
PS D:\documents\TheGym\Content\Git\Exercises> git add index.html
PS D:\documents\TheGym\Content\Git\Exercises> git status
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   index.html

PS D:\documents\TheGym\Content\Git\Exercises> git commit -m "create the index.html file with some content."
[main (root-commit) c1a52d7] create the index.html file with some content.
 1 file changed, 11 insertions(+)
 create mode 100644 index.html
PS D:\documents\TheGym\Content\Git\Exercises> git remote add origin https://github.com/Gengachris/Gym-Git-Exercise-Solutions.git
PS D:\documents\TheGym\Content\Git\Exercises> git pull origin main
From https://github.com/Gengachris/Gym-Git-Exercise-Solutions
 * branch            main       -> FETCH_HEAD
fatal: refusing to merge unrelated histories
PS D:\documents\TheGym\Content\Git\Exercises> git push -u origin main -f
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 397 bytes | 397.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/Gengachris/Gym-Git-Exercise-Solutions.git
 + cd09931...c1a52d7 main -> main (forced update)
branch 'main' set up to track 'origin/main'.
PS D:\documents\TheGym\Content\Git\Exercises> git switch -c dev
Switched to a new branch 'dev'
PS D:\documents\TheGym\Content\Git\Exercises> git branch test
PS D:\documents\TheGym\Content\Git\Exercises> git switch dev
Already on 'dev'
PS D:\documents\TheGym\Content\Git\Exercises> git switch test
Switched to branch 'test'
PS D:\documents\TheGym\Content\Git\Exercises> git switch dev 
Switched to branch 'dev'
PS D:\documents\TheGym\Content\Git\Exercises> git branch -d test
Deleted branch test (was c1a52d7).
PS D:\documents\TheGym\Content\Git\Exercises> 

```
