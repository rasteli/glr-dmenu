# Maintainer: Gabriel Rasteli <archgabr@tutanota.com>
pkgname=glr-dmenu-git
pkgver=5.0
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

package() {
	cd glr-dmenu
	make DESTDIR="$pkgdir/" install
}
