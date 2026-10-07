---
name: xiazhouqi-warm
description: "Build or refine calm, warm, soft, layered, mobile-first web UI in Xiazhouqi Warm｜下周七·暖杏: milk-apricot ground, pale-orange light, muted sage/mist-blue balance, restrained glass, breathing space, warm-brown typography, gentle lyrical copy, and reliable single-file HTML. Trigger on xiazhouqi-warm, Xiazhouqi Warm, 下周七·暖杏, 下周七风格, 奶杏风, 暖杏风, 奶杏+淡橙, 柔和毛玻璃, 温柔但高级."
version: 1.1.0
---

# Xiazhouqi Warm｜下周七·暖杏

**Repository:** `xiazhouqi-warm-skill`  
**Version:** `1.1.0`  
**Primary use:** 个人主页、生活档案、旅行/照片页面、日记、纪念页、温柔版账号档案、私人入口、轻量工具页  
**Core character:** 温暖、柔和、清新、克制、生活感、轻毛玻璃、移动端优先

> **温暖但不甜腻，柔和但不幼态，毛玻璃但不炫技，文艺但不空泛**

执行层原则：

> **底色给温度，玻璃给空气，留白给呼吸，字重给层级，颜色只做轻声提醒**

Warm 不是“页面全部变成米黄色”，也不是“粉橙渐变 + 大圆角 + 玻璃卡片”的网红模板。它是一套偏个人、偏生活、偏长期保存的设计语言：以奶杏为底，以淡橙作为光感，用雾绿和雾蓝压住甜度，再通过暖棕文字、透明层次、柔和边框和细腻留白，让页面有温度但不黏腻。

---

# 0. Canonical Reference｜官方视觉基准（硬规则）

`examples/warm-template.html` 是当前 Xiazhouqi Warm 的 **Canonical Visual Reference / 官方全组件视觉母版**。

当任务涉及创建、重构、扩展或统一 Warm 风格网页时：

1. **先读取本 `SKILL.md`**
2. **随后必须读取 `examples/warm-template.html`**
3. 先观察真实成品中的背景、玻璃层级、文字颜色、间距、卡片密度、照片容器、生活型组件与移动端行为
4. 再根据任务需要读取 `references/`、`tokens.css` 与其他 examples
5. 不复制母版文案和业务内容，只继承视觉语言、材质、比例、组件逻辑和响应式关系

视觉判断优先级：

> **用户当前明确要求 > 已确认成品 / `warm-template.html` > 本 Skill 抽象规则 > 旧示例**

但数据完整性、安全、内容同步和明确硬规则始终以用户要求与本 `SKILL.md` 为准。

母版重点覆盖：Hero、导航、摘要、个人介绍、便签、照片、链接卡、信息卡、列表、标签、Copy / Toast、Quote、Timeline、任务、进度、表单、Switch、Tabs、Alert、Accordion、私密入口、Empty State 与响应式布局。

---

# 1. 适用范围

优先用于：

- 个人主页 / About 页面
- 生活档案
- 旅行 / 照片展示
- 日记 / 年度计划 / 纪念页
- 自媒体介绍页
- 邮箱 / 账号档案（希望更有生活感时）
- 私人档案馆入口
- 轻量个人工具页
- 学习 / 项目记录页
- 需要长期保存的单文件 HTML

谨慎用于：

- 高密度银行卡 / 财务页面
- 大量账号安全信息
- 强操作后台
- 需要极高扫描速度的数据页

如果“信息效率 > 氛围”，优先 `Xiazhouqi Clear｜下周七·清透`。如果用户明确指定 Warm，则继续执行 Warm，但应主动降低装饰密度。

---

# 2. Warm 的五组张力

Warm 必须同时满足：

1. **温暖，但不黄**
2. **柔和，但不糊**
3. **文艺，但不矫情**
4. **玻璃，但不透明度泛滥**
5. **有设计感，但内容仍然第一**

第一眼应有：奶杏、柔光、轻空气感、少量黄昏与植物自然色、大量白 / 奶白、暖棕文字、轻边框、暖而柔的阴影，以及“个人物件感”。

第一眼不应像：奶茶店菜单、少女粉网页、马卡龙 UI、全屏暖橙渐变、玻璃拟态 Demo、儿童产品、Pinterest 拼贴模板或 SaaS Dashboard。

---

# 3. 基础色系统

## 3.1 Ground｜背景

```css
--warm-bg-1: #fff8ef;
--warm-bg-2: #f5eee5;
--warm-bg-3: #eef2ef;
```

推荐：

