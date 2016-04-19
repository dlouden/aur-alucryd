# Maintainer: Phillip Schichtel <phillip.public@schich.tel>
pkgname=adapta-gtk-theme
_gtk3_version='3.20'
pkgver="${_gtk3_version}.3.56"
pkgrel=1
pkgdesc="An adaptive Gtk+ theme based on Material Design Guidelines."
arch=(any)
url="https://github.com/tista500/Adapta"
license=('GPL2')
install="${pkgname}.install"
depends=('gtk2' 'gtk3>=3.18' "gtk3<=${_gtk3_version}.99")
optdepends=('paper-icon-theme-git: A fitting icon theme'
            'gnome-tweak-tool: A graphical tool to tweak gnome settings')
source=("${pkgname}.tar.gz::https://github.com/tista500/Adapta/archive/${pkgver}.tar.gz")
sha256sums=(890f0758b6c00b26fa40840c41e8e0d2155575cad4d112eecfd1bc5bbde30e26)

_theme_name=Adapta
_extracted_folder="${_theme_name}-$pkgver"

package() {
    target="${pkgdir}/usr/share/themes/${_theme_name}"
    install -dm755 "$target"
    cp -dpr --no-preserve=ownership "${_extracted_folder}/." "$target"
}
