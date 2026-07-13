# 布局模式库

> Ayu 小岛系统的布局骨架。重点不是“网页排版感”，而是像住在森林里的游戏面板、公告栏、护照页、图鉴页。

---

## 总原则

- 同一页面至少混用 3 种布局，不要整页一个网格到底
- 内容层优先用暖米/米白卡片，外层保留森林绿叶子纹理背景
- 布局要像“系统界面 + 生活痕迹”，不要像 SaaS 官网或普通作品集
- 圆角要厚，边框要软，阴影要短，不做玻璃感和冷灰感
- 大多数 section 以左对齐或偏左构图为主，避免标准网页居中病

---

## 1. NookPhone Hero

**适用**：App 首页、个人入口页、功能首页

```html
<section class="hero-phone">
  <div class="hero-copy">...</div>
  <div class="hero-device">...</div>
</section>
```

```css
.hero-phone {
  display: grid;
  grid-template-columns: 0.95fr 1.05fr;
  gap: clamp(24px, 4vw, 56px);
  align-items: center;
}
```

要点：
- 一侧是角色信息、欢迎语、状态胶囊
- 一侧是手机 / 系统主面板
- 设备区可以更大，做出“这是系统入口”的主视觉感

---

## 2. Leaf Board Banner

**适用**：landing 首屏、活动公告、欢迎页

```html
<section class="leaf-banner">
  <div class="board-intro">...</div>
</section>
```

```css
.leaf-banner {
  padding: clamp(28px, 5vw, 56px);
  border-radius: 36px;
}
```

要点：
- 像挂在森林里的木制布告板
- 内容块上下不必完全对称，留一点生活化松弛感
- 可配叶片、贴纸、便签、日期角标

---

## 3. Passport Split

**适用**：个人介绍、角色设定、关于页

```html
<section class="passport-split">
  <aside class="passport-side">...</aside>
  <div class="passport-main">...</div>
</section>
```

```css
.passport-split {
  display: grid;
  grid-template-columns: 280px 1fr;
  gap: clamp(18px, 3vw, 32px);
  align-items: start;
}
```

要点：
- 左边固定头像、昵称、称号、印章
- 右边放简介、能力、收藏偏好、最近动态
- 移动端改为纵向堆叠

---

## 4. Bulletin Stack

**适用**：教程页、长内容页、说明页

```html
<section class="bulletin-stack">
  <article class="memo-block">...</article>
  <article class="memo-block">...</article>
</section>
```

```css
.bulletin-stack {
  display: flex;
  flex-direction: column;
  gap: clamp(18px, 2.8vw, 28px);
}
```

要点：
- 一块一块像公告、纸条、任务单往下排
- 每块可以有不同抬头，不要都长一样
- 适合把长文拆成更“能呼吸”的生活面板

---

## 5. Module Grid

**适用**：功能入口、卡片导航、组件总览

```html
<section class="module-grid">
  <div class="module-card">...</div>
  <div class="module-card">...</div>
  <div class="module-card">...</div>
</section>
```

```css
.module-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: clamp(14px, 2vw, 20px);
}
@media (max-width: 900px) {
  .module-grid { grid-template-columns: 1fr; }
}
```

要点：
- 卡片之间要有角色差异，不要只是同模板换标题
- 可以混用图鉴卡、便签卡、状态卡、入口卡

---

## 6. Collectible Shelf

**适用**：小红书卡片、收藏图鉴、灵感展示

```html
<section class="collectible-shelf">
  <div class="shelf-card tall">...</div>
  <div class="shelf-card">...</div>
</section>
```

```css
.collectible-shelf {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 18px;
}
```

要点：
- 更像“收藏卡册/展示板”，不是网页卡片列表
- 可以一高一矮、一大一小，制造收纳感

---

## 7. Guide Path Steps

**适用**：教程流程、安装步骤、新手引导

```html
<section class="guide-steps">
  <div class="guide-step">...</div>
  <div class="guide-step">...</div>
</section>
```

```css
.guide-steps {
  display: grid;
  gap: clamp(16px, 2.5vw, 24px);
}
```

要点：
- 像游戏任务链，不像企业流程图
- 用编号木牌、叶片节点、贴纸箭头来组织顺序
- 3 到 6 步最舒适

---

## 8. Board + Sidebar

**适用**：教程索引、知识看板、长页导航

```html
<section class="board-sidebar">
  <aside class="board-nav">...</aside>
  <div class="board-content">...</div>
</section>
```

```css
.board-sidebar {
  display: grid;
  grid-template-columns: 220px 1fr;
  gap: clamp(18px, 3vw, 30px);
}
```

要点：
- 左边像便签式目录或小地图
- 右边是正文模块
- 目录视觉上要像系统部件，不是普通锚点列表

---

## 9. Status Dashboard

**适用**：App 功能页、任务页、数据页

```html
<section class="status-dashboard">
  <div class="status-hero">...</div>
  <div class="status-panels">...</div>
</section>
```

```css
.status-panels {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 16px;
}
```

要点：
- 像游戏原生系统页
- 适合状态、进度、清单、地图入口组合

---

## 10. Long Letter

**适用**：公众号、长阅读、品牌发信

```html
<section class="long-letter">
  <section class="letter-head">...</section>
  <section class="letter-body">...</section>
</section>
```

要点：
- 像小岛来信、公告栏、长纸信
- 节奏靠“标题板 + 正文纸块 + 分隔贴纸”，不要靠杂志编号

---

## 11. Scene Mix

**适用**：需要更像真实生活而不是模板页的页面

建议组合：

1. `Leaf Board Banner` 做开场
2. `Passport Split` 或 `NookPhone Hero` 做角色主信息
3. `Bulletin Stack` 做正文
4. `Module Grid` / `Status Dashboard` 做功能入口
5. `Collectible Shelf` 做展示收尾

---

## 响应式规则

- 900px 以下，所有双栏结构优先折成单栏
- 手机端更像“竖版系统面板堆叠”，不要硬保桌面多栏
- 卡片之间的层级感保留，尺寸关系可以变，但语气不能变

---

## 禁忌

- 不要大面积冷灰留白
- 不要整页都是统一白卡 + 阴影的网页模板结构
- 不要使用居中对称 Hero 套路
- 不要用 Esther 旧系统里的杂志感大编号、蓝黄红三色节奏来主导 Ayu 页面
