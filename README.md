# Ayu Design Skill

一套给 AI 看的个人品牌设计系统。

把审美写成操作手册，AI 每次帮你做页面时必须翻这本手册，不能自由发挥。**限制 AI 的自由度 = 保证输出质量。**

> ⚠️ **使用前请先完成 `brand-dna.md` 的配置：** 确认品牌基因、欢迎语、页面气质，并放入你自己的头像 `assets/avatar.png`。

---

## Demo

用这套系统生成的主要页面类型：

### 📖 教程型 / Knowledge Board

像岛上的学习布告栏，不像课程后台或文档 SaaS。

🔗 本地查看：`demo-readme-tutorial.html`

---

### 🎪 活动页 / Landing

更像小岛公告板和品牌入口，不像正式官网。

🔗 本地查看：`demo-landing.html`

---

### 📱 App 型 / 功能型

NookPhone 气质、小岛工具页、图鉴与状态面板。

🔗 本地查看：`demo-app.html`

---

### 📕 小红书图文卡片

更像图鉴、收藏卡册、角色条目，不是海报模板页。

🔗 本地查看：`demo-cards.html`

---

### 📮 公众号排版

公众号长阅读模式，像岛上的公告板 / 长信，而不是旧杂志编号风。

🔗 本地查看：`assets/template-wechat.html` / `assets/demo-wechat.html`

---

### 📜 布局 Playground

围绕入口页、App 页、教程页、图鉴页整理的 Ayu 布局骨架。

🔗 本地查看：`demo-layouts.html`

---

### 🧩 组件库全览

基于 `animal-island-ui` 语汇整理的 Ayu 小岛系统组件总览页。

🔗 本地查看：`components-preview.html`

---

## 核心逻辑

```text
SKILL.md(流程 - AI 按什么步骤干活)
    ↓
brand-dna.md + references/*(规范 - 能用什么不能用什么)
    ↓
assets/template-*.html(起点 - 从模板改,不从零写)
```

- AI 不能随便发明页面气质 → 必须先对齐阿鱼的小岛系统
- AI 不能随便用颜色 → 只能用你定义的品牌色 + 扩展规则
- AI 不能随便写样式 → 必须优先从小岛组件家族里选
- AI 做完要自检 → 对照 checklist 逐条过，P0 不过就打回

---

## 文件结构

```text
ayu-design-system/
├── SKILL.md                    ← 7步工作流(大脑)
├── brand-dna.md                ← 品牌基因:颜色/字体/气质/禁忌(需配置)
├── assets/                     ← 模板骨架(起点)
│   ├── template-tutorial.html      教程页模板
│   ├── template-landing.html       活动页模板
│   ├── template-app.html           App型模板
│   ├── template-cards.html         小红书卡片模板
│   ├── template-wechat.html        公众号模板
│   ├── demo-wechat.html            公众号示例页
│   ├── html2canvas.min.js          卡片导出依赖
│   ├── avatar.png                  当前头像
│   └── avatar-placeholder.svg      占位头像
└── references/                 ← 规则和零件(知识库)
    ├── layouts.md                  布局模式
    ├── components.md               组件家族说明
    ├── checklist.md                质量检查清单(P0/P1/P2)
    ├── scene-tutorial.md           教程场景规范
    ├── scene-landing.md            活动页场景规范
    ├── scene-app.md                App型场景规范
    ├── scene-cards.md              小红书卡片场景规范
    └── scene-wechat.md             公众号排版场景规范
```

---

## 7 步工作流

AI 每次做设计必须按这个顺序走：

| # | 做什么 | 为什么 |
|---|--------|--------|
| 1 | 问 5 个问题(类型/受众/几屏/素材/约束) | 不自作主张 |
| 2 | 读 `brand-dna.md` + 对应场景文件 | 先学规矩再动手 |
| 3 | 从 `assets/` 复制对应模板 | 从半成品开始，不从零写 |
| 4 | 从 `references/layouts.md` 选布局 | 每个 section 不能一样 |
| 5 | 从 `references/components.md` 选组件 | 禁止用 HTML 默认样式 |
| 6 | 对照 `references/checklist.md` 自检 | P0 不过就打回 |
| 7 | 交付 HTML 文件 | 浏览器打开就能看 |

---

## 品牌基因速览

### 三色

| 颜色 | 色值 | 比例 / 用途 |
|------|------|------|
| 主色 | `#19C8B9` | 60% · 薄荷绿 |
| 强调色 | `#F7CD67` | 30% · 阳光黄 |
| 点缀色 | `#E59266` | 10% · 蜜柑橙 |

### 辅助色

| 颜色 | 色值 | 用途 |
|------|------|------|
| 森林绿 | `#67BF9D` | 小岛氛围背景 |
| 暖米 | `#F7F3DF` | 卡片底、大面积暖背景 |
| 米白 | `#F8F8F0` | 页面主内容层 |
| 标题棕 | `#794F27` | 标题、重点文字 |
| 正文棕 | `#725D42` | 正文 |
| 辅助灰 | `#9F927D` | 次要说明 |

### 字体

| 用途 | 字体 |
|------|------|
| 中文标题 | `ZCOOL KuaiLe` |
| 英文标题/数字 | `Nunito` |
| 正文 | `Noto Sans SC` + `Nunito` |

### 气质关键词

动森小岛风 · 手绘手作感 · NookPhone 色系 · 有人物居住感 · 可收集感 · **不像 AI**

### 禁忌

蓝紫渐变 · 冷灰背景 · glassmorphism · neon · Inter/Roboto/Arial 默认感 · 通用 SaaS 风 · HTML 默认样式 · 看起来像 AI 生成的通用模板

---

## 质量检查

**P0(必须全过)**

品牌三色比例 · 无禁忌元素 · 无 HTML 默认样式 · 暖中性色内容层 · 响应式 · 页面语言统一 · 截图发社交媒体不会被说“又是 AI 做的”

**P1(应过)**

至少一个具有小岛系统感的核心组件 · 角色感明确 · 页面有生活气而不是纯展示感

**P2(加分)**

真实 icon 体系 · 图鉴/护照/便签等语义组件充分统一 · 长文模式和短内容模式都能看出同一个系统

---

## 怎么用

1. Fork 或克隆本仓库
2. 确认 `assets/avatar.png` 是你当前要用的头像
3. 打开 `brand-dna.md`，把品牌信息和页面气质更新成你自己的
4. 做页面时从 `assets/template-*.html` 起步，不从空白页开始
5. 把仓库链接发给 AI Agent，告诉它：

> 帮我读这个设计系统，以后做页面按这个规范来。

核心不是这些文件本身，而是**你的审美判断力和判断标准**。这些文件的作用，是把你的判断写成 AI 能执行的规则。

---

## Credits

- 改编自 ESTHER不二 (esthersjw) 的原始设计系统
- 当前 UI 组件语言优先参考 `animal-island-ui`
- Built for 阿鱼 Ayu / Yoselin 的个人小岛系统

---

## License

[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)

本仓库采用 CC BY-NC-SA 4.0 协议。

- ✅ 可自由使用、修改、分享
- ✅ 必须署名原作者 ESTHER不二，并标注当前改编版本 ayu-design-system
- ❌ 禁止商用
- 🔄 修改后必须以相同协议分享
