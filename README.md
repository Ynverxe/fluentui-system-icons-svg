# Packaging of FluentUI System Icons for Linux
FluentUI System Icons is intended to be used in web-applications, so it doesn't provide a packaging for non-web environments and I wanted to use this SVG icons in my shell. This packaging is for Arch Linux based distros. It installs all svg files under `/usr/share/fluentui-system-icons-svg` with the format `ic_fluent_<name>_<size>_<regular/filled>.svg`.

## Install
__Arch Linux__

```bash

git clone https://github.com/Ynverxe/fluentui-system-icons-svg
cd fluentui-system-icons-remapped
makepkg -srci
```
