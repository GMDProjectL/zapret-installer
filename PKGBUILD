pkgname=zapret-installer
pkgver=1.1
pkgrel=1
pkgdesc="Zapret Linux Installer"
arch=('any')
url="https://github.com/GMDProjectL/zapret.installer"
license=('MIT')
depends=('git' 'bash' 'ipset')
makedepends=()
checkdepends=()
optdepends=()
backup=()
options=()
install=
source=(${pkgname}::"git+https://github.com/GMDProjectL/zapret.installer.git")

package() {
    cd "$srcdir"

    install -d "${pkgdir}/opt/zapret.installer"
    install -d "${pkgdir}/usr/share/applications"
    install -d "${pkgdir}/usr/bin"

    cp -a ./zapret-installer/* "${pkgdir}/opt/zapret.installer/"

    cp "../zapret-installer.desktop" "${pkgdir}/usr/share/applications/"

    ln -s /opt/zapret.installer/zapret-control.sh "${pkgdir}/usr/bin/zapret"

    rm -rf "${pkgdir}/opt/zapret.installer/.git"
}
