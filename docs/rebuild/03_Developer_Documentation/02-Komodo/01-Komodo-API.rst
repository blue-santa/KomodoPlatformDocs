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

To erase all synced blockchain data, the following files should be deleted:

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
``addressindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to maintain an index of all addresses and balances. It is initiated at run time and it is used to query address balances across the entire chain.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions above===.

The ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

``addressindex`` is enabled by default on any asset chain that utilizes the ``cc`` smart contract protocol.

Usage:

To initiate the ``addressindex`` command at runtime, include ``-addressindex=1`` as a parameter.

::

  ``./komodod -addressindex=1``

To set the ``addressindex`` feature as a default parameter, include the parameter in the coin's ``.conf`` configuration file.

::

  ``addressindex=1``

-txindex
--------
``txindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to track every transaction made on the relevant blockchain.

``txindex`` is enabled by default on all KMD-based coin daemons, and is utilized in dPoW, JUMBLR, and the CryptoConditions smart-contract protocol. Disabling the feature will cause a normal KMD-based coin daemon to malfunction.

-timestampindex
---------------
``timestampindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to maintain a timestamp index for all blockhashes. It is initiated at run time and it is used to query blocks by a range of timestamps.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions above===.

The ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

Usage:

To initiate the ``timestampindex`` command at runtime, include ``-timestampindex=1`` as a parameter.

::

  ``./komodod -timestampindex=1``

To set the ``timestampindex`` feature as a default parameter, include the parameter in the ``komodo.conf`` configuration file.

::

  ``timestampindex=1``

-spentindex
----------
``spentindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to maintain a full index of all spent transactions (txids). The parameter is called at runtime and it is used to search across the entire chain history.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions above===.

The ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

``spentindex`` is enabled by default on any asset chain that utilizes the ``cc`` smart contract protocol.

Usage:

To initiate the ``spentindex`` command at runtime, include ``-spentindex=1`` as a parameter.

::
  ``./komodod -spentindex=1``

To set the ``spentindex`` feature as a default parameter, include the parameter in the ``komodo.conf`` configuration file.

::
  ``spentindex=1``

AddressIndex
============
The AddressIndex API commands are used to query various aspects of the blockchain's history. Most require the ===link=== ``addressindex`` feature to be enabled, as these API commands scan the entire blockchain history.

getaddressbalance
-----------------
::
	getaddressbalance '{"address": ["address_string", "address_string", ...]}'

The ``getaddressbalance`` method returns the confirmed balance for an address(es). It requires ===link=== ``addressindex`` to be enabled.

===Insert "Run" sandbox here===
  Komodo API Demo: getaddressbalance method
  (example code)
  Run/Reset Buttons
===End sandbox===

Arguments:

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
	  "balance_string"  		       // (number)   the current confirmed balance of satoshis
	  "received_string" 		       // (number)   the total confirmed number of satoshis received (including change)
	}

Examples:
 * (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

	command:

	./komodo-cli getaddressbalance '{"addresses":["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'

	response:

	{
    "balance": 40000,
    "received": 1011916229
  }

::

	command:

	curl --user myrpcuser:myuserpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressbalance", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

	response:

  {
    "result": {
      "balance": 450010000,
      "received": 1711916229
    },
    "error": null,
    "id": "curltest"
  }


getaddressdeltas
----------------
::
  getaddressdeltas '{"addresses": ["address_string", "address_string", ...]}'

  getaddressdeltas '{"addresses": ["address_string", "address_string", ...], "start": start_number, "end": end_number, "chainInfo": boolean}'

The ``getaddressdeltas`` method returns all confirmed balance changes of an address. The parameters allow the user to optionally limit the response to a given interval of blocks. The method requires ===link=== ``addressindex`` to be enabled.

===Insert "Run" sandbox here===
  Komodo API Demo: getaddressdeltas method
  (example code)
  Run/Reset Buttons
===End sandbox===

Arguments:

::

	{
	  "addresses" 					   //
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

Examples (no optional parameters):
 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

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

  {
    "result": [
      {
        "satoshis": 1011876229,
        "txid": "39c61e8ea769ba1fc971cb7dadc531f25a2528d01a4244f379043248b6c51cc1",
        "index": 0,
        "blockindex": 0,
        "height": 1,
        "address": "RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"
      }
    ],
    "error": null,
    "id": "curltest"
  }


::
  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressdeltas", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"],"start":1,"end":200,"chainInfo":true}]}' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
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
    },
    "error": null,
    "id": "curltest"
  }


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
	  "addresses"
	    [
	      "address"                // (string)     the base58check encoded address
	      ,...                     //              the method accepts multiple addresses
	    ]
	}

Result:

::

	[
	  {
	    "address"                  // (string)     the base58check encoded address
	    "txid"                     // (string)     the related txid
	    "index"                    // (number)     the related input or output index
	    "satoshis"                 // (number)     the difference of satoshis
	    "timestamp"                // (number)     the time the transaction entered the mempool (seconds)
	    "prevtxid"                 // (string)     the previous txid (if spending)
	    "prevout"                  // (string)     the previous transaction output index (if spending)
	  }
	]

Examples:
 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	./komodo-cli getaddressmempool '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'

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

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressmempool", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
  "result": [
    {
      "address": "RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb",
      "txid": "708d8b67ea1f1b0a534515088911e90e77d623cddf901633e24cbb5b4c6f793c",
      "index": 0,
      "satoshis": -50000000,
      "timestamp": 1536603876,
      "prevtxid": "17474b73ec5a985c78a46435a021a1ad3ebd5609724ffd23d9c787c30f661342",
      "prevout": 1
    }
  ],
  "error": null,
  "id": "curltest"
}

getaddresstxids
---------------

::

  getaddresstxids '{"addresses": ["address_string"]}'

The ``getaddresstxids`` method returns the txids for an address(es). It requires ===link=== ``addressindex`` to be enabled.

===Insert "Run" sandbox here===
  Komodo API Demo: getaddresstxids method
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

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

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

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddresstxids", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
  "result": [
    "39c61e8ea769ba1fc971cb7dadc531f25a2528d01a4244f379043248b6c51cc1",
    "800e4331018d02458ff4f2a7722f0508b810f7fcf53bc1c5ac85aec4e5fa706b",
    "2a3c3664851370ff762b47d735cc661e3dbce4cf36b6c1b74799f3b1c847bd52"
  ],
  "error": null,
  "id": "curltest"
}

getaddressutxos
---------------
::

  getaddressutxos '{"addresses": ["address_string"]}'

The ``getaddressutxos`` method returns all unspent outputs for an address. It requires ===link==``addressindex`` to be enabled.

===Insert "Run" sandbox here===
  Komodo API Demo: getaddresstxids method
  (example code)
  Run/Reset Buttons
===End sandbox===

Arguments:

::

	{
	  "addresses"
	    [
	      "address"                // (string)   the base58check encoded address
	      ,...                     //            the method accepts multiple addresses
	    ],
	  "chainInfo"                  // (boolean)  include chain info with results
	}

Result:

::

	[
	  {
	    "address"                  // (string)   the address base58check encoded
	    "txid"                     // (string)   the output txid
	    "height"                   // (number)   the block height
	    "outputIndex"              // (number)   the output index
	    "script"                   // (string)   the script hex encoded
	    "satoshis"                 // (number)   the number of satoshis of the output
	  }
	]

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getaddressutxos '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'

  response:

  [
    {
      "address": "RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb",
      "txid": "2a3c3664851370ff762b47d735cc661e3dbce4cf36b6c1b74799f3b1c847bd52",
      "outputIndex": 0,
      "script": "2102e0d9ea73a391400ed2cb090e029d3f03eda0efaf371da11f436c076d817025e4ac",
      "satoshis": 10000,
      "height": 3
    }
  ]

::

  command:

  ./komodo-cli getaddressutxos '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"], "chainInfo": true}'


  response:

  {
    "utxos": [
      {
        "address": "RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb",
        "txid": "2a3c3664851370ff762b47d735cc661e3dbce4cf36b6c1b74799f3b1c847bd52",
        "outputIndex": 0,
        "script": "2102e0d9ea73a391400ed2cb090e029d3f03eda0efaf371da11f436c076d817025e4ac",
        "satoshis": 10000,
        "height": 3
      }
    ],
    "hash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
    "height": 398
  }

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressutxos", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": [
      {
        "address": "RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb",
        "txid": "2a3c3664851370ff762b47d735cc661e3dbce4cf36b6c1b74799f3b1c847bd52",
        "outputIndex": 0,
        "script": "2102e0d9ea73a391400ed2cb090e029d3f03eda0efaf371da11f436c076d817025e4ac",
        "satoshis": 10000,
        "height": 3
      }
    ],
    "error": null,
    "id": "curltest"
  }

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressutxos", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"], "chainInfo": true}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
      "utxos": [
        {
          "address": "RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb",
          "txid": "2a3c3664851370ff762b47d735cc661e3dbce4cf36b6c1b74799f3b1c847bd52",
          "outputIndex": 0,
          "script": "2102e0d9ea73a391400ed2cb090e029d3f03eda0efaf371da11f436c076d817025e4ac",
          "satoshis": 10000,
          "height": 3
        }
      ],
      "hash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
      "height": 398
    },
    "error": null,
    "id": "curltest"
  }


Blockchain
==========

getbestblockhash
----------------

::

  getbestblockhash

Returns the hash of the best (tip) block in the longest block chain.


===Insert "Run" sandbox here===
  Komodo API Demo
  (example code)
  Run/Reset Buttons
===End sandbox===


Arguments:

::

  (none)

Result:

::

	"hex"                        // (string)     the block hash hex encoded

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

  komodo-cli getbestblockhash

  response:

  0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getbestblockhash", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
    "error": null,
    "id": "curltest"
  }

getblock
--------

::

   getblock hash|height ( verbose )

The ``getblock`` command returns the block's relevant state information.

The verbose input is optional. The default value is true, and it will return a JSON object with information about the indicated block. If verbose is ``false``, the command returns a string that is serialized hex-encoded data for the indicated block.

Arguments:

::

	"hash|height"             // (string, required)                 the block hash or height
	verbose                   // (boolean, optional, default=true)  true returns a json object, false returns hex-encoded data

Result (for verbose = ``true``):

::

  {
    "hash"                  // (string)           the block hash (same as provided hash)
    "confirmations"         // (numeric)          the number of confirmations, or -1 if the block is not on the main chain
    "size"                  // (numeric)          the block size
    "height"                // (numeric)          the block height or index (same as provided height)
    "version"               // (numeric)          the block version
    "merkleroot"            // (string)           the merkle root
    "tx"
      [                     // (array of string)  the transaction ids
        "transactionid"     // (string)           the transaction id
        ,...
      ]
    "time"                  // (numeric)          the block time in seconds since epoch (Jan 1 1970 GMT)
    "nonce"                 // (numeric)          the nonce
    "bits"                  // (string)           the bits
    "difficulty"            // (numeric)          the difficulty
    "previousblockhash"     // (string)           the hash of the previous block
    "nextblockhash"         // (string)           the hash of the next block
  }

Result (for verbose=``false``):

