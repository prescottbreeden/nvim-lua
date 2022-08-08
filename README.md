# Neovim Lunar Setup
This repo requires Neovim 0.8, most packages are pinned so it should remain stable.

[Neovim v0.8.0]](https://github.com/neovim/neovim/releases).  [Upgrade](#upgrade-to-latest-release) if you're on an earlier version. 

## Install
Move your current nvim folder to the side by renaming it `old_nvim_env` or whatever suits your fancy.
Clone this:
```
git clone https://github.com/prescottbreeden/nvim-lua.git ~/.config/nvim
```
Run `nvim` and wait for the plugins to be installed 
You will notice treesitter pulling in a bunch of parsers the next time you open Neovim

**NOTE** The default font on Packer can be impossible to read, use visual block highlighting to read outputs that look like blank lines

## Get healthy

Open `nvim` and enter the following:

```
:checkhealth
```

### Adding support for copy/paste

- On mac `pbcopy` should be builtin

- On Ubuntu

  ```
  sudo apt install xsel
  ```

- On Arch Linux

  ```
  sudo pacman -S xsel
  ```

Next we need to install python support (node is optional)

- Neovim python support

  ```
  pip install pynvim
  ```

- Neovim node support

  ```
  npm i -g neovim
  ```
---

### Upgrade to latest release

Assuming you [built from source](https://github.com/neovim/neovim/wiki/Building-Neovim#quick-start), `cd` into the folder where you cloned `neovim` and run the following commands. 
```
git pull
make distclean && make CMAKE_BUILD_TYPE=Release
sudo make install
nvim -v
```

> The computing scientist's main challenge is not to get confused by the complexities of his own making. 

\- Edsger W. Dijkstra
