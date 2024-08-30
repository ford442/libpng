# libpng
libpng 1.6.43 from SourceForge


libpng is the official PNG reference library. It supports almost all PNG features, is extensible, and has been extensively tested for over 28 years. The home site for development versions (i.e., may be buggy or subject to change or include experimental features) is https://libpng.sourceforge.io/, and the place to go for questions about the library is the png-mng-implement mailing list.

libpng is available as ANSI C (C89) source code and requires zlib 1.0.4 or later (1.2.13 or later recommended for performance and security reasons). The current public release, libpng 1.6.43, adds support for the eXIf chunk in the push-style PNG API (courtesy of Chris Blume) as well as numerous minor fixes and improvements. The pngexifinfo utility can now be found in contrib/pngexif as well.

Portability Note

The libpng 1.6.x series continues the evolution of the libpng API, finally hiding the contents of the venerable and hoary png_struct and png_info data structures inside private (i.e., non-installed) header files. Instead of direct struct-access, applications should be using the various png_get_xxx() and png_set_xxx() accessor functions, which have existed for almost as long as libpng itself.
The portability notice should not come as a particular surprise to anyone who has added libpng support to an application this millenium; the manual has warned of it since at least July 2000. (Specifically: "Starting with version 2.0.0, both structures are going to be hidden, and the contents of the structures will only be accessible through the png_get/png_set functions." OK, so the version number was off a bit...and the grammar, too, but who's counting?) Those whose apps depend on the older API need not panic, however (for now); libpng 1.2.x continues to get security fixes, as has 1.0.x for well over a decade. (Greg no longer bothers to list either series here; enough's enough, folks. Update those apps now!)

The 1.5.x and later series also include a new, more thorough test program (pngvalid.c) and a new pnglibconf.h header file that tracks what features were enabled or disabled when libpng was built. On the other hand, they no longer internally include the zlib.h header file, so applications that formerly depended on png.h to provide that will now need to include it explicitly. Complete differences relative to libpng 1.4.x are detailed here.
See the bottom of this page for warnings about security and crash bugs in versions up through libpng 1.6.36.
In addition to the main library sources, all of the 1.2.x/1.4.x/1.5.x/1.6.x/1.7.x series include the rpng, rpng2 and wpng demo programs, the pngminus demo program, a subset of Willem van Schaik's PngSuite test images, and Willem's VisualPng demo program.
