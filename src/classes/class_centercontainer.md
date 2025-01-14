<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/master/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/master/doc/classes/CenterContainer.xml。 -->

<div id="_class_centercontainer"></div>

# CenterContainer

**继承：** [`Container`](class_container.md) **<** [`Control`](class_control.md) **<** [`CanvasItem`](class_canvasitem.md) **<** [`Node`](class_node.md) **<** [`Object`](class_object.md)

A container that keeps child controls in its center.

## 描述

**CenterContainer** is a container that keeps all of its child controls in its center at their minimum size.

## 属性

|||
|:-:|:--|
| [`bool`](class_bool.md) | [`use_top_left`](class_centercontainer.md#class_centercontainer_property_use_top_left) | ``false`` |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_centercontainer_property_use_top_left"></div>

[`bool`](class_bool.md) **use_top_left** = ``false`` <div id="class_centercontainer_property_use_top_left"></div>

- `void` **set_use_top_left** ( value: [`bool`](class_bool.md) )
- [`bool`](class_bool.md) **is_using_top_left** ( )

If `true`, centers children relative to the **CenterContainer**'s top left corner.

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
