<p align="center">
    <img width="200" alt="Alacritty Logo" src="https://raw.githubusercontent.com/alacritty/alacritty/master/extra/logo/compat/alacritty-term%2Bscanlines.png">
</p>

<h1 align="center">Alacritty - A fast, cross-platform, OpenGL terminal emulator</h1>

<p align="center">
  <img alt="Alacritty - A fast, cross-platform, OpenGL terminal emulator"
       src="https://raw.githubusercontent.com/alacritty/alacritty/master/extra/promo/alacritty-readme.png">
</p>

## About

Alacritty is a modern terminal emulator that comes with sensible defaults, but
allows for extensive [configuration](#configuration). By integrating with other
applications, rather than reimplementing their functionality, it manages to
provide a flexible set of [features](./docs/features.md) with high performance.
The supported platforms currently consist of BSD, Linux, macOS and Windows.

The software is considered to be at a **beta** level of readiness; there are
a few missing features and bugs to be fixed, but it is already used by many as
a daily driver.

Precompiled binaries are available from the [GitHub releases page](https://github.com/alacritty/alacritty/releases).

Join [`#alacritty`] on libera.chat if you have questions or looking for a quick help.

[`#alacritty`]: https://web.libera.chat/gamja/?channels=#alacritty

## Features

You can find an overview over the features available in Alacritty [here](./docs/features.md).
This is the spin-off version to include a terminal keyword highlighter. (mild performance degradation)

## Further information

- [Announcing Alacritty, a GPU-Accelerated Terminal Emulator](https://jwilm.io/blog/announcing-alacritty/) January 6, 2017
- [A talk about Alacritty at the Rust Meetup January 2017](https://www.youtube.com/watch?v=qHOdYO3WUTk) January 19, 2017
- [Alacritty Lands Scrollback, Publishes Benchmarks](https://jwilm.io/blog/alacritty-lands-scrollback/) September 17, 2018

## Installation

```
git clone https://github.com/Lycheus/alacritty-highlight.git
cd alacritty

cargo build --release

# run it directly:
./target/release/alacritty

```

### Requirements

- At least OpenGL ES 2.0
- [Windows] ConPTY support (Windows 10 version 1809 or higher)

## Configuration
### Config example

Put this in ~/.config/alacritty/alacritty.toml:

Or the other location that you use for alacritty configuration.

```
[keyword_highlight]
enabled = true

rules = [
  # case-insensitive "kenny"
  { regex = "(?i)kenny", foreground = "#FF8000"},

  # error-ish stuff
  { regex = "(?i)error|failed|fatal", foreground = "#181818", background = "#ff5555", underline = true, bold = true },

  # warnings
  { regex = "(?i)warning", foreground = "#181818", background = "#f1fa8c" },
]
```

Color format ("#RRGGBB") matches Alacritty’s documented config format.

## License

Alacritty is released under the [Apache License, Version 2.0].

[Apache License, Version 2.0]: https://github.com/alacritty/alacritty/blob/master/LICENSE-APACHE
