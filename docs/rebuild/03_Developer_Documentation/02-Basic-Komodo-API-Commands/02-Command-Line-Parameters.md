https://en.bitcoin.it/wiki/Running_Bitcoin

-----
Coin Daemon Maintenance and Command-Line Arguments
==================================================

===add in a section about how to find your rpcuser, rpcpassword, and rpcport===

=== we need to add this section above in the index? Or perhaps this stuff should be condensed into the Control section? Maybe the index commands should be condensed into the generate section, too? ===

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

=== Put this section elsewhere: To launch the coin daemon in mining mode is set with the command line argument ``-gen`` (or ``komodo.conf`` setting gen)===

-bantime
-mempooltxinputlimit

addressindex
------------
``addressindex`` is a coin-daemon parameter that instructs a KMD-based coin daemon to maintain an index of all addresses and balances. It is initiated at run time and it is used to query address balances across the entire chain.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions===.

The ===link=== ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

``addressindex`` is enabled by default on any asset chain that utilizes the CryptoConditions smart-contract protocol.

Usage:

To initiate the ``addressindex`` command at runtime, include ``-addressindex=1`` as a parameter.

::

  ``komodod -addressindex=1``

To set the ``addressindex`` feature as a default parameter, include the parameter as a separate line in the coin's ``.conf`` configuration file.

::

  ``addressindex=1``

txindex
-------
``txindex`` is a parameter that instructs a KMD-based coin daemon to track every transaction made on the relevant blockchain.

``txindex`` is enabled by default on all KMD-based coin daemons, and is utilized in delayed Proof of Work (dPoW), JUMBLR, and the CryptoConditions (CC) smart-contract protocol. Disabling the feature will cause a normal KMD-based coin daemon to malfunction.


reindex
-------

`reindex` is a runtime daemon parameter that instructs the daemon to reindex the currently synced blockchain data.

* Note: Depending on the size and state of the chain you are reindexing, this parameter may prolong the daemon launch time.

Usage:

::

  `komodod -reindex`

timestampindex
--------------
``timestampindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to maintain a timestamp index for all blockhashes. It is initiated at run time and it is used to query blocks by a range of timestamps.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions===.

The ``-reindex`` parameter is NOT a viable alternative method for resyncing the blockchain in this circumstance.

Usage:

To initiate the ``timestampindex`` command at runtime, include ``-timestampindex=1`` as a parameter.

::

  ``./komodod -timestampindex=1``

To set the ``timestampindex`` feature as a default parameter, include the parameter in the ``komodo.conf`` configuration file.

::

  ``timestampindex=1``

spentindex
----------
``spentindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to maintain a full index of all spent transactions (txids). The parameter is called at runtime and it is used to search across the entire chain history.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions===.

The ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

``spentindex`` is enabled by default on any asset chain that utilizes the ``cc`` smart contract protocol.

Usage:

To initiate the ``spentindex`` command at runtime, include ``-spentindex=1`` as a parameter.

::
  ``./komodod -spentindex=1``

To set the ``spentindex`` feature as a default parameter, include the parameter in the ``komodo.conf`` configuration file.

::
  ``spentindex=1``

regtest
-------

The `regtest` parameter insturcts the coin daemon to run a regression test network.

Usage:

To run the `regtest` network once, use the `-regtest` argument at runtime.

::

  ./komodod -regtest

To set `regtest` as the default daemon state, place `regtest=0` as a new line in the `YOURCOIN.conf` file.

::

  regtest=0

proxy

`proxy` is a runtime daemon parameter that allows the user to connect via a `SOCKS5` proxy.

Usage:

For one-time usage, include `-proxy` as a runtime argument.

::

  komodod -proxy=127.0.0.1:9050

To include this proxy by default, include this parameter as a separate line in the ``COIN.conf`` file.

::

  proxy=127.0.0.1:9050

bind
----

``bind`` is a runtime parameter that instructs the coin daemon to bind to a given address and always listen on it.

Use ``[host]:port`` notation for IPv6.

Usage:

For one-time usage, include `-bind=<address>` at runtime.

::

  komodod -bind=<address>

To set as a default parameter, include `bind=<address>` in your `COIN.conf` file.

::

  bind=<address>


whitebind
---------

``whitelist`` is a runtime parameter that binds the daemon to a given address and whitelists peers connecting to it.

Use [host]:port notation for IPv6

Usage:

For single-time usage, include ``-whitebind=<addr>`` at runtime.

::

  komodod -whitebind=<addr>

To set as a default, include ``whitebind=<addr>`` as a separate line in the relevant ``COIN.conf`` file.

::

  whitebind=<addr>

addnode
-------

