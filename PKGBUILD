# Contributor: William Rea <sillywilly@gmail.com>
# Contributor: Giorgio Lando <patroclo7@gmail.com>
# Maintainer: Siôn Le Roux <sinisterstuf@gmail.com>

pkgname=tomboy-reminder
pkgver=0.9.1
pkgrel=1
pkgdesc="A tomboy plugin to tell Tomboy to pop up a note when you want to be reminded"
url="http://flukkost.nu/blog/tomboy-reminder/"
depends=('tomboy')
arch=(any)
license=(GPL)
source=("http://flukkost.nu/tomboy-reminder-0.9.1.tar.bz2")
md5sums=('eab03f5e989d72cd4e26daf75444db98')

build() {
  export MONO_SHARED_DIR=$startdir/src/.wabi
  mkdir -p $MONO_SHARED_DIR

  cd $startdir/src/$pkgname-$pkgver
  ./configure --prefix=/usr
  make || return 1
  make DESTDIR=$startdir/pkg install

  rm -r $MONO_SHARED_DIR
}
