# Maintainer: Khralkatorrix <garuda2550@gmail.com>

pkgname=libgw2dattools
_pkgname=gw2dattools
pkgver=1.0.r65.c1cc7cf
pkgrel=1
pkgdesc="Collection of tools to make building programs for the Guild Wars 2's dat file easier."
arch=('x86_64')
url="https://github.com/kytulendu/gw2dattools"
license=(GPL)
makedepends=(cmake)
source=("git+https://github.com/kytulendu/gw2dattools.git")
sha256sums=('SKIP')

pkgver() {
    cd "${srcdir}/$_pkgname"
    echo "1.0.r$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}

build() {
    cd "${srcdir}/$_pkgname"
    cmake . -DCMAKE_INSTALL_PREFIX="/usr"
    make
}

package() {
    cd "${srcdir}/$_pkgname"
    make DESTDIR="$pkgdir" install
}
