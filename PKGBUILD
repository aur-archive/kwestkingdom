# Maintainer: David Couzelis <drcouzelis@gmail.com>
pkgname=kwestkingdom
pkgver=0.2
pkgrel=2
epoch=
pkgdesc="A cute 2D turn based strategy game"
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/qogreatness/"
license=('GPL')
groups=()
depends=('allegro4')
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=(http://sourceforge.net/projects/qogreatness/files/${pkgname}-${pkgver}.tar.gz)
noextract=()
md5sums=('5a944f538eed91a12eac301359368662')

build() {
	cd "$srcdir/$pkgname-$pkgver"
	./configure --prefix=/usr
	make
}

check() {
	cd "$srcdir/$pkgname-$pkgver"
	make -k check
}

package() {
	cd "$srcdir/$pkgname-$pkgver"
	make DESTDIR="$pkgdir/" install
	install -D -m644 system/kwestkingdom.png $pkgdir/usr/share/pixmaps/kwestkingdom.png
	install -D -m644 system/kwestkingdom.desktop $pkgdir/usr/share/applications/kwestkingdom.desktop
}
