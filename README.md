# ChicagoCRT

[![Original](https://img.shields.io/badge/Original_Code-by_malxau-blue?style=flat-square&logo=github)](https://github.com/malxau/minicrt)
[![GitHub issues](https://img.shields.io/github/issues/analogfeelings/chicagocrt?style=flat-square&logo=github&label=Issues)](https://github.com/AnalogFeelings/chicagocrt/issues)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/analogfeelings/chicagocrt?label=Pull%20Requests&style=flat-square&logo=github)](https://github.com/AnalogFeelings/chicagocrt/pulls)
[![GitHub](https://img.shields.io/github/license/analogfeelings/chicagocrt?label=License&style=flat-square&logo=opensourceinitiative&logoColor=white)](https://github.com/AnalogFeelings/chicagocrt/blob/master/LICENSE)
[![GitHub commit activity (branch)](https://img.shields.io/github/commit-activity/m/analogfeelings/chicagocrt/master?label=Commit%20Activity&style=flat-square&logo=github)](https://github.com/AnalogFeelings/chicagocrt/graphs/commit-activity)
[![GitHub Repo stars](https://img.shields.io/github/stars/analogfeelings/chicagocrt?label=Stargazers&style=flat-square&logo=github)](https://github.com/AnalogFeelings/chicagocrt/stargazers)
[![Mastodon Follow](https://img.shields.io/mastodon/follow/109309123442839534?domain=https%3A%2F%2Ftech.lgbt%2F&style=flat-square&logo=mastodon&logoColor=white&label=Follow%20Me!&color=6364ff)](https://tech.lgbt/@analog_feelings)

ChicagoCRT is a fork of MiniCRT designed to run on systems Windows 95 and higher, on x86.

## :thinking: Inspiration

MattKC has recently published a video on porting .NET Framework to Windows 95, which made me think about doing the same, but with programs compiled on modern Windows SDKs.

I knew it was possible, since MSVC allows you to disable the standard library and enhanced instructions, but I had to get around the artificial limitation imposed by the system version
in the PE header.

## :desktop_computer: System Requirements

ChicagoCRT does not depend on APIs newer than Windows NT 3.1 or Windows 95. A Unicode binary with ChicagoCRT can run on NT 3.1; an ANSI binary can run on Windows 95.

> [!IMPORTANT]
> Newer compilers will mark executables as requiring Windows Vista or higher.  
> This is an artificial limitation, and you can find a script to get around this on my GitHub Gists. (TODO)

## :toolbox: Build instructions

Requires Visual Studio 2022, with the C++ workload installed and the Windows SDK.  
Building can be done as with any standard C++ project, and the output will be found on the `Build` folder.

> [!NOTE]
> Due to the nature of computers running Windows 95, enhanced instructions (e.g. SSE, AVX) have been disabled entirely.  
> Programs that link to ChicagoCRT should ideally also disable enhanced instructions.

# :balance_scale: License

This software is licensed under the terms of the MIT license.  
You can read the terms [here](LICENSE).

