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