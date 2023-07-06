Building Zclassic
================

# Ubuntu 22.04:

sudo apt-get install build-essential libtool autotools-dev automake pkg-config bsdmainutils python3 libssl-dev

sudo apt-get install libevent-dev libboost-system-dev libboost-filesystem-dev libboost-test-dev libboost-thread-dev libfmt-dev


BDB_PREFIX=$(pwd)/bdb4.8/db-4.8.30.NC/build_unix/build/
./autogen.sh
./configure LDFLAGS="-L${BDB_PREFIX}/lib/" CPPFLAGS="-I${BDB_PREFIX}/include/" --enable-upnp-default
make


See doc/build-*.md for instructions on building the various
elements of the Zclassic Core reference implementation of Zclassic.