::

	"data"                     // (string)          a string that is serialized, hex-encoded data for the indicated block

Examples (using blockhash):
 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getblock "00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09"

  response:

  {
    "hash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
    "confirmations": 1,
    "size": 278,
    "height": 398,
    "version": 4,
    "merkleroot": "d6e8292d85181a177c21497a7e636fc4f1eef1fbd2887b3a19e1d72134429668",
    "segid": -2,
    "tx": [
      "d6e8292d85181a177c21497a7e636fc4f1eef1fbd2887b3a19e1d72134429668"
    ],
    "time": 1536603968,
    "nonce": "00002474e66d5ef243d7b0a8eec32983492daf29e0b0887bd67b2107d1000004",
    "solution": "30a5e9153392b643d139cf205b270d55cb7d3b4779fd7a3666bdb744ef221c966fde1324",
    "bits": "200f0ef8",
    "difficulty": 1.000023305960651,
    "chainwork": "0000000000000000000000000000000000000000000000000000000000001a7f",
    "anchor": "59d2cde5e65c1414c32ba54f0fe4bdb3d67618125286e6a191317917c812c6d7",
    "valuePools": [
      {
        "id": "sprout",
        "monitored": true,
        "chainValue": 0.00000000,
        "chainValueZat": 0,
        "valueDelta": 0.00000000,
        "valueDeltaZat": 0
      }
    ],
    "previousblockhash": "09f9b547842b38a7748c8633eedb609b269138fdb3f2f75570fcb0d653fe42f4"
  }

::

  command:

  komodo-cli -ac_name=SIDD getblock "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084" false

  response:

  04000000f442fe53d6b0fc7055f7f2b3fd3891269b60dbee33868c74a7382b8447b5f9096896423421d7e1193a7b88d2fbf1eef1c46f637e7a49217c171a18852d29e8d6000000000000000000000000000000000000000000000000000000000000000040b7965bf80e0f20040000d107217bd67b88b0e029af2d498329c3eea8b0d743f25e6de6742400002430a5e9153392b643d139cf205b270d55cb7d3b4779fd7a3666bdb744ef221c966fde13240101000000010000000000000000000000000000000000000000000000000000000000000000ffffffff05028e010101ffffffff0110270000000000002321033097c6f4b12bd13a2e39b686b3a2fc30fe55a1d51221d857421e40564d5e237cac3fb7965b

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": ["00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09"] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
      "hash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
      "confirmations": 1,
      "size": 278,
      "height": 398,
      "version": 4,
      "merkleroot": "d6e8292d85181a177c21497a7e636fc4f1eef1fbd2887b3a19e1d72134429668",
      "segid": -2,
      "tx": [
        "d6e8292d85181a177c21497a7e636fc4f1eef1fbd2887b3a19e1d72134429668"
      ],
      "time": 1536603968,
      "nonce": "00002474e66d5ef243d7b0a8eec32983492daf29e0b0887bd67b2107d1000004",
      "solution": "30a5e9153392b643d139cf205b270d55cb7d3b4779fd7a3666bdb744ef221c966fde1324",
      "bits": "200f0ef8",
      "difficulty": 1.000023305960651,
      "chainwork": "0000000000000000000000000000000000000000000000000000000000001a7f",
      "anchor": "59d2cde5e65c1414c32ba54f0fe4bdb3d67618125286e6a191317917c812c6d7",
      "valuePools": [
        {
          "id": "sprout",
          "monitored": true,
          "chainValue": 0,
          "chainValueZat": 0,
          "valueDelta": 0,
          "valueDeltaZat": 0
        }
      ],
      "previousblockhash": "09f9b547842b38a7748c8633eedb609b269138fdb3f2f75570fcb0d653fe42f4"
    },
    "error": null,
    "id": "curltest"
  }

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": ["00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09", false] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": "04000000f442fe53d6b0fc7055f7f2b3fd3891269b60dbee33868c74a7382b8447b5f9096896423421d7e1193a7b88d2fbf1eef1c46f637e7a49217c171a18852d29e8d6000000000000000000000000000000000000000000000000000000000000000040b7965bf80e0f20040000d107217bd67b88b0e029af2d498329c3eea8b0d743f25e6de6742400002430a5e9153392b643d139cf205b270d55cb7d3b4779fd7a3666bdb744ef221c966fde13240101000000010000000000000000000000000000000000000000000000000000000000000000ffffffff05028e010101ffffffff0110270000000000002321033097c6f4b12bd13a2e39b686b3a2fc30fe55a1d51221d857421e40564d5e237cac3fb7965b",
    "error": null,
    "id": "curltest"
  }


