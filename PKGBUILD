# Maintainer: Archlatam <Jose Dragic Corelinux dot org>
# Maintainer: m4teo

pkgname="plymouth-theme-corelinux"
pkgdesc="The default Plymouth theme for Core Linux"
pkgver=r3.148c3ed
pkgrel=1
arch=("any")
url="https://github.com/archlatam/plymouth-theme-corelinux"
license=("GPL-3.0-only")
depends=("plymouth")
makedepends=("git")
source=("git+$url.git")
sha256sums=("SKIP")
install=$pkgname.install

pkgver() {
  cd "$srcdir/$pkgname" || exit
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/$pkgname" || exit

  install -dm755 "$pkgdir/usr/share/plymouth/themes"
  cp -r --no-preserve=ownership usr/share/plymouth/themes/corelinux \
    "$pkgdir/usr/share/plymouth/themes/"

  find "$pkgdir/usr/share/plymouth/themes/corelinux" -type d -exec chmod 755 {} +
  find "$pkgdir/usr/share/plymouth/themes/corelinux" -type f -exec chmod 644 {} +

  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
