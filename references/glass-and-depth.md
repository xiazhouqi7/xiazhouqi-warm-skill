# Glass & Depth

Warm 的玻璃是“空气感”，不是炫技。

## Header

```css
background: linear-gradient(135deg,rgba(255,255,255,.78),rgba(255,247,237,.58));
border: 1px solid rgba(255,255,255,.76);
backdrop-filter: blur(24px);
box-shadow: 0 18px 50px rgba(97,70,45,.10);
```

## Section

```css
background: rgba(255,255,255,.66);
border: 1px solid rgba(255,255,255,.70);
backdrop-filter: blur(20px);
box-shadow: 0 10px 26px rgba(97,70,45,.08);
```

## Card

```css
background: linear-gradient(145deg,rgba(255,255,255,.84),rgba(255,248,241,.62));
border: 1px solid rgba(255,255,255,.78);
backdrop-filter: blur(10px);
box-shadow: 0 8px 16px rgba(97,70,45,.04);
```

## Hard rules

- 文本背景必须足够实
- 玻璃层不能比内容更醒目
- 不使用彩虹折射
- 不使用高亮粗白边
- 不在所有小控件上重复玻璃
- `backdrop-filter` 失效时页面仍应可读
