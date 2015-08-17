# Maintainer: Simon Perry <aur [at] sanxion [dot] net>
# Contributor: Jonas Nyrén <jonas.nyren*mindkiller.com>

pkgname=sidplay-residfp
pkgver=1.0.1
pkgrel=3
pkgdesc="Sidplay2 fork with improved filter emulation."
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/sidplay-residfp/"
license=('GPL')
depends=('sidplay-residfp-libs>=1.0.1')
install=${pkgname}.install
source=("http://downloads.sourceforge.net/project/sidplay-residfp/sidplayfp/1.0/sidplayfp-${pkgver}.tar.gz")
sha256sums=('052ce23ce2b8857785087d45e06db5fe21eae8b45b2b7ba5618fa2ce7777f679')

build() {
  cd ${srcdir}/sidplayfp-${pkgver}

  ./configure --prefix=/usr --mandir=/usr/man
  make
}

package() {
  cd sidplayfp-${pkgver}
  make DESTDIR="${pkgdir}" install
}

