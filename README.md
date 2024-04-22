# Git Exercises

## Bundle 1

### Exercise 1

``` bash
ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop
$ mkdir git_exercises

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop
$ cd git_exercises

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises
$ git init
Initialized empty Git repository in C:/Users/ingab/Desktop/git_exercises/.git/

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (master)
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (master)
$ vi README.md

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (master)
$ rm -r README.md

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (master)
$ ls

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (master)
$ git branch -m main

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ vi README.md

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ ls
README.md

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git add README.md
warning: in the working copy of 'README.md', LF will be replaced by CRLF the next time Git touches it

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git commit -m "A file has been added"
[main (root-commit) 3b1d35a] A file has been added
 1 file changed, 1 insertion(+)
 create mode 100644 README.md

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git remote add https://github.com/DevRamona/gitStarted.git
usage: git remote add [<options>] <name> <url>

    -f, --[no-]fetch      fetch the remote branches
    --[no-]tags           import all tags and associated objects when fetching
                          or do not fetch any tag at all (--no-tags)
    -t, --[no-]track <branch>
                          branch(es) to track
    -m, --[no-]master <branch>
                          master branch
    --[no-]mirror[=(push|fetch)]
                          set up remote as a mirror to push to or fetch from


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git remote add origin https://github.com/DevRamona/gitStarted.git

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git push --set-upstream origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (3/3), 276 bytes | 276.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git checkout b dev
error: pathspec 'b' did not match any file(s) known to git
error: pathspec 'dev' did not match any file(s) known to git

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git checkout -b dev
Switched to a new branch 'dev'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git status
On branch dev
nothing to commit, working tree clean

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git branch
* dev
  main

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git push origin dev
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/DevRamona/gitStarted/pull/new/dev
remote:
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      dev -> dev

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git checkout -b test
Switched to a new branch 'test'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (test)
$ git push origin test
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
remote: Create a pull request for 'test' on GitHub by visiting:
remote:      https://github.com/DevRamona/gitStarted/pull/new/test
remote:
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      test -> test

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (test)
$ git checkout dev
Switched to branch 'dev'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git branch -d test
Deleted branch test (was 3b1d35a).

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git push origin --delete test
To https://github.com/DevRamona/gitStarted.git
 - [deleted]         test

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$
```

### Exercise 2 
``` bash 
ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git add home.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash save "home stash"
Saved working directory and index state On dev: home stash

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash list 
stash@{0}: On dev: home stash

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git add about.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash save "about stash"
Saved working directory and index state On dev: about stash

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash list 
stash@{0}: On dev: about stash
stash@{1}: On dev: home stash

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git add home.html 

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash save "home1.html"
Saved working directory and index state On dev: home1.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash list 
stash@{0}: On dev: home1.html
stash@{1}: On dev: about stash
stash@{2}: On dev: home stash

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git add team.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash save "team stash"
Saved working directory and index state On dev: team stash

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash list 
stash@{0}: On dev: team stash
stash@{1}: On dev: home1.html
stash@{2}: On dev: about stash
stash@{3}: On dev: home stash

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash pop stash@{2}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{2} (1c021d4f1fbddc7b8cb045c23801b422bd812452)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git status 
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (e77744db5b22d148885bfe6fa5d430c8babfc110)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git commit -m "Added the home and about"
[dev 0f3d5b6] Added the home and about
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git push --set-upstream origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 529 bytes | 176.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), done.
To https://github.com/DevRamona/gitStarted.git
   3b1d35a..0f3d5b6  dev -> dev
branch 'dev' set up to track 'origin/dev'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git stash pop 
On branch dev
Your branch is up to date with 'origin/dev'.

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (29cad467e24e5dbc0d837557e6e2cd0e4f21a949)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git reset --hard
HEAD is now at 0f3d5b6 Added the home and about

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git status
On branch dev
Your branch is up to date with 'origin/dev'.

nothing to commit, working tree clean
```


## Bundle 2

### Exercise 1

```bash

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (dev)
$ git checkout -b ft/bundle-2
Switched to a new branch 'ft/bundle-2'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/bundle-2)
$ git add .

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/bundle-2)
$ git commit -m "new changes added"
[ft/bundle-2 98d1fa2] new changes added
 1 file changed, 12 insertions(+)
 create mode 100644 services.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/bundle-2)
$ git push --set-upstream origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 472 bytes | 472.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/DevRamona/gitStarted/pull/new/ft/bundle-2
remote:
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2
branch 'ft/bundle-2' set up to track 'origin/ft/bundle-2'.
```

### Exercise 2 

``` bash
ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git checkout -b ft/service-redesign       
Switched to a new branch 'ft/service-redesign'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/service-redesign)
$ git add services.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/service-redesign)
$ git commit -m "New changes added to the service page"
[ft/service-redesign 216fdd1] New changes added to the service page
 1 file changed, 2 insertions(+)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/DevRamona/gitStarted/pull/new/ft/service-redesign
remote:
To https://github.com/DevRamona/gitStarted.gremote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/DevRamona/gitStarted/pull/new/ft/service-redesign       
remote:
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/service-redesign)
$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git add services.html 

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git commit -m "Additional changes within o
ne file"
[main 0be0c32] Additional changes within one file
 1 file changed, 2 insertions(+)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git push 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads     
Compressing objects: 100% (3/3), done.      
Writing objects: 100% (3/3), 353 bytes | 353.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/DevRamona/gitStarted.git
Your branch is up to date with 'origin/ft/service-redesign'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/service-redesign)
Merge branch 'main' into ft/service-redesign
$  git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/service-redesign|MERGING)
$ git add services.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/service-redesign|MERGING)
$ git commit
[ft/service-redesign fd56d50] Merge branch 'main' into ft/service-redesign

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/service-redesign)
$ git push 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 396 bytes | 132.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/DevRamona/gitStarted.git
   216fdd1..fd56d50  ft/service-redesign -> ft/service-redesign

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/service-redesign)
$
``` 