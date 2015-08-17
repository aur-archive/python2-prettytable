# Maintainer: Sebastien Leduc <sebastien@sleduc.fr>
# Contributor: Emmanuel Gil Peyrot <linkmauve@linkmauve.fr>

pkgname='python2-prettytable'
pkgver=0.7.2
pkgrel=2
pkgdesc="A simple Python library for easily displaying tabular data in a visually appealing ASCII table format"
url="http://pypi.python.org/pypi/PrettyTable"
arch=('any')
license=('BSD')
depends=('python2')
makedepends=('python2-distribute')
source=("http://pypi.python.org/packages/source/P/PrettyTable/prettytable-${pkgver}.tar.gz")
md5sums=('a6b80afeef286ce66733d54a0296b13b')

build() {
  cd "$srcdir/prettytable-$pkgver"
  python2 setup.py build
}

package() {
  cd "$srcdir/prettytable-$pkgver"
  chmod 644 -R prettytable.egg-info
  python2 setup.py install --root="$pkgdir/"
}
