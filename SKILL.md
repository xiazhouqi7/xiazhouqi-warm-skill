---
name: xiazhouqi-warm
description: "Build or refine calm, warm, soft, layered, mobile-first web UI in Xiazhouqi Warm｜下周七·暖杏: milk-apricot ground, pale-orange light, muted sage/mist-blue balance, restrained glass, breathing space, warm-brown typography, gentle lyrical copy, and reliable single-file HTML. Trigger on xiazhouqi-warm, Xiazhouqi Warm, 下周七·暖杏, 下周七风格, 奶杏风, 暖杏风, 奶杏+淡橙, 柔和毛玻璃, 温柔但高级."
version: 1.0.0
---

# Xiazhouqi Warm｜下周七·暖杏

**Repository:** `xiazhouqi-warm-skill`  
**Version:** `1.0.0`  
**Primary use:** 个人主页、生活档案、旅行/照片页面、日记、纪念页、温柔版账号档案、私人入口、轻量工具页  
**Core character:** 温暖、柔和、清新、克制、生活感、轻毛玻璃、移动端优先

> **温暖但不甜腻，柔和但不幼态，毛玻璃但不炫技，文艺但不空泛**

执行层原则：

> **底色给温度，玻璃给空气，留白给呼吸，字重给层级，颜色只做轻声提醒**

Warm 不是“页面全部变成米黄色”，也不是“粉橙渐变 + 大圆角 + 玻璃卡片”的网红模板。

它是一套偏个人、偏生活、偏长期保存的设计语言：以奶杏为底，以淡橙作为光感，用雾绿和雾蓝压住甜度，再通过暖棕文字、透明层次、柔和边框和细腻留白，让页面有温度但不黏腻。

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

如果“信息效率 > 氛围”，优先 `Xiazhouqi Clear｜下周七·清透`。

---

# 2. Warm 的五组张力

Warm 必须同时满足下面五组关系：

1. **温暖，但不黄**
2. **柔和，但不糊**
3. **文艺，但不矫情**
4. **玻璃，但不透明度泛滥**
5. **有设计感，但内容仍然第一**

如果只满足前半句，页面通常会变俗；如果只满足后半句，页面又会失去 Warm 的辨识度。

---

# 3. 视觉气质

Warm 第一眼应该是：

- 奶杏
- 柔光
- 轻空气感
- 有一点黄昏与植物的自然色
- 白色仍然占很大比例
- 深色文字偏暖棕，而不是纯黑
- 边框很轻
- 阴影偏暖且柔
- 页面有个人物件感，不像 SaaS Dashboard

Warm 不应该是：

- 奶茶店菜单
- 少女粉网页
- 马卡龙 UI
- 全屏暖橙渐变
- 玻璃拟态 Demo
- 过度圆润的儿童产品
- Pinterest 模板拼贴

详见 `references/philosophy.md`。

---

# 4. 基础色系统

## 4.1 Ground｜背景底色

默认三色：

```css
--warm-bg-1: #fff8ef; /* 奶杏 */
--warm-bg-2: #f5eee5; /* 燕麦灰杏 */
--warm-bg-3: #eef2ef; /* 雾绿灰 */
```

推荐背景：

```css
background:
  radial-gradient(circle at 10% 8%, rgba(255,214,168,.58), transparent 34%),
  radial-gradient(circle at 90% 4%, rgba(218,229,214,.68), transparent 32%),
  radial-gradient(circle at 86% 86%, rgba(246,198,156,.38), transparent 36%),
  linear-gradient(135deg,var(--warm-bg-1),var(--warm-bg-2) 48%,var(--warm-bg-3));
```

规则：

- 橙色是“光”，不是“底漆”
- 雾绿用于压甜度
- 背景变化要缓慢，不出现明显色块边界
- 不做高饱和黄 / 橙大面积铺色

## 4.2 Text｜文字

```css
--warm-text-main: #2e2924;
--warm-text-body: #5a514a;
--warm-text-soft: #7b7068;
--warm-text-faint: #a1968d;
```

禁用默认纯黑 `#000` 作为大面积正文。

## 4.3 Accent｜主暖色

```css
--warm-apricot: #d99a68;
--warm-apricot-deep: #b96b3d;
--warm-apricot-soft: #fff0df;
```

支持色：

```css
--warm-sage: #8db39a;
--warm-sage-soft: #edf3ee;

--warm-mist-blue: #8fb9df;
--warm-mist-blue-soft: #edf3f7;

--warm-dusty-rose: #d89490;
--warm-dusty-rose-soft: #f7ecea;

--warm-silver: #afb4bd;
```

