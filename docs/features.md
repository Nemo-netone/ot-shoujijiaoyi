# 功能说明

## 项目定位

面向手机商品、分类、轮播、购物车、订单和用户管理的交易商城演示系统。

## 功能树

| 模块 | 责任 | 数据归属 |
|---|---|---|
| 手机商品 | 商品标题、分类、价格、库存和上架状态 | `items.module_key = goods` |
| 分类管理 | 手机品牌、系列、层级和排序 | `items.module_key = category` |
| 首页轮播 | 首页推荐图、跳转地址和排序 | `items.module_key = carousel` |
| 购物车 | 加购、数量、价格和结算准备 | `items.module_key = cart` |
| 订单管理 | 订单、明细、支付和配送状态 | `items.module_key = order` |
| 用户管理 | 用户、地址、联系方式和禁用状态 | `items.module_key = user` |

## 使用场景

1. 访客打开 `https://ot-shoujijiaoyi.pages.dev`，先浏览项目定位、核心模块和演示账号。
2. 使用公开账号登录，进入工作台查看统计数据。
3. 通过模块侧边栏进入业务表，进行列表浏览、关键词搜索、新增、编辑和删除。
4. 管理员可完整演示数据维护流程；普通用户和工作人员账号用于展示不同角色入口。

## 调用链和数据流

```text
浏览器
  -> site/app.js
  -> /api/login 或 /api/items/*
  -> site/_worker.js
  -> Supabase RPC public.ot_shoujijiaoyi_demo_rest
  -> ot_shoujijiaoyi.accounts / ot_shoujijiaoyi.items
```

## 推荐演示路径

```text
登录 -> 工作台统计 -> 手机商品 -> 分类管理 -> 首页轮播 -> 购物车 -> 新增一条记录 -> 编辑状态 -> 删除测试记录
```

## 演示边界

- 已实现：登录、统计、业务模块列表、搜索、新增、编辑、删除。
- 部分实现：原项目的复杂权限、文件上传、第三方服务以作品集展示为主。
- 未接入：真实支付、短信、地图、邮件、生产级文件存储。
