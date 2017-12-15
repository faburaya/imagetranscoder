This C++ application transcodes batches of images between formats JPEG, JPEG XR and TIFF with configurable quality level. It uses Microsoft windows Imaging Components and is capable of also transfering metadata between different formats (EXIF, IFD, XMP etc.)

The solution can build this application both for the console (command prompt) or Windows Store (UWP application), and is meant to be built by Visual C++ 2015 and depends on 3FD v2.4+ (https://github.com/faburaya/3fd) installed in a location defined by an enviroment variable to be called "_3FD_HOME".

Windows 10 (at least build 14393) is recommended.

Console usage:

 ImageTranscoder [/x] [/q:target_quality] path1 [path2 ...]

           /x, /jxr   Whether the files should be transcoded to JPEG XR instead
                      of regular JPEG

     /q:, /quality:   The target quality for the output transcoded image (when
                      ommited, default = 0.95; min = 0.01; max = 1)

        directories   The paths for the directories whose contained files will
                      be transcoded (expects from  1 to 32 values)