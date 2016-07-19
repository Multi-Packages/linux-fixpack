pkgname=linux-fixpack
pkgver=1.2
pkgrel=1
pkgdesc="Archivos necesarios para un mejor desempeño en linux y soluciones a algunos errores"
url=""
arch=('x86_64')
license=('Custom')
depends=('systemd')
install=$pkgname.install
source=("disable-freeze.conf" "disable-hugepage.conf"
        "nvidia-vsync.sh"
        "ShimesOne_PERSONAL.ttf" "kenyan coffee rg.ttf"
        "xorg.conf"
        "Windows.png" "usb.png" "shutdown.png" "restart.png" #"Background.png"
        "Daemon.conf"
        "40custom" "30os-prober" "10linux" "Grub"
        "Sudoers"
        )
md5sums=('bd051983fcb130ef9121fa25417d5e26' '4d9c22a72093f21410f76a310106ee83'
         'a8523186e44a27f04f52cb4ee4630346'
         'c7f93cc3b7d43e54ab8b699f9f199b7f' 'cf7776a6e66004c9abacd2e994947c83'
         '201e3d92fee2969d640f35d309c5b290'
         'ea62cd439a461443e9a6f3400bd23ad6' '23f8ca310b6848bccd5e2af5cf4081d3' 'b96d4d35f34abc705238b2526a117c52' '3e3d6b41b73f2187d45b9c6a7c193098'
         '3faad556069aed9b1489ad152e3818e9'
         'e00808081ab479fcc742552961ce2a6b' '483bf6fe365b1478c8f69ec011fc5909' '03fe43503193fefaec1f459a1d31a617' '34f8e9fa9b279d786cfa53eebdbf182f'
         'ec622e17fbbb05503407322cc8e34a91'
         )

# prepare() {
# 
# }

package() {
 install -dm755 "${pkgdir}"/{usr/share/{fonts/TTF,grub/themes/midna/icons},etc/{sysctl.d,tmpfiles.d,profile.d,X11,pulse,grub.d,default}}
    cp -f disable-freeze.conf "${pkgdir}"/etc/sysctl.d
    cp -f disable-hugepage.conf "${pkgdir}"/etc/tmpfiles.d
    cp -f nvidia-vsync.sh "${pkgdir}"/etc/profile.d
    cp -f xorg.conf "${pkgdir}"/etc/X11
    cp -f *.ttf "${pkgdir}"/usr/share/fonts/TTF
#     cp -f Background.png "${pkgdir}"/usr/share/grub/themes/midna/
    cp -f {restart.png,usb.png,Windows.png,shutdown.png} \
    "${pkgdir}"/usr/share/grub/themes/midna/icons
    cp -f Daemon.conf "${pkgdir}"/etc/pulse
    cp -f {40custom,30os-prober,10linux} "${pkgdir}"/etc/grub.d
    cp -f Grub "${pkgdir}"/etc/default
    cp -f Sudoers "${pkgdir}"/etc/
}
