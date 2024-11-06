<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/classes/AudioEffectStereoEnhance.xml。 -->

<div id="_class_audioeffectstereoenhance"></div>

# AudioEffectStereoEnhance

**继承：** [`AudioEffect`](class_audioeffect.md) **<** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

An audio effect that can be used to adjust the intensity of stereo panning.

## 描述

An audio effect that can be used to adjust the intensity of stereo panning.

## 属性

|||
|:-:|:--|
| [`float`](class_float.md) | [`pan_pullout`](class_audioeffectstereoenhance.md#class_audioeffectstereoenhance_property_pan_pullout)         | ``1.0`` |
| [`float`](class_float.md) | [`surround`](class_audioeffectstereoenhance.md#class_audioeffectstereoenhance_property_surround)               | ``0.0`` |
| [`float`](class_float.md) | [`time_pullout_ms`](class_audioeffectstereoenhance.md#class_audioeffectstereoenhance_property_time_pullout_ms) | ``0.0`` |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_audioeffectstereoenhance_property_pan_pullout"></div>

[`float`](class_float.md) **pan_pullout** = ``1.0`` <div id="class_audioeffectstereoenhance_property_pan_pullout"></div>

- `void` **set_pan_pullout** ( value: [`float`](class_float.md) )
- [`float`](class_float.md) **get_pan_pullout** ( )

Values greater than 1.0 increase intensity of any panning on audio passing through this effect, whereas values less than 1.0 will decrease the panning intensity. A value of 0.0 will downmix audio to mono.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_audioeffectstereoenhance_property_surround"></div>

[`float`](class_float.md) **surround** = ``0.0`` <div id="class_audioeffectstereoenhance_property_surround"></div>

- `void` **set_surround** ( value: [`float`](class_float.md) )
- [`float`](class_float.md) **get_surround** ( )

该属性目前没有描述，请帮我们\ :ref:`贡献一个 <doc_updating_the_class_reference>`\ 吧！

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_audioeffectstereoenhance_property_time_pullout_ms"></div>

[`float`](class_float.md) **time_pullout_ms** = ``0.0`` <div id="class_audioeffectstereoenhance_property_time_pullout_ms"></div>

- `void` **set_time_pullout** ( value: [`float`](class_float.md) )
- [`float`](class_float.md) **get_time_pullout** ( )

该属性目前没有描述，请帮我们\ :ref:`贡献一个 <doc_updating_the_class_reference>`\ 吧！

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
