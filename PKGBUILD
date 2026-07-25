pkgbase=fluentui-system-icons
pkgname=(
  "fluentui-system-icons-svg"
  "fluentui-system-icons-devices-icon-theme"
)
pkgver=1.1.333
pkgrel=1
pkgdesc="SVG files of Microsoft's FluentUI System Icon packaged in a plain layout"
arch=("any")
url="https://github.com/Ynverxe/fluentui-system-icons-remapped"
license=("MIT")
source=("https://github.com/Microsoft/fluentui-system-icons/archive/refs/tags/${pkgver}.tar.gz")
sha256sums=('b96f17d9870841f5156667492042f5793ed50121c40f1789b990373cf696767b')

package_fluentui-system-icons-svg() {
  local baseDir="${pkgdir}/usr/share/fluentui-system-icons-remapped"

  install -dm755 $baseDir

  cd $srcdir

  cd "fluentui-system-icons-${pkgver}"

  readarray -d '' -t iconList < <(find assets -type f -name "*.svg" -print0)

  for path in "${iconList[@]}"; do
    install -Dm755 "$path" "$baseDir"
  done
}

package_fluentui-system-icons-devices-icon-theme() {
  depends=('fluentui-system-icons-svg')
  declare -A mappings=(
    ["audio-input-microphone"]="mic"
    ["battery"]="battery_10"
    ["battery-caution"]="battery_warning"
    ["camera-photo"]="camera"
    ["camera-video"]="video"
    ["computer"]="desktop"
    ["computer-laptop"]="laptop"
    ["drive-harddisk"]="hard_drive"
    ["drive-optical"]="cd"
    ["input-gaming"]="xbox_controller"
    ["input-keyboard"]="keyboard"
    ["input-tablet"]="pen_sparks"
    ["drive-removable-media"]="storage"
    ["media-flash"]="storage"
    ["media-flop"]="storage"
    ["network-wireless"]="wifi_1"
    ["phone"]="phone"
    ["smartphone"]="phone"
    ["printer"]="print"
    ["video-display"]="tv"
  )
}
