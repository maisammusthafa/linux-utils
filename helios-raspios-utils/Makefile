pkgname = helios-raspios-utils

install:
	dpkg-deb --build $(pkgname)
	sudo dpkg -i $(pkgname).deb
	rm -f $(pkgname).deb
