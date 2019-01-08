# Contributor: Falcony <falcony@users.sourceforge.net>
pkgname=husky-fidoconf
pkgver=1.4rc5
pkgrel=1
pkgdesc="Fidoconfig for Husky hpt Fido messages tosser"
arch=(i686 x86_64)
license=('GPL')
url="http://sourceforge.net/projects/fidoip/"
depends=('unzip')
source=(fidoconf-1.4-rc5.tar.gz)
md5sums=('23ba4abb49ea4fbf28d0255b24e6f627')

build() {
        cp $startdir/huskymak.cfg $srcdir/huskymak.cfg
        cp /var/abs/local/husky-smapi/smapi-2.4-rc5.tar.gz $srcdir
	cd $srcdir ; tar -xzpf smapi-2.4-rc5.tar.gz
	cd $srcdir/fidoconf
	MAKEFLAGS="" make || exit 1
	make PREFIX=$pkgdir/usr/local ETCDIR=$pkgdir/usr/local/etc/fido install || exit 1
}
