# $Id: PKGBUILD 113973 2014-07-01 10:51:04Z spupykin $
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Contributor: Dag Odenhall <dag.odenhall@gmail.com>
# Contributor: Grigorios Bouzakis <grbzks@gmail.com>

pkgname=dwm
pkgver=6.0
pkgrel=2
pkgdesc="A dynamic window manager for X"
url="http://dwm.suckless.org"
arch=('i686' 'x86_64')
license=('MIT')
options=(zipman)
depends=('libx11' 'libxinerama')
source=('BUGS'
	'config.def.h'
	'config.mk'
	'dwm.1'
	'dwm.c'
	'dwm.png'
	'LICENSE'
	'Makefile'
	'README'
	'TODO'
	'transient.c')
md5sums=('52e14d735198cdea8d8e2bfd4ae4a8d3'
         '2453e037f46449774ec8afab49b4f1a2'
         '5304aecde3f8df8dc8209b64a26fb001'
         'a3266b808f66a4056acf898f43de069f'
         'd29bffe46c2baa33539cb9c5296e4772'
         'b410e9a038520b0a117644dba003da62'
         'db588cfe64c7603bac704cdd0bed61c3'
         '61292cbd8fc92cfae40a4a8267052c99'
         '071f8af116f50e3d6b7ea0ab39b343d0'
         'd8bc5503bee09688adfb9984fb2a96e7'
         '1f002e4c3da39eed17c5581e8649daa1')

build() {
  cd $srcdir
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
  cd $srcdir
  make PREFIX=/usr DESTDIR=$pkgdir install
  install -m644 -D LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
  install -m644 -D README $pkgdir/usr/share/doc/$pkgname/README
}
