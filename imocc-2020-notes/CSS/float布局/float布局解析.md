## float 布局解析

> 这里讲的圣杯布局和双飞翼布局，效果完全相同

**圣杯布局和双飞翼布局的目的**：

- 三栏布局，中间一栏最先加载和渲染（因为内容最重要）
  - 中间一栏 -- 指渲染效果在中间的那栏
  - 最先加载和渲染 -- html 的渲染步骤/顺序是“自上而下，自外向内”
- 两侧内容宽度固定，中间内容随着宽度自适应
- 一般用于 PC 网页

**圣杯布局和双飞翼布局的技术总结**：

- 只要满足以下特点，都叫做这两种布局。。。

- 使用 float 布局
- 两侧使用 margin 负值，以便和中间内容横向重叠
- 防止中间内容被两侧覆盖，一个用 padding 一个用 margin