``addnode`` is a runtime parameter that tells the daemon which nodes are trusted to act as seed nodes. After connecting to a node via ``addnode``, the trusted node will send your node the list of all nodes that it is connected to, and your node will then connect to these additional nodes.

This contrasts the ===link=== ``connect`` runtime parameter, as the latter does not attempt to connect your node to additional nodes.

If you are behind a firewall or are having issues connecting to the network, ``addnode`` is a stronger option.

On the other hand, if you want to connect only to designated and trusted nodes, ``connect`` is a stronger option.

If you run multiple nodes that are connected via LAN, it is not necessary for each node to open multiple connections. Instead, use ``connect`` to connect all to one primary node, and then use ``addnode`` on the primary node to connect to the network.

Thanks goes to [Noodle] on Freenode.

Usage:

For each desired seed node, Include ``addnode=<address>`` as a separate line in the ``COIN.conf``.

::

  addnode=69.164.218.197

connect
-------

``connect`` is a runtime parameter to connect to a trusted peer node, but not to request or add any additional nodes the trusted node may provide.

Please refer to the ``addnode`` parameter entry for more information.

Usage:

Include ``connect=<address>`` as a separate line in the relevant ``COIN.conf`` file.

::

  connect=69.164.218.197

listen
-------

Listening mode, enabled by default except when 'connect' is being used
  #listen=1

  # Maximum number of inbound+outbound connections.
  #maxconnections=

  #
  # JSON-RPC options (for controlling a running Komodo/komodod process)
  #

  # server=1 tells komodod to accept JSON-RPC commands (set as default if not specified)
  #server=1

  # Bind to given address to listen for JSON-RPC connections. Use [host]:port notation for IPv6.
  # This option can be specified multiple times (default: bind to all interfaces)
  #rpcbind=<addr>

  # You must set rpcuser and rpcpassword to secure the JSON-RPC api
  #rpcuser=Ulysses
  #rpcpassword=YourSuperGreatPasswordNumber_DO_NOT_USE_THIS_OR_YOU_WILL_GET_ROBBED_385593

  # How many seconds komodo will wait for a complete RPC HTTP request.
  # after the HTTP connection is established.
  #rpcclienttimeout=30

  # By default, only RPC connections from localhost are allowed.
  # Specify as many rpcallowip= settings as you like to allow connections from other hosts,
  # either as a single IPv4/IPv6 or with a subnet specification.

  # NOTE: opening up the RPC port to hosts outside your local trusted network is NOT RECOMMENDED,
  # because the rpcpassword is transmitted over the network unencrypted and also because anyone
  # that can authenticate on the RPC port can steal your keys + take over the account running komodod
  # For more information see https://github.com/zcash/zcash/issues/1497

  #rpcallowip=10.1.1.34/255.255.255.0
  #rpcallowip=1.2.3.4/24
  #rpcallowip=2001:db8:85a3:0:0:8a2e:370:7334/96

  # Listen for RPC connections on this TCP port:
  #rpcport=8232

  # You can use Komodo or komodod to send commands to Komodo/komodod
  # running on another host using this option:
  #rpcconnect=127.0.0.1

  # Transaction Fee

  # Send transactions as zero-fee transactions if possible (default: 0)
  #sendfreetransactions=0

  # Create transactions that have enough fees (or priority) so they are likely to # begin confirmation within n blocks (default: 1).
  # This setting is overridden by the -paytxfee option.
  #txconfirmtarget=n

  # Miscellaneous options

  # Enable attempt to mine komodo.
  #gen=0

  # Set the number of threads to be used for mining komodo (-1 = all cores).
  #genproclimit=1

  # Specify a different Equihash solver (e.g. "tromp") to try to mine komodo
  # faster when gen=1.
  #equihashsolver=default

  # Pre-generate this many public/private key pairs, so wallet backups will be valid for
  # both prior transactions and several dozen future transactions.
  #keypool=100

  # Pay an optional transaction fee every time you send komodo.  Transactions with fees
  # are more likely than free transactions to be included in generated blocks, so may
  # be validated sooner. This setting does not affect private transactions created with
  # 'z_sendmany'.
  #paytxfee=0.00

  #Rewind the chain to specific block height. This is useful for creating snapshots at a given block height.
  #rewind=777777

  #Stop the chain a specific block height. This is useful for creating snapshots at a given block height.
  #stopat=1000000

  #Set an address to use as change address for all transactions. This value must be set to a 33 byte pubkey. All mined coins will also be sent to this address.
  #pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392

  #Forfeit all user rewards to miners. Set this to explicitly not claim user rewards.
  #exchange=1

  #Donate all user rewards to a a specific address. This value must be set to a 33 byte pubkey.
  #donation=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392

  # The exportdir parameter tells the coin daemon where to store your
  #exportdir=/home/myusername/mydirectory
