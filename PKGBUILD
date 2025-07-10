pkgname=opencode
pkgrel=1
pkgdesc="A brief description of the OpenCode project"
arch=('x86_64' 'arm64')
url="https://github.com/klarkc/opencode"
license=('MIT')
provides=("${pkgname}")
conflicts=("${pkgname}")
vcs=('git')

pkgver=v1.0.0.1.g2810c72

pkgver() {
  git describe --long --tags | sed 's/\([^-]*-\)-g/\1r/' | sed 's/-/./g'
}

source=()

prepare() {
  rsync -a ../ ./
}

build() {
  go build -o opencode .
}

package() {
  install -Dm755 opencode "${pkgdir}/usr/bin/opencode"
}
