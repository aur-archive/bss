# Archtrack maintainer: Evan Teitelman <teitelmanevan at gmail dot com>
# Contributor: Francesco Piccinno <stack.box@gmail.com>

pkgname=bss
pkgver=0.8
pkgrel=1
pkgdesc="Bluetooth stack smasher / fuzzer"
url="http://www.secuobs.com/news/15022006-bss_0_8.shtml"
license=('GPL')
depends=('python' 'python-pycurl')
arch=(i686 x86_64)
depends=('bluez' 'bluez-libs')
source=(http://www.secuobs.com/$pkgname-$pkgver.tar.gz)
md5sums=('1b5debfd7b4eb6e035677828a7b291dc')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  sed -i -e 's/\/local//g' Makefile
  make

  install -Dm755 bss $pkgdir/usr/bin/bss
  mkdir -p $pkgdir/usr/share/$pkgname/
  cp -r README BUGS TODO replay_packet $pkgdir/usr/share/$pkgname/
}
