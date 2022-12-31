# NextWM

Manual tiling wayland compositor written with wlroots aimed to be a bspwm clone.

Note: NextWM is still a work in progress project. It won't be useable anytime soon, but when it is I will be the first one to spam screenshots of it in the readme.

<p align=center>
    <a href="https://builds.sr.ht/~shinyzenith/NextWM/commits/master/ubuntu.yml"><img src="https://builds.sr.ht/~shinyzenith/NextWM/commits/master/ubuntu.yml.svg"</a>
    <a href="https://github.com/waycrate/NextWM/actions"><img src="https://github.com/waycrate/nextwm/actions/workflows/arch.yaml/badge.svg"></a>
</p>

## License:

The entire project is licensed as BSD-2 "Simplified" unless stated otherwise in the file header.

## Aim

I want to learn how to write wlroots compositors with this project and keep everything commented to a great extent for others to learn from.
The wlroots ecosystem is hard to initially get into as per my experience and I want to change that via NextWM.

## Why multiple implementations of Nextctl?

Since this project is meant to teach others, why not show people how wayland clients are written in different languages :) ?

## Building

By default Xwayland always executes in the background. The `-Dxwayland-lazy` flag was added to mitigate this issue however this may have slightly worse xwayland startup times.

By default Nextctl C codebase is compiled and put in the mentioned `--prefix`. The `-Dnextctl-rs` / `-Dnextctl-go` flag compiles the Go/Rust versions instead. All versions of the tool are exactly identical.

### Depedencies

1. `cargo` (Optional. Required if you build Rust implementation of Nextctl) *
1. `go-wayland-scanner` ([Optional](https://github.com/rajveermalviya/go-wayland). required if you build Go implementation of Nextctl) *
1. `go` (Optional. Required if you build Go implementation of Nextctl) *
1. `libevdev`
1. `libinput`
1. `make` *
1. `pixman`
1. `pkg-config` *
1. `scdoc` (Optional. If scdoc binary is not found, man pages are not generated.) *
1. `wayland-protocols` *
1. `wayland`
1. `wlroots` 0.15
1. `xkbcommon`
1. `zig` 0.9.1 *

_\* Compile-time dependencies_

## Steps

```bash
git clone --recursive https://git.sr.ht/~shinyzenith/NextWM
sudo make install
```

## Keybind handling

Consider using the compositors in-built key mapper or [swhkd](https://github.com/shinyzenith/swhkd) if you're looking for a sxhkd like experience.

## Contributing:

Send patches to:
[~shinyzenith/NextWM@lists.sr.ht](https://lists.sr.ht/~shinyzenith/NextWM)

## Bug tracker:

https://todo.sr.ht/~shinyzenith/NextWM

## Support

-   https://matrix.to/#/#waycrate-tools:matrix.org
