## ZeroMQ Building ##

This project provides some prebuilt ZeroMQ configuration scripts for easy building on various platforms.  It contains as a submodule, the [libzmq][libzmq-release].  In addition, it contains the following bindings for libzmq:

 - [C++ binding for 0MQ][cppzmq-release] (Header-only)
 - [ZMQ C++ wrapper (with no added magic)][zmqcpp-release] (Header-only)
 - [C++ binding with Boost::ASIO integration][azmq-release] (Header-only)

You can check these directories out in any location on your computer, but the default location that the `build.sh` script looks for is as a parent directory to where you check out the [libzmq][libzmq-release] and within the `bindings` directory for the binding git projects.  By default, this project contains submodules of the subprojects in the correct locations.

[libzmq-release]: https://github.com/toonetown/libzmq
[cppzmq-release]: https://github.com/toonetown/cppzmq
[zmqcpp-release]: https://github.com/toonetown/zmqcpp
[azmq-release]: https://github.com/toonetown/azmq

### Requirements ###

The following are supported to build the OpenSSL project:

To build on macOS:

 * macOS 10.13 (High Sierra)
 
 * Xcode 9.1 (From Mac App Store)
     * Run Xcode and accept all first-run prompts

To build on Windows:

 * Windows 10
 
 * Visual Studio 2017 (or 2015)
     * Make sure and install `Programming Languages | Visual C++ | Common Tools for Visual C++ 2017` as well
     * If you have both 2017 and 2015 installed, you can select to build for 2015 by setting `SET MSVC_VERSION=14.0` (the default is to use 14.1) prior to running the `build.bat` file.

To build for Android:

 * macOS requirements above
 
 * Android NDK r15c
     * You must set the environment variable `ANDROID_NDK_HOME` to point to your NDK installation

     
### Build Steps ###

You can build the libraries using the `build.sh` script:

    ./build.sh [/path/to/libzmq-dist] [/paths/to/bindings...] <plat.arch|plat|'clean'>

Run `./build.sh` itself to see details on its options.

You can modify the execution of the scripts by setting various environment variables.  See the script sources for lists of these variables.
