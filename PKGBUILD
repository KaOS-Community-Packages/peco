pkgname=peco
pkgver=0.5.4
pkgrel=1
pkgdesc='Simplistic interactive filtering tool'
arch=('x86_64')
url='https://github.com/peco/peco'
license=('MIT')
#source=("https://github.com/peco/$pkgname/releases/download/v$pkgver/peco_linux_amd64.tar.gz")
source=("https://github.com/peco/$pkgname/archive/v$pkgver.tar.gz")
makedepends=('go')
sha256sums=('06636082070634256b5adc4c24955ad2c520b24fec528131d0ce203c31aa209d')

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
