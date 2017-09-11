# libjpeg_compile
migw32 libjpeg compile

1.Get msys
Get it From http://www.mingw.org/;https://sourceforge.net/projects/mingw/
I put it on d:\nangui\msys.

2.Install MinGW
I use tdm version 492，It is a version of Code :: blocks.
From http://tdm-gcc.tdragon.net;
I put it on d:\MinGW.

3.Get libjpeg sources
From http://www.ijg.org/, take the zip format package . I took the jpeg_9b version.

4.Prepare a building directory
Create a jpeg directory inside D:\nanagui,it will hold the built library.
Decompress the libjpeg sources in D:\nanagui\jpegsr9b, so you have a jpeg-9b directory in there.

5../configure, make, make install
Run the following commands in an MSYS shell:
cd /d/nanagui/jpegsr9b/jpeg-9b
./configure --prefix=/d/nanagui/jpeg

Add the following definition to the jconfig.h

 #define HAVE_PROTOTYPES 1

make
make install

As an additional step, you can run make test for safety.

These commands will build both static and shared versions of libjpeg.

6.Copy include and lib to MinGW
Copy include and lib to D:/MinGW from /d/nanagui/jpeg.
