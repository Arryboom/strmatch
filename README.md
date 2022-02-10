# strmatch

>X64 strmatch from official with fixed support for newest x64dbg sdk.

Simple string matching plugin for x64dbg. Supports UTF8, UTF16 and Local codepages.

```
[strmatch] documentation:
  1. Command: strmatch_set index, "string"
  2. Expression function: [action]_[encoding](va, index)
  Actions: strcmp, stricmp, strstr, stristr
  Encodings: utf8, utf16, local
  Example: strcmp_utf16(va, index)
```

# Example

```
strmatch_set 1337, "hello"
stristr_utf8(edx, 1337)
```



original at https://github.com/x64dbg/strmatch/


/build64/Release/PluginTemplate.dp64



---


# PluginTemplate

Template CMake project for x64dbg plugins. This uses [cmkr](https://build-cpp.github.io/cmkr/), `cmake.toml` contains the project configuration.

## Using the template

You can click the green *Use this template* button. See the article [*Creating a repository from a template*
](https://docs.github.com/en/free-pro-team@latest/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template) by GitHub for more details.

Alternatively you can download a ZIP of this repository and set up the template locally.

## Building

From a Visual Studio command prompt:

```
cmake -B build64 -A x64
cmake --build build64 --config Release
```

You will get `build64\PluginTemplate.sln` that you can open in Visual Studio.

To build a 32-bit plugin:

```
cmake -B build32 -A Win32
cmake --build build32 --config Release
```

Alternatively you can open this folder in Visual Studio/CLion/Qt Creator.

![building animation](https://github.com/x64dbg/PluginTemplate/blob/3951eb4b320b7a26164616ab5141414e8cd5b0a1/building.gif?raw=true)



