!SLIDE bullets
# SVN VS. GIT #

* Network addiction VS. Full local repository
* Fossile history VS. Live history
* Merge VS. Rebase
* Expensive branches VS. Free branches
* Directory centric VS. File centric

!SLIDE center
# Network addition VS. Full local repository #

## PICTUREME: SVN star vs GIT network


!SLIDE center
# Fossile history VS. Live history #

## PICTUREME: SVN fossile vs GIT live


!SLIDE center
# Merge VS. Rebase #

## PICTUREME: SVN silo-like branches merging VS. GIT graft-like rebasing


!SLIDE commandline
# Expensive branches VS. Free branches

    $ svn copy http://svn.example.com/repos/calc/trunk \
      http://svn.example.com/repos/calc/branches/my-calc-branch \
      -m "Creating a private branch of /calc/trunk."

    $ git branch my-calc-branch


!SLIDE center
# Directory centric VS. File centric #

## PICTUREME: SVN example with lots of .svn VS. GIT example with only one root .git
