# 🐧 Githubdemo

> 🍞 一个简单的 C++ 项目，记录新手成长的第一步

[![Arch Linux](https://img.shields.io/badge/Arch_Linux-1793D1?logo=archlinux&logoColor=white)](https://archlinux.org/)
[![C++](https://img.shields.io/badge/C++-00599C?logo=cplusplus&logoColor=white)](https://isocpp.org/)
[![GitHub](https://img.shields.io/github/license/Yukonila/Githubdemo?color=blue)](https://github.com/Yukonila/Githubdemo/blob/master/LICENSE)

---

## 📖 目录

- [🔧 环境配置](#-环境配置)
- [⚙️ CLion 设置](#️-clion-设置)
- [📝 项目结构](#-项目结构)
- [❓ 常见问题](#-常见问题)

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

#### 3️⃣ 生成 SSH 密钥（推荐）

```bash
ssh-keygen -t ed25519 -C "你的邮箱" -f ~/.ssh/id_ed25519 -N ""
cat ~/.ssh/id_ed25519.pub  # 复制输出到 GitHub → Settings → SSH keys
```

#### 4️⃣ 测试连接

```bash
ssh -T git@github.com
```

---

## ⚙️ CLion 设置

### 1️⃣ 打开项目

1. 启动 CLion  
2. 点击 **File → Open**  
3. 选择 `/home/Koni/Mycpp` 目录  
4. 点击 **OK**

### 2️⃣ 配置 CMake

CLion 会自动读取 `CMakeLists.txt`，但可以手动调整：

1. 点击右上角 **CMake** 配置下拉框 → **Edit Configurations**  
2. 确保 **Build, Run, and Tests** 使用 `GitHubdemo` 目标  
3. 点击 **Apply** 保存

### 3️⃣ 忽略本地文件

CLion 会生成 `.idea/` 和 `cmake-build-debug/` 文件夹，这些是本地配置，**不需要提交到 GitHub**：

- `.idea/`：CLion 项目配置（编译器路径、代码风格等）  
- `cmake-build-debug/`：编译输出（可执行文件、中间文件）

### 4️⃣ 重新加载项目

修改 `CMakeLists.txt` 后，点击：  
**Tools → CMake → Reload CMake Project**  
或点击右上角 **Sync Project with CMakeLists.txt** 🔄

---

## 📝 项目结构

```
Githubdemo/
├── CMakeLists.txt      # CMake 构建配置
├── main.cpp            # 主程序入口
├── cmake-build-debug/  # 编译输出（自动生成，不提交）
├── .git/               # Git 版本控制
└── README.md           # 本文件
```

> 💡 **说明**：`.idea/` 和 `cmake-build-debug/` 是本地生成的，不会上传到 GitHub。

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