页面默认主色家族不超过 3 组；档案型页面按分类可增加，但都必须低饱和。

详见 `references/design-system.md`。

---

# 5. 色彩比例

默认视觉比例：

> **65–75% 白 / 奶白结构 + 15–22% 奶杏背景 + 8–15% 淡橙 / 雾绿 / 雾蓝提示色**

Warm 绝对不是“所有容器都带颜色”。

大面积容器优先：

- 白
- 半透明白
- 奶白
- 非常淡的暖杏

颜色用于：

- 背景光斑
- 小标签
- 分类 badge
- 小图标底
- 小圆点
- 极淡边框
- 少量局部渐变

---

# 6. 毛玻璃系统（签名元素）

Warm 允许玻璃成为辨识度的一部分，但必须分层。

## 6.1 Header glass

```css
background: linear-gradient(
  135deg,
  rgba(255,255,255,.78),
  rgba(255,247,237,.58)
);
border: 1px solid rgba(255,255,255,.76);
backdrop-filter: blur(24px);
-webkit-backdrop-filter: blur(24px);
```

用于最上层身份 / 主题区域。

## 6.2 Section glass

```css
background: rgba(255,255,255,.66);
border: 1px solid rgba(255,255,255,.70);
backdrop-filter: blur(20px);
-webkit-backdrop-filter: blur(20px);
```

## 6.3 Card glass

```css
background: linear-gradient(
  145deg,
  rgba(255,255,255,.84),
  rgba(255,248,241,.62)
);
border: 1px solid rgba(255,255,255,.78);
backdrop-filter: blur(10px);
-webkit-backdrop-filter: blur(10px);
```

## 6.4 玻璃硬规则

- 玻璃必须能看见背后有“空气 / 背景光感”，否则没有意义
- 文字承载区域透明度不能低到影响可读性
- 不做高亮白边 + 强反射 + 彩虹折射
- 不把每一个按钮、标签、输入框都做成玻璃
- 玻璃负责气氛，不负责信息层级

详见 `references/glass-and-depth.md`。

---

# 7. 阴影系统

阴影偏暖，不使用冷黑重投影。

```css
--warm-shadow-header: 0 18px 50px rgba(97,70,45,.10);
--warm-shadow-section: 0 10px 26px rgba(97,70,45,.08);
--warm-shadow-card: 0 8px 16px rgba(97,70,45,.04);
--warm-shadow-icon: 0 10px 25px rgba(201,130,85,.22);
```

规则：

- 大结构阴影更扩散
- 卡片阴影更轻
- 同一层级阴影一致
- 不要卡片全部漂浮很高

---

# 8. 圆角系统

Warm 比 Clear 略柔，但不能“全员巨型圆角”。

```css
--warm-r-header: 28px;
--warm-r-section: 28px;
--warm-r-card: 20px;
--warm-r-small: 14px;
--warm-r-pill: 999px;
```

手机：

- Header：24–26px
- Section：22–24px
- Card：18–20px

层级顺序：

**Header / 大 Section > Card > Small control > Pill**

---

# 9. 字体与排版

默认字体：

```css
font-family:
  -apple-system,
  BlinkMacSystemFont,
  "SF Pro Text",
  "SF Pro Display",
  system-ui,
  "PingFang SC",
  "Microsoft YaHei",
  sans-serif;
```

不依赖网络字体。

建议：

- 页面标题：28–36px / `720–760`
- Section 标题：16–19px / `680–730`
- Card 标题：14–16px / `650–710`
- 正文：13–15px / `400–500`
- 元信息：11–13px
- 行高：正文 1.65–1.85

Warm 的标题可以比 Clear 更柔和，不需要极端粗体。

---

# 10. 文案规则（Warm 的核心差异）

Warm **允许轻文学感**。

但文案必须像“生活里自然写下的一句”，而不是为了文艺而文艺。

## 10.1 可接受

- `把散落在数字世界里的名字，收入一册安静的簿`
- `带着一点岛屿空气的浅色卡片`
- `像把走过的路，慢慢理了一遍`
- `把日常慢慢收好`

## 10.2 不接受

- 连续 3 个以上比喻
- 每个 Section 都写长段散文
- “云端、星河、光芒、灵魂、宇宙”同时出现
- 为没有内容的区域硬写情绪文案
- “高级感、治愈感、氛围感”这种自我描述

## 10.3 标点

