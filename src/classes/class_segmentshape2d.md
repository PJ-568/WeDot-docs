<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/master/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/master/doc/classes/SegmentShape2D.xml。 -->

<div id="_class_segmentshape2d"></div>

# SegmentShape2D

**继承：** [`Shape2D`](class_shape2d.md) **<** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

A 2D line segment shape used for physics collision.

## 描述

A 2D line segment shape, intended for use in physics. Usually used to provide a shape for a [`CollisionShape2D`](class_collisionshape2d.md).

## 属性

|||
|:-:|:--|
| [`Vector2`](class_vector2.md) | [`a`](class_segmentshape2d.md#class_segmentshape2d_property_a) | ``Vector2(0, 0)``  |
| [`Vector2`](class_vector2.md) | [`b`](class_segmentshape2d.md#class_segmentshape2d_property_b) | ``Vector2(0, 10)`` |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_segmentshape2d_property_a"></div>

[`Vector2`](class_vector2.md) **a** = ``Vector2(0, 0)`` <div id="class_segmentshape2d_property_a"></div>

- `void` **set_a** ( value: [`Vector2`](class_vector2.md) )
- [`Vector2`](class_vector2.md) **get_a** ( )

The segment's first point position.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_segmentshape2d_property_b"></div>

[`Vector2`](class_vector2.md) **b** = ``Vector2(0, 10)`` <div id="class_segmentshape2d_property_b"></div>

- `void` **set_b** ( value: [`Vector2`](class_vector2.md) )
- [`Vector2`](class_vector2.md) **get_b** ( )

The segment's second point position.

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
