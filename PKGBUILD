# Maintainer:  Andrzej Giniewicz <gginiu@gmail.com>

pkgname=libwacom
pkgver=0.4
pkgrel=1
pkgdesc="Wacom model identification library"
arch=('i686' 'x86_64')
url="http://linuxwacom.sourceforge.net/"
license=('MIT')
source=(http://prdownloads.sourceforge.net/linuxwacom/$pkgname-$pkgver.tar.bz2)
md5sums=('3c047c39da72fdf00fb34a92fe570cfa')
options=(!libtool)

build() {
  cd "${srcdir}"/$pkgname-$pkgver
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}"/$pkgname-$pkgver
  make DESTDIR="${pkgdir}" install
  install -Dm644 COPYING "${pkgdir}"/usr/share/licenses/${pkgname}/COPYING
}

