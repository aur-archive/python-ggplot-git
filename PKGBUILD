# Maintainer: dnuux <dnuuxx@gmail.com>

pkgname=python-ggplot-git
_pkgname=ggplot
pkgver=r535.462b833
pkgrel=1
pkgdesc="ggplot for python (git version)"
url="https://github.com/yhat/ggplot/"
arch=('any')
license=('BSD')
depends=('python-pandas' 'python-matplotlib' 'python-statsmodels' 'python-brewer2mpl')
makedepends=('git')
provides=('python-ggplot')
conflicts=('python-ggplot')
source=("git://github.com/yhat/${_pkgname}.git")
sha1sums=("SKIP")

pkgver() {
  cd "${srcdir}/${_pkgname}"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
  cd "${srcdir}/${_pkgname}"
  python setup.py build
}

package() {
  cd "${srcdir}/${_pkgname}"
  python setup.py install --root="${pkgdir}" --optimize=1
}
