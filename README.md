wxHaskell
=========

wxWidgets wrapper for Haskell

This is
=======

This is a fork of [wxHaskell/wxHaskell](https://github.com/wxHaskell/wxHaskell) intended to hold the necessary changes to build Debian-style binary packages of wxHaskell.

This is not
===========

This is *not* the development branch of wxHaskell. Please refer to [wxHaskell/wxHaskell](https://github.com/wxHaskell/wxHaskell) instead.

Status
======

Prebuilt binary packages for Ubuntu Raring (13.04) and Ubuntu Precise (12.04 LTS), built using this tree, are [provided on my Launchpad PPA](https://launchpad.net/~bert-massop/+archive/wxhaskell/).
The relevant wxWidgets2.9 libraries are also provided for, since they are not yet in the mainline repositories.

This fork has been tested to compile against wxWidgets 2.9.3 and wxWidgets 2.9.5 on Ubuntu Raring (13.04) and Ubuntu Precise (12.04 LTS) by means of the Debian package build mechanism.

Building
========

The easy way
------------

Make sure you have the necessary dependencies installed. These can be found in *debian/control* after *Build-Depends*.

    fakeroot debian/rules binary

The pbuilder way
----------------

Make sure your pbuilder environment has the necessary dependencies available. These can be found in *debian/control* after *Build-Depends*.

    debuild -S -i -I
    pbuilder --build ../haskell-wxhaskell_<version>.dsc --distribution <distro>
