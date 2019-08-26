Document where to download the source file and how to compile binary:

busybox:
  Source for the latest released version, as well as daily snapshots,
  can always be downloaded from: https://busybox.net/downloads/
  Compile steps : make defconfig / make menuconfig / make

  BusyBox is extremely configurable.  This allows you to include only the
  components and options you need, thereby reducing binary size.  Run 'make
  config' or 'make menuconfig' to select the functionality that you wish to
  enable.  (See 'make help' for more commands.)


dmidecode:
  Can always be downloaded or also get the latest sources using git:http://www.nongnu.org/dmidecode/
  Compile steps : make

  The home web page for dmidecode is hosted on Savannah: http://www.nongnu.org/dmidecode/
  You will find the latest version (including CVS) there, as well as fresh news
  and other interesting material, such as a list of related projects and articles.

  There's no configure script, so simply run "make" to build dmidecode, and
  "make install" to install it. You also can use "make uninstall" to remove
  all the files you installed.

  Run "make" on ubuntu, compilation defaults to link dynamic libraries,
  so binary size is very small and can't run well on board.
  We can modify makefile to 'LDFLAGS = -static' support static compilation.


mke2fs:
  can always be downloaded or also get the latest sources using git: http://e2fsprogs.sourceforge.net/
  Compile steps : ./configure / make
  You can always find information about the latest version at the the e2fsprogs web page,
  which is:http://e2fsprogs.sourceforge.net

  Run "make" on ubuntu, compilation defaults to link dynamic libraries,
  so binary size is very small and can't run well on board.
  We can modify makefile to 'LDFLAGS = -static' support static compilation.


mkfs.fat:
  Can get the latest sources using git: https://github.com/dosfstools/dosfstools
  dosfstools are built using an autoconf/automake system, so the standard method applies:
  Compile steps : ./autogen.sh / ./configure / make

  Run "make" on ubuntu, compilation defaults to link dynamic libraries,
  so binary size is very small and can't run well on board.
  We can modify makefile to 'LDFLAGS = -static' support static compilation.


sgdisk:
  Can get the latest sources using git: https://github.com/Shihta/gdisk
  Compile steps : make

  If you have following make error, you can fix this error by 'sudo apt-get install libncursesw5-dev' .
       gptcurses.cc:25:10: fatal error: ncursesw/ncurses.h: No such file or directory
       #include <ncursesw/ncurses.h>
       ^~~~~~~~~~~~~~~~~~~~
       compilation terminated.
       <builtin>: recipe for target 'gptcurses.o' failed
       make: *** [gptcurses.o] Error 1

  Run "make" on ubuntu, compilation defaults to link dynamic libraries,
  so binary size is very small and can't run well on board.
  We can modify makefile to 'LDFLAGS = -static' support static compilation.

