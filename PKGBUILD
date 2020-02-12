# Maintainer: Artoria Pendragon <saber-nyan@ya.ru>
# Hooks: https://www.reddit.com/r/archlinux/comments/4zrsc3/keep_your_system_fully_functional_after_a_kernel/d6yin0r/
pkgname=kernel-modules-hook
pkgver=0.1.7
pkgrel=1
pkgdesc="Keeps your system fully functional after a kernel upgrade"
arch=('any')
url="https://github.com/saber-nyan/kernel-modules-hook"
license=('UNLICENSE')
depends=('rsync')
install="${pkgname}.install"
source=("linux-modules-cleanup.conf"
		"linux-modules-cleanup.service"
		"10-linux-modules-post.hook"
		"10-linux-modules-pre.hook"
		"UNLICENSE")
sha256sums=('4169b44c297ddb7aad2220c6eba7c7942e3396f92528c59617955ab5560cb4cf'
            '2f2a055e989dfb595f7bfd1df184e6363b20b1771daa6b605e2608d943e31586'
            'e3ad821ee0f0acafbe502e0b70408b30ff6aa92f37a635893aeabae68eaa77e8'
            'f7ea2947c3fbe1510b3ea5cc5793b8197f0718dcb12daea3da9b27b3cf1c4116'
            '7e12e5df4bae12cb21581ba157ced20e1986a0508dd10d0e8a4ab9a4cf94e85c')

package() {
	install -Dm644 'linux-modules-cleanup.conf' "${pkgdir}/usr/lib/tmpfiles.d/linux-modules-cleanup.conf"
	install -Dm644 'linux-modules-cleanup.service' "${pkgdir}/usr/lib/systemd/system/linux-modules-cleanup.service"
	install -Dm644 '10-linux-modules-post.hook' "${pkgdir}/usr/share/libalpm/hooks/10-linux-modules-post.hook"
	install -Dm644 '10-linux-modules-pre.hook' "${pkgdir}/usr/share/libalpm/hooks/10-linux-modules-pre.hook"
	install -Dm644 'UNLICENSE' "${pkgdir}/usr/share/licenses/${pkgname}/UNLICENSE"
}
