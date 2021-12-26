# Maintainer: Gabriel Rasteli <archgabr@tutanota.com>
pkgname=glr-dmenu-git
pkgver=5.0.r7.8d487d0
pkgrel=1
pkgdesc="My personal build of dmenu."
arch=(x86_64)
url="https://gitlab.com/glr01/glr-dmenu.git"
license=('MIT')
depends=(ttf-hack)
makedepends=(git)
checkdepends=()
optdepends=()
provides=(dmenu)
conflicts=(dmenu)
replaces=()
backup=()
options=()
install=
changelog=
source=("git+$url")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
  cd "${_pkgname}"
  printf "5.0.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build () {
  cd glr-dmenu
  make X11NC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
	cd glr-dmenu
  make PREFIX=/usr DESTDIR="${pkgdir}" install
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pgkname}/LICENSE"
  install -Dm644 README.md "${pkgdir}/usr/share/doc/${pgkname}/README.md"
}
