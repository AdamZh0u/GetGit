
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

## branch create and quick merge 
```bash
## create branch and switch to
git checkout -b dev 

# or 
git switch -c dev
# or 
git branch dev  ## == git branch -c dev
git checkout dev

touch license
## do changes in license 
git add license 
git commit -m "add license to dev"

## 
git checkout master
git merge # quick merge mode

git branch -d dev
```

## git conflict
```bash
git switch -c dev


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
