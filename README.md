# 个人知识库 + 作品集

纯静态网站，用 GitHub Pages 免费托管。

## 目录结构

```
.
├── index.html              首页(导航入口)
├── portfolio/
│   └── index.html          作品集展示页
└── notes/                  知识库(Docsify 驱动)
    ├── index.html          Docsify 加载器,一般不用改
    ├── custom.css           视觉样式,与主站统一
    ├── README.md            知识库首页内容
    ├── _sidebar.md          左侧目录导航
    └── example-note.md      示例笔记
```

## 部署到 GitHub Pages

1. 把这个仓库 push 到 GitHub(仓库需要是 Public,除非你是付费账户)
2. 进入仓库 **Settings → Pages**
3. **Source** 选择 `main` 分支,目录选 `/ (root)`
4. 保存，等 1-2 分钟，访问 `https://你的用户名.github.io/仓库名/`

## 日常更新

**加一个新作品** → 编辑 `portfolio/index.html`,复制一份 `.project` 区块，改标题、描述、标签、封面图，改完 push 即可。

**加一篇新笔记** → 在 `notes/` 下新建一个 `.md` 文件，然后在 `notes/_sidebar.md` 里加一行链接。不需要碰 HTML。

**换字体 / 配色** → 全站的颜色变量集中定义在每个 HTML 文件顶部的 `:root{ ... }` 里,以及 `notes/custom.css`,改这几处颜色值即可全局生效。

## 本地预览

不需要构建工具,用任意静态服务器打开即可,比如：

```bash
python3 -m http.server 8000
```

然后浏览器打开 `http://localhost:8000`。

（如果直接双击打开 `notes/index.html`，Docsify 的 Markdown 加载在部分浏览器上会因为本地文件安全限制而失败，建议用上面的方式起一个本地服务器。）
