Coin Daemon Maintenance, Command-Line Arguments, Default Settings
=================================================================

Initiating and Accessing the Coin Daemon
----------------------------------------

When running a Komodo-compatible blockchain from the command line, the user interacts through two separate methods. The first is the coin daemon itself, ``komodod``. This software is initiated by calling it from the command line and including any runtime parameters. When running a Komodo-compatible blockchain other than the main KMD blockchain, the user should include the ``-ac_name=COINNAME`` and ``-ac_supply=COINSUPPLY`` parameters.

::

  To launch the KMD main net:

  komodod

  To launch a KMD-compatible chain with a coin supply of 1000000:

  komodod -ac_name=COINNAME -ac_supply=1000000


* Other parameters may also be included as necessary. See below for a list of runtime parameters.

The second software for Komodo-compatible interaction is ``komodo-cli``. This software allows the user to send RPC and other API commands to the coin daemon when it is running. This software is accessed by calling ``komodo-cli`` at the command line and including the desired commands, as well as the designated ``-ac_name`` and ``-ac_supply`` indicators for KMD-compatible chains.

* Note: see also ===link=== Accessing the Coin Daemon Remotely

::

  To call ``getbalance`` from the KMD coin daemon:

  komodo-cli getbalance

  To call ``getbalance`` from a KMD-compatible coin daemon for a coin with a supply of 1000000:

  komodo-cli -ac_name=COINNAME -ac_supply=100000 getbalance

Accessing the Coin Daemon Remotely
----------------------------------

To access a coin daemon remotely -- for example, via a ``curl`` command in the shell -- the user will need to obtain the ``rpcuser``, ``rpcpassword``, and ``rpcport`` from the ``.conf`` file of the relevant coin daemon.

Assuming the default installation location, the ``.conf`` file can be found by exploring the following directories:

::
	MacOS: ``~/Library/Application Support/Komodo``
	Windows: ``C:\Users\myusername\AppData\Roaming\Komodo\``
	GNU/Linux: ``~/.komodo``

Within that directory there are also subfolders containing all KMD-compatible coin daemon ``.conf`` files.

Manually deleting blockchain data
---------------------------------
Sometimes it is necessary to manually delete all blockchain data. This should automatically trigger a full resync of the blockchain.

Users should exercise caution not to delete the ``wallet.dat`` file during this procedure. We recommend that the user make frequent backups of the ``wallet.dat`` file, especially before deleting files from the application directory.

To erase all synced blockchain data, the following files should be deleted from the `.komodo` folder:

::
  ``blocks``
  ``chainstate``
  ``notarisations``
  ``komodostate``
  ``komodostate.ind``

Default file locations:
::
	MacOS: ``~/Library/Application Support/Komodo``
	Windows: ``C:\Users\myusername\AppData\Roaming\Komodo\``
	GNU/Linux: ``~/.komodo``

Common Runtime Parameters and the .conf Settings
------------------------------------------------

The following is an abbreviated list of runtime parameters and settings that can be initiated in a coin daemon's ===link=== ``.conf`` file.

These commands largely derive from the upstream BTC software. (Komodo is a fork of Zcash, which is a privacy-centric fork of BTC.)

To see additional runtime parameters not included here, please visit the relevant Bitcoin wiki page:

===link=== https://en.bitcoin.it/wiki/Running_Bitcoin

addressindex
------------
``addressindex`` is a coin-daemon parameter that instructs a KMD-based coin daemon to maintain an index of all addresses and balances. It is initiated at run time and it is used to query address balances across the entire chain.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions===.

The ===link=== ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

``addressindex`` is enabled by default on any asset chain that utilizes the CryptoConditions (CC) smart-contract protocol.

Usage:

As a runtime parameter:

::

  ``komodod -addressindex=1``

As a default value in the coin's ``.conf`` file:

::

  ``addressindex=1``

txindex
-------
``txindex`` is a parameter that instructs a KMD-based coin daemon to track every transaction made on the relevant blockchain.

``txindex`` is enabled by default on all KMD-based coin daemons, and is utilized in delayed Proof of Work (dPoW), JUMBLR, and the CryptoConditions (CC) smart-contract protocol. Disabling the feature will cause a normal KMD-based coin daemon to malfunction.

reindex
-------

`reindex` is a runtime parameter that instructs the daemon to re-index the currently synced blockchain data.

* Note: Depending on the size and state of the chain you are re-indexing, this parameter may prolong the daemon launch time.

Usage:

::

