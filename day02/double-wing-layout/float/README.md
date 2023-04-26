> 参考视频：https://www.bilibili.com/video/BV1nT411s76L

## 补充

> 注意：视频中包含一个额外的要求，加载顺序——即要求中间部分首先加载

“首先加载”, 按照我的理解, 是指DOM渲染层级的加载; 而DOM加载顺序是：自外向内, 自上向下

```html
<parent>
    <child-1></child-1>
    <child-2></child-2>
</parent>
```

上面代码中, DOM加载顺序是 `parent -> child-1 -> child-2`

> 自外向内: `parent -> child-*`
> 自上向下: `child-1 -> child-2`