<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/master/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/master/doc/classes/VisualShaderNodeResizableBase.xml。 -->

<div id="_class_visualshadernoderesizablebase"></div>

# VisualShaderNodeResizableBase

**继承：** [`VisualShaderNode`](class_visualshadernode.md) **<** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

**派生：** [`VisualShaderNodeCurveTexture`](class_visualshadernodecurvetexture.md), [`VisualShaderNodeCurveXYZTexture`](class_visualshadernodecurvexyztexture.md), [`VisualShaderNodeFrame`](class_visualshadernodeframe.md), [`VisualShaderNodeGroupBase`](class_visualshadernodegroupbase.md)

Base class for resizable nodes in a visual shader graph.

## 描述

Resizable nodes have a handle that allows the user to adjust their size as needed.

## 属性

|||
|:-:|:--|
| [`Vector2`](class_vector2.md) | [`size`](class_visualshadernoderesizablebase.md#class_visualshadernoderesizablebase_property_size) | ``Vector2(0, 0)`` |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_visualshadernoderesizablebase_property_size"></div>

[`Vector2`](class_vector2.md) **size** = ``Vector2(0, 0)`` <div id="class_visualshadernoderesizablebase_property_size"></div>

- `void` **set_size** ( value: [`Vector2`](class_vector2.md) )
- [`Vector2`](class_vector2.md) **get_size** ( )

The size of the node in the visual shader graph.

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
