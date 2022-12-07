pkgname=arch-tor-auto-socket
pkgver=1.0
pkgrel=0
pkgdesc="Automated starting and stopping of tor on port 9050"
url="https://github.com/p1x3l101-10/arch-tor-auto-socket"
licence=('none')
arch=('any")
depends=('systemd' 'tor')
provides=("${pkgname}")
source=(
  'torrc.socket.conf'
  'tor-socket.service'
  'tor-proxy.service'
  'tor-proxy.socket'
)
sha256sums=('SKIP' 'SKIP' 'SKIP' 'SKIP')

package() {
  cd "$srcdir/$pkgname"
  install -Dm644 torrc.socket.conf "$pkgdir/etc/tor/torrc.socket.conf"
  install -Dm644 tor-socket.service "$pkgdir/usr/lib/systemd/system/tor-socket.service"
  install -Dm644 tor-proxy.service "$pkgdir/usr/lib/systemd/system/tor-proxy.service"
  install -Dm644 tor-proxy.socket "$pkgdir/usr/lib/systemd/system/tor-proxy.socket"
}
