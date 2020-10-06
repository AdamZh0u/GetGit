
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

git status
git add readme.md
git status
git add license
git status
git commit



```



resources: https://github.com/dtbootcamp/getting-started-with-git-and-github