Examples (using block height):

 * (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

  komodo-cli getblock 120

  response:

  {
    "hash": "0939408360b273fd681bbe5823999655fd5a7240303cdcbf952afe252246cc13",
    "confirmations": 279,
    "size": 277,
    "height": 120,
    "version": 4,
    "merkleroot": "4781cefbf7e14f6d7cdf89ae972391ae59b5776d1ed51204e94e65adf3ca6331",
    "segid": -2,
    "tx": [
      "4781cefbf7e14f6d7cdf89ae972391ae59b5776d1ed51204e94e65adf3ca6331"
    ],
    "time": 1536347890,
    "nonce": "000054c5822bb572319a67a89a3f511cf8caf8cd8ed6b7739c0b044b62ea000b",
    "solution": "03fc1abba5f415b1c422942835d46c7ba3e94665964da4c31e236c6cf9b3dfe6ffb65db1",
    "bits": "200f0f08",
    "difficulty": 1.000007093003461,
    "chainwork": "0000000000000000000000000000000000000000000000000000000000000809",
    "anchor": "59d2cde5e65c1414c32ba54f0fe4bdb3d67618125286e6a191317917c812c6d7",
    "valuePools": [
      {
        "id": "sprout",
        "monitored": true,
        "chainValue": 0.00000000,
        "chainValueZat": 0,
        "valueDelta": 0.00000000,
        "valueDeltaZat": 0
      }
    ],
    "previousblockhash": "01d1bfef50e079c53b36463fdf0ae55dc26b2205cd5f39c2bd030d19c2375e28",
    "nextblockhash": "0438bfda6a2706a622df7808fa5f4f32ac2e5d3039895ff8cb080d7e8e231188"
  }

::

  command:

  komodo-cli getblock 120 false

  response:

  04000000285e37c2190d03bdc2395fcd05226bc25de50adf3f46363bc579e050efbfd1013163caf3ad654ee90412d51e6d77b559ae912397ae89df7c6d4fe1f7fbce81470000000000000000000000000000000000000000000000000000000000000000f2ce925b080f0f200b00ea624b040b9c73b7d68ecdf8caf81c513f9aa8679a3172b52b82c55400002403fc1abba5f415b1c422942835d46c7ba3e94665964da4c31e236c6cf9b3dfe6ffb65db10101000000010000000000000000000000000000000000000000000000000000000000000000ffffffff0401780101ffffffff011027000000000000232103c0259e1a166e53f6ccf094ce37c0843d4a013622603bc301b4eb0f89c7cce823acf1ce925b

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": ["120"] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
      "hash": "0939408360b273fd681bbe5823999655fd5a7240303cdcbf952afe252246cc13",
      "confirmations": 279,
      "size": 277,
      "height": 120,
      "version": 4,
      "merkleroot": "4781cefbf7e14f6d7cdf89ae972391ae59b5776d1ed51204e94e65adf3ca6331",
      "segid": -2,
      "tx": [
        "4781cefbf7e14f6d7cdf89ae972391ae59b5776d1ed51204e94e65adf3ca6331"
      ],
      "time": 1536347890,
      "nonce": "000054c5822bb572319a67a89a3f511cf8caf8cd8ed6b7739c0b044b62ea000b",
      "solution": "03fc1abba5f415b1c422942835d46c7ba3e94665964da4c31e236c6cf9b3dfe6ffb65db1",
      "bits": "200f0f08",
      "difficulty": 1.000007093003461,
      "chainwork": "0000000000000000000000000000000000000000000000000000000000000809",
      "anchor": "59d2cde5e65c1414c32ba54f0fe4bdb3d67618125286e6a191317917c812c6d7",
      "valuePools": [
        {
          "id": "sprout",
          "monitored": true,
          "chainValue": 0,
          "chainValueZat": 0,
          "valueDelta": 0,
          "valueDeltaZat": 0
        }
      ],
      "previousblockhash": "01d1bfef50e079c53b36463fdf0ae55dc26b2205cd5f39c2bd030d19c2375e28",
      "nextblockhash": "0438bfda6a2706a622df7808fa5f4f32ac2e5d3039895ff8cb080d7e8e231188"
    },
    "error": null,
    "id": "curltest"
  }


::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": ["120", false] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": "04000000285e37c2190d03bdc2395fcd05226bc25de50adf3f46363bc579e050efbfd1013163caf3ad654ee90412d51e6d77b559ae912397ae89df7c6d4fe1f7fbce81470000000000000000000000000000000000000000000000000000000000000000f2ce925b080f0f200b00ea624b040b9c73b7d68ecdf8caf81c513f9aa8679a3172b52b82c55400002403fc1abba5f415b1c422942835d46c7ba3e94665964da4c31e236c6cf9b3dfe6ffb65db10101000000010000000000000000000000000000000000000000000000000000000000000000ffffffff0401780101ffffffff011027000000000000232103c0259e1a166e53f6ccf094ce37c0843d4a013622603bc301b4eb0f89c7cce823acf1ce925b",
    "error": null,
    "id": "curltest"
  }

getblockchaininfo
-----------------

::

  getblockchaininfo

The ``getblockchaininfo`` method returns a JSON object containing state information about blockchain processing.

 * Note that when the chain tip is at the last block before a network upgrade activation, the consensus.chaintipc value is not equal to the consensus.nextblock value. ``consensus.chaintip != consensus.nextblock``.

Arguments:

::

  (none)

Result:

::

  {
    "chain"                       // (string)         current network name as defined in BIP70 (main, test, regtest)
    "blocks"                      // (numeric)        the current number of blocks processed in the server
    "headers"                     // (numeric)        the current number of headers we have validated
    "bestblockhash"               // (string)         the hash of the currently best block
    "difficulty"                  // (numeric)        the current difficulty
    "verificationprogress"        // (numeric)        estimate of verification progress [0..1]
    "chainwork"                   // (string)         total amount of work in active chain, in hexadecimal
    "commitments"                 // (numeric)        the current number of note commitments in the commitment tree
    "softforks": [                // (array)          status of softforks in progress
      {
        "id"                      // (string)         name of softfork
        "version"                 // (numeric)        block version
        "enforce": {              // (object)         progress toward enforcing the softfork rules for new-version blocks
          "status"                // (boolean)        true if threshold reached
          "found"                 // (numeric)        number of blocks with the new version found
          "required"              // (numeric)        number of blocks required to trigger
          "window"                // (numeric)        maximum size of examined window of recent blocks
        },
        "reject": {
          ...                     // (object)         progress toward rejecting pre-softfork blocks (same fields as "enforce")
        }
      }, ...                      //                  can return multiple softfork objects
    ],
    "upgrades": {                 // (object)         status of network upgrades
      "xxxxxxxxx_string": {       // (string)         branch ID of the upgrade
          "name"                  // (string)         name of upgrade
          "activationheight"      // (numeric)        block height of activation
          "status"                // (string)         status of upgrade
          "info"                  // (string)         additional information about upgrade
      }, ...                      //                  can return multiple branch_ID_strings
    },
    "consensus": {                // (object)         branch IDs of the current and upcoming consensus rules
     "chaintip"                   // (string)         branch ID used to validate the current chain tip
     "nextblock"                  // (string)         branch ID that the next block will be validated under
    }
  }

