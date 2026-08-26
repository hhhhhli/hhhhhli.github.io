# Li Huang's Personal Homepage

简洁清晰的学术个人主页（纯静态 HTML，无构建依赖），结构参考经典学术主页：
Bio / Recent News / Research / Publications / Patents / Awards / Education。

## 本地预览

```bash
cd /home/hl/Tools/myPage
python3 -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 部署到 GitHub Pages（推荐）

1. 在 GitHub 上创建仓库，命名为 `<你的用户名>.github.io`（例如 `huangli-zju.github.io`），公开仓库。
2. 推送本目录内容（index.html 和 assets/）：
   ```bash
   git init
   git add index.html assets/
   git commit -m "Init personal homepage"
   git branch -M main
   git remote add origin git@github.com:<你的用户名>/<你的用户名>.github.io.git
   git push -u origin main
   ```
3. 等待 1–2 分钟，访问 `https://<你的用户名>.github.io` 即可。

> 也可以放到任意仓库（如 `homepage`），在仓库 Settings → Pages 里选 `main` 分支开启 Pages。

## 部署到 Gitee Pages（可选）

Gitee Pages 需要实名认证，且免费版更新后需手动在「服务 → Gitee Pages」点击更新，
境内外访问速度不如 GitHub Pages + CDN。步骤：创建公开仓库 → 推送上述文件 →
仓库页「服务 → Gitee Pages」→ 部署分支选 `main` → 启动/更新。

## 维护

- 新闻：编辑 `index.html` 中 `<section id="news">`。
- 论文：编辑 `<section id="publications">`，每篇一个 `<div class="pub">`。
- 图片：放在 `assets/`，研究板块的 teaser 图在对应 `<figure class="teaser">` 中替换。
