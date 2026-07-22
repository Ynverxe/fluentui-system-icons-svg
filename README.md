# Packaging of FluentUI System Icons for Linux
FluentUI System Icons doesn't have a way to be used in applications other than web, so it doesn't provide a packaging for non-web environments and I wanted to use this SVG icons in my shell. This packaging is for Arch Linux based distros. It installs all svg files under `/usr/share/fluentui-system-icons-remapped` with the format `ic_fluent_<name>_<size>_<regular/filled>.svg`.

## Install
__Arch Linux__
`bash
git clone https://github.com/Ynverxe/fluentui-system-icons-remapped
cd fluentui-system-icons-remapped
makepkg -srci
`
