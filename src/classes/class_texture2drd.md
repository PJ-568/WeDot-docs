<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/classes/Texture2DRD.xml。 -->

<div id="_class_texture2drd"></div>

# Texture2DRD

**继承：** [`Texture2D`](class_texture2d.md) **<** [`Texture`](class_texture.md) **<** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

Texture for 2D that is bound to a texture created on the [`RenderingDevice`](class_renderingdevice.md).

## 描述

This texture class allows you to use a 2D texture created directly on the [`RenderingDevice`](class_renderingdevice.md) as a texture for materials, meshes, etc.

## 属性

|||
|:-:|:--|
| [`bool`](class_bool.md) | resource_local_to_scene                                                            | ``false`` (overrides [`Resource`](class_resource.md#class_resource_property_resource_local_to_scene)) |
| [`RID`](class_rid.md)   | [`texture_rd_rid`](class_texture2drd.md#class_texture2drd_property_texture_rd_rid) |                                                                                                       |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_texture2drd_property_texture_rd_rid"></div>

[`RID`](class_rid.md) **texture_rd_rid** <div id="class_texture2drd_property_texture_rd_rid"></div>

- `void` **set_texture_rd_rid** ( value: [`RID`](class_rid.md) )
- [`RID`](class_rid.md) **get_texture_rd_rid** ( )

The RID of the texture object created on the [`RenderingDevice`](class_renderingdevice.md).

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
