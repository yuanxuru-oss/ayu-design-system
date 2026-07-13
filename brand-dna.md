# Brand DNA — 品牌基因 · 阿鱼 Ayu

> 🐧 阿鱼的个人IP设计系统。基于 animal-island-ui 组件库，动森小岛治愈风格。

---

## 🎨 IP固定三色

| 色名 | 色值 | 用途 |
|------|------|------|
| 薄荷绿 | `#19C8B9` | 主色调、标题、超链接、主按钮、重点标记 |
| 阳光黄 | `#F7CD67` | 强调、装饰、badges、高亮、连接线 |
| 蜜柑橙 | `#E59266` | 点缀、标签、CTA、收藏、小面积装饰 |

三色比例原则：主色60% · 强调色30% · 点缀色10%（点缀色永远是点缀，不做主色）

### 辅助色

| 色名 | 色值 | 用途 |
|------|------|------|
| 暖米 | `#F7F3DF` | 卡片底、大面积暖色背景 |
| 米白 | `#F8F8F0` | 页面主背景 |
| 正文棕 | `#725D42` | 正文文字 |
| 标题棕 | `#794F27` | 标题、重点文字 |
| 辅助灰 | `#9F927D` | 次要文字、说明 |
| 边框 | `#C4B89E` | 卡片边框、分割线 |

### NookPhone 扩展色板

```
np-green  #8AC68A    np-teal   #82D5BB    np-yellow #F7CD67
np-orange #E59266    np-pink   #F8A6B2    np-blue   #889DF0
```

---

## 👤 头像/IP形象

头像文件：`assets/avatar.png`（阿鱼企鹅形象，建议正方形，至少 400×400px）

完整IP形象：`assets/character.png`（如有全身/半身企鹅形象）

当前使用：`ayu-penguin.png` — 圆润企鹅头像，动森风

### 使用规则
- 需要头像时优先用 `assets/avatar.png`
- 圆形裁切为主（`border-radius: 50%`），圆角方形为辅助（`border-radius: 20px`）
- 头像外圈用薄荷绿 `#19C8B9` 边框

---

## 🔤 字体基因

### 核心原则
- **标题用手绘感中文** — ZCOOL KuaiLe（快乐体），带来温度
- **英文用圆润无衬线** — Nunito，匹配动森风
- **正文中英文混排** — Noto Sans SC + Nunito
- **中英文搭配** — 英文做装饰/标签，中文承载内容

### 字体池

| 场景 | 字体 | 备注 |
|------|------|------|
| 中文标题 | `ZCOOL KuaiLe`（快乐体） | Google Fonts，手绘感 |
| 英文标题/数字 | `Nunito` (800) | 圆润无衬线，温暖 |
| 正文 | `Noto Sans SC` + `Nunito` | 跨平台可读性 |
| 等宽/代码 | `Fira Code` | 技术场景专用 |

### 字号系统（fluid sizing）
- Hero大标题: `clamp(2.8rem, 7vw, 5.5rem)` — ZCOOL KuaiLe
- Section标题: `clamp(1.6rem, 4vw, 2.6rem)` — ZCOOL KuaiLe
- 卡片标题: `1.15rem ~ 1.4rem` — Nunito 800
- 正文: `16px`
- 辅助文字: `0.78rem ~ 0.85rem`
- 大装饰数字: `clamp(3rem, 8vw, 7rem)` + `opacity: 0.12~0.2`

---

## ✨ 气质关键词

设计出来的东西应该让人觉得：

- **动森小岛风** — Animal Crossing 治愈感，不是幼儿风
- **手绘蜡笔感** — 有温度、有人味、像手作
- **不像AI** — 这是最高优先级的约束
- **温暖但有品质** — 不是廉价可爱，有设计师眼光
- **NookPhone 色系** — 一看就知道是动森风
- **个人品牌感** — 一眼认出是"阿鱼的小岛"
- **卡片有手工感** — 拍立得白框、✧ 印章、暖渐变底、倾斜悬停

