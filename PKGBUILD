# $Id: PKGBUILD 65496 2012-02-21 06:39:38Z spupykin $
# Maintainer: Sergej Pupykin <pupykin.s+arch@gmail.com>
# Maintainer: Alex Ciurana <icrave@gmail.com>

pkgname=recorder
pkgver=1.4.5
pkgrel=2
url="http://code.google.com/p/recorder/"
pkgdesc="A simple GTK+ disc burner."
arch=('any')
license=('GPL')
depends=('pygtk' 'cdrkit' 'dvd+rw-tools')
makedepends=('gettext')
optdepends=("vcdimager: Support for VCD/SVCD modes"
	    "cdrdao: Support for VCD/SVCD modes"
	    "vorbis-tools: Support for ogg files on CD Audio mode"
	    "mpg123: Support for mp3 files on CD Audio mode")
source=(http://recorder.googlecode.com/files/$pkgname-$pkgver.tar.bz2)
md5sums=('a56caebad5ae3c1121a5b458abadf415')

build() {
  cd $srcdir/recorder-$pkgver
  # python2 fix
  sed -i 's_#!/usr/bin/env python_#!/usr/bin/env python2_' recorder
  make DESTDIR=$pkgdir install
}
