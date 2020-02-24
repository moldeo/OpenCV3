## OpenCV3
moldeo plugin for OpenCV Version 3 with full contrib installation

#First compile and install opencv with opencv_contrib, this script will attemp (in debian) to install standard dependencies, clone the 3.4 version from repository, compile it and install it:
./installOpenCV.sh .

#Wait

## Compile the Moldeo OpenCV 3 Plugin

##Like any plugin, you need to have libmoldeo-dev installed from the official repository firt (checkout https://www.moldeo.org/descargas#linux), then install libmoldeo-dev:

#Add key for Moldeo Repository:
sudo apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 0BA12F72

#Adding Moldeo Repository (xenial - Ubuntu 16.04):
sudo apt-add-repository "deb http://www.moldeo.org/repository xenial main"

#Adding Moldeo Repository (bionic - Ubuntu 18.04):
sudo apt-add-repository "deb http://www.moldeo.org/repository bionic main"

#Adding Odoo Moldeo Dev Library:
sudo apt install libmoldeo-dev

##Finally configure, compile and install:
./autogen.sh --prefix=/usr
make
sudo make install
