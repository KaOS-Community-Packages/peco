pkgname=peco
pkgver=0.5.1
pkgrel=1
pkgdesc='Simplistic interactive filtering tool'
arch=('x86_64')
url='https://github.com/peco/peco'
license=('MIT')
source=("https://github.com/peco/$pkgname/releases/download/v$pkgver/peco_linux_amd64.tar.gz")
sha256sums=('75b0c2d6ae671e47936d505cd10c38e91ad3a2a7a2150b5f2d8ff3522c441a31')

package() {
	install -Dm 755 "$srcdir/peco_linux_amd64/peco" "$pkgdir/usr/local/bin/$pkgname"
}
