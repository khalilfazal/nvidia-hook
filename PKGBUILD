# Maintainer: Maxime Gauduin <alucryd@archlinux.org>

pkgname=nvidia-hook
pkgver=2.2
pkgrel=3
pkgdesc='mkinitcpio hook to compile the NVIDIA modules'
url='https://github.com/alucryd/mkinitcpio-hooks'
arch=('any')
license=('GPL3')
depends=('nvidia-dkms')
install='nvidia-hook.install'
source=('https://raw.githubusercontent.com/khalilfazal/nvidia-hook/master/nvidia')
sha256sums=('066f906a785743167b1d772d3ee610125ce7aa0627bf7be8ce3e9574a965a867')

package() {
  install -dm 755 "${pkgdir}"/usr/lib/initcpio/install
  sed "s/_arch/$CARCH/" -i nvidia
  install -m 644 nvidia "${pkgdir}"/usr/lib/initcpio/install/
}

# vim: ts=2 sw=2 et:
