*************************************
Komodo Main Chain - API Documentation
*************************************

Synopsis of KMD
===============

Komodo (KMD) is the main chain in the Komodo ecosystem.

KMD is a blockchain platform that provides users with the ability to build independent blockchains. A blockchain built on KMD receives security from the Bitcoin hash rate (optional), zero-knowledge privacy from the Zcash parameters, and is powerful, scalable, and capable of interaction with other independent blockchains.

To install Komodo on your machine, please visit the article, [Guide to Install Komodo].

For a more detailed description of the Komodo ecosystem, please refer to the [Komodo Whitepaper].

API Introduction
================

The Komodo daemon, ``komodod``, comes with an Application Program Interface (API).

The API is accessed through the ``komodo-cli`` software, which is provided during Komodo installation.

To access the API commands, open a new terminal, proceed to the directory where ``komodod`` and ``komodo-cli`` are installed, and execute:

``./komodo-cli [API COMMAND]`` (Linux)

The API can likewise be used for all KMD-based independent blockchains. Two modifications are required: the name of the independent blockchain and the total coin supply.

``./komodo-cli -ac_name=[BLOCKCHAIN NAME] -ac_supply=[BLOCKCHAIN COIN SUPPLY]``

The list of available API commands can be retrieved locally by executing:

``./komodo-cli help``

To learn more about a specific API command, execute:

``./komodo-cli help [API COMMAND]``.

List of API Commands by Category
================================

Click any of the API options below to be taken to their summary. You may also navigate by the links in the Navigation Bar. Press the ``Home`` button on your keyboard to return to the top of the page.

:ref:`Category: Addressindex <Addressindex>`
--------------------------------------------

:ref:`getaddressbalance`
:ref:`getaddressdeltas`
:ref:`getaddressmempool`
:ref:`getaddresstxids`
:ref:`getaddressutxos`

:ref:`Category: Blockchain <Blockchain>`
----------------------------------------

:ref:`MoMoMdata symbol kmdheight notarized_height`
:ref:`allMoMs kmdstarti kmdendi`
:ref:`calc_MoM height MoMdepth`
:ref:`getbestblockhash`
:ref:`getblock "hash|height" ( verbose )`
:ref:`getblockchaininfo`
:ref:`getblockcount`

:ref:`getblockhash index`
:ref:`getblockhashes timestamp`
:ref:`getblockheader "hash" ( verbose )`
:ref:`getchaintips`
:ref:`getdifficulty`
:ref:`getmempoolinfo`
:ref:`getrawmempool ( verbose )`
:ref:`getspentinfo`
:ref:`gettxout "txid" n ( includemempool )`
:ref:`gettxoutproof ["txid",...] ( blockhash )`
:ref:`gettxoutsetinfo`
:ref:`height_MoM height`
:ref:`kvsearch key`
:ref:`kvupdate key value flags/passphrase`
:ref:`minerids needs height`
:ref:`notaries height timestamp`
:ref:`paxpending needs no args`
:ref:`paxprice "base" "rel" height`
:ref:`paxprices "base" "rel" maxsamples`
:ref:`txMoMproof needs a txid`
:ref:`verifychain ( checklevel numblocks )`
:ref:`verifytxoutproof "proof"`

:ref:`Category: Control <Control>`
----------------------------------

:ref:`getinfo`
:ref:`help ( "command" )`
:ref:`stop <komodo-api-stop>`

:ref:`Category: Disclosure <Disclosure>`
----------------------------------------

:ref:`z_getpaymentdisclosure "txid" "js_index" "output_index" ("message")`
:ref:`z_validatepaymentdisclosure "paymentdisclosure"`

:ref:`Category: Generating <Generating>`
----------------------------------------

:ref:`generate numblocks`
:ref:`getgenerate`
:ref:`setgenerate generate ( genproclimit )`

:ref:`Category: Mining <Mining>`
--------------------------------

:ref:`getblocksubsidy height`
:ref:`getblocktemplate ( "jsonrequestobject" )`
:ref:`getlocalsolps`
:ref:`getmininginfo`
:ref:`getnetworkhashps ( blocks height )`
:ref:`getnetworksolps ( blocks height )`
:ref:`prioritisetransaction \<txid\> \<priority delta\> \<fee delta\>`
:ref:`submitblock "hexdata" ( "jsonparametersobject" )`

:ref:`Category: Network <Network>`
----------------------------------

