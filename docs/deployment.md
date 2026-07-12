# 部署说明

- Cloudflare Pages 项目：`ot-shoujijiaoyi`
- 生产分支：`main`
- 发布目录：`original-site/`
- 稳定地址：https://ot-shoujijiaoyi.pages.dev
- API：同源 Pages Worker，入口为 `original-site/_worker.js`
- 数据：项目隔离 Supabase schema，凭据仅配置在 Cloudflare secrets

2026-07-12 已真实部署，并完成健康检查、三类账号登录、`product` 商品列表、CRUD、桌面端和移动端浏览器验证。`site/` 为旧统一兜底页面，生产发布使用 `original-site/`。