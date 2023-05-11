## 02-margin-纵向重叠

### 代码

> 如下代码，AAA 和 BBB 之间的距离是多少？

```html
<p>AAA</p>
<p></p>
<p></p>
<p></p>
<p>BBB</p>
```

```css
p {
  font-size: 16px;
  line-height: 1;
  margin-top: 10px;
  margin-bottom: 15px;
}
```

### 查看效果

4 个 p 标签，最终效果是 p:first-child 与 p:last-child 之间的距离是 15px

### 解析

- 相邻元素的 margin-top 和 margin-bottom 会发生重叠
- 空白内容的 `<p></p>` 也会重叠
  - 指的应该是：互相会重叠+与上面的 margin-top 和 margin-bottom 也重叠

### 了解更多
