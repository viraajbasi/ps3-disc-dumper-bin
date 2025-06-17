# Maintainer: Viraaj Basi <viraajbasi@gmail.com>
pkgname=ps3-disc-dumper-bin
pkgver=4.3.8
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
	'137ccb4d868bea5d9812baa6fcf2a152faf48361ef2f94162b3524c2f36e1e0c8cc5ae9a6d6bd973dd36827d360a0d27bbbf7467e996585a5d394bde1f982f20'
	'a04ebce59dfe0b55cb3908320bc2a89cd0b0a058aac2b04b013d7e7e815add57a7cd279d04fecd4d51397a4ab98d490a2919e204d53e602be79bdb6044a7d812'
	'06b17f6705cd3e82e3d6cade872e25464346c00624fce88f1f5a3d3ebc1d163a4a5d0f73ba1fe07e0f5f372c7510f054976bd416bcb1088fb4b05487fcaba0d7'
)

package() {
    install -Dm755 "${srcdir}/${pkgname/-bin/}" "${pkgdir}/usr/bin/${pkgname/-bin/}"
    install -Dm644 "${srcdir}/${pkgname/-bin/}-${pkgver}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    install -Dm644 "ps3-disc-dumper.desktop" "${pkgdir}/usr/share/applications/ps3-disc-dumper.desktop"
}
