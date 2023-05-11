## HTML 语义化

### 毫无语义化的版本

```html
<div>标题</div>
<div>
  <div>一段文字</div>
  <div>
    <div>列表1</div>
    <div>列表2</div>
  </div>
</div>
```

### 语义化比较好的版本

```html
<h1>标题</h1>
<div>
  <p>一段文字</p>
  <ul>
    <li>列表1</li>
    <li>列表2</li>
  </ul>
</div>
```

### HTML 语义化的意义

- 让人更容易读懂（增加带啊吗可读性）
- 让搜索引擎更容易读懂（SEO）

## 块级元素&内联元素

- display: block/table; 有 div h1 h2 table ul ol p 等
- display: inline/inline-block; 有 span img input button 等

> 差别在于是否能独占一行
