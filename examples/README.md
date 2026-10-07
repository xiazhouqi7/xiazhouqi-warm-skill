# Examples

这些示例只演示 Xiazhouqi Warm 的信息结构、组件与视觉语言，不包含真实个人数据。

## `warm-template.html` — Canonical Reference

这是当前 Xiazhouqi Warm 的**官方全组件视觉基准母版**。

生成或重构 Warm 风格网页前，优先读取并观察这份模板，重点学习：

- 奶杏 / 燕麦灰杏 / 雾绿灰的背景平衡
- 淡橙只作为光感，不作为整页底漆
- 暖棕文字层级
- Header / Section / Card 三层轻毛玻璃
- Badge、Tag、按钮与轻量状态色
- 个人主页、生活文字、便签纸与轻文学文案
- 照片 / 旅行媒体的自然暖调容器
- 链接卡、档案列表、历史内容弱化
- Copy / Toast 等轻工具交互
- Timeline、Quote、任务、进度条
- Input / Select / Textarea / Switch / Tabs
- Accordion、私密入口、Empty State
- 手机单列与桌面 2–3 列的响应式关系

**不要机械复制示例文案或业务内容。** 应继承视觉语言、空气感、比例、间距、材质和组件逻辑，再根据真实内容重新组织页面。

如果抽象文字规则与已经确认的视觉结果出现轻微差异，`warm-template.html` 可作为视觉判断的重要基准；数据、安全、内容同步与明确硬规则仍以 `SKILL.md` 为准。

## `warm-personal-archive.html`

观察：
- 奶杏 / 淡橙 / 雾绿背景平衡
- Header / Section / Card 三层玻璃
- 温柔档案型信息结构
- 分类 badge
- 移动端一列

## `warm-life-page.html`

观察：
- 更少卡片
- 更大呼吸
- 生活型文案
- 照片 / 记录型页面如何不过度设计

## 推荐读取顺序

1. `SKILL.md`
2. `examples/warm-template.html`
3. 根据任务需要再读取 `references/`、`tokens.css` 与其他 examples

如果示例与 `SKILL.md` 的数据、安全或明确硬规则冲突，以 `SKILL.md` 为准。
