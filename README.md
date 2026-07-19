# dmenu — custom build

My personal build of [dmenu](https://tools.suckless.org/dmenu/), the dynamic menu for X, with patches and tweaks applied on top of the vanilla suckless source.

![screenshot](screenshot.png)

## Changes from vanilla dmenu

<!-- List your patches and custom features here. Examples: -->
- **[Patch name]** — short description of what it does
- **[Patch name]** — short description of what it does
- Custom colorscheme / font configured in `config.h`

## Requirements

- Xlib header files (`libx11-dev`, `libxft-dev`, `libxinerama-dev` on Debian/Ubuntu)
- A C compiler and `make`

## Installation

Clone the repository and build:

```sh
git clone https://github.com/YOURUSERNAME/YOURREPO.git
cd YOURREPO
sudo make clean install
```

By default dmenu installs to `/usr/local`. Edit `config.mk` to change the install location or library paths.

## Usage

Run `dmenu_run` to launch programs, or pipe any newline-separated list into `dmenu`:

```sh
ls | dmenu -p "pick a file:"
```

See `man dmenu` for all options.

## Configuration

Configuration is done at compile time by editing `config.h` (fonts, colors, prompt behavior, etc.). After making changes, rebuild and reinstall:

```sh
sudo make clean install
```

## Credits

Based on [dmenu](https://tools.suckless.org/dmenu/) by the [suckless.org](https://suckless.org) team. See `LICENSE` for details.
