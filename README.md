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

## Bundle 3

### Exercise 1

```bash

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git add team.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git commit -m "Additional page of team"   
[ft/team-page 48e2a61] Additional page of team
 1 file changed, 16 insertions(+)
 create mode 100644 team.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git push 
fatal: The current branch ft/team-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/team-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git push --set-upstream ft/team-page
fatal: 'ft/team-page' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git push --set-upstream origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads     
Compressing objects: 100% (3/3), done.      
Writing objects: 100% (3/3), 477 bytes | 238.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote:
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      ft/team-page -> ft/teamremote:
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      ft/team-page -> ft/team-page
branch 'ft/team-page' set up to track 'origin/ft/team-page'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git checkout main 
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git checkout ft/contact-page
error: pathspec 'ft/contact-page' did not match any file(s) known to git

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.
commit 48e2a6127c58337efb29c845efefba9ff0d40818 (HEAD -> ft/team-page, origin/ft/team-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:09:56 2024 +0200

    Additional page of team

commit fd56d50fc146f887de79a431086410af5afd4a70 (origin/ft/service-redesign, ft/service-redesign)
Merge: 216fdd1 0be0c32
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 16:58:21 2024 +0200

    Merge branch 'main' into ft/service-redesign


    Merge branch 'main' into ft/service-redesign

commit 0be0c323511a2d30e992dc2e679c525c5618f99f (origin/main, main, ft/contact-page)    
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 16:38:03 2024 +0200      

    Additional changes within one file      

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git checkout -b ft/contact-page
fatal: a branch named 'ft/contact-page' already exists

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git cherry-pick
usage: git cherry-pick [--edit] [-n] [-m <parent-number>] [-s] [-x] [--ff]
                       [-S[<keyid>]] <commit>...
   or: git cherry-pick (--continue | --skip | --abort | --quit)

    --quit                end revert or cherry-pick sequence
    --continue            resume revert or cherry-pick sequence
    --abort               cancel revert or cherry-pick sequence
    --skip                skip current commit and continue
    --[no-]cleanup <mode> how to strip spaces and #comments from message
    -n, --no-commit       don't automatically commit
    --commit              opposite of --no-commit
    -e, --[no-]edit       edit the commit message
    -s, --[no-]signoff    add a Signed-off-by trailer
    -m, --[no-]mainline <parent-number>     
                          select mainline parent
    --[no-]rerere-autoupdate
                          update the index with reused conflict resolution if possible  
    --[no-]strategy <strategy>
                          merge strategy    
    -X, --[no-]strategy-option <option>     
                          option for merge strategy
    -S, --[no-]gpg-sign[=<key-id>]
                          GPG sign commit   
    --[no-]allow-empty-message
                          allow commits with empty messages
    --[no-]keep-redundant-commits
                          keep redundant, empty commits


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git cherry pick 0be0c323511a2d30e992dc2e679c525c5618f99f
fatal: unknown commit pick

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git cherry pick fd56d50fc146f887de79a431086410af5afd4a70
fatal: unknown commit pick

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git cherry-pick fd56d50fc146f887de79a431086410af5afd4a70
error: commit fd56d50fc146f887de79a431086410af5afd4a70 is a merge but no -m option was given.
fatal: cherry-pick failed

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git cherry-pick fd56d50fc146f887de79a431086410af5afd4a70
error: commit fd56d50fc146f887de79a431086410af5afd4a70 is a merge but no -m option was given.
fatal: cherry-pick failed

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git log
commit 0be0c323511a2d30e992dc2e679c525c5618f99f (HEAD -> ft/contact-page, origin/main, main)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 16:38:03 2024 +0200

    Additional changes within one file

commit 5c724e9438e643037dceb3a5b5d254acaa8411fa
Merge: 3b1d35a 98d1fa2
Author: uwumukiza123 <113632531+uwumukiza123@users.noreply.github.com>
Date:   Mon Apr 22 16:16:19 2024 +0200

    Merge pull request #1 from DevRamona/ft/bundle-2

    Added new HTML files.

commit 98d1fa2819e90c5740dfcf0a4e03391dfc646712 (origin/ft/bundle-2, ft/bundle-2)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 15:59:39 2024 +0200

    new changes added

commit 0f3d5b628d62fbef02e5bd5d6925a5754d7a7f11 (origin/dev, dev)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 15:41:13 2024 +0200

    Added the home and about

commit 3b1d35a89fbe93c81322f0bde42f24ee23ac6a15
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 12:33:11 2024 +0200

    A file has been added

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
Your branch is up to date with 'origin/ft/team-page'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git log
commit 48e2a6127c58337efb29c845efefba9ff0d40818 (HEAD -> ft/team-page, origin/ft/team-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:09:56 2024 +0200

    Additional page of team

commit fd56d50fc146f887de79a431086410af5afd4a70 (origin/ft/service-redesign, ft/service-redesign)
Merge: 216fdd1 0be0c32
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 16:58:21 2024 +0200

    Merge branch 'main' into ft/service-redesign

commit 0be0c323511a2d30e992dc2e679c525c5618f99f (origin/main, main, ft/contact-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 16:38:03 2024 +0200

    Additional changes within one file

commit 216fdd1ab5e231fb94ecf68d14356854eb58bde3
Author: DevRamona <r.ingabire@alustudent.com>

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git cherry-pick 48e2a6127c58337efb29c845efefba9ff0d40818
[ft/contact-page 2ea66aa] Additional page of team
 Date: Mon Apr 22 17:09:56 2024 +0200
 1 file changed, 16 insertions(+)
 create mode 100644 team.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git log
commit 2ea66aa7fb64b3a16eeaa4ab51dd773182beac39 (HEAD -> ft/contact-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:09:56 2024 +0200

    Additional page of team

commit 0be0c323511a2d30e992dc2e679c525c5618f99f (origin/main, main)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 16:38:03 2024 +0200

    Additional changes within one file

commit 5c724e9438e643037dceb3a5b5d254acaa8411fa
Merge: 3b1d35a 98d1fa2
Author: uwumukiza123 <113632531+uwumukiza123@users.noreply.github.com>
Date:   Mon Apr 22 16:16:19 2024 +0200

    Merge pull request #1 from DevRamona/ft/bundle-2

    Added new HTML files.


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git add .

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git commit -m "Added a new file for the contact"
[ft/contact-page ca107e2] Added a new file for the contact
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git push 
fatal: The current branch ft/contact-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/contact-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git push --set-upstream origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 772 bytes | 85.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/DevRamona/gitStarted/pull/new/ft/contact-page
remote:
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      ft/contact-page -> ft/contact-page
branch 'ft/contact-page' set up to track 'origin/ft/contact-page'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/contact-page)
$ git checkout -b ft/faq-page
Switched to a new branch 'ft/faq-page'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git add .

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git commit -m "Created a new page for FAQ"
[ft/faq-page 50d9077] Created a new page for FAQ
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git push 
fatal: The current branch ft/faq-page has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/faq-page

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git push --set-upstream origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 447 bytes | 223.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/DevRamona/gitStarted/pull/new/ft/faq-page
remote:
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      ft/faq-page -> ft/faq-page
branch 'ft/faq-page' set up to track 'origin/ft/faq-page'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git log
commit 50d90771a0dc3d1bc48c0b07caa861c11a15e988 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:49:10 2024 +0200

    Created a new page for FAQ

commit ca107e201c9cc1946e9636e86b3e2c0cfccf623d (origin/ft/contact-page, ft/contact-page)
Author: DevRamona <r.ingabire@alustudent.com>
Revert "Additional page of team"
Date:   Mon Apr 22 17:43:53 2024 +0200

    Added a new file for the contact

commit 2ea66aa7fb64b3a16eeaa4ab51dd773182beac39
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:09:56 2024 +0200

    Additional page of team


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git revert fd56d50fc146f887de79a431086410af5afd4a70
error: commit fd56d50fc146f887de79a431086410af5afd4a70 is a merge but no -m option was given.
fatal: revert failed

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git revert 48e2a6127c58337efb29c845efefba9ff0d40818
[ft/faq-page a83204f] Revert "Additional page of team"
 1 file changed, 16 deletions(-)
 delete mode 100644 team.html

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git push 
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 280 bytes | 280.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/DevRamona/gitStarted.git
   50d9077..a83204f  ft/faq-page -> ft/faq-page

   ```

   ### Exercise 2

   ```  bash

   ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git checkout -b ft/home-page-redesign

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git add .

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git commit -m "Additional pages have been added"
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git add .

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git commit -m "Additional pages have been added"
[main bd888d6] Additional pages have been added
 1 file changed, 1 insertion(+)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git log 
commit bd888d65e40ec601726907e0fa613e6eb3f16cad (HEAD -> main)
commit bd888d65e40ec601726907e0fa613e6eb3f16cad (HEAD -> main)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 19:33:21 2024 +0200

    Additional pages have been added

commit 0be0c323511a2d30e992dc2e679c525c5618f99f (origin/main)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 16:38:03 2024 +0200

    Additional changes within one file

commit 5c724e9438e643037dceb3a5b5d254acaa8411fa
Merge: 3b1d35a 98d1fa2
Author: uwumukiza123 <113632531+uwumukiza123@users.noreply.github.com>
Date:   Mon Apr 22 16:16:19 2024 +0200

    Merge pull request #1 from DevRamona/ft/bundle-2

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git push 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 342 bytes | 171.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/DevRamona/gitStarted.git
   0be0c32..bd888d6  main -> main

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git log 
commit bd888d65e40ec601726907e0fa613e6eb3f16cad (HEAD -> main, origin/main)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 19:33:21 2024 +0200

    Additional pages have been added

commit 0be0c323511a2d30e992dc2e679c525c5618f99f
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 16:38:03 2024 +0200

    Additional changes within one file

commit 5c724e9438e643037dceb3a5b5d254acaa8411fa
Merge: 3b1d35a 98d1fa2
Author: uwumukiza123 <113632531+uwumukiza123@users.noreply.github.com>
Date:   Mon Apr 22 16:16:19 2024 +0200

    Merge pull request #1 from DevRamona/ft/bundle-2

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git rebase main
Current branch main is up to date.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git log 
commit bd888d65e40ec601726907e0fa613e6eb3f16cad (HEAD -> main, origin/main)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 19:33:21 2024 +0200

    Additional pages have been added

commit 0be0c323511a2d30e992dc2e679c525c5618f99f
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 16:38:03 2024 +0200

    Additional changes within one file

commit 5c724e9438e643037dceb3a5b5d254acaa8411fa
Merge: 3b1d35a 98d1fa2
Author: uwumukiza123 <113632531+uwumukiza123@users.noreply.github.com>
Date:   Mon Apr 22 16:16:19 2024 +0200

    Merge pull request #1 from DevRamona/ft/bundle-2

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git add .

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git commit -m "Added a new paragraph within the home"
[main 722bfc3] Added a new paragraph within the home
 1 file changed, 14 insertions(+), 8 deletions(-)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git push 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 620 bytes | 620.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/DevRamona/gitStarted.git
   bd888d6..722bfc3  main -> main

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git checkout ft/home-page-redesign
Switched to branch 'ft/home-page-redesign'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git log
commit a83204f45835133044631bdc379790791fe29657 (HEAD -> ft/home-page-redesign, origin/ft/faq-page, ft/faq-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:57:42 2024 +0200

    Revert "Additional page of team"

    This reverts commit 48e2a6127c58337efb29c845efefba9ff0d40818.

commit 50d90771a0dc3d1bc48c0b07caa861c11a15e988
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:49:10 2024 +0200

    Created a new page for FAQ

commit ca107e201c9cc1946e9636e86b3e2c0cfccf623d (origin/ft/contact-page, ft/contact-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:43:53 2024 +0200


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git status 
On branch ft/home-page-redesign
nothing to commit, working tree clean

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git log
commit a83204f45835133044631bdc379790791fe29657 (HEAD -> ft/home-page-redesign, origin/ft/faq-page, ft/faq-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:57:42 2024 +0200

    Revert "Additional page of team"

    This reverts commit 48e2a6127c58337efb29c845efefba9ff0d40818.

commit 50d90771a0dc3d1bc48c0b07caa861c11a15e988
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:49:10 2024 +0200

    Created a new page for FAQ

commit ca107e201c9cc1946e9636e86b3e2c0cfccf623d (origin/ft/contact-page, ft/contact-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:43:53 2024 +0200


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git rebase main 
Successfully rebased and updated refs/heads/ft/home-page-redesign.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git log
commit 1fc15577716c8573298a4dd14539556a9055575b (HEAD -> ft/home-page-redesign)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:57:42 2024 +0200

    Revert "Additional page of team"

    This reverts commit 48e2a6127c58337efb29c845efefba9ff0d40818.

commit ffb23cfac15767345f3a973f0d6b0e28ac5f9157
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:49:10 2024 +0200

    Created a new page for FAQ

commit 39289253702334d3d552ba737d0701ea6308ddfc
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:43:53 2024 +0200


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git add .

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git commit -m "Added a new paragraph within the home"
[ft/home-page-redesign 2872586] Added a new paragraph within the home
 1 file changed, 4 insertions(+)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git push
fatal: The current branch ft/home-page-redesign has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin ft/home-page-redesign

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git push --set-upstream origin ft/home-page-redesign
Enumerating objects: 16, done.
Counting objects: 100% (16/16), done.
Delta compression using up to 4 threads
Compressing objects: 100% (14/14), done.
Writing objects: 100% (14/14), 1.76 KiB | 899.00 KiB/s, done.
Total 14 (delta 7), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (7/7), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/home-page-redesign' on GitHub by visiting:
remote:      https://github.com/DevRamona/gitStarted/pull/new/ft/home-page-redesign
remote:
To https://github.com/DevRamona/gitStarted.git
 * [new branch]      ft/home-page-redesign -> ft/home-page-redesign
branch 'ft/home-page-redesign' set up to track 'origin/ft/home-page-redesign'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/home-page-redesign)
$ git checkout ft/faq-page 
Switched to branch 'ft/faq-page'
Your branch is up to date with 'origin/ft/faq-page'.

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git log 
commit a83204f45835133044631bdc379790791fe29657 (HEAD -> ft/faq-page, origin/ft/faq-page)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:57:42 2024 +0200

    Revert "Additional page of team"

    This reverts commit 48e2a6127c58337efb29c845efefba9ff0d40818.

commit 50d90771a0dc3d1bc48c0b07caa861c11a15e988
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:49:10 2024 +0200

    Created a new page for FAQ

commit ca107e201c9cc1946e9636e86b3e2c0cfccf623d (origin/ft/contact-page, ft/contact-page)
Merge branch 'main' into f/merge
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 17:43:53 2024 +0200


ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (ft/faq-page)
$ git checkout -b f/merge
Switched to a new branch 'f/merge'

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (f/merge)
$ git status
On branch f/merge
nothing to commit, working tree clean

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (f/merge)
$ git merge main
Merge made by the 'ort' strategy.
 home.html | 23 +++++++++++++++--------
 1 file changed, 15 insertions(+), 8 deletions(-)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (f/merge)
$ git log
commit 2b7be94f37457a37e971368c96827f567a289d0c (HEAD -> f/merge)
Merge: a83204f 722bfc3
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 20:14:09 2024 +0200

    Merge branch 'main' into f/merge

commit 722bfc3c59d411b8155ac0e162ad6041d31b2ebe (origin/main, main)
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 19:58:07 2024 +0200

    Added a new paragraph within the home

commit bd888d65e40ec601726907e0fa613e6eb3f16cad
Author: DevRamona <r.ingabire@alustudent.com>
Date:   Mon Apr 22 19:33:21 2024 +0200

    Additional pages have been added

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (f/merge)
 
 ```

 ## Bundle 4 


 ### Exercise 1 

 ``` bash
 ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git remote add git-copy https://github.com/DevRamona/gitBundle4.git

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git remote 
git-copy
origin

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git add .

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git commit -m "Added a new heading"
[main 54bbdb9] Added a new heading
 1 file changed, 1 insertion(+)

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git push origin 
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 343 bytes | 171.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.   
To https://github.com/DevRamona/gitStarted.git
   722bfc3..54bbdb9  main -> main

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

ingab@DESKTOP-13J8UH7 MINGW64 ~/Desktop/git_exercises (main)
$ git push git-copy
Enumerating objects: 23, done.
Counting objects: 100% (23/23), done.
Delta compression using up to 4 threads
Compressing objects: 100% (22/22), done.
Writing objects: 100% (23/23), 3.29 KiB | 374.00 KiB/s, done.
Total 23 (delta 10), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (10/10), done.
To https://github.com/DevRamona/gitBundle4.git
 * [new branch]      main -> main

```