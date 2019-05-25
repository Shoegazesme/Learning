## Day04 5月25日 星期五

| 名称           | 组合器 | 选择                                                         |
| :------------- | :----- | :----------------------------------------------------------- |
| 选择器组       | A,B    | 匹配满足A（和/或）B的任意元素（参见下方 [同一规则集上的多个选择器](https://developer.mozilla.org/zh-CN/docs/Learn/CSS/Introduction_to_CSS/Combinators_and_multiple_selectors#同一规则集上的多个选择器)）. |
| 后代选择器     | A B    | 匹配B元素，满足条件：B是A的后代结点（B是A的子节点，或者A的子节点的子节点） |
| 子选择器       | A > B  | 匹配B元素，满足条件：B是A的直接子节点                        |
| 相邻兄弟选择器 | A + B  | 匹配B元素，满足条件：B是A的下一个兄弟节点（AB有相同的父结点，并且B紧跟在A的后面） |
| 通用兄弟选择器 | A ~ B  | 匹配B元素，满足条件：B是A之后的任意一个兄弟节点（AB有相同的父节点，B在A之后，但不一定是紧挨着A） |

### 控制继承

CSS为处理继承提供了四种特殊的通用属性值：

- [`inherit`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/inherit)： 该值将应用到选定元素的属性值设置为与其父元素一样。	
- [`initial`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/initial) ：该值将应用到选定元素的属性值设置为与浏览器默认样式表中该元素设置的值一样。如果浏览器默认样式表中没有设置值，并且该属性是自然继承的，那么该属性值就被设置为 `inherit`。
- [`unset`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/unset) ：该值将属性重置为其自然值，即如果属性是自然继承的，那么它就表现得像 `inherit`，否则就是表现得像 `initial`。
- [`revert`](https://developer.mozilla.org/zh-CN/docs/Web/CSS/revert) ：如果当前的节点没有应用任何样式，则将该属性恢复到它所拥有的值。换句话说，属性值被设置成自定义样式所定义的属性（如果被设置）， 否则属性值被设置成用户代理的默认样式。