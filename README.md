# 橡树旁 Roots & Clouds — caroldearoak.com

Carol Hu 的个人网站。Astro 静态站,零后端,md 写作。

## 本地预览

```bash
cd /Users/hu/project/caroldearoak
npm run dev
# 打开 http://localhost:4321
```

## 怎么加一篇文章

在 `src/blog/` 里新建一个 md 文件,文件名格式 `YYYY-MM-DD-标题拼音.md`,开头写:

```markdown
---
title: 文章标题
date: 2026-10-12
description: 一句话摘要(列表页显示)
---

正文,支持 md 全部语法。
```

保存后本地预览自动刷新,文章列表自动按日期排序。

## 改页面文字

- 首页:`src/pages/index.astro`
- 关于页:`src/pages/about.astro`(里面有两处 `【替换】` 标记,记得改成可公开口径)
- 站名/页脚:`src/layouts/Base.astro`
- 配色/字体:`src/styles/global.css`

## 部署到 Vercel(一次性)

1. 推 GitHub:

```bash
cd /Users/hu/project/caroldearoak
git init && git add -A && git commit -m "init: 橡树旁"
# 在 GitHub 上新建空仓库 caroldearoak 后:
git remote add origin git@github.com:<你的用户名>/caroldearoak.git
git branch -M main
git push -u origin main
```

2. [vercel.com](https://vercel.com) → 用 GitHub 登录 → Add New Project → 导入 caroldearoak 仓库 → 框架自动识别为 Astro → Deploy。

3. 绑域名:Vercel 项目 → Settings → Domains → 添加 `caroldearoak.com` 和 `www.caroldearoak.com`。

4. 阿里云控制台 → 域名解析,按 Vercel 提示添加(通常是):
   - `A` 记录:`@ → 76.76.21.21`
   - `CNAME` 记录:`www → cname.vercel-dns.com`

5. 等 DNS 生效(几分钟到 1 小时),HTTPS 证书 Vercel 自动签发。

以后每次 `git push`,网站自动更新。
