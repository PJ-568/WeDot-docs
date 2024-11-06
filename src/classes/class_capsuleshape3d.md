<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/classes/CapsuleShape3D.xml。 -->

<div id="_class_capsuleshape3d"></div>

# CapsuleShape3D

**继承：** [`Shape3D`](class_shape3d.md) **<** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

A 3D capsule shape used for physics collision.

## 描述

A 3D capsule shape, intended for use in physics. Usually used to provide a shape for a [`CollisionShape3D`](class_collisionshape3d.md).

 **Performance:** **CapsuleShape3D** is fast to check collisions against. It is faster than [`CylinderShape3D`](class_cylindershape3d.md), but slower than [`SphereShape3D`](class_sphereshape3d.md) and [`BoxShape3D`](class_boxshape3d.md).

## 属性

|||
|:-:|:--|
| [`float`](class_float.md) | [`height`](#class_capsuleshape3d_property_height) | ``2.0`` |
| [`float`](class_float.md) | [`radius`](#class_capsuleshape3d_property_radius) | ``0.5`` |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_capsuleshape3d_property_height"></div>

[`float`](class_float.md) **height** = ``2.0`` <div id="class_capsuleshape3d_property_height"></div>

- `void` **set_height** ( value: [`float`](class_float.md) )
- [`float`](class_float.md) **get_height** ( )

The capsule's height.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_capsuleshape3d_property_radius"></div>

[`float`](class_float.md) **radius** = ``0.5`` <div id="class_capsuleshape3d_property_radius"></div>

- `void` **set_radius** ( value: [`float`](class_float.md) )
- [`float`](class_float.md) **get_radius** ( )

The capsule's radius.

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
