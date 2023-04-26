> * Author: licoded
> * CreateDate: 2023-04-26 09:27:51
> * LastModifyDate: 2023-04-26 09:27:51

# flex缩写属性+关键字属性值--它们的展开值你知道/能记住吗？

## 介绍&解释

- flex的缩写属性，不遵循默认值补全"缩写缺省值"（--缩写中没有指定的值）
    - 遵循的例子: border属性
        - `border: 2px;` === `border: 2px none currentColor;`
        - `border: #fff;` === `border: medium none #fff;`
        - `border: solid;` === `border: medium solid currentColor;`
    - (CSS specification)这样做/设计的目的是让flex属性的表现更符合我们日常开发需要的效果；
- flex的关键字属性也同样友好

## 具体内容

> flex属性的默认值: `flex: 0 1 auto;`

- `flex: 0;`
    - `flex: 0 1 0%;`
    - 表现为最小内容宽度，对于文字会呈现“一柱擎天”的效果
- `flex: 1;`
    - `flex: 1 1 0%;`
    - 一般设置 `flex: 1;` 就是要 `flex-basis: 0%;`, 即基础尺寸为0
- `flex: <width>;`
    - `flex: 1 1 <width>;`
    - 一般设置 `flex: <width>;` 就是要 `flex-grow: 1`, 也就是尺寸保持向外的弹性
        - 是吗? why?
- `flex: auto;`
    - `flex: 1 1 auto;`
    - auto: 自动填满剩余空间or自动收缩
- `flex: none;`
    - `flex: 0 0 auto;`
    - none: 即没有，flex子项没有弹性
    - 此时，基础尺寸由内容决定，因此通常表现为最大内容宽度