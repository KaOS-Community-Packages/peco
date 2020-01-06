pkgname=peco
pkgver=0.5.5
pkgrel=1
pkgdesc='Simplistic interactive filtering tool'
arch=('x86_64')
url='https://github.com/peco/peco'
license=('MIT')
#source=("https://github.com/peco/$pkgname/releases/download/v$pkgver/peco_linux_amd64.tar.gz")
source=("https://github.com/peco/$pkgname/archive/v$pkgver.tar.gz")
makedepends=('go')
sha256sums=('ce4191cb16d924c81cce1ebd0340d98739794745d19565ba8a84ef1e12e1960c')

build() {
	cd "${srcdir}/${pkgname}-${pkgver}"
	GOFLAGS=-mod=vendor
	go mod vendor
	make build
}

package() {
	install -Dm 755 \
	        "${srcdir}/${pkgname}-${pkgver}/releases/${pkgname}_linux_amd64/${pkgname}" \
	        "$pkgdir/usr/local/bin/$pkgname"
}
