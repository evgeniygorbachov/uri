# URI

This is a component witch implements [RFC 3986](https://tools.ietf.org/html/rfc3986), "Uniform Resource Identifier (URI): Generic Syntax".

# Building

### Prerequisites

* CMake version 3.8+
* conan
* C++11 toolchain

### Build system generation

Create and jump into a folder:

```bash
mkdir build
cd build
```

Install the dependencies with conan:

```bash
conan install ..
```

Generate build system:

```bash
cmake -G "Visual Studio 15 2017" -A "x64" ..
```

### Building

Either use CMake or your toolchain's IDE to build. For example:

```bash
cd build
cmake --build . --config Release
```