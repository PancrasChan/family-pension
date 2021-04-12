## 初始化仓库
```
git init
```
## 新增文件
```
git add directory
```
## 提交文件
```
git commit -m 提交说明文字
```
## 远程仓库
### 查看远程仓库
```
git remote show origin
```
### 移除远程仓库
```
git remote rm origin
```
### 添加远程仓库
```
git remote add origin {origin_url}
```
<!-- ## 将本地仓库关联到远程仓库
```
git remote show origin
git remote rm origin
git remote add origin https://github.com/PancrasChan/xxxx
``` -->
## 提交到远程仓库
```
git push -u origin master
git push origin master
git push
```
## 删除文件
```
git rm filename
```
## 重命名移动文件
```
git mv src-filename des-filename
```
## 配置用户名邮箱
```
git config --global user.name="xxxx"
git config --global user.email="xxxx"
git config --global --list
git config --add --local user.name="xxxx"
git config --add --local user.email="yyyy"
git config --local --list
```
## 本地文件操作状态
```
git status
```
## 用户操作日志
```
git log --author="xxxxx"
gig log --oneline
git log --oneline --graph
```
## 查看操作详情
```
git show commit-id
```
## 查看文件差别
```
git diff
```
## 还原文件到最后一次提交状态
```
git reset HEAD filename
git checkout -- filename
```
## 退回前N个版本
一个^代表退回前一个版本
N个^代表退回前N个版本
```
git reset --hard HEAD^
```
```
git reset -hard {commit-id}
```

```
git checkout {commit-id} -- {filename}
```
## 标签管理
```
git tag {tag-name}
git tag {tag-name} {commit-id}
git tag -d {tag-name}
git tag
git push origin {tag-name}
```
## 分支管理
### 查看分支列表
```
git branch
git branch -av
```
### 创建分支
```
git branch {branch-name}
```
### 切换分支
```
git checkout {branch-name}
```
### 创建并切换分支
```
git checkout -b {branch-name}
```
### 删除本地分支
```
git branch -d {branch-name}
```
### 合并分支
```
git merge {branch-name}
git merge --abort
```
### 将分支提交到github
```
git push origin {branch-name}
git push --set-upstream origin {branch-name}
```
### 删除github远程分支
```
git push origin --delete {branch-name}
git push origin :{branch-name}
```
## 生成SSH密钥
```
ssh-keygen -t rsa -C "user.email"
cat ~/.ssh/id_rsa.pub
```
### 从远程仓库拉取更新
```
git pull origin {remote-branch-name}:{local-branch-name}
```