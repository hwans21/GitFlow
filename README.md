# GitFlow

 git add .
 git commit -am 'work 1'
 clear
 git tag 0.1
 git checkout -b develop
 git commit -am 'work 2'
 git commit -am 'work 3'
 git checkout -b release/0.2
 git status
 git add .
 git commit -am 'release 0.2 1'
 git commit -am 'release 0.2 2'
 git checkout develop
 git merge release/0.2
 git checkout release/0.2
 git checkout master
 git merge --no-ff release/0.2
 git branch -d release/0.2
 git tag 0.2
 git checkout develop
 git branch feature/short
 git branch feature/long
 git checkout feature/short
 git commit -am 'short 1'
 git add .
 git commit -am 'short 1'
 git checkout feature/long
 git add .
 git commit -am 'long 1'
 git checkout develop
 git merge --no-ff feature/short
 git branch -d feature/short
 git checkout -b release/1.0
 git commit -am 'short 3 - bug fix'
 git commit -am 'work 4 - bug fix'
 git checkout develop
 git merge --no-ff release/1.0
 git checkout master
 git merge --no-ff release/1.0
 git tag 1.0
 git branch -d release/1.0
 git checkout -b hotfixes/1.1
 git add .
 git commit -am 'hotfix 1.1'
 git checkout develop
 git merge --no-ff hotfixes/1.1
 git checkout master
 git merge --no-ff hotfixes/1.1
 git tag 1.1
 git branch -d hotfixes/1.1
