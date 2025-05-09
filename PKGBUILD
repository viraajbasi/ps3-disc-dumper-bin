# Maintainer: Viraaj Basi <viraajbasi@gmail.com>
pkgname=ps3-disc-dumper-bin
pkgver=4.3.6
pkgrel=2
pkgdesc="A handy utility to make decrypted PS3 disc dumps"
arch=('x86_64')
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
	'7da0b5b6a762d07deee537b82df0a3daebf2bb540b79c6a590af959a380d3c034dbb884c71b84485310ac39329661df7704d3795c69c8bdddd4f30fbb1a8286d'
	'a79ce33969a60cae727b41fd3bc969be78eb8244911e6c4ad978623f4763f8d8c28c27c9418dc4a40593d0ca613a9b16a63296b514a8c20ba333036b8e0b6de6'
	'06b17f6705cd3e82e3d6cade872e25464346c00624fce88f1f5a3d3ebc1d163a4a5d0f73ba1fe07e0f5f372c7510f054976bd416bcb1088fb4b05487fcaba0d7'
)

package() {
    install -Dm755 "${srcdir}/${pkgname/-bin/}" "${pkgdir}/usr/bin/${pkgname/-bin/}"
    install -Dm644 "${srcdir}/${pkgname/-bin/}-${pkgver}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    install -Dm644 "ps3-disc-dumper.desktop" "${pkgdir}/usr/share/applications/ps3-disc-dumper.desktop"
}
