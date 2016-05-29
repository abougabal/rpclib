# Getting started

This document details the steps of getting everything in place to be able to use `callme`.

## What you need

### Compiler

`callme` uses some C++14 features, and as such, requires a very recent compiler. The following compilers are tried and tested with `callme` at the moment:

  * g++ 5.0
  * clang++ 3.7
  * MSVC 2015 Update 1

TIP: Newer versions of these compilers are expected to work.

### Tools

In addition to a capable compiler, you will need:

  * [CMake 3.x](https://cmake.org)
  * GNU make (on \*nixes) or MSBuild/Visual Studio (on Microsoft Windows).

### Dependencies

`callme` has no external library dependencies, i.e. you don't need to install any extra libraries to use it. The library does use third-party code, but it is hidden both during compilation and linking (i.e. it means you don't need to worry about linking against those same libraries).

TIP: See the [Design](design.md) documentation for details on how `callme` handles its dependencies.


## Building

`callme` uses CMake and has a very conventional build process. If you know how to build a CMake-based library, you know how to build `callme`.

If not, you can read the <<building.adoc#,Building>> chapter for step-by-step instructions. You can also visit that document for information learn about advanced building options.

## Your first project with `callme`: "Here's my number"

In order to integrate `callme` into your project, you will need to have it built and stored somewhere on your system. Place the `callme` headers into your include path, and link libcallme.a with your executable. The exact process of that depends on your compiler and/or IDE.

### CMake/Clion

`callme` ships with a CMake module that can be used to find the library in the system. Using it is pretty simple: place Findcallme.cmake into your CMake module path, then add the following to your CMakeLists.txt:

```cmake
find_package(callme)
```

### Microsoft Visual Studio

TBD

### XCode

TBD