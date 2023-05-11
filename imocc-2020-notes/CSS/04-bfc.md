## 04-bfc

### questions

- 什么是 BFC？如何应用？

### 解析

**什么是 BFC**:

- block format context，块级格式上下文
- 一块独立渲染区域，内部元素的渲染不会影响边界以外的元素

**形成 BFC 的常见条件:**

- float 不是 none
- position 是 absolute 或 fixed
- overflow 不是 visible
- display 是 flex inline-block 等

**BFC的常见应用:**

- 清除浮动