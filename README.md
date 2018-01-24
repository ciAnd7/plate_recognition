Automatic number plate recognition library
=================
Cross-platform ANPR open source library ( C++ )

[Measuring recognition](Measurements.md)

Support only Russian plate GOST 50577-93.

I have no build servers, so at the end of the description of the commit put a platform under which it was made.

Support platforms
-------
* Windows - norm
* Android - norm
* Linux (Debian) - norm
* Mac - not tested yet, but should support
* iOS - not tested yet, but should support

Compilers
-------
* Visual Studio 2012 - norm
* Visual Studio 2013 - norm
* mingw-g++ - norm
* Android NDK r9b - norm
* g++ 4.7.2 - norm

Dependencies
-------
* OpenCV for image processing
* Qt

Recognition library depends only on OpenCV.

Why auto_test_desktop program depends on Qt?
* read/write directory files list
* implement work thread in not gui thread


Build with qmake
-------
1. In file "opencv.pri" set path to OpenCV.
2. In file "opencv.pri" set version of OpenCV.
3. In file "auto_test_desktop/main.cpp" hardcoded folder for test images for Android device.


Debian Stretch Headless Build & Run
=============================

```
# apt-get install sudo vim
$ sudo apt-get install build-essential cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev libopencv-dev libtesseract-dev libleptonica-dev  liblog4cplus-dev libcurl3-dev 
$ sudo apt-get install qt5-qmake qt5-default
$ qmake ; make
$ bin/release/auto_test_desktop -i ./test_data/Y900XA177.jpg 
```

