StartLife Core (fork of PIVX) integration/staging repository
======================================



Quick installation of the StartLife daemon under linux. See detailed instructions there [build-unix.md](build-unix.md)

Installation of libraries (using root user):

    add-apt-repository ppa:bitcoin/bitcoin -y
    apt-get update
    apt-get install -y build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils
    apt-get install -y libboost-system-dev libboost-filesystem-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev
    apt-get install -y libdb4.8-dev libdb4.8++-dev

Cloning the repository and compiling (use any user with the sudo group):

    cd
    git clone https://github.com/startlifecoin/startlife.git
    cd startlife
    ./autogen.sh
    ./configure
    sudo make install
    cd src
    sudo strip startlifed
    sudo strip startlife-cli
    sudo strip startlife-tx
    cd ..

Running the daemon:

    startlifed 

Stopping the daemon:

    startlife-cli stop

Demon status:

    startlife-cli getinfo
    startlife-cli mnsync status

All binaries for different operating systems, you can download in the releases repository:

https://github.com/startlifecoin/startlife/releases

P2P port: 27018, RPC port: 27019 
-
Distributed under the MIT software license, see the accompanying file COPYING or http://www.opensource.org/licenses/mit-license.php.
