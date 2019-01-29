This git repo contains a number of embedded git repos.

I found all of them on Github using a search for language KRL.

Some of these may be helpful when working on CS462 labs (i.e. "how the hell does this work in practice" vs. "what does the manual say poorly")

I created this by just cloning the repositories at first, then I used 
```
find . -name '.git' -execdir git remote -v \; | grep "fetch" >> remotes.txt
awk 'system("git submodule add " $2)' remotes.txt
```
to "reconstitute" all the repos as proper submodules.

To clone this, use `git clone --recurse-submodules`.

