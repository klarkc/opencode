pkgname=opencode
pkgver=$(git describe --tags --always)
pkgrel=1

pkgdesc="A brief description of the OpenCode project"
arch=('x86_64' 'arm64')
url="https://github.com/klarkc/opencode"
license=('MIT')

source=()

prepare() {
  rsync -a --exclude='.git' --exclude='pkg' ../ .
}

build() {
  go build -o opencode .
}

package() {
  install -Dm755 opencode "${pkgdir}/usr/bin/opencode"
}
