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
source=("https://github.com/OpenSCAP/scap-security-guide/releases/download/v${pkgver}/scap-security-guide-${pkgver}.zip")
md5sums=('ac895d2e5146817e0e18c520cfa729bc')

build() {
	cd "$srcdir/${pkgname}"
	make
}

package() {
	cd "$srcdir/${pkgname}"
	make DESTDIR="$pkgdir/" SSG_VERSION_IS_GIT_SNAPSHOT=no install
}