:ref:`addnode "node" "add|remove|onetry"`
:ref:`clearbanned`
:ref:`disconnectnode "node"`
:ref:`getaddednodeinfo dns ( "node" )`
:ref:`getconnectioncount`
:ref:`getdeprecationinfo`
:ref:`getnettotals`
:ref:`getnetworkinfo`
:ref:`getpeerinfo`
:ref:`listbanned`
:ref:`ping`
:ref:`setban "ip(/netmask)" "add|remove" (bantime) (absolute)`

:ref:`Category: Rawtransactions <Rawtransactions>`
--------------------------------------------------

:ref:`createrawtransaction [{"txid":"id","vout":n},...] {"address":amount,...}`
:ref:`decoderawtransaction "hexstring"`
:ref:`decodescript "hex"`
:ref:`fundrawtransaction "hexstring"`
:ref:`getrawtransaction "txid" ( verbose )`
:ref:`sendrawtransaction "hexstring" ( allowhighfees )`
:ref:`signrawtransaction "hexstring" ( [{"txid":"id","vout":n,"scriptPubKey":"hex","redeemScript":"hex"},...] ["privatekey1",...] sighashtype )`

:ref:`Category: Util <Util>`
----------------------------

:ref:`createmultisig nrequired ["key",...]`
:ref:`estimatefee nblocks`
:ref:`estimatepriority nblocks`
:ref:`invalidateblock "hash"`
:ref:`jumblr_deposit "depositaddress"`
:ref:`jumblr_pause`
:ref:`jumblr_resume`
:ref:`jumblr_secret "secretaddress"`
:ref:`reconsiderblock "hash"`
:ref:`validateaddress "komodoaddress"`
:ref:`verifymessage "komodoaddress" "signature" "message"`
:ref:`z_validateaddress "zaddr"`

:ref:`Category: Wallet <Wallet>`
--------------------------------

:ref:`addmultisigaddress nrequired ["key",...] ( "account" )`
:ref:`backupwallet "destination"`
:ref:`dumpprivkey "komodoaddress"`
:ref:`dumpwallet "filename"`
:ref:`encryptwallet "passphrase"`
:ref:`getaccount "KMD_address"`
:ref:`getaccountaddress "account"`
:ref:`getaddressesbyaccount "account"`
:ref:`getbalance ( "account" minconf includeWatchonly )`
:ref:`getnewaddress ( "account" )`
:ref:`getrawchangeaddress`
:ref:`getreceivedbyaccount "account" ( minconf )`
:ref:`getreceivedbyaddress "KMD_address" ( minconf )`
:ref:`gettransaction "txid" ( includeWatchonly )`
:ref:`getunconfirmedbalance`
:ref:`getwalletinfo`
:ref:`importaddress "address" ( "label" rescan )`
:ref:`importprivkey "komodoprivkey" ( "label" rescan )`
:ref:`importwallet "filename"`
:ref:`keypoolrefill ( newsize )`
:ref:`listaccounts ( minconf includeWatchonly)`
:ref:`listaddressgroupings`
:ref:`listlockunspent`
:ref:`listreceivedbyaccount ( minconf includeempty includeWatchonly)`
:ref:`listreceivedbyaddress ( minconf includeempty includeWatchonly)`
:ref:`listsinceblock ( "blockhash" target-confirmations includeWatchonly)`
:ref:`listtransactions ( "account" count from includeWatchonly)`
:ref:`listunspent ( minconf maxconf  ["address",...] )`
:ref:`lockunspent unlock [{"txid":"txid","vout":n},...]`
:ref:`move "fromaccount" "toaccount" amount ( minconf "comment" )`
:ref:`resendwallettransactions`
:ref:`sendfrom "fromaccount" "toKMDaddress" amount ( minconf "comment" "comment-to" )`
:ref:`sendmany "fromaccount" {"address":amount,...} ( minconf "comment" ["address",...] )`
:ref:`sendtoaddress "KMD_address" amount ( "comment" "comment-to" subtractfeefromamount )`
:ref:`setaccount "KMD_address" "account"`
:ref:`settxfee amount`
:ref:`signmessage "KMD address" "message"`
:ref:`z_exportkey "zaddr"`
:ref:`z_exportviewingkey "zaddr"`
:ref:`z_exportwallet "filename"`
:ref:`z_getbalance "address" ( minconf )`
:ref:`z_getnewaddress`
:ref:`z_getoperationresult (["operationid", ...])`
:ref:`z_getoperationstatus (["operationid", ...])`
:ref:`z_gettotalbalance ( minconf includeWatchonly )`
:ref:`z_importkey "zkey" ( rescan startHeight )`
:ref:`z_importviewingkey "vkey" ( rescan startHeight )`
:ref:`z_importwallet "filename"`
:ref:`z_listaddresses ( includeWatchonly )`
:ref:`z_listoperationids`
:ref:`z_listreceivedbyaddress "address" ( minconf )`
:ref:`z_mergetoaddress ["fromaddress", ...] "toaddress" ( fee ) ( transparent_limit ) ( shielded_limit ) ( memo )`
:ref:`z_sendmany "fromaddress" [{"address":...,"amount":...},...] ( minconf ) ( fee )`
:ref:`z_shieldcoinbase "fromaddress" "tozaddress" ( fee ) ( limit )`
:ref:`zcbenchmark benchmarktype samplecount`
:ref:`zcrawjoinsplit rawtx inputs outputs vpub_old vpub_new`
:ref:`zcrawkeygen`
:ref:`zcrawreceive zcsecretkey encryptednote`
:ref:`zcsamplejoinsplit`

