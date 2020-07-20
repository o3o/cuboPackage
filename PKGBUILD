# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Orfeo Da Vià 
pkgname=cubo
pkgver=0.2.1.r0.e0dcc39
pkgrel=1
pkgdesc="A (meta) build system with multiple backends"
arch=(x86_64)
url="https://github.com/o3o/cubo.git"
license=('Boost')
depends=('liblphobos')
makedepends=(git ldc)
#checkdepends=() usato per le librerie di test
optdepends=()
provides=(cubo)
#backup=() usato per i file di configurazione
source=("git+$url")
md5sums=('SKIP')
#validpgpkeys=()

pkgver() {
   #echo $srcdir
   cd "$srcdir/cubo"
   git describe --long --tags | sed 's/^v//;s/\([^-]*-\)g/r\1/;s/-/./g;s/\.rc./rc/g'
}

build() {
   cd "$pkgname"
   dub build -q --compiler=ldc -brelease
}

check() {
   cd "$pkgname"
   dub test
}

package() {
   # binaries
   install -Dm755 "$srcdir/cubo/cubo" "$pkgdir/usr/local/bin/cubo"
 
 #    install -Dm755 "$srcdir/dfmt/bin/dfmt" "$pkgdir/usr/bin/dfmtinstall -Dm755 "cubo" "${pkgdir}/usr/local/bin/"
}
