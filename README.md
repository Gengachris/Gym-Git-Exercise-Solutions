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






### Exercise 2

```bash

PS D:\documents\TheGym\Content\Git\Exercises> git status                                 
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.html

nothing added to commit but untracked files present (use "git add" to track)
PS D:\documents\TheGym\Content\Git\Exercises> git stash push -m "creating the home page."
No local changes to save
PS D:\documents\TheGym\Content\Git\Exercises> git add home.html                          
PS D:\documents\TheGym\Content\Git\Exercises> git status
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   home.html

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   home.html

PS D:\documents\TheGym\Content\Git\Exercises> git stash push -m "added the new paragraph."
Saved working directory and index state On dev: added the new paragraph.
PS D:\documents\TheGym\Content\Git\Exercises> git add about.html                          
PS D:\documents\TheGym\Content\Git\Exercises> git stash push -m "added the new list in about.html file."     
Saved working directory and index state On dev: added the new list in about.html file.
PS D:\documents\TheGym\Content\Git\Exercises> git stash list
stash@{0}: On dev: added the new list in about.html file.
stash@{1}: On dev: added the new paragraph.
PS D:\documents\TheGym\Content\Git\Exercises> git add team.html                                         
PS D:\documents\TheGym\Content\Git\Exercises> git stash push -m "added the new team member in team.html file." 
Saved working directory and index state On dev: added the new team member in team.html file.
PS D:\documents\TheGym\Content\Git\Exercises> git stash list
stash@{0}: On dev: added the new team member in team.html file.
stash@{1}: On dev: added the new list in about.html file.
stash@{2}: On dev: added the new paragraph.
PS D:\documents\TheGym\Content\Git\Exercises> git stash pop stash@{1}
error: unknown switch `e'
usage: git stash pop [--index] [-q | --quiet] [<stash>]

    -q, --[no-]quiet      be quiet, only report errors
    --[no-]index          attempt to recreate the index

PS D:\documents\TheGym\Content\Git\Exercises> git stash pop "stash@{1}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (01a388edbcd0b38c9ebae740ed75afdabaab9a6c)
PS D:\documents\TheGym\Content\Git\Exercises> git stash list           
stash@{0}: On dev: added the new team member in team.html file.
stash@{1}: On dev: added the new paragraph.
PS D:\documents\TheGym\Content\Git\Exercises> git stash pop "stash@{1}"
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (87dccdc5db4f1f2eddc44c65ea67d62f6ba15b34)
PS D:\documents\TheGym\Content\Git\Exercises> git commit -m "adding about and home files"
[dev b9f0553] adding about and home files
 2 files changed, 29 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
PS D:\documents\TheGym\Content\Git\Exercises> git stash list                             
stash@{0}: On dev: added the new team member in team.html file.
PS D:\documents\TheGym\Content\Git\Exercises> git stash pop                              
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (1c1b4570f7351e8e47ef76343eeb130a8f8c5dd7)
PS D:\documents\TheGym\Content\Git\Exercises> git reset HEAD team.html
PS D:\documents\TheGym\Content\Git\Exercises> git status
On branch dev
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        team.html

nothing added to commit but untracked files present (use "git add" to track)
PS D:\documents\TheGym\Content\Git\Exercises> 




```
