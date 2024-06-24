# Why is this here?

We want to use std::span, but that is available only since c++20 (gcc 10), but the esp8266 sdk uses only gcc 8.4 so we can't directly use it. But std::span was adopted from the C++ Standard Guidelines and Microsoft still has span implementation in their GSL library. So we can use theirs to get the same support. There is currently a problem when compiling with [older gcc](https://github.com/microsoft/GSL/issues/1148), so until [the PR with fix](https://github.com/microsoft/GSL/pull/1149), we need to use the fixed versions from the PR.
