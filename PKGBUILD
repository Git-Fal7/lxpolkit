pkgname=lxpolkit
pkgver=0.1.0
pkgrel=1
pkgdesc="Simple policykit authentication agent for LXDE"
arch=('i686' 'x86_64')
url="http://blog.lxde.org/?p=674"
license=('GPL')
depends=('gtk2' 'polkit')
makedepends=('intltool')
source=(git+git://github.com/git-fal7/lxpolkit)
md5sums=('SKIP')

build() {
  cd "$srcdir/$pkgname"
  chmod +x ./configure
  ./configure --prefix=/usr --sysconfdir=/etc --libexecdir=/usr/lib/$pkgname
  make
}

package() {
  cd "$srcdir/$pkgname"
  make DESTDIR="$pkgdir/" install
}
