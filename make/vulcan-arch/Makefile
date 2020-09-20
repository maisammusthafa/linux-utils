pkgname = vulcan-arch-utils-1.0.0-1-any.pkg.tar.zst
target = 'vulcan'

install:
	@if [ $(shell hostname) == $(target) ]; then \
		makepkg -f;\
		sudo pacman -U $(pkgname);\
		rm -rf pkg $(pkgname);\
	else\
		echo error: required target machine is \'$(target)\';\
	fi
