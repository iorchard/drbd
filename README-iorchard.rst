Build drbd debian package
==========================

This is a guide to build drbd package for debian 11 (bullseye).

Install pre-requisite package.::

   $ sudo apt install -y dkms build-essential \
         flex autoconf automake \
         debhelper devscripts

List tags to build.::

   $ git tag -l

Check out the tag.::

   $ git checkout drbd-9.0.28-1

Build debian package.::

   $ debuild -b -us -uc

The deb packages are in upper directory.::

   $ $ ls drbd-dkms*.deb
   drbd-dkms_9.0.28-1_all.deb

