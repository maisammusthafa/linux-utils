SHELL := /bin/bash

pkgname = vulcan-arch-utils-1.0.0-1-any.pkg.tar.zst
target = 'vulcan-arch'

.PHONY: install

install:
	@MACHINE="$$(hostname)-$$(sed -n 's/^ID=//p' /etc/*release)"; \
	if [ "$$MACHINE" == $(target) ]; then \
		makepkg -f; \
		sudo pacman -U $(pkgname); \
		rm -rf pkg $(pkgname); \
	else \
		echo error: required target machine is \'$(target)\'; \
	fi
