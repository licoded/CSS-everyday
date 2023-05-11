## 手写 clearfix

### 实现代码

```css
.clearfix:after {
  content: "";
  display: table;
  clear: both;
}
```

### 解析

为什么使用 `display: table` 而不是 `display: block`

> 因为 `display: table` 可以做到即使内容空的，也能占据行高
> 具体渲染细节，TODO...
