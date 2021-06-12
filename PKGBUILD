pkgname=peco
pkgver=0.5.10
pkgrel=1
pkgdesc='Simplistic interactive filtering tool'
arch=('x86_64')
url='https://github.com/peco/peco'
license=('MIT')
#source=("https://github.com/peco/$pkgname/releases/download/v$pkgver/peco_linux_amd64.tar.gz")
source=("https://github.com/peco/$pkgname/archive/v$pkgver.tar.gz")
makedepends=('go')
sha256sums=('90d87503265c12f8583f5c6bc19c83eba7a2e15219a6339d5041628aa48c4705')

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
sha256sums=('781c2effc4f6a58d9ff96fb0fc8b0fba3aab56a91a34933d68c5de3aea5fe3f6')
