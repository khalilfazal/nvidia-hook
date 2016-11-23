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
sha256sums=('e8f3885be0b17f6973f43a06c6d315f3c69023b16c91884af40ef8f12738bc63')

package() {
  install -dm 755 "${pkgdir}"/usr/lib/initcpio/install
  sed "s/_arch/$CARCH/" -i nvidia
  install -m 644 nvidia "${pkgdir}"/usr/lib/initcpio/install/
}

# vim: ts=2 sw=2 et:
