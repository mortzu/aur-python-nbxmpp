# Maintainer:
# Contributor: Eric Bélanger <eric@archlinux.org>

pkgname=python-nbxmpp
pkgdesc="A Python library to use Jabber/XMPP networks in a non-blocking way"
pkgver=1.0.0
pkgrel=1
arch=(any)
url="https://dev.gajim.org/gajim/python-nbxmpp/"
license=(GPL3)
depends=(python)
source=($pkgname-$pkgver.tar.gz::https://dev.gajim.org/gajim/python-nbxmpp/repository/nbxmpp-$pkgver/archive.tar.gz)
sha256sums=('754c0ef2a5a58fc47e520f711ed1327957129510e98e1a4957d32126c9336557')

prepare() {
  mv $pkgname-nbxmpp-* $pkgname-$pkgver
}

build() {
  cd $pkgname-$pkgver
  python setup.py build
}

package() {
  cd $pkgname-$pkgver
  python setup.py install --root="$pkgdir"
}