=== Do we need to set it up so that you can link directly to a spot in the doc? Or is that there already? If there is a mechanism, can we make it more obvious in the docs by adding a link next to the name?===

Coin Daemon Maintenance and Parameters
======================================

=== we need to add this section above in the index ===

Manually deleting blockchain data
---------------------------------
Sometimes it is necessary to manually delete all blockchain data. This should automatically trigger a full resync of the blockchain.

Users should exercise caution not to delete the ``wallet.dat`` file during this procedure. We recommend that the user make frequent backups of the ``wallet.dat`` file, especially before deleting files from the application directory.

To erase all synced blockchain data, following files should be deleted:

::
  ``blocks``
  ``chainstate``
  ``notarisations``
  ``komodostate``
  ``komodostate.ind``

Default file locations:
::
	MacOS: ``~/Library/Application Support/Komodo``
	Windows: ===need this==
	GNU/Linux: ``~/.komodo``

-addressindex
-------------
``addressindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to make a full index of all addresses and balances. It is initiated at run time, and it enables rapid search across the entire blockchain history.

When utilizing this command the synced blockchain data should be deleted to allow for a full resync. The user may need to manually delete the blockchain data beforehand ===link to manual deletion instructions above===.

The ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

Usage:

To initiate the ``addressindex`` command at runtime, include ``-addressindex=1`` as a parameter.

::

  ``./komodod -addressindex=1``

To set the ``addressindex`` feature as a default parameter, include the parameter in the ``komodo.conf`` configuration file.

::

  ``addressindex=1``

-timestampindex
---------------
``timestampindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to make a full index of all === transaction timestamps ===. It is initiated at run time and it enables rapid search across the entire blockchain history.

When utilizing this command the synced blockchain data should be deleted to allow for a full resync. The user may need to manually delete the blockchain data before executing the command ===link to manual deletion instructions above===.

The ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

Usage:

To initiate the ``timestampindex`` command at runtime, include ``-timestampindex=1`` as a parameter.

::

  ``./komodod -timestampindex=1``

To set the ``timestampindex`` feature as a default parameter, include the parameter in the ``komodo.conf`` configuration file.

::

  ``timestampindex=1``

-unspentindex
------------
``unspentindex`` is a coin daemon parameter that is initiated at run time. The command instructs a KMD-based coin daemon to make a full index of all === unspent transactions (utxos) ===. It is commonly used in web-based blockchain explorers for rapid search across the entire blockchain history.

When utilizing this command the synced blockchain data should be deleted to allow for a full resync. The user may need to manually delete the blockchain data before executing the command ===link to manual deletion instructions above===.

The ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

Usage:

To initiate the ``unspentindex`` command at runtime, include ``-unspentindex=1`` as a parameter.

::

  ``./komodod -unspentindex=1``

To set the ``unspentindex`` feature as a default parameter, include the parameter in the ``komodo.conf`` configuration file.

::

  ``unspentindex=1``

-spentindex
----------
``spentindex`` is a coin daemon parameter that is initiated at run time. The command instructs a KMD-based coin daemon to make a full index of all === spent transactions (utxos) ===. It is commonly used in web-based blockchain explorers for rapid search across the entire blockchain history.

When utilizing this command the synced blockchain data should be deleted to allow for a full resync. The user may need to manually delete the blockchain data before executing the command ===link to manual deletion instructions above===.

The ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

Usage:

To initiate the ``spentindex`` command at runtime, include ``-spentindex=1`` as a parameter.

::
  ``./komodod -spentindex=1``

To set the ``spentindex`` feature as a default parameter, include the parameter in the ``komodo.conf`` configuration file.

::
  ``spentindex=1``

AddressIndex
============
The AddressIndex API commands are used to query various aspects of the blockchain's history. Most require the ===link=== ``addressindex`` feature, as these API commands scan the entire blockchain history.

getaddressbalance
-----------------
::
	getaddressbalance '{"address": ["address_string", "address_string", ...]}'

The ``getaddressbalance`` method returns the confirmed balance for an address(es). It requires the ===link=== ``addressindex`` to be enabled.

===Insert "Run" sandbox here===
  Komodo API Demo: getaddressbalance method
  (example code)
  Run/Reset Buttons
===End sandbox===

Arguments:

===(italics?)===
getaddressbalance '{"address": ["address_string", "address_string", ...]}'

::
	{
	  "addresses"					        //
	    [
	      "address_string"        // (string)    base58check encoded address
	      , ...							      //             this method can accept multiple addresses
	    ]
	}

Response:
::

	{
	  "balance_string"  		       // (number) the current confirmed balance, listed in satoshis
	  "received_string" 		       // (number) the total confirmed number of satoshis received (including change)
	}

Examples:
===italics===(the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)
::

	command:
	# ./komodo-cli getaddressbalance '{"addresses":["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'

	response:
	{
    "balance": 40000,
    "received": 1011916229
  }

	command:
	# curl --user myrpcuser:myuserpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressbalance", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

	response:
	{"result":{"balance":40000,"received":1011916229},"error":null,"id":"curltest"}

getaddressdeltas
----------------
::
  getaddressdeltas '{"addresses": ["address_string", "address_string", ...]}'

  getaddressdeltas '{"addresses": ["address_string", "address_string", ...], "start": start_number, "end": end_number, "chainInfo": boolean}'

The ``getaddressdeltas`` method returns all confirmed balance changes of an address. The parameters allow the user to optionally limit the response to a given interval of blocks. The method requires ===link===``addressindex`` to be enabled.

===Insert "Run" sandbox here===
Komodo API Demo: getaddressdeltas method
(example code)
Run/Reset Buttons
===End sandbox===

Arguments:

::

	{
	  "addresses" 					   //            the "addresses" property name
	    [
        "address" 				   // (string)   the base58check encoded address
	      ,...							   //            this method accepts multiple addresses
	    ]
	  "start" 							   // (number)   the start block height
	  "end" 								   // (number)   the end block height
	  "chainInfo" 					   // (boolean)  include chain info in results (only applies if start and end specified)
	}

Result:

::

	[
	  {
	    "satoshis"             // (number)   the difference of satoshis
	    "txid"                 // (string)   the related transaction id
	    "index"                // (number)   the related input or output index
	    "height"               // (number)   the block height
	    "address"              // (string)   the base58check encoded address
	  }
	]

Example (no optional parameters):
===italics===(the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:
	./komodo-cli getaddressdeltas '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'

  response:
  [
    {
      "satoshis": 1011876229,
      "txid": "39c61e8ea769ba1fc971cb7dadc531f25a2528d01a4244f379043248b6c51cc1",
      "index": 0,
      "blockindex": 0,
      "height": 1,
      "address": "RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"
    }
  ]

::
  command:
  ./komodo-cli getaddressdeltas '{"addresses":["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"],"start":1,"end":200,"chainInfo":true}'


  response:
  {
    "deltas": [
      {
        "satoshis": 1011876229,
        "txid": "39c61e8ea769ba1fc971cb7dadc531f25a2528d01a4244f379043248b6c51cc1",
        "index": 0,
        "blockindex": 0,
        "height": 1,
        "address": "RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"
      }
    ],
    "start": {
      "hash": "022df4cd1b0bdf548fedc48f27c6367536a560857f61f9bec4b35179c8a45734",
      "height": 1
    },
    "end": {
      "hash": "001fd35407abd8f4e2ec9734ce6f91d820ff553efcb9c39d657afed84da84963",
      "height": 200
    }
  }

::
  command:
	curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressdeltas", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:
  {"result":[{"satoshis":1011876229,"txid":"39c61e8ea769ba1fc971cb7dadc531f25a2528d01a4244f379043248b6c51cc1","index":0,"blockindex":0,"height":1,"address":"RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"}],"error":null,"id":"curltest"}

::
  command:
  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressdeltas", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"],"start":1,"end":200,"chainInfo":true}]}' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:
  {"result":{"deltas":[{"satoshis":1011876229,"txid":"39c61e8ea769ba1fc971cb7dadc531f25a2528d01a4244f379043248b6c51cc1","index":0,"blockindex":0,"height":1,"address":"RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"}],"start":{"hash":"022df4cd1b0bdf548fedc48f27c6367536a560857f61f9bec4b35179c8a45734","height":1},"end":{"hash":"001fd35407abd8f4e2ec9734ce6f91d820ff553efcb9c39d657afed84da84963","height":200}},"error":null,"id":"curltest"}