- 标题 / 标签 / 导航：不加句号
- 单行短副标题：通常不加句号
- 两句以上完整描述：可以正常使用标点
- 尾页短文：允许完整标点与留白

## 10.4 密度

一个 Section 最多 1–2 句氛围文案。

> **一句有温度，胜过一段装腔**

详见 `references/typography-and-copy.md`。

---

# 11. Header 规范

Header 是 Warm 最重要的气质来源之一。

推荐组成：

- 1 个小图标 / 主题图标
- 1 个主标题
- 0–1 段副标题
- 可选极少量 chips

图标参考：

```css
.page-icon {
  width: 40px;
  height: 40px;
  border-radius: 16px;
  background: linear-gradient(135deg,#f0bd88,#d79a67);
  box-shadow: var(--warm-shadow-icon);
}
```

不要：

- 巨型 Hero 占半屏
- 5–8 个统计标签塞 Header
- 加无关 slogan
- 大面积橙色图标

---

# 12. Section 规范

Section 是“生活分区 / 语义分区”。

它需要比卡片更有呼吸。

推荐：

```css
.section {
  padding: 18px;
  border-radius: var(--warm-r-section);
  background: rgba(255,255,255,.66);
  border: 1px solid rgba(255,255,255,.70);
  box-shadow: var(--warm-shadow-section);
  backdrop-filter: blur(20px);
}
```

Section 之间：

- 16–24px
- 内容越独立，距离越大
- 同一主题连续组可更紧

> **大组呼吸，小组紧凑**

---

# 13. Card 规范

Card 不是越多越好。

Card 需要承担至少一个任务：

- 把一组信息捆在一起
- 提升一个重点
- 承载可操作内容
- 隔开需要保护 / 区分的信息

普通卡：

```css
.card {
  border-radius: 20px;
  padding: 13px 14px;
  background: linear-gradient(
    145deg,
    rgba(255,255,255,.84),
    rgba(255,248,241,.62)
  );
  border: 1px solid rgba(255,255,255,.78);
  box-shadow: var(--warm-shadow-card);
}
```

不需要每张卡都有装饰光斑。

如果使用 `::before` / `::after` 装饰，必须：

```css
pointer-events: none;
```

避免挡住复制按钮等交互。

---

# 14. 分类色

Warm 的分类色比 Clear 更“柔光化”。

示例：

- Outlook → 雾霾蓝
- Gmail → 灰粉红
- QQ → 鼠尾草绿
- Apple → 银灰
- Aliyun → 淡雾蓝
- Sina → 杏橙

Badge 可以使用柔和小渐变：

```css
background: linear-gradient(135deg,#7fb0dc,#9fc5f5);
```

但正文卡片仍然保持奶白 / 半透明白。

同类信息保持同一色系。

---

# 15. Tag / Chip

Tag 不承担主视觉。

推荐：

```css
.tag {
  font-size: 10px;
  padding: 4px 8px;
  border-radius: 999px;
  border: 1px solid rgba(190,160,130,.18);
  background: rgba(255,255,255,.82);
  color: var(--warm-text-soft);
}
```

重点 tag 可使用淡杏底，不使用实心橙色大标签。

避免：

- 5 种彩色 tag 堆在一张卡
- tag 比标题更显眼
- 所有信息都做成 pill

---

# 16. 顶部导航

默认保持在正常文档流。

**硬规则：不默认 sticky / fixed。**

短分类 ≤ 6 个时：

- 优先一排完整显示
- 先缩短文字
- 再缩小间距
- 最后才考虑横向滚动

分类很多时：

- 可以横向滚动
- 或使用紧凑 grid

Warm 导航可以有：

- 半透明白底
- 小圆点
- 轻阴影
- 很淡的 blur

但不能变成悬浮“胶囊岛”。

---

# 17. 按钮与复制控件

Warm 的工具按钮必须“轻”。

复制按钮：

- 视觉 22–26px
- 暖棕 / 淡杏
- 不使用高饱和蓝
- 不抢标题
- 实际触控范围建议 36–44px（通过 wrapper 扩展）

参考：

```css
.copy-btn {
  width: 24px;
  height: 24px;
  border: 1px solid rgba(190,135,82,.18);
  background: rgba(255,250,245,.58);
  color: rgba(154,98,59,.62);
  border-radius: 999px;
  box-shadow: 0 2px 7px rgba(180,140,100,.06);
}
```

Toast 可以 fixed，但只用于短暂反馈。

---

# 18. 图片 / 照片规范

Warm 很适合图片，但不要把照片处理成滤镜模板。

