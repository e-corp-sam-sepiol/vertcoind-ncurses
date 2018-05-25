# vertcoind-ncurses v0.3.1

Based on esotericnonsense's Python ncurses front-end for bitcoind. Uses the JSON-RPC API.
Adapted to display vertcoind data. Thank you for your incredible work esotericnonsense,
this would not be possible without you.

![ScreenShot](/img/vertcoind-ncurses.gif)

- esotericnonsense (Daniel Edgecumbe)
- Sam Sepiol - Modifications made to enable vertcoind support

Donations
---------

If you have found esotericnonsense's bitcoind-ncurses2 useful, please consider donating.

All funds go towards the operating costs of his hardware and future
Bitcoin development projects.

https://github.com/esotericnonsense/bitcoind-ncurses2

![ScreenShot](/img/3BYFucUnVNhZjUDf6tZweuZ5r9PPjPEcRv.png)

Feedback
--------

Please report any problems using the Github issue tracker. Pull requests are
also welcomed.
The author, esotericnonsense, can often be found milling around on #bitcoin
(Freenode).

**bitcoin 3BYFucUnVNhZjUDf6tZweuZ5r9PPjPEcRv**


## Dependencies

* Developed with python 3.6.2, Bitcoin Core 0.15.0.1
* Adapted to Vertcoin Core Vertcoin Core Daemon version v0.12.0.0-d2a8ef4
* PyPi packages: aiohttp and async-timeout (see requirements.txt)

## Features

* Updating monitor mode showing vertcoind's status, including:
* Current block information: hash, height, fees, timestamp, age, diff, ...
* Basic block explorer with fast seeking, no external DB required
* Basic transaction viewer with fast seeking, best with -txindex=1
* Ability to query blocks by hash, height; transactions by txid
* Wallet transaction and balance viewer
* Charting network monitor
* Peer/connection information
* Basic debug console functionality

## Installation and usage

```
git clone https://github.com/e-corp-sam-sepiol/vertcoind-ncurses.git
```

```
cd vertcoind-ncurses/
pip3 install -r requirements.txt
```
or, on Arch Linux:
```
pacman -S python-aiohttp python-async-timeout
```

```
cd vertcoind-ncurses/
python3 main.py
```

vertcoind-ncurses2 will automatically use the cookie file available in
~/.vertcoin/, or the RPC settings in ~/.vertcoin/vertcoin.conf. To use a different
datadir, specify the --datadir flag:

```
python3 main.py --datadir /some/path/to/your/datadir
```

This is an early development release and based on a complete rewrite of the original
bitcoind-ncurses. Expect the unexpected.

