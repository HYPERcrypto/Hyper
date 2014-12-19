Copyright (c) 2014 Hyper Developers <br />
Copyright (c) 2009-2012 Bitcoin Developers

Distributed under the MIT/X11 software license, see the accompanying file
license.txt or http://www.opensource.org/licenses/mit-license.php.  This
product includes software developed by the OpenSSL Project for use in the
OpenSSL Toolkit (http://www.openssl.org/).  This product includes cryptographic
software written by Eric Young (eay@cryptsoft.com) and UPnP software written by
Thomas Bernard.

See readme-qt.rst for instructions on building Bitcoin QT, the
graphical user interface.

OSX BUILD NOTES
===================

All of the commands should be executed in Terminal.app. It's in
/Applications/Utilities.

You need to install XCode with all the options checked so that the compiler and
everything is available in /usr not just /Developer I think it comes on the DVD
but you can get the current version from http://developer.apple.com.

1.  Clone the github tree to get the source code:

        git clone git@github.com:bitcoin/bitcoin.git bitcoin

2.  Download and install MacPorts from http://www.macports.org/. For 10.7 Lion:

        Edit /opt/local/etc/macports/macports.conf and uncomment "build_arch i386"

3.  Install dependencies from MacPorts

        sudo port install boost db48 openssl miniupnpc

Optionally install qrencode (and set USE_QRCODE=1):

        sudo port install qrencode

4.  Now you should be able to build bitcoind:

        cd bitcoin/src
        make -f makefile.osx

Run:

        ./bitcoind --help  # for a list of command-line options.

Run:

        ./bitcoind -daemon # to start the bitcoin daemon.

Run:

        ./bitcoind help # When the daemon is running, to get a list of RPC commands
