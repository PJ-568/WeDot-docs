<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/master/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/master/doc/classes/Tweener.xml。 -->

<div id="_class_tweener"></div>

# Tweener

**继承：** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

**派生：** [`CallbackTweener`](class_callbacktweener.md), [`IntervalTweener`](class_intervaltweener.md), [`MethodTweener`](class_methodtweener.md), [`PropertyTweener`](class_propertytweener.md)

Abstract class for all Tweeners used by [`Tween`](class_tween.md).

## 描述

Tweeners are objects that perform a specific animating task, e.g. interpolating a property or calling a method at a given time. A **Tweener** can't be created manually, you need to use a dedicated method from [`Tween`](class_tween.md).

<!-- rst-class:: classref-section-separator -->

---

## 信号

<div id="_class_class_tweener_signal_finished"></div>

**finished** ( ) <div id="class_tweener_signal_finished"></div>

Emitted when the **Tweener** has just finished its job or became invalid (e.g. due to a freed object).

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
