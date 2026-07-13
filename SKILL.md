---
name: ayu-design-system
description: 阿鱼的个人IP设计系统。做 HTML 页面、个人网站、教程页、landing、App 页、图文卡片、公众号排版等前端设计时自动触发。
author: Yoselin（adapted from ESTHER不二 / esthersjw）
license: CC BY-NC-SA 4.0
repo: https://github.com/yuanxuru-oss/ayu-design-system
---

> 基于 ESTHER不二 (esthersjw) 的原始设计系统改编。
> 当前正式风格以阿鱼 Ayu 的 brand DNA 为准，UI 组件语言优先参考 `animal-island-ui`。

触发条件：当用户要求制作 HTML 页面、个人页面、教程页面、介绍页面、landing、活动页、App 型页面、组件预览、图文卡片、公众号排版等视觉前端任务时触发。

## 使用方式（7 步工作流）

### Step 1: 澄清需求
向用户确认 5 件事：
1. 类型：教程 / landing / App / 卡片 / 公众号？
2. 受众：给谁看，偏生活、偏功能还是偏说明？
3. 页面数量或 section 数：一页还是多页？
4. 素材：文案、图片、头像、icon、已有参考？
5. 硬约束：必须保留什么，不能出现什么？

### Step 2: 读规范
1. 必读 `brand-dna.md`
2. 按场景选读：
   - 教程 / 说明 / 知识页 → `references/scene-tutorial.md`
   - landing / 入口 / 公告页 → `references/scene-landing.md`
   - App / 功能页 → `references/scene-app.md`
   - 小红书卡片 / 图文页 → `references/scene-cards.md`
   - 公众号排版 → `references/scene-wechat.md`

### Step 3: 拷模板
从 `assets/` 里选对应模板起步，不从零开始：
- 教程页 → `assets/template-tutorial.html`
- landing 页 → `assets/template-landing.html`
- App 页 → `assets/template-app.html`
- 卡片页 → `assets/template-cards.html`
- 公众号 → `assets/template-wechat.html`

### Step 4: 选布局
先看 `references/layouts.md`，选择符合 Ayu 小岛系统的布局骨架。

规则：
- 不做通用网页布局复用
- 一页里至少混用 3 种布局语义
- 优先使用 `NookPhone Hero / Leaf Board Banner / Passport Split / Bulletin Stack / Module Grid`

### Step 5: 选组件
优先从 `references/components.md` 里挑组件家族。

硬规则：
- 组件要有“原生 UI 系统感”
- 禁止同一模板重复复制只换标题
- 优先使用 `Passport Card / Module Entry Card / Memo Card / Collectible Card / Status Panel / Board Panel / WeChat Reading Block`
- UI 总览页优先沿用 `animal-island-ui` 的原生部件语汇

### Step 6: 自检
对照 `references/checklist.md` 逐条检查：
- P0 必须全过
- P1 尽量都过
- P2 作为加分项

补充要求：
- 看起来要像“有人生活在里面的系统”
- 不能像 SaaS、博客模板、课程后台、通用 AI 页面

### Step 7: 交付
输出最终 HTML，并确保本地浏览器可直接打开预览。

---

## 场景速查

| 类型 | 规范文件 | 模板 |
|------|----------|------|
| 教程 / 说明页 | `references/scene-tutorial.md` | `assets/template-tutorial.html` |
| landing / 入口页 | `references/scene-landing.md` | `assets/template-landing.html` |
| App / 功能页 | `references/scene-app.md` | `assets/template-app.html` |
| 图文卡片 | `references/scene-cards.md` | `assets/template-cards.html` |
| 公众号排版 | `references/scene-wechat.md` | `assets/template-wechat.html` |

---

## 核心原则

- 从模板改，不从零画
- 先对齐阿鱼品牌，再谈创意发挥
- 页面首先要像 Ayu 的系统，其次才是某种网页类型
- 组件要像一个活的岛上 UI 体系，不是文档页组件展厅

---

## 禁忌

- 不要回到 Esther 旧系统的蓝黄红 editorial 视觉
- 不要冷灰、科技、玻璃、SaaS、模板站气质
- 不要 HTML 默认组件
- 不要“看起来就是 AI 做的”
