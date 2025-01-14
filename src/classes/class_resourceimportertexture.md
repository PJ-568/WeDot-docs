<!-- ⚠ 请勿编辑本文件 ⚠ -->
<!-- 本文档使用脚本从 WeDot 引擎源码仓库生成。 -->
<!-- 生成脚本：https://github.com/WeDot-Engine/WeDot/tree/master/doc/tools/make_md.py； -->
<!-- 原文件：https://github.com/WeDot-Engine/WeDot/tree/master/doc/classes/ResourceImporterTexture.xml。 -->

<div id="_class_resourceimportertexture"></div>

# ResourceImporterTexture

**继承：** [`ResourceImporter`](class_resourceimporter.md) **<** [`RefCounted`](class_refcounted.md) **<** [`Object`](class_object.md)

Imports an image for use in 2D or 3D rendering.

## 描述

This importer imports [`CompressedTexture2D`](class_compressedtexture2d.md) resources. If you need to process the image in scripts in a more convenient way, use [`ResourceImporterImage`](class_resourceimporterimage.md) instead. See also [`ResourceImporterLayeredTexture`](class_resourceimporterlayeredtexture.md).

## 属性

|||
|:-:|:--|
| [`int`](class_int.md)       | [`compress/channel_pack`](class_resourceimportertexture.md#class_resourceimportertexture_property_compress/channel_pack)                                     | ``0``     |
| [`int`](class_int.md)       | [`compress/hdr_compression`](class_resourceimportertexture.md#class_resourceimportertexture_property_compress/hdr_compression)                               | ``1``     |
| [`bool`](class_bool.md)     | [`compress/high_quality`](class_resourceimportertexture.md#class_resourceimportertexture_property_compress/high_quality)                                     | ``false`` |
| [`float`](class_float.md)   | [`compress/lossy_quality`](class_resourceimportertexture.md#class_resourceimportertexture_property_compress/lossy_quality)                                   | ``0.7``   |
| [`int`](class_int.md)       | [`compress/mode`](class_resourceimportertexture.md#class_resourceimportertexture_property_compress/mode)                                                     | ``0``     |
| [`int`](class_int.md)       | [`compress/normal_map`](class_resourceimportertexture.md#class_resourceimportertexture_property_compress/normal_map)                                         | ``0``     |
| [`int`](class_int.md)       | [`detect_3d/compress_to`](class_resourceimportertexture.md#class_resourceimportertexture_property_detect_3d/compress_to)                                     | ``1``     |
| [`bool`](class_bool.md)     | [`editor/convert_colors_with_editor_theme`](class_resourceimportertexture.md#class_resourceimportertexture_property_editor/convert_colors_with_editor_theme) | ``false`` |
| [`bool`](class_bool.md)     | [`editor/scale_with_editor_scale`](class_resourceimportertexture.md#class_resourceimportertexture_property_editor/scale_with_editor_scale)                   | ``false`` |
| [`bool`](class_bool.md)     | [`mipmaps/generate`](class_resourceimportertexture.md#class_resourceimportertexture_property_mipmaps/generate)                                               | ``false`` |
| [`int`](class_int.md)       | [`mipmaps/limit`](class_resourceimportertexture.md#class_resourceimportertexture_property_mipmaps/limit)                                                     | ``-1``    |
| [`bool`](class_bool.md)     | [`process/fix_alpha_border`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/fix_alpha_border)                               | ``true``  |
| [`bool`](class_bool.md)     | [`process/hdr_as_srgb`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/hdr_as_srgb)                                         | ``false`` |
| [`bool`](class_bool.md)     | [`process/hdr_clamp_exposure`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/hdr_clamp_exposure)                           | ``false`` |
| [`bool`](class_bool.md)     | [`process/normal_map_invert_y`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/normal_map_invert_y)                         | ``false`` |
| [`bool`](class_bool.md)     | [`process/premult_alpha`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/premult_alpha)                                     | ``false`` |
| [`int`](class_int.md)       | [`process/size_limit`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/size_limit)                                           | ``0``     |
| [`int`](class_int.md)       | [`roughness/mode`](class_resourceimportertexture.md#class_resourceimportertexture_property_roughness/mode)                                                   | ``0``     |
| [`String`](class_string.md) | [`roughness/src_normal`](class_resourceimportertexture.md#class_resourceimportertexture_property_roughness/src_normal)                                       | ``""``    |
| [`float`](class_float.md)   | [`svg/scale`](class_resourceimportertexture.md#class_resourceimportertexture_property_svg/scale)                                                             | ``1.0``   |

<!-- rst-class:: classref-section-separator -->

---

## 属性说明

<div id="_class_resourceimportertexture_property_compress/channel_pack"></div>

[`int`](class_int.md) **compress/channel_pack** = ``0`` <div id="class_resourceimportertexture_property_compress/channel_pack"></div>

Controls how color channels should be used in the imported texture.

 **sRGB Friendly:** Prevents the RG color format from being used, as it does not support sRGB color.

 **Optimized:** Allows the RG color format to be used if the texture does not use the blue channel. This reduces memory usage if the texture's blue channel can be discarded (all pixels must have a blue value of `0`).

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_compress/hdr_compression"></div>

[`int`](class_int.md) **compress/hdr_compression** = ``1`` <div id="class_resourceimportertexture_property_compress/hdr_compression"></div>

Controls how VRAM compression should be performed for HDR images.

 **Disabled:** Never use VRAM compression for HDR textures, regardless of whether they're opaque or transparent. Instead, the texture is converted to RGBE9995 (9-bits per channel + 5-bit exponent = 32 bits per pixel) to reduce memory usage compared to a half-float or single-precision float image format.

 **Opaque Only:** Only uses VRAM compression for opaque HDR textures. This is due to a limitation of HDR formats, as there is no VRAM-compressed HDR format that supports transparency at the same time.

 **Always:** Force VRAM compression even for HDR textures with an alpha channel. To perform this, the alpha channel is discarded on import.

 **Note:** Only effective on Radiance HDR (`.hdr`) and OpenEXR (`.exr`) images.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_compress/high_quality"></div>

[`bool`](class_bool.md) **compress/high_quality** = ``false`` <div id="class_resourceimportertexture_property_compress/high_quality"></div>

If `true`, uses BPTC compression on desktop platforms and ASTC compression on mobile platforms. When using BPTC, BC7 is used for SDR textures and BC6H is used for HDR textures.

If `false`, uses the faster but lower-quality S3TC compression on desktop platforms and ETC2 on mobile/web platforms. When using S3TC, DXT1 (BC1) is used for opaque textures and DXT5 (BC3) is used for transparent or normal map (RGTC) textures.

BPTC and ASTC support VRAM compression for HDR textures, but S3TC and ETC2 do not (see [`compress/hdr_compression`](class_resourceimportertexture.md#class_resourceimportertexture_property_compress/hdr_compression)).

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_compress/lossy_quality"></div>

[`float`](class_float.md) **compress/lossy_quality** = ``0.7`` <div id="class_resourceimportertexture_property_compress/lossy_quality"></div>

The quality to use when using the **Lossy** compression mode. Higher values result in better quality, at the cost of larger file sizes. Lossy quality does not affect memory usage of the imported texture, only its file size on disk.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_compress/mode"></div>

[`int`](class_int.md) **compress/mode** = ``0`` <div id="class_resourceimportertexture_property_compress/mode"></div>

The compression mode to use. Each compression mode provides a different tradeoff:

 **Lossless**: Original quality, high memory usage, high size on disk, fast import.

 **Lossy:** Reduced quality, high memory usage, low size on disk, fast import.

 **VRAM Compressed:** Reduced quality, low memory usage, low size on disk, slowest import. Only use for textures in 3D scenes, not for 2D elements.

 **VRAM Uncompressed:** Original quality, high memory usage, highest size on disk, fastest import.

 **Basis Universal:** Reduced quality, low memory usage, lowest size on disk, slow import. Only use for textures in 3D scenes, not for 2D elements.

See [*Compress mode*](../tutorials/assets_pipeline/importing_images.md#compress-mode) in the manual for more details.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_compress/normal_map"></div>

[`int`](class_int.md) **compress/normal_map** = ``0`` <div id="class_resourceimportertexture_property_compress/normal_map"></div>

When using a texture as normal map, only the red and green channels are required. Given regular texture compression algorithms produce artifacts that don't look that nice in normal maps, the RGTC compression format is the best fit for this data. Forcing this option to Enable will make Godot import the image as RGTC compressed. By default, it's set to Detect. This means that if the texture is ever detected to be used as a normal map, it will be changed to Enable and reimported automatically.

Note that RGTC compression affects the resulting normal map image. You will have to adjust custom shaders that use the normal map's blue channel to take this into account. Built-in material shaders already ignore the blue channel in a normal map (regardless of the actual normal map's contents).

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_detect_3d/compress_to"></div>

[`int`](class_int.md) **detect_3d/compress_to** = ``1`` <div id="class_resourceimportertexture_property_detect_3d/compress_to"></div>

This changes the [`compress/mode`](class_resourceimportertexture.md#class_resourceimportertexture_property_compress/mode) option that is used when a texture is detected as being used in 3D.

Changing this import option only has an effect if a texture is detected as being used in 3D. Changing this to **Disabled** then reimporting will not change the existing compress mode on a texture (if it's detected to be used in 3D), but choosing **VRAM Compressed** or **Basis Universal** will.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_editor/convert_colors_with_editor_theme"></div>

[`bool`](class_bool.md) **editor/convert_colors_with_editor_theme** = ``false`` <div id="class_resourceimportertexture_property_editor/convert_colors_with_editor_theme"></div>

If `true`, converts the imported image's colors to match [`EditorSettings.interface/theme/icon_and_font_color`](class_editorsettings.md#class_editorsettings_property_interface/theme/icon_and_font_color). This assumes the image uses the exact same colors as [*Godot's own color palette for editor icons*](../contributing/development/editor/creating_icons), with the source file designed for a dark editor theme. This should be enabled for editor plugin icons and custom class icons, but should be left disabled otherwise.

 **Note:** Only available for SVG images.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_editor/scale_with_editor_scale"></div>

[`bool`](class_bool.md) **editor/scale_with_editor_scale** = ``false`` <div id="class_resourceimportertexture_property_editor/scale_with_editor_scale"></div>

If `true`, scales the imported image to match [`EditorSettings.interface/editor/custom_display_scale`](class_editorsettings.md#class_editorsettings_property_interface/editor/custom_display_scale). This should be enabled for editor plugin icons and custom class icons, but should be left disabled otherwise.

 **Note:** Only available for SVG images.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_mipmaps/generate"></div>

[`bool`](class_bool.md) **mipmaps/generate** = ``false`` <div id="class_resourceimportertexture_property_mipmaps/generate"></div>

If `true`, smaller versions of the texture are generated on import. For example, a 64×64 texture will generate 6 mipmaps (32×32, 16×16, 8×8, 4×4, 2×2, 1×1). This has several benefits:

- Textures will not become grainy in the distance (in 3D), or if scaled down due to [`Camera2D`](class_camera2d.md) zoom or [`CanvasItem`](class_canvasitem.md) scale (in 2D).

- Performance will improve if the texture is displayed in the distance, since sampling smaller versions of the original texture is faster and requires less memory bandwidth.

The downside of mipmaps is that they increase memory usage by roughly 33%.

It's recommended to enable mipmaps in 3D. However, in 2D, this should only be enabled if your project visibly benefits from having mipmaps enabled. If the camera never zooms out significantly, there won't be a benefit to enabling mipmaps but memory usage will increase.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_mipmaps/limit"></div>

[`int`](class_int.md) **mipmaps/limit** = ``-1`` <div id="class_resourceimportertexture_property_mipmaps/limit"></div>

Unimplemented. This currently has no effect when changed.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_process/fix_alpha_border"></div>

[`bool`](class_bool.md) **process/fix_alpha_border** = ``true`` <div id="class_resourceimportertexture_property_process/fix_alpha_border"></div>

If `true`, puts pixels of the same surrounding color in transition from transparent to opaque areas. For textures displayed with bilinear filtering, this helps to reduce the outline effect when exporting images from an image editor.

It's recommended to leave this enabled (as it is by default), unless this causes issues for a particular image.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_process/hdr_as_srgb"></div>

[`bool`](class_bool.md) **process/hdr_as_srgb** = ``false`` <div id="class_resourceimportertexture_property_process/hdr_as_srgb"></div>

Some HDR images you can find online may be broken and contain sRGB color data (instead of linear color data). It is advised not to use those files. If you absolutely have to, enabling [`process/hdr_as_srgb`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/hdr_as_srgb) will make them look correct.

 **Warning:** Enabling [`process/hdr_as_srgb`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/hdr_as_srgb) on well-formatted HDR images will cause the resulting image to look too dark, so leave this on `false` if unsure.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_process/hdr_clamp_exposure"></div>

[`bool`](class_bool.md) **process/hdr_clamp_exposure** = ``false`` <div id="class_resourceimportertexture_property_process/hdr_clamp_exposure"></div>

If `true`, clamps exposure in the imported high dynamic range images using a smart clamping formula (without introducing *visible* clipping).

Some HDR panorama images you can find online may contain extremely bright pixels, due to being taken from real life sources without any clipping.

While these HDR panorama images are accurate to real life, this can cause the radiance map generated by Godot to contain sparkles when used as a background sky. This can be seen in material reflections (even on rough materials in extreme cases). Enabling [`process/hdr_clamp_exposure`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/hdr_clamp_exposure) can resolve this.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_process/normal_map_invert_y"></div>

[`bool`](class_bool.md) **process/normal_map_invert_y** = ``false`` <div id="class_resourceimportertexture_property_process/normal_map_invert_y"></div>

If `true`, convert the normal map from Y- (DirectX-style) to Y+ (OpenGL-style) by inverting its green color channel. This is the normal map convention expected by Godot.

More information about normal maps (including a coordinate order table for popular engines) can be found [*here*](http://wiki.polycount.com/wiki/Normal_Map_Technical_Details).

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_process/premult_alpha"></div>

[`bool`](class_bool.md) **process/premult_alpha** = ``false`` <div id="class_resourceimportertexture_property_process/premult_alpha"></div>

An alternative to fixing darkened borders with [`process/fix_alpha_border`](class_resourceimportertexture.md#class_resourceimportertexture_property_process/fix_alpha_border) is to use premultiplied alpha. By enabling this option, the texture will be converted to this format. A premultiplied alpha texture requires specific materials to be displayed correctly:

- In 2D, a [`CanvasItemMaterial`](class_canvasitemmaterial.md) will need to be created and configured to use the [`CanvasItemMaterial.BLEND_MODE_PREMULT_ALPHA`](class_canvasitemmaterial.md#class_canvasitemmaterial_constant_blend_mode_premult_alpha) blend mode on [`CanvasItem`](class_canvasitem.md) s that use this texture. In custom `@canvas_item` shaders, `render_mode blend_premul_alpha;` should be used.

- In 3D, a [`BaseMaterial3D`](class_basematerial3d.md) will need to be created and configured to use the [`BaseMaterial3D.BLEND_MODE_PREMULT_ALPHA`](class_basematerial3d.md#class_basematerial3d_constant_blend_mode_premult_alpha) blend mode on materials that use this texture. In custom `spatial` shaders, `render_mode blend_premul_alpha;` should be used.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_process/size_limit"></div>

[`int`](class_int.md) **process/size_limit** = ``0`` <div id="class_resourceimportertexture_property_process/size_limit"></div>

If set to a value greater than `0`, the size of the texture is limited on import to a value smaller than or equal to the value specified here. For non-square textures, the size limit affects the longer dimension, with the shorter dimension scaled to preserve aspect ratio. Resizing is performed using cubic interpolation.

This can be used to reduce memory usage without affecting the source images, or avoid issues with textures not displaying on mobile/web platforms (as these usually can't display textures larger than 4096×4096).

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_roughness/mode"></div>

[`int`](class_int.md) **roughness/mode** = ``0`` <div id="class_resourceimportertexture_property_roughness/mode"></div>

The color channel to consider as a roughness map in this texture. Only effective if Roughness > Src Normal is not empty.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_roughness/src_normal"></div>

[`String`](class_string.md) **roughness/src_normal** = ``""`` <div id="class_resourceimportertexture_property_roughness/src_normal"></div>

The path to the texture to consider as a normal map for roughness filtering on import. Specifying this can help decrease specular aliasing slightly in 3D.

Roughness filtering on import is only used in 3D rendering, not 2D.

<!-- rst-class:: classref-item-separator -->

---

<div id="_class_resourceimportertexture_property_svg/scale"></div>

[`float`](class_float.md) **svg/scale** = ``1.0`` <div id="class_resourceimportertexture_property_svg/scale"></div>

The scale the SVG should be rendered at, with `1.0` being the original design size. Higher values result in a larger image. Note that unlike font oversampling, this affects the size the SVG is rendered at in 2D. See also [`editor/scale_with_editor_scale`](class_resourceimportertexture.md#class_resourceimportertexture_property_editor/scale_with_editor_scale).

 **Note:** Only available for SVG images.

[^virtual]: 本方法通常需要用户覆盖才能生效。
[^const]: 本方法无副作用，不会修改该实例的任何成员变量。
[^vararg]: 本方法除了能接受在此处描述的参数外，还能够继续接受任意数量的参数。
[^constructor]: 本方法用于构造某个类型。
[^static]: 调用本方法无需实例，可直接使用类名进行调用。
[^operator]: 本方法描述的是使用本类型作为左操作数的有效运算符。
[^bitfield]: 这个值是由下列位标志构成位掩码的整数。
[^void]: 无返回值。
