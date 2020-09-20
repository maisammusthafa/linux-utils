pkgname = helios-raspios-utils
src = ../../src/helios-raspios
bin = $(pkgname)/usr/bin

install:
	mkdir -p $(bin)
	rsync -aL --delete $(src)/ $(bin)/
	dpkg-deb --build $(pkgname)
	sudo dpkg -i $(pkgname).deb
	rm -f $(pkgname).deb
