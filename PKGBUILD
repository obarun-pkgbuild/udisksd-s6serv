# Maintainer: Eric Vidal <eric@obarun.org>

pkgname=udisksd-s6serv
pkgver=0.1
pkgrel=1
pkgdesc="udisks2 service for s6"
arch=(x86_64)
license=('beerware')
depends=('udisks2' 's6' 's6-rc' 's6-boot')
conflicts=()
source=('udisksd.daemon.run.s6'
		'udisksd.log.run.s6'
		'udisksd.logd'
		'LICENSE')
md5sums=('42f1b01b5ef9a80c4494f0c0186c0aaa'
         '241a50247bb7ca1ac3d79203e7a67960'
         'dee6bca7efbd181ee0507c4d4ee41c1b'
         '191a37ae657aa17e37e75d0242865dba')

package() {
	
	# daemon
	install -Dm 0755 "$srcdir/udisksd.daemon.run.s6" "$pkgdir/etc/s6-serv/available/classic/udisksd/run"
	
	# log
	install -Dm 0755 "$srcdir/udisksd.log.run.s6" "$pkgdir/etc/s6-serv/available/classic/udisksd/log/run"
	install -Dm 0644 "$srcdir/udisksd.logd" "$pkgdir/etc/s6-serv/log.d/udisksd"
	
	install -Dm 0755 "$srcdir/LICENSE" "$pkgdir/usr/share/licenses/udisksd-s6serv/LICENSE"
}
