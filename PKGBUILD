# Maintainer: Arda Atci<phystecharda@gmail.com>
pkgname=dwm-phyOS
pkgver=6.4
pkgrel=1
pkgdesc="dwm build for phyOS"
arch=(x86_64)
url="git://github.com/PhyTech-R0/dwm-phyOS"
license=('MIT')
depends=('libxcb' 'libxft-bgra' 'imlib2' 'libconfig')
makedepends=('git' 'make')
optdepends=('fonts-phyOS' 'dmenu-phyOS' 'st-phyOS' 'dwmblocks-phyOS')
provides=("dwm")
conflicts=("dwm")
options=('zipman')
source=('git+https://github.com/PhyTech-R0/dwm-phyOS')
md5sums=('SKIP')

package() {
	cd "$pkgname"
	[ -f "$HOME/.config/phyos/dwm/keys.h" ] && yes | cp -f "$HOME/.config/phyos/dwm/keys.h" ./keys.h
	make
	make PREFIX=/usr DESTDIR="$pkgdir/" install
}
