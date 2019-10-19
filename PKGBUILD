# Maintainer: Khralkatorrix <garuda2550@gmail.com>

pkgname=libgw2dattools
_pkgname=gw2dattools
pkgver=1.0.r64.65e7244
pkgrel=1
pkgdesc="Collection of tools to make building programs for the Guild Wars 2's dat file easier."
arch=('x86_64')
url="https://github.com/kytulendu/gw2dattools"
license=(GPL)
makedepends=(cmake)
source=("git://github.com/kytulendu/gw2dattools.git")
sha256sums=('SKIP')

pkgver() {
    cd $_pkgname
    echo "1.0.r$(git rev-list --count HEAD).$(git rev-parse --short HEAD)"
}

build() {
    cd $_pkgname
    cmake . -DCMAKE_INSTALL_PREFIX="/usr"
    make
}

package() {
    cd $_pkgname
    make DESTDIR="$pkgdir" install
}
