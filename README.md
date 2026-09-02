# Li Huang's Personal Homepage

简洁清晰的学术个人主页(纯静态 HTML,无构建依赖)。
板块:Bio / Recent News / Research / Publications / Awards / Education。

- 仓库:<https://github.com/hhhhhli/hhhhhli.github.io>
- 主页:<https://hhhhhli.github.io/>

## 首次部署(GitHub 网页上做一次)

1. **改 public**:仓库页 → Settings → General → Danger Zone → Change visibility → Public
2. **改名为 `hhhhhli.github.io`**:Settings → General → Repository name → Rename
   (重命名后 GitHub 自动重定向旧地址,本地 remote 建议同步更新,见下文)
3. **开启 Pages**(若未自动开启):Settings → Pages → Source 选 Deploy from a branch,
   Branch 选 `master` / `(root)`,保存
4. 1–2 分钟后访问 <https://hhhhhli.github.io/> 确认生效

## 重命名后同步本地 remote

```bash
git remote set-url origin git@github.com:hhhhhli/hhhhhli.github.io.git
```

## 本地预览

```bash
python3 -m http.server 8000
# 浏览器打开 http://localhost:8000
```

## 更新主页

```bash
# 编辑 index.html 后:
git add index.html
git commit -m "Update xxx"
git push
```

## 维护指南

- 新闻:编辑 `index.html` 中 `<section id="news">`
- 论文:编辑 `index.html` 中 `<section id="publications">`,每篇一个 `<div class="pub">`
- 之后想给论文加配图:把图片放进 `assets/`,在对应 `.pub` 里加
  `<img src="assets/xxx.png" style="height:110px;border-radius:6px;border:1px solid #e4e7eb;">`
  (`cv/cv_assets/` 里还有 DLODepth、衣物分类、路径规划等现成配图可复制过来用)
- 照片:替换 `assets/photo.jpg`
