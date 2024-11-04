<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/4.3/doc/classes/Variant.xml。 -->

<div id="_class_variant"></div>

# Variant

The most important data type in Godot.

## 描述

In computer programming, a Variant class is a class that is designed to store a variety of other types. Dynamic programming languages like PHP, Lua, JavaScript and GDScript like to use them to store variables' data on the backend. With these Variants, properties are able to change value types freely.



```gdscript

    var foo = 2 # foo is dynamically an integer
    foo = "Now foo is a string!"
    foo = RefCounted.new() # foo is an Object
    var bar: int = 2 # bar is a statically typed integer.
    # bar = "Uh oh! I can't make statically typed variables become a different type!"
```

```csharp

    // C# is statically typed. Once a variable has a type it cannot be changed. You can use the `var` keyword to let the compiler infer the type automatically.
    var foo = 2; // Foo is a 32-bit integer (int). Be cautious, integers in GDScript are 64-bit and the direct C# equivalent is `long`.
    // foo = "foo was and will always be an integer. It cannot be turned into a string!";
    var boo = "Boo is a string!";
    var ref = new RefCounted(); // var is especially useful when used together with a constructor.
    
    // Godot also provides a Variant type that works like a union of all the Variant-compatible types.
    Variant fooVar = 2; // fooVar is dynamically an integer (stored as a `long` in the Variant type).
    fooVar = "Now fooVar is a string!";
    fooVar = new RefCounted(); // fooVar is a GodotObject.
```



Godot tracks all scripting API variables within Variants. Without even realizing it, you use Variants all the time. When a particular language enforces its own rules for keeping data typed, then that language is applying its own custom logic over the base Variant scripting API.

- GDScript automatically wrap values in them. It keeps all data in plain Variants by default and then optionally enforces custom static typing rules on variable types.

- C# is statically typed, but uses its own implementation of the Variant type in place of Godot's **Variant** class when it needs to represent a dynamic value. C# Variant can be assigned any compatible type implicitly but converting requires an explicit cast.

The global [`@GlobalScope.typeof`](#class_@globalscope_method_typeof) function returns the enumerated value of the Variant type stored in the current variable (see [Variant.Type](#enum_@globalscope_variant.type)).



```gdscript

    var foo = 2
    match typeof(foo):
        TYPE_NIL:
            print("foo is null")
        TYPE_INT:
            print("foo is an integer")
        TYPE_OBJECT:
            # Note that Objects are their own special category.
            # To get the name of the underlying Object type, you need the `get_class()` method.
            print("foo is a(n) %s" % foo.get_class()) # inject the class name into a formatted string.
            # Note that this does not get the script's `class_name` global identifier.
            # If the `class_name` is needed, use `foo.get_script().get_global_name()` instead.
```

```csharp

    Variant foo = 2;
    switch (foo.VariantType)
    {
        case Variant.Type.Nil:
            GD.Print("foo is null");
            break;
        case Variant.Type.Int:
            GD.Print("foo is an integer");
            break;
        case Variant.Type.Object:
            // Note that Objects are their own special category.
            // You can convert a Variant to a GodotObject and use reflection to get its name.
            GD.Print($"foo is a(n) {foo.AsGodotObject().GetType().Name}");
            break;
    }
```



A Variant takes up only 20 bytes and can store almost any engine datatype inside of it. Variants are rarely used to hold information for long periods of time. Instead, they are used mainly for communication, editing, serialization and moving data around.

Godot has specifically invested in making its Variant class as flexible as possible; so much so that it is used for a multitude of operations to facilitate communication between all of Godot's systems.

A Variant:

- Can store almost any datatype.

- Can perform operations between many variants. GDScript uses Variant as its atomic/native datatype.

- Can be hashed, so it can be compared quickly to other variants.

- Can be used to convert safely between datatypes.

- Can be used to abstract calling methods and their arguments. Godot exports all its functions through variants.

- Can be used to defer calls or move data between threads.

- Can be serialized as binary and stored to disk, or transferred via network.

- Can be serialized to text and use it for printing values and editable settings.

- Can work as an exported property, so the editor can edit it universally.

- Can be used for dictionaries, arrays, parsers, etc.

 **Containers (Array and Dictionary):** Both are implemented using variants. A [`Dictionary`](class_dictionary.md) can match any datatype used as key to any other datatype. An [`Array`](class_array.md) just holds an array of Variants. Of course, a Variant can also hold a [`Dictionary`](class_dictionary.md) and an [`Array`](class_array.md) inside, making it even more flexible.

Modifications to a container will modify all references to it. A [`Mutex`](class_mutex.md) should be created to lock it if multi-threaded access is desired.









通过 C# 使用该 API 时会有显著不同，详见 :ref:`doc_c_sharp_differences`\ 。

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。