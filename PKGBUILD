# Maintainer: Leonidas P. <jpegxguy at outlook dot com>
# Maintainer: Jerry <isjerryxiao at outlook dot com>
# Contributor: Anes Belfodil <ans.belfodil at gmail dot com>
# Contributor: David Rheinsberg <david.rheinsberg at gmail dot com>
# Contributor: David Herrmann <dh.herrmann at gmail dot com>

_pkgname=qemu-user-static
_pkgver="7.2"
_pkgadditver="+dfsg-5~bpo11+1"
pkgname=${_pkgname}-bin
pkgver=${_pkgver//\~/}
pkgrel=1
pkgdesc='A generic and open source machine emulator, statically linked'
arch=('x86_64' 'i686' 'aarch64' 'armv7h' 'armv6h')
url="http://wiki.qemu.org"
license=('GPL2' 'LGPL2.1')
depends=('binfmt-qemu-static')
provides=("qemu-user" "${_pkgname}" "qemu-arm-static")
conflicts=("qemu-user" "${_pkgname}" "qemu-arm-static")

source_x86_64=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_amd64.deb")
source_i686=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_i386.deb")
source_aarch64=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_arm64.deb")
source_armv7h=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_armhf.deb")
source_armv6h=("https://deb.debian.org/debian/pool/main/q/qemu/${_pkgname}_${_pkgver}${_pkgadditver}_armel.deb")

sha256sums_x86_64=("8ffbf761a3740cb907d42bdb79a5873329d8a43894e8f10a31a2d60f4cae5c3b")
sha256sums_i686=("b887c95d8deee2959e69c9988fe675d8de448ece62e2000ccf60abc089fb4def")
sha256sums_aarch64=("3fc618dd931fa15d61fd3f96ca95986c7dce1dc0a1e3eab2d9e6f7a321bd997f")
sha256sums_armv7h=("d8cb4706c2221cc4e07382dbc9574852424b664bfa36cefef214571751796649")
sha256sums_armv6h=("ad4e684193436c39c4c1d79ec423140922aeb715c75ae3b4f24e96d58224a27d")

package() {
	tar -C "${pkgdir}" -xf "${srcdir}/data.tar.xz" --exclude=./usr/share/man/man1/qemu-debootstrap.1.gz ./usr/bin ./usr/share/man
}
