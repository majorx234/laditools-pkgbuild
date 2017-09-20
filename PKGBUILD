# Maintainer: WoefulDerelict <WoefulDerelict at GMail dot com>

pkgname=laditools
pkgver=1.1.0
pkgrel=2
pkgdesc="Utilities to improve integration and workflow with JACK and LASH."
arch=('any')
url="https://launchpad.net/laditools"
license=('GPL3')
depends=('glade' 'jack' 'pygtk' 'python2' 'python2-enum34' 'python2-yaml')
makedepends=('git' 'python2-distutils-extra')

_tag=v${pkgver}
_dir=${pkgname}
source=("${_dir}"::"git+https://github.com/alessio/laditools.git")
sha256sums=('SKIP')

build() {
  cd "${srcdir}/${pkgname}"
  python2 setup.py build
}

package() {
  cd "${srcdir}/${pkgname}"
  python2 setup.py install --prefix=/usr --root="${pkgdir}/"
}
