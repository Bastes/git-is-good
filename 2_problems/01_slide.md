!SLIDE bullets incremental
# SVN VS. GIT

* Network addict VS. Full local
* Fossile VS. Live history
* Expensive VS. Free branches

!SLIDE center
## Network VS. Full local

![SVN (star) VS. GIT (network)](./svn-star-git-network.png)


!SLIDE center
## Fossile VS. Live history

![SVN (fossile) VS. GIT (live)](./svn-fossile-git-live.png)


!SLIDE commandline incremental
## Expensive VS. Free branch

    $ svn copy http://svn.example.com/repos/calc/trunk \
      http://svn.example.com/repos/calc/branches/my-calc-branch \
      -m "Creating a private branch of /calc/trunk."

    $ git branch my-calc-branch
