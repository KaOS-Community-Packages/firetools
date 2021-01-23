pkgname=firetools
pkgver=0.9.64
pkgrel=1
pkgdesc='Graphical user interface of Firejail security sandbox.'
arch=('x86_64')
url='https://firejailtools.wordpress.com/'
license=(GPL2)
depends=('firejail')
source=("https://github.com/netblue30/firetools/releases/download/${pkgver}/firetools-${pkgver}.tar.xz")
md5sums=('a95af117c8bd1c78a67de450a8ecb97a')

build(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr --with-qmake=/usr/bin/qmake-qt5
    make -j$(nproc)

}

package(){

    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
