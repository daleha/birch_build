# Usage

Add the appropriate directory for your platform in "bins" to your system path, so that you are able to run premake with the command "premake4".

## Generating make scripts

Premake supports building msvs, gnu make, and even xcode project files. For instance, on linux you might do:

* premake4 gmake release # to generate a makefile for GNU gmake for \*nix platforms 
* premake4 xcode debug # to generate an xcode project for osx with debug symbols
* premake4 vs2010 release # to generate a release build script for windows platform using the visual studio compiler collection.


## Writing premake scripts

Premake scripts are designed to encapsulate all of the **sematic** data needed to build a project. For instance, which include directories to use for a platform, where the source and headers are, etc. This ommits all of the implementation details, and allows for a single file to be used to target several platforms.

Details on premake syntax can be found at [premake scripting referenc][1], and general info can be found at [the premake website][2].

You should specify common debug and release configurations, as well as platform specific ones in the premake source file.

 [1] http://industriousone.com/scripting-reference
 [2] http://industriousone.com/what-premake


## The basics

Premake will by default run the file "premake4.lua" if none are specified. You should have this file include your actual build file, as that tends to be the standard way of doing things. 

To see how this works change directory into the source directory, and run "premake4 gmake". This will generate the files (\*.lua) used to build premake (yes - premake builds itself!).


