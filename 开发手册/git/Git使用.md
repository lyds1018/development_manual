## 1. 安装 Git

### Windows

[下载 Git for Windows](https://git-scm.com/download/win) → 安装时勾选 **"Add Git to PATH"**。

### Linux（Debian/Ubuntu）

```
sudo apt update && sudo apt install -y git
```

------

## 2. 配置 Git 用户信息（首次使用必做）

```
git config --global user.name "你的名字"
git config --global user.email "你的邮箱"
```

> `--global` 表示全局生效，只需要设置一次。
>  如果只想对当前仓库设置，可以去掉 `--global`。

------

## 3. 获取项目地址

去项目主页（如 GitHub/GitLab/Gitee）找到 **Clone** 地址，有两种方式：

- HTTPS：`https://github.com/用户名/仓库名.git`（适合简单场景）
- SSH：`git@github.com:用户名/仓库名.git`（需要配置 SSH key）

------

## 4. 克隆项目

```
git clone 仓库地址
```

例如：

```
git clone https://github.com/scikit-learn/scikit-learn.git
```

> 默认会克隆所有分支到本地，并在本地切到默认分支（通常是 `main` 或 `master`）。

------

## 5. 进入项目目录

```
cd 项目目录名
```

------

## 6. （可选）切换到其他分支或标签

```
# 查看所有分支
git branch -a

# 切换到某个分支
git checkout 分支名

# 切换到某个版本标签
git checkout 标签名
```

------

## 7. 拉取最新代码（更新本地项目）

```
git pull
```

> 作用：将远程仓库的更新同步到本地当前分支。

------

## 8. 常见问题

- **权限错误**（HTTPS 拉取时）
   需要输入 GitHub 用户名和 Token（Token 可在 GitHub 设置生成）。
- **SSH 无法访问**
   先运行 `ssh-keygen -t rsa -b 4096 -C "邮箱"` 生成密钥，并添加到 GitHub/GitLab 的 SSH keys 设置中。