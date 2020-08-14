# Git

These is some Git knowledge in CTSM. 



## How to merge master to feature branch or feature to master


### Merge origin/master branch to feature branch
1. Change branch to master, and pull to update all commits
   ```bash{.line-numbers}
   $ git checkout master
   $ git pull
   ```
2. Change branch to target, and pull to update commits
   ```bash{.line-numbers}
   $ git checkout feature
   $ git pull
   ```
3. Merge master to feature(⚠️ current is feature branch)
   ```bash{.line-numbers}
   $ git merge master
   ```



### Merge feature branch to origin/master branch
1. Origin/master is the remote master branch, while master is the local master branch.
   ```bash{.line-numbers}
   $ git checkout master
   $ git pull origin/master
   $ git merge feature
   $ git push origin/master
   ```


## How to rollback to previous commit

1. Find the previous commit ID by commit ‘Git log’ or tool ‘source tree’.  
   ![](https://github.com/ZiqianWangSap/TestMarkdown/blob/master/images/markdown/rollback1.png?raw=true)
2. Reset to previous commit id  
   ```bash{.line-numbers}
   $ Git rest –hard 385cbaf
   ```  
    ![](https://github.com/ZiqianWangSap/TestMarkdown/blob/master/images/markdown/rollback2.png?raw=true)
3. Fix conflict and commit your change  
    ```bash{.line-numbers}
    $ Git rebase --continue
    ```  
    ![](https://github.com/ZiqianWangSap/TestMarkdown/blob/master/images/markdown/rollback3.png?raw=true)


## How to create new branch 

1. Create a new Branch
   ```bash{.line-numbers}
   Git checkout -b "new branch"
   ```  
1. Upload new branch to git web & set remote
   ```bash{.line-numbers}
   $ Git push -u origin "new branch"
   ``` 
    ![](https://github.com/ZiqianWangSap/TestMarkdown/blob/master/images/markdown/newBranch1.png?raw=true)
