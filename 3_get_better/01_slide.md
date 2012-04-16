!SLIDE bullets
# GIT better

* Database overview
* Usual commands
* Rebasing
* Tools and advices


!SLIDE bullets
# Database overview

* Repositories
* Commits
* Tags
* Branches


!SLIDE center
# Repositories

## PICTUREME: trees


!SLIDE bullets commandline
# Repositories

* Complete history (local and remotes)
* Any number of remotes
* Commit offline


!SLIDE center
# Commits

## PICTUREME: wood


!SLIDE bullets
# Commits

* Unique non-incremental hash id
* Only what's been added (files, lines)
* Mandatory commit message
* Ref to previous commit


!SLIDE center
# Tags

## PICTUREME: engraving on a tree


!SLIDE bullets
# Tags

* Label referencing a commit
* Well, that's all it's doing


!SLIDE center
# Branches

## PICTUREME: Terminal leaf on a branch


!SLIDE bullets
# Branches

* Label referencing a commit
* Can be selected
* When selected, follows on each commit
* Easy to move around (reset, rebase)


!SLIDE commandline
# Usual commands (1)

Make any directory a git repository
    $ git init
Add a file / directory to the upcoming commit
    $ git add file-or-directory
Commit any current changes with a message
    $ git commit -am "Whatever message"
Adds current changes to the last commit
    $ git commit --amend -a


!SLIDE commandline
# Usual commands (2)

Create a branch (starting at current commit)
    $ git branch the-branch
Get to a branch (and set it as current branch)
    $ git checkout the-branch
Review a specific commit (detached from a branch)
    $ git checkout the-commit-hash-or-tag-name
See current files status (changed, staged, ...)
    $ git status


!SLIDE commandline
# Usual commands (3)

Undo the last commit, keeping changes as if uncommited
    $ git reset HEAD^
Undo the last commit, destroying any changes (commited or not)
    $ git reset --hard HEAD^
Undo current uncommited changes
    $ git reset --hard HEAD
Apply a commit it on top of current branch
    $ git cherry-pick the-commit-hash-branch-or-tag-name


!SLIDE commandline
# Usual commands (4)

Update remote informations
    $ git fetch the-remote
Apply changes from a remote branch
    $ git pull the-remote the-branch
Send changes of a local branch to a remote
    $ git push the-remote the-branch
Set a remote branch to a specific commit
    $ git push the-remote the-reference:the-remote-branch


!SLIDE center
# Rebasing

## PICTUREME: grafting a branch


!SLIDE bullets
# Why not just merge ?

* Atomic changes VS. Different codebases
* Branche's author VS. Repository admin
* Topic branches VS. Blurry master
* Readable history VS. Tangle of commits


!SLIDE center
# Rebase effects

## PICTUREME: rebase before-after


!SLIDE commandline
# How to rebase

Start rebasing on a branch
    $ git rebase the-branch

No conflict ? Lucky you

Conflict ? Edit conflicting files, then
    $ git add conflicting.file
    $ git rebase --continue


!SLIDE bullets
# Tools and advices

* Gui
* Configuration
* Advice


!SLIDE bullets
# Gui

* MacOS:
  * GitX [http://gitx.frim.nl/](http://gitx.frim.nl/)
* Linux:
  * Gitg [http://git.gnome.org/browse/gitg](http://git.gnome.org/browse/gitg)
* Windows:
  * msysgit [http://code.google.com/p/msysgit](http://code.google.com/p/msysgit)
  * TortoiseGit [http://code.google.com/p/tortoisegit/](http://code.google.com/p/tortoisegit/)


!SLIDE commandline
# Configuration

Your references
    $ git config --global user.name "Whoever Youare"
    $ git config --global user.email "whoever.youare@mail.com"

Global ignore file
    $ echo ".DS_Store" >> ~/.gitignore
    $ git config --global core.excludesfile ~/.gitignore


!SLIDE commandline
# Configuration

Color output
    $ git config --global color.branch auto
    $ git config --global color.diff auto
    $ git config --global color.interactive auto
    $ git config --global color.status auto


!SLIDE commandline
# Configuration

Auto-rebase by default
    $ git config --global branch.autosetuprebase always
    $ git config branch.the-branch.rebase true

Default text editor
    $ git config --global core.editor "mate -w"

Merge tool
    $ git config --global merge.tool opendiff


!SLIDE bullets
# Advice

* Keep it atomic
* Make topic branches
* Rebase before merge
* Use fixup! and squash!
* DON'T PANIC
