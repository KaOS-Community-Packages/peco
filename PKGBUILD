pkgname=peco
pkgver=0.5.3
pkgrel=1
pkgdesc='Simplistic interactive filtering tool'
arch=('x86_64')
url='https://github.com/peco/peco'
license=('MIT')
#source=("https://github.com/peco/$pkgname/releases/download/v$pkgver/peco_linux_amd64.tar.gz")
source=("https://github.com/peco/$pkgname/archive/v$pkgver.tar.gz")
makedepends=('go')
sha256sums=('ac7d12a1f960ef04afea0c54c5ee754301fb4d85b0e65746826b142de13c843a')

prepare() {
	[[ -e "$srcdir/src" ]] && rm -rf "$srcdir/src"
	mkdir -p "$srcdir/src/github.com/peco"
	mv "$srcdir/$pkgname-$pkgver" "$srcdir/src/github.com/peco/$pkgname"
}

build() {
	[[ ! -e "$srcdir/build" ]] && mkdir "$srcdir/build"
	cd "$srcdir/src/github.com/peco/$pkgname"
	export GOPATH="$srcdir"
	make installdeps
	go build -o "$srcdir/build/$pkgname" "cmd/$pkgname/$pkgname.go"
}

package() {
	install -Dm 755 "$srcdir/build/$pkgname" "$pkgdir/usr/local/bin/$pkgname"
}