原则：

- 自然暖，不是整体橙
- 保留肤色 / 天空 / 植物真实颜色
- 允许轻微暖调与低对比
- 不加厚重暗角
- 不做发黄复古滤镜
- 不给照片套假手机框

卡片照片：

- radius 18–24px
- `object-fit: cover`
- 柔和阴影
- 文字不直接压在复杂画面上，除非有足够遮罩

旅行页：

- 主图大，文字少
- 让照片提供情绪，文案不要重复描述照片

详见 `references/photos-and-media.md`。

---

# 19. 布局与呼吸节奏

核心规律：

> **Same thought close · Same group moderate · New semantic group clearly farther**

建议：

- 页面外边距：手机 12–14px；桌面 20–24px
- Header → Nav：14–20px
- Nav → Section：16–22px
- Section 间：16–24px
- Section 内标题 → 内容：10–14px
- Card gap：10–14px
- Card 内部同组信息：4–8px

Warm 的留白是“呼吸”，不是“空旷”。

详见 `references/layout-and-spacing.md`。

---

# 20. 响应式（硬规则）

手机优先。

必须验证：

- 360px
- 375px
- 390px
- 430px
- 768px+
- 1280px

默认：

- 手机单列
- 平板根据内容 2 列
- 桌面最多 2–3 列
- 不为填满屏幕强行 4 列

防溢出：

```css
* { box-sizing: border-box; }

html, body {
  max-width: 100%;
  overflow-x: hidden;
}

.breakable {
  min-width: 0;
  overflow-wrap: anywhere;
}
```

---

# 21. iPhone / 本地 HTML

如果页面需要本地打开：

- 单文件优先
- CSS 内联优先
- SVG 内联优先
- 无 CDN
- 无网络字体
- 无外部 JS

输入框：

```css
@supports (-webkit-touch-callout:none) {
  input, textarea, select, button {
    font-size: 16px;
  }
}
```

避免 iPhone 自动放大。

---

# 22. JavaScript 使用原则

核心内容不能因为 JS 失效而整页空白。

JS 适合增强：

- copy
- Toast
- 小动画
- 轻筛选
- 非关键切换

如果是私人入口 / 密码页：

- 允许使用 JS
- 但本地预览环境要有可靠方案
- 不把核心正文放进 iframe / srcdoc
- 不声称前端密码是真加密

详见 `references/mobile-and-compatibility.md`。

---

# 23. 动效

Warm 的动效比 Clear 可以更“软”，但不能漂。

推荐：

- 150–220ms
- opacity
- translateY 2–6px
- scale .98–1
- hover 轻微提升 1–2px

禁止：

- 漂浮粒子作为常驻主视觉
- 大范围鼠标追踪光晕
- 卡片 3D 强倾斜
- 持续发光
- 呼吸灯循环
- 背景持续运动导致阅读疲劳

---

# 24. 个人主页 / 生活页模式

如果内容较少：

- 允许更大 Header
- 允许一张主图
- Section 数量减少
- 卡片不必处处存在
- 文案可以更轻、更有留白

如果内容很多：

- 减少装饰
- 缩短副标题
- Section 更清晰
- Card 更紧凑

Warm 随内容密度调整，不是固定模板。

---

# 25. 档案页模式

Warm 档案页必须同时满足：

- 有温度
- 仍然好找信息

因此：

- 分类用柔和 badge / 小圆点
- 标题清楚
- 正文对比足够
- 大量信息用 list row，不全做大卡片
- 重点账号 / 主卡可稍微抬高层级
- 历史内容退灰，不要隐藏

---

# 26. 内容与数据同步（硬规则）

如果用户只说“改成 Warm 风格”：

- 不改账号
- 不改金额
- 不改卡号
- 不改用途
- 不改密码
- 不擅自增加说明性数据

如果用户要求“按最新标准同步”：

1. 当前对话最新明确确认
2. 最新完成的独立页面
3. 最新上传文件
4. 聚合页旧副本
5. 更早文件

冲突时不要静默猜。

---

# 27. 聚合页 / 档案馆

总入口负责：

- Warm 的统一背景
- 统一 Header / 目录
- 返回逻辑
- 整体呼吸感

子模块保留自己合理的信息结构。

不要为了统一 Warm，把每个子模块都强行改成相同卡片模板。

---

# 28. 代码维护

应该：

- 一套最终 CSS
- 合并重复 media query
- 删除旧补丁
- 变量集中管理
- 注释清楚
- 保留数据完整性

不应该：

