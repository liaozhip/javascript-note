# git的一些常用命令

## 添加到暂存区

- `git add [file1 file2 ...]`  要添加的文件
- `git add .`  提交所有

## 提交到本地仓库

- `git commit [file1 file2 ...] -m 'message'`  提交指定文件
- `git commit -m 'message'` 提交并填写说明

## 同步到远程仓库

- `git push`

## 删除

- `git rm -r -n --cached [file]`  预览要删除的已提交文件
- `git rm -r --cached [file]` 移除仓库中的文件

## 回退

- `git reset HEAD [file]`  指定文件从暂存区回退到工作区
- `git reset HEAD`  所有文件从暂存区回退到工作区
- `git reset --hard [commit_id]`  回退到指定版本号
- `git checkout [file]`  指定文件从暂存区回退到工作区
- `git checkout .`  回退暂存区的所有文件到工作区

## 查看

- `git log` 查看日志
- `git status`  显示所有变化的文件

## 分支

- `git branch`  列出所有分支
- `git branch -r`  列出所有远程分支
- `git branch -a`  列出所有本地和远程分支
- `git branch [branch-name]`  新建分支
- `git checkout -b [branch-name]` 新建分支并切换
- `git checkout [branch-name]`  切换到指定分支
