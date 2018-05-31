pkgname=ruby-bundler
pkgver=1.16.2
pkgrel=1
pkgdesc='Bundler manages an application’s dependencies through its entire life, across many machines, systematically and repeatably'
arch=('x86_64')
url='https://bundler.io'
license=('MIT')
depends=('ruby')
options=('!emptydirs')
source=("https://rubygems.org/downloads/${_gemfile}")
noextract=("${_gemfile}")
sha256sums=('3bb53e03db0a8008161eb4c816ccd317120d3c415ba6fee6f90bbc7f7eec8690')
_gemfile="bundler-${pkgver}.gem"

package() {
	local _gd="$(gem environment gemdir)"
	gem install \
		-i "${pkgdir}/${_gd}" \
		-n "${pkgdir}/usr/bin" \
		--no-user-install \
		--no-document \
		--ignore-dependencies \
		"${srcdir}/${_gemfile}"
}