As a runtime parameter:

  `komodod -reindex`

timestampindex
--------------
``timestampindex`` is a runtime parameter that instructs a KMD-based coin daemon to maintain a timestamp index for all blockhashes. It is initiated at run time and it is used to query blocks by a range of timestamps.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions===.

The ``-reindex`` parameter is NOT a viable alternative method for re-syncing the blockchain in this circumstance.

Usage:

As a runtime parameter:

::

  ``./komodod -timestampindex=1``

As a default value in the coin's ``.conf`` file:

::

  ``timestampindex=1``

spentindex
----------
``spentindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to maintain a full index of all spent transactions (txids). The parameter is called at runtime and it is used to search across the entire chain history.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions===.

The ``-reindex`` parameter is not a viable alternative method for re-syncing the blockchain in this circumstance.

``spentindex`` is enabled by default on any asset chain that utilizes the ``cc`` smart contract protocol.

Usage:

As a runtime parameter:

::
  ``./komodod -spentindex=1``

As a default value in the coin's ``.conf`` file:

::
  ``spentindex=1``

regtest
-------

The `regtest` parameter instructs the coin daemon to run a regression test network (a useful tool for rapid trial and testing).

Usage:

As a runtime parameter:

::

  ./komodod -regtest

As a default value in the coin's ``.conf`` file:

::

  regtest=0

bantime
-------

``bantime`` is a runtime parameter that sets the default number of seconds for a ban initiated during the daemon's session. The default is 86400.

Usage:

As a runtime parameter:

::

  -bantime=100000

As a default value in the coin's ``.conf`` file:

::

  bantime=100000

mempooltxinputlimit
-------------------
** DEPRECATED **

``mempooltxinputlimit`` is a runtime parameter inherited from Zcash. The functionality is facilitated is now enabled by default, and therefore the parameter is now deprecated. Please see the Zcash documentation for more information: https://blog.z.cash/new-release-1-1-0/.

proxy
-----

`proxy` is a runtime daemon parameter that allows the user to connect via a `SOCKS5` proxy.

Usage:

As a runtime parameter:

::

  komodod -proxy=127.0.0.1:9050

As a default value in the coin's ``.conf`` file:

::

  proxy=127.0.0.1:9050

bind
----

``bind`` is a runtime parameter that instructs the coin daemon to bind to a given address and always listen on it.

Use ``[host]:port`` notation for IPv6.

Usage:

As a runtime parameter:

::

  komodod -bind=127.0.0.1:9050

As a default value in the coin's ``.conf`` file:

::

  bind=127.0.0.1:9050

whitebind
---------

``whitelist`` is a runtime parameter that binds the daemon to a given address and whitelists peers connecting to it.

Use [host]:port notation for IPv6

Usage:

As a runtime parameter:

::

  komodod -whitebind=127.0.0.1:9050

As a default value in the coin's ``.conf`` file:

::

  whitebind=127.0.0.1:9050

addnode
-------

``addnode`` is a runtime parameter that tells the daemon which nodes are trusted to act as seed nodes. After connecting to a node via ``addnode``, the trusted node will send your node the list of all nodes that it is connected to, and your node will then connect to these additional nodes until the ===link=== max limit is reached.

This contrasts from the ===link=== ``connect`` runtime parameter, as the latter does not attempt to connect your node to additional nodes.

If you are behind a firewall or are having issues connecting to the network, ``addnode`` is a stronger option.

On the other hand, if you want to connect only to designated and trusted nodes, ``connect`` is a stronger option.

If you run multiple nodes that are connected via a LAN, it is not necessary for each node to open multiple connections. Instead, use ``connect`` to connect all to one primary node, and then use ``addnode`` on the primary node to connect to the network.

Usage:

As a default value in the coin's ``.conf`` file:

::

  addnode=69.164.218.197

connect
-------

``connect`` is a runtime parameter to connect to a trusted peer node, but not to request or add any additional nodes.

Please refer to the ===link=== ``addnode`` parameter entry for more information.

Usage:

As a default value in the coin's ``.conf`` file:

::

  connect=69.164.218.197

gen
---

``gen`` is a runtime parameter that instructs the daemon to attempt to generate new blocks, and thereby mine new coins.

* Note: see also ===link=== ``setgenerate``

Usage:

As a runtime parameter:

::

  komodod -gen=0

As a default value in the coin's ``.conf`` file:

::

  gen=0

listen
-------

``listen`` instructs the daemon to listen for RPC calls on the network. It is enabled by default, except when ===link=== ``connect`` is used.

