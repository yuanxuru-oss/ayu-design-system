# 组件库

> Ayu 小岛系统组件说明。UI 基础语汇优先参考 `animal-island-ui`，强调 NookPhone、图鉴、护照卡、便签卡、可收集条目等原生小岛组件感，而不是通用网页组件库。

## 使用原则

- **先选组件家族，再写内容。** 不要先写一堆内容，再硬塞进不合适的壳子里。
- **同类内容用同类组件。** 一个页面里不要同时出现三四种完全不同的卡片逻辑。
- **优先系统感，不优先花哨。** 这套系统的目标不是“组件很多”，而是“像住在同一个游戏手机 / 小岛系统里”。
- **默认不用 HTML 原生样式。** 引用、列表、状态、步骤、说明，都要通过下列组件家族去表达。

---

## 组件家族索引

| 家族 | 适用场景 | 关键词 |
|------|------|------|
| Passport Card | 人物页、作者信息、状态档案 | resident / identity / profile |
| Module Entry Card | App 页、导航页、图鉴入口 | entry / app / icon / module |
| Memo Card | 提示、规则、说明、灵感 | memo / note / paper / notice |
| Collectible Card | 小红书卡片、图鉴条目、角色卡 | collectible / entry / catalog |
| Status Panel | 任务、进度、里程、天气、状态 | progress / status / miles |
| Board Panel | Landing、教程页、长说明块 | board / notice / guide |
| WeChat Reading Block | 公众号长文、专栏、长阅读模式 | article / longform / reading |

---

## 1. Passport Card

适用场景：作者信息、角色资料页、品牌档案、状态卡。

气质要求：
- 像游戏里的居民护照
- 头像始终是视觉中心
- 信息字段要精炼，不做复杂表单感

推荐结构：

```html
<section class="passport-card">
  <div class="passport-head">
    <span>RESIDENT</span>
    <span>AYU ISLAND</span>
  </div>
  <div class="passport-body">
    <img src="avatar.png" alt="Ayu avatar">
    <div>
      <h3>阿鱼 Ayu</h3>
      <p>想成为魔法抽卡师的小巫师</p>
      <div class="passport-meta">
        <div class="k">身份</div><div>小岛居民 / 魔法抽卡师</div>
        <div class="k">状态</div><div>灵感活跃中</div>
      </div>
    </div>
  </div>
</section>
```

---

## 2. Module Entry Card

适用场景：App 入口、Landing 导航模块、图鉴分类入口、功能列表。

气质要求：
- 必须带 icon 或 icon 感
- 更像 NookPhone 入口块，不像网页功能卡
- 文字短、功能清楚

推荐结构：

```html
<article class="module-entry">
  <div class="entry-icon">
    <img src="animal-island-icons/icon-design.svg" alt="">
  </div>
  <div>
    <h3>图鉴入口</h3>
    <p>适合知识分类、条目入口、收藏目录。</p>
  </div>
</article>
```

可用 icon 方向：
- `critterpedia`
- `design`
- `map`
- `diy`
- `miles`
- `shopping`
- `chat`
- `camera`

---

## 3. Memo Card

适用场景：说明、提示、规则、编辑注、灵感卡、侧边便签。

气质要求：
- 有纸条 / 便签 / 胶带感
- 适合短内容，不适合超长正文
- 是生活感的重要来源

推荐结构：

```html
<article class="memo-card">
  <h3>小岛提示</h3>
  <p>这里适合放说明、规则或一句灵感，不要写成很重的正文区块。</p>
</article>
```

---

## 4. Collectible Card

适用场景：小红书图文卡片、图鉴页、角色条目页、收藏页。

气质要求：
- 要有“可收集”的感觉
- 更像条目 / 卡册 / 图鉴页
- 不要做成普通网页介绍卡

推荐结构：

```html
<article class="collectible-card">
  <div class="collect-head">COLLECTIBLE</div>
  <div class="collect-body">
    <span class="collect-stamp">角色设定卡</span>
    <h3>阿鱼的小巫师身份</h3>
    <p>适合放称号、欢迎语、人物设定或今日签语。</p>
  </div>
</article>
```

---

## 5. Status Panel

适用场景：里程、任务、阶段进度、天气、今日状态、数据摘要。

气质要求：
- 更像游戏内状态面板
- 可以有 badge / meter / progress
- 不要做成企业 dashboard

推荐结构：

```html
<section class="status-panel">
  <h3>状态面板</h3>
  <div class="status-row">
    <div class="status-item">
      <b>里程标记</b>
      <span class="status-badge">72%</span>
    </div>
  </div>
</section>
```

---

## 6. Board Panel

适用场景：Landing 主介绍区、教程说明块、长说明容器、内容导航。

气质要求：
- 像公告板，不像 SaaS 模块
- 可以承载长说明，但不能太“文档产品”
- 适合和 Memo / Passport / Entry 组件混排

推荐结构：

```html
<section class="board-panel">
  <h2>欢迎来到阿鱼的小岛</h2>
  <p>这里适合承接一段较长说明，但它仍然应该像生活化的品牌公告板。</p>
</section>
```

---

## 7. WeChat Reading Block

适用场景：公众号排版、专栏、长阅读页面。

气质要求：
- 是“小岛系统里的长阅读模式”
- 更像公告板 / 长信 / 阅读界面
- 不沿用 Esther 旧杂志编号风

推荐块类型：
- 顶部人物引导块
- 居中金句块
- 入口式段落块
- Memo 式说明块
- 阅读型章节块

---

## 组件选择建议

### App 页面
- 主组件：`Module Entry Card` + `Status Panel`
- 辅组件：`Passport Card` + `Memo Card`

### Landing 页面
- 主组件：`Board Panel` + `Passport Card`
- 辅组件：`Module Entry Card` + `Memo Card`

### Tutorial 页面
- 主组件：`Board Panel` + `Memo Card`
- 辅组件：`Passport Card` + `Status Panel`

### Cards 页面
- 主组件：`Collectible Card`
- 辅组件：`Memo Card` + `Passport Card`

### WeChat 页面
- 主组件：`WeChat Reading Block`
- 辅组件：`Memo Card` + `Passport Card`

---

## 禁止事项

- 禁止回到 Esther 旧的 51 组件目录思路
- 禁止使用 Fraunces / Inter / 旧蓝黄红气质作为默认组件基础
- 禁止把页面做成“组件展览会”
- 禁止默认 `<blockquote>`、默认 `<ul>`、默认 `<table>`
- 禁止用企业 dashboard 的视觉去做状态面板

---

## 一句话判断

如果一个组件截图单独拿出来，看不出它属于阿鱼的小岛系统，那它就还不够对。
