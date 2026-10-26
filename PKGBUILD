# Maintainer: Archlatam <Jose Dragic Corelinux dot org>
# Maintainer: m4teo

pkgname="plymouth-theme-corelinux"
pkgdesc="The default Plymouth theme for Core Linux"
pkgver=r2.b83ca55
pkgrel=1
arch=("any")
url="https://github.com/archlatam/plymouth-theme-corelinux"
license=("GPL")
makedepends=("git")
source=("git+$url.git")
sha256sums=("SKIP")
install=$pkgname.install

pkgver() {
  cd "$srcdir/$pkgname" || exit
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  install -d "$pkgdir/usr/share/plymouth/themes/corelinux"
  cp -rf "$srcdir/$pkgname/usr" "$pkgdir"
}
