# xyz-cmake
Cmake helper, that allows you to configure your multibinary, multilibrary C/C++ project, via a json file.
Refer to [xyz-cmake-example](https://github.com/BenjaminKern/xyz-cmake-example) for example usage.
# Features
- Create [doctest](https://github.com/doctest/doctest) unittest for C++ libraries
- Create [greatest](https://github.com/silentbicycle/greatest) unittest for C libraries
- Create a debian package via CPack
# Prerequisites
- cmake >= 3.19
- File layout for a C++ library foo, unit tests via [doctest](https://github.com/doctest/doctest) if test folder is not empty, header only library if src folder is empty, private headers are in the src folder
```
  foo/include/foo/*.h
  foo/src/*.cpp
  foo/test/*.cpp
```
- File layout for a C library bar, unit tests via [greatest](https://github.com/silentbicycle/greatest) if test folder is not empty, header only library if src folder is empty, private headers are in the src folder 
```
  bar/include/bar/*.h
  bar/src/*.c
  bar/test/*.c
```
- File layout for a C binary blub, private headers are in the src folder
```
  blub/src/*.c
```
- File layout for a C++ binary blob, private headers are in the src folder
```
  blob/src/*.cpp
```
- Src files are globbed
