# Git

These is Git knowledge in CTSM. 



## How to merge master to feature branch or feature to master


### Merge origin/master branch to feature branch
1. Change branch to master, and pull to update all commits
    1. `$ git checkout master`
    2. `$ git pull`
2. Change branch to target, and pull to update commits
    1. `$ git checkout feature`
    2. `$ git pull`
3. Merge master to feature(⚠️ current is feature branch)
    1. `$ git merge master`


### Merge feature branch to origin/master branch
1. Origin/master is the remote master branch, while master is the local master branch.
   1. `$ git checkout master`
   2. `$ git pull origin/master`
   3. `$ git merge feature`
   4. `$ git push origin/master`


## How to rollback to previous commit

1. Find the previous commit ID by commit ‘Git log’ or tool ‘source tree’.  
   ![](https://github.com/ZiqianWangSap/TestMarkdown/blob/master/images/markdown/rollback1.png?raw=true)
2. Reset to previous commit id  
`$ Git rest –hard 385cbaf`  
![](https://github.com/ZiqianWangSap/TestMarkdown/blob/master/images/markdown/rollback2.png?raw=true)
1. Fix conflict and commit your change
`$ Git rebase --continue`
![]([2020-08-14-12-17-32.png](https://github.com/ZiqianWangSap/TestMarkdown/blob/master/images/markdown/rollback3.png?raw=true))


## How to create new branch 

1. Create a new Branch
`$ Git checkout -b "new branch"`
2. Upload new branch to git web & set remote
`$ Git push -u origin "new branch"`
![](https://github.com/ZiqianWangSap/TestMarkdown/blob/master/images/markdown/newBranch1.png?raw=true)
