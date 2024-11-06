<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/classes/CameraTexture.xml。 -->

<div id="_class_cameratexture"></div>

# CameraTexture

**继承：** [`Texture2D`](class_texture2d.md) **<** [`Texture`](class_texture.md) **<** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

Texture provided by a [`CameraFeed`](class_camerafeed.md).

## 描述

This texture gives access to the camera texture provided by a [`CameraFeed`](class_camerafeed.md).

 **Note:** Many cameras supply YCbCr images which need to be converted in a shader.

## 属性

|||
|:-:|:--|
| [`int`](class_int.md)                     | [`camera_feed_id`](class_cameratexture.md#class_cameratexture_property_camera_feed_id)     | ``0``                                                                                                 |
| [`bool`](class_bool.md)                   | [`camera_is_active`](class_cameratexture.md#class_cameratexture_property_camera_is_active) | ``false``                                                                                             |
| [`bool`](class_bool.md)                   | resource_local_to_scene                                                                    | ``false`` (overrides [`Resource`](class_resource.md#class_resource_property_resource_local_to_scene)) |
| [FeedImage](#enum_cameraserver_feedimage) | [`which_feed`](class_cameratexture.md#class_cameratexture_property_which_feed)             | ``0``                                                                                                 |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_cameratexture_property_camera_feed_id"></div>

[`int`](class_int.md) **camera_feed_id** = ``0`` <div id="class_cameratexture_property_camera_feed_id"></div>

- `void` **set_camera_feed_id** ( value: [`int`](class_int.md) )
- [`int`](class_int.md) **get_camera_feed_id** ( )

The ID of the [`CameraFeed`](class_camerafeed.md) for which we want to display the image.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_cameratexture_property_camera_is_active"></div>

[`bool`](class_bool.md) **camera_is_active** = ``false`` <div id="class_cameratexture_property_camera_is_active"></div>

- `void` **set_camera_active** ( value: [`bool`](class_bool.md) )
- [`bool`](class_bool.md) **get_camera_active** ( )

Convenience property that gives access to the active property of the [`CameraFeed`](class_camerafeed.md).

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_cameratexture_property_which_feed"></div>

[FeedImage](#enum_cameraserver_feedimage) **which_feed** = ``0`` <div id="class_cameratexture_property_which_feed"></div>

- `void` **set_which_feed** ( value: [FeedImage](#enum_cameraserver_feedimage) )
- [FeedImage](#enum_cameraserver_feedimage) **get_which_feed** ( )

Which image within the [`CameraFeed`](class_camerafeed.md) we want access to, important if the camera image is split in a Y and CbCr component.

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