Examples:

 * (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

  komodo-cli getblockchaininfo

  response:

  {
    "chain": "regtest",
    "blocks": 398,
    "headers": 398,
    "bestblockhash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
    "difficulty": 1.000023305960651,
    "verificationprogress": 1,
    "chainwork": "0000000000000000000000000000000000000000000000000000000000001a7f",
    "pruned": false,
    "commitments": 0,
    "valuePools": [
      {
        "id": "sprout",
        "monitored": true,
        "chainValue": 0.00000000,
        "chainValueZat": 0
      }
    ],
    "softforks": [
      {
        "id": "bip34",
        "version": 2,
        "enforce": {
          "status": false,
          "found": 399,
          "required": 750,
          "window": 1000
        },
        "reject": {
          "status": false,
          "found": 399,
          "required": 950,
          "window": 1000
        }
      }
    ],
    "upgrades": {
    },
    "consensus": {
      "chaintip": "00000000",
      "nextblock": "00000000"
    }
  }

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockchaininfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
      "chain": "regtest",
      "blocks": 398,
      "headers": 398,
      "bestblockhash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
      "difficulty": 1.000023305960651,
      "verificationprogress": 1,
      "chainwork": "0000000000000000000000000000000000000000000000000000000000001a7f",
      "pruned": false,
      "commitments": 0,
      "valuePools": [
        {
          "id": "sprout",
          "monitored": true,
          "chainValue": 0,
          "chainValueZat": 0
        }
      ],
      "softforks": [
        {
          "id": "bip34",
          "version": 2,
          "enforce": {
            "status": false,
            "found": 399,
            "required": 750,
            "window": 1000
          },
          "reject": {
            "status": false,
            "found": 399,
            "required": 950,
            "window": 1000
          }
        }
      ],
      "upgrades": {},
      "consensus": {
        "chaintip": "00000000",
        "nextblock": "00000000"
      }
    },
    "error": null,
    "id": "curltest"
  }

getblockcount
-------------

::

  getblockcount

The ``getblockcount`` method returns the number of blocks in the best valid block chain.

Arguments:

::

  (none)

Result:

::

	(numeric) The current block count

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

  komodo-cli getblockcount

  response:

  398

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockcount", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": 398,
    "error": null,
    "id": "curltest"
  }

getblockhash
------------

::

  getblockhash index

The ``getblockhash`` method returns the hash of the indicated block index, according to the best blockchain at the time provided.

Arguments:

::

	index                         // (numeric, required)     the block index

Result:

::

	"hash"                        // (string)                the block hash

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

  komodo-cli getblockhash 100

  response:

  08674c7a6ab6c40000d45e2094f2cafc6575bfcfdd1ce90fa0060fa573803024

::

  command:

	curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockhash", "params": [1000] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": "08674c7a6ab6c40000d45e2094f2cafc6575bfcfdd1ce90fa0060fa573803024",
    "error": null,
    "id": "curltest"
  }

getblockhashes timestamp
------------------------

::

  getblockhashes high low '{"noOrphans": bool, "logicalTimes": bool}'

The ``getblockhashes`` method returns an array of hashes of blocks within the timestamp range provided.

Arguments:

::

	high                       // (numeric, required)    the newer block timestamp
	low                        // (numeric, required)    the older block timestamp
	options                    // (string, required)     a json object, formatted as a string
    {
      "noOrphans"            // (boolean)              will only include blocks on the main chain
      "logicalTimes"         // (boolean)              will include logical timestamps with hashes
    }

Result:

::

	[
		  "hash"                 // (string)               the block hash
	]
	[
	  {
	    "blockhash"            // (string)               the block hash
	    "logicalts"            // (numeric)              the logical timestamp
	  }
	]

Examples:
 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getblockhashes 1231614698 1231024505

  response:


::

  command:

	curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockhashes", "params": [1231614698, 1231024505] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

::
  command:

  komodo-cli getblockhashes 1231614698 1231024505 '{"noOrphans":false, "logicalTimes":true}'

  response:

getblockheader
--------------

::

  getblockheader "hash" ( verbose )

The ``getblockheader`` method returns information about the indicated block.

The verbose input is optional. If verbose is false, the method returns a string that is serialized, hex-encoded data for the indicated blockheader. If verbose is true, the method returns a JSON object with information about the indicated blockheader.

Arguments:

::

	"hash"                  // (string, required)                  the block hash
	verbose                 // (boolean, optional, default=true)   true returns a json object, false returns hex-encoded data

Result (for verbose = true):

::

	{
	  "hash"                 // (string)       the block hash (same as provided)
	  "confirmations"        // (numeric)      the number of confirmations, or -1 if the block is not on the main chain
	  "height"               // (numeric)      the block height or index
	  "version"              // (numeric)      the block version
	  "merkleroot"           // (string)       the merkle root
	  "time"                 // (numeric)      the block time in seconds since epoch (Jan 1 1970 GMT)
	  "nonce"                // (numeric)      the nonce
	  "bits"                 // (string)       the bits
	  "difficulty"           // (numeric)      the difficulty
	  "previousblockhash"    // (string)       the hash of the previous block
	  "nextblockhash"        // (string)       the hash of the next block
	}

