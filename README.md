# marathi keyboard for Ubuntu
## Instructions to install gamabhana keyboard into ibus...

mkdir gamabhana
mkdir gamabhana/DEBIAN
mkdir -p gamabhana/usr/share/m17n/

wget https://raw.githubusercontent.com/shantanuo/spell_check/master/mr-gamabhana.mim -O /usr/share/m17n/mr-gamabhana.mim

cp /usr/share/m17n/mr-gamabhana.mim gamabhana/usr/share/m17n/

vi gamabhana/DEBIAN/control

Package: gamabhana
Version: 0.1
Maintainer: Shantanu Oak
Architecture: all
Description: gamabhana marathi keyboard for ibus

dpkg-deb --build gamabhana

dpkg -i gamabhana.deb
