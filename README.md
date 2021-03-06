[![Build Status](https://travis-ci.com/bincrafters/conan-lksctp-tools.svg?branch=release/1.0.17)](https://travis-ci.com/bincrafters/conan-lksctp-tools)
[![CircleCI](https://circleci.com/gh/bincrafters/conan-lksctp-tools/tree/stable%2F1.0.17.svg?style=svg)](https://circleci.com/gh/bincrafters/conan-lksctp-tools/tree/stable%2F1.0.17)
[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://img.shields.io/badge/License-GPL%20v2-blue.svg)

# Linux Kernel Stream Control Transmission Protocol Tools

[Conan.io](https://conan.io) package for [lksctp-tools](https://github.com/sctp/lksctp-tools) project

The packages generated with this **conanfile** can be found in [Bintray](https://bintray.com/bincrafters/public-conan/lksctp-tools%3Abincrafters).

## Build packages

Download conan client from [Conan.io](https://conan.io) and run:

    $ python build.py

If your are in Windows you should run it from a VisualStudio console in order to get "mc.exe" in path.

## Upload packages to server

    $ conan upload lksctp-tools/1.0.17@bincrafters/stable --all

## Reuse the packages

### Basic setup

    $ conan install lksctp-tools/1.0.17@bincrafters/stable

### Project setup

If you handle multiple dependencies in your project is better to add a *conanfile.txt*

    [requires]
    lksctp-tools/1.0.17@bincrafters/stable

    [options]
    lksctp-tools:shared=True # False
    lksctp-tools:with_sctp=True # False (a tool when used with existing TCP binaries replaces TCP with SCTP.)

    [generators]
    txt
    cmake

Complete the installation of requirements for your project running:</small></span>

    conan install .

Project setup installs the library (and all his dependencies) and generates the files *conanbuildinfo.txt* and *conanbuildinfo.cmake* with all the paths and variables that you need to link with your dependencies.

### License
[MIT](LICENSE)
