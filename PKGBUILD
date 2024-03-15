# SPDX-License-Identifier: AGPL-3.0
#
# Maintainer: Truocolo <truocolo@aol.com>
# Maintainer: Pellegrino Prevete (tallero) <pellegrinoprevete@gmail.com>
# Contributor: Fabio Castelli (muflone) <webreg@muflone.com>

pkgname=mediascan
pkgver=1
pkgrel=2
_pkgdesc=(
  "Scan a directory for media files"
  "using Android media library."
)
pkgdesc="${_pkgdesc[*]}"
arch=(
  any
)
_http="https://github.com"
_ns="themartiancompany"
url="${_http}/${_ns}/${pkgname}"
license=(
  AGPL3
)
depends=(
  bash
)
makedepends=(
  git
)
optdepends=(
  'termux-api: to run in termux'
)
checkdepends=(
  shellcheck
)
source=(
  "git+${_url}"
  Makefile
)
sha256sums=(
  SKIP
  77eb4eb49bc286f772ce32721713e86836afa66547931a6e104414d100957f6e)

check() {
  cd \
    "${pkgname}"
  make \
    -k \
    check
}


package() {
  cd \
    "${pkgname}"
  make \
    PREFIX="/usr" \
    DESTDIR="${pkgdir}" \
    install
}

# vim: ft=sh syn=sh et
