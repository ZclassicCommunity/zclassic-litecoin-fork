Building Zclassic
================

BDB=$(pwd)/bdb4.8/db-4.8.30.NC/build_unix/build/
./autogen.sh
./configure LDFLAGS="-L${BDB_PREFIX}/lib/" CPPFLAGS="-I${BDB_PREFIX}/include/" --enable-upnp-default
make


See doc/build-*.md for instructions on building the various
elements of the Zclassic Core reference implementation of Zclassic.
