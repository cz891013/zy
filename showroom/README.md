# AI 数字人展厅

Cursor 风格暗色主题展厅页面，嵌入 **本地数字人视频** + **Coze 智能问答**，可 iframe 部署到 GitHub Pages。

## 快速开始

### 1. 放入数字人视频

将你的数字人视频文件（`.mp4` / `.webm`）放入 `showroom/` 目录。

然后编辑 `index.html`，找到：

```html
<video ... src="about:blank"
```

改为你的文件名，例如：

```html
<video ... src="digital-human.mp4"
```

> 视频推荐：竖屏 9:16，静音自动播放，建议体积 ≤20MB。

### 2. Coze 问答 — 已配置 ✅

Coze 智能体已嵌入，开箱即用。

如需更换 Bot，编辑 `index.html` 中 Coze 区域的 `<iframe src="...">`。

### 3. 部署到 GitHub Pages

```bash
# 将 showroom 目录推送到 GitHub
git add showroom/
git commit -m "add AI showroom"
git push
```

在仓库 **Settings → Pages** 中配置：
- **Source**: Deploy from a branch
- **Branch**: main（或你的分支）
- **Folder**: `/showroom`

部署后访问 `https://<你的用户名>.github.io/<仓库名>/showroom/`

### 4. 通过 iframe 嵌入

```html
<iframe
  src="https://<你的用户名>.github.io/<仓库名>/showroom/"
  width="100%"
  height="800px"
  frameborder="0"
  allow="autoplay; microphone; camera"
></iframe>
```

## 文件结构

```
showroom/
├── index.html       # 主页面（单文件，无外部依赖）
├── avatar.mp4       # ← 你的数字人视频文件（放入即可）
└── README.md        # 本文件
```