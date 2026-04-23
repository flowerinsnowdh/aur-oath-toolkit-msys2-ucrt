# SPDX-License-Identifier: GPL-3.0-or-later

# Copyright (C) 2026  flowerinsnow
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <https://www.gnu.org/licenses/>.

pkgname='oath-toolkit-msys2-ucrt'
pkgver='2.6.14'
pkgrel='1'
pkgdesc='OATH one-time password toolkit'
arch=('x86_64')
url='https://oath-toolkit.codeberg.page/'
license=(
    'GPL-3.0-or-later'
)
depends=(
    'mingw-w64-ucrt-x86_64-gcc-base'
)
provides=(
    "oath-toolkit=${pkgver}-${pkgrel}"
)
conflicts=(
    'oath-toolkit'
)
source=(
    "https://download.savannah.nongnu.org/releases/oath-toolkit/oath-toolkit-${pkgver}.tar.gz"
    "https://download.savannah.nongnu.org/releases/oath-toolkit/oath-toolkit-${pkgver}.tar.gz.sig"
)
validpgpkeys=(
    'B1D2BD1375BECB784CF4F8C4D73CF638C53C06BE'
)
b2sums=(
    '0d20e9d60350268080abd245b47bd84ae426a0007cba8af049994a1f6a5f9153220a570f3ff93432a8c369e8becc342011cea46cf3c75cad2e3f8a70107af2e3'
    'f0db16bedcd731a3f25d26bb2a303fc2bef91e5fdfedc24cd0e5ae7c6c2ec19bd0d68f2931632cb3bcad279cccf4e400b70439d1b1715ef3c373792d7e8cd32d'
)
build() {
    cd "${srcdir}/oath-toolkit-${pkgver}/" && \
        ./configure && make
}
package() {
    install -Dm755 "${srcdir}/oath-toolkit-${pkgver}/oathtool/oathtool.exe" "${pkgdir}/usr/bin/oathtool.exe" && \
        install -Dm644 "${srcdir}/oath-toolkit-${pkgver}/liboath/oath.h" "${pkgdir}/usr/include/liboath/oath.h" && \
        install -Dm644 "${srcdir}/oath-toolkit-${pkgver}/liboath/liboath.pc" "${pkgdir}/usr/lib/pkgconfig/liboath.pc"
}