Usage:

::

As a runtime parameter:

  -listen=1

As a default value in the coin's ``.conf`` file:

  listen=1

maxconnections
--------------

``maxconnections`` indicates the maximum number of inbound and outbound connections.

Usage:

As a runtime parameter:

::

  -maxconnections=NUMBER

As a default value in the coin's ``.conf`` file:

::

  maxconnections=NUMBER

server
------

``server`` is a runtime parameter that instructions the daemon to accept json-rpc commands. It is enabled by default.

Usage:

As a runtime parameter:

::

  -server=1

As a default value in the coin's ``.conf`` file:

::

  server=1

rpcbind
-------

``rpcbind`` is a runtime parameter that instructs the daemon to listen for json-rpc connections.

Use [host]:port notation for IPv6.

This option can be specified multiple times (default: bind to all interfaces).

Usage:

As a runtime parameter:

::

  komodod -rpcbind=127.0.0.1:9704

As a default value in the coin's ``.conf`` file:

  rpcbind=127.0.0.1:9704

rpcclienttimeout
----------------

``rpcclienttimeout`` is a runtime parameter that indicates to the daemon the number of seconds to wait for a rpc command to complete before killing the process.

Usage:

As a runtime parameter:

::

  komodod -rpcclienttimeout=SECONDS

As a default value in the coin's ``.conf`` file:

::

  rpcclientttimeout=SECONDS

rpcallowip
----------

By default, only RPC connections from localhost are allowed.

Specify as many ``rpcallowip=`` settings as you like to allow connections from other hosts, either as a single IPv4/IPv6 or with a subnet specification.

* Note: opening up the RPC port to hosts outside your local trusted network is NOT RECOMMENDED, because the rpcpassword is transmitted over the network unencrypted and also because anyone that can authenticate on the RPC port can steal your keys and take over the account running komodod.

For more information see https://github.com/zcash/zcash/issues/1497

Usage:

As a default value in the coin's ``.conf`` file:

::

  rpcallowip=10.1.1.34/255.255.255.0
  rpcallowip=1.2.3.4/24
  rpcallowip=2001:db8:85a3:0:0:8a2e:370:7334/96

rpcport
-------

The ``rpcport`` tells the daemon to listen for RPC connections on the indicated TCP port.

Usage:

As a default value in the coin's ``.conf`` file:

::

  rpcport=8232

rpcconnect
----------

``rpcconnect`` allows the user to connect to komodod and send RPC commands on another host using this option:

Usage:

As a default value in the coin's ``.conf`` file:

::

  rpcconnect=127.0.0.1

sendfreetransactions
--------------------

``sendfreetransactions`` instructs the daemon to send transactions as zero-fee transactions if possible. The default value is 0.

Usage:

As a default value in the coin's ``.conf`` file:

::

  sendfreetransactions=0

genproclimit
------------

``genproclimit`` sets the number of threads to be used for mining komodo (-1 = all cores).

Usage:

As a default value in the coin's ``.conf`` file:

::

  genproclimit=1

keypool
-------

``keypool`` instructs the daemon to pre-generate a certain number of public/private key pairs. This can facilitate wallet.dat backups being valid for both prior transactions and several dozen future transactions.

Usage:

As a default value in the coin's ``.conf`` file:

::

  keypool=100

rewind
------

``rewind`` rewinds the chain to specific block height. This is useful for creating snapshots at a given block height.

Usage:

As a runtime parameter:

::

  -rewind=777777

stopat
------

``stopat`` stops the chain at a specific block height. This is useful for creating snapshots at a given block height.

Usage:

As a runtime parameter:

::

  -stopat=1000000

pubkey
------

``pubkey`` sets an address to use as a change address for all transactions. This value must be set to a 33 byte pubkey. All mined coins will also be sent to this address.

Usage:

As a default value in the coin's ``.conf`` file:

::

  pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392

exchange
--------

``exchange`` forfeits all user rewards to miners. Set this to explicitly not claim user rewards.

Usage:

As a default value in the coin's ``.conf`` file:

::

  exchange=1

donation
--------

``donation`` donates all user rewards to a a specific address. This value must be set to a 33 byte pubkey.

Usage:

As a default value in the coin's ``.conf`` file:

::

  donation=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392

exportdir
---------

``exportdir`` tells the coin daemon where to store your export dirirectory.

Usage:

As a default value in the coin's ``.conf`` file:

  exportdir=/home/myusername/mydirectory
