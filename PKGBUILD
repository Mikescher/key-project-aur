# Maintainer: Mikescher <aur@mikescher.com>
# Repo:       https://github.com/Mikescher/key-project-aur

pkgname=key-project
pkgver=2.10.0
pkgrel=1

pkgdesc="A program to use formal verification with Java programs"

url="https://www.key-project.org/"
license=('GPL')

arch=('any')
depends=('java-runtime')

source=(
  "key-project"
  "key-project.desktop"
  "key-project16.png"
  "key-project32.png"
  "key-project64.png"
  "https://www.key-project.org/dist/$pkgver/key-$pkgver-exe.jar"
)

noextract=("key-$pkgver-exe.jar")

sha256sums=(
  '102d85d94612272a66bf4612b06ffa0561b709bbeb3ea55ed9bd28b339211f18'
  'e7ec88c40bce27a7c344c90bc39c54a0f2a20e239f277a6e77cdbf6036957d7f'
  'f88c92559367ca052427ef090fa934a39753200a029a29b83092309912df36a8'
  'ac2686c9d152af629f3beb2bcf219b8017df37adb8534ab054184c14b5e40b62'
  'ac2686c9d152af629f3beb2bcf219b8017df37adb8534ab054184c14b5e40b62'
  'eda4c9550ca5ca759f52c461a811d87dfb44dec9ec4bf3029eda4dd5cc33f145'
)

package()
{

  install -D -m644 "$srcdir/key-project.desktop"         "$pkgdir/usr/share/applications/key-project.desktop"

  install -D -m644 "$srcdir/key-project16.png"           "$pkgdir/usr/share/icons/hicolor/16x16/apps/key-project.png"
  install -D -m644 "$srcdir/key-project32.png"           "$pkgdir/usr/share/icons/hicolor/32x32/apps/key-project.png"
  install -D -m644 "$srcdir/key-project64.png"           "$pkgdir/usr/share/icons/hicolor/64x64/apps/key-project.png"

  mkdir -p "$pkgdir/usr/share/java/key-project"

  install -D -m644 "$srcdir/key-$pkgver-exe.jar"          "${pkgdir}/usr/share/java/key-project/key-project.jar"
  install -D -m755 "$srcdir/key-project"                 "${pkgdir}/usr/bin/key-project"

}

