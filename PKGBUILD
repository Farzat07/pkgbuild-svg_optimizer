# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: A Farzat <a@farzat.xyz>

_gemname=svg_optimizer
pkgname=ruby-$_gemname
pkgver=0.3.0
pkgrel=1
pkgdesc="SVG optimization based on Node's SVGO"
arch=(any)
url='https://github.com/fnando/svg_optimizer'
license=(MIT)
depends=(ruby ruby-nokogiri)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('4595963f857d7a2d794a1a2be4fe32aa379d6d15')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.md" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.md"
}