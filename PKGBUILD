# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: uberushaximus <uberushaximus AT gmail DOT com>

_gemname=leveldb
pkgname=ruby-$_gemname
pkgver=0.1.9
pkgrel=1
pkgdesc='LevelDB for Ruby'
arch=(i686 x86_64)
url='https://github.com/DAddYE/leveldb'
license=(MIT)
depends=(ruby ruby-fiddler-rb)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('b430d0e9d0ea03bf7b58ccd76ff18f6325044aa6')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
}
