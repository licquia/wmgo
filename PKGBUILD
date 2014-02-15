# Maintainer: Max Nickel <max.nickel@gmail.com>

pkgname=wmgo-git
pkgver=9c4d530
pkgrel=1
pkgdesc="A dmenu-based app launcher for EWMH compatible window managers (awesome wm, openbox, etc.)."
url="https://github.com/mnick/wmgo"
arch=('i686' 'x86_64')
license=('GPL')
makedepends=('git')
depends=('dmenu' 'lsx' 'wmctrl')
source=("$pkgname"::'git+https://github.com/mnick/wmgo.git')

pkgver() {
  cd "$srcdir/$pkgname"
  # Use the tag of the last commit
  git describe --long --always | sed -E 's/([^-]*-g)/r\1/;s/-/./g'
}

package () {
    cd "$srcdir"
    install -d -m755 "$pkgdir/usr/bin"
    install -m755 "$srcdir/$pkgname/wmgo" "$pkgdir/usr/bin/wmgo"
}

md5sums=('SKIP')
