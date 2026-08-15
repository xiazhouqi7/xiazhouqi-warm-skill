# Mobile & Compatibility

## Target widths

必须测试：

- 360px
- 375px
- 390px
- 430px
- 768px
- 1280px

## Overflow

```css
* { box-sizing: border-box; }

html, body {
  max-width: 100%;
  overflow-x: hidden;
}

.row,
.card,
.value,
.title {
  min-width: 0;
}

.breakable {
  overflow-wrap: anywhere;
}
```

## iPhone zoom

```css
@supports (-webkit-touch-callout:none) {
  input,
  textarea,
  select,
  button {
    font-size: 16px;
  }
}
```

## Copy reliability

```css
.card::before,
.card::after {
  pointer-events: none;
}

.copy-btn {
  position: relative;
  z-index: 5;
  touch-action: manipulation;
}
```

## Local HTML

优先单文件、内联 CSS / SVG、无 CDN、无网络字体、无外部 JS。

## Password / entrance

本地私人页的前端密码只是访问门槛，不是真加密。

避免：
- iframe
- srcdoc
- 把整页内容动态注入后才显示

核心正文应直接存在当前 DOM 中。
