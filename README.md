# caroldearoak.com — MMDP 作品展示站

2026-11-22 改版：站点内容由「橡树旁博客（本体建模系列 5 篇 + ad-kg 演示页）」**完全替换**为 **MMDP 多模态数据工厂作品展示**（单页静态站：`public/index.html` + `prototypes/` 12 个产品原型页 + `shots/` 24 张实测截图 + 本地化前端依赖 `assets/`）。

## 结构

- Astro 仅作为构建壳：`src/pages/` 为空，`public/` 内容原样拷入 `dist/`
- 部署管线不变：push 到 GitHub → Cloudflare 构建发布
- 本地预览：`npm run dev` / `npm run build && npm run preview`

## 旧站内容还原方式（二选一）

1. **git 还原点**：`git checkout oak-blog-last -- src public`（tag 打在替换前最后一次提交）
2. **本地全量存档**：`/Users/hu/project/oaksite-archive-20261122/`（含未提交过的 `about.astro` 实名定稿版——该文件从未进入 git 历史，只在此存档）

## 内容诚实边界（沿袭 showcase 原则）

- 截图=运行中系统实测（非设计稿）；数据=夹具播种
- 多模态解析=macOS 专属（服务器如实显示未部署）
- 生产部署/真实运营=不在作品范围