---

## 🎨 配色扩展原则

当三色不够用时：

- 背景永远偏暖：`#F8F8F0`（主背景）、`#F7F3DF`（卡片暖米底）
- 文字永远非纯黑：用 `#725D42`（正文）或 `#794F27`（标题）
- 次要文字：`#9F927D`
- 绝不用纯黑 `#000` 或纯白 `#FFF`
- 卡片底色用暖米 `#F7F3DF`，白卡片用 `#FFFFFF` + 暖阴影
- 阴影全用暖色调 `rgba(61,52,40,...)`
- 径向渐变制造层次，不用纯平色

---

## 🧩 组件库

本设计系统使用 **animal-island-ui** 作为组件库。

### 卡片类型
| 卡片 | CSS类 | 用途 |
|------|------|------|
| Memo Card | `.memo-card` | 画廊作品卡片 — 拍立得白框 + 暖渐变底 + ✦ 印章 + 悬停倾斜 |
| Content Card | `.content-card` / `.sp-card` | 通用内容卡片 — 白底 + 24px 圆角 + 双层暖阴影 |
| Widget Card | `.widget-card` / `.sp-widget` | 侧边栏小组件 — 白底 + 20px 圆角 |
| Passport Card | `.passport-card` | 护照/身份卡片 — 暖米底 + 薄荷绿头栏 + 圆形头像 |

### 按钮
- 全部 Pill 形状：`border-radius: 50px`
- 主按钮：`background: #19C8B9; color: #fff`
- 边框按钮：`border: 2px solid #19C8B9`
- 焦点态：`#FFCC00`（黄色，不用蓝色）

### Icon 集
10 个 SVG icon（动森主题）：miles / diy / camera / variant / chat / helicopter / map / design / critterpedia / shopping

---

## 🚫 通用禁忌清单

| 类型 | 禁止 |
|------|------|
| 配色 | 蓝紫渐变、cyan、neon、纯黑白、冷灰背景 |
| 字体 | Inter/Roboto/Arial等通用字体 |
| 圆角 | 小于 12px、直角矩形 |
| 阴影 | 冷灰色阴影（必须用暖棕调 rgba(61,52,40,...)） |
| 焦点 | 蓝色焦点框（必须用黄色 #FFCC00） |
| 动效 | bounce/elastic、无限循环动画 |
| 装饰 | glassmorphism、AI光效、渐变文字 |
| 整体 | 看起来像AI生成的通用模板 |
| 默认样式 | 绝不用浏览器默认的 blockquote / ul / ol / table |

### 自检问题
做完设计后问自己：
1. 这个页面截图发到社交媒体，会不会被人评论"又是AI做的"？
2. 能不能一眼认出这是"阿鱼的小岛"？
3. 有没有动森风的感觉？（暖色、圆润、手工感、NookPhone色系）

---

## 📐 通用间距原则

- Section之间: `clamp(80px, 12vh, 160px)`
- 内容块之间: `clamp(40px, 6vw, 100px)`
- 卡片内padding: `clamp(28px, 3vw, 44px)`
- 元素间gap: `clamp(24px, 3vw, 48px)`
- 全部用 `clamp()` 做fluid sizing
- `max-width: 1300px` + `margin: 0 auto` 约束内容宽度

---

## 📱 响应式通用规则

- 断点: 900px（两栏→单栏）、600px（字号微缩）
- 移动端是"重新排列"不是"缩小"
- 尊重 `prefers-reduced-motion`
- 移动端不隐藏内容——adapt不amputate

---

## 🔍 细节规范

- **选中文本高亮**: `::selection { background: #F7CD67; color: #5c4a1f; }`
- **链接悬停**: 用薄荷绿底色块或下划线，不用变色
- **焦点**: `:focus-visible { outline: 2px solid #FFCC00; outline-offset: 2px; }`

---

*This is the foundation. Every scene file builds on top of this.*
*组件库: animal-island-ui | 头像: ayu-penguin.png | 调色板: NookPhone 13色*
