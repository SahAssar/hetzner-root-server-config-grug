pkgname=hetzner-root-server-config-grug
pkgver=0.0.1
pkgver() {
  # Use number of revisions and hash as version
  cd "$pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}
pkgrel=1
arch=('any')
pkgdesc="A server config for grug, setting domains etc."
url="https://git.grug.se/admin/hetzner-root-server-config-grug"
license=('MIT')
depends=()
makedepends=()
provides=('server-config-grug')
conflicts=('server-config-grug')
install="script.install"
package() {
  mkdir -p "$pkgdir/etc"
  cp server.env "$pkgdir/etc/"
  cp secrets.env.template "$pkgdir/etc/"
}
