# Maintainer: BigfootACA <bigfoot@classfun.cn>

_pyname=django-debreach
pkgname=python-$_pyname
pkgver=2.0.1
pkgrel=1
pkgdesc="Adds middleware to give some added protection against the BREACH attack in Django."
arch=(any)
url="http://github.com/lpomfrey/django-debreach"
license=(BSD)
depends=(
	python
	python-django
)
makedepends=(python-setuptools)
source=(https://pypi.io/packages/source/${_pyname::1}/$_pyname/$_pyname-$pkgver.tar.gz)
md5sums=('db16c67273d9be65618ef2910c8b23c8')
sha256sums=('3dd90385918daef4951e67ef6c3dcb550ac5164d84f5cc9889ed52e312597d68')
sha512sums=('7b18e7232a376683e3ad42d09878718cf08186c6ddc4bd05c3e30bbbe82f4e07f074910a9943078b1fed7fa708d21591d4489ea8ae162803a61c56fe705f4145')

check(){
	cd $_pyname-$pkgver
	python runtests.py
}

package(){
	cd $_pyname-$pkgver
	python setup.py install --root "$pkgdir" --optimize=1
	install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
