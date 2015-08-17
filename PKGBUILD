# Maintainer: Simon Hafner <hafnersimon@gmail.com>
pkgname=opensc_epass2003
pkgver=7b79dbc
pkgrel=1
pkgdesc="Access smart cards that support cryptographic operations"
arch=(i686 x86_64)
url="https://github.com/entersafe/OpenSC/tree/ePass2003_1"
license=('LGPL')
groups=()
depends=(openssl pcsclite libltdl)
makedepends=('git')
provides=(opensc)
conflicts=(opensc)
replaces=()
backup=()
options=()
install=
source=("https://github.com/entersafe/OpenSC/zipball/ePass2003_1")
md5sums=('b6c31f74f8a5e484f2287efc4398414b')
noextract=()

build() {
  cd "$srcdir/entersafe-OpenSC-$pkgver"
  ./bootstrap
  ./configure --prefix=/usr --sysconfdir=/etc/opensc --enable-openssl
  make
}

package() {
  cd "$srcdir/entersafe-OpenSC-$pkgver"
  make DESTDIR="$pkgdir/" install
}

# vim:set ts=2 sw=2 et:
