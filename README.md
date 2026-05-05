# 🚀 Arch Linux 新手：第一次上传代码到 GitHub

> 本指南适用于刚接触 Linux 和 GitHub 的开发者，手把手教你如何在 Arch Linux 上配置环境并上传代码。

---

## 📋 目录

1. [安装 Git](#1-安装-git)
2. [配置 Git 用户信息](#2-配置-git-用户信息)
3. [生成 SSH 密钥](#3-生成-ssh-密钥)
4. [在 GitHub 添加 SSH 密钥](#4-在-github-添加-ssh-密钥)
5. [克隆/初始化仓库](#5-克隆或初始化仓库)
6. [提交并推送代码](#6-提交并推送代码)

---

## 1. 安装 Git

```bash
sudo pacman -Sy git
```

验证安装：

```bash
git --version
```

---

## 2. 配置 Git 用户信息

```bash
git config --global user.name "你的GitHub用户名"
git config --global user.email "你的GitHub绑定邮箱"
```

查看配置：

```bash
git config --list
```

---

## 3. 生成 SSH 密钥

```bash
ssh-keygen -t ed25519 -C "你的GitHub邮箱" -f ~/.ssh/id_ed25519 -N ""
```

查看公钥（复制输出内容）：

```bash
cat ~/.ssh/id_ed25519.pub
```

---

## 4. 在 GitHub 添加 SSH 密钥

1. 打开 [GitHub Settings → SSH and GPG keys](https://github.com/settings/keys)
2. 点击 **New SSH key**
3. Title 填：`ArchLinux-Main`（或你喜欢的名字）
4. Key 填上面复制的公钥内容
5. 点击 **Add SSH key**

---

## 5. 克隆或初始化仓库

### 方式一：克隆已有仓库

```bash
git clone git@github.com:你的用户名/仓库名.git
cd 仓库名
```

### 方式二：初始化新项目

```bash
mkdir 项目名 && cd 项目名
git init
```

---

## 6. 提交并推送代码

```bash
# 添加所有文件
git add .

# 提交（带说明）
git commit -m "初始化项目"

# 添加远程仓库（如果没加过）
git remote add origin git@github.com:你的用户名/仓库名.git

# 推送到 GitHub
git push -u origin master
```

---

## ✅ 常见问题

### Q: 推送时提示 "Permission denied (publickey)"？
A: 检查 SSH 密钥是否已添加到 GitHub，运行 `ssh -T git@github.com` 测试连接。

### Q: 如何查看当前远程仓库？
```bash
git remote -v
```

### Q: 如何更新远程仓库地址？
```bash
git remote set-url origin git@github.com:你的用户名/仓库名.git
```

---

## 🎉 恭喜！

现在你已经成功在 Arch Linux 上配置了 Git 并上传了第一份代码！

---

> 📝 本项目由 Koni 首次上传，记录新手成长的第一步 🐧  
> 有问题随时联系我～ 😊
