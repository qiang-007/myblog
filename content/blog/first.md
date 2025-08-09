+++
date = '2025-08-09T16:09:13+08:00'
draft = false
title = 'First'

+++

## 1 把别人的仓库变成自己的

### 1.1 克隆原仓库到本地

```bash
git clone https://github.com/原作者/原仓库.git
cd 原仓库  # 进入克隆的目录
```
### 1.2 移除原远程仓库关联删除默认的 origin远程

```bash
git remote remove origin
```
### 1.3 在 GitHub 创建新仓库
1. 登录 GitHub → "+" → "New repository"
2. 不要勾选 "Add a README file"（保持空仓库）
3. 获取新仓库的 URL（如 https://github.com/你的用户名/新仓库名.git）
### 1.4 关联自己的远程仓库

```bash
git remote add origin https://github.com/你的用户名/新仓库名.git
```
### 1.5 重命名分支（可选但推荐）

```bash
git branch -M main  # 将默认分支改为 main（或其他名称）
```
### 1.6 推送所有分支到新仓库

```bash
git push -u origin --all # 推送所有分支
```

----
## 2 新增/删除/修改本地仓库文件，该如何同步到远程（以删除为例）
### 2.1 命令行删除
#### 2.1.1 进入仓库目录

```bash
cd /path/to/your/repo
```
#### 2.1.2 删除文件夹（比如名为 'old-dir'）

```bash
git rm -r old-dir
```
#### 2.1.3 提交变更

```bash
git commit -m "Remove old-dir"
```
#### 2.1.4 推送到GitHub

```bash
git push origin main
```

### 2.2 手动删除
若你直接通过资源管理器删除了文件夹，Git 会检测到该变更。你可以使用以下命令来提交。

```bash
# 进入仓库
cd /path/to/your/repo
# 暂存所有变更
git add --all
git commit -m "Manually removed folder"
git push origin main
```
