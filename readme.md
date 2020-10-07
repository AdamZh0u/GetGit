
## init git

```bash 
mkdir learngit
cd learngit
pwd

git init 

touch readme.md
git add readme.md
git commit -m "add a markdown file"
```

## change file and diff
```bash
git status
git diff readme.md

git add readme.md
git commit -m "change file and diff"
git status
```

## git log and reset
```bash
git log # 显示版本
git log --pretty=oneline

git reset --hard HEAD^  ##回退一个版本
git log 

git reset --hard 6983  # 根据hash前几位指定版本
```

## stage, add and commit 
```bash
touch license

## change license and readem.md

git status ## 显示工作区 stage 变化
git add readme.md
git status
git add license
git status
git commit

git add readme.md
git add readme.md
git commit ## 多次修改放到暂存区
```

## checkout -- file
回退未add的修改
```bash
## change readme.md
123

git checkout -- readme.md
```
将未commit的add到暂存区的回退 unstage
```bash
123
git add readme.md
git reset HEAD readme.md 
```
两次add 后怎么推到第一次add的？

## remove and checkout back 
```bash
rm license 
git status

git rm license 
git satus
git commit -m "rm license" ## rm file in folder and in git

rm license 
git checkout -- license ## recover
```

## remote repo
```bash
ssh-keygen -t rsa -C "youremail@example.com" 
```
id_rsa 
id_rsa.pub公钥

```bash
git remote add origin git@github.com:AdamZh0u/GetGit.git ## origin

git push -u origin master ## --upstream 远程origin 
```

## create branch
```bash
git checkout -b dev ## 创建并切换到
git branch ## 查看分支
git checkout master ## 切换回master

git merge dev ## 合并dev到当前分支 快速合并
git branch -b dev ## 删除dev
git branch
```

```bash
git switch -c dev ## create dev
git switch master ## git switch to master
```

## merge conflicts
```bash

```

## fork workflow
```bash
fork repo1
git clone frepo1
git remote -v # show frepo1
git remote add upstream repo1
git remote -v # show frepo1 repo1

git checkout -b branch master
## changing on branch

git checkout master
git pull upstream master
## pull new changes to local master

git checkout -b branch_new master
git merge branch
git branch -m branch_new branch## rename
git push origin branch

pull request merge branch to master
```


resources: https://github.com/dtbootcamp/getting-started-with-git-and-github
https://nvie.com/posts/a-successful-git-branching-model/