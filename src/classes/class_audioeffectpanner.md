<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/classes/AudioEffectPanner.xml。 -->

<div id="_class_audioeffectpanner"></div>

# AudioEffectPanner

**继承：** [`AudioEffect`](class_audioeffect.md) **<** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

Adds a panner audio effect to an audio bus. Pans sound left or right.

## 描述

Determines how much of an audio signal is sent to the left and right buses.

## 属性

|||
|:-:|:--|
| [`float`](class_float.md) | [`pan`](class_audioeffectpanner.md#class_audioeffectpanner_property_pan) | ``0.0`` |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_audioeffectpanner_property_pan"></div>

[`float`](class_float.md) **pan** = ``0.0`` <div id="class_audioeffectpanner_property_pan"></div>

- `void` **set_pan** ( value: [`float`](class_float.md) )
- [`float`](class_float.md) **get_pan** ( )

Pan position. Value can range from -1 (fully left) to 1 (fully right).

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
