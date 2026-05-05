# 🐧 Githubdemo

> 🍞 一个简单的 C++ 项目，记录新手成长的第一步

[![Arch Linux](https://img.shields.io/badge/Arch_Linux-1793D1?logo=archlinux&logoColor=white)](https://archlinux.org/)
[![C++](https://img.shields.io/badge/C++-00599C?logo=cplusplus&logoColor=white)](https://isocpp.org/)
[![GitHub](https://img.shields.io/github/license/Yukonila/Githubdemo?color=blue)](https://github.com/Yukonila/Githubdemo/blob/master/LICENSE)

---

## 📖 目录

- [🚀 快速开始](#-快速开始)
- [🔧 环境配置](#-环境配置)
- [📝 项目结构](#-项目结构)
- [❓ 常见问题](#-常见问题)
- [🤝 贡献指南](#-贡献指南)

---

## 🚀 快速开始

```bash
# 克隆仓库
git clone git@github.com:Yukonila/Githubdemo.git
cd Githubdemo

# 编译运行
cmake -B cmake-build-debug
cmake --build cmake-build-debug
./cmake-build-debug/Githubdemo
```

---

## 🔧 环境配置

### Arch Linux 用户

#### 1️⃣ 安装依赖

```bash
sudo pacman -Sy base-devel cmake git
```

#### 2️⃣ 配置 Git

```bash
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
```

#### 3️⃣ 生成 SSH 密钥

```bash
ssh-keygen -t ed25519 -C "你的邮箱" -f ~/.ssh/id_ed25519 -N ""
cat ~/.ssh/id_ed25519.pub  # 复制输出到 GitHub → Settings → SSH keys
```

#### 4️⃣ 测试连接

```bash
ssh -T git@github.com
```

---

## 📝 项目结构

```
Githubdemo/
├── CMakeLists.txt      # CMake 构建配置
├── main.cpp            # 主程序入口
├── cmake-build-debug/  # 编译输出（自动生成，不提交）
├── .git/               # Git 版本控制
├── .gitignore          # Git 忽略配置（CLion/.idea/等）
├── .idea/              # CLion 配置（本地，不提交）
└── README.md           # 本文件
```

> 💡 **说明**：`.idea/` 和 `cmake-build-debug/` 是本地生成的，已加入 `.gitignore`，不会上传到 GitHub。

---

## ❓ 常见问题

### Q: 推送时提示 "Permission denied (publickey)"？

A: 检查 SSH 密钥是否已添加到 GitHub，运行 `ssh -T git@github.com` 测试连接。

### Q: 如何查看当前远程仓库？

```bash
git remote -v
```

### Q: 如何更新远程仓库地址？

```bash
git remote set-url origin git@github.com:Yukonila/Githubdemo.git
```

### Q: 如何回退到上一个提交？

```bash
git reset --hard HEAD~1
```

---

## 🤝 贡献指南

欢迎提交 Issue 和 Pull Request！  
请确保代码通过编译并添加必要的注释。

---

## 📊 技术栈

| 技术 | 版本 |
|------|------|
| C++  | ISO/IEC 14882:2020 |
| CMake | ≥ 3.20 |
| Arch Linux | Rolling Release |

---

## 🎉 恭喜！

你已经完成了新手入门指南！🎉

> 📝 **项目由 Yukonila 创建**  
> 🐧 **首次提交时间：2025-05-05**  
> ✨ **记录成长，分享知识**

---

<div align="center">

![GitHub stars](https://img.shields.io/github/stars/Yukonila/Githubdemo?style=social)
![GitHub forks](https://img.shields.io/github/forks/Yukonila/Githubdemo?style=social)

</div>
