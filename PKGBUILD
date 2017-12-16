pkgname=peco
pkgver=0.5.2
pkgrel=1
pkgdesc='Simplistic interactive filtering tool'
arch=('x86_64')
url='https://github.com/peco/peco'
license=('MIT')
source=("https://github.com/peco/$pkgname/releases/download/v$pkgver/peco_linux_amd64.tar.gz")
sha256sums=('3dfb85c44c68cd10584c9813f96bd979ae1118735819eda9588cc4ef8adcb99f')

package() {
	install -Dm 755 "$srcdir/peco_linux_amd64/peco" "$pkgdir/usr/local/bin/$pkgname"
}
