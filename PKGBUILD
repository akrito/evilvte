# Maintainer: Thomas Weißschuh <thomas_weissschuh || lavabit || com>
# Contributor: Zveroy <zy at aafg dot ws>
# Contributor: Jonas Haag <jonas at lophus dot org>
# Contributor: Pardi Tommaso <homer.j.simson.bis at gmail dot com>

pkgname=evilvte-git
pkgver=20120823
pkgrel=1
pkgdesc='VTE based, highly customizable terminal emulator'
url='http://www.calno.com/evilvte/'
arch=('i686' 'x86_64')
provides=('evilvte-git' 'evilvte')
conflicts=('evilvte')
license=('GPL2')
depends=('vte3' 'hicolor-icon-theme')
makedepends=('pkg-config')

# Use these so pkgver gets updated, but we don't really care.
_gitroot="git://github.com/akrito/evilvte.git"
_gitname="evilvte"
install=evilvte.install

build(){
    # Never do this
    cd "$startdir"
    cp -f config.h src/
    ./configure --prefix=/usr
    make
}

package(){
    cd "$startdir"
    make DESTDIR=${pkgdir} install
}