```css
background:
  radial-gradient(circle at 10% 8%, rgba(255,214,168,.58), transparent 34%),
  radial-gradient(circle at 90% 4%, rgba(218,229,214,.68), transparent 32%),
  radial-gradient(circle at 86% 86%, rgba(246,198,156,.38), transparent 36%),
  linear-gradient(135deg,var(--warm-bg-1),var(--warm-bg-2) 48%,var(--warm-bg-3));
```

硬规则：

- 橙色是“光”，不是“底漆”
- 雾绿负责压甜度
- 背景变化缓慢，不出现明显色块边界
- 不做高饱和黄 / 橙大面积铺色

## 3.2 Text｜文字

```css
--warm-text-main: #2e2924;
--warm-text-body: #5a514a;
--warm-text-soft: #7b7068;
--warm-text-faint: #a1968d;
```

大面积正文不使用纯黑 `#000`。

## 3.3 Accent｜提示色

```css
--warm-apricot: #d99a68;
--warm-apricot-deep: #b96b3d;
--warm-apricot-soft: #fff0df;
--warm-sage: #8db39a;
--warm-sage-soft: #edf3ee;
--warm-mist-blue: #8fb9df;
--warm-mist-blue-soft: #edf3f7;
--warm-dusty-rose: #d89490;
--warm-dusty-rose-soft: #f7ecea;
--warm-silver: #afb4bd;
```

默认视觉比例：

> **65–75% 白 / 奶白结构 + 15–22% 奶杏背景 + 8–15% 淡橙 / 雾绿 / 雾蓝提示色**

颜色优先用于背景光斑、小标签、badge、小图标底、小圆点、极淡边框、状态提示和少量局部渐变。

---

# 4. 三层毛玻璃系统

Warm 的签名元素之一是**克制的玻璃层次**。

### Header glass

```css
background: linear-gradient(135deg,rgba(255,255,255,.78),rgba(255,247,237,.58));
border: 1px solid rgba(255,255,255,.76);
backdrop-filter: blur(24px);
```

### Section glass

```css
background: rgba(255,255,255,.66);
border: 1px solid rgba(255,255,255,.70);
backdrop-filter: blur(20px);
```

### Card glass

```css
background: linear-gradient(145deg,rgba(255,255,255,.84),rgba(255,248,241,.62));
border: 1px solid rgba(255,255,255,.78);
backdrop-filter: blur(10px);
```

硬规则：

- 玻璃必须能看见背后的空气 / 光感，否则没有意义
- 玻璃负责气氛，不负责信息层级
- 不把每个按钮、标签、输入框都做成玻璃
- 不做高亮白边、强反射、彩虹折射
- 文字承载区域透明度必须保证可读性

---

# 5. 阴影与圆角

阴影偏暖，不使用冷黑重投影。

```css
--warm-shadow-header: 0 18px 50px rgba(97,70,45,.10);
--warm-shadow-section: 0 10px 26px rgba(97,70,45,.08);
--warm-shadow-card: 0 8px 16px rgba(97,70,45,.04);
--warm-shadow-icon: 0 10px 25px rgba(201,130,85,.22);
```

圆角：

```css
--warm-r-header: 28px;
--warm-r-section: 28px;
--warm-r-card: 20px;
--warm-r-small: 14px;
--warm-r-pill: 999px;
```

层级顺序：`Header / Section > Card > Small control > Pill`。Warm 比 Clear 略柔，但禁止“全员巨型圆角”。

---

# 6. 字体与文案

默认使用系统字体，不依赖网络字体。

建议：

- 页面标题：28–36px / `720–760`
- Section：16–19px / `680–730`
- Card：14–16px / `650–710`
- 正文：13–15px / `400–500`
- 元信息：11–13px
- 正文行高：1.65–1.85

Warm 允许轻文学感，但必须像生活里自然写下的一句。

可接受：

- `把日常慢慢收好`
- `像把走过的路，慢慢理了一遍`
- `带着一点岛屿空气的浅色卡片`

禁止：

- 连续 3 个以上比喻
- 每个 Section 都写长散文
- 同时堆“云端、星河、光芒、灵魂、宇宙”等词
- 用“高级感 / 治愈感 / 氛围感”自我描述

> **一句有温度，胜过一段装腔**

标题 / 标签 / 导航和单行短副标题默认不加句号。

---

# 7. Header / Section / Card

Header 是 Warm 最重要的气质来源之一。推荐：小图标 + 主标题 + 0–1 段副标题 + 极少量 chips。不要巨型 Hero 占半屏，也不要堆 5–8 个统计标签。

Section 是生活 / 语义分区，要比 Card 更有呼吸。

> **大组呼吸，小组紧凑**

Card 不是默认容器。它至少要承担一个任务：捆住一组信息、抬高重点、承载操作或隔开需要保护的信息。

