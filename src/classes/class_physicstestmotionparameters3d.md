<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/classes/PhysicsTestMotionParameters3D.xml。 -->

<div id="_class_physicstestmotionparameters3d"></div>

# PhysicsTestMotionParameters3D

**继承：** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

Provides parameters for [`PhysicsServer3D.body_test_motion`](class_physicsserver3d.md#class_physicsserver3d_method_body_test_motion).

## 描述

By changing various properties of this object, such as the motion, you can configure the parameters for [`PhysicsServer3D.body_test_motion`](class_physicsserver3d.md#class_physicsserver3d_method_body_test_motion).

## 属性

|||
|:-:|:--|
| [`bool`](class_bool.md)                       | [`collide_separation_ray`](class_physicstestmotionparameters3d.md#class_physicstestmotionparameters3d_property_collide_separation_ray) | ``false``                                           |
| [Array](class_array.md) [`RID`](class_rid.md) | [`exclude_bodies`](class_physicstestmotionparameters3d.md#class_physicstestmotionparameters3d_property_exclude_bodies)                 | ``[]``                                              |
| [Array](class_array.md) [`int`](class_int.md) | [`exclude_objects`](class_physicstestmotionparameters3d.md#class_physicstestmotionparameters3d_property_exclude_objects)               | ``[]``                                              |
| [`Transform3D`](class_transform3d.md)         | [`from`](class_physicstestmotionparameters3d.md#class_physicstestmotionparameters3d_property_from)                                     | ``Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`` |
| [`float`](class_float.md)                     | [`margin`](class_physicstestmotionparameters3d.md#class_physicstestmotionparameters3d_property_margin)                                 | ``0.001``                                           |
| [`int`](class_int.md)                         | [`max_collisions`](class_physicstestmotionparameters3d.md#class_physicstestmotionparameters3d_property_max_collisions)                 | ``1``                                               |
| [`Vector3`](class_vector3.md)                 | [`motion`](class_physicstestmotionparameters3d.md#class_physicstestmotionparameters3d_property_motion)                                 | ``Vector3(0, 0, 0)``                                |
| [`bool`](class_bool.md)                       | [`recovery_as_collision`](class_physicstestmotionparameters3d.md#class_physicstestmotionparameters3d_property_recovery_as_collision)   | ``false``                                           |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_physicstestmotionparameters3d_property_collide_separation_ray"></div>

[`bool`](class_bool.md) **collide_separation_ray** = ``false`` <div id="class_physicstestmotionparameters3d_property_collide_separation_ray"></div>

- `void` **set_collide_separation_ray_enabled** ( value: [`bool`](class_bool.md) )
- [`bool`](class_bool.md) **is_collide_separation_ray_enabled** ( )

If set to `true`, shapes of type [`PhysicsServer3D.SHAPE_SEPARATION_RAY`](class_physicsserver3d.md#class_physicsserver3d_constant_shape_separation_ray) are used to detect collisions and can stop the motion. Can be useful when snapping to the ground.

If set to `false`, shapes of type [`PhysicsServer3D.SHAPE_SEPARATION_RAY`](class_physicsserver3d.md#class_physicsserver3d_constant_shape_separation_ray) are only used for separation when overlapping with other bodies. That's the main use for separation ray shapes.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_physicstestmotionparameters3d_property_exclude_bodies"></div>

[Array](class_array.md) [`RID`](class_rid.md) **exclude_bodies** = ``[]`` <div id="class_physicstestmotionparameters3d_property_exclude_bodies"></div>

- `void` **set_exclude_bodies** ( value: [Array](class_array.md) [`RID`](class_rid.md) )
- [Array](class_array.md) [`RID`](class_rid.md) **get_exclude_bodies** ( )

Optional array of body [`RID`](class_rid.md) to exclude from collision. Use [`CollisionObject3D.get_rid`](class_collisionobject3d.md#class_collisionobject3d_method_get_rid) to get the [`RID`](class_rid.md) associated with a [`CollisionObject3D`](class_collisionobject3d.md)-derived node.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_physicstestmotionparameters3d_property_exclude_objects"></div>

[Array](class_array.md) [`int`](class_int.md) **exclude_objects** = ``[]`` <div id="class_physicstestmotionparameters3d_property_exclude_objects"></div>

- `void` **set_exclude_objects** ( value: [Array](class_array.md) [`int`](class_int.md) )
- [Array](class_array.md) [`int`](class_int.md) **get_exclude_objects** ( )

Optional array of object unique instance ID to exclude from collision. See [`Object.get_instance_id`](class_object.md#class_object_method_get_instance_id).

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_physicstestmotionparameters3d_property_from"></div>

[`Transform3D`](class_transform3d.md) **from** = ``Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`` <div id="class_physicstestmotionparameters3d_property_from"></div>

- `void` **set_from** ( value: [`Transform3D`](class_transform3d.md) )
- [`Transform3D`](class_transform3d.md) **get_from** ( )

Transform in global space where the motion should start. Usually set to [`Node3D.global_transform`](class_node3d.md#class_node3d_property_global_transform) for the current body's transform.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_physicstestmotionparameters3d_property_margin"></div>

[`float`](class_float.md) **margin** = ``0.001`` <div id="class_physicstestmotionparameters3d_property_margin"></div>

- `void` **set_margin** ( value: [`float`](class_float.md) )
- [`float`](class_float.md) **get_margin** ( )

Increases the size of the shapes involved in the collision detection.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_physicstestmotionparameters3d_property_max_collisions"></div>

[`int`](class_int.md) **max_collisions** = ``1`` <div id="class_physicstestmotionparameters3d_property_max_collisions"></div>

- `void` **set_max_collisions** ( value: [`int`](class_int.md) )
- [`int`](class_int.md) **get_max_collisions** ( )

Maximum number of returned collisions, between `1` and `32`. Always returns the deepest detected collisions.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_physicstestmotionparameters3d_property_motion"></div>

[`Vector3`](class_vector3.md) **motion** = ``Vector3(0, 0, 0)`` <div id="class_physicstestmotionparameters3d_property_motion"></div>

- `void` **set_motion** ( value: [`Vector3`](class_vector3.md) )
- [`Vector3`](class_vector3.md) **get_motion** ( )

Motion vector to define the length and direction of the motion to test.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_physicstestmotionparameters3d_property_recovery_as_collision"></div>

[`bool`](class_bool.md) **recovery_as_collision** = ``false`` <div id="class_physicstestmotionparameters3d_property_recovery_as_collision"></div>

- `void` **set_recovery_as_collision_enabled** ( value: [`bool`](class_bool.md) )
- [`bool`](class_bool.md) **is_recovery_as_collision_enabled** ( )

If set to `true`, any depenetration from the recovery phase is reported as a collision; this is used e.g. by [`CharacterBody3D`](class_characterbody3d.md) for improving floor detection during floor snapping.

If set to `false`, only collisions resulting from the motion are reported, which is generally the desired behavior.

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
