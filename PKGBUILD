# Maintainer nochecksum <nochecksum at users dot noreply dot github dot com>
pkgname=gogs-openrc
pkgver=20151212
pkgrel=1
pkgdesc="Gogs init scripts for OpenRC"
arch=('any')
url="https://github.com/nochecksum/aur-gogs-openrc"
license=('APACHE')
groups=()
depends=('gogs' 'openrc')
makedepends=('git')
source=(git+git://github.com/nochecksum/aur-gogs-openrc)
md5sums=('SKIP')

package() {
	cd "$srcdir"
	install -Dm755 gogs.confd "$pkgdir"/etc/conf.d/gogs
	install -Dm755 gogs.initd "$pkgdir"/etc/init.d/gogs
}
