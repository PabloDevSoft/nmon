#
# Contribuidor: Pablo Henrique <pablohenriquedev32@gmail.com>
#

pkgname=nmon
pkgver=16n
pkgrel=2
pkgdesc="Ferramenta de monitoramento de desempenho AIX e Unix."
arch=('x86_64')
url="http://localhost/nmon"
license=('GPL')
depends=('ncurses')
source=("nmon.tar.gz")
sha256sums=('SKIP')

build()
{
    cd "$pkgname"
    cc -o nmon lmon$pkgver.c $LDFLAGS $CFLAGS -g -O3 -lncurses -lm -D X86
}

package()
{
    cd "$pkgname"
    install -D -m 0755 nmon "$pkgdir/usr/bin/nmon"
}
