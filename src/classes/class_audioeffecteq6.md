<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/master/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/master/doc/classes/AudioEffectEQ6.xml。 -->

<div id="_class_audioeffecteq6"></div>

# AudioEffectEQ6

**继承：** [`AudioEffectEQ`](class_audioeffecteq.md) **<** [`AudioEffect`](class_audioeffect.md) **<** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

Adds a 6-band equalizer audio effect to an audio bus. Gives you control over frequencies from 32 Hz to 10000 Hz.

Each frequency can be modulated between -60/+24 dB.

## 描述

Frequency bands:

Band 1: 32 Hz

Band 2: 100 Hz

Band 3: 320 Hz

Band 4: 1000 Hz

Band 5: 3200 Hz

Band 6: 10000 Hz

See also [`AudioEffectEQ`](class_audioeffecteq.md), [`AudioEffectEQ10`](class_audioeffecteq10.md), [`AudioEffectEQ21`](class_audioeffecteq21.md).

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