Result (for verbose=false):

::

	"data"                   // (string)       a string that is serialized hex-encoded data for the indicated block

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getblockheader "00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09"

  response:

  {
    "hash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
    "confirmations": 1,
    "height": 398,
    "version": 4,
    "merkleroot": "d6e8292d85181a177c21497a7e636fc4f1eef1fbd2887b3a19e1d72134429668",
    "time": 1536603968,
    "nonce": "00002474e66d5ef243d7b0a8eec32983492daf29e0b0887bd67b2107d1000004",
    "solution": "30a5e9153392b643d139cf205b270d55cb7d3b4779fd7a3666bdb744ef221c966fde1324",
    "bits": "200f0ef8",
    "difficulty": 1.000023305960651,
    "chainwork": "0000000000000000000000000000000000000000000000000000000000001a7f",
    "segid": -2,
    "previousblockhash": "09f9b547842b38a7748c8633eedb609b269138fdb3f2f75570fcb0d653fe42f4"
  }

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockheader", "params": ["0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084"] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
      "hash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
      "confirmations": 1,
      "height": 398,
      "version": 4,
      "merkleroot": "d6e8292d85181a177c21497a7e636fc4f1eef1fbd2887b3a19e1d72134429668",
      "time": 1536603968,
      "nonce": "00002474e66d5ef243d7b0a8eec32983492daf29e0b0887bd67b2107d1000004",
      "solution": "30a5e9153392b643d139cf205b270d55cb7d3b4779fd7a3666bdb744ef221c966fde1324",
      "bits": "200f0ef8",
      "difficulty": 1.000023305960651,
      "chainwork": "0000000000000000000000000000000000000000000000000000000000001a7f",
      "segid": -2,
      "previousblockhash": "09f9b547842b38a7748c8633eedb609b269138fdb3f2f75570fcb0d653fe42f4"
    },
    "error": null,
    "id": "curltest"
  }

getchaintips
------------
::

  getchaintips

The ``getchaintips`` method returns information about all known tips in the block tree, including the main chain and any orphaned branches.

Arguments:

::

  (none)

Result:

::

	[
	  {
	    "height"               // (numeric)    height of the chain tip
	    "hash"                 // (string)     block hash of the tip
	    "branchlen"            // (numeric)    zero for main chain
	    "status"               // (string)     "active" for the main chain
	  },
	  {
	    "height"               // (numeric)    height of the branch tip
	    "hash"                 // (string)     blockhash of the branch tip
	    "branchlen"            // (numeric)    length of branch connecting the tip to the main chain
	    "status"               // (string)     status of the chain
	  }
	]

Possible values for status:

::

	1.  "invalid"               this branch contains at least one invalid block
	2.  "headers-only"          not all blocks for this branch are available, but the headers are valid
	3.  "valid-headers"         all blocks are available for this branch, but they were never fully validated
	4.  "valid-fork"            this branch is not part of the active chain, but is fully validated
	5.  "active"                this is the tip of the active main chain, which is certainly valid

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getchaintips

  response:

  [
    {
      "height": 398,
      "hash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
      "branchlen": 0,
      "status": "active"
    }
  ]

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getchaintips", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": [
      {
        "height": 398,
        "hash": "0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084",
        "branchlen": 0,
        "status": "active"
      }
    ],
    "error": null,
    "id": "curltest"
  }

getdifficulty
-------------

::

  getdifficulty

The ``getdifficulty`` method returns the proof-of-work difficulty as a multiple of the minimum difficulty.

Arguments:

::

  (none)

Result:

::

	number                     // (numeric)  the proof-of-work difficulty as a multiple of the minimum difficulty

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getdifficulty

  response:

  1.000023305960651


::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getdifficulty", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": 1.000023305960651,
    "error": null,
    "id": "curltest"
  }

getmempoolinfo
--------------

::

  getmempoolinfo

The ``getmempoolinfo`` method returns details on the active state of the transaction memory pool.

Arguments:

::

  (none)

Result:

::

	{
	  "size"                 // (numeric)    current tx count
	  "bytes"                // (numeric)    sum of all tx sizes
	  "usage"                // (numeric)    total memory usage for the mempool
	}

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getmempoolinfo

  response:

  {
    "size": 1,
    "bytes": 226,
    "usage": 896
  }

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getmempoolinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
      "size": 1,
      "bytes": 226,
      "usage": 896
    },
    "error": null,
    "id": "curltest"
  }

getrawmempool
-------------

::

  getrawmempool ( verbose )

The ``getrawmempool`` method returns all transaction ids in the memory pool as a JSON array of transaction ids.

The verbose input is optional and is false by default. When it is true, the method instead returns a JSON object with various related data.

Arguments:

::

	verbose                // (boolean, optional, default=false)     true for a JSON object, false for a JSON array of transaction ids

Result (verbose = false):

::

	[
	  "transactionid"                 // (string)    the transaction id
	  ,...
	]

Result (verbose = true):

::

	{
	  "transactionid" : {
	    "size"                        // (numeric)   transaction size in bytes
	    "fee"                         // (numeric)   transaction fee in ZEC
    	"time"                        // (numeric)   local time transaction entered pool in seconds since 1 Jan 1970 GMT
    	"height"                      // (numeric)   block height when transaction entered pool
    	"startingpriority"            // (numeric)   priority when transaction entered pool
    	"currentpriority"             // (numeric)   transaction priority now
    	"depends": [                  // (array)     unconfirmed transactions used as inputs for this transaction
        "transactionid"             // (string)    parent transaction id
	       ...
      ]
	  }, ...
	}

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

  komodo-cli getrawmempool true

  response:

  {
    "44760f145303cae081819c6e54665d6716c98e97691603b4edf133b8180e6048": {
      "size": 488,
      "fee": 0.00011462,
      "time": 1536618366,
      "height": 448,
      "startingpriority": 20910198.65384615,
      "currentpriority": 20910198.65384615,
      "depends": [
      ]
    }
  }

