# Maintainer: Brian Bidulock <bidulock@openss7.org>
# Contributor: Anton Bazhenov <anton.bazhenov at gmail>
# Contributor: gh0stwizard <vitaliy.tokarev@gmail.com>

pkgname=wmifinfo
pkgver=0.11
pkgrel=4
pkgdesc="A simple applet showing basic network configuration for all available interfaces"
arch=('i686' 'x86_64' 'aarch64')
url="https://www.dockapps.net/wmifinfo"
license=('GPL')
depends=('libxpm')
source=("https://www.dockapps.net/download/${pkgname}-${pkgver}.tgz")
md5sums=('361a1797c47632cdd0d9e97c83ca2851')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  install -Dm755 ${pkgname} "${pkgdir}/usr/bin/${pkgname}"
  install -Dm644 README "${pkgdir}/usr/share/doc/${pkgname}/README"
}