禁止所有内容卡片化。文字、照片、List row、Timeline、便签、Quote、空状态等都可以成为页面结构的一部分。

装饰伪元素必须 `pointer-events:none`，不得挡住复制等交互。

---

# 8. Badge / Tag / 导航 / 按钮

分类色比 Clear 更“柔光化”，同类信息保持同一色系。正文卡片仍以奶白 / 半透明白为主。

Tag 不承担主视觉：小、淡、少。不要一张卡塞 5 种彩色标签，也不要所有信息都做成 pill。

顶部导航默认保持正常文档流，**不默认 sticky / fixed**。短分类优先完整显示，分类多时才横向滚动或紧凑 grid。

Warm 的工具按钮必须轻。复制按钮视觉可以小，但触控区要稳定；不使用高饱和蓝。

Toast 可以 fixed，但只用于短暂反馈。

---

# 9. 图片 / 照片 / 生活物件

Warm 很适合图片，但不要把照片处理成滤镜模板。

原则：

- 自然暖，不整体发橙
- 保留肤色、天空、植物真实颜色
- 允许轻微暖调与低对比
- 不加厚暗角
- 不做发黄复古滤镜
- 不给照片套假手机框

旅行页：主图大、文字少，让照片提供情绪，文案不要重复描述照片。

生活页允许便签、纸张、咖啡、桌面等“个人物件感”组件，但不要把页面做成手账素材拼贴。

---

# 10. 列表 / 历史 / 计划 / 表单

大量档案信息优先使用 List row，不强行变成一长串大卡片。

历史 / 低频内容：降低阴影和文字对比，自然退后，不必隐藏。

Warm 可以做任务与计划，但任务感要轻：完成后降低存在感，不把页面做成 KPI Dashboard。

进度条使用低饱和暖杏、雾绿或雾蓝，不用高饱和主色。

Input / Select / Textarea 保持暖白、轻边框、清楚 focus；Switch、Tabs 与 Alert 只做轻量状态表达，不做“水晶控件”。

Accordion 用于重要但低频的信息，默认减少主页面噪音。

---

# 11. 私密入口与安全表达

私密入口继续使用 Warm 的奶杏、暖白与轻玻璃，不需要黑色保险箱 / 黑客风。

前端单文件密码只是一层界面访问门槛，不是真正数据加密。不得声称它能保护 HTML 源码中的敏感信息。

核心正文禁止通过 iframe / srcdoc 承载。

---

# 12. 布局与响应式（硬规则）

核心节奏：

> **Same thought close · Same group moderate · New semantic group clearly farther**

建议：

- 手机外边距：12–14px
- 桌面外边距：20–24px
- Header → Nav：14–20px
- Nav → Section：16–22px
- Section 间：16–24px
- Card gap：10–14px
- 同组信息：4–8px

必须验证：360 / 375 / 390 / 430 / 768+ / 1280px。

默认手机单列；平板 2 列；桌面最多 2–3 列，不为填满屏幕强行 4 列。

```css
* { box-sizing: border-box; }
html,body { max-width:100%; overflow-x:hidden; }
.breakable { min-width:0; overflow-wrap:anywhere; }
```

iPhone：

```css
@supports (-webkit-touch-callout:none) {
  input,textarea,select,button { font-size:16px; }
}
```

避免输入框自动放大。

---

# 13. JavaScript / 单文件可靠性

需要本地打开时优先：单 HTML、内联 CSS、内联 SVG、无 CDN、无网络字体、无外部 JS。

JS 优先用于增强：Copy、Toast、小动画、轻筛选、非关键切换。

关键正文不能因为 JS 失效而整页空白。

Warm 动效推荐 150–220ms、opacity、translateY 2–6px、scale .98–1、hover 轻微提升 1–2px。

禁止粒子常驻、鼠标追踪大光晕、3D 强倾斜、持续发光、呼吸灯和干扰阅读的背景运动。

---

# 14. 内容与数据同步（硬规则）

如果用户只说“改成 Warm 风格”：

- 不改账号
- 不改金额
- 不改卡号
- 不改用途
- 不改密码
- 不擅自增加说明性数据

要求按最新内容同步时，优先级：

1. 当前对话最新明确确认
2. 最新完成的独立页面
3. 最新上传文件
4. 聚合页旧副本
5. 更早文件

冲突时不静默猜测。

总入口统一背景、Header、目录、返回逻辑和整体呼吸感；内部模块保留合理的信息结构，不为了统一 Warm 强行变成相同卡片模板。

---

# 15. 代码维护

应该：

- 一套最终 CSS
- 变量集中管理
- 合并重复 media query
- 删除旧 patch
- class 语义清楚
- 保留数据完整性

不应该：

