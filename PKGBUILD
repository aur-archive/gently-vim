# Maintainer: Gently <toddrpartridge@gmail.com>

pkgname=gently-vim
pkgver=0.86
pkgrel=1
pkgdesc="A thorough Vim configuration file meant to replace the local ~/.vimrc."
arch=("any")
url="https://github.com/Gen2ly/gently-vim"
license=("GPL2")
depends=("vim" "vim-jellybeans")
makedepends=("git")
install=${pkgname}.install
changelog=
source=("git://github.com/Gen2ly/gently-vim")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir"/$pkgname
  git describe | sed 's/^v//;s/-.*//'
}

package() {
  cd "$srcdir/$pkgname"
  install -Dm644 license.txt   "$pkgdir"/usr/share/licenses/$pkgname/license.txt
  install -Dm755 ${pkgname/-/.} "$pkgdir"/usr/share/vim/vimfiles/${pkgname/-/.}
}

# vim:set ts=2 sw=2 et:
