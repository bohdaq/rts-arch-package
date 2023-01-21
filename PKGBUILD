# Maintainer: Bohdan Tsap <bohdan.tsap@tutanota.com>
pkgname=rust-tls-server
binname=rts
pkgver=9.0.0
pkgrel=1
epoch=
pkgdesc="Web server for handling HTTPS using TLS"
arch=('x86_64')
url="https://github.com/bohdaq/rust-tls-server"
license=('MIT' 'APACHE' 'ISC' 'CC-BY-4.0' 'LGPL-3.0')
groups=()
depends=()
makedepends=(cargo)
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("$pkgname-$pkgver.tar.gz::https://github.com/bohdaq/$pkgname/archive/$pkgver.tar.gz")
sha256sums=('1c22acf96400a9aa85fcd3564b654de95d48b6e8124a5f89806b4dee7ea2a0a9')
noextract=()
validpgpkeys=()

prepare() {
	cd $pkgname-$pkgver
	cargo fetch --target "$CARCH-unknown-linux-gnu"	
}

build() {
	cd $pkgname-$pkgver
	export RUSTUP_TOOLCHAIN=stable
	export CARGO_TARGET_DIR=target
	cargo build --frozen --release --all-features
}

check() {
	cd $pkgname-$pkgver
	export RUST_TOOLCHAIN=stable
	cargo test --frozen --all-features	
}

package() {
	cd $pkgname-$pkgver
	install -Dm0755 -t "$pkgdir/usr/bin" "target/release/$binname"
}
