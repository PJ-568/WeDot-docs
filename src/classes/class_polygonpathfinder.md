<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/master/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/master/doc/classes/PolygonPathFinder.xml。 -->

<div id="_class_polygonpathfinder"></div>

# PolygonPathFinder

**继承：** [`Resource`](class_resource.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

该类目前没有描述，请帮我们\ :ref:`贡献一个 <doc_updating_the_class_reference>`\ 吧！

## 方法

|||
|:-:|:--|
| [`PackedVector2Array`](class_packedvector2array.md) | [`find_path`](class_polygonpathfinder.md#class_polygonpathfinder_method_find_path) ( from: [`Vector2`](class_vector2.md), to: [`Vector2`](class_vector2.md) )                                            |
| [`Rect2`](class_rect2.md)                           | [`get_bounds`](class_polygonpathfinder.md#class_polygonpathfinder_method_get_bounds) ( ) const[^const]                                                                                                   |
| [`Vector2`](class_vector2.md)                       | [`get_closest_point`](class_polygonpathfinder.md#class_polygonpathfinder_method_get_closest_point) ( point: [`Vector2`](class_vector2.md) ) const[^const]                                                |
| [`PackedVector2Array`](class_packedvector2array.md) | [`get_intersections`](class_polygonpathfinder.md#class_polygonpathfinder_method_get_intersections) ( from: [`Vector2`](class_vector2.md), to: [`Vector2`](class_vector2.md) ) const[^const]              |
| [`float`](class_float.md)                           | [`get_point_penalty`](class_polygonpathfinder.md#class_polygonpathfinder_method_get_point_penalty) ( idx: [`int`](class_int.md) ) const[^const]                                                          |
| [`bool`](class_bool.md)                             | [`is_point_inside`](class_polygonpathfinder.md#class_polygonpathfinder_method_is_point_inside) ( point: [`Vector2`](class_vector2.md) ) const[^const]                                                    |
| `void`                                              | [`set_point_penalty`](class_polygonpathfinder.md#class_polygonpathfinder_method_set_point_penalty) ( idx: [`int`](class_int.md), penalty: [`float`](class_float.md) )                                    |
| `void`                                              | [`setup`](class_polygonpathfinder.md#class_polygonpathfinder_method_setup) ( points: [`PackedVector2Array`](class_packedvector2array.md), connections: [`PackedInt32Array`](class_packedint32array.md) ) |

<!-- rst-class:: classref-section-separator -->

---

## 方法说明

<div id="_class_polygonpathfinder_method_find_path"></div>

[`PackedVector2Array`](class_packedvector2array.md) **find_path** ( from: [`Vector2`](class_vector2.md), to: [`Vector2`](class_vector2.md) )<div id="class_polygonpathfinder_method_find_path"></div>

该方法目前没有描述，请帮我们\ :ref:`贡献一个 <doc_updating_the_class_reference>`\ 吧！

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_polygonpathfinder_method_get_bounds"></div>

[`Rect2`](class_rect2.md) **get_bounds** ( ) const[^const]<div id="class_polygonpathfinder_method_get_bounds"></div>

该方法目前没有描述，请帮我们\ :ref:`贡献一个 <doc_updating_the_class_reference>`\ 吧！

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_polygonpathfinder_method_get_closest_point"></div>

[`Vector2`](class_vector2.md) **get_closest_point** ( point: [`Vector2`](class_vector2.md) ) const[^const]<div id="class_polygonpathfinder_method_get_closest_point"></div>

该方法目前没有描述，请帮我们\ :ref:`贡献一个 <doc_updating_the_class_reference>`\ 吧！

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_polygonpathfinder_method_get_intersections"></div>

[`PackedVector2Array`](class_packedvector2array.md) **get_intersections** ( from: [`Vector2`](class_vector2.md), to: [`Vector2`](class_vector2.md) ) const[^const]<div id="class_polygonpathfinder_method_get_intersections"></div>

该方法目前没有描述，请帮我们\ :ref:`贡献一个 <doc_updating_the_class_reference>`\ 吧！

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_polygonpathfinder_method_get_point_penalty"></div>

[`float`](class_float.md) **get_point_penalty** ( idx: [`int`](class_int.md) ) const[^const]<div id="class_polygonpathfinder_method_get_point_penalty"></div>

该方法目前没有描述，请帮我们\ :ref:`贡献一个 <doc_updating_the_class_reference>`\ 吧！

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_polygonpathfinder_method_is_point_inside"></div>

[`bool`](class_bool.md) **is_point_inside** ( point: [`Vector2`](class_vector2.md) ) const[^const]<div id="class_polygonpathfinder_method_is_point_inside"></div>

Returns `true` if `point` falls inside the polygon area.



```gdscript

    var polygon_path_finder = PolygonPathFinder.new()
    var points = [Vector2(0.0, 0.0), Vector2(1.0, 0.0), Vector2(0.0, 1.0)]
    var connections = [0, 1, 1, 2, 2, 0]
    polygon_path_finder.setup(points, connections)
    print(polygon_path_finder.is_point_inside(Vector2(0.2, 0.2))) # Prints true
    print(polygon_path_finder.is_point_inside(Vector2(1.0, 1.0))) # Prints false
```

```csharp

    var polygonPathFinder = new PolygonPathFinder();
    var points = new Vector2[]
    {
        new Vector2(0.0f, 0.0f),
        new Vector2(1.0f, 0.0f),
        new Vector2(0.0f, 1.0f)
    };
    var connections = new int[] { 0, 1, 1, 2, 2, 0 };
    polygonPathFinder.Setup(points, connections);
    GD.Print(polygonPathFinder.IsPointInside(new Vector2(0.2f, 0.2f))); // Prints true
    GD.Print(polygonPathFinder.IsPointInside(new Vector2(1.0f, 1.0f))); // Prints false
```







<!-- rst-class:: classref-item-separator -->

---

<div id="_class_polygonpathfinder_method_set_point_penalty"></div>

`void` **set_point_penalty** ( idx: [`int`](class_int.md), penalty: [`float`](class_float.md) )<div id="class_polygonpathfinder_method_set_point_penalty"></div>

该方法目前没有描述，请帮我们\ :ref:`贡献一个 <doc_updating_the_class_reference>`\ 吧！

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_polygonpathfinder_method_setup"></div>

`void` **setup** ( points: [`PackedVector2Array`](class_packedvector2array.md), connections: [`PackedInt32Array`](class_packedint32array.md) )<div id="class_polygonpathfinder_method_setup"></div>

Sets up **PolygonPathFinder** with an array of points that define the vertices of the polygon, and an array of indices that determine the edges of the polygon.

The length of `connections` must be even, returns an error if odd.



```gdscript

    var polygon_path_finder = PolygonPathFinder.new()
    var points = [Vector2(0.0, 0.0), Vector2(1.0, 0.0), Vector2(0.0, 1.0)]
    var connections = [0, 1, 1, 2, 2, 0]
    polygon_path_finder.setup(points, connections)
```

```csharp

    var polygonPathFinder = new PolygonPathFinder();
    var points = new Vector2[]
    {
        new Vector2(0.0f, 0.0f),
        new Vector2(1.0f, 0.0f),
        new Vector2(0.0f, 1.0f)
    };
    var connections = new int[] { 0, 1, 1, 2, 2, 0 };
    polygonPathFinder.Setup(points, connections);
```







[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
