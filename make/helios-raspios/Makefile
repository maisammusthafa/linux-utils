SHELL := /bin/bash

pkgname := helios-raspios-utils
src := ../../src/helios-raspios
bin := $(pkgname)/usr/bin
target := 'helios-raspbian'

.PHONY: install

install:
	@MACHINE="$$(hostnamectl hostname)-$$(sed -n 's/^ID=//p' /etc/*release)"; \
	if [ "$$MACHINE" == $(target) ]; then \
		mkdir -p $(bin); \
		rsync -aL --delete $(src)/ $(bin)/; \
		dpkg-deb --build $(pkgname); \
		sudo dpkg -i $(pkgname).deb; \
		rm -f $(pkgname).deb; \
	else \
		echo error: required target machine is \'$(target)\'; \
	fi