- 文件末尾长期堆 `fix v8 / v9`
- 同 selector 十几次 `!important`
- 为了手机修复破坏桌面
- 为几张卡引入大型 UI 框架
- 依赖外部资源才能呈现完整风格

---

# 16. 可访问性

至少保证：

- 正文对比度足够
- 暖色不让文字淡到难读
- 颜色不是唯一分类方式
- 按钮有 `aria-label`
- 图片有合适 `alt`
- 点击区可靠
- focus 可见
- 尊重 `prefers-reduced-motion`

---

# 17. 默认禁止事项

- 全屏纯米黄
- 大面积纯橙
- 粉色少女风
- 马卡龙彩虹卡片
- 玻璃无处不在
- 纯黑文字压暖背景
- 巨型圆角堆叠
- 所有内容都卡片化
- 悬浮顶部分类栏
- 过度文艺文案
- Emoji 满屏
- 3D 卡片强倾斜
- 持续粒子动画 / 呼吸灯
- 为了好看发明用户信息
- 手机横向溢出
- 本地 HTML 依赖外部 CDN
- iframe / srcdoc 承载核心正文
- 复制按钮被装饰层挡住
- 把 Warm 做成奶茶店 / 网红模板

---

# 18. 执行流程

当用户说“按 xiazhouqi-warm-skill 做 / 改”时：

1. 读取 `SKILL.md`
2. **读取 `examples/warm-template.html`，先对齐真实视觉基准**
3. 读取源文件，确认数据、功能、结构、移动端与交互
4. 判断页面类型和内容密度
5. 先重构信息分组，再做视觉
6. 建立奶杏 + 淡橙光 + 雾绿 / 雾蓝平衡背景
7. 建立 Header / Section / Card 三层透明度
8. 用字重、留白和结构做主次，颜色只做轻提示
9. 根据内容选择照片、便签、List、Card、Timeline、Quote、Task、Form 等组件，不机械复制母版
10. 检查 360–390px、长字符串、输入框、按钮和无横向溢出
11. 确保 JS 失效时核心内容仍可读取
12. 删除多余 patch 和无意义说明
13. 最后对照 `warm-template.html` 与验收清单复核

---

# 19. 验收清单

- [ ] 第一眼温暖，但不是黄色页面
- [ ] 第一眼柔和，但文字依然清楚
- [ ] 淡橙像光，不像底漆
- [ ] 雾绿 / 雾蓝成功压住甜度
- [ ] 文字使用暖棕层级
- [ ] Header / Section / Card 玻璃层级明确
- [ ] 玻璃没有影响可读性
- [ ] Header 没有过高
- [ ] Section 有呼吸
- [ ] Card 没有泛滥
- [ ] 文案有一点温度但不过度
- [ ] 图片自然，不是重滤镜
- [ ] 导航默认不 sticky / fixed
- [ ] 360–390px 无横向溢出
- [ ] 复制按钮小而淡，但稳定点击
- [ ] 输入框不会触发 iPhone 自动放大
- [ ] 核心正文不依赖 iframe / srcdoc
- [ ] 改风格时数据未被擅自改变
- [ ] HTML 没有堆叠大量旧 CSS patch
- [ ] 页面不像网红模板或 SaaS Dashboard
- [ ] 页面像一个长期会留下来的个人页面
- [ ] 最终视觉与 `examples/warm-template.html` 属于同一设计语言

---

# 20. 最终记忆口诀

1. **Warm 不是全屏米黄**
2. **橙色是光，不是底漆**
3. **雾绿和雾蓝负责压甜度**
4. **暖棕文字比纯黑更适合 Warm**
5. **玻璃给空气，不给信息层级**
6. **大组呼吸，小组紧凑**
7. **一句有温度，胜过一段装腔**
8. **卡片必须有工作，不是默认容器**
9. **手机真实使用，比桌面 Demo 更重要**
10. **温暖但不甜腻，柔和但不幼态**
11. **先看真实母版，再开始设计**

---

## Reference loading

### Mandatory first read

- `examples/warm-template.html` — **Canonical Visual Reference**，创建或重构 Warm 网页时必须优先读取

### Read as needed

- `references/philosophy.md`
- `references/design-system.md`
- `references/typography-and-copy.md`
- `references/glass-and-depth.md`
- `references/layout-and-spacing.md`
- `references/components-and-navigation.md`
- `references/photos-and-media.md`
- `references/mobile-and-compatibility.md`
- `references/content-sync-and-maintenance.md`
- `references/anti-patterns-and-checklist.md`
- `tokens.css`
- `examples/warm-personal-archive.html`
- `examples/warm-life-page.html`
- `reference.html` — 兼容入口，会指向 canonical template

**Xiazhouqi Warm｜下周七·暖杏 v1.1.0**