getaddressmempool
-----------------
::
  getaddressmempool '{"addresses": ["address_string"]}'

The ``getaddressmempool`` method returns all mempool deltas for an address. It requires ===link===``addressindex`` to be enabled.

===Insert "Run" sandbox here===
Komodo API Demo: getaddressmempool method
(example code)
Run/Reset Buttons
===End sandbox===

Arguments:

::

	{
	  "addresses":
	    [
	      "address":               // (string)     the base58check encoded address
	      ,...
	    ]
	}

Result:

::

	[
	  {
	    "address":                 // (string)     the base58check encoded address
	    "txid":                    // (string)     the related txid
	    "index":                   // (number)     the related input or output index
	    "satoshis":                // (number)     the difference of satoshis
	    "timestamp":               // (number)     the time the transaction entered the mempool (seconds)
	    "prevtxid":                // (string)     the previous txid (if spending)
	    "prevout":                 // (string)     the previous transaction output index (if spending)
	  }
	]

Examples:

::

  command:
	# komodo-cli getaddressmempool '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'

  response:
  [
    {
      "address": "RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb",
      "txid": "55c9830c0b2efcbbbac4fb813ff0d85722c6d720a748459287b60ef96cdb6732",
      "index": 1,
      "satoshis": 200000000,
      "timestamp": 1536356143
    }
  ]


  command:
  # curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressmempool", "params": [{"addresses": ["komodo-cli getaddressmempool '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:


getaddresstxids
---------------
::
  getaddresstxids '{"addresses": ["address_string"]}'

The ``getaddresstxids`` method returns the txids for an address(es). It requires ===link=== ``addressindex`` to be enabled.

===Insert "Run" sandbox here===
  Komodo API Demo: getaddressmempool method
  (example code)
  Run/Reset Buttons
===End sandbox===

Arguments:

::
	{
	  "addresses"
	    [
	      "address"                   // (string)   the base58check encoded address
	      ,...                        //            method accepts multiple addresses
	    ],
	  "start"                         // (number)   the start block height
	  "end"                           // (number)   the end block height
	}

Result:

::

	[
    "transactionid"                // (string)   the transaction id
	  ,...                           //            returns multiple transaction ids
	]

Examples:

::

  command:
	# komodo-cli getaddresstxids '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb","RQUAkqRiRMqxcNrB29B4duTK4qkqfV9HVJ"]}'

  response:
  [
    "39c61e8ea769ba1fc971cb7dadc531f25a2528d01a4244f379043248b6c51cc1",
    "800e4331018d02458ff4f2a7722f0508b810f7fcf53bc1c5ac85aec4e5fa706b",
    "2a3c3664851370ff762b47d735cc661e3dbce4cf36b6c1b74799f3b1c847bd52",
    "275f8383d85c0873c91ebfea3917d4136c89f43526da053177922d6c036634af"
  ]

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddresstxids", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

getaddressutxos
---------------

Returns all unspent outputs for an address (requires addressindex to be enabled).

Arguments:

::

	{
	  "addresses"
	    [
	      "address"  (string) The base58check encoded address
	      ,...
	    ],
	  "chainInfo"  (boolean) Include chain info with results
	}

Result:

::

	[
	  {
	    "address"  (string) The address base58check encoded
	    "txid"  (string) The output txid
	    "height"  (number) The block height
	    "outputIndex"  (number) The output index
	    "script"  (strin) The script hex encoded
	    "satoshis"  (number) The number of satoshis of the output
	  }
	]

Examples:

::

	> komodo-cli getaddressutxos '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'
	> curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressutxos", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/
