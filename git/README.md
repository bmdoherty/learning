git config --global user.name 'bmdoherty'

Set up a new Git repo within the current directory.
git init

git status

git add .

Use the given <msg> as the commit message. 
git commit -m 'add file'

git log

git diff

git diff --staged

git reset index.html

automatically stage files that have been modified and deleted & commit
git commit -a -m 'commit already tracked'

git commit --amend -m 'stuff'

Undo the commit, and put the files back in staging.
git reset --soft HEAD^

Discard your changes, '--' dnt accidemtallu checkout branch 
git checkout -- test.html index.html

remove the most recent commit, and all its changes reset to commit before last, HEAD^
git reset --hard HEAD^

Add address in the origin repo.
git remote add origin git@test.com:example/test.git

git push -u origin master

clone a repo
git clone git@test.com:example/test.git

get a list of all our remotes
git remote -v

create branch and checkout one line
git checkout -b mybranch

bring changes from mybranch into master
git checkout master
git merge mybranch

git pull to fetch and merge at the same time
git pull

mark conflict as resoved, 
git add .

push a local branch to a remote
git push origin mybranch

get remotes
git fetch

list of remote branches
git branch -r

delete remote branch
git push origin :mybranch

branch status, Check for stale branches that are tracking "origin".
git remote show origin

Clean up your local references
git remote prune origin

Display the tags
git tag

create tag with message
git tag -a 'v1.2.3' -m 'message'

push tags to origin
git push -tags

checkout a tag
git checkout 'v1.2.3'

Rebase the current mybranch on master
git checkout mybranch
git rebase master
git checkout master
git merge mybranch

get changes to origin master
git fetch

move local master commits after the commits from origin/master.
git rebase

continue reabse after resolving a conflict
git rebase --continue

view log, one line
git log --oneline

compare branch with master
git diff master mybranch

 a diff that includes the previous commit, as well as its parent.
 git diff HEAD~2

 get commit and diff info (-p patch)
 git log -p

 get author and diff info
 git blame index.html

 create alias
 git config alias.co checkout

rebase with master
git rebase master

git stash save 'test'

git stash list

git stash apply

git stash drop

git stash --keep-index

git stash list --stat

git stash show --patch stash@{2}

git stash branch mybranch

unix file endings on commit
git config core.autocrlf input

convert line endings from Unix to Windows formats on checkout.
git config core.autocrlf true

.gitattributes
*     text=auto
*.rb text
*.js text

*.bat text eol=crlf
*.sh text eol=lf

*.png binary

git cherry-pick 3fbd473

edit and change message
git cherry-pick -e 3fbd473 -m 'test'

git cherry-pick --no-commit b447335 b59d285

cherry pick keep where it comes from
git cherry-pick -x bdf9578

with person who signed off
git cherry-pick -x --signoff bdf9578

git add submodule
git submodule add git@petstore.com:gallery_js.git

git submodule init

git submodule update

apply detached commit on to branch, mybranch
git branch mybranch a7eded4

check if submodules require pushes
git push --recurse-submodules check

push submodules when needed
git push --recurse-submodules on-demand

alias for above
git config alias.pushall 'push --recurse-submodules=on-demand'

move code & index to a commit
git reset --hard ab27026

see local head changes
git reflog

force delete branch
git branch -D mybranch

find last commit on deleted branch
git log --walk-reflogs

create branch from a commit
git branch mybranch aaafb5e3e33a174a5cb5f45c543d3dd927dfdf32
