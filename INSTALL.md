# Installing Pony

Prebuilt Pony binaries are available on a number of platforms. They are built using a very generic CPU instruction set and as such, will not provide maximum performance. If you need to get the best performance possible from your Pony program, we strongly recommend [building from source](BUILD.md).

## Linux

Prebuilt Linux packages are available via [ponyup](https://github.com/ponylang/ponyup) for Glibc and musl libc based Linux distribution. You can install nightly builds as well as official releases using ponyup.

To install the most recent ponyc:

```bash
ponyup update ponyc release
```

Additional requirements:

All ponyc Linux installations need a C compiler such as gcc or clang installed. The following distributions have additional requirements:

Distribution | Requires
--- | ---
alpine | libexecinfo
fedora | libatomic

## macOS

Prebuilt macOS packages are available via [ponyup](https://github.com/ponylang/ponyup). You can also install nightly builds using ponyup.

To install the most recent ponyc on macOS:

```bash
ponyup update ponyc release
```

## Windows

Windows users will need to install:

- Visual Studio 2019, 2017 or 2015 (available [here](https://www.visualstudio.com/vs/community/)) or the Visual C++ Build Tools 2019, 2017 or 2015 (available [here](https://visualstudio.microsoft.com/visual-cpp-build-tools/)), and
  - If using Visual Studio 2015, install the Windows 10 SDK (available [here](https://developer.microsoft.com/en-us/windows/downloads/windows-10-sdk)).
  - If using Visual Studio 2017 or 2019, install the "Desktop Development with C++" workload.
  - If using Visual C++ Build Tools 2017 or 2019, install the "Visual C++ build tools" workload, and the "Visual Studio C++ core features" individual component.
  - If using Visual Studio 2017 or 2019, or Visual C++ Build Tools 2017 or 2019, make sure the latest `Windows 10 SDK (10.x.x.x) for Desktop` will be installed.

Once you have installed the prerequisites, you can download the latest ponyc release from [bintray](https://dl.bintray.com/pony-language/ponyc-win/).

Unzip the release file in a convenient location, and you will find `ponyc.exe` in the `ponyc\bin` directory. Following extraction, to make `ponyc.exe` globally available, add it to your `PATH` either by using Advanced System Settings->Environment Variables to extend `PATH` or by using the `setx` command, e.g. `setx PATH "%PATH%;<directory you unzipped to>\ponyc\bin"`
