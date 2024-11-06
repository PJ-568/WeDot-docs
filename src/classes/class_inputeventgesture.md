<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/classes/InputEventGesture.xml。 -->

<div id="_class_inputeventgesture"></div>

# InputEventGesture

**继承：** [`InputEventWithModifiers`](class_inputeventwithmodifiers.md) **<** [`InputEventFromWindow`](class_inputeventfromwindow.md) **<** [`InputEvent`](class_inputevent.md) **<** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

**派生：** [`InputEventMagnifyGesture`](class_inputeventmagnifygesture.md), [`InputEventPanGesture`](class_inputeventpangesture.md)

Abstract base class for touch gestures.

## 描述

InputEventGestures are sent when a user performs a supported gesture on a touch screen. Gestures can't be emulated using mouse, because they typically require multi-touch.

## 属性

|||
|:-:|:--|
| [`Vector2`](class_vector2.md) | [`position`](#class_inputeventgesture_property_position) | ``Vector2(0, 0)`` |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_inputeventgesture_property_position"></div>

[`Vector2`](class_vector2.md) **position** = ``Vector2(0, 0)`` <div id="class_inputeventgesture_property_position"></div>

- `void` **set_position** ( value: [`Vector2`](class_vector2.md) )
- [`Vector2`](class_vector2.md) **get_position** ( )

The local gesture position relative to the [`Viewport`](class_viewport.md). If used in [`Control._gui_input`](#class_control_private_method__gui_input), the position is relative to the current [`Control`](class_control.md) that received this gesture.

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
