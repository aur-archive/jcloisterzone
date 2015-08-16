# Maintainer: Kuredant <kuredant[at]gmail[dot]com>

pkgname=jcloisterzone
pkgver=3.1.1
pkgrel=1
pkgdesc="A Java implementation of the popular board game Carcassonne"
arch=('any')
license=('AGPL3')
url="http://jcloisterzone.com/"
depends=('java-environment')
source=("http://jcloisterzone.com/builds/JCloisterZone-${pkgver}.zip"
        "${pkgname}.desktop"
        "${pkgname}.launcher"
        "${pkgname}.png")
sha256sums=('cef289925eb2bd8770a2af0a0bd8247533840335c508c0c5326c607a7d7042f4'
            'b797e5bd69cd9f450935d3869e5352e727bbb9eb52dd0994775b931163aa3c01'
            'a65e0670137634e3e6cd63ff37147e71f459c2cb5f088be539bdb319e0803b9f'
            '012a090df7f1fa30fe3ede444eab92cb2f6fd3c37e1b6786f04da9feb3f7cf38')

package() {
  cd "${srcdir}"

  install -Dm755 "${srcdir}/${pkgname}.launcher" \
      "${pkgdir}/usr/bin/${pkgname}"

  install -Dm644 "${srcdir}/JCloisterZone/JCloisterZone.jar" \
      "${pkgdir}/usr/share/${pkgname}/${pkgname}.jar"
  install -Dm644 "${srcdir}/JCloisterZone/plugins/classic.jar" \
      "${pkgdir}/usr/share/${pkgname}/plugins/classic.jar"
  install -Dm644 "${srcdir}/JCloisterZone/plugins/rgg_siege.jar" \
      "${pkgdir}/usr/share/${pkgname}/plugins/rgg_siege.jar"

  install -Dm644 "${srcdir}/${pkgname}.desktop" \
      "${pkgdir}/usr/share/applications/${pkgname}.desktop"
  install -Dm644 "${srcdir}/${pkgname}.png" \
      "${pkgdir}/usr/share/pixmaps/${pkgname}.png"
}

# vim:set ts=2 sw=2 et:
