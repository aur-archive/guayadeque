# Maintainer: Sial <NAME at cpan dot org>
# Contributor: Ner0
# Contributor: Martin Herndl <martin.herndl@gmail.com>

pkgname=guayadeque
pkgver=0.3.5
pkgrel=4
pkgdesc="A Full Featured Linux media player to manage large collections"
arch=('i686' 'x86_64')
url="http://guayadeque.org/"
license=('GPL3')
depends=('wxgtk' 'sqlite3' 'curl' 'taglib>=1.6.1' 'flac' 'desktop-file-utils')
makedepends=('cmake')
optdepends=('gstreamer0.10-plugins: To play all kind of music files'
	'gvfs: Support for external devices')
conflicts=('guayadeque-svn')
install=$pkgname.install
source=("http://downloads.sourceforge.net/project/$pkgname/$pkgname/$pkgver/$pkgname-$pkgver.tar.bz2")
md5sums=('984921531e4a04c578fdc99783e6068c')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./build
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}
