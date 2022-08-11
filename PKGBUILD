pkgname=vtmessenger
pkgver=3.1.13
pkgrel=1
pkgdesc="VT Messenger"
arch=(x86_64)
url="https://t.me/vtmsg"
license=(unknown)
depends=(alsa-lib expat gtk3 libgcrypt libgnome-keyring libnotify libxss libxtst nss xdg-utils)
optdepends=(gnome-keyring)
source_x86_64=("linux64.zip")
sha256sums_x86_64=('06feab09d8410349d0635f1757c0afc74327c15b849d3e05fa1a7ea6d31449f3')
noextract=(linux64.zip)
options=(!strip)

pkgver() {
  bsdtar -zxf linux64.zip version
  cat version | sed 's/^v//g'
}

package() {
  install -d "${pkgdir}/opt/vtmessenger"
  bsdtar -xf linux64.zip -C "${pkgdir}/opt/vtmessenger"

  install -d "${pkgdir}/usr/bin"
  ln -s /opt/vtmessenger/vk "${pkgdir}/usr/bin/vtmessenger"

  install -D "${pkgdir}/opt/vtmessenger/icon256.png" "${pkgdir}/usr/share/pixmaps/vtmessenger.png"

  install -d "${pkgdir}/usr/share/applications/"
  cat > ${pkgdir}/usr/share/applications/vtmessenger.desktop << _EOD
[Desktop Entry]
Name=VT Messenger
Exec=/opt/vtmessenger/vk %U
Terminal=false
Type=Application
Icon=vtmessenger
Comment=
Categories=;
_EOD
}
