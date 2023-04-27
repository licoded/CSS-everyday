position 是 CSS 一个很重要的属性，设定值包括 static、absolute、relative、fixed 和 sticky 五个。

## static

默认值

## absolute

名字误导人，实际上是相对定位，相对于第一个非static的ancestor

不跟随文档流，即不会在文档流中占据位置；

> absolute的含义可能是“不跟随文档流”；relative是“跟随文档流的”;

### 一种经典的布局方法——父相子绝

> 父亲声明为 `position: relative;`，以在文档流中占位；
> 儿子声明为 `position: absolute;`，相对于父亲进行定位，就可以搞一些花里胡哨的效果啦!

## relative

跟随文档流，即会在文档流中占据位置；虽然自身显示的位置已经偏离了文档流；

### 注意：relative元素也可以设置 `left, right, top, bottom`

与 absolute 元素的差别在与
- relative相对自身; absolute相对于第一个非static的祖先;
- 若在同一方向上设置两个对立的值，比如同时设置了 left 和 right 值
    - relative会忽略 right 值 
        - 根据文档方向是 LTR（从左向右）, 则 left 属性生效；反之如果是 RTL, 则 right 属性生效
    - absolute则会根据 left 和 right 值来设置自身 宽度/width

## fixed

相对于窗口/body来定位，页面滚动不影响/改变它的位置

**适用场景**: 底部弹窗/广告; 回到顶部的导航组件; 

## sticky

设置 `top: 0` 时就表现为:

- 一开始跟relative一样, 跟随文档流
- 当滚动到满足 `top: 0` 后, 就表现得与 fixed 一致?

> A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed).

**兼容性差**: Not supported in IE/Edge 15 or earlier. Supported in Safari from version 6.1 with a -webkit- prefix.

**适用场景**: 博客网站的目录; 带header的普通网站的sidebar

## 参考链接

- https://www.bilibili.com/video/BV1iE411W7ug
- https://www.w3schools.com/cssref/pr_class_position.php