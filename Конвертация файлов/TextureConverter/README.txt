LICENSE
-------
This software uses the Squish library. Squish is used under the MIT License. See http://code.google.com/p/libsquish/ for details.

This software uses the FreeImage open source image library. See http://freeimage.sourceforge.net for details.
FreeImage is used under the FIPL, version 1.0.

Full license and copyright information can be found in LICENSE.txt

USAGE
-----

   TextureConverter.exe  [-r <stretch|paste>] [-t <1d|2d|3d|cubemap>] [-e
                         <big|little>] [--filter <box|bilinear|bspline
                         |bicubic|catmulllrom|lanczos3>] -f <bc1|bc2|bc3
                         |x8r8g8b8|argb|rgb|l16|a8|dxt1|dxt3|dxt5> -p
                         <opengl|gles2|d3d9|xbox360|ps3> [--premultiply]
                         [--info] [--mipmap] [-s] [--pow2] [-v <1>] [-h
                         <64>] [-w <512>] -o <output.tex> -i
                         <input.png[;input2.png;input3.png]> [--]


Where:

   -r <stretch|paste>,  --resize <stretch|paste>
     The method used to resize a texture

   -t <1d|2d|3d|cubemap>,  --type <1d|2d|3d|cubemap>
     The type of texture to create

   -e <big|little>,  --endian <big|little>
     Endianness to output

   --filter <box|bilinear|bspline|bicubic|catmulllrom|lanczos3>
     Resize filter to use

   -f <bc1|bc2|bc3|x8r8g8b8|argb|rgb|l16|a8|dxt1|dxt3|dxt5>,  --format <bc1
      |bc2|bc3|x8r8g8b8|argb|rgb|l16|a8|dxt1|dxt3|dxt5>
     (required)  Pixel format to convert the texture to

   -p <opengl|gles2|d3d9|xbox360|ps3>,  --platform <opengl|gles2|d3d9
      |xbox360|ps3>
     (required)  Platform to convert the texture for.

   --premultiply
     Premultiply alpha

   --info
     Print texture info

   --mipmap
     Generate Mip Maps

   -s,  --swizzle
     Swizzle the texture on platforms that support it. Imposes platform
     specific alignment & size restrictions.

   --pow2
     Make primary mipmap a power of two

   -v <1>,  --verbosity <1>
     Output verbosity

   -h <64>,  --height <64>
     Height to resize the primary mipmap to. No resizing occurs if
     unspecified.

   -w <512>,  --width <512>
     Width to resize the primary mipmap to. No resizing occurs if
     unspecified.

   -o <output.tex>,  --outfile <output.tex>
     (required)  Input texture filename

   -i <input.png[;input2.png;input3.png]>,  --infiles
      <input.png[;input2.png;input3.png]>
     (required)  Input texture filenames

   --,  --ignore_rest
     Ignores the rest of the labeled arguments following this flag.
