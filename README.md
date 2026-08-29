# 高中72篇必背古诗文 · GitHub Pages 一键部署版

这是已经配置好的纯静态 GitHub Pages 项目。

## 最简单的上传方法

1. 在 GitHub 新建一个仓库，例如 `72-classics`。
2. 把这个文件夹里的**所有文件和文件夹**上传到仓库根目录。
   - 必须包括隐藏目录 `.github`
   - `index.html` 必须位于仓库根目录
3. 提交到 `main` 分支。
4. 打开仓库：
   `Settings → Pages`
5. 在 **Build and deployment → Source** 中选择 **GitHub Actions**。
6. 打开仓库顶部的 `Actions`。
7. 等待 **Deploy GitHub Pages** 变成绿色。
8. 再回 `Settings → Pages`，即可看到网站地址。

之后每次修改并推送到 `main`，网站会自动重新发布。

## 项目结构

```text
.
├── .github/
│   └── workflows/
│       └── pages.yml
├── .nojekyll
├── index.html
├── 404.html
└── README.md
```

## 为什么这样配置

- 不需要 Node.js
- 不需要 npm
- 不需要 Vite / React / Vue 构建
- 不需要改绝对路径
- 支持 GitHub 项目站点：
  `https://用户名.github.io/仓库名/`
- 每次 push 到 `main` 自动部署

## 如果 Actions 报 Pages 未启用

打开：

`Settings → Pages → Build and deployment → Source → GitHub Actions`

然后重新运行 Actions。

## 自定义域名

以后如需自定义域名，建议直接在：

`Settings → Pages → Custom domain`

里配置。
