pkgname="fluentui-system-icons-remapped"
pkgver=1.1.333
pkgrel=1
pkgdesc="SVG files of Microsoft's FluentUI System Icon packaged in a plain layout"
arch=("any")
url="https://github.com/Ynverxe/fluentui-system-icons-remapped"
license=("MIT")
source=("https://github.com/Microsoft/fluentui-system-icons/archive/refs/tags/${pkgver}.tar.gz")
sha256sums=('b96f17d9870841f5156667492042f5793ed50121c40f1789b990373cf696767b')

package() {
  local baseDir="${pkgdir}/usr/share/fluentui-system-icons-remapped"

  install -dm755 $baseDir

  cd $srcdir

  cd "fluentui-system-icons-${pkgver}"

  readarray -d '' -t iconList < <(find assets -type f -name "*.svg" -print0)

  for path in "${iconList[@]}"; do
    install -Dm755 "$path" "$baseDir"
  done
}
