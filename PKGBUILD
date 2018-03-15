# Maintainer: Malachi Soord <me@malachisoord.com>
pkgname=redactedbetter
pkgver=1
pkgrel=1
pkgdesc="A small Python script that accepts a list of directories containing FLAC files as arguments and converts them to MP3 with the specified options. It can optionally create a torrent file."
arch=('any')
license=('MIT')
depends=('python' 'mktorrent' 'flac')
optdepends=(
	'lame: MP3 support'
	'sox: dither support')
source=("https://github.com/Mechazawa/REDBetter-crawler/archive/ec6228bfeb9a6df6d6686215c6cd372d03ec050e.zip")
sha256sums=('1d535535ddc5bc26076d8ae3d7f8633afcf7bd16f33877cf20c60bb1b45d961e')

build() {
	cd REDBetter-crawler-ec6228bfeb9a6df6d6686215c6cd372d03ec050e
	python setup.py build
}

package() {
	cd REDBetter-crawler-ec6228bfeb9a6df6d6686215c6cd372d03ec050e
	python setup.py install --root="$pkgdir/" --optimize=1
}
