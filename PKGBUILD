# Maintainer: Malachi Soord <me@malachisoord.com>
pkgname=python2-redactedbetter
pkgver=1
pkgrel=1
pkgdesc="redactedbetter is a script which searches your torrent download directory for any FLAC torrents which do not have transcodes, then automatically transcodes and uploads the torrents to redacted.ch."
arch=('any')
license=('MIT')
depends=('python2' 'python2-pip' 'mktorrent' 'flac')
optdepends=(
	'lame: MP3 support'
	'sox: dither support')
source=("https://github.com/Mechazawa/REDBetter-crawler/archive/ec6228bfeb9a6df6d6686215c6cd372d03ec050e.zip")
sha256sums=('1d535535ddc5bc26076d8ae3d7f8633afcf7bd16f33877cf20c60bb1b45d961e')

build() {
	cd REDBetter-crawler-ec6228bfeb9a6df6d6686215c6cd372d03ec050e
	# PIP_CONFIG_FILE=/dev/null pip2 install --isolated --root="$pkgdir" --ignore-installed --no-deps -r requirements.txt
	python2 setup.py build
}

package() {
	cd REDBetter-crawler-ec6228bfeb9a6df6d6686215c6cd372d03ec050e
	python2 setup.py install --root="$pkgdir/" --optimize=1
}
