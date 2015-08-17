pkgname=ttf-d2fonts
pkgver=1.3
pkgrel=2
pkgdesc="Put Descent fonts into Word documents and more."
arch=(any)
url="http://descentvalhalla.com/d2/downloads/fonts.aspx"
license=("Non-commercial redistribution")
depends=(fontconfig xorg-font-utils)
makedepends=(dos2unix)
source=("http://descentvalhalla.com/files/d2/misc/fonts/${pkgname#ttf-}.zip")
md5sums=('6bb429ebcd20f40e55bc3120110c7749')
install=$pkgname.install

prepare() {
	find "$srcdir" -type f -exec dos2unix {} \;
}

package() {
  install -Dm644 "$srcdir/DESCLOGO.TTF" "$pkgdir/usr/share/fonts/TTF/DESCLOGO.TTF"
  install -m644 "$srcdir/DESCMENU.TTF" "$pkgdir/usr/share/fonts/TTF/DESCMENU.TTF"
  install -m644 "$srcdir/DESCSCOR.TTF" "$pkgdir/usr/share/fonts/TTF/DESCSCOR.TTF"
  install -Dm644 "$srcdir/LIESMICH.TXT" "$pkgdir/usr/share/licenses/$pkgname/LIESMICH.TXT"
  install -m644 "$srcdir/README.TXT" "$pkgdir/usr/share/licenses/$pkgname/README.TXT"
}