::

  command:

	curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getrawmempool", "params": [true] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
      "44760f145303cae081819c6e54665d6716c98e97691603b4edf133b8180e6048": {
        "size": 488,
        "fee": 0.00011462,
        "time": 1536618366,
        "height": 448,
        "startingpriority": 20910198.65384615,
        "currentpriority": 20910198.65384615,
        "depends": []
      }
    },
    "error": null,
    "id": "curltest"
  }

getspentinfo
------------

::

  getspentinfo '{"txid": txid_string, "index", block_height_number}'

The ``getspentinfo`` method returns the transaction id and index where an output is spent.

Arguments:

::

	{
	  "txid"             // (string)     the hex string of the txid
	  "index"            // (number)     the start block height
	}

Result:

::

	{
	  "txid"             // (string)     the transaction id
	  "index"            // (number)     the spending input index
	  ,...
	}

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getspentinfo '{"txid": "41ec75822318373bd00513efe7c708e745ab370db08ef4e0bd2ba4882ea77b40", "index": 0}'

  response:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getspentinfo", "params": [{"txid": "41ec75822318373bd00513efe7c708e745ab370db08ef4e0bd2ba4882ea77b40", "index": 0}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

gettxout
--------

::

  gettxout "txid_string" vout_number ( includemempool_bool )

The ``gettxout`` method returns details about an unspent transaction output.

Arguments:

::

	"txid"                       // (string, required)     the transaction id
	vout                         // (numeric, required)    vout value
	includemempool               // (boolean, optional)    whether to include the mempool

Result:

::

	{
	  "bestblock"                // (string)               the block hash
	  "confirmations"            // (numeric)              the number of confirmations
	  "value"                    // (numeric)              the transaction value in ZEC
  	"scriptPubKey": {          //
    	 "asm"                   // (string)
    	 "hex"                   // (string)
    	 "reqSigs"               // (numeric)              number of required signatures
    	 "type"                  // (string)               the type, e.g. pubkeyhash
    	 "addresses" : [         // (array of strings)     array of addresses
    	    "zcashaddress"       // (string)               address on blockchain
    	    ,...
    	 ]
  	},
  	"version"                  // (numeric)              the version
  	"coinbase"                 // (boolean)              coinbase or not
	}

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli gettxout "txid" 1

  response:

  {
    "bestblock": "0e398d8d00f7846f28b47a6c0da16b14002441f5a5340b6d492060c698bdd84c",
    "confirmations": 252,
    "value": 0.00010000,
    "scriptPubKey": {
      "asm": "03c0259e1a166e53f6ccf094ce37c0843d4a013622603bc301b4eb0f89c7cce823 OP_CHECKSIG",
      "hex": "2103c0259e1a166e53f6ccf094ce37c0843d4a013622603bc301b4eb0f89c7cce823ac",
      "reqSigs": 1,
      "type": "pubkey",
      "addresses": [
        "RM1mKzZDEr462UBqVjXSKXR3F83yMpG3Ue"
      ]
    },
    "version": 1,
    "coinbase": true
  }

::

  command:

	curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "gettxout", "params": ["txid", 1] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
      "bestblock": "0e398d8d00f7846f28b47a6c0da16b14002441f5a5340b6d492060c698bdd84c",
      "confirmations": 252,
      "value": 0.0001,
      "scriptPubKey": {
        "asm": "03c0259e1a166e53f6ccf094ce37c0843d4a013622603bc301b4eb0f89c7cce823 OP_CHECKSIG",
        "hex": "2103c0259e1a166e53f6ccf094ce37c0843d4a013622603bc301b4eb0f89c7cce823ac",
        "reqSigs": 1,
        "type": "pubkey",
        "addresses": [
          "RM1mKzZDEr462UBqVjXSKXR3F83yMpG3Ue"
        ]
      },
      "version": 1,
      "coinbase": true
    },
    "error": null,
    "id": "curltest"
  }

gettxoutproof
-------------

::

  gettxoutproof '["transaction_id_string",...]' ( "blockhash_string" )

The ``gettxoutproof`` method returns a hex-encoded proof showing that the indicated transaction was included in a block.

**NOTE:** By default this function only works in certain situations. It is successful when there is an unspent output in the utxo for this transaction. It is possible to make the command always successful; you need to maintain a transaction index, using the ``-txindex`` command-line option at runtime, or you must manually specify the hash of the block in which the transaction is included.

Arguments:

::

  [
    "txid_string"                  // (string)               a transaction hash
    ,...
  ]
	"blockhash_string"               // (string, optional)     if specified, looks for txid in the block with this hash

Result:

::

	"data"                           // (string)               a string that is a serialized, hex-encoded data for the proof

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

  ./komodo-cli -ac_name=SIDD gettxoutproof '["c71f4a2ebf87bdd588e3aa168917933ee4be1661245ebf52d5708a8339cf9d7a"]' "0a28e2fb630b282138bf23bb79f597b11acff6f57c8d9c1c10fa54770035c813"

  response:

  040000004cd8bd98c66020496d0b34a5f5412400146ba10d6c7ab4286f84f7008d8d390e9ca9575183f60906e293e9766997396bec59f1c0b966085de3d17f8ac3c9d5280000000000000000000000000000000000000000000000000000000000000000da05975bf50e0f202d004b81fcc388cfd411d8c7c59a548e070b5affe938ce8ce830f10b298b00002402939a9a31df1305b40d26d9748283b102c708258717248d0d63f01d2957d8e3dcf56f6e03000000022e4babc29707fbdd8da2e4277b7c8b8b09e837f409eb047c936904d75fc8e6267a9dcf39838a70d552bf5e246116bee43e93178916aae388d5bd87bf2e4a1fc7010d