- 文件末尾持续追加 `/* fix v8 */`
- 同 selector 十几次 `!important`
- 为了一个手机问题破坏桌面
- 引入大型 UI 框架只为几个卡片
- 依赖外部资源才能看到完整风格

---

# 29. 可访问性

至少保证：

- 正文对比度够
- 暖色不能让文字变淡到难读
- 颜色不是唯一分类方式
- 按钮有 `aria-label`
- 图片有合适 `alt`
- 点击区可靠
- focus 可见
- 动效尊重 `prefers-reduced-motion`

---

# 30. Warm 与 Clear 的边界

## 选择 Warm

当关键词是：

- 生活
- 温柔
- 奶杏
- 毛玻璃
- 照片
- 日记
- 旅行
- 纪念
- 个人主页
- 有一点文艺

## 选择 Clear

当关键词是：

- 银行卡
- 财务
- 高密度
- 账号管理
- 快速扫描
- 极简
- Apple 感
- 信息优先

如果用户明确点名某个 Skill，以用户指定为准。

---

# 31. 禁止事项

Warm 默认禁止：

- 全屏纯米黄
- 大面积纯橙
- 粉色少女风
- 马卡龙彩虹卡片
- 玻璃无处不在
- 纯黑文字压在暖背景上
- 巨型圆角堆叠
- 所有内容都卡片化
- 悬浮顶部分类栏
- 过度文艺文案
- Emoji 满屏
- 3D 卡片强倾斜
- 持续粒子动画
- 为了好看发明用户信息
- 手机横向溢出
- 本地 HTML 依赖外部 CDN
- iframe / srcdoc 承载核心正文
- 复制按钮被装饰层挡住

详见 `references/anti-patterns-and-checklist.md`。

---

# 32. 执行流程

当用户说“按 xiazhouqi-warm-skill 改”：

1. **读取源文件**
   - 数据
   - 页面功能
   - 当前信息层级
   - 手机适配
   - 密码 / 复制 / 切换交互

2. **判断页面类型**
   - 个人主页
   - 生活页
   - 图片页
   - 档案页
   - 工具页

3. **判断是否应该真的使用 Warm**
   - 如果用户明确指定 Warm，执行
   - 如果未指定且信息极密，可建议 Clear，但不擅自替换

4. **先重构信息结构**
   - 大组
   - 小组
   - 主次
   - 当前 / 历史
   - 内容 / 操作

5. **建立背景**
   - 奶杏
   - 淡橙光
   - 雾绿平衡
   - 不出现高饱和

6. **建立三层透明度**
   - Header
   - Section
   - Card

7. **建立字重和间距**
   - 先层级
   - 后颜色

8. **加入少量 Warm 签名元素**
   - 柔和 badge
   - 小图标
   - 轻光斑
   - 温柔副标题

9. **移动端检查**
   - 360 / 390px
   - 长字符串
   - 导航一排
   - 按钮点击
   - 输入框

10. **代码清理**
   - 不叠 patch
   - 不依赖 CDN

11. **文案检查**
   - 有温度
   - 不堆比喻
   - 不发明内容

12. **最终验收**
   - 运行 checklist

---

# 33. 验收清单

- [ ] 第一眼温暖，但不是黄色页面
- [ ] 第一眼柔和，但文字依然清楚
- [ ] 淡橙像光，不像底色
- [ ] 雾绿 / 雾蓝成功压住甜度
- [ ] 文字使用暖棕层级
- [ ] 毛玻璃层级明确
- [ ] 玻璃没有影响可读性
- [ ] Header 没有过高
- [ ] Section 有呼吸
- [ ] Card 没有泛滥
- [ ] 文案有一点温度但不过度
- [ ] 标题 / 标签没有多余句号
- [ ] 图片自然，不是重滤镜
- [ ] 导航默认不 sticky / fixed
- [ ] ≤6 个短分类优先一排
- [ ] 360–390px 无横向溢出
- [ ] 复制按钮小而淡，但稳定点击
- [ ] 输入框不会触发 iPhone 自动放大
- [ ] 核心正文不依赖 iframe / srcdoc
- [ ] 改风格时数据未被擅自改变
- [ ] HTML 没有堆叠大量旧 CSS patch
- [ ] 页面不像网红模板
- [ ] 页面像一个“长期会留下来的个人页面”

---

# 34. 最终记忆口诀

如果只记住 10 句话：

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

---

## Reference loading

按任务需要读取：

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
- `reference.html`

**Xiazhouqi Warm｜下周七·暖杏 v1.0.0**
