# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=udisks-s6serv
pkgver=0.1
pkgrel=1
pkgdesc="udisks service for s6"
arch=(x86_64)
license=('beerware')
depends=('udisks' 's6' 's6-rc' 's6-boot')
conflicts=()
install=udisks-s6serv.install
source=('udisks.daemon.run.s6'
		'udisks.log.run.s6'
		'LICENSE')
md5sums=('9e4bd3b6935dd042c462fe8b9ea2ea89'
         '7c56f2e1a2b9054f50c165b57a3a33de'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/udisks.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/udisks/run"
	
	# log
	install -Dm 0755 "$srcdir/udisks.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/udisks/log/run"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/udisks-s6serv/LICENSE"
}
