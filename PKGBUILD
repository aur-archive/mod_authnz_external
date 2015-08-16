# Contributor: Graziano Giuliani <g.giuliani@seco.it>
# Contributor: Pierre Bourdon <delroth@gmail.com>
# Maintainer: Arthur Darcet <arthur.darcet@m4x.org>

pkgname=mod_authnz_external
pkgver=3.3.2
pkgrel=0
pkgdesc='Apache External Authentication Modules'
arch=('i686' 'x86_64')
url='http://code.google.com/p/mod-auth-external/'
license=('Apache')
depends=('apache>=2.4.0')
install=mod_authnz_external.install
source=(http://mod-auth-external.googlecode.com/files/$pkgname-$pkgver.tar.gz)
sha1sums=('c3b9b25b0c2043d1fd7ab4572a01a9c58f226fc1')

package() {
  cd $srcdir/$pkgname-$pkgver
  make build || return 1
  install -D -m755 .libs/mod_authnz_external.so $pkgdir/usr/lib/httpd/modules/mod_authnz_external.so
}
