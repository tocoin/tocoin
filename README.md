Tocoin integration/staging tree
================================

http://www.tocoin.org

Copyright (c) 2009-2013 Bitcoin Developers.
Copyright (c) 2011-2013 Litecoin Developers.
Copyright (c) 2013-2014 Tocoin Developers.

What is Tocoin?
----------------

Tocoin is a lite version of Bitcoin using scrypt as a proof-of-work algorithm.

It is based on the Litecoin codebase (starting with v0.8.6.1) and uses the same principles on it's own unique blockchain.

 - 2.5 minute block targets
 - subsidy halves in 840k blocks (~4 years)
 - ~84 million total coins

The rest is the same as Bitcoin.
 - 50 coins per block
 - 2016 blocks to retarget difficulty

[Note that Tocoin uses it's own blockchain and unique genesis block, there is
no crossover or connection with any other coin blockchain]. 

For more information, as well as an immediately useable, binary version of
the Tocoin client sofware (once available), see http://www.tocoin.org.

The source is freely available on github: https://github.com/tocoin/tocoin
Please check there for the current development status & latest release.

License
-------

Tocoin is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Tocoin
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion (if they haven't already) on the
[mailing list](http://sourceforge.net/mailarchive/forum.php?forum_name=bitcoin-development).

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/bitcoin/bitcoin/tags) are created
regularly to indicate new official, stable release versions of Tocoin.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./tocoin-qt_test

