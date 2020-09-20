pkgname = helios-arch-utils-1.0.0-1-any.pkg.tar.zst

install:
	makepkg -f
	sudo pacman -U $(pkgname)
	rm -rf pkg $(pkgname)
