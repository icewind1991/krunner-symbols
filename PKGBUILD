# Maintainer: Dominik Schreiber <dev@dominikschreiber.de>
pkgname=plasma5-runners-symbols
pkgver=1.0
pkgrel=1
pkgdesc="A little krunner plugin (Plasma 5) to retrieve unicode symbols, or any other string, based on a corresponding keyword"
arch=('any')
url="https://github.com/domschrei/krunner-symbols"
license=('GPL')
groups=()
depends=()
makedepends=('extra-cmake-modules')
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("git+https://github.com/domschrei/krunner-symbols.git")
noextract=()

prepare() {
  mkdir -p build
}

build() {
  cd build
  cmake ../krunner-symbols -DCMAKE_INSTALL_PREFIX=`kf5-config --prefix` -DQT_PLUGIN_INSTALL_DIR=`kf5-config --qt-plugins` -DCMAKE_BUILD_TYPE=Release
  make
}

package() {
  cd build
  make install DESTDIR="${pkgdir}"
}

md5sums=('SKIP')
