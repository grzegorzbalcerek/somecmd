git
* git-scm.com
```text
/etc/gitconfig # --system # MSys root/etc/gitconfig
~/.gitconfig # --global
.gitignore
EDITOR
GIT_EDITOR
```

```bash
git config --list
git config --global alias.aa 'add --all'
git config --global alias.cam 'commit --amend -m'
git config --global alias.camd 'commit --amend -m $(date +%F)'
git config --global alias.cm 'commit -m'
git config --global alias.cmd 'commit -m $(date +%F)'
git config --global alias.co 'checkout'
git config --global alias.d 'diff'
git config --global alias.lo 'log --oneline'
git config --global alias.loa 'log --oneline --graph --all --decorate'
git config --global alias.p 'push'
git config --global alias.pf 'push --force'
git config --global alias.s 'status'
git config --global user.email 'email@some.domain'
git config --global user.name 'some.name'
git config --global core.editor emacs
```

```bash
git help status
git status --help
man git status
man git-status
```

```bash
git init
git add readme.md
git commit -m add.readme.md
git remote add origin https://github.com/grzegorzbalcerek/somecmd
git push -u origin master
git push --set-upstream origin master
```
```bash
git clone https:#github.com/grzegorzbalcerek/somecmd
git clone https:#github.com/grzegorzbalcerek/somecmd somecmd2
```
```bash
git status
git status -s
git add .
git add --all
git diff
git diff --staged
git diff --cached
git branch
git branch -D branch-to-be-deleted-locally
git checkout -b branch
git clone https:#github.com/outr/scribe
git commit --amend -m message
git commit -m message
git commit some.path
git commit -m message --author some.author --date some.date
git push
git push --delete origin branch-or-tag-to-be-deleted-remotely
git push --force
git push --tags
git rebase master --interactive
git status
git tag new-tag
git reflog
git show master@{yesterday}
git rm file.name
git rm --cached file.name
git rm log/\*.log
git rm \*~
```
```bash
git add -p
git log -g master
git show HEAD^
git show abcd123^2
git show HEAD~3 == git show HEAD^^^
git log origin/master..HEAD
git log A ^B # reacheable by A ale not by B
git log A..B == git log ^A B == git log B --not A
git log A...B
git log --left-right A...B
git branch # lists branches
git branch mybranch # create new branch (pointer)
git checkout mybranch # moves HEAD to point to mybranch and update the working dir
git checkout # switch between branches
git checkout -b mybranch # == git branch+checkout
git checkout -b mybranch master
git branch --merged # gałęzie już merged (można je skasować)
git branch --no-merged # gałęzie jeszcze nie merged
git merge mybranch
git branch -d mybranch # delete a branch
git branch -D mybranch # delete a branch nawet jeśli nie jest merged
git branch -r
git push
git fetch
git pull
git log
git log mybranch
git log --oneline
git log --oneline --graph --all --decorate
git log A ^B # reacheable by A ale not by B
git log -p
git log --stat
git log --stat --no-merges
git diff # unstaged
git diff --staged
git log
git log path
git log revision # start at a given revision
git log --patch  # -p # show diff for each commit output
git log --stat
git log --word-diff
git diff master~1 master
git diff master~1..master
git diff master~1 master -- path
git diff
git diff master
git diff --stat master~1 master
git diff --word-diff master~1 master
git rev-parse master
git remote --verbose
git remote rename
git remote remove
git remote show
git remote prune
```

```text
master
63e8fa
ref~1
ref~2
ref^
ref^^
HEAD
```