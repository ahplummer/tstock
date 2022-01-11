# Maintainer: Your Name <gabriel.t.banks@gmail.com>
pkgname=tstock
pkgver=1.0
pkgrel=1
pkgdesc="A simple command-line tool for viewing stock charts in the terminal."
arch=(x86_64)
url="https://github.com/Gbox4/tstock"
license=('GPL')
depends=()
makedepends=(git make)
optdepends=()
provides=(tstock)
source=("git+$url")
md5sums=('SKIP')

# prepare() {
# 	cd "$pkgname-$pkgver"
# 	patch -p1 -i "$srcdir/$pkgname-$pkgver.patch"
# }

build() {
	cd "$pkgname-$pkgver"
	./configure --prefix=/usr
	make
}

check() {
	cd "$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
}