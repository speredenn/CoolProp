.. _wrappers:

******************
Available Wrappers
******************

CoolProp at its core is a C++ library, but it can be of interest to use this code base from other programming environments.  For that reason, wrappers have been constructed for most of the programming languages of technical interest to allow users to seamlessly interface CoolProp and existing codebases.

Downloads and instructions for each wrapper are included in the page for the wrapper given in the table below.

==============================================  ===========================  =======================================
Target                                          Operating Systems            Notes
==============================================  ===========================  =======================================
:ref:`Static library <static_library>`          linux, OSX, win
:ref:`Shared library (DLL) <shared_library>`    linux, OSX, win
:ref:`Python <Python>`                          linux, OSX, win              Wrapper is Cython based
:ref:`Octave <Octave>`                          linux, OSX, win              Wrapper is SWIG based
:ref:`C# <Csharp>`                              linux, OSX, win              Wrapper is SWIG based
:ref:`MATLAB <MATLAB>`                          linux, OSX, win              Wrapper is SWIG based
:ref:`Java <Java>`                              linux, OSX, win              Wrapper is SWIG based
:ref:`Scilab <Scilab>`                          linux, OSX, win              Wrapper is SWIG based (experimental)
:ref:`Julia <Julia>`                            linux, OSX, win              
:ref:`Modelica <Modelica>`                      linux, OSX, win
:ref:`PHP <PHP>`                                linux, OSX, win              Mostly used on linux
:ref:`Javascript <Javascript>`                  cross-platform               Works in all internet browsers
:ref:`Labview <Labview>`                        windows only
:ref:`Maple <Maple>`                            linux, OSX, win
:ref:`MathCAD <MathCAD>`                        windows only
:ref:`SMath Studio <SMath>`                     linux, OSX, win
:ref:`Mathematica <Mathematica>`
:ref:`FORTRAN <FORTRAN>`                        linux, OSX, win
:ref:`EES <EES>`                                windows only
:ref:`Microsoft Excel <Excel>`                  windows only
:ref:`LibreOffice <LibreOffice>`                windows, linux
:ref:`Delphi & Lazarus <Delphi>`                linux, OSX, win
==============================================  ===========================  =======================================

.. _wrapper_common_prereqs:

Common Wrapper Prerequisites
============================

On all platforms for which CoolProp is supported, the compilation of one of the wrappers requires a few common prerequisites, described here. They are:

* git (to interface with the CoolProp repository at https://github.com/CoolProp/CoolProp)
* CMake (platform-independent software to generate makefiles)
* C++ compiler (see below)
* 7-zip

Windows
-------
On Windows, download the newest binary installer for CMake from `CMake downloads <http://www.cmake.org/cmake/resources/software.html>`_.  Run the installer.  Check that at the command prompt you can do something like::

    C:\Users\XXXX>cmake -version
    cmake version 2.8.12.2

For git, your best best is the installer from http://msysgit.github.io/.  Check that at the command prompt you can do something like::

    C:\Users\XXXX>git --version
    git version 1.9.4.msysgit.0

For 7-zip, download the installer from http://www.7-zip.org/ .  Check that at the command prompt you can do something like::

    C:\Users\XXXX>7z

    7-Zip [64] 9.20  Copyright (c) 1999-2010 Igor Pavlov  2010-11-18

    Usage: 7z <command> [<switches>...] <archive_name> [<file_names>...]
           [<@listfiles...>]

For the C++ compiler, the options are a bit more complicated.  There are multiple (binary incompatible) versions of Visual Studio, as well as G++ ports for windows (MinGW).  Unless you are compiling the python wrappers, you can compile with MinGW, so you should obtain the `MinGW installer <http://sourceforge.net/projects/mingw/files/Installer/mingw-get-setup.exe/download>`_ and run it.  You should install all the packages available, and you MUST(!!) install to a path without spaces. ``C:\MinGW`` is recommended as an installation path. Be sure to add the folder ``C:\MinGw`` to your PATH variable.

If you want to build 64-bit extensions, you MUST install professional versions of visual studio, which can be obtained for free if you have a student ID card from Microsoft Dreamspark.  You will require Visual Studio 2008 Professional for python 2.x, and Visual Studio 2010 Professional for python 3.x.  Otherwise you can select Visual Studio version freely.

All three compilers should co-exist happily on the path, so you should be fine installing all three, but they are rather sizeable installs.

Linux
-----
On debian based linux distributions (ubuntu, etc.), you can simply do::

    sudo apt-get install cmake git g++ p7zip

although ``git`` is probably already packaged with your operating system; ``g++`` probably isn't

OSX
---
OSX should come with a c++ compiler (clang), for git and cmake your best bet is `Homebrew <http://brew.sh/>`_.  With Homebrew installed, you can just do::

    brew install cmake git p7zip

If you have never done any command-line compilation before on OSX, chances are that you do not have the utilities needed. Thus you need to first install Xcode: see the description on the page http://guide.macports.org/#installing.xcode . After installing, you need to accept the license by running the following command in the Terminal::

    xcodebuild -license

and explicitly typing "agree" before closing. Then you can use the compiler from the command line.

.. toctree::
    :hidden:

    Octave/index.rst
    Csharp/index.rst
    MATLAB/index.rst
    MathCAD/index.rst
    FORTRAN/index.rst
    PHP/index.rst
    EES/index.rst
    Java/index.rst
    Javascript/index.rst
    Julia/index.rst
    Labview/index.rst
    Python/index.rst
    LibreOffice/index.rst
    Excel/index.rst
    Maple/index.rst
    Scilab/index.rst
    SMath/index.rst
    StaticLibrary/index.rst
    SharedLibrary/index.rst
    DelphiLazarus/index.rst