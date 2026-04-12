# Maintainer: Viraaj Basi <viraajbasi@gmail.com>
pkgname=ps3-disc-dumper-bin
pkgver=4.4.4
pkgrel=1
pkgdesc="A handy utility to make decrypted PS3 disc dumps"
arch=('x86_64')
provides=('ps3-disc-dumper')
conflicts=('ps3-disc-dumper')
url="https://github.com/13xforever/ps3-disc-dumper"
license=('MIT')
depends=('glibc' 'zlib' 'gcc-libs')
options=('!strip')
source=(
	"https://github.com/13xforever/${pkgname/-bin/}/releases/download/v${pkgver}/${pkgname/-bin/}_linux_v${pkgver}.zip"
	"https://github.com/13xforever/${pkgname/-bin/}/archive/refs/tags/v${pkgver}.tar.gz"
	"ps3-disc-dumper.desktop"
)
b2sums=('6505f6c0702133d68a094fc6da88dc3117ea8dedea09a3d6ce759338885fb10105afd54ec46ed8d01e8ff0ae6deb97634a5b57a9ca56fd73b169b7ed4825e030'
        '648dfd62ede77f0578817651f4b1b1fcc068d7160539fd472af1ccf0d336b5766f4f1399d37c5d345e0627e65dcebdbcf3dc454b0dd5cedbd3cca35e653ecbea'
        '06b17f6705cd3e82e3d6cade872e25464346c00624fce88f1f5a3d3ebc1d163a4a5d0f73ba1fe07e0f5f372c7510f054976bd416bcb1088fb4b05487fcaba0d7')

package() {
    install -Dm755 "${srcdir}/${pkgname/-bin/}" "${pkgdir}/usr/bin/${pkgname/-bin/}"
    install -Dm644 "${srcdir}/${pkgname/-bin/}-${pkgver}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    install -Dm644 "ps3-disc-dumper.desktop" "${pkgdir}/usr/share/applications/ps3-disc-dumper.desktop"
}
