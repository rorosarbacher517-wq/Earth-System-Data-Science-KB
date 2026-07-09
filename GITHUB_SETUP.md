# GitHub 仓库创建与发布说明

目标仓库建议：

```text
Earth-System-Data-Science-KB
```

推荐远端地址：

```text
https://github.com/rorosarbacher517-wq/Earth-System-Data-Science-KB
```

## 推荐账号结构

```text
rorosarbacher517-wq/
  rorosarbacher517-wq            # Profile 仓库，用于 GitHub 主页 README
  rorosarbacher517-wq.github.io  # 个人网站，可选
  Earth-System-Data-Science-KB   # 本知识库主体
  Bin_Fan                        # 可改成下级项目名
  GridWeatherAgent               # 具体项目
```

## 在 GitHub 网页新建仓库

1. 打开 `https://github.com/new`。
2. Owner 选择 `rorosarbacher517-wq`。
3. Repository name 填 `Earth-System-Data-Science-KB`。
4. Description 可填：

```text
Personal knowledge base for Earth system data science, remote sensing, carbon flux, policy, methods, and applications.
```

5. 选择 Public 或 Private。
6. 不要勾选初始化 README、`.gitignore` 或 License，因为本地已经有内容。

## 如果本机 Git 可用后的命令

进入这个目录：

```powershell
cd C:\Users\2021206190012-FanBin\Documents\HLS_METE_CARBON_FFP\work\Earth-System-Data-Science-KB
```

初始化并提交：

```powershell
git init
git add .
git commit -m "Build personal earth system data science knowledge base"
git branch -M main
git remote add origin https://github.com/rorosarbacher517-wq/Earth-System-Data-Science-KB.git
git push -u origin main
```

## Profile 仓库建议

如果想让 GitHub 账号主页展示个人介绍，应另建一个与用户名同名的仓库：

```text
rorosarbacher517-wq
```

里面放一个 `README.md`，链接到：

- `Earth-System-Data-Science-KB`
- 个人网站
- 代表项目，如 GridWeatherAgent、HLS carbon flux project 等