gettxoutsetinfo
---------------

::

  gettxoutsetinfo

The ``gettxoutsetinfo`` method returns statistics about the unspent transaction output set.

* Note this call may take a long time to complete, depending on the state of your blockchain.

Arguments

::

  (none)

Result:

::

	{
	  "height"                 // (numeric)        the current block height (index)
	  "bestblock"              // (string)         the best block hash hex
	  "transactions"           // (numeric)        the number of transactions
	  "txouts"                 // (numeric)        the number of output transactions
 	  "bytes_serialized"       // (numeric)        the serialized size
	  "hash_serialized"        // (string)         the serialized hash
	  "total_amount"           // (numeric)        the total amount
	}

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

	command:

  komodo-cli gettxoutsetinfo

  response:

  {
    "height": 459,
    "bestblock": "0a28e2fb630b282138bf23bb79f597b11acff6f57c8d9c1c10fa54770035c813",
    "transactions": 258,
    "txouts": 261,
    "bytes_serialized": 18051,
    "hash_serialized": "fdd2039fa21400be0928b26dfe534f543dc5090989bcbd97fdc81b30ce7dca3a",
    "total_amount": 10.16456229
  }

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "gettxoutsetinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": {
      "height": 459,
      "bestblock": "0a28e2fb630b282138bf23bb79f597b11acff6f57c8d9c1c10fa54770035c813",
      "transactions": 258,
      "txouts": 261,
      "bytes_serialized": 18051,
      "hash_serialized": "fdd2039fa21400be0928b26dfe534f543dc5090989bcbd97fdc81b30ce7dca3a",
      "total_amount": 10.16456229
    },
    "error": null,
    "id": "curltest"
  }

kvsearch key
------------

``COMING SOON``

kvupdate key value flags/passphrase
-----------------------------------

``COMING SOON``

minerids needs height
---------------------

``COMING SOON``

notaries height timestamp
-------------------------

``COMING SOON``

paxpending
----------

::

  paxpending

``DEPRECATED``

paxprice
--------

::

  paxprice "base" "rel" height

``DEPRECATED``

paxprices
---------

::

  paxprices "base" "rel" maxsamples

``DEPRECATED``

txMoMproof needs a txid
-----------------------

``COMING SOON``

verifychain
-----------

::

  verifychain ( checklevel numblocks )

The ``verifychain`` method verifies the coin daemon's blockchain database.

Arguments:

::

	checklevel           // (numeric, optional, 0-4, default=3)        indicates the thoroughness of block verification
	numblocks            // (numeric, optional, default=288, 0=all)    indicates the number of blocks to verify

Result:

::

	true|false           // (boolean)                                  verification was successful or unsuccessful

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli verifychain

  response:

  true

::

  command:

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "verifychain", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
    "result": true,
    "error": null,
    "id": "curltest"
  }

verifytxoutproof
----------------

::

  verifytxoutproof "proof_string"

The ``verifytxoutproof`` method verifies that a proof points to a transaction in a block. It returns the transaction to which the proof is committed, or it will throw an RPC error if the block is not in the current best chain.

Arguments:

::

	"proof_string"             // (string, required)       the hex-encoded proof generated by gettxoutproof

Result:

::

	[
    "txid"                   // (array, strings)         the transaction ids which the proof commits to; the array is empty if the proof is invalid
  ]

Examples:

*  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

  komodo-cli -ac_name=SIDD verifytxoutproof "040000004cd8bd98c66020496d0b34a5f5412400146ba10d6c7ab4286f84f7008d8d390e9ca9575183f60906e293e9766997396bec59f1c0b966085de3d17f8ac3c9d5280000000000000000000000000000000000000000000000000000000000000000da05975bf50e0f202d004b81fcc388cfd411d8c7c59a548e070b5affe938ce8ce830f10b298b00002402939a9a31df1305b40d26d9748283b102c708258717248d0d63f01d2957d8e3dcf56f6e03000000022e4babc29707fbdd8da2e4277b7c8b8b09e837f409eb047c936904d75fc8e6267a9dcf39838a70d552bf5e246116bee43e93178916aae388d5bd87bf2e4a1fc7010d"

  response:

  [
    "c71f4a2ebf87bdd588e3aa168917933ee4be1661245ebf52d5708a8339cf9d7a"
  ]

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc    --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "verifytxoutproof", "params": ["040000004cd8bd98c66020496d0b34a5f5412400146ba10d6c7ab4286f84f7008d8d390e9ca9575183f60906e293e9766997396bec59f1c0b966085de3d17f8ac3c9d5280000000000000000000000000000000000000000000000000000000000000000da05975bf50e0f202d004b81fcc388cfd411d8c7c59a548e070b5affe938ce8ce830f10b298b00002402939a9a31df1305b40d26d9748283b102c708258717248d0d63f01d2957d8e3dcf56f6e03000000022e4babc29707fbdd8da2e4277b7c8b8b09e837f409eb047c936904d75fc8e6267a9dcf39838a70d552bf5e246116bee43e93178916aae388d5bd87bf2e4a1fc7010d"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801

  response:

  {
    "result": [
      "c71f4a2ebf87bdd588e3aa168917933ee4be1661245ebf52d5708a8339cf9d7a"
    ],
    "error": null,
    "id": "curltest"
  }
