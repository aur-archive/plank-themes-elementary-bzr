# Maintainer: Maxime Gauduin <alucryd@archlinux.org> 

pkgname=plank-themes-elementary-bzr
pkgver=r4
pkgrel=1
pkgdesc='elementary themes for plank'
arch=('any')
url='https://launchpad.net/elementary-community/elementary-plank-themes'
license=('GPL3')
depends=('plank')
makedepends=('bzr')
provides=("${pkgname%-*}")
conflicts=("${pkgname%-*}")
source=("${pkgname%-*}::bzr+http://bazaar.launchpad.net/~versable/elementary-community/elementary-plank-themes/")
sha256sums=('SKIP')

pkgver() {
  cd ${pkgname%-*}

  printf "r%s" "$(bzr revno)"
}

package() {
  cd ${pkgname%-*}

  mkdir -p "${pkgdir}"/usr/share/plank
  cp -dr --no-preserve=ownership themes "${pkgdir}"/usr/share/plank/
}

# vim: ts=2 sw=2 et:
