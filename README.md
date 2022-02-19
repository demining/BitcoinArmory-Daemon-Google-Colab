-------------------------
### Run BitcoinArmory-Daemon-Google-Colab

https://colab.research.google.com/drive/1OShIMVcFZ_khsUIBOIV1lzrqAGo1gfm_?usp=sharing

-------------------------

*No Longer Maintained! as of 2013-15-01*

Please consult the BitcoinArmory project for the new daemon.

This repository is kept as a reference for the purposes of the original author.

---------

BitcoinArmory-Daemon provides a <b>JSON-RPC interface</b> to Armory which is suitable for use on webservers and other instances where a GUI is not desired.

Installation
============

* Install dependencies, including armory dependencies (see below).
* Download and extract the files.
* Copy your watch-only wallet to the same directory as you extracted the source.

How To Use
=======

Ensure bitcoind is running.

Start the bitcoind-daemon json-rpc server

`$ python armory-daemon.py`

Run this command from the directory the source was extracted to.

Now any client can access through jsonrpc. See [https://en.bitcoin.it/wiki/API_reference_(JSON-RPC)]
for examples of how to run a json-rpc client.

The default port for the rpc server is 7070, and can be changed in armory-daemon.py

Available Methods
-----------------
`getbalance()`

Returns a decimal value in BTC for the total remaining balance in the wallet.


`getnewaddress()`

Returns the next address in the wallet as a string.


`getreceivedbyaddress(address)`

Returns a decimal value in BTC for the amount received by the address.


`sendtoaddress(address, amount)`

`amount` is a decimal value in BTC. Returns an unsigned transaction as a string. Implementation of signing and broadcasting is left to the client.

Dependencies
------------

The [usual armory dependencies] still apply, in addition to

<b>txjson-rpc<b>

`$ sudo pip install txJSON-RPC`

More info at [https://launchpad.net/txjsonrpc](https://launchpad.net/txjsonrpc)

[https://en.bitcoin.it/wiki/API_reference_(JSON-RPC)]: https://en.bitcoin.it/wiki/API_reference_(JSON-RPC)
[usual armory dependencies]: https://bitcointalk.org/index.php?topic=92496.msg1027061#msg1027061
