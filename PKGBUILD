# Maintainer: Bucky 'Igneous' Wolfe <pmigneous@gmail.com>

pkgname=dawn-rpg
pkgver=0.0.47
pkgrel=3
pkgdesc="A 2d RPG set in a fantasy world."
arch=(i686 x86_64)
license=('GPL')
url="http://www.nongnu.org/dawn-rpg/"
#depends=('sdl' 'sdl_image' 'libgl' 'mesa' 'freeglut' 'freetype2' 'lua' 'tolua++')
#source=('http://downloads.sourceforge.net/project/dawn-rpg/dawn-rpg/dawn-0.0.30.tar.gz' 'http://necrotox.in/dawn/configure.patch')
#md5sums=('b798a934c19f5aee6b2587b3ebe2e665' 'ea540f1ccba6d89ec9161ea080712c45')
depends=('sdl' 'sdl_image' 'libgl' 'mesa' 'freeglut' 'freetype2' 'lua' 'tolua++')
source=("http://download.savannah.gnu.org/releases/dawn-rpg/dawn-rpg-${pkgver}.tar.gz")
md5sums=('158c034a1a79f697f496a0a331e5eacb')
build()
{
  cd "${srcdir}/${pkgname}"
#  patch -p0 < ${srcdir}/configure.patch || return 1
  ./configure --prefix=/usr
  make || return 1
}

package()
{
  cd "${srcdir}/${pkgname}"
  make DESTDIR="${pkgdir}" install
}
