
I. Building the Tcl thread extension for Windows
================================================

Thread extension supports two build options:


o. MinGW builds:
----------------

The extension can be compiled under Windows using the
MinGW (http://www.mingw.org) environment. You can also
download the ready-to-go copy of the MinGW from the
same place you've downloaded this extension.

You should compile the Tcl core with MinGW first. After
that, you can compile the extension by running the
configure/make from this directory. You can also use the
CONFIG script to do this. You might want to edit the
script to match your environment and then just do:

    sh CONFIG

This should go smoothly, once you got Tcl core compiled ok.


o. Microsoft MSVC++ build:
--------------------------

You should use the makefile.vc file for the MSVC++ located
in the vc/ directory. Please consult the README.vc.txt and
makefile.vc files for more details.
Alternatively, you can use the MSVC++ IDE and open the 
thread_win.dsw workspace file.


II. Building optional support libraries
=======================================

As of 2.6 release, this extension supports persistent shared 
variables. To use this functionality, you might need to download 
and compile some other supporting libraries. Currently, there is 
a simple implementation of shared variable persistency built atop
of popular GNU Gdbm package. You can obtain the latest version of
the Gdbm from: http://www.gnu.org/software/gdbm/gdbm.html.

For the impatient, there are Windows ports of GNU Gdbm found on
various places on the Internet. The easiest way to start is to go 
to the GnuWin32 project: http://sourceforge.net/projects/gnuwin32
and fetch yourself a compiled GNU Gdbm DLL. 

-EOF-
