
Automatically exported from code.google.com/p/pymissile

# From Google Code repo:

## pymissile

Control your Marks and Spencer USB Missile Launcher on Linux (and maybe other platforms that support python and libusb).

## Tested on

* Ubuntu-5.04
  * (please report other success stories) 

## Requirements

* python (>=2.3)
* libusb (>=0.1.8)
* pyusb (==0.3.1) python module with patch included below
* urwid python module 

## Install

1. ensure python is installed and right version

2. install libusb-0.1.18 or better (available [here][1]) or use package appropriate for your distro, e.g. on ubuntu:

  ~~~
  $ sudo apt-get install libusb-dev
  ~~~

3. install pyusb-0.3.1 (available [here][2] or [archived here][3]) but patched (see below):

  ~~~
  $ wget http://pymissile.googlecode.com/svn/trunk/pyusb-0.3.1.tar.gz
  $ tar zxvf pyusb-0.3.1.tar.gz
  $ cd pyusb-0.3.1
  $ wget http://pymissile.googlecode.com/svn/trunk/pyusb-0.3.1-kernel-detach.patch
  $ patch -p1 < pyusb-0.3.1-kernel-detach.patch
  $ sudo python setup.py install
  ~~~

4. install urwid-0.8.10 (available [here][4])
5. plug in Missile Launcher
6. run missile.py as root (maybe non-root will work if you mess with libusb, let me know the details if that's the case)

  ~~~
  $ wget http://pymissile.googlecode.com/svn/trunk/missile.py 
  $ chmod +x ./missile.py
  $ sudo ./missile.py
  ~~~

## Screenshot and Videos


## Usage

1. Install
2. Aim
3. ...
4. Profit$ 

## Todo

* commandline interface
* use webcam and motion to have automated sentry (aim and fire)
  * DONE but not documented yet 
* daemon and xmlrpc interface for remote aim and shooting of coworkers
  * SORT OF DONE: manual control is available via the above TODO, needs documentation 


  [1]: http://libusb.sourceforge.net/
  [2]: http://sourceforge.net/projects/pyusb/
  [3]: http://pymissile.googlecode.com/svn/trunk/pyusb-0.3.1.tar.gz
  [4]: http://excess.org/urwid/
  [5]: http://motion.sourceforge.net/
