---
description: Important to manage the total usage. Otherwise browsers may crash.
---

# Memory Usage

## GPU

### Texture

So, these are the sizes for different common texture formats:

* L \(luminance, e.g. greyscale\): width \* height \* 1 byte.
* LA \(luminance and alpha, common for fonts\): width \* height \* 2 bytes.
* RGB \(color, no alpha\): width \* height \* 3 bytes.
* RGBA \(color with alpha\): width \* height \* 4 bytes.
* DXT1/BC1 \(color, binary alpha\): \(width \* height \* 4 bytes\) / 8 \(8:1 compression ratio\).
* DXT3/BC2 \(color, sharp alpha\)/DXT5/BC3 \(color, gradient alpha\): \(width \* height \* 4 bytes\) / 4 \(4:1 compression ratio\).

If you use a image with [mipmaps](http://en.wikipedia.org/wiki/Mipmap), the texture will require 4/3 as much memory. 

### Geometry



## CPU

