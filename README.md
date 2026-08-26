# Li Huang's Personal Homepage

简洁清晰的学术个人主页（纯静态 HTML，无构建依赖）。
板块：Bio / Recent News / Research / Publications / Awards / Education。

仓库：<https://github.com/hhhhhli/hhhhhli>

## 开启 GitHub Pages（需要做一次）

1. 打开仓库页面 → **Settings → Pages**
2. Source 选 **Deploy from a branch**，Branch 选 `main` / `(root)`，保存
3. 1–2 分钟后访问：<https://hhhhhli.github.io/hhhhhli/>

> **注意**：
> - Pages 地址带 `/hhhhli` 路径后缀。如果想用根地址 `https://hhhhhli.github.io/`，
>   把仓库重命名为 `hhhhhli.github.io` 即可（Settings → General → Rename，页面内容无需改动，资源路径是相对路径，两种地址都兼容）。
> - 免费版 GitHub 账号要求仓库为 **public** 才能开 Pages；private 仓库需要 GitHub Pro。

## 本地预览

```bash
cd /home/hl/Tools/myPage
python3 -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 更新主页

```bash
# 编辑 index.html 后：
git add index.html
git commit -m "Update xxx"
git push
```

## 维护指南

- 新闻：编辑 `index.html` 中 `<section id="news">`
- 论文：编辑 `<section id="publications">`，每篇一个 `<div class="pub">`
- 之后想给论文加配图：把图片放进 `assets/`，在对应 `.pub` 里加
  `<img src="assets/xxx.png" style="height:110px;border-radius:6px;border:1px solid #e4e7eb;">`
  （`cv/cv_assets/` 里还有 DLODepth、衣物分类、路径规划等现成配图可复制过来用）
- 照片：替换 `assets/photo.jpg`
