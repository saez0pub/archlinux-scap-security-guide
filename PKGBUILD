# Maintainer: Jean Prat https://github.com/saez0pub/archlinux-scap-security-guide
pkgname=scap-security-guide
pkgver=0.1.29
pkgrel=1
pkgdesc="Baseline compliance content in SCAP formats http://www.open-scap.org/security-policies/scap-security-guide"
arch=('any')
url="http://www.open-scap.org/security-policies/scap-security-guide"
license=('https://github.com/OpenSCAP/scap-security-guide/blob/master/LICENSE')
depends=()
makedepends=('make' 'git')
source=("https://github.com/OpenSCAP/scap-security-guide/archive/v${pkgver}.zip")
md5sums=('e7f70b3ec76fc50103d8971ea83e6835')

build() {
	cd "$srcdir/${pkgname}-${pkgver}"
	make
}

package() {
	cd "$srcdir/${pkgname}-${pkgver}"
	make DESTDIR="$pkgdir/" SSG_VERSION_IS_GIT_SNAPSHOT=no install
}
