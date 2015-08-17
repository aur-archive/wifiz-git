# Maintainer: Cody Dostal <dostalcody@gmail.com>

pkgname=wifiz-git
_gitname=WiFiz
pkgver=0.9.2.5
pkgrel=2
pkgdesc="Please install NETGUI instead of this one. NetCTL GUI Frontend, 
written in wxPython."
arch=('any')
url="https://github.com/codywd/$_gitname"
license=('MIT')
depends=('python2' 'wxpython' 'wireless_tools' 'netctl' 'wpa_supplicant')
makedepends=('git')
optdepends=('gedit: manually edit profiles')
conflicts=('wifiz' 'wifiz-nightly')
provides=('wifiz')
source=("git://github.com/codywd/$_gitname.git")
sha256sums=('SKIP')

pkgver() {
  cd "$srcdir/$_gitname"
  git describe --always --long | sed -E 's/([^-]*-g)/r\1/;s/-/./g'
}

package() {
  cd "$srcdir/$_gitname"
  python2 setup.py install --root="$pkgdir/" --optimize=1
}
