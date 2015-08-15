# Maintainer: Arch Haskell Team <arch-haskell@haskell.org>
_hkgname=equal-files
pkgname=equal-files
pkgver=0.0.3
pkgrel=3
pkgdesc="Shell command for finding equal files"
url="http://hackage.haskell.org/package/${_hkgname}"
license=('GPL')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-filemanip<0.4' 'haskell-bytestring=0.9.1.7' 'haskell-explicit-exception<0.1' 'haskell-mtl<1.2')
depends=('gmp')
options=('strip')
source=(http://hackage.haskell.org/packages/archive/${_hkgname}/${pkgver}/${_hkgname}-${pkgver}.tar.gz)
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
md5sums=('dda960866d0ed229fcbddfda58d06d34')
