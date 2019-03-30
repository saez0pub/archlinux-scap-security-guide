# Maintainer: Jean Prat https://github.com/saez0pub/archlinux-scap-security-guide
pkgname=content
pkgver=0.1.43
pkgrel=1
pkgdesc="Baseline compliance content in SCAP formats http://www.open-scap.org/security-policies/scap-security-guide"
arch=('any')
url="http://www.open-scap.org/security-policies/scap-security-guide"
license=('https://github.com/ComplianceAsCode/content/blob/master/LICENSE')
depends=()
makedepends=('cmake' 'make')
source=("https://github.com/ComplianceAsCode/content/archive/v${pkgver}.tar.gz")
md5sums=('e0862326d7512144cee91c6f893557e3')

build() {
	cd "$srcdir/${pkgname}-${pkgver}/build"
	cmake ../
	make -j4
}

package() {
	cd "$srcdir/${pkgname}-${pkgver}/build"
	make DESTDIR="$pkgdir/" install
}
