# Maintainer: Viraaj Basi <viraajbasi@gmail.com>
pkgname=ps3-disc-dumper-bin
pkgver=4.3.7
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
b2sums=(
	'3b82f36503ad2894668c122eb39d42c1f266845f881e2cfdb9b55f061094ed215805d6c4f92f3d000b566535aec868ddb4449ae8d2f4cea4bec226ebaa02cf5a'
	'a4295c6c28754ea502ac08c9be8c50b66f19bbf78ba4a6ff79a2db017226fdc72ec9e07489f389605f9475c77ef6b27bbaf05a969ef9a03f8387d93589192e5d'
	'06b17f6705cd3e82e3d6cade872e25464346c00624fce88f1f5a3d3ebc1d163a4a5d0f73ba1fe07e0f5f372c7510f054976bd416bcb1088fb4b05487fcaba0d7'
)

package() {
    install -Dm755 "${srcdir}/${pkgname/-bin/}" "${pkgdir}/usr/bin/${pkgname/-bin/}"
    install -Dm644 "${srcdir}/${pkgname/-bin/}-${pkgver}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    install -Dm644 "ps3-disc-dumper.desktop" "${pkgdir}/usr/share/applications/ps3-disc-dumper.desktop"
}
