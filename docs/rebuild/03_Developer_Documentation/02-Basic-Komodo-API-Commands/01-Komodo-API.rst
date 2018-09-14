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

``komodo-cli [API COMMAND]`` (Linux)

The API can likewise be used for all KMD-based independent blockchains. Two modifications are required: the name of the independent blockchain and the total coin supply.

``komodo-cli -ac_name=[BLOCKCHAIN NAME] -ac_supply=[BLOCKCHAIN COIN SUPPLY]``

The list of available API commands can be retrieved locally by executing:

``komodo-cli help``

To learn more about a specific API command, execute:

``komodo-cli help [API COMMAND]``.

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
:ref:`minerids height`
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

=== we need to add this section above in the index? Or perhaps this stuff should be condensed into the Control section? Maybe the index commands should be condensed into the generate section, too? ===

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
``txindex`` is a parameter that instructs a KMD-based coin daemon to track every transaction made on the relevant blockchain.

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
-----------
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
  Komodo API Demo
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

	komodo-cli getaddressbalance '{"addresses":["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'

	response:

	{
    "balance": 40000,
    "received": 1011916229
  }

::

	command:

	curl --user myrpcuser:myuserpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressbalance", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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
  Komodo API Demo
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

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getaddressdeltas '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'

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

  komodo-cli getaddressdeltas '{"addresses":["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"],"start":1,"end":200,"chainInfo":true}'


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

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressdeltas", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressdeltas", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"],"start":1,"end":200,"chainInfo":true}]}' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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
  getaddressmempool '{"addresses": ["address_string", "address_string", ... ]}'

The ``getaddressmempool`` method returns all mempool deltas for an address. It requires ===link===``addressindex`` to be enabled.

===Insert "Run" sandbox here===
  Komodo API Demo
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

	komodo-cli getaddressmempool '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}'

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressmempool", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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
  Komodo API Demo
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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddresstxids", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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
  Komodo API Demo
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

  komodo-cli getaddressutxos '{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"], "chainInfo": true}'


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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressutxos", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressutxos", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"], "chainInfo": true}] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getbestblockhash", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": ["00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": ["00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09", false] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": ["120"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": ["120", false] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockchaininfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockcount", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockhash", "params": [1000] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": "08674c7a6ab6c40000d45e2094f2cafc6575bfcfdd1ce90fa0060fa573803024",
    "error": null,
    "id": "curltest"
  }

getblockhashes
--------------

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

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockhashes", "params": [1231614698, 1231024505] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockheader", "params": ["0dd66ee1f151c38f73843378c08715ee3f4d3cf2888783e2846b81c057987084"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getchaintips", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

	number             // (numeric)  the proof-of-work difficulty as a multiple of the minimum difficulty

Examples:

 *  (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

::

  command:

	komodo-cli getdifficulty

  response:

  1.000023305960651


::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getdifficulty", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getmempoolinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getrawmempool", "params": [true] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getspentinfo", "params": [{"txid": "41ec75822318373bd00513efe7c708e745ab370db08ef4e0bd2ba4882ea77b40", "index": 0}] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "gettxout", "params": ["txid", 1] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

  komodo-cli -ac_name=SIDD gettxoutproof '["c71f4a2ebf87bdd588e3aa168917933ee4be1661245ebf52d5708a8339cf9d7a"]' "0a28e2fb630b282138bf23bb79f597b11acff6f57c8d9c1c10fa54770035c813"

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "gettxoutsetinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

kvsearch
--------

::

  kvsearch "key_string"

The ``kvsearch`` method searches for a key stored via the ===link=== ``kvupdate`` command.

 * Note: This feature is only available for asset chains.

Arguments:

  key                // (string, required)    search the chain for this key

Result:
{
  "coin"             // (string)              chain the key is stored on
  "currentheight"    // (numeric)             current height of the chain
  "key"              // (string)              key
  "keylen"           // (string)              length of the key
  "owner"            // (string)              hex string representing the owner of the key
  "height"           // (numeric)             height the key was stored at
  "expiration"       // (numeric)             height the key will expire
  "flags": x         // (numeric)             1 if the key was created with a password; 0 otherwise
  "value"            // (string)              stored value
  "valuesize"        // (string)              amount of characters stored
}

Examples:

::

  command:

  komodo-cli kvsearch examplekey

  response:

  {
    "coin": "MYCOIN",
    "currentheight": 566,
    "key": "examplekey",
    "keylen": 10,
    "owner": "1ff91604c6adb6ec550e7575fe9f1ca591704572e125f55bed03a21c242c31b7",
    "height": 561,
    "expiration": 2001,
    "flags": 0,
    "value": "examplevalue",
    "valuesize": 12
  }

::

  command:

  curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "kvsearch", "params": ["examplekey"] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  response:

  {
    "result": {
      "coin": "MYCOIN",
      "currentheight": 566,
      "key": "examplekey",
      "keylen": 10,
      "owner": "1ff91604c6adb6ec550e7575fe9f1ca591704572e125f55bed03a21c242c31b7",
      "height": 561,
      "expiration": 2001,
      "flags": 0,
      "value": "examplevalue",
      "valuesize": 12
    },
    "error": null,
    "id": "curltest"
  }


kvupdate
--------

::

  kvupdate "key_string" "value_string" days "passphrase_string"

The ``kvupdate`` method stores a key/value pair via OP_RETURN.

This feature is only available for asset chains.

The maximum value memory size is 8kB.

Arguments:

::

  "key"                     // (string, required)     key (should be unique)
  "value"                   // (string, required)     value
  "days"                    // (numeric, required)    amount of days before the key expires (1440 blocks/day); minimum 1 day
  "passphrase"              // (string, optional)     passphrase required to update this key

Result:

::
  {
    "coin"                  // (string)               chain the key is stored on
    "height"                // (numeric)              height the key was stored at
    "expiration"            // (numeric)              height the key will expire
    "flags"                 // (string)               amount of days the key will be stored
    "key"                   // (numeric)              stored key
    "keylen"                // (numeric)              length of the key
    "value"                 // (numeric)              stored value
    "valuesize"             // (string)               length of the stored value
    "fee"                   // (string)               transaction fee paid to store the key
    "txid"                  // (string)               transaction id
  }

Examples:

::

  command:

  komodo-cli kvupdate "examplekey" "examplevalue" 2 "examplepassphrase"

  response:

  {
    "coin": "MYCOIN",
    "owner": "1ff91604c6adb6ec550e7575fe9f1ca591704572e125f55bed03a21c242c31b7",
    "height": 566,
    "expiration": 2006,
    "flags": 3,
    "key": "examplekey",
    "keylen": 10,
    "value": "examplevalue",
    "valuesize": 12,
    "fee": 0.001,
    "txid": "2dc76f39188bb006931a2c924fdf66bc3baf149bf880fffad778cabd6ace5749"
  }

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc   --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "kvupdate", "params": ["examplekey", "examplevalue", "2", "examplepassphrase"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801

  response:

  {
    "result": {
      "coin": "MYCOIN",
      "owner": "1ff91604c6adb6ec550e7575fe9f1ca591704572e125f55bed03a21c242c31b7",
      "height": 566,
      "expiration": 2006,
      "flags": 3,
      "key": "examplekey",
      "keylen": 10,
      "value": "examplevalue",
      "valuesize": 12,
      "fee": 0.001,
      "txid": "9f44dc664882198b14e9a8c466d466efcdd070ccb6f57be8e2884aa11e7b2a30"
    },
    "error": null,
    "id": "curltest"
  }

minerids
--------

::

  minerids height

The ``minerids`` method returns information about the notary nodes and external miners at a specific block height. The response will calculate results according to the 2000 blocks proceeding the indicated "height" block.

Arguments:

::

  heights                   // (number)   the block height for the query

Results:

::

  {
    "mined": [
      {
        "notaryid"          // (number)   the id of the specific notary node
        "kmdaddress"        // (string)   the KMD address of the notary node
        "pubkey"            // (string)   the public signing key of the notary node
        "blocks"            // (number)
      }
    ]
  }

Examples:


::

  command:

  komodo-cli minerids 1000000

  response:

  {
    "mined": [
      {
        "notaryid": 0,
        "KMDaddress": "RNJmgYaFF5DbnrNUX6pMYz9rcnDKC2tuAc",
        "pubkey": "03b7621b44118017a16043f19b30cc8a4cfe068ac4e42417bae16ba460c80f3828",
        "blocks": 22
      }
        ...     // (63 responses omitted from the documentation for brevity)
      ,
      {
        "pubkey": "external miners",
        "blocks": 541
      }
    ],
    "numnotaries": 64
  }

::

  command:

  curl --user userb4911b4842afadc2:68c3394f2b2ee55fddeb8e8e2c3fd372 --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "minerids", "params": ["1000000"] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  response:

  {
    "result": {
      "mined": [
        {
          "notaryid": 0,
          "KMDaddress": "RNJmgYaFF5DbnrNUX6pMYz9rcnDKC2tuAc",
          "pubkey": "03b7621b44118017a16043f19b30cc8a4cfe068ac4e42417bae16ba460c80f3828",
          "blocks": 22
        }
          ...     // (63 responses omitted from the documentation for brevity)
        ,
        {
          "pubkey": "external miners",
          "blocks": 541
        }
      ],
      "numnotaries": 64
    },
    "error": null,
    "id": "curltest"
  }

notaries height timestamp
-------------------------

::

  notaries height timestamp

  notaries height

  notaries timestamp

The ``notaries`` method returns the public key, BTC address, and KMD address for each Komodo notary node.

Either or both of the height and timestamp parameters will suffice.

Arguments:

::

                          // (at least one of the inputs must be provided)
  height                  // (number)     the block height desired for the query
  timestamp               // (number)     the timestamp of the block desired for the query

Results:

  {
    "notaries": [
      {
        "pubkey"          // (string)       the public signing key of the indicated notary node, used on the KMD network to create notary-node authorized transactions
        "BTCaddress"      // (string)       the public BTC address the notary node uses on the BTC blockchain to create notarizations
        "KMDaddress"      // (string)       the public KMD address the notary node uses on the KMD blockchain to create notarizations
      },
        ...               //                property will return typically 64 objects
    ],
    "numnotaries"         // (number)       the number of notary nodes; typically it is 64, but may vary on rare circumstances, such as during election seasons
    "height"              // (number)       the block height number at which the notary-node information applies
    "timestamp"           // (number)       the timestamp at which the notary-node information applies
  }

Examples:

 * Note: Information about myrpcuser, myrpcpassword, and myrpcport can be found in the coin's .conf file.

::

  command:

  komodo-cli notaries 1536365515

  response:

  {
    "notaries": [
      {
        "pubkey": "03b7621b44118017a16043f19b30cc8a4cfe068ac4e42417bae16ba460c80f3828",
        "BTCaddress": "1E2ac2gxeFR2ir1H3vqETTperWkiXkwy99",
        "KMDaddress": "RNJmgYaFF5DbnrNUX6pMYz9rcnDKC2tuAc"
      },
        ...   // (63 responses omitted from the documentation for brevity)
    ],
    "numnotaries": 64,
    "height": 1536365515,
    "timestamp": 1536792974
  }

::

  command:
  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "notaries", "params": ["1000000"] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {
  "result": {
    "notaries": [
      {
        "pubkey": "03b7621b44118017a16043f19b30cc8a4cfe068ac4e42417bae16ba460c80f3828",
        "BTCaddress": "1E2ac2gxeFR2ir1H3vqETTperWkiXkwy99",
        "KMDaddress": "RNJmgYaFF5DbnrNUX6pMYz9rcnDKC2tuAc"
      },
        ...       // (63 responses omitted from documentation for brevity)
    ],
    "numnotaries": 64,
    "height": 1000000,
    "timestamp": 1536365515
  },
  "error": null,
  "id": "curltest"
}

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

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "verifychain", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

The ``verifytxoutproof`` method verifies that a proof points to a transaction in a block. It returns the transaction to which the proof is comitted, or it will throw an RPC error if the block is not in the current best chain.

Arguments:

::

	"proof_string"             // (string, required)       the hex-encoded proof generated by gettxoutproof

Result:

::

	[
    "txid"                   // (array, strings)         the transaction ids which the proof commits to; the array is empty if the proof is invalid
  ]

Examples:

 * (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

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

Control
=======

getinfo
-------

::

  getinfo

The ``getinfo`` method returns an object containing various state info.

Arguments:

::

  (none)

Result:

::

	{
	  "version"              // (numeric)          the server version
	  "protocolversion"      // (numeric)          the protocol version
	  "walletversion"        // (numeric)          the wallet version
	  "balance"              // (numeric)          the total Zcash balance of the wallet
	  "blocks"               // (numeric)          the current number of blocks processed in the server
	  "timeoffset"           // (numeric)          the time offset
	  "connections"          // (numeric)          the number of connections
	  "proxy"                // (string, optional) the proxy used by the server
	  "difficulty"           // (numeric)          the current difficulty
	  "testnet"              // (boolean)          if the server is using testnet or not
	  "keypoololdest"        // (numeric)          the timestamp (seconds since GMT epoch) of the oldest pre-generated key in the key pool
	  "keypoolsize"          // (numeric)          how many new keys are pre-generated
	  "unlocked_until"       // (numeric)          the timestamp in seconds since epoch (midnight Jan 1 1970 GMT) that the wallet is unlocked for transfers, or 0 if the wallet is locked
	  "paytxfee"             // (numeric)          the transaction fee set in ZEC/kB
	  "relayfee"             // (numeric)          minimum relay fee for non-free transactions in ZEC/kB
	  "errors"               // (string)           any error messages
	}

Examples:

::

  command:

	komodo-cli getinfo

  response:

  {
    "version": 1001550,
    "protocolversion": 170003,
    "KMDversion": "0.2.0",
    "notarized": 0,
    "prevMoMheight": 0,
    "notarizedhash": "0000000000000000000000000000000000000000000000000000000000000000",
    "notarizedtxid": "0000000000000000000000000000000000000000000000000000000000000000",
    "notarizedtxid_height": "mempool",
    "KMDnotarized_height": 0,
    "notarized_confirms": 0,
    "walletversion": 60000,
    "balance": 10.16429765,
    "blocks": 459,
    "longestchain": 0,
    "timeoffset": 0,
    "tiptime": 1536624090,
    "connections": 0,
    "proxy": "",
    "difficulty": 1.000026345948652,
    "testnet": false,
    "keypoololdest": 1536262464,
    "keypoolsize": 101,
    "paytxfee": 0.00000000,
    "relayfee": 0.00000100,
    "errors": "",
    "name": "SIDD",
    "p2pport": 9800,
    "rpcport": 9801,
    "magic": -759875707,
    "premine": 10
  }

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": {
      "version": 1001550,
      "protocolversion": 170003,
      "KMDversion": "0.2.0",
      "notarized": 0,
      "prevMoMheight": 0,
      "notarizedhash": "0000000000000000000000000000000000000000000000000000000000000000",
      "notarizedtxid": "0000000000000000000000000000000000000000000000000000000000000000",
      "notarizedtxid_height": "mempool",
      "KMDnotarized_height": 0,
      "notarized_confirms": 0,
      "walletversion": 60000,
      "balance": 10.16429765,
      "blocks": 459,
      "longestchain": 0,
      "timeoffset": 0,
      "tiptime": 1536624090,
      "connections": 0,
      "proxy": "",
      "difficulty": 1.000026345948652,
      "testnet": false,
      "keypoololdest": 1536262464,
      "keypoolsize": 101,
      "paytxfee": 0,
      "relayfee": 1e-06,
      "errors": "",
      "name": "SIDD",
      "p2pport": 9800,
      "rpcport": 9801,
      "magic": -759875707,
      "premine": 10
    },
    "error": null,
    "id": "curltest"
  }

help
----

::

  help ( "command" )

List all commands, or get help for a specified command.

Arguments:

::

	"command"            // (string, optional)     the command requiring assistance

Result:

::

	"text"               // (string)               the help text

===What is this below?===

.. _komodo-api-stop:

stop
----

::

  stop

The ``stop`` method instructs the a KMD-based coin daemon to shut down.

The amount of time it takes to shut down the chain will vary depending on the chain's current state. Forcefully stopping the chain should be avoided, as it may cause a corruption in the local database. In the event of a corrupted database, the user will need to resync their blockchain.

Arguments:

::

  (none)

Result:

::

  (for the KMD coin daemon)

  "Komodo server stopping"

  (for a KMD-based coin daemon)

  "[coin name] Komodo server stopping"

Examples:

::

  command:

  komodo-cli stop

  result:

  "Komodo server stopping"

Disclosure
==========

z_getpaymentdisclosure
----------------------

::

  z_getpaymentdisclosure "transaction_id_string" "js_index_string" "output_index_string" ("message")

The ``z_getpaymentdisclosure`` method generates a payment disclosure for a given ``joinsplit`` output.

**EXPERIMENTAL FEATURE**

**WARNING**: Payment disclosure is currently DISABLED. This call always fails.

Arguments:

::

	"txid"                   // (string, required)
	"js_index"               // (string, required)
	"output_index"           // (string, required)
	"message"                // (string, optional)

Result:

::

	"paymentdisclosure"      // (string)             hex data string, with "zpd:" prefix.

Examples:

::

  command:

	komodo-cli z_getpaymentdisclosure 96f12882450429324d5f3b48630e3168220e49ab7b0f066e5c2935a6b88bb0f2 0 0 "refund"

  response:

  (currently disabled)

  command:

	curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "z_getpaymentdisclosure", "params": ["96f12882450429324d5f3b48630e3168220e49ab7b0f066e5c2935a6b88bb0f2", 0, 0, "refund"] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  (currently disabled)

z_validatepaymentdisclosure
---------------------------

::

  z_validatepaymentdisclosure "paymentdisclosure"

The ``z_validatepaymentdisclosure`` method validates a payment disclosure.

**EXPERIMENTAL FEATURE**

**WARNING**: Payment disclosure is currently DISABLED. This call always fails.

Arguments:

::

	"paymentdisclosure"        // (string, required)   hex data string, with "zpd:" prefix

Examples:

::

  command:

  komodo-cli z_validatepaymentdisclosure "zpd:706462ff004c561a0447ba2ec51184e6c204..."

  response:

  (currently disabled)

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "z_validatepaymentdisclosure", "params": ["zpd:706462ff004c561a0447ba2ec51184e6c204..."] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  (currently disabled)

Generating
==========

===Note to self: we don't really need descriptions about the primary sections.===

generate
--------

::

  generate numblocks

  **Note**: this function can only be used on a ``-regtest`` network (for testing purposes)

The ``generate`` method instructs the coin daemon to immediately mine the indicated number of blocks.

Arguments:

::

	numblocks          // (numeric)     the desired number of blocks to generate

Result:

::

	[
    blockhashes      // (array)       hashes of blocks generated
  ]

Examples:

::

  command:

	komodo-cli generate 2

  response:

  [
    "0475316d63fe48bb9d58373595cb334fc2553f65496edfb2fb17b9ed06f4c480",
    "00d29a2b7dec52baa9ab8e4264363f32b4989eef7dbb0a9932fbc11274195b5a"
  ]

getgenerate
-----------

::

  getgenerate

The ``getgenerate`` method returns a boolean value indicating the server's mining (coin-generating) status.

The default value is false.

===This section on launching -gen needs to be elsewhere...? Or combined? I think a few of these sections, including index and mining, go under control... ===

=== Put this section elsewhere: To launch the coin daemon in mining mode is set with the command line argument ``-gen`` (or ``komodo.conf`` setting gen)===

Arguments:

::

  (none)

Result:

::

	true|false             // (boolean)    indicates whether the server is set to generate coins

Examples:

::

  command:

	komodo-cli getgenerate

  response:

  false

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getgenerate", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  ===getting an error message right now===

setgenerate
-----------

::

  setgenerate generate ( genproclimit )

The ``setgenerate`` method allows the user to set the 'generate' property in the coin daemon to ``true`` or ``false``, thus turning generation (mining) on or off.

Generation is limited to 'genproclimit' processors. -1 is unlimited.

===link== * See the ``getgenerate`` call to query the current setting.

Arguments:

::

	generate               // (boolean, required)    set to true to turn on generation; set to off to turn off generation
	genproclimit           // (numeric, optional)    set the processor limit for when generation is on; use value "-1" for unlimited

Response:

::

  (none)

Examples:

::

(turn on generation with unlimited processors)

  command:

	komodo-cli setgenerate true -1

  response:

  (none)

(check the setting)

::

  command:

  komodo-cli getgenerate

  response:

  true

(turn off generation)

::

  command:

	komodo-cli setgenerate false

  reponse:

  (none)

(turning the setting on via JSON rpc)

::

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "setgenerate", "params": [true, 1] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": null,
    "error": null,
    "id": "curltest"
  }

Mining
======

getblocksubsidy
---------------

::

  getblocksubsidy height_number

The ``getblocksubsidy`` method returns the block-subsidy reward. The resulting calculation takes into account the mining slow start. This method can be used in conjunction with custom mining rewards designed by the developers of a KMD asset chain.

Arguments:

::

	height          // (numeric, optional)  the block height; if the height is not provided, the method defaults to the current height of the chain

Result:

::

	{
	  "miner"       // (numeric)             the mining reward amount in KMD.
	}

Examples:

::

  command:

	komodo-cli getblocksubsidy 100

  response:

  {
    "miner": 0.00010000
  }

::

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockubsidy", "params": [1000] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

getblocktemplate
----------------

::

  getblocktemplate ( "jsonrequestobject" )

The ``getblocktemplate`` method returns data that is necessary to construct a block.

See https://en.bitcoin.it/wiki/BIP_0022 for full specification.

If the request parameters include a ``mode`` key, that is used to explicitly select between the default 'template' request or a 'proposal'.

Arguments:

::

	"jsonrequestobject"            // (string, optional)   a json object in the following spec
	     {
	       "mode":"template"       // (string, optional)   this must be set to "template" or "omitted"
	       "capabilities":[        // (array, optional)    a list of strings
	           "support"           // (string)             client side supported features: 'longpoll', 'coinbasetxn', 'coinbasevalue', 'proposal', 'serverlist', 'workid'
	           ,...
	         ]
	     }

Result:

::

	{
	  "version"                        // (numeric)          the block version
	  "previousblockhash"              // (string)           the hash of current highest block
	  "transactions" : [               // (array)            contents of non-coinbase transactions that should be included in the next block
	      {
	         "data"                    // (string)           transaction data encoded in hexadecimal (byte-for-byte)
	         "hash"                    // (string)           hash/id encoded in little-endian hexadecimal
	         "depends" : [             // (array)            array of numbers
	             number                // (numeric)          transactions before this one (by 1-based index in 'transactions' list) that must be present in the final block if this one is
	             ,...
	         ],
	         "fee"                     // (numeric)          difference in value between transaction inputs and outputs (in Satoshis); for coinbase transactions, this is a negative Number of the total collected block fees (ie, not including the block subsidy); if key is not present, fee is unknown and clients MUST NOT assume there isn't one
	         "sigops"                  // (numeric)          total number of SigOps, as counted for purposes of block limits; if key is not present, sigop count is unknown and clients MUST NOT assume there aren't any
	         "required"                // (boolean)          if provided and true, this transaction must be in the final block
	      }
	      ,...
	  ],
	  "coinbasetxn" : {
      ...                            // (json object)      information for coinbase transaction
     },
	  "target"                         // (string)           the hash target
	  "mintime"                        // (numeric)          the minimum timestamp appropriate for next block time in seconds since epoch (Jan 1 1970 GMT)
	  "mutable" : [                    // (array of string)  list of ways the block template may be changed
	     "value"                       // (string)           a way the block template may be changed, e.g. 'time', 'transactions', 'prevblock'
	     ,...
	  ],
	  "noncerange"                     // (string)           a range of valid nonces
	  "sigoplimit"                     // (numeric)          limit of sigops in blocks
	  "sizelimit"                      // (numeric)          limit of block size
	  "curtime"                        // (numeric)          current timestamp in seconds since epoch (Jan 1 1970 GMT)
	  "bits"                           // (string)           compressed target of next block
	  "height"                         // (numeric)          the height of the next block
	}

Examples:

::

  command:

	komodo-cli getblocktemplate '{"mode":"template","capabilities":["workid"]}'

  response:

  {
    "capabilities": [
      "proposal"
    ],
    "version": 4,
    "previousblockhash": "0ec57dbbaa7fdb290b847981e38908482b1be05f375f021c4d1f6f6315fd5c7e",
    "transactions": [
    ],
    "coinbasetxn": {
      "data": "01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff0503d7590f00ffffffff0100a3e111000000002321029400ae04d9c0e3e49b114fc5e0a7e250ece5f5b5b8f1614075ddfd62c67319aeac1ba2985b",
      "hash": "6af34ca0711ff5c7d3b4d2334ec55f4995014261f3c537446537169f9b96b0d6",
      "depends": [
      ],
      "fee": 0,
      "sigops": 1,
      "coinbasevalue": 300000000,
      "required": true
    },
    "longpollid": "0ec57dbbaa7fdb290b847981e38908482b1be05f375f021c4d1f6f6315fd5c7e39",
    "target": "000000070be50000000000000000000000000000000000000000000000000000",
    "mintime": 1536729153,
    "mutable": [
      "time",
      "transactions",
      "prevblock"
    ],
    "noncerange": "00000000ffffffff",
    "sigoplimit": 20000,
    "sizelimit": 2000000,
    "curtime": 1536729628,
    "bits": "1d070be5",
    "height": 1006039
  }

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblocktemplate", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": {
      "capabilities": [
        "proposal"
      ],
      "version": 4,
      "previousblockhash": "0c77fb62dcabffd39c0b4ad79da9a51ecc4265158b01ae09d7fd70f93ab7d499",
      "transactions": [
        {
          "data": "010000000d0bf48c25bbb9e5c9cf2959c39ea62266784932a17a8fe1ad190197c398e341870200000048473044022071db2fad2d5bab5f6cf8e2d415fe9cfbc146fc561ce55c379044d5eab7206e1b0220296970cf0265e28a49ac525faef6114386d2ed5c8ea2ced9ccfcd37ca4563bf401ffffffff50aca334345c7b4e7285d883d58efeb74c43e58d4fa61bac21f922a014f292aa1700000048473044022038f17fe42006a3f30ff658f0c8b1495567ffd0dbbe4ba36229df4bcabce201740220516ed6fca4a453f3305b47315d5efd2b230b3a575cb506cb04c89a730a62eade01ffffffff73e2bd82aa10c0bf751d7eabff50209e46827294c2b77932a096f89f7a4aa631210000004847304402200d7f4c2b8a537c98e19f0044d97c0d5ee6afb598d9b4523d586ec39b5be68ed0022071c5587f347bf56b0d1a340e6326c1ec612ee6a77abf5a24e93a446eeaee31af01ffffffffc335b0a285d04766b560bec88c191ed4494bb7e6e964eba1f5ccde3a89ad2e5a0100000049483045022100dce3c8e92b1487bb39681e58634f6414df14bf848b4a0de3ce11e2ddd4b5836202201e8ce810a67fb84350c62e3c5ed28bc1350d754f3a61a3c1a85e824c946fb30801ffffffff2ed2a51a1f8fe7feb456fa21c4ae172733d921c933e0ddc1368cfd9e09a746e5030000004847304402204f2c0eee23e34937b624e8ec4f0221ad3a43787fdbaa5b936ac39d2a3d30d7fe02200fd6e39b0eac4cbd80601f9625b40152e3bad6115f4d1e158b8709aa215778fb01ffffffff31b2c613750303538593437354af923637ee972932d1997fc93bf8d9199ebe905c000000494830450221008c760aef6b34d79e7076b6c249506c91070931f641039f44243e6abf798c731d02203c9a44d0adb04e64956720b4a97b49944825fa704679c21b18679a63c98e99ec01ffffffff0a81b4834feaa5f1044540928290e6d19667ede024923836d94bac13c7c9237914000000494830450221009d8ceb46e48dc0e86e13b0a549efbedc95ca199e1068f8e5e1f31cf4460dee3f022005079476092ac474c42ffae9fcf49fba82f68c94637ea97add61a5b1a147badb01ffffffffd81465cb221c3374a0a69bffc9f2bc225249328c50badd8683c351b2c30fdb171700000048473044022039da2916a77777c77b1a97840d1a888f2b12f0994ad134c8075a0b659884211a022006cbb6c807d1814b88f280e0036306e6d73cc79c0b6ff60966f47161feaccb3e01ffffffff59128ea85b2240d8b781a00b1ad0ebcdd8502d8d3f5722878f963b7f601e1d69020000004847304402203374d06656f35edf5d1b0d16455da2d6f22520a00c948a9c1d6bf51dba7a70ef0220529ec3146e080a637118b891a6b739f58e6f57d2aa3a24759a39eb6696af36ac01ffffffffc7d79714f379e9de8d752861f27d7e4685137dc6db5ad2cd50ec7b36429826d7050000004847304402207a426bb189ac657a9e8b699c67091de8df28306ce67b14653aea561800dfcb1502207e00216a6ff84e3f5b6d82c0683d8ea72a9fd6f636f9b3102b657e09a5f7481501ffffffffd872945ebfef211230ad8147f994892ab45c6cb4710ac29950e40354e1861d78e300000049483045022100af153b219376ffcbef42bd900e678d2504a6acd7c2bf945dcae895a9f07da79702201615016f196ad9452755d9c303fa151c242ed963b5373d148db733482487e8af01ffffffff671edc29af69a848081dd3790afb3fb113377d995e34ea9f219331d5c18c6885ad000000484730440220572ad6110ca5bafd749cfb77740f1aaac35e18c4a814cfb771c5286dd8b1249802207f4a27b90ff91663ee8ec6fc14dae64d16274fd2e35069ac6891de0385740a9801ffffffffba4dc1b3ef20747310640e4e0337c8db570ec63fa62eeffc492098502eaa9a2e5700000049483045022100f3ac3b80a66b6f1e6f96faf15a6535b104fbba987b357732e5b45830841a0a0a02202fee1f97494b2232a32517272d49992612729f4d9f762ede8d9b06ddf294293001ffffffff02f0810100000000002321020e46e79a2a8d12b9b5d12c7a91adb4e454edfae43c0a0cb805427d2ac7613fd9ac0000000000000000506a4c4da83be8f6e61cb9837708c1a847bdd80b8b8c1e1b9067b338433ca6c663869d004c6e01004345414c00e76cb540d63746c82676637b51e4f9f894c444822844224dd840975c7652dd760e00000000000000",
          "hash": "14473b8754bf69cc365784633e1a80787d4f9f950c95c48af0c6a28983c31098",
          "depends": [],
          "fee": 31200,
          "sigops": 1
        }
      ],
      "coinbasetxn": {
        "data": "01000000010000000000000000000000000000000000000000000000000000000000000000ffffffff0503e6590f00ffffffff01a010e311000000002321029400ae04d9c0e3e49b114fc5e0a7e250ece5f5b5b8f1614075ddfd62c67319aeac57a4985b",
        "hash": "334b02c0c2fa087862f845fefbd8f6ac4b72e4aed6d024f22b7fa0aa84759006",
        "depends": [],
        "fee": -93600,
        "sigops": 1,
        "coinbasevalue": 300000000,
        "required": true
      },
      "longpollid": "0c77fb62dcabffd39c0b4ad79da9a51ecc4265158b01ae09d7fd70f93ab7d499147",
      "target": "0000000670be0000000000000000000000000000000000000000000000000000",
      "mintime": 1536729888,
      "mutable": [
        "time",
        "transactions",
        "prevblock"
      ],
      "noncerange": "00000000ffffffff",
      "sigoplimit": 20000,
      "sizelimit": 2000000,
      "curtime": 1536730200,
      "bits": "1d0670be",
      "height": 1006054
    },
    "error": null,
    "id": "curltest"
  }

getlocalsolps
-------------

  :: getlocalsolps

The ``getlocalsolps`` method returns the average local solutions per second since this node was started.

* Note: this is the same information shown on the metrics screen (if enabled)

Arguments:

::

  (none)

Result:

	"data"             // (numeric) solutions per second average

Examples:

::

  command:

	komodo-cli getlocalsolps

  response:

  0

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getlocalsolps", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": 0,
    "error": null,
    "id": "curltest"
  }

getmininginfo
-------------

::

  getmininginfo

Returns a json object containing mining-related information.

Result:

::

	{
	  "blocks"                 // (numeric)      the current block
	  "currentblocksize"       // (numeric)      the last block size
	  "currentblocktx"         // (numeric)      the last block transaction
	  "difficulty"             // (numeric)      the current difficulty
	  "errors": "..."          // (string)       current errors
	  "generate"               // (boolean)      if the generation is on or off (see ===links=== getgenerate or setgenerate calls)
	  "genproclimit"           // (numeric)      the processor limit for generation; -1 if no generation (see ===links=== getgenerate or setgenerate calls)
	  "localsolps"             // (numeric)      the average local solution rate (solutions per second) since this node was started
	  "networksolps"           // (numeric)      the estimated network solution rate (solutions per second)
	  "pooledtx": n            // (numeric)      the size of the mem pool
	  "testnet"                // (boolean)      if using testnet or not
	  "chain"                  // (string)       current network name as defined in BIP70 (main, test, regtest)
	}

Examples:

* Note: the myrpcuser, myrpcpassword, and myrpcport can be found in the coin's ``.conf`` file.

::

  command:

	komodo-cli getmininginfo

  response:

  {
    "blocks": 1007341,
    "currentblocksize": 0,
    "currentblocktx": 0,
    "difficulty": 42918151.0730477,
    "errors": "",
    "genproclimit": -1,
    "localsolps": 0,
    "networksolps": 11414148,
    "networkhashps": 11414148,
    "pooledtx": 5,
    "testnet": false,
    "chain": "main",
    "generate": false,
    "numthreads": -1
  }

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getmininginfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": {
      "blocks": 1007341,
      "currentblocksize": 0,
      "currentblocktx": 0,
      "difficulty": 42918151.0730477,
      "errors": "",
      "genproclimit": -1,
      "localsolps": 0,
      "networksolps": 11414148,
      "networkhashps": 11414148,
      "pooledtx": 11,
      "testnet": false,
      "chain": "main",
      "generate": false,
      "numthreads": -1
    },
    "error": null,
    "id": "curltest"
  }

getnetworkhashps
----------------

**DEPRECATED** Use getnetworksolps instead.

::

  getnetworkhashps ( blocks height )

The ``getnetworkhashps`` method returns the estimated network solutions per second based on the last ``n`` blocks.

Pass in ``blocks]`` value to override the default # of blocks. Passing in ``-1`` will return a value based on the average hashps of the relevant difficulty window.
Pass in ``height`` to estimate the network speed at the time when a certain block was found.

Arguments:

::

	blocks           // (numeric, optional, default=120)   the number of blocks (use -1 to calculate over the relevant difficulty averaging window)
	height           // (numeric, optional, default=-1)    to estimate at the time of the given height

Result:

::

	data             // (numeric)                          solutions per second estimated

Examples:

::


  command:

  komodo-cli getnetworkhashps

  response:

  10724120

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getnetworkhashps", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": 10449287,
    "error": null,
    "id": "curltest"
  }

getnetworksolps
---------------

::

  getnetworksolps ( blocks height )

The ``getnetworksolps`` method returns the estimated network solutions per second based on the last ``n`` blocks.

Pass in ``blocks`` to override the default number of blocks. Use -1 to calculate according to the relevant difficulty averaging window.
Pass in ``height`` to estimate the network speed at the time when a certain block was found.

Arguments:

::

	blocks           // (numeric, optional, default=120)     the number of blocks; use -1 to calculate according to the relevant difficulty averaging window
	height           // (numeric, optional, default=-1)      to estimate at the time of the given height

Result:

::

	data             // (numeric)                            solutions per second estimated

Examples:

::

  command:

  komodo-cli getnetworksolps

  response:

  9954190

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getnetworksolps", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

prioritisetransaction
---------------------

::

  prioritisetransaction txid priority_delta_number fee_delta_number

The ``prioritisetransaction`` method instructs the daemon to accept the indicated transaction into mined blocks at a higher (or lower) priority. The transaction selection algorithm considers the transaction as it would have a higher priority.

* Note: This method is inherited from the original Bitcoin protocol, of which KMD is a fork (via Zcash). For more information and examples, please see the link to Bitcoin API documentation provided above.

Arguments:

::

	"transaction_id"                 // (string, required)     the transaction id
	priority delta                   // (numeric, required)    the priority to add or subtract

	fee delta                        // (numeric, required)    the fee value (in satoshis) to add (or subtract, if negative).

Result:

::

	true                             // (boolean)              returns true

Examples:


::

  command:

  komodo-cli prioritisetransaction "txid" 0.0 10000

  result:

  true

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "prioritisetransaction", "params": ["txid", 0.0, 10000] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  result:

  {
    "result": true,
    "error": null,
    "id": "curltest"
  }

submitblock
-----------

::

  submitblock "hexdata" ( "jsonparametersobject" )

The ``submitblock`` method instructs the daemon to propose a new block to the network.

The 'jsonparametersobject' parameter is currently ignored. See https://en.bitcoin.it/wiki/BIP_0022 for full specification.

Arguments:

::

	"hexdata"                    // (string, required)               the hex-encoded block data to submit
	"jsonparametersobject"       // (string, optional)               object of optional parameters

::

	    {
	      "workid"               // (string, sometimes optional)     if the server provides a workid, it MUST be included with submissions
	    }

Result:

::

	"duplicate"                    // node already has valid copy of block
	"duplicate-invalid"            // node already has block, but it is invalid
	"duplicate-inconclusive"       // node already has block but has not validated it
	"inconclusive"                 // node has not validated the block, it may not be on the node's current best chain
	"rejected"                     // block was rejected as invalid

For more information on ``submitblock`` parameters and results, see: https://github.com/bitcoin/bips/blob/master/bip-0022.mediawiki#block-submission

Examples:

::

  command:

	komodo-cli submitblock "mydata"

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "submitblock", "params": ["mydata"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

Network
=======

addnode
-------

::

  addnode "node" "add|remove|onetry"

The ``addnode`` method attempts to add or remove a node from the addnode list, or to make a single attempt to connect to a node.

Arguments:

::

	"node"                 // (string, required)     the node (see getpeerinfo for nodes)
	"command"              // (string, required)     'add' to add a node to the list, 'remove' to remove a node from the list, 'onetry' to try a connection to the node once

Result:

::

  (none)

Examples:

::

  command:

	komodo-cli addnode "192.168.0.6:8233" "onetry"

  response:

  (none)

::

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "addnode", "params": ["192.168.0.6:8233", "onetry"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  (none)

clearbanned
-----------

::

  clearbanned

The ``clearbanned`` method clears all banned IPs.

Arguments:

::

  (none)

Results:

::

  (none)

Examples:

::

  command:

	komodo-cli clearbanned

  response:

  (none)

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "clearbanned", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  (none)

disconnectnode
--------------

::

  disconnectnode "node"

The ``disconnectnode`` method instructs the daemon to immediately disconnect from the specified node.

Use ``getpeerinfo`` to determine method result.

Arguments:

::

	"node"             // (string, required)     the node's address (see getpeerinfo for nodes)

Response:

::

  (none)

Examples:

::

	command:

  komodo-cli disconnectnode "192.168.0.6:8233"

  response:

  (none - see "getpeerinfo" to determine connection status)

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "disconnectnode", "params": ["192.168.0.6:8233"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  (none - see "getpeerinfo" to determine connection status)

getaddednodeinfo
----------------

::

  getaddednodeinfo dns ( "node" )

The ``getaddednodeinfo`` method returns information about the given added node, or all added nodes

If ``dns`` is set to ``false``, only a list of added nodes is returned. Otherwise, connection information is also be provided.

* Note: ``onetry`` addnodes are not listed here.

Arguments:

::

	dns                      // (boolean, required)    if false, only a list of added nodes will be provided; otherwise, connection information is also provided
	"node"                   // (string, optional)     if provided, the method returns information about this specific node; otherwise, all nodes are returned

Result:

::

	[
	  {
	    "addednode"          // (string)               the node ip address
	    "connected"          // (boolean)              if connected
	    "addresses" : [
	       {
	         "address"       // (string)               the KMD server host and port
	         "connected"     // (string)               "connected" accepts two possible values: "inbound" or "outbound"
	       }
	       ,...
	     ]
	  }
	  ,...
	]

Examples:

::

  command:

	komodo-cli getaddednodeinfo true

  response:

  [
    {
      "addednode": "78.47.196.146",
      "connected": true,
      "addresses": [
        {
          "address": "78.47.196.146:7770",
          "connected": "outbound"
        }
      ]
    }
  ]

::

  command:

  komodo-cli getaddednodeinfo true "78.47.205.239"

  response:

  [
    {
      "addednode": "78.47.205.239",
      "connected": true,
      "addresses": [
        {
          "address": "78.47.205.239:7770",
          "connected": "outbound"
        }
      ]
    }
  ]

::

  command:

  curl --user userb4911b4842afadc2:68c3394f2b2ee55fddeb8e8e2c3fd372 --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddednodeinfo", "params": [true, "78.47.205.239"] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  response:

  {
    "result": [
      {
        "addednode": "78.47.205.239",
        "connected": true,
        "addresses": [
          {
            "address": "78.47.205.239:7770",
            "connected": "outbound"
          }
        ]
      }
    ],
    "error": null,
    "id": "curltest"
  }

getconnectioncount
------------------

::

  getconnectioncount

The ``getconnectioncount`` method returns the number of connections to other nodes.

Arguments:

  (none)

Result:

::

	n              // (numeric)    the connection count

Examples:

::

  command:

	komodo-cli getconnectioncount

  response:

  10

::

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getconnectioncount", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": 10,
    "error": null,
    "id": "curltest"
  }

getdeprecationinfo
------------------

::

  getdeprecationinfo

The ``getdeprecationinfo`` method returns an object containing current version and deprecation block height.

 * Note: This method is applicable only to the KMD mainnet.

Arguments:

  (none)

Result:

::

	{
	  "version"              // (numeric)    the server version
	  "subversion"           // (string)     the server sub-version string (i.e. "/MagicBean:x.y.z[-v]/")
	  "deprecationheight"    // (numeric)    the block height at which this version will deprecate and shut down (unless ===link?=== -disabledeprecation is set)
	}

Examples:

::

  command:

	komodo-cli getdeprecationinfo

  response:

  {
    "version": 1001550,
    "subversion": "/MagicBean:1.0.15/",
    "deprecationheight": 1400000
  }

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getdeprecationinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": {
      "version": 1001550,
      "subversion": "/MagicBean:1.0.15/",
      "deprecationheight": 1400000
    },
    "error": null,
    "id": "curltest"
  }

getnettotals
------------

::

  getnettotals

The ``getnettotals`` method returns information about network traffic, including bytes in, bytes out,
and current time.

Arguments:

  (none)

Result:

::

	{
	  "totalbytesrecv"         // (numeric)      total bytes received
	  "totalbytessent"         // (numeric)      total bytes sent
	  "timemillis"             // (numeric)      total cpu time
	}

Examples:

::

  command:

	komodo-cli getnettotals

  response:

  {
    "totalbytesrecv": 29853501,
    "totalbytessent": 15589555,
    "timemillis": 1536821874559
  }

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getnettotals", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": {
      "totalbytesrecv": 29872297,
      "totalbytessent": 15650741,
      "timemillis": 1536821938902
    },
    "error": null,
    "id": "curltest"
  }

getnetworkinfo
--------------

::

  getnetworkinfo

The ``getnetworkinfo`` method returns an object containing various state info regarding P2P networking.

Arguments:

::

  (none)

Result:

::

	{
	  "version"                // (numeric)    the server version
	  "subversion"             // (string)     the server subversion string (i.e. "/MagicBean:x.y.z[-v]/")
	  "protocolversion"        // (numeric)    the protocol version
	  "localservices"          // (string)     the services we offer to the network
	  "timeoffset"             // (numeric)    the time offset
	  "connections"            // (numeric)    the number of connections
	  "networks": [            // (array)      information per network
	  {
	    "name"                 // (string)     network (ipv4, ipv6 or onion)
	    "limited"              // (boolean)    is the network limited using -onlynet?
	    "reachable"            // (boolean)    is the network reachable?
	    "proxy"                // (string)     (submitted as "host:port") the proxy that is used for this network, or empty if none
	  }
	  ,...
	  ],
	  "relayfee"               // (numeric)    minimum relay fee for non-free transactions in ZEC/kB
	  "localaddresses": [      // (array)      list of local addresses
	  {
	    "address"              // (string)     network address
	    "port"                 // (numeric)    network port
	    "score"                // (numeric)    relative score
	  }
	  ,...
	  ]
	  "warnings"               // (string)     any network warnings (such as alert messages)
	}

Examples:

::

  command:

	komodo-cli getnetworkinfo

  response:

  {
    "version": 1001550,
    "subversion": "/MagicBean:1.0.15/",
    "protocolversion": 170003,
    "localservices": "0000000000000001",
    "timeoffset": -1,
    "connections": 10,
    "networks": [
      {
        "name": "ipv4",
        "limited": false,
        "reachable": true,
        "proxy": "",
        "proxy_randomize_credentials": false
      },
      {
        "name": "ipv6",
        "limited": false,
        "reachable": true,
        "proxy": "",
        "proxy_randomize_credentials": false
      },
      {
        "name": "onion",
        "limited": true,
        "reachable": false,
        "proxy": "",
        "proxy_randomize_credentials": false
      }
    ],
    "relayfee": 0.00000100,
    "localaddresses": [
    ],
    "warnings": ""
  }

::

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getnetworkinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": {
      "version": 1001550,
      "subversion": "/MagicBean:1.0.15/",
      "protocolversion": 170003,
      "localservices": "0000000000000001",
      "timeoffset": -1,
      "connections": 10,
      "networks": [
        {
          "name": "ipv4",
          "limited": false,
          "reachable": true,
          "proxy": "",
          "proxy_randomize_credentials": false
        },
        {
          "name": "ipv6",
          "limited": false,
          "reachable": true,
          "proxy": "",
          "proxy_randomize_credentials": false
        },
        {
          "name": "onion",
          "limited": true,
          "reachable": false,
          "proxy": "",
          "proxy_randomize_credentials": false
        }
      ],
      "relayfee": 1e-06,
      "localaddresses": [],
      "warnings": ""
    },
    "error": null,
    "id": "curltest"
  }

getpeerinfo
-----------

::

  getpeerinfo

The ``getpeerinfo`` method returns data about each connected network node as a json array of objects.

Arguments:

  (none)

Result:

::

	[
	  {
	    "id"                       // (numeric)    peer index
	    "addr":,                   // (string)     the ip address and port of the peer ("host:port")
	    "addrlocal"                // (string)     local address ("ip:port")
	    "services"                 // (string)     the services offered
	    "lastsend"                 // (numeric)    the time in seconds since epoch (Jan 1 1970 GMT) of the last send
	    "lastrecv"                 // (numeric)    the time in seconds since epoch (Jan 1 1970 GMT) of the last receive
	    "bytessent"                // (numeric)    the total bytes sent
	    "bytesrecv"                // (numeric)    the total bytes received
	    "conntime"                 // (numeric)    the connection time in seconds since epoch (Jan 1 1970 GMT)
	    "timeoffset"               // (numeric)    the time offset in seconds
	    "pingtime"                 // (numeric)    ping time
	    "pingwait"                 // (numeric)    ping wait
	    "version"                  // (numeric)    the peer version, such as 170002
	    "subver"                   // (string)     the string version (i.e. "/MagicBean:x.y.z[-v]/")
	    "inbound"                  // (boolean)    inbound (true) or outbound (false)
	    "startingheight"           // (numeric)    the starting height (block) of the peer
	    "banscore"                 // (numeric)    the ban score
	    "synced_headers"           // (numeric)    the last header we have in common with this peer
	    "synced_blocks"            // (numeric)    the last block we have in common with this peer
	    "inflight": [
	       number,                 // (numeric)    the heights of blocks we're currently asking from this peer
	       ...
	    ]
	  }
	  ,...
	]

Examples:

::

  command:

	komodo-cli getpeerinfo

  response:

  [
    {
      "id": 1,
      "addr": "78.47.196.146:7770",
      "addrlocal": "69.178.104.172:49724",
      "services": "0000000000000001",
      "lastsend": 1536827621,
      "lastrecv": 1536827617,
      "bytessent": 5181633,
      "bytesrecv": 6245958,
      "conntime": 1536792412,
      "timeoffset": -2,
      "pingtime": 0.234065,
      "version": 170003,
      "subver": "/MagicBean:1.0.15/",
      "inbound": false,
      "startingheight": 1007074,
      "banscore": 45,
      "synced_headers": 1007671,
      "synced_blocks": 1007671,
      "inflight": [
      ],
      "whitelisted": false
    }
  ]

::

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getpeerinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": [
      {
        "id": 1,
        "addr": "78.47.196.146:7770",
        "addrlocal": "69.178.104.172:49724",
        "services": "0000000000000001",
        "lastsend": 1536827702,
        "lastrecv": 1536827698,
        "bytessent": 5195639,
        "bytesrecv": 6247781,
        "conntime": 1536792412,
        "timeoffset": -2,
        "pingtime": 0.234605,
        "version": 170003,
        "subver": "/MagicBean:1.0.15/",
        "inbound": false,
        "startingheight": 1007074,
        "banscore": 45,
        "synced_headers": 1007672,
        "synced_blocks": 1007672,
        "inflight": [],
        "whitelisted": false
      }
    ],
    "error": null,
    "id": "curltest"
  }

listbanned
----------

::

  listbanned

The ``listbanned`` method lists all banned IP addresses and subnets.

Arguments:

  (none)

Results:

  [
    {
      "address"           // (string)   the address/subnet that is banned
      "banned_until"      // (numeric)  the timestamp, at which point the ban will be removed
    },
     ...
  ]

Examples:

::

1.

	komodo-cli listbanned


  [
    {
      "address": "78.47.205.239/255.255.255.255",
      "banned_until": 1536945306
    }
  ]

2.

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listbanned", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  {
    "result": [
      {
        "address": "78.47.205.239/255.255.255.255",
        "banned_until": 1536945306
      }
    ],
    "error": null,
    "id": "curltest"
  }

ping
----

::

  ping

The ``ping`` method requests that a ping be sent to all other nodes, to measure ping time.

Results provided in getpeerinfo, pingtime and pingwait fields are decimal seconds.
Ping command is handled in queue with all other commands, so it measures processing backlog, not just network ping.

Arguments:

::

  (none)

Results:

::

  (none - use ===link=== ``getpeerinfo`` for )

Examples:

::

  command:

	komodo-cli ping

  response:

  (none)

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "ping", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": null,
    "error": null,
    "id": "curltest"
  }

setban "ip(/netmask)" "add|remove" (bantime) (absolute)
-------------------------------------------------------

The ``setban`` method attempts to add or remove an IP address (and subnet, if indicated) from the banned list.

Arguments:

::

	1. "ip(/netmask)" (string, ip required) the IP/subnet (see ===link===getpeerinfo for nodes ip) with an optional netmask (default is /32 = single ip)
	2. "command"      (string, required) 'add' to add an IP/subnet to the list, 'remove' to remove an IP/subnet from the list
	3. bantime      (numeric, optional) indicates how long (in seconds) the ip is banned (or until when, if [absolute] is set) (0 or empty means using the default time of 24h, which can also be overwritten using the ===do we need to make this -bantime its own method somewhere?=== -bantime startup argument)
	4. absolute     (boolean, optional) if set to true, the bantime must be an absolute timestamp (in seconds) since epoch (Jan 1 1970 GMT)

Examples:

  command:

	komodo-cli setban "192.168.0.6" "add" 86400

  response:

  (none - use the ===link=== ``listbanned`` method to view the results)

::

  command:

  komodo-cli setban "192.168.0.0/24" "add"

  response:

  (none - use the ===link=== ``listbanned`` method to view the results)

  curl --user userb4911b4842afadc2:68c3394f2b2ee55fddeb8e8e2c3fd372 --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "setban", "params": ["78.47.205.239", "add", 86400] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

Rawtransactions
===============

createrawtransaction '[{"txid": "id_string", "vout": number},...]' '{"address":amount,...}'
------------------------------------------------------------------------

The ``createrawtransaction`` method creates a transaction, spending the given inputs and sending to the given addresses. The method returns a hex-encoded raw transaction.

* Note: This is a raw transaction, and therefore the inputs are not signed and the transaction is not stored in the wallet nor transmitted to the network.

Arguments:

::

	"transactions"              (string, required) a json array of json objects
    [
       {
         "txid"     (string, required) the transaction id
         "vout"               (numeric, required) the output number
       }
         ,...
    ]
	"addresses"                 (string, required) a json object with addresses as keys and amounts as values
    {
      "address"               (numeric, required) the key is the KMD or asset-chain address, the value is the COIN amount
      ,...
    }

Result:

::

	"transaction"                (string) a hex string of the transaction

Examples:

::

  command:

	komodo-cli createrawtransaction '[{"txid":"9f44dc664882198b14e9a8c466d466efcdd070ccb6f57be8e2884aa11e7b2a30","vout":0}]' '{"RHCXHfXCZQpbUbihNHh5gTwfr7NXmJXmHi":0.01}'

  response:

  0100000001302a7b1ea14a88e2e87bf5b6cc70d0cdef66d466c4a8e9148b19824866dc449f0000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000

::

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "createrawtransaction", "params": [[{"txid":"9f44dc664882198b14e9a8c466d466efcdd070ccb6f57be8e2884aa11e7b2a30","vout":0}], {"RHCXHfXCZQpbUbihNHh5gTwfr7NXmJXmHi":0.01} ]}' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  {
    "result": "0100000001302a7b1ea14a88e2e87bf5b6cc70d0cdef66d466c4a8e9148b19824866dc449f0000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000",
    "error": null,
    "id": "curltest"
  }

decoderawtransaction "hexstring"
--------------------------------

The ``decoderawtransaction`` method returns a JSON object representing the serialized, hex-encoded transaction.

Arguments:

::

	"hex"      (string, required)    the transaction hex string

Result:

::

	{
	  "txid"        (string) the transaction id
	  "overwintered"   (boolean) the overwintered flag
	  "version"          (numeric) the version
	  "versiongroupid"   (string, optional) the version group id (overwintered txs)
	  "locktime"        (numeric) the lock time
	  "expiryheight"     (numeric, optional) last valid block height for mining transaction (overwintered txs)
	  "vin" : [               (array of json objects)
	     {
	       "txid"    (string) the transaction id
	       "vout"         (numeric) the output number
	       "scriptSig"     (json object) the script
	         "asm"  (string) asm
	         "hex"   (string) hex
	       },
	       "sequence"     (numeric) the script sequence number
	     }
	     ,...
	  ],
	  "vout" : [             (array of json objects)
	     {
	       "value"            (numeric) The value in KMD or the asset chain's COIN
	       "number"                    (numeric) index
	       "scriptPubKey" : {          (json object)
	         "asm"          (string) the asm
	         "hex"          (string) the hex
	         "reqSigs"            (numeric) the required sigs
	         "type"  (string) the type, eg 'pubkeyhash'
	         "addresses" : [           (json array of string)
	           "t12tvKAXCxZjSmdNbao16dKXC8tRWfcF5oc"   (string) KMD or asset chain address
	           ,...
	         ]
	       }
	     }
	     ,...
	  ],
	  "vjoinsplit" : [        (array of json objects, only for version >= 2)
	     {
	       "vpub_old"         (numeric) public input value in KMD
	       "vpub_new"         (numeric) public output value in KMD
	       "anchor"         (string) the anchor
	       "nullifiers" : [            (json array of string)
	         "hex"                     (string) input note nullifier
	         ,...
	       ],
	       "commitments" : [           (json array of string)
	         "hex"                     (string) output note commitment
	         ,...
	       ],
	       "onetimePubKey"  (string) the onetime public key used to encrypt the ciphertexts
	       "randomSeed"     (string) the random seed
	       "macs" : [                  (json array of string)
	         "hex"                     (string) input note MAC
	         ,...
	       ],
	       "proof"          (string) the zero-knowledge proof
	       "ciphertexts" : [           (json array of string)
	         "hex"                     (string) output note ciphertext
	         ,...
	       ]
	     }
	     ,...
	  ],
	}

Examples:

::

  command:

	komodo-cli decoderawtransaction "0100000001302a7b1ea14a88e2e87bf5b6cc70d0cdef66d466c4a8e9148b19824866dc449f0000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"

  response:

  {
    "txid": "bdb537d0a0588eb63e696d5f6e5cdc7bda071fe39327c680f42e8c3af6719df1",
    "size": 85,
    "version": 1,
    "locktime": 0,
    "vin": [
      {
        "txid": "9f44dc664882198b14e9a8c466d466efcdd070ccb6f57be8e2884aa11e7b2a30",
        "vout": 0,
        "scriptSig": {
          "asm": "",
          "hex": ""
        },
        "sequence": 4294967295
      }
    ],
    "vout": [
      {
        "value": 0.01000000,
        "valueSat": 1000000,
        "n": 0,
        "scriptPubKey": {
          "asm": "OP_DUP OP_HASH160 56def632e67aa11c25ac16a0ee52893c2e5a2b6a OP_EQUALVERIFY OP_CHECKSIG",
          "hex": "76a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac",
          "reqSigs": 1,
          "type": "pubkeyhash",
          "addresses": [
            "RHCXHfXCZQpbUbihNHh5gTwfr7NXmJXmHi"
          ]
        }
      }
    ],
    "vjoinsplit": [
    ]
  }

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "decoderawtransaction", "params": ["0100000001302a7b1ea14a88e2e87bf5b6cc70d0cdef66d466c4a8e9148b19824866dc449f0000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  {
    "result": {
      "txid": "bdb537d0a0588eb63e696d5f6e5cdc7bda071fe39327c680f42e8c3af6719df1",
      "size": 85,
      "version": 1,
      "locktime": 0,
      "vin": [
        {
          "txid": "9f44dc664882198b14e9a8c466d466efcdd070ccb6f57be8e2884aa11e7b2a30",
          "vout": 0,
          "scriptSig": {
            "asm": "",
            "hex": ""
          },
          "sequence": 4294967295
        }
      ],
      "vout": [
        {
          "value": 0.01,
          "valueSat": 1000000,
          "n": 0,
          "scriptPubKey": {
            "asm": "OP_DUP OP_HASH160 56def632e67aa11c25ac16a0ee52893c2e5a2b6a OP_EQUALVERIFY OP_CHECKSIG",
            "hex": "76a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac",
            "reqSigs": 1,
            "type": "pubkeyhash",
            "addresses": [
              "RHCXHfXCZQpbUbihNHh5gTwfr7NXmJXmHi"
            ]
          }
        }
      ],
      "vjoinsplit": []
    },
    "error": null,
    "id": "curltest"
  }

decodescript "hex"
------------------

Decode a hex-encoded script.

Arguments:

::

	"hex"     (string) the hex encoded script

Result:

::

	{
	  "asm"   (string) script public key
	  "hex"   (string) hex encoded public key
	  "type" (string) the output type
	  "reqSigs"    (numeric) the required signatures
	  "addresses": [
	     "address"     (string) KMD address
	     ,...
	  ],
	  "p2sh":"address" (string) script address
	}

Examples:

::

  command:

  komodo-cli decodescript "0100000001302a7b1ea14a88e2e87bf5b6cc70d0cdef66d466c4a8e9148b19824866dc449f0000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"

  response:

  {
    "asm": "0 0 0 48 7b1ea14a88e2e87bf5b6cc70d0cdef66d466c4a8e9148b19824866dc449f0000000000ffffffff014042 00000000001976a91456def632e67a OP_LESSTHANOREQUAL [error]",
    "type": "nonstandard",
    "p2sh": "bQXGP7b2uRaWbMGkLaJat9LisWr8ZMGLbs"
  }

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "decodescript", "params": ["0100000001302a7b1ea14a88e2e87bf5b6cc70d0cdef66d466c4a8e9148b19824866dc449f0000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  {
    "result": {
      "asm": "0 0 0 48 7b1ea14a88e2e87bf5b6cc70d0cdef66d466c4a8e9148b19824866dc449f0000000000ffffffff014042 00000000001976a91456def632e67a OP_LESSTHANOREQUAL [error]",
      "type": "nonstandard",
      "p2sh": "bQXGP7b2uRaWbMGkLaJat9LisWr8ZMGLbs"
    },
    "error": null,
    "id": "curltest"
  }

fundrawtransaction "hexstring"
------------------------------

The ``fundrawtransaction`` method adds inputs to a transaction until it has enough ``in`` value to meet its ``out`` value. This will not modify existing inputs, and will add one ``change`` output to the outputs.

* Note: Inputs which were signed may need to be resigned after completion since in/outputs have been added. To sign the inputs added, use ``signrawtransaction``.

* Note: This method comes from the BTC codebase, of which KMD is ultimately a fork (via Zcash). For full details, please see https://bitcoin.org/en/developer-reference#fundrawtransaction

Arguments:

::

	"hexstring"    (string, required) The hex string of the raw transaction

Result:

::

	{
	  "hex"  (string)  the resulting raw transaction (hex-encoded string)
	  "fee"          (numeric) the fee added to the transaction
	  "changepos":       (numeric) the position of the added change output, or -1
	}
	"hex"

Examples:

Create a transaction with no inputs

::

  command:

	komodo-cli createrawtransaction "[]" '{"RHCXHfXCZQpbUbihNHh5gTwfr7NXmJXmHi":0.01}'

  response:

  01000000000140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000

Add sufficient unsigned inputs to meet the output value

::

  command:

	komodo-cli fundrawtransaction "rawtransactionhex"

  response:

  {
    "hex": "01000000660aeb1fef3f0f6e8e9598a2f4b434466b5ccb95e49aa7c4286bc5392d43fa1f280000000000feffffff0d204965060600f1e79bfd183e7ee1b5b9b61c6379d6c95984cb7cdf79231c4c0000000000feffffff0d3eba8ce5b6b6ee7d2e804be57dbe4544d7b7169caf5afd6f207c1275e8977e0000000000feffffff04f8b24c1eb3aeb01cc483a5b6922eb341da17fd42c944b0bb18998c04fea67e0000000000feffffff0360b074597abb6e32c319078ea5f83cdfc85d5c892c0388893d8b66876c077b0000000000feffffff0e2ae757c446029f5dbea36926883744a2d3fe8ee05381c2b4311e7d58057fd40000000000feffffff149c5bbedff321a7810d5db264829ffa5529a4f29ca3a452b0543736339bf0260000000000feffffff1f9e6624bb5185f0b51d36a3a94982f0d8a325bdf81db90bf67945354a6f40c60000000000feffffff22e752f465434c0563a7e0b9d104b8633bdbd6073bbe61d17dee0d53ac8220430000000000feffffff2780816ab4fd0177dfff1a98b7783bbefe8d08f339c964d2438b7e73c8ce614c0000000000feffffff2da12ef31d8678120d4961c9090035ae9e8f48dcfe4e2f461fb10437473c2bc90000000000feffffff39a00efcf7f678ecf0252ee2b4998a43121aaad28abe518be06a830fd34ae24e0000000000feffffff3c5b78d98b3edf510b003cc5723270854313d51ad40859ba08a622f3a269a6690000000000feffffff3ca10423750150708e817fe0020a7fd0a687a0456158db659af112dfefefa2990000000000feffffff4005c2dd439c35e3f04384142b66871e15a72149218d66be2ca3b13f7e1604b00000000000feffffff408d53f3499c6db833b4a9b19aa8cf61c95182775a0539efef9c62a0456520c40000000000feffffff43671a7bd5f31ee1642842027378035d73b06d446fbb1666e95638eb0d55d1c90000000000feffffff45ee4a5c7a98f315d26c1020b26576500ecae4d6a6a78b3ad169788006e7c76c0000000000feffffff48244290df0dccc781e7d081c731081c2e7e022176cc7b4b31fd92c1e31d970e0000000000feffffff48c28c27f8303266e0547b8c453b9823baed7a9e06105c09ba4cf65cb2bd5d2b0000000000feffffff4b28d567f5933d5992559fb19f90115b145db32bd1b6e52d309021da8e6063cc0000000000feffffff4d45006be4acc1bf5c69722cb744b967e615d2d35014fc82cf61c2a4905717a50000000000feffffff4d8540fa9e580b140359e0a17aac6415ca80072f9ba26fc2b43914092f4702400000000000feffffff4ff26de89311f83d65a3936e06937f30a75dd50594246d910035bcbe19c0ea6a0000000000feffffff511e169a83c0c0f8ee7163c34fa0e3b024275892419f11a2bb96d4976d3f9b470000000000feffffff52325adf85f74f38f467bc3a99657f322988add8aebb371bd080088efb95836f0000000000feffffff532ff452f8423507348c542063deb6f257de711237ff8d718143358128e2c6470000000000feffffff5b0d6fe54dce0515e6947f5170478cabb06d1e855365a6b7dbb0118c4450ff0b0000000000feffffff5b7db5b32a8e8e8c6307a7d0afec7062637eec39670f1afb08f0b04a50fbc4740000000000feffffff5cbecf874fd1996cd4e49cd41c98a586c533eac1ebc37df92cf5a9545203f9350000000000feffffff5d015b907e23b9c5e00907013f66d258fab2f016842f0c8e69346d72b0221dd70000000000feffffff65c461a04f571b50ab4fe3e367952bfba755eec9b6ed23cb460ab3bdc873fff80000000000feffffff686da3cbb1a1af26c2c01793345a5fb8ee47829aa907ab95b8144fbeda1707920000000000feffffff6896423421d7e1193a7b88d2fbf1eef1c46f637e7a49217c171a18852d29e8d60000000000feffffff6a0f6f77ae1d42dc96c39c620f401f32c9774f18f1a039e97b4b405b8aaa757d0000000000feffffff6cfa0bcd2e2689498496dc4b15feb0fc535667a88005f2c88198265bb1f8f3d80000000000feffffff705456a54cb0b94ec15890bd957dd778581f606270a331ad5b15ef48684a5fc40000000000feffffff718076a7dd771121e817b98e98f46c7f52722d6cdfca9130203fe5965f0a3c000000000000feffffff780ed86aeead9747bc96bf7053b02ada6ac566481763e70c29d3d00162bc7b530000000000feffffff7b3ad2352be9169286629dcf064fa769c23a8aabd468c30eec35a0c79b61f1f80000000000feffffff7fc4676bc415a467bd10d303eacd54617acfb6876945e3bf1217dfd208c6d58d0000000000feffffff80fe96eb05e5fcf89fa7e19b1a653e0b8164cba383e2d2ff5934a61c42698cb10000000000feffffff875ea454109c4725766d372f0fe395dd4744737378b3a246094dc0db7fb6e95f0000000000feffffff87b7c1fd810834fdd892975a795b9e6c1b1aa398436ae3ecb19bce62ac11aa4e0000000000feffffff88b22fca9de29db1901e9c8accbf1caf8fd4d5a37802b3bf5142038809ee3c690000000000feffffff89e4b0f44e022cf53736520aef84a324100f19f4f0862c9d2150b686e951d3740000000000feffffff8e0611807aa639621ca6be13a2eda8d98c32867041f929dbbef7742c7c867db00000000000feffffff8e77d64182b666e50377b3c9a39395735a89d2c90f5ff62024143f2c25ea51d50000000000feffffff8fe0b55ad0e150fbfe8d263c44527b967c44fd79ebbe88a09a91a4318f1c17c40000000000feffffff91ad86b51f541d480383681c4faa26575f723154ed6e39cb76e03317c8984c610000000000feffffff927673288f7c95f452e035b65c8cd46a57e58451b93dcfecfae0c33f00b4e5350000000000feffffff9477cc8e7dddfa7d183bfe0771def3778e7b2641996a3ea52f42d085d4007d190000000000feffffff948a1e5af04f265b29fd23700d1ac9926b5bed71ed5b2968f29abaa15036848c0000000000feffffff98a1cd6c74d9d42f88032e74182cfe8e71f125eb7eb1b49e8334d5b17bf4d07e0000000000feffffff9a7fefd1b1409dfc23d6be09dab5692cd9f6c59c98b2d7b0231f40b396999c2b0000000000feffffff9b0ed42c0446f8ea3c19b47be97f42d1a546bbd6a5a311cded5c1dd16c3606d40000000000feffffff9ba78bb678f5b7a289ca37b49835bc6ad383e2089dd3711833383c0c6e6d40cb0000000000feffffff9d2bdc85ec46fb0457dd41f02f5f7b203ff8c844062f3376c7f86cf2144dc6a60000000000feffffff9dc64c498135ebd6c025d7d43ae71120d6477bcbcd9828aebe21911ea21655c80000000000feffffffa0c3203666c02ea6f958408c8f2241b4d6e3a8beb9ab54736fe73621feb57ce40000000000feffffffa14e8b18777a8710e58942b56d094243151299f033cc21bb3ad3dfce2b3e77ad0000000000feffffffa262a97a28944d41d47c7f8788528c797d322f7abc0390c20bf22e3b835e127a0000000000feffffffaa3c2496b8237d865f81ff0bb8eb01bf2b69ee806463816ec83b60cace7a58330000000000feffffffabfc5cf05834234e1ee8a3c87c8de5d6a07f9530a09f2b34d9303ef30d8646cf0000000000feffffffa2d1512943366ab64e6d1749b81f993e830e5b546a87b9bd68fe0c5c865da9530100000000feffffffad976a10bc9ebe391cee6b83191520a9d0fb62a24e969477a4cc6dd26b29e4da0000000000feffffffadd486a6d94629b19713d723301b135c11af92b5ed69e6f0b9ed07d417078b240000000000feffffffb04574d6517ca90a26e07a749ebcde23f67f7ef8a594b23e699fa084529d96e80000000000feffffffb2197245ddc53b189c18d05d167210fd6291c6b9116862144c3654da5bb55d060000000000feffffffb4b953583df750085d727027674f69c6ba63513915941e42924a462d5bc15c9b0000000000feffffffb7f5149ac38efb591ad8c3a46ec9e979d5647c964190a135342435b55484dd570000000000feffffffbfc02225e0c5351bbeb63adb8e3b7859752363a5b85f5b2a6da5240a449e80650000000000feffffffc0def09bb3cbf791c52764cceadd389199be9d7603cc3d6d213ba45ffc98518d0000000000feffffffc5c9957c3a3e03204e603c313368d3c01206320beddfd28b850fd17b09a61a410000000000feffffffc64396e634d716a5ae280d9fd821507239d7b25a812eea6751254e462c8a73a50000000000feffffffc69c9cdd6825a657be1a06008f73b78cf185a9d195ba771451ca1ec09ce54d4f0000000000feffffffca6112fdc1db1a441961f6eb62b492c1397732cc5519d40f6aa335612f42d39c0000000000feffffffcb15dbc245dec1ef8cb8e25ef11921ca804c023e6ad803ebcb2a7b98380b60b30000000000feffffffcfe47e6ce0780c4594a2d1b76a2906c0a9ea32d39a73c244aa9d5d8dea67248c0000000000feffffffd0a4d502c22cea7da0d1a3cf99aef598b74fad19a6de35f21c6fd0d1b8cf27560000000000feffffffd25452b8575cafca10255179f95c8c66e255329220b7ff645af522af7b8038320000000000feffffffd3922dfd1a65216bbcd4646d0cbcfa70cfe587775cf4c673043c57061f48d7630000000000feffffffd75c777645d534009bc8e7b2c0b58a78cd63f41f47f6cd30868aeaf9b55e47700000000000feffffffd8f837530faf0d9b50efe1d79aed453b11916d565a2b9c40a380a85f0be2af6b0000000000feffffffdbce76e284668c829366dafd00ae4884ea39b2aa597cc1b4d2a37991a9b2ea560000000000feffffffe481d9493d67997104c12972b7c8a73fb87b16e228665bb784436fc0f58d7e660000000000feffffffe7a22d3d87255e4adaab9a6fd8a72320299a6902426424aa8b2b89b7c3b0c0950000000000feffffffe80ac9635b6bd91c1935eca6df80876ac8cdc87a2b91e925cfdcc0f06059b2e50000000000feffffffedad3357a1a9aeeb8c2771cc6f284db92a2aa31f458e35bb270216015bb0edd40000000000feffffffee85afefc31a99a4616bfb228e1f48691976b900ecdfe838e1310bf5b33fadcf0000000000fefffffff13e4784de0564595f3b4cce57ec0d8a4b72a798feb65f5fbca5b26a3a91d0760000000000fefffffff205212771fd3ca5a68340fa307810e44315ae02464b5d8a235ba6bca691bd710000000000fefffffff31cea9351fddc36393fa996962e204c461a34ff1c6ad243b3a4902440f165da0000000000fefffffff3c67e78777cc42ae2834bcf5dce5493fbcfcc6e0aabd7608cf4f9c936a37f490000000000fefffffff3ddc14df664f6e4f59b1f1e25241a61fc69f13125ea5a67edbd03b37d332eb50000000000fefffffff614bd5d83278ad95d8c5bf6fefe59b3675e832cc1c2349d7952aa734fd202830000000000fefffffff67ef42d75fc5d36ff32ab40f5c9f88f279a1173ee1db227a4706aa0480d66ab0000000000fefffffff69f0798ab6de485dcfe72391f4cbb1e5f4d39ee8f852b80fd4bb730eabd8e930000000000fefffffff8dd75e7c674cf7bf15f42fcb1256ef4f16b96e0ff6a359bc24c07ba734f09a30000000000fefffffffa0c47583d4c6f18e12b93764ccf57d2430a52bdd0ceb611924a79c82daf48b90000000000fefffffffa5ca0440f302bcf118946714dba6e81036e48477ff3a315084fe682aea6d1d50000000000fefffffffef369694bf0493161762e49d7ca16f1ba600250d801a848d0ca8d3f2d677d4a0000000000feffffff02c5490f00000000001976a9146843838a0aa11686cd0c01fbf470c9c5f302249488ac40420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000",
    "changepos": 0,
    "fee": 0.00011740
  }

Sign the transaction

::

	./komodo-cli signrawtransaction "01000000660aeb1fef3f0f6e8e9598a2f4b434466b5ccb95e49aa7c4286bc5392d43fa1f280000000000feffffff0d204965060600f1e79bfd183e7ee1b5b9b61c6379d6c95984cb7cdf79231c4c0000000000feffffff0d3eba8ce5b6b6ee7d2e804be57dbe4544d7b7169caf5afd6f207c1275e8977e0000000000feffffff04f8b24c1eb3aeb01cc483a5b6922eb341da17fd42c944b0bb18998c04fea67e0000000000feffffff0360b074597abb6e32c319078ea5f83cdfc85d5c892c0388893d8b66876c077b0000000000feffffff0e2ae757c446029f5dbea36926883744a2d3fe8ee05381c2b4311e7d58057fd40000000000feffffff149c5bbedff321a7810d5db264829ffa5529a4f29ca3a452b0543736339bf0260000000000feffffff1f9e6624bb5185f0b51d36a3a94982f0d8a325bdf81db90bf67945354a6f40c60000000000feffffff22e752f465434c0563a7e0b9d104b8633bdbd6073bbe61d17dee0d53ac8220430000000000feffffff2780816ab4fd0177dfff1a98b7783bbefe8d08f339c964d2438b7e73c8ce614c0000000000feffffff2da12ef31d8678120d4961c9090035ae9e8f48dcfe4e2f461fb10437473c2bc90000000000feffffff39a00efcf7f678ecf0252ee2b4998a43121aaad28abe518be06a830fd34ae24e0000000000feffffff3c5b78d98b3edf510b003cc5723270854313d51ad40859ba08a622f3a269a6690000000000feffffff3ca10423750150708e817fe0020a7fd0a687a0456158db659af112dfefefa2990000000000feffffff4005c2dd439c35e3f04384142b66871e15a72149218d66be2ca3b13f7e1604b00000000000feffffff408d53f3499c6db833b4a9b19aa8cf61c95182775a0539efef9c62a0456520c40000000000feffffff43671a7bd5f31ee1642842027378035d73b06d446fbb1666e95638eb0d55d1c90000000000feffffff45ee4a5c7a98f315d26c1020b26576500ecae4d6a6a78b3ad169788006e7c76c0000000000feffffff48244290df0dccc781e7d081c731081c2e7e022176cc7b4b31fd92c1e31d970e0000000000feffffff48c28c27f8303266e0547b8c453b9823baed7a9e06105c09ba4cf65cb2bd5d2b0000000000feffffff4b28d567f5933d5992559fb19f90115b145db32bd1b6e52d309021da8e6063cc0000000000feffffff4d45006be4acc1bf5c69722cb744b967e615d2d35014fc82cf61c2a4905717a50000000000feffffff4d8540fa9e580b140359e0a17aac6415ca80072f9ba26fc2b43914092f4702400000000000feffffff4ff26de89311f83d65a3936e06937f30a75dd50594246d910035bcbe19c0ea6a0000000000feffffff511e169a83c0c0f8ee7163c34fa0e3b024275892419f11a2bb96d4976d3f9b470000000000feffffff52325adf85f74f38f467bc3a99657f322988add8aebb371bd080088efb95836f0000000000feffffff532ff452f8423507348c542063deb6f257de711237ff8d718143358128e2c6470000000000feffffff5b0d6fe54dce0515e6947f5170478cabb06d1e855365a6b7dbb0118c4450ff0b0000000000feffffff5b7db5b32a8e8e8c6307a7d0afec7062637eec39670f1afb08f0b04a50fbc4740000000000feffffff5cbecf874fd1996cd4e49cd41c98a586c533eac1ebc37df92cf5a9545203f9350000000000feffffff5d015b907e23b9c5e00907013f66d258fab2f016842f0c8e69346d72b0221dd70000000000feffffff65c461a04f571b50ab4fe3e367952bfba755eec9b6ed23cb460ab3bdc873fff80000000000feffffff686da3cbb1a1af26c2c01793345a5fb8ee47829aa907ab95b8144fbeda1707920000000000feffffff6896423421d7e1193a7b88d2fbf1eef1c46f637e7a49217c171a18852d29e8d60000000000feffffff6a0f6f77ae1d42dc96c39c620f401f32c9774f18f1a039e97b4b405b8aaa757d0000000000feffffff6cfa0bcd2e2689498496dc4b15feb0fc535667a88005f2c88198265bb1f8f3d80000000000feffffff705456a54cb0b94ec15890bd957dd778581f606270a331ad5b15ef48684a5fc40000000000feffffff718076a7dd771121e817b98e98f46c7f52722d6cdfca9130203fe5965f0a3c000000000000feffffff780ed86aeead9747bc96bf7053b02ada6ac566481763e70c29d3d00162bc7b530000000000feffffff7b3ad2352be9169286629dcf064fa769c23a8aabd468c30eec35a0c79b61f1f80000000000feffffff7fc4676bc415a467bd10d303eacd54617acfb6876945e3bf1217dfd208c6d58d0000000000feffffff80fe96eb05e5fcf89fa7e19b1a653e0b8164cba383e2d2ff5934a61c42698cb10000000000feffffff875ea454109c4725766d372f0fe395dd4744737378b3a246094dc0db7fb6e95f0000000000feffffff87b7c1fd810834fdd892975a795b9e6c1b1aa398436ae3ecb19bce62ac11aa4e0000000000feffffff88b22fca9de29db1901e9c8accbf1caf8fd4d5a37802b3bf5142038809ee3c690000000000feffffff89e4b0f44e022cf53736520aef84a324100f19f4f0862c9d2150b686e951d3740000000000feffffff8e0611807aa639621ca6be13a2eda8d98c32867041f929dbbef7742c7c867db00000000000feffffff8e77d64182b666e50377b3c9a39395735a89d2c90f5ff62024143f2c25ea51d50000000000feffffff8fe0b55ad0e150fbfe8d263c44527b967c44fd79ebbe88a09a91a4318f1c17c40000000000feffffff91ad86b51f541d480383681c4faa26575f723154ed6e39cb76e03317c8984c610000000000feffffff927673288f7c95f452e035b65c8cd46a57e58451b93dcfecfae0c33f00b4e5350000000000feffffff9477cc8e7dddfa7d183bfe0771def3778e7b2641996a3ea52f42d085d4007d190000000000feffffff948a1e5af04f265b29fd23700d1ac9926b5bed71ed5b2968f29abaa15036848c0000000000feffffff98a1cd6c74d9d42f88032e74182cfe8e71f125eb7eb1b49e8334d5b17bf4d07e0000000000feffffff9a7fefd1b1409dfc23d6be09dab5692cd9f6c59c98b2d7b0231f40b396999c2b0000000000feffffff9b0ed42c0446f8ea3c19b47be97f42d1a546bbd6a5a311cded5c1dd16c3606d40000000000feffffff9ba78bb678f5b7a289ca37b49835bc6ad383e2089dd3711833383c0c6e6d40cb0000000000feffffff9d2bdc85ec46fb0457dd41f02f5f7b203ff8c844062f3376c7f86cf2144dc6a60000000000feffffff9dc64c498135ebd6c025d7d43ae71120d6477bcbcd9828aebe21911ea21655c80000000000feffffffa0c3203666c02ea6f958408c8f2241b4d6e3a8beb9ab54736fe73621feb57ce40000000000feffffffa14e8b18777a8710e58942b56d094243151299f033cc21bb3ad3dfce2b3e77ad0000000000feffffffa262a97a28944d41d47c7f8788528c797d322f7abc0390c20bf22e3b835e127a0000000000feffffffaa3c2496b8237d865f81ff0bb8eb01bf2b69ee806463816ec83b60cace7a58330000000000feffffffabfc5cf05834234e1ee8a3c87c8de5d6a07f9530a09f2b34d9303ef30d8646cf0000000000feffffffa2d1512943366ab64e6d1749b81f993e830e5b546a87b9bd68fe0c5c865da9530100000000feffffffad976a10bc9ebe391cee6b83191520a9d0fb62a24e969477a4cc6dd26b29e4da0000000000feffffffadd486a6d94629b19713d723301b135c11af92b5ed69e6f0b9ed07d417078b240000000000feffffffb04574d6517ca90a26e07a749ebcde23f67f7ef8a594b23e699fa084529d96e80000000000feffffffb2197245ddc53b189c18d05d167210fd6291c6b9116862144c3654da5bb55d060000000000feffffffb4b953583df750085d727027674f69c6ba63513915941e42924a462d5bc15c9b0000000000feffffffb7f5149ac38efb591ad8c3a46ec9e979d5647c964190a135342435b55484dd570000000000feffffffbfc02225e0c5351bbeb63adb8e3b7859752363a5b85f5b2a6da5240a449e80650000000000feffffffc0def09bb3cbf791c52764cceadd389199be9d7603cc3d6d213ba45ffc98518d0000000000feffffffc5c9957c3a3e03204e603c313368d3c01206320beddfd28b850fd17b09a61a410000000000feffffffc64396e634d716a5ae280d9fd821507239d7b25a812eea6751254e462c8a73a50000000000feffffffc69c9cdd6825a657be1a06008f73b78cf185a9d195ba771451ca1ec09ce54d4f0000000000feffffffca6112fdc1db1a441961f6eb62b492c1397732cc5519d40f6aa335612f42d39c0000000000feffffffcb15dbc245dec1ef8cb8e25ef11921ca804c023e6ad803ebcb2a7b98380b60b30000000000feffffffcfe47e6ce0780c4594a2d1b76a2906c0a9ea32d39a73c244aa9d5d8dea67248c0000000000feffffffd0a4d502c22cea7da0d1a3cf99aef598b74fad19a6de35f21c6fd0d1b8cf27560000000000feffffffd25452b8575cafca10255179f95c8c66e255329220b7ff645af522af7b8038320000000000feffffffd3922dfd1a65216bbcd4646d0cbcfa70cfe587775cf4c673043c57061f48d7630000000000feffffffd75c777645d534009bc8e7b2c0b58a78cd63f41f47f6cd30868aeaf9b55e47700000000000feffffffd8f837530faf0d9b50efe1d79aed453b11916d565a2b9c40a380a85f0be2af6b0000000000feffffffdbce76e284668c829366dafd00ae4884ea39b2aa597cc1b4d2a37991a9b2ea560000000000feffffffe481d9493d67997104c12972b7c8a73fb87b16e228665bb784436fc0f58d7e660000000000feffffffe7a22d3d87255e4adaab9a6fd8a72320299a6902426424aa8b2b89b7c3b0c0950000000000feffffffe80ac9635b6bd91c1935eca6df80876ac8cdc87a2b91e925cfdcc0f06059b2e50000000000feffffffedad3357a1a9aeeb8c2771cc6f284db92a2aa31f458e35bb270216015bb0edd40000000000feffffffee85afefc31a99a4616bfb228e1f48691976b900ecdfe838e1310bf5b33fadcf0000000000fefffffff13e4784de0564595f3b4cce57ec0d8a4b72a798feb65f5fbca5b26a3a91d0760000000000fefffffff205212771fd3ca5a68340fa307810e44315ae02464b5d8a235ba6bca691bd710000000000fefffffff31cea9351fddc36393fa996962e204c461a34ff1c6ad243b3a4902440f165da0000000000fefffffff3c67e78777cc42ae2834bcf5dce5493fbcfcc6e0aabd7608cf4f9c936a37f490000000000fefffffff3ddc14df664f6e4f59b1f1e25241a61fc69f13125ea5a67edbd03b37d332eb50000000000fefffffff614bd5d83278ad95d8c5bf6fefe59b3675e832cc1c2349d7952aa734fd202830000000000fefffffff67ef42d75fc5d36ff32ab40f5c9f88f279a1173ee1db227a4706aa0480d66ab0000000000fefffffff69f0798ab6de485dcfe72391f4cbb1e5f4d39ee8f852b80fd4bb730eabd8e930000000000fefffffff8dd75e7c674cf7bf15f42fcb1256ef4f16b96e0ff6a359bc24c07ba734f09a30000000000fefffffffa0c47583d4c6f18e12b93764ccf57d2430a52bdd0ceb611924a79c82daf48b90000000000fefffffffa5ca0440f302bcf118946714dba6e81036e48477ff3a315084fe682aea6d1d50000000000fefffffffef369694bf0493161762e49d7ca16f1ba600250d801a848d0ca8d3f2d677d4a0000000000feffffff02c5490f00000000001976a9146843838a0aa11686cd0c01fbf470c9c5f302249488ac40420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"

  response:

  {
    "hex": "01000000660aeb1fef3f0f6e8e9598a2f4b434466b5ccb95e49aa7c4286bc5392d43fa1f2800000000484730440220234b370cddf91b27e172cb5d6257a9807e63cf680a644229147b39d87e597875022047a58509a11b190107a9ff6e08143bd0d450db233518ed26f123bd739576e9c201feffffff0d204965060600f1e79bfd183e7ee1b5b9b61c6379d6c95984cb7cdf79231c4c000000004847304402202ffed5ef972b01ec4290343ab0bc4cff989d0047f2cbc9e8b69f0f3102824c0e02203c7e3214344e6ac430e4f996a8980e7d9172ea1e8c0c238ba32b8930f4d4119301feffffff0d3eba8ce5b6b6ee7d2e804be57dbe4544d7b7169caf5afd6f207c1275e8977e00000000484730440220096fdd062535f200897de2f2dfb7d782499dc5fc24d8e06805eebed6ec125c07022077e4379409bd7c9052608e8cd52cd83b0c9314c623d9b85012eab28e10f8c13601feffffff04f8b24c1eb3aeb01cc483a5b6922eb341da17fd42c944b0bb18998c04fea67e000000004847304402204a8f45abf51333ec7c4491cd5750e5d46785475ebdb0a13a6a946711f17483a9022075805ee9f2130c3938e273c280b6b14b27640349b537b55348c40ede1508938f01feffffff0360b074597abb6e32c319078ea5f83cdfc85d5c892c0388893d8b66876c077b000000004948304502210089c7919c6e7412a1569434f74caf7110bbb0341361384067265c142c8e033b2d02203d5eaa583d727fad487bbb689bf433bac32d907e707043e8f96f8c50fd3480d501feffffff0e2ae757c446029f5dbea36926883744a2d3fe8ee05381c2b4311e7d58057fd40000000049483045022100a0672d882511b01696192965175f3827e65ef8d45b3217b563d0f97f3cab512602205c568b5c1eda0c149976380b38d2f93ee384500bb5eecf6e9f3f2101d649eace01feffffff149c5bbedff321a7810d5db264829ffa5529a4f29ca3a452b0543736339bf0260000000049483045022100981f7f5210e17e1c73fe5083ca7b29a5b1a9dfbbf5474c109069a4b3eecbb5c5022065e21331260c718788b72902da250418b0091537a540e8f6152ae097632637da01feffffff1f9e6624bb5185f0b51d36a3a94982f0d8a325bdf81db90bf67945354a6f40c6000000004847304402204391d39a88d2f8427396bbbca508bcdb3b6897c25bee4c68d357b878419285a602205da8f54aec5bb9253aeaa9b4c4a1a8a2fe602e894422da0279f21f9799a3540201feffffff22e752f465434c0563a7e0b9d104b8633bdbd6073bbe61d17dee0d53ac8220430000000049483045022100d5a4b70ce4542e30a7cfb09ea259405ee202f99b556c88604b06a86419b2e72602202417376668f93e44b404ec2bfe6e797b699367604de296377dfc6944afce722901feffffff2780816ab4fd0177dfff1a98b7783bbefe8d08f339c964d2438b7e73c8ce614c00000000494830450221009d1878ce69f3a438748bcc73de00d531492cd36d2bf7a292bc5bbf67fcf6c774022066e1705510ed5a5177e78a71ba9891d69e11a7a3bc28599d5d18c29c2033a00e01feffffff2da12ef31d8678120d4961c9090035ae9e8f48dcfe4e2f461fb10437473c2bc90000000049483045022100fe0f6284ddb97b4595d77cf7ad5ef4f5caa67cb7c4b6e6ee9812bac076787377022032991f85e1962140673af04a85a442bca3df931ca52c365d3cf24e79b782b2d101feffffff39a00efcf7f678ecf0252ee2b4998a43121aaad28abe518be06a830fd34ae24e0000000048473044022038759690b62c95f80a54d3bde28abdf7dddae992ee4a18c511a4d442da67d758022016aa7dba3da26aa7531731222a0f66cec25c5026cc4903b51dd3fe5483af4cc401feffffff3c5b78d98b3edf510b003cc5723270854313d51ad40859ba08a622f3a269a66900000000484730440220141e545e4ea0c27a630972d474b7d95dd2c9da1a129a7e680016e4ad70c5579102207a3384d8c988bfa526bea0f7cebfb8a8d81ae4b7272d23e83268791fc8eba2bf01feffffff3ca10423750150708e817fe0020a7fd0a687a0456158db659af112dfefefa299000000004847304402205c4e4f8934cea71191f87208bbbaae36b2b3ac4f7282256cc05446cdd1ccc0980220038db0a46e2b06fd61acdf1b47a5de87b787a62a1b65db823c904efa6223129b01feffffff4005c2dd439c35e3f04384142b66871e15a72149218d66be2ca3b13f7e1604b0000000004847304402206b8854445fdb689929143c8daf33fa52ddee06c360073f6262ffea4db0b8b71102200b4d7a166bfa81e8f2570afcd9de338b9a0d7bc72a3962c775205933690f302901feffffff408d53f3499c6db833b4a9b19aa8cf61c95182775a0539efef9c62a0456520c40000000049483045022100c1f028354c1034e61d59999070a8ab554a97f81583d72f38c0f6b0b7a52fe8ab0220538d6fec3f35a595614602203b360730b2f13c3bd879fdadca06dd8a16b90b9d01feffffff43671a7bd5f31ee1642842027378035d73b06d446fbb1666e95638eb0d55d1c9000000004847304402203fc7529cc7a96726728a4aa6a1698fc31bad94d1eadda2a0f74ea8f22d752869022011983a3c457e5c7ffc87b576d877e6f02ab8e08dbda6a94dfbf245315a3365e201feffffff45ee4a5c7a98f315d26c1020b26576500ecae4d6a6a78b3ad169788006e7c76c000000004847304402207a60671e1d0cd3d5d7b8eb2a1b53a0014f30de45f0e379a30435a47e7f9861eb0220689af75a99876c1d1d206869dca223806c45ad64f32cc08cd624936ec6c0600f01feffffff48244290df0dccc781e7d081c731081c2e7e022176cc7b4b31fd92c1e31d970e000000004847304402201972bc346632bcd5166cecbd9d7ca29583c7ad938640d7db9f4bdc6629fff086022019135d7341ef96813a839c6cc14f47c7d2e42c262abbe8747e16c6869cf2b90a01feffffff48c28c27f8303266e0547b8c453b9823baed7a9e06105c09ba4cf65cb2bd5d2b000000004847304402205e40a09a37c939cfa6b5143a2ce596452ecbbd223400922b0001bda694f4c63602205aad66d989167c9bbca130aa489de6286390e55f9e9ef4c5c043c2f13377c7c701feffffff4b28d567f5933d5992559fb19f90115b145db32bd1b6e52d309021da8e6063cc0000000049483045022100ceb282925d7eac742085d5ac48443e9af8b72873fb7a2f96b4e196a58a4b29d7022074790a63adec4088a5d5c2bf1fa80597be0e17afc7490620163a873a2ef1855d01feffffff4d45006be4acc1bf5c69722cb744b967e615d2d35014fc82cf61c2a4905717a50000000049483045022100c6f42ccf0af44182e144aa925b631cab8d90959fa96eb0453335a970e74910d402205e99e1f1d23813e336a3c96efd6e75490f3b5d807f0f2bbc677499cc0b92f47a01feffffff4d8540fa9e580b140359e0a17aac6415ca80072f9ba26fc2b43914092f4702400000000049483045022100b42e72fdb23f4f50af0222d5e590bcc676d60858583dffc1ba8b35730e1c8eb102207cc50ecd38639100131b4c4950cedaac4c4ee37c7a6f87d3ed7fb7eb165559c101feffffff4ff26de89311f83d65a3936e06937f30a75dd50594246d910035bcbe19c0ea6a00000000484730440220425c41bc88fce16ba54f2611a54737d9b5197abc541c730711157b290486cdc6022003f967d0f98864249d80720c65e04c475cbc12c482104aa7e45a06bc9eb080b901feffffff511e169a83c0c0f8ee7163c34fa0e3b024275892419f11a2bb96d4976d3f9b4700000000484730440220136e776a7bfe3fdb5a5b8db2783452ed7cf1fe3c89ec001ed69455a082337e49022057e7dc0ace7ae100a2f2c26291cfe80352b34dfd9269d07468ee2dfba13fc02001feffffff52325adf85f74f38f467bc3a99657f322988add8aebb371bd080088efb95836f000000004847304402201fafc46f92d80a9b4f71a15113ae8e8182dcaa09cff63645db5b858044f329730220160082cc1a3bb262458a204040c3ecc23b276c4558ea095c1b66e20a4004e26b01feffffff532ff452f8423507348c542063deb6f257de711237ff8d718143358128e2c6470000000049483045022100d8dfe5557eae68e8b3da5cc787b14e85fb4d10d2c8a80eda12e69b807319ff9902200b104ae561f1d9c4f0c1646327686f890aed1ea8fb1c1b411f07059517737d0001feffffff5b0d6fe54dce0515e6947f5170478cabb06d1e855365a6b7dbb0118c4450ff0b000000004847304402207fad37e344180882f9cfa3e36d036282a91467ff15fca2f24278f5fa5283b99d0220325dda0a7c35a85cb617bcac369ec0033023c221771cf02f1f877f693f1059d901feffffff5b7db5b32a8e8e8c6307a7d0afec7062637eec39670f1afb08f0b04a50fbc47400000000484730440220752cc9659edbddc78293b1947f84d2bd69e32ef4d5425d4e55df4ca74a7a962402203a755152ab6d38a7ba91f26f476d611cd9c6b27167d6e20b511c4830038d102c01feffffff5cbecf874fd1996cd4e49cd41c98a586c533eac1ebc37df92cf5a9545203f935000000004847304402203af4f03cfed41a4d8387a0859324ce3c40c953582e8848867d06d3aef096deba0220104c18b2e243cf7f076d2833c4fac30e0f5e62b58bc039cba6ce7fe47ea394a101feffffff5d015b907e23b9c5e00907013f66d258fab2f016842f0c8e69346d72b0221dd70000000049483045022100bc3e1c873f25e1a661ef81c109de1758ab13df3fc591540658c5fc05bb1e8c150220309b87661ce039899d5be3b510fcdbb9464ff8cb47af06c016390d79daa7029c01feffffff65c461a04f571b50ab4fe3e367952bfba755eec9b6ed23cb460ab3bdc873fff80000000048473044022037b231fec860afbac51e3034e1308e1873d87dc586258ad8c7ede04cf0fab97e022012eceff07cf09a2c3d2f6884ee885ff9f8e7526de8c08b54e5e538ab223bb31b01feffffff686da3cbb1a1af26c2c01793345a5fb8ee47829aa907ab95b8144fbeda1707920000000049483045022100a0d89b8331105f34528f2c9687f53897a2a14f57cde1390513b4d0fda530a4200220573800bfa5cba98af2a08fa3e87fd0142fe1db6f391a4d160f70565b1078210d01feffffff6896423421d7e1193a7b88d2fbf1eef1c46f637e7a49217c171a18852d29e8d60000000049483045022100cde87af1eb614761149aef298153c541e24ff45345f99dbef18bf2379d27f347022063115fb6b37842eb7cc4d8910ccd047635a9674e72d9418894614014c19d583a01feffffff6a0f6f77ae1d42dc96c39c620f401f32c9774f18f1a039e97b4b405b8aaa757d0000000049483045022100a82d1afe573bfaf0668b3acbec55f68bcbb58bed7b806d59837c32f3560cd1d70220198904866e0bd9d19cc465cf09e256c439ad5309caffa347b8c416443ed07a0c01feffffff6cfa0bcd2e2689498496dc4b15feb0fc535667a88005f2c88198265bb1f8f3d8000000004847304402207917043acb4879438625ace42109cc1bee16054222473d2f975b3edf27286f3602207413e93cf5e696de7c0d210dfa70cd4dd9e62e78ed86a3d99682ef8ea5c064cd01feffffff705456a54cb0b94ec15890bd957dd778581f606270a331ad5b15ef48684a5fc4000000004847304402206668503174e874bc09d999d7bc47f82a5ac47c3f1bc1c43ffa1cca74c1cde4410220616df31f268371b61d83acdfd394a7bcd8da5817174faa29b51c648786c5405a01feffffff718076a7dd771121e817b98e98f46c7f52722d6cdfca9130203fe5965f0a3c00000000004847304402200f1c2ef04cf5fceacb53724360ce3af3794d14ef8a47d4d09c8e3b95b20e48770220659021ba00a68e5f2f4053ec904cc7e65b5bd5db76ff45a9be4ba35ad1a2d0a201feffffff780ed86aeead9747bc96bf7053b02ada6ac566481763e70c29d3d00162bc7b530000000048473044022027f04c7d149ed6c9c72ce3956917444cb5f943aa95adb694ec30ef53c930cfe202206dc14b5f1d59b6724fea484501e36fe7bf40849614921cf76130ec20665f35d401feffffff7b3ad2352be9169286629dcf064fa769c23a8aabd468c30eec35a0c79b61f1f80000000049483045022100c4a61d02e54b0c0b8a9749d394d6447326bf66f3524388b8854c5585ad71704702200b0e71e178082df01e66d0bb72aad0238b0063018cae190c2f21c0fbd78a462001feffffff7fc4676bc415a467bd10d303eacd54617acfb6876945e3bf1217dfd208c6d58d0000000048473044022064ab0c92b7cb2205f1d7af0a2faa441eac041cbb892b166b8f1f060019301546022066924807801b03876a0ac1830eb355ed26c7a67b9e28fcb0b3c6dc5d3c8ca1db01feffffff80fe96eb05e5fcf89fa7e19b1a653e0b8164cba383e2d2ff5934a61c42698cb100000000484730440220515b9c588036449b326ab8d74679cf65c7fe780a03b23ba8428cf829a070abd402204c71e343cfe18e166b7259509b47dcbec0b5b29a764e4dbd29a39479ef60d34601feffffff875ea454109c4725766d372f0fe395dd4744737378b3a246094dc0db7fb6e95f0000000048473044022039167229a3f6ece80aebdfb425608c855989a0e7934abe0c4fca1175f60d46b5022069f57fb057a537cd95e5ebd6a93709e0bffde3d05bd01322f08d0fecef7c061f01feffffff87b7c1fd810834fdd892975a795b9e6c1b1aa398436ae3ecb19bce62ac11aa4e0000000049483045022100ab701a93c793c182bd54f06f80de91c03e36fa9b33b220a91d028f2196d329b5022020e23cff44abe2510b50ce0a8cab286d3ae17c59d8aebd20b42613b764a128c801feffffff88b22fca9de29db1901e9c8accbf1caf8fd4d5a37802b3bf5142038809ee3c6900000000494830450221008ade6fbaec28bf02b3914ffc62c4e0dd7da3d50b41b1054653826a38573e6c13022032d2528595fad675d3f01aad532bdd5ca64960a9cdec35822bb0e69b57fb78ba01feffffff89e4b0f44e022cf53736520aef84a324100f19f4f0862c9d2150b686e951d3740000000049483045022100e69902cff246e6ae5ae8a502aaf2ecc0f8505b8546b17fef18a6e2dde8703bc60220121b6293f7c24aad7766900a746693b9e30ef4e8cc1ca01b2ed4537b47debd2f01feffffff8e0611807aa639621ca6be13a2eda8d98c32867041f929dbbef7742c7c867db000000000484730440220710257eb2b9f5e7b9517770f81c0999a7fcd5b798d8665e0674abec0909b5bad02207bcbcebecb36661cbc8793575f62524dac431fbee3f9c02fb0d854933357694001feffffff8e77d64182b666e50377b3c9a39395735a89d2c90f5ff62024143f2c25ea51d50000000049483045022100ec5f6927e57df66eefcd1275d4236f38841466cdb29aa9ed8c6f8b8f64e0cc4302200141c090ae22c294844bd0b5179f97fd4b98cee426dfb795c3288f37f67a70e401feffffff8fe0b55ad0e150fbfe8d263c44527b967c44fd79ebbe88a09a91a4318f1c17c40000000049483045022100bbaec071109be2005be905bc0b2877286f24cfdb4d8431a31c8f57d802db31270220345e56f174738a6a191ef0a91c4cdeb686dd552d8992ea6ce7517e0ff9cafad001feffffff91ad86b51f541d480383681c4faa26575f723154ed6e39cb76e03317c8984c610000000048473044022046628accc862ea34ab15232f97505cf673d8bfd23d6316677e524e3643e92a20022078414e64419c96474fe2559c30134ac4c08b5a0617a0dc9bd1ce09e85a8df89001feffffff927673288f7c95f452e035b65c8cd46a57e58451b93dcfecfae0c33f00b4e5350000000049483045022100b9e84841140ae7b9bf08f82e014247a8c270d4073b457fbee74743c413e0b4370220292fc63652cd2fae0d1baf9c705de61478b2ec8d4623b9ecaf2aca715c1e69d801feffffff9477cc8e7dddfa7d183bfe0771def3778e7b2641996a3ea52f42d085d4007d190000000048473044022073842db3431ea57cb4aa05435648817bacb36a623e2528817e399126068fbd8b02206744687cfc5587f07d6a507eeeb2aaff45731b3dd9222c40f2b62b60e4db59b301feffffff948a1e5af04f265b29fd23700d1ac9926b5bed71ed5b2968f29abaa15036848c000000004847304402207c5440b72bc608cdf4c7fad0bccdc19d43877e31b22fe3f5873f558a6068e28c022013e3a5b0b11eeec0bfd5cc8317c8a61ccf28ce19a1b50fd7759502a350b991e401feffffff98a1cd6c74d9d42f88032e74182cfe8e71f125eb7eb1b49e8334d5b17bf4d07e00000000484730440220393955bb76c236467d92d42091a290631cbcd9ef3c3f177ace6f1ce73abe319f0220153d5c0aef39f5cea8ef53822993e374dc6d66a758d599f25d2e934d8c97769601feffffff9a7fefd1b1409dfc23d6be09dab5692cd9f6c59c98b2d7b0231f40b396999c2b000000004847304402201f9d944711c3ee35c47b68ddac1a0e1f728884847d8df788b398157de22e9bbd022005d97ceca294e96f5484420189d7a99b9850ecb2c849223ddb934c6c772e32f401feffffff9b0ed42c0446f8ea3c19b47be97f42d1a546bbd6a5a311cded5c1dd16c3606d40000000049483045022100d42b4c9c6fbcbd65d69f0967cca562227f8fbab7ca2727822eb9eb4d0ce8e77a022049d752916ee19c285675786aa04c37d7025e2cef6907f70849f55cda414f3fb501feffffff9ba78bb678f5b7a289ca37b49835bc6ad383e2089dd3711833383c0c6e6d40cb000000004847304402205d3a652a05971d324947fb9d4d15e98393262498e09a6d8fdde7422af91d341a022070e017f2edf61310cb724401a451c1d2be59175e68b49e5c1f82f20084f0b2e501feffffff9d2bdc85ec46fb0457dd41f02f5f7b203ff8c844062f3376c7f86cf2144dc6a6000000004847304402202f93a774f96364ad8fdf46132f47dde1fac4b833d1cf7c20c6c69f03c605c09702207cf7ef42d8c97b96e349d023efd9e7e0b1fd74c50561290d16f3f122e1ead8fb01feffffff9dc64c498135ebd6c025d7d43ae71120d6477bcbcd9828aebe21911ea21655c80000000049483045022100f72cd391c5dd1bc77de0605a3cb35c246a5c1cc14e7b9b3fc1cdd90fd42cfa4b022069049bca8a2f5100ada2a407a2354d04efa94573a7cd1bfa4130cde66e481a1001feffffffa0c3203666c02ea6f958408c8f2241b4d6e3a8beb9ab54736fe73621feb57ce40000000049483045022100daa9b7a48975348b41dfdf8b5e4614721fd018b950d3cec1d7009386bffddb470220522220c5f3ad8f1f19cb0eafea1aae7a3489cdd3dcb3d64f2ce75bd2066a73dd01feffffffa14e8b18777a8710e58942b56d094243151299f033cc21bb3ad3dfce2b3e77ad0000000049483045022100a9e02b9ad05da478a1cf06a235743d202d1f9e8c2e969ea8b1b7d5fe6778fd9602203880f139bf40766d264c2d7f858eb36dc2257b4cacd116cacca400645f80680401feffffffa262a97a28944d41d47c7f8788528c797d322f7abc0390c20bf22e3b835e127a0000000048473044022059a9da8cb72d3d3967ad3adcfb400ee6043ee088707424728de63cba9361da2102206ca3e6681ff149bff11135315d431e24e05aa3c794b41ef0822b8969b0d1597401feffffffaa3c2496b8237d865f81ff0bb8eb01bf2b69ee806463816ec83b60cace7a5833000000004847304402205637e4e9538fa7489e017da763bce9182c5e78492fe23d5366c0638af15c7eef022034e9a552d342053c4184cea58684ffbd0881467cd0a40f009db155275deae1c001feffffffabfc5cf05834234e1ee8a3c87c8de5d6a07f9530a09f2b34d9303ef30d8646cf0000000049483045022100a68eff499320029204dd73f707d36d65583d21ebfa063d770f55139ed546ea8102206646e141b55f506ed457f24311eeec6e302833f69cd08c9ea3086c78f82dfd3801feffffffa2d1512943366ab64e6d1749b81f993e830e5b546a87b9bd68fe0c5c865da953010000006b483045022100c686f7a4b2e8af7deca60cb20b0c626609548f5426dda6bf33207f82923e0ea202200d9c36dc490f014d0d4970ce8c18621d39b6c0c134c7e43da0f62326725598ba01210360cfa32fd05b4c3bc270fc6e8c891af45a149d34664746ffc67f5cb49c6b5f5bfeffffffad976a10bc9ebe391cee6b83191520a9d0fb62a24e969477a4cc6dd26b29e4da000000004847304402203385b46d676be7f898b316fdcf56a8521bda2224ae891b48be05cd880ae7a0e502201f6de4117623336529e445e0943c519e80150cf0d4a5b1427766d06db2d7a26b01feffffffadd486a6d94629b19713d723301b135c11af92b5ed69e6f0b9ed07d417078b2400000000484730440220575a03c7a331f65defeab66ab1404503a700ece0780889266bd1866ff806096b022069348e446f67f551949267b49861e96904e0b47c75a220aa1cd7ffec3b8fa7d801feffffffb04574d6517ca90a26e07a749ebcde23f67f7ef8a594b23e699fa084529d96e80000000049483045022100948f7ec200d121bdea79b29bf1c608c6d5e007aec62acfb3a5cbcae84ce457490220431802ca646caacfeaf1827e1ceb70f07752413c65bb50db24957166603bab3f01feffffffb2197245ddc53b189c18d05d167210fd6291c6b9116862144c3654da5bb55d06000000004847304402204def3dfa143d5887b4075f45d92a91df9825f1e08bee1c29901c1f117ab30df302207eff300c5347d13f531ec36789a6f4f66c07149ff4c86f21107d0f21dc400d9e01feffffffb4b953583df750085d727027674f69c6ba63513915941e42924a462d5bc15c9b0000000049483045022100a267fdd914d9ce78ca819e08312fb2b3c0f9c395bd30d22b26ea8c6a8af3618f0220548b821abd8f1f1fec1db25fbc277cbfc5840e47185a830174a97b74645af60401feffffffb7f5149ac38efb591ad8c3a46ec9e979d5647c964190a135342435b55484dd570000000049483045022100d1d05a271a8516b9357b0e3e73d5413aa138ae9a10c1ccbe30ba7ef15994c24202203df3584a99260ff637db9515361b258e6cf7fbbfa15278b29173dd2c4f25264901feffffffbfc02225e0c5351bbeb63adb8e3b7859752363a5b85f5b2a6da5240a449e8065000000004948304502210082c85c2c7d8316e9e3cfba9f5bafcdbbeaf0509c3e896bd4121f19e4b82cbfe6022070d7650714cb1975215fe109b8f1da2eea866abbdf05e487eb1d75e12776e52d01feffffffc0def09bb3cbf791c52764cceadd389199be9d7603cc3d6d213ba45ffc98518d0000000049483045022100841df35265191f063a9ad2414ec9b36fe39ef9ae13c9fde0e82d67ec9bc654e302206dd8523cf58547ab425ea55a8d879e75d31558701d4f57d76b0f67736ca5e5ea01feffffffc5c9957c3a3e03204e603c313368d3c01206320beddfd28b850fd17b09a61a410000000049483045022100c3467add04b9e313238376a0d3867bc5b59fca8b2eb76bcc18fbc0b0805e63960220578a2cf379848771a9b13e12559cd130853c7f02d9ab497a74f3305aeaf7b00b01feffffffc64396e634d716a5ae280d9fd821507239d7b25a812eea6751254e462c8a73a50000000048473044022040e5e55b23846cbd5e0af588564e5501d58cf2a18eb485c562352fe2801230d002200c70fcf828a81c1cfb856a2d2cc9de21f2564e6080b2f84f44c65b679f49d09c01feffffffc69c9cdd6825a657be1a06008f73b78cf185a9d195ba771451ca1ec09ce54d4f0000000049483045022100e10488858800081f775278c5d844ba2c2cda71ebb4a822d028637191e13efb2602203f7e7f580dad9d7ed1d4cda38222095d8377917c7d4e90c8abb4b9bf3a40975c01feffffffca6112fdc1db1a441961f6eb62b492c1397732cc5519d40f6aa335612f42d39c000000004948304502210097ed9842254112825356823d7365ce8d0bbc973702be7f25951e21f48fcd6e5702203a0aab0ef62926936815e1d9490b335359f766d0ace9b858d59bbd8ba26cb1d901feffffffcb15dbc245dec1ef8cb8e25ef11921ca804c023e6ad803ebcb2a7b98380b60b30000000049483045022100bb9285cab4a68dcb68b46687b59ab1769a0b5aa1ea6f45488e189f58e698321f02205e6499101ee3b0f005e6d3ba151282c236a79d32488e16b1867c6e70c8f7f51001feffffffcfe47e6ce0780c4594a2d1b76a2906c0a9ea32d39a73c244aa9d5d8dea67248c0000000049483045022100a4681709fd0b79ceaddd9d695bd5c740391970a1feff2dd3a90674d20ca95a2a022076dbad3df0c4f8158eba4a087650feeeb1736b5a8b03aef15f698be4fc668abd01feffffffd0a4d502c22cea7da0d1a3cf99aef598b74fad19a6de35f21c6fd0d1b8cf275600000000494830450221009d8a22fe94f18d0a65e8f188b702b4023948e236ac2efd36bfb20d2054e1d55402201383ab2ed9465790eb9496483f10f54e40ae201fb98358cbdd71a0e650ad1b9701feffffffd25452b8575cafca10255179f95c8c66e255329220b7ff645af522af7b8038320000000048473044022013581d5e4794efb6df6dbe04339478ecf019493814d9d52390b6cc790c998762022006aef7acc10019a8cfd7ae99e11e5877a9cf1a5a6ef084549815435f7b681e1801feffffffd3922dfd1a65216bbcd4646d0cbcfa70cfe587775cf4c673043c57061f48d763000000004847304402200bc9095368e4409c7debdf0871f18af1d36e1a4851e4b948a1ce362926550611022034fb19afe76cf133e4bb561fcd3cfe7f3d49743fd75022c124b6e45bd9f503cd01feffffffd75c777645d534009bc8e7b2c0b58a78cd63f41f47f6cd30868aeaf9b55e477000000000494830450221008f4a11d94e97f02e3226c509c70a3582a280ea3bf33309ec392ceeda7a59567e022044bf0d858442058b7c5fd8c73e47287f9283e957fdb39fc005cef70e22b0c07001feffffffd8f837530faf0d9b50efe1d79aed453b11916d565a2b9c40a380a85f0be2af6b0000000048473044022065ac672cfaffe8f8d02fb8064cb54f4d335e7af222452ee71c9b249602cbfcac02202cdb7e8cc05c52db51b71a05258abaf0810d61199eff9ee0ea37d8c373a876ab01feffffffdbce76e284668c829366dafd00ae4884ea39b2aa597cc1b4d2a37991a9b2ea56000000004847304402204480dd6aac1167bb49f32fc04feaa3a7c19ad6cba48479cb72dc7d0bd71ca279022036e654a48cadceba49dbb097892ce5d90d8f082460fb18776d353e9d832ba83301feffffffe481d9493d67997104c12972b7c8a73fb87b16e228665bb784436fc0f58d7e66000000004847304402203645fe9770f3851392a85b8dc9dd405ab13fd8434122f6763de459129527fd0702204d240e91298a1487d496feb320dee028df7dbb5c9236e5d62a4964347f97279001feffffffe7a22d3d87255e4adaab9a6fd8a72320299a6902426424aa8b2b89b7c3b0c0950000000049483045022100b362e030a6739f020622f0f7e34c48fc4ff6147ed88a194a37a8a04c8e42822a0220755bcc63667eb4cbcd52108d27245765176c6c5b2e9a77013aea4d7474c0a1ec01feffffffe80ac9635b6bd91c1935eca6df80876ac8cdc87a2b91e925cfdcc0f06059b2e5000000004847304402204a2b8c311a11920eef4d64e786c5f26ed82d4c1562f2cc0e73fd5a5374c7061e02203693e77f88372a335d1463df4edd062b6dfe2bb895d56d58f3a404c27757378501feffffffedad3357a1a9aeeb8c2771cc6f284db92a2aa31f458e35bb270216015bb0edd40000000049483045022100abad2415b7c6ca9ccf3c52b4008c4d531360f2d6541d9025ec2caa4d764b46da022054f5d2833704686a860fcf978313a3c6c61f16e9a1cf84a3e4ac76c8950dabb701feffffffee85afefc31a99a4616bfb228e1f48691976b900ecdfe838e1310bf5b33fadcf000000004847304402200f7afc12d43432f5303b892b08417743d43a05bf938719428a88c85e255e5b0d02201a12cc706286a1c9329f9e37e62143866563b3773769def6912494a73c17a9f201fefffffff13e4784de0564595f3b4cce57ec0d8a4b72a798feb65f5fbca5b26a3a91d0760000000049483045022100fd3c9b2e02db889ae2bd43537a308a87a7d701bac19083e3a985a93674239e2802206dd36da12f3f2b222ce4387cb91e1098c5f93d25ce95fed0e5d21e6724af554401fefffffff205212771fd3ca5a68340fa307810e44315ae02464b5d8a235ba6bca691bd710000000048473044022062aa2571a91a7e06f0e96570bb3a348296ce7b756ceed48fe69be91f94a6c5c70220631885aa6fc967e40cd1820c83310143884e175227c5434e33b89245598d5e5c01fefffffff31cea9351fddc36393fa996962e204c461a34ff1c6ad243b3a4902440f165da000000004847304402203355527ee222e6bc756ef30c6ad687a21109a5175b1eb27592e9e1938b9e8f850220206ea10896e9e307ee73d33813048fece04bbeda702e11cae8bd61297b73590601fefffffff3c67e78777cc42ae2834bcf5dce5493fbcfcc6e0aabd7608cf4f9c936a37f49000000004847304402207cd40b7d6ca2b869d3f00c0babb484c7a2896c080c593767e0a293acd1505a9c02203a2f8c191b20fe4fb08958b3bb20411834d17f7fa075deb8b2272d22112ec8b001fefffffff3ddc14df664f6e4f59b1f1e25241a61fc69f13125ea5a67edbd03b37d332eb50000000049483045022100a40f81d4e1791d0253a2484656c27994d1e42aaaf77995e9fa6e0eb02480bde30220669c0bfbd0772ec1ad8ca9357eb3ca1100d7b40ed97bb34e23c8cecb42511c7001fefffffff614bd5d83278ad95d8c5bf6fefe59b3675e832cc1c2349d7952aa734fd20283000000004847304402207709f2089f820012e76eaa6221aa0b9776cbdcd0b0b458d400c7c1ca9ed7eedb02200de75bbdae8100b4b27e5deb164e13d596b6661248be45d817b573cdf8cb2c7c01fefffffff67ef42d75fc5d36ff32ab40f5c9f88f279a1173ee1db227a4706aa0480d66ab0000000049483045022100b09aa2cca247052451537f64801ea561506bff82794a8870c077c32c69d0bebc022013bceb4edd8f126af25c07a74d5c16935b0e916cdcc25d49ee335c430400eb2601fefffffff69f0798ab6de485dcfe72391f4cbb1e5f4d39ee8f852b80fd4bb730eabd8e9300000000494830450221009d91a34a7294250ac5b31bc86a2f7ceac8ce79e49d8ac7b3b02ad0cc278f16d102207b9ea41b03e72746a67e7bedfd1cad7f5055a915abdabc13f8e51815f29e983601fefffffff8dd75e7c674cf7bf15f42fcb1256ef4f16b96e0ff6a359bc24c07ba734f09a30000000049483045022100cf9283df82dc2c0d26c2fc9349d16faf2c961919066798705da4afe6fbf27af202207740172e195f5713eff2aeb39d12923625401dea6a0c4b4aa19be3b973c9077601fefffffffa0c47583d4c6f18e12b93764ccf57d2430a52bdd0ceb611924a79c82daf48b9000000004847304402207b46c5dfb4e65c5f91f9770acca2a1ad24a4cdd7e4f27ac9c5e55b14f8d7c00202203b17ab29bd9be1559d550cae9f79728a644682a8aab5db1a1cc3432bad159f4701fefffffffa5ca0440f302bcf118946714dba6e81036e48477ff3a315084fe682aea6d1d50000000049483045022100929668780086aa4c8945fc6d9aaa340ee8ae2807ff2f6a89623ffa102d2bdf6d0220318d3e075a82195af58a66b47c8d62849d69ed1da2e07402d89440a6a77b63ba01fefffffffef369694bf0493161762e49d7ca16f1ba600250d801a848d0ca8d3f2d677d4a0000000049483045022100f7dd5f966156c81a1d2aa694befa6b19e35aa8d7fa199c37a803cd382836fdbe0220669d85a44632a8ea6093b783693c4626ad8c71be4b82b027c4cdfa63682a9a1601feffffff02c5490f00000000001976a9146843838a0aa11686cd0c01fbf470c9c5f302249488ac40420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000",
    "complete": true
  }

Send the transaction

::

  command:

	./komodo-cli sendrawtransaction "01000000660aeb1fef3f0f6e8e9598a2f4b434466b5ccb95e49aa7c4286bc5392d43fa1f2800000000484730440220234b370cddf91b27e172cb5d6257a9807e63cf680a644229147b39d87e597875022047a58509a11b190107a9ff6e08143bd0d450db233518ed26f123bd739576e9c201feffffff0d204965060600f1e79bfd183e7ee1b5b9b61c6379d6c95984cb7cdf79231c4c000000004847304402202ffed5ef972b01ec4290343ab0bc4cff989d0047f2cbc9e8b69f0f3102824c0e02203c7e3214344e6ac430e4f996a8980e7d9172ea1e8c0c238ba32b8930f4d4119301feffffff0d3eba8ce5b6b6ee7d2e804be57dbe4544d7b7169caf5afd6f207c1275e8977e00000000484730440220096fdd062535f200897de2f2dfb7d782499dc5fc24d8e06805eebed6ec125c07022077e4379409bd7c9052608e8cd52cd83b0c9314c623d9b85012eab28e10f8c13601feffffff04f8b24c1eb3aeb01cc483a5b6922eb341da17fd42c944b0bb18998c04fea67e000000004847304402204a8f45abf51333ec7c4491cd5750e5d46785475ebdb0a13a6a946711f17483a9022075805ee9f2130c3938e273c280b6b14b27640349b537b55348c40ede1508938f01feffffff0360b074597abb6e32c319078ea5f83cdfc85d5c892c0388893d8b66876c077b000000004948304502210089c7919c6e7412a1569434f74caf7110bbb0341361384067265c142c8e033b2d02203d5eaa583d727fad487bbb689bf433bac32d907e707043e8f96f8c50fd3480d501feffffff0e2ae757c446029f5dbea36926883744a2d3fe8ee05381c2b4311e7d58057fd40000000049483045022100a0672d882511b01696192965175f3827e65ef8d45b3217b563d0f97f3cab512602205c568b5c1eda0c149976380b38d2f93ee384500bb5eecf6e9f3f2101d649eace01feffffff149c5bbedff321a7810d5db264829ffa5529a4f29ca3a452b0543736339bf0260000000049483045022100981f7f5210e17e1c73fe5083ca7b29a5b1a9dfbbf5474c109069a4b3eecbb5c5022065e21331260c718788b72902da250418b0091537a540e8f6152ae097632637da01feffffff1f9e6624bb5185f0b51d36a3a94982f0d8a325bdf81db90bf67945354a6f40c6000000004847304402204391d39a88d2f8427396bbbca508bcdb3b6897c25bee4c68d357b878419285a602205da8f54aec5bb9253aeaa9b4c4a1a8a2fe602e894422da0279f21f9799a3540201feffffff22e752f465434c0563a7e0b9d104b8633bdbd6073bbe61d17dee0d53ac8220430000000049483045022100d5a4b70ce4542e30a7cfb09ea259405ee202f99b556c88604b06a86419b2e72602202417376668f93e44b404ec2bfe6e797b699367604de296377dfc6944afce722901feffffff2780816ab4fd0177dfff1a98b7783bbefe8d08f339c964d2438b7e73c8ce614c00000000494830450221009d1878ce69f3a438748bcc73de00d531492cd36d2bf7a292bc5bbf67fcf6c774022066e1705510ed5a5177e78a71ba9891d69e11a7a3bc28599d5d18c29c2033a00e01feffffff2da12ef31d8678120d4961c9090035ae9e8f48dcfe4e2f461fb10437473c2bc90000000049483045022100fe0f6284ddb97b4595d77cf7ad5ef4f5caa67cb7c4b6e6ee9812bac076787377022032991f85e1962140673af04a85a442bca3df931ca52c365d3cf24e79b782b2d101feffffff39a00efcf7f678ecf0252ee2b4998a43121aaad28abe518be06a830fd34ae24e0000000048473044022038759690b62c95f80a54d3bde28abdf7dddae992ee4a18c511a4d442da67d758022016aa7dba3da26aa7531731222a0f66cec25c5026cc4903b51dd3fe5483af4cc401feffffff3c5b78d98b3edf510b003cc5723270854313d51ad40859ba08a622f3a269a66900000000484730440220141e545e4ea0c27a630972d474b7d95dd2c9da1a129a7e680016e4ad70c5579102207a3384d8c988bfa526bea0f7cebfb8a8d81ae4b7272d23e83268791fc8eba2bf01feffffff3ca10423750150708e817fe0020a7fd0a687a0456158db659af112dfefefa299000000004847304402205c4e4f8934cea71191f87208bbbaae36b2b3ac4f7282256cc05446cdd1ccc0980220038db0a46e2b06fd61acdf1b47a5de87b787a62a1b65db823c904efa6223129b01feffffff4005c2dd439c35e3f04384142b66871e15a72149218d66be2ca3b13f7e1604b0000000004847304402206b8854445fdb689929143c8daf33fa52ddee06c360073f6262ffea4db0b8b71102200b4d7a166bfa81e8f2570afcd9de338b9a0d7bc72a3962c775205933690f302901feffffff408d53f3499c6db833b4a9b19aa8cf61c95182775a0539efef9c62a0456520c40000000049483045022100c1f028354c1034e61d59999070a8ab554a97f81583d72f38c0f6b0b7a52fe8ab0220538d6fec3f35a595614602203b360730b2f13c3bd879fdadca06dd8a16b90b9d01feffffff43671a7bd5f31ee1642842027378035d73b06d446fbb1666e95638eb0d55d1c9000000004847304402203fc7529cc7a96726728a4aa6a1698fc31bad94d1eadda2a0f74ea8f22d752869022011983a3c457e5c7ffc87b576d877e6f02ab8e08dbda6a94dfbf245315a3365e201feffffff45ee4a5c7a98f315d26c1020b26576500ecae4d6a6a78b3ad169788006e7c76c000000004847304402207a60671e1d0cd3d5d7b8eb2a1b53a0014f30de45f0e379a30435a47e7f9861eb0220689af75a99876c1d1d206869dca223806c45ad64f32cc08cd624936ec6c0600f01feffffff48244290df0dccc781e7d081c731081c2e7e022176cc7b4b31fd92c1e31d970e000000004847304402201972bc346632bcd5166cecbd9d7ca29583c7ad938640d7db9f4bdc6629fff086022019135d7341ef96813a839c6cc14f47c7d2e42c262abbe8747e16c6869cf2b90a01feffffff48c28c27f8303266e0547b8c453b9823baed7a9e06105c09ba4cf65cb2bd5d2b000000004847304402205e40a09a37c939cfa6b5143a2ce596452ecbbd223400922b0001bda694f4c63602205aad66d989167c9bbca130aa489de6286390e55f9e9ef4c5c043c2f13377c7c701feffffff4b28d567f5933d5992559fb19f90115b145db32bd1b6e52d309021da8e6063cc0000000049483045022100ceb282925d7eac742085d5ac48443e9af8b72873fb7a2f96b4e196a58a4b29d7022074790a63adec4088a5d5c2bf1fa80597be0e17afc7490620163a873a2ef1855d01feffffff4d45006be4acc1bf5c69722cb744b967e615d2d35014fc82cf61c2a4905717a50000000049483045022100c6f42ccf0af44182e144aa925b631cab8d90959fa96eb0453335a970e74910d402205e99e1f1d23813e336a3c96efd6e75490f3b5d807f0f2bbc677499cc0b92f47a01feffffff4d8540fa9e580b140359e0a17aac6415ca80072f9ba26fc2b43914092f4702400000000049483045022100b42e72fdb23f4f50af0222d5e590bcc676d60858583dffc1ba8b35730e1c8eb102207cc50ecd38639100131b4c4950cedaac4c4ee37c7a6f87d3ed7fb7eb165559c101feffffff4ff26de89311f83d65a3936e06937f30a75dd50594246d910035bcbe19c0ea6a00000000484730440220425c41bc88fce16ba54f2611a54737d9b5197abc541c730711157b290486cdc6022003f967d0f98864249d80720c65e04c475cbc12c482104aa7e45a06bc9eb080b901feffffff511e169a83c0c0f8ee7163c34fa0e3b024275892419f11a2bb96d4976d3f9b4700000000484730440220136e776a7bfe3fdb5a5b8db2783452ed7cf1fe3c89ec001ed69455a082337e49022057e7dc0ace7ae100a2f2c26291cfe80352b34dfd9269d07468ee2dfba13fc02001feffffff52325adf85f74f38f467bc3a99657f322988add8aebb371bd080088efb95836f000000004847304402201fafc46f92d80a9b4f71a15113ae8e8182dcaa09cff63645db5b858044f329730220160082cc1a3bb262458a204040c3ecc23b276c4558ea095c1b66e20a4004e26b01feffffff532ff452f8423507348c542063deb6f257de711237ff8d718143358128e2c6470000000049483045022100d8dfe5557eae68e8b3da5cc787b14e85fb4d10d2c8a80eda12e69b807319ff9902200b104ae561f1d9c4f0c1646327686f890aed1ea8fb1c1b411f07059517737d0001feffffff5b0d6fe54dce0515e6947f5170478cabb06d1e855365a6b7dbb0118c4450ff0b000000004847304402207fad37e344180882f9cfa3e36d036282a91467ff15fca2f24278f5fa5283b99d0220325dda0a7c35a85cb617bcac369ec0033023c221771cf02f1f877f693f1059d901feffffff5b7db5b32a8e8e8c6307a7d0afec7062637eec39670f1afb08f0b04a50fbc47400000000484730440220752cc9659edbddc78293b1947f84d2bd69e32ef4d5425d4e55df4ca74a7a962402203a755152ab6d38a7ba91f26f476d611cd9c6b27167d6e20b511c4830038d102c01feffffff5cbecf874fd1996cd4e49cd41c98a586c533eac1ebc37df92cf5a9545203f935000000004847304402203af4f03cfed41a4d8387a0859324ce3c40c953582e8848867d06d3aef096deba0220104c18b2e243cf7f076d2833c4fac30e0f5e62b58bc039cba6ce7fe47ea394a101feffffff5d015b907e23b9c5e00907013f66d258fab2f016842f0c8e69346d72b0221dd70000000049483045022100bc3e1c873f25e1a661ef81c109de1758ab13df3fc591540658c5fc05bb1e8c150220309b87661ce039899d5be3b510fcdbb9464ff8cb47af06c016390d79daa7029c01feffffff65c461a04f571b50ab4fe3e367952bfba755eec9b6ed23cb460ab3bdc873fff80000000048473044022037b231fec860afbac51e3034e1308e1873d87dc586258ad8c7ede04cf0fab97e022012eceff07cf09a2c3d2f6884ee885ff9f8e7526de8c08b54e5e538ab223bb31b01feffffff686da3cbb1a1af26c2c01793345a5fb8ee47829aa907ab95b8144fbeda1707920000000049483045022100a0d89b8331105f34528f2c9687f53897a2a14f57cde1390513b4d0fda530a4200220573800bfa5cba98af2a08fa3e87fd0142fe1db6f391a4d160f70565b1078210d01feffffff6896423421d7e1193a7b88d2fbf1eef1c46f637e7a49217c171a18852d29e8d60000000049483045022100cde87af1eb614761149aef298153c541e24ff45345f99dbef18bf2379d27f347022063115fb6b37842eb7cc4d8910ccd047635a9674e72d9418894614014c19d583a01feffffff6a0f6f77ae1d42dc96c39c620f401f32c9774f18f1a039e97b4b405b8aaa757d0000000049483045022100a82d1afe573bfaf0668b3acbec55f68bcbb58bed7b806d59837c32f3560cd1d70220198904866e0bd9d19cc465cf09e256c439ad5309caffa347b8c416443ed07a0c01feffffff6cfa0bcd2e2689498496dc4b15feb0fc535667a88005f2c88198265bb1f8f3d8000000004847304402207917043acb4879438625ace42109cc1bee16054222473d2f975b3edf27286f3602207413e93cf5e696de7c0d210dfa70cd4dd9e62e78ed86a3d99682ef8ea5c064cd01feffffff705456a54cb0b94ec15890bd957dd778581f606270a331ad5b15ef48684a5fc4000000004847304402206668503174e874bc09d999d7bc47f82a5ac47c3f1bc1c43ffa1cca74c1cde4410220616df31f268371b61d83acdfd394a7bcd8da5817174faa29b51c648786c5405a01feffffff718076a7dd771121e817b98e98f46c7f52722d6cdfca9130203fe5965f0a3c00000000004847304402200f1c2ef04cf5fceacb53724360ce3af3794d14ef8a47d4d09c8e3b95b20e48770220659021ba00a68e5f2f4053ec904cc7e65b5bd5db76ff45a9be4ba35ad1a2d0a201feffffff780ed86aeead9747bc96bf7053b02ada6ac566481763e70c29d3d00162bc7b530000000048473044022027f04c7d149ed6c9c72ce3956917444cb5f943aa95adb694ec30ef53c930cfe202206dc14b5f1d59b6724fea484501e36fe7bf40849614921cf76130ec20665f35d401feffffff7b3ad2352be9169286629dcf064fa769c23a8aabd468c30eec35a0c79b61f1f80000000049483045022100c4a61d02e54b0c0b8a9749d394d6447326bf66f3524388b8854c5585ad71704702200b0e71e178082df01e66d0bb72aad0238b0063018cae190c2f21c0fbd78a462001feffffff7fc4676bc415a467bd10d303eacd54617acfb6876945e3bf1217dfd208c6d58d0000000048473044022064ab0c92b7cb2205f1d7af0a2faa441eac041cbb892b166b8f1f060019301546022066924807801b03876a0ac1830eb355ed26c7a67b9e28fcb0b3c6dc5d3c8ca1db01feffffff80fe96eb05e5fcf89fa7e19b1a653e0b8164cba383e2d2ff5934a61c42698cb100000000484730440220515b9c588036449b326ab8d74679cf65c7fe780a03b23ba8428cf829a070abd402204c71e343cfe18e166b7259509b47dcbec0b5b29a764e4dbd29a39479ef60d34601feffffff875ea454109c4725766d372f0fe395dd4744737378b3a246094dc0db7fb6e95f0000000048473044022039167229a3f6ece80aebdfb425608c855989a0e7934abe0c4fca1175f60d46b5022069f57fb057a537cd95e5ebd6a93709e0bffde3d05bd01322f08d0fecef7c061f01feffffff87b7c1fd810834fdd892975a795b9e6c1b1aa398436ae3ecb19bce62ac11aa4e0000000049483045022100ab701a93c793c182bd54f06f80de91c03e36fa9b33b220a91d028f2196d329b5022020e23cff44abe2510b50ce0a8cab286d3ae17c59d8aebd20b42613b764a128c801feffffff88b22fca9de29db1901e9c8accbf1caf8fd4d5a37802b3bf5142038809ee3c6900000000494830450221008ade6fbaec28bf02b3914ffc62c4e0dd7da3d50b41b1054653826a38573e6c13022032d2528595fad675d3f01aad532bdd5ca64960a9cdec35822bb0e69b57fb78ba01feffffff89e4b0f44e022cf53736520aef84a324100f19f4f0862c9d2150b686e951d3740000000049483045022100e69902cff246e6ae5ae8a502aaf2ecc0f8505b8546b17fef18a6e2dde8703bc60220121b6293f7c24aad7766900a746693b9e30ef4e8cc1ca01b2ed4537b47debd2f01feffffff8e0611807aa639621ca6be13a2eda8d98c32867041f929dbbef7742c7c867db000000000484730440220710257eb2b9f5e7b9517770f81c0999a7fcd5b798d8665e0674abec0909b5bad02207bcbcebecb36661cbc8793575f62524dac431fbee3f9c02fb0d854933357694001feffffff8e77d64182b666e50377b3c9a39395735a89d2c90f5ff62024143f2c25ea51d50000000049483045022100ec5f6927e57df66eefcd1275d4236f38841466cdb29aa9ed8c6f8b8f64e0cc4302200141c090ae22c294844bd0b5179f97fd4b98cee426dfb795c3288f37f67a70e401feffffff8fe0b55ad0e150fbfe8d263c44527b967c44fd79ebbe88a09a91a4318f1c17c40000000049483045022100bbaec071109be2005be905bc0b2877286f24cfdb4d8431a31c8f57d802db31270220345e56f174738a6a191ef0a91c4cdeb686dd552d8992ea6ce7517e0ff9cafad001feffffff91ad86b51f541d480383681c4faa26575f723154ed6e39cb76e03317c8984c610000000048473044022046628accc862ea34ab15232f97505cf673d8bfd23d6316677e524e3643e92a20022078414e64419c96474fe2559c30134ac4c08b5a0617a0dc9bd1ce09e85a8df89001feffffff927673288f7c95f452e035b65c8cd46a57e58451b93dcfecfae0c33f00b4e5350000000049483045022100b9e84841140ae7b9bf08f82e014247a8c270d4073b457fbee74743c413e0b4370220292fc63652cd2fae0d1baf9c705de61478b2ec8d4623b9ecaf2aca715c1e69d801feffffff9477cc8e7dddfa7d183bfe0771def3778e7b2641996a3ea52f42d085d4007d190000000048473044022073842db3431ea57cb4aa05435648817bacb36a623e2528817e399126068fbd8b02206744687cfc5587f07d6a507eeeb2aaff45731b3dd9222c40f2b62b60e4db59b301feffffff948a1e5af04f265b29fd23700d1ac9926b5bed71ed5b2968f29abaa15036848c000000004847304402207c5440b72bc608cdf4c7fad0bccdc19d43877e31b22fe3f5873f558a6068e28c022013e3a5b0b11eeec0bfd5cc8317c8a61ccf28ce19a1b50fd7759502a350b991e401feffffff98a1cd6c74d9d42f88032e74182cfe8e71f125eb7eb1b49e8334d5b17bf4d07e00000000484730440220393955bb76c236467d92d42091a290631cbcd9ef3c3f177ace6f1ce73abe319f0220153d5c0aef39f5cea8ef53822993e374dc6d66a758d599f25d2e934d8c97769601feffffff9a7fefd1b1409dfc23d6be09dab5692cd9f6c59c98b2d7b0231f40b396999c2b000000004847304402201f9d944711c3ee35c47b68ddac1a0e1f728884847d8df788b398157de22e9bbd022005d97ceca294e96f5484420189d7a99b9850ecb2c849223ddb934c6c772e32f401feffffff9b0ed42c0446f8ea3c19b47be97f42d1a546bbd6a5a311cded5c1dd16c3606d40000000049483045022100d42b4c9c6fbcbd65d69f0967cca562227f8fbab7ca2727822eb9eb4d0ce8e77a022049d752916ee19c285675786aa04c37d7025e2cef6907f70849f55cda414f3fb501feffffff9ba78bb678f5b7a289ca37b49835bc6ad383e2089dd3711833383c0c6e6d40cb000000004847304402205d3a652a05971d324947fb9d4d15e98393262498e09a6d8fdde7422af91d341a022070e017f2edf61310cb724401a451c1d2be59175e68b49e5c1f82f20084f0b2e501feffffff9d2bdc85ec46fb0457dd41f02f5f7b203ff8c844062f3376c7f86cf2144dc6a6000000004847304402202f93a774f96364ad8fdf46132f47dde1fac4b833d1cf7c20c6c69f03c605c09702207cf7ef42d8c97b96e349d023efd9e7e0b1fd74c50561290d16f3f122e1ead8fb01feffffff9dc64c498135ebd6c025d7d43ae71120d6477bcbcd9828aebe21911ea21655c80000000049483045022100f72cd391c5dd1bc77de0605a3cb35c246a5c1cc14e7b9b3fc1cdd90fd42cfa4b022069049bca8a2f5100ada2a407a2354d04efa94573a7cd1bfa4130cde66e481a1001feffffffa0c3203666c02ea6f958408c8f2241b4d6e3a8beb9ab54736fe73621feb57ce40000000049483045022100daa9b7a48975348b41dfdf8b5e4614721fd018b950d3cec1d7009386bffddb470220522220c5f3ad8f1f19cb0eafea1aae7a3489cdd3dcb3d64f2ce75bd2066a73dd01feffffffa14e8b18777a8710e58942b56d094243151299f033cc21bb3ad3dfce2b3e77ad0000000049483045022100a9e02b9ad05da478a1cf06a235743d202d1f9e8c2e969ea8b1b7d5fe6778fd9602203880f139bf40766d264c2d7f858eb36dc2257b4cacd116cacca400645f80680401feffffffa262a97a28944d41d47c7f8788528c797d322f7abc0390c20bf22e3b835e127a0000000048473044022059a9da8cb72d3d3967ad3adcfb400ee6043ee088707424728de63cba9361da2102206ca3e6681ff149bff11135315d431e24e05aa3c794b41ef0822b8969b0d1597401feffffffaa3c2496b8237d865f81ff0bb8eb01bf2b69ee806463816ec83b60cace7a5833000000004847304402205637e4e9538fa7489e017da763bce9182c5e78492fe23d5366c0638af15c7eef022034e9a552d342053c4184cea58684ffbd0881467cd0a40f009db155275deae1c001feffffffabfc5cf05834234e1ee8a3c87c8de5d6a07f9530a09f2b34d9303ef30d8646cf0000000049483045022100a68eff499320029204dd73f707d36d65583d21ebfa063d770f55139ed546ea8102206646e141b55f506ed457f24311eeec6e302833f69cd08c9ea3086c78f82dfd3801feffffffa2d1512943366ab64e6d1749b81f993e830e5b546a87b9bd68fe0c5c865da953010000006b483045022100c686f7a4b2e8af7deca60cb20b0c626609548f5426dda6bf33207f82923e0ea202200d9c36dc490f014d0d4970ce8c18621d39b6c0c134c7e43da0f62326725598ba01210360cfa32fd05b4c3bc270fc6e8c891af45a149d34664746ffc67f5cb49c6b5f5bfeffffffad976a10bc9ebe391cee6b83191520a9d0fb62a24e969477a4cc6dd26b29e4da000000004847304402203385b46d676be7f898b316fdcf56a8521bda2224ae891b48be05cd880ae7a0e502201f6de4117623336529e445e0943c519e80150cf0d4a5b1427766d06db2d7a26b01feffffffadd486a6d94629b19713d723301b135c11af92b5ed69e6f0b9ed07d417078b2400000000484730440220575a03c7a331f65defeab66ab1404503a700ece0780889266bd1866ff806096b022069348e446f67f551949267b49861e96904e0b47c75a220aa1cd7ffec3b8fa7d801feffffffb04574d6517ca90a26e07a749ebcde23f67f7ef8a594b23e699fa084529d96e80000000049483045022100948f7ec200d121bdea79b29bf1c608c6d5e007aec62acfb3a5cbcae84ce457490220431802ca646caacfeaf1827e1ceb70f07752413c65bb50db24957166603bab3f01feffffffb2197245ddc53b189c18d05d167210fd6291c6b9116862144c3654da5bb55d06000000004847304402204def3dfa143d5887b4075f45d92a91df9825f1e08bee1c29901c1f117ab30df302207eff300c5347d13f531ec36789a6f4f66c07149ff4c86f21107d0f21dc400d9e01feffffffb4b953583df750085d727027674f69c6ba63513915941e42924a462d5bc15c9b0000000049483045022100a267fdd914d9ce78ca819e08312fb2b3c0f9c395bd30d22b26ea8c6a8af3618f0220548b821abd8f1f1fec1db25fbc277cbfc5840e47185a830174a97b74645af60401feffffffb7f5149ac38efb591ad8c3a46ec9e979d5647c964190a135342435b55484dd570000000049483045022100d1d05a271a8516b9357b0e3e73d5413aa138ae9a10c1ccbe30ba7ef15994c24202203df3584a99260ff637db9515361b258e6cf7fbbfa15278b29173dd2c4f25264901feffffffbfc02225e0c5351bbeb63adb8e3b7859752363a5b85f5b2a6da5240a449e8065000000004948304502210082c85c2c7d8316e9e3cfba9f5bafcdbbeaf0509c3e896bd4121f19e4b82cbfe6022070d7650714cb1975215fe109b8f1da2eea866abbdf05e487eb1d75e12776e52d01feffffffc0def09bb3cbf791c52764cceadd389199be9d7603cc3d6d213ba45ffc98518d0000000049483045022100841df35265191f063a9ad2414ec9b36fe39ef9ae13c9fde0e82d67ec9bc654e302206dd8523cf58547ab425ea55a8d879e75d31558701d4f57d76b0f67736ca5e5ea01feffffffc5c9957c3a3e03204e603c313368d3c01206320beddfd28b850fd17b09a61a410000000049483045022100c3467add04b9e313238376a0d3867bc5b59fca8b2eb76bcc18fbc0b0805e63960220578a2cf379848771a9b13e12559cd130853c7f02d9ab497a74f3305aeaf7b00b01feffffffc64396e634d716a5ae280d9fd821507239d7b25a812eea6751254e462c8a73a50000000048473044022040e5e55b23846cbd5e0af588564e5501d58cf2a18eb485c562352fe2801230d002200c70fcf828a81c1cfb856a2d2cc9de21f2564e6080b2f84f44c65b679f49d09c01feffffffc69c9cdd6825a657be1a06008f73b78cf185a9d195ba771451ca1ec09ce54d4f0000000049483045022100e10488858800081f775278c5d844ba2c2cda71ebb4a822d028637191e13efb2602203f7e7f580dad9d7ed1d4cda38222095d8377917c7d4e90c8abb4b9bf3a40975c01feffffffca6112fdc1db1a441961f6eb62b492c1397732cc5519d40f6aa335612f42d39c000000004948304502210097ed9842254112825356823d7365ce8d0bbc973702be7f25951e21f48fcd6e5702203a0aab0ef62926936815e1d9490b335359f766d0ace9b858d59bbd8ba26cb1d901feffffffcb15dbc245dec1ef8cb8e25ef11921ca804c023e6ad803ebcb2a7b98380b60b30000000049483045022100bb9285cab4a68dcb68b46687b59ab1769a0b5aa1ea6f45488e189f58e698321f02205e6499101ee3b0f005e6d3ba151282c236a79d32488e16b1867c6e70c8f7f51001feffffffcfe47e6ce0780c4594a2d1b76a2906c0a9ea32d39a73c244aa9d5d8dea67248c0000000049483045022100a4681709fd0b79ceaddd9d695bd5c740391970a1feff2dd3a90674d20ca95a2a022076dbad3df0c4f8158eba4a087650feeeb1736b5a8b03aef15f698be4fc668abd01feffffffd0a4d502c22cea7da0d1a3cf99aef598b74fad19a6de35f21c6fd0d1b8cf275600000000494830450221009d8a22fe94f18d0a65e8f188b702b4023948e236ac2efd36bfb20d2054e1d55402201383ab2ed9465790eb9496483f10f54e40ae201fb98358cbdd71a0e650ad1b9701feffffffd25452b8575cafca10255179f95c8c66e255329220b7ff645af522af7b8038320000000048473044022013581d5e4794efb6df6dbe04339478ecf019493814d9d52390b6cc790c998762022006aef7acc10019a8cfd7ae99e11e5877a9cf1a5a6ef084549815435f7b681e1801feffffffd3922dfd1a65216bbcd4646d0cbcfa70cfe587775cf4c673043c57061f48d763000000004847304402200bc9095368e4409c7debdf0871f18af1d36e1a4851e4b948a1ce362926550611022034fb19afe76cf133e4bb561fcd3cfe7f3d49743fd75022c124b6e45bd9f503cd01feffffffd75c777645d534009bc8e7b2c0b58a78cd63f41f47f6cd30868aeaf9b55e477000000000494830450221008f4a11d94e97f02e3226c509c70a3582a280ea3bf33309ec392ceeda7a59567e022044bf0d858442058b7c5fd8c73e47287f9283e957fdb39fc005cef70e22b0c07001feffffffd8f837530faf0d9b50efe1d79aed453b11916d565a2b9c40a380a85f0be2af6b0000000048473044022065ac672cfaffe8f8d02fb8064cb54f4d335e7af222452ee71c9b249602cbfcac02202cdb7e8cc05c52db51b71a05258abaf0810d61199eff9ee0ea37d8c373a876ab01feffffffdbce76e284668c829366dafd00ae4884ea39b2aa597cc1b4d2a37991a9b2ea56000000004847304402204480dd6aac1167bb49f32fc04feaa3a7c19ad6cba48479cb72dc7d0bd71ca279022036e654a48cadceba49dbb097892ce5d90d8f082460fb18776d353e9d832ba83301feffffffe481d9493d67997104c12972b7c8a73fb87b16e228665bb784436fc0f58d7e66000000004847304402203645fe9770f3851392a85b8dc9dd405ab13fd8434122f6763de459129527fd0702204d240e91298a1487d496feb320dee028df7dbb5c9236e5d62a4964347f97279001feffffffe7a22d3d87255e4adaab9a6fd8a72320299a6902426424aa8b2b89b7c3b0c0950000000049483045022100b362e030a6739f020622f0f7e34c48fc4ff6147ed88a194a37a8a04c8e42822a0220755bcc63667eb4cbcd52108d27245765176c6c5b2e9a77013aea4d7474c0a1ec01feffffffe80ac9635b6bd91c1935eca6df80876ac8cdc87a2b91e925cfdcc0f06059b2e5000000004847304402204a2b8c311a11920eef4d64e786c5f26ed82d4c1562f2cc0e73fd5a5374c7061e02203693e77f88372a335d1463df4edd062b6dfe2bb895d56d58f3a404c27757378501feffffffedad3357a1a9aeeb8c2771cc6f284db92a2aa31f458e35bb270216015bb0edd40000000049483045022100abad2415b7c6ca9ccf3c52b4008c4d531360f2d6541d9025ec2caa4d764b46da022054f5d2833704686a860fcf978313a3c6c61f16e9a1cf84a3e4ac76c8950dabb701feffffffee85afefc31a99a4616bfb228e1f48691976b900ecdfe838e1310bf5b33fadcf000000004847304402200f7afc12d43432f5303b892b08417743d43a05bf938719428a88c85e255e5b0d02201a12cc706286a1c9329f9e37e62143866563b3773769def6912494a73c17a9f201fefffffff13e4784de0564595f3b4cce57ec0d8a4b72a798feb65f5fbca5b26a3a91d0760000000049483045022100fd3c9b2e02db889ae2bd43537a308a87a7d701bac19083e3a985a93674239e2802206dd36da12f3f2b222ce4387cb91e1098c5f93d25ce95fed0e5d21e6724af554401fefffffff205212771fd3ca5a68340fa307810e44315ae02464b5d8a235ba6bca691bd710000000048473044022062aa2571a91a7e06f0e96570bb3a348296ce7b756ceed48fe69be91f94a6c5c70220631885aa6fc967e40cd1820c83310143884e175227c5434e33b89245598d5e5c01fefffffff31cea9351fddc36393fa996962e204c461a34ff1c6ad243b3a4902440f165da000000004847304402203355527ee222e6bc756ef30c6ad687a21109a5175b1eb27592e9e1938b9e8f850220206ea10896e9e307ee73d33813048fece04bbeda702e11cae8bd61297b73590601fefffffff3c67e78777cc42ae2834bcf5dce5493fbcfcc6e0aabd7608cf4f9c936a37f49000000004847304402207cd40b7d6ca2b869d3f00c0babb484c7a2896c080c593767e0a293acd1505a9c02203a2f8c191b20fe4fb08958b3bb20411834d17f7fa075deb8b2272d22112ec8b001fefffffff3ddc14df664f6e4f59b1f1e25241a61fc69f13125ea5a67edbd03b37d332eb50000000049483045022100a40f81d4e1791d0253a2484656c27994d1e42aaaf77995e9fa6e0eb02480bde30220669c0bfbd0772ec1ad8ca9357eb3ca1100d7b40ed97bb34e23c8cecb42511c7001fefffffff614bd5d83278ad95d8c5bf6fefe59b3675e832cc1c2349d7952aa734fd20283000000004847304402207709f2089f820012e76eaa6221aa0b9776cbdcd0b0b458d400c7c1ca9ed7eedb02200de75bbdae8100b4b27e5deb164e13d596b6661248be45d817b573cdf8cb2c7c01fefffffff67ef42d75fc5d36ff32ab40f5c9f88f279a1173ee1db227a4706aa0480d66ab0000000049483045022100b09aa2cca247052451537f64801ea561506bff82794a8870c077c32c69d0bebc022013bceb4edd8f126af25c07a74d5c16935b0e916cdcc25d49ee335c430400eb2601fefffffff69f0798ab6de485dcfe72391f4cbb1e5f4d39ee8f852b80fd4bb730eabd8e9300000000494830450221009d91a34a7294250ac5b31bc86a2f7ceac8ce79e49d8ac7b3b02ad0cc278f16d102207b9ea41b03e72746a67e7bedfd1cad7f5055a915abdabc13f8e51815f29e983601fefffffff8dd75e7c674cf7bf15f42fcb1256ef4f16b96e0ff6a359bc24c07ba734f09a30000000049483045022100cf9283df82dc2c0d26c2fc9349d16faf2c961919066798705da4afe6fbf27af202207740172e195f5713eff2aeb39d12923625401dea6a0c4b4aa19be3b973c9077601fefffffffa0c47583d4c6f18e12b93764ccf57d2430a52bdd0ceb611924a79c82daf48b9000000004847304402207b46c5dfb4e65c5f91f9770acca2a1ad24a4cdd7e4f27ac9c5e55b14f8d7c00202203b17ab29bd9be1559d550cae9f79728a644682a8aab5db1a1cc3432bad159f4701fefffffffa5ca0440f302bcf118946714dba6e81036e48477ff3a315084fe682aea6d1d50000000049483045022100929668780086aa4c8945fc6d9aaa340ee8ae2807ff2f6a89623ffa102d2bdf6d0220318d3e075a82195af58a66b47c8d62849d69ed1da2e07402d89440a6a77b63ba01fefffffffef369694bf0493161762e49d7ca16f1ba600250d801a848d0ca8d3f2d677d4a0000000049483045022100f7dd5f966156c81a1d2aa694befa6b19e35aa8d7fa199c37a803cd382836fdbe0220669d85a44632a8ea6093b783693c4626ad8c71be4b82b027c4cdfa63682a9a1601feffffff02c5490f00000000001976a9146843838a0aa11686cd0c01fbf470c9c5f302249488ac40420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"

  response:

  a44feb2e788d0332e283d8ca69c6a20999944dccac93246cbf9b36d841b08c95

getrawtransaction "transaction_id_string" ( verbose )
------------------------------------

The ``getrawtransaction`` method returns the raw transaction data.

If ``verbose=0``, the method returns a string that is serialized, hex-encoded data for 'txid'. If ``verbose`` is non-zero, the method returns an object with information about 'txid'.


 * Note: By default, this function only works sometimes. For example, when the tx is in the mempool or there is an unspent output in the utxo for this transaction. To make it complete successfully, you need to maintain a transaction index, using the ``-txindex`` run time parameter.

 * Note: This method comes from the BTC codebase, of which KMD is ultimately a fork (via Zcash). For full details, please see https://bitcoin.org/en/developer-reference#getrawtransaction

Arguments:

::

	"txid"      (string, required) the transaction id
	verbose       (numeric, optional, default=0) if 0, the method returns a string; otherwise, it returns a json object

Result (if verbose is not set or set to 0):

::

	"data"      (string) the serialized, hex-encoded data for 'txid'

Result (if verbose > 0):

::

	{
	  "hex"       (string) the serialized, hex-encoded data for 'txid'
	  "txid"        (string) the transaction id (same as provided)
	  "version"          (numeric) the version
	  "locktime"        (numeric) the lock time
	  "expiryheight"    (numeric, optional) the block height after which the transaction expires
	  "vin" : [
	     {
	       "txid"    (string) the transaction id
	       "vout"         (numeric)
	       "scriptSig": {     (json object) the script
	         "asm"  (string) asm
	         "hex"   (string) hex
	       },
	       "sequence"      (numeric) the script sequence number
	     }
	     ,...
	  ],
	  "vout" : [
	     {
	       "value"            (numeric) the value in KMD or the asset-chain COIN
	       "number"                    (numeric) index
	       "scriptPubKey" : {
	         "asm"          (string) the asm
	         "hex"          (string) the hex
	         "reqSigs"            (numeric) the required sigs
	         "type"  (string) the type, eg 'pubkeyhash'
    	     "addresses" : [
    	       "zcashaddress"          (string) KMD or asset-chain address
    	       ,...
    	     ]
    	   }
    	 }
    	 ,...
	  ],
	  "vjoinsplit" : [
	     {
	       "vpub_old"         (numeric) public input value in KMD
	       "vpub_new"         (numeric) public output value in KMD
	       "anchor"         (string) the anchor
	       "nullifiers" : [            (json array of string)
	         "hex"                     (string) input note nullifier
	         ,...
	       ],
	       "commitments" : [           (json array of string)
	         "hex"                     (string) output note commitment
	         ,...
	       ],
	       "onetimePubKey"  (string) the onetime public key used to encrypt the ciphertexts
	       "randomSeed"     (string) the random seed
	       "macs" : [                  (json array of string)
	         "hex"                     (string) input note MAC
	         ,...
	       ],
	       "proof"          (string) the zero-knowledge proof
	       "ciphertexts" : [           (json array of string)
	         "hex"                     (string) output note ciphertext
	         ,...
	       ]
	     }
	     ,...
	  ],
	  "blockhash"   (string) the block hash
	  "confirmations"      (numeric) the confirmations
	  "time"              (numeric) the transaction time in seconds since epoch (Jan 1 1970 GMT)
	  "blocktime"         (numeric) the block time in seconds since epoch (Jan 1 1970 GMT)
	}

Examples:

::

  command:

	komodo-cli getrawtransaction "a44feb2e788d0332e283d8ca69c6a20999944dccac93246cbf9b36d841b08c95"

  response:

  01000000660aeb1fef3f0f6e8e9598a2f4b434466b5ccb95e49aa7c4286bc5392d43fa1f2800000000484730440220234b370cddf91b27e172cb5d6257a9807e63cf680a644229147b39d87e597875022047a58509a11b190107a9ff6e08143bd0d450db233518ed26f123bd739576e9c201feffffff0d204965060600f1e79bfd183e7ee1b5b9b61c6379d6c95984cb7cdf79231c4c000000004847304402202ffed5ef972b01ec4290343ab0bc4cff989d0047f2cbc9e8b69f0f3102824c0e02203c7e3214344e6ac430e4f996a8980e7d9172ea1e8c0c238ba32b8930f4d4119301feffffff0d3eba8ce5b6b6ee7d2e804be57dbe4544d7b7169caf5afd6f207c1275e8977e00000000484730440220096fdd062535f200897de2f2dfb7d782499dc5fc24d8e06805eebed6ec125c07022077e4379409bd7c9052608e8cd52cd83b0c9314c623d9b85012eab28e10f8c13601feffffff04f8b24c1eb3aeb01cc483a5b6922eb341da17fd42c944b0bb18998c04fea67e000000004847304402204a8f45abf51333ec7c4491cd5750e5d46785475ebdb0a13a6a946711f17483a9022075805ee9f2130c3938e273c280b6b14b27640349b537b55348c40ede1508938f01feffffff0360b074597abb6e32c319078ea5f83cdfc85d5c892c0388893d8b66876c077b000000004948304502210089c7919c6e7412a1569434f74caf7110bbb0341361384067265c142c8e033b2d02203d5eaa583d727fad487bbb689bf433bac32d907e707043e8f96f8c50fd3480d501feffffff0e2ae757c446029f5dbea36926883744a2d3fe8ee05381c2b4311e7d58057fd40000000049483045022100a0672d882511b01696192965175f3827e65ef8d45b3217b563d0f97f3cab512602205c568b5c1eda0c149976380b38d2f93ee384500bb5eecf6e9f3f2101d649eace01feffffff149c5bbedff321a7810d5db264829ffa5529a4f29ca3a452b0543736339bf0260000000049483045022100981f7f5210e17e1c73fe5083ca7b29a5b1a9dfbbf5474c109069a4b3eecbb5c5022065e21331260c718788b72902da250418b0091537a540e8f6152ae097632637da01feffffff1f9e6624bb5185f0b51d36a3a94982f0d8a325bdf81db90bf67945354a6f40c6000000004847304402204391d39a88d2f8427396bbbca508bcdb3b6897c25bee4c68d357b878419285a602205da8f54aec5bb9253aeaa9b4c4a1a8a2fe602e894422da0279f21f9799a3540201feffffff22e752f465434c0563a7e0b9d104b8633bdbd6073bbe61d17dee0d53ac8220430000000049483045022100d5a4b70ce4542e30a7cfb09ea259405ee202f99b556c88604b06a86419b2e72602202417376668f93e44b404ec2bfe6e797b699367604de296377dfc6944afce722901feffffff2780816ab4fd0177dfff1a98b7783bbefe8d08f339c964d2438b7e73c8ce614c00000000494830450221009d1878ce69f3a438748bcc73de00d531492cd36d2bf7a292bc5bbf67fcf6c774022066e1705510ed5a5177e78a71ba9891d69e11a7a3bc28599d5d18c29c2033a00e01feffffff2da12ef31d8678120d4961c9090035ae9e8f48dcfe4e2f461fb10437473c2bc90000000049483045022100fe0f6284ddb97b4595d77cf7ad5ef4f5caa67cb7c4b6e6ee9812bac076787377022032991f85e1962140673af04a85a442bca3df931ca52c365d3cf24e79b782b2d101feffffff39a00efcf7f678ecf0252ee2b4998a43121aaad28abe518be06a830fd34ae24e0000000048473044022038759690b62c95f80a54d3bde28abdf7dddae992ee4a18c511a4d442da67d758022016aa7dba3da26aa7531731222a0f66cec25c5026cc4903b51dd3fe5483af4cc401feffffff3c5b78d98b3edf510b003cc5723270854313d51ad40859ba08a622f3a269a66900000000484730440220141e545e4ea0c27a630972d474b7d95dd2c9da1a129a7e680016e4ad70c5579102207a3384d8c988bfa526bea0f7cebfb8a8d81ae4b7272d23e83268791fc8eba2bf01feffffff3ca10423750150708e817fe0020a7fd0a687a0456158db659af112dfefefa299000000004847304402205c4e4f8934cea71191f87208bbbaae36b2b3ac4f7282256cc05446cdd1ccc0980220038db0a46e2b06fd61acdf1b47a5de87b787a62a1b65db823c904efa6223129b01feffffff4005c2dd439c35e3f04384142b66871e15a72149218d66be2ca3b13f7e1604b0000000004847304402206b8854445fdb689929143c8daf33fa52ddee06c360073f6262ffea4db0b8b71102200b4d7a166bfa81e8f2570afcd9de338b9a0d7bc72a3962c775205933690f302901feffffff408d53f3499c6db833b4a9b19aa8cf61c95182775a0539efef9c62a0456520c40000000049483045022100c1f028354c1034e61d59999070a8ab554a97f81583d72f38c0f6b0b7a52fe8ab0220538d6fec3f35a595614602203b360730b2f13c3bd879fdadca06dd8a16b90b9d01feffffff43671a7bd5f31ee1642842027378035d73b06d446fbb1666e95638eb0d55d1c9000000004847304402203fc7529cc7a96726728a4aa6a1698fc31bad94d1eadda2a0f74ea8f22d752869022011983a3c457e5c7ffc87b576d877e6f02ab8e08dbda6a94dfbf245315a3365e201feffffff45ee4a5c7a98f315d26c1020b26576500ecae4d6a6a78b3ad169788006e7c76c000000004847304402207a60671e1d0cd3d5d7b8eb2a1b53a0014f30de45f0e379a30435a47e7f9861eb0220689af75a99876c1d1d206869dca223806c45ad64f32cc08cd624936ec6c0600f01feffffff48244290df0dccc781e7d081c731081c2e7e022176cc7b4b31fd92c1e31d970e000000004847304402201972bc346632bcd5166cecbd9d7ca29583c7ad938640d7db9f4bdc6629fff086022019135d7341ef96813a839c6cc14f47c7d2e42c262abbe8747e16c6869cf2b90a01feffffff48c28c27f8303266e0547b8c453b9823baed7a9e06105c09ba4cf65cb2bd5d2b000000004847304402205e40a09a37c939cfa6b5143a2ce596452ecbbd223400922b0001bda694f4c63602205aad66d989167c9bbca130aa489de6286390e55f9e9ef4c5c043c2f13377c7c701feffffff4b28d567f5933d5992559fb19f90115b145db32bd1b6e52d309021da8e6063cc0000000049483045022100ceb282925d7eac742085d5ac48443e9af8b72873fb7a2f96b4e196a58a4b29d7022074790a63adec4088a5d5c2bf1fa80597be0e17afc7490620163a873a2ef1855d01feffffff4d45006be4acc1bf5c69722cb744b967e615d2d35014fc82cf61c2a4905717a50000000049483045022100c6f42ccf0af44182e144aa925b631cab8d90959fa96eb0453335a970e74910d402205e99e1f1d23813e336a3c96efd6e75490f3b5d807f0f2bbc677499cc0b92f47a01feffffff4d8540fa9e580b140359e0a17aac6415ca80072f9ba26fc2b43914092f4702400000000049483045022100b42e72fdb23f4f50af0222d5e590bcc676d60858583dffc1ba8b35730e1c8eb102207cc50ecd38639100131b4c4950cedaac4c4ee37c7a6f87d3ed7fb7eb165559c101feffffff4ff26de89311f83d65a3936e06937f30a75dd50594246d910035bcbe19c0ea6a00000000484730440220425c41bc88fce16ba54f2611a54737d9b5197abc541c730711157b290486cdc6022003f967d0f98864249d80720c65e04c475cbc12c482104aa7e45a06bc9eb080b901feffffff511e169a83c0c0f8ee7163c34fa0e3b024275892419f11a2bb96d4976d3f9b4700000000484730440220136e776a7bfe3fdb5a5b8db2783452ed7cf1fe3c89ec001ed69455a082337e49022057e7dc0ace7ae100a2f2c26291cfe80352b34dfd9269d07468ee2dfba13fc02001feffffff52325adf85f74f38f467bc3a99657f322988add8aebb371bd080088efb95836f000000004847304402201fafc46f92d80a9b4f71a15113ae8e8182dcaa09cff63645db5b858044f329730220160082cc1a3bb262458a204040c3ecc23b276c4558ea095c1b66e20a4004e26b01feffffff532ff452f8423507348c542063deb6f257de711237ff8d718143358128e2c6470000000049483045022100d8dfe5557eae68e8b3da5cc787b14e85fb4d10d2c8a80eda12e69b807319ff9902200b104ae561f1d9c4f0c1646327686f890aed1ea8fb1c1b411f07059517737d0001feffffff5b0d6fe54dce0515e6947f5170478cabb06d1e855365a6b7dbb0118c4450ff0b000000004847304402207fad37e344180882f9cfa3e36d036282a91467ff15fca2f24278f5fa5283b99d0220325dda0a7c35a85cb617bcac369ec0033023c221771cf02f1f877f693f1059d901feffffff5b7db5b32a8e8e8c6307a7d0afec7062637eec39670f1afb08f0b04a50fbc47400000000484730440220752cc9659edbddc78293b1947f84d2bd69e32ef4d5425d4e55df4ca74a7a962402203a755152ab6d38a7ba91f26f476d611cd9c6b27167d6e20b511c4830038d102c01feffffff5cbecf874fd1996cd4e49cd41c98a586c533eac1ebc37df92cf5a9545203f935000000004847304402203af4f03cfed41a4d8387a0859324ce3c40c953582e8848867d06d3aef096deba0220104c18b2e243cf7f076d2833c4fac30e0f5e62b58bc039cba6ce7fe47ea394a101feffffff5d015b907e23b9c5e00907013f66d258fab2f016842f0c8e69346d72b0221dd70000000049483045022100bc3e1c873f25e1a661ef81c109de1758ab13df3fc591540658c5fc05bb1e8c150220309b87661ce039899d5be3b510fcdbb9464ff8cb47af06c016390d79daa7029c01feffffff65c461a04f571b50ab4fe3e367952bfba755eec9b6ed23cb460ab3bdc873fff80000000048473044022037b231fec860afbac51e3034e1308e1873d87dc586258ad8c7ede04cf0fab97e022012eceff07cf09a2c3d2f6884ee885ff9f8e7526de8c08b54e5e538ab223bb31b01feffffff686da3cbb1a1af26c2c01793345a5fb8ee47829aa907ab95b8144fbeda1707920000000049483045022100a0d89b8331105f34528f2c9687f53897a2a14f57cde1390513b4d0fda530a4200220573800bfa5cba98af2a08fa3e87fd0142fe1db6f391a4d160f70565b1078210d01feffffff6896423421d7e1193a7b88d2fbf1eef1c46f637e7a49217c171a18852d29e8d60000000049483045022100cde87af1eb614761149aef298153c541e24ff45345f99dbef18bf2379d27f347022063115fb6b37842eb7cc4d8910ccd047635a9674e72d9418894614014c19d583a01feffffff6a0f6f77ae1d42dc96c39c620f401f32c9774f18f1a039e97b4b405b8aaa757d0000000049483045022100a82d1afe573bfaf0668b3acbec55f68bcbb58bed7b806d59837c32f3560cd1d70220198904866e0bd9d19cc465cf09e256c439ad5309caffa347b8c416443ed07a0c01feffffff6cfa0bcd2e2689498496dc4b15feb0fc535667a88005f2c88198265bb1f8f3d8000000004847304402207917043acb4879438625ace42109cc1bee16054222473d2f975b3edf27286f3602207413e93cf5e696de7c0d210dfa70cd4dd9e62e78ed86a3d99682ef8ea5c064cd01feffffff705456a54cb0b94ec15890bd957dd778581f606270a331ad5b15ef48684a5fc4000000004847304402206668503174e874bc09d999d7bc47f82a5ac47c3f1bc1c43ffa1cca74c1cde4410220616df31f268371b61d83acdfd394a7bcd8da5817174faa29b51c648786c5405a01feffffff718076a7dd771121e817b98e98f46c7f52722d6cdfca9130203fe5965f0a3c00000000004847304402200f1c2ef04cf5fceacb53724360ce3af3794d14ef8a47d4d09c8e3b95b20e48770220659021ba00a68e5f2f4053ec904cc7e65b5bd5db76ff45a9be4ba35ad1a2d0a201feffffff780ed86aeead9747bc96bf7053b02ada6ac566481763e70c29d3d00162bc7b530000000048473044022027f04c7d149ed6c9c72ce3956917444cb5f943aa95adb694ec30ef53c930cfe202206dc14b5f1d59b6724fea484501e36fe7bf40849614921cf76130ec20665f35d401feffffff7b3ad2352be9169286629dcf064fa769c23a8aabd468c30eec35a0c79b61f1f80000000049483045022100c4a61d02e54b0c0b8a9749d394d6447326bf66f3524388b8854c5585ad71704702200b0e71e178082df01e66d0bb72aad0238b0063018cae190c2f21c0fbd78a462001feffffff7fc4676bc415a467bd10d303eacd54617acfb6876945e3bf1217dfd208c6d58d0000000048473044022064ab0c92b7cb2205f1d7af0a2faa441eac041cbb892b166b8f1f060019301546022066924807801b03876a0ac1830eb355ed26c7a67b9e28fcb0b3c6dc5d3c8ca1db01feffffff80fe96eb05e5fcf89fa7e19b1a653e0b8164cba383e2d2ff5934a61c42698cb100000000484730440220515b9c588036449b326ab8d74679cf65c7fe780a03b23ba8428cf829a070abd402204c71e343cfe18e166b7259509b47dcbec0b5b29a764e4dbd29a39479ef60d34601feffffff875ea454109c4725766d372f0fe395dd4744737378b3a246094dc0db7fb6e95f0000000048473044022039167229a3f6ece80aebdfb425608c855989a0e7934abe0c4fca1175f60d46b5022069f57fb057a537cd95e5ebd6a93709e0bffde3d05bd01322f08d0fecef7c061f01feffffff87b7c1fd810834fdd892975a795b9e6c1b1aa398436ae3ecb19bce62ac11aa4e0000000049483045022100ab701a93c793c182bd54f06f80de91c03e36fa9b33b220a91d028f2196d329b5022020e23cff44abe2510b50ce0a8cab286d3ae17c59d8aebd20b42613b764a128c801feffffff88b22fca9de29db1901e9c8accbf1caf8fd4d5a37802b3bf5142038809ee3c6900000000494830450221008ade6fbaec28bf02b3914ffc62c4e0dd7da3d50b41b1054653826a38573e6c13022032d2528595fad675d3f01aad532bdd5ca64960a9cdec35822bb0e69b57fb78ba01feffffff89e4b0f44e022cf53736520aef84a324100f19f4f0862c9d2150b686e951d3740000000049483045022100e69902cff246e6ae5ae8a502aaf2ecc0f8505b8546b17fef18a6e2dde8703bc60220121b6293f7c24aad7766900a746693b9e30ef4e8cc1ca01b2ed4537b47debd2f01feffffff8e0611807aa639621ca6be13a2eda8d98c32867041f929dbbef7742c7c867db000000000484730440220710257eb2b9f5e7b9517770f81c0999a7fcd5b798d8665e0674abec0909b5bad02207bcbcebecb36661cbc8793575f62524dac431fbee3f9c02fb0d854933357694001feffffff8e77d64182b666e50377b3c9a39395735a89d2c90f5ff62024143f2c25ea51d50000000049483045022100ec5f6927e57df66eefcd1275d4236f38841466cdb29aa9ed8c6f8b8f64e0cc4302200141c090ae22c294844bd0b5179f97fd4b98cee426dfb795c3288f37f67a70e401feffffff8fe0b55ad0e150fbfe8d263c44527b967c44fd79ebbe88a09a91a4318f1c17c40000000049483045022100bbaec071109be2005be905bc0b2877286f24cfdb4d8431a31c8f57d802db31270220345e56f174738a6a191ef0a91c4cdeb686dd552d8992ea6ce7517e0ff9cafad001feffffff91ad86b51f541d480383681c4faa26575f723154ed6e39cb76e03317c8984c610000000048473044022046628accc862ea34ab15232f97505cf673d8bfd23d6316677e524e3643e92a20022078414e64419c96474fe2559c30134ac4c08b5a0617a0dc9bd1ce09e85a8df89001feffffff927673288f7c95f452e035b65c8cd46a57e58451b93dcfecfae0c33f00b4e5350000000049483045022100b9e84841140ae7b9bf08f82e014247a8c270d4073b457fbee74743c413e0b4370220292fc63652cd2fae0d1baf9c705de61478b2ec8d4623b9ecaf2aca715c1e69d801feffffff9477cc8e7dddfa7d183bfe0771def3778e7b2641996a3ea52f42d085d4007d190000000048473044022073842db3431ea57cb4aa05435648817bacb36a623e2528817e399126068fbd8b02206744687cfc5587f07d6a507eeeb2aaff45731b3dd9222c40f2b62b60e4db59b301feffffff948a1e5af04f265b29fd23700d1ac9926b5bed71ed5b2968f29abaa15036848c000000004847304402207c5440b72bc608cdf4c7fad0bccdc19d43877e31b22fe3f5873f558a6068e28c022013e3a5b0b11eeec0bfd5cc8317c8a61ccf28ce19a1b50fd7759502a350b991e401feffffff98a1cd6c74d9d42f88032e74182cfe8e71f125eb7eb1b49e8334d5b17bf4d07e00000000484730440220393955bb76c236467d92d42091a290631cbcd9ef3c3f177ace6f1ce73abe319f0220153d5c0aef39f5cea8ef53822993e374dc6d66a758d599f25d2e934d8c97769601feffffff9a7fefd1b1409dfc23d6be09dab5692cd9f6c59c98b2d7b0231f40b396999c2b000000004847304402201f9d944711c3ee35c47b68ddac1a0e1f728884847d8df788b398157de22e9bbd022005d97ceca294e96f5484420189d7a99b9850ecb2c849223ddb934c6c772e32f401feffffff9b0ed42c0446f8ea3c19b47be97f42d1a546bbd6a5a311cded5c1dd16c3606d40000000049483045022100d42b4c9c6fbcbd65d69f0967cca562227f8fbab7ca2727822eb9eb4d0ce8e77a022049d752916ee19c285675786aa04c37d7025e2cef6907f70849f55cda414f3fb501feffffff9ba78bb678f5b7a289ca37b49835bc6ad383e2089dd3711833383c0c6e6d40cb000000004847304402205d3a652a05971d324947fb9d4d15e98393262498e09a6d8fdde7422af91d341a022070e017f2edf61310cb724401a451c1d2be59175e68b49e5c1f82f20084f0b2e501feffffff9d2bdc85ec46fb0457dd41f02f5f7b203ff8c844062f3376c7f86cf2144dc6a6000000004847304402202f93a774f96364ad8fdf46132f47dde1fac4b833d1cf7c20c6c69f03c605c09702207cf7ef42d8c97b96e349d023efd9e7e0b1fd74c50561290d16f3f122e1ead8fb01feffffff9dc64c498135ebd6c025d7d43ae71120d6477bcbcd9828aebe21911ea21655c80000000049483045022100f72cd391c5dd1bc77de0605a3cb35c246a5c1cc14e7b9b3fc1cdd90fd42cfa4b022069049bca8a2f5100ada2a407a2354d04efa94573a7cd1bfa4130cde66e481a1001feffffffa0c3203666c02ea6f958408c8f2241b4d6e3a8beb9ab54736fe73621feb57ce40000000049483045022100daa9b7a48975348b41dfdf8b5e4614721fd018b950d3cec1d7009386bffddb470220522220c5f3ad8f1f19cb0eafea1aae7a3489cdd3dcb3d64f2ce75bd2066a73dd01feffffffa14e8b18777a8710e58942b56d094243151299f033cc21bb3ad3dfce2b3e77ad0000000049483045022100a9e02b9ad05da478a1cf06a235743d202d1f9e8c2e969ea8b1b7d5fe6778fd9602203880f139bf40766d264c2d7f858eb36dc2257b4cacd116cacca400645f80680401feffffffa262a97a28944d41d47c7f8788528c797d322f7abc0390c20bf22e3b835e127a0000000048473044022059a9da8cb72d3d3967ad3adcfb400ee6043ee088707424728de63cba9361da2102206ca3e6681ff149bff11135315d431e24e05aa3c794b41ef0822b8969b0d1597401feffffffaa3c2496b8237d865f81ff0bb8eb01bf2b69ee806463816ec83b60cace7a5833000000004847304402205637e4e9538fa7489e017da763bce9182c5e78492fe23d5366c0638af15c7eef022034e9a552d342053c4184cea58684ffbd0881467cd0a40f009db155275deae1c001feffffffabfc5cf05834234e1ee8a3c87c8de5d6a07f9530a09f2b34d9303ef30d8646cf0000000049483045022100a68eff499320029204dd73f707d36d65583d21ebfa063d770f55139ed546ea8102206646e141b55f506ed457f24311eeec6e302833f69cd08c9ea3086c78f82dfd3801feffffffa2d1512943366ab64e6d1749b81f993e830e5b546a87b9bd68fe0c5c865da953010000006b483045022100c686f7a4b2e8af7deca60cb20b0c626609548f5426dda6bf33207f82923e0ea202200d9c36dc490f014d0d4970ce8c18621d39b6c0c134c7e43da0f62326725598ba01210360cfa32fd05b4c3bc270fc6e8c891af45a149d34664746ffc67f5cb49c6b5f5bfeffffffad976a10bc9ebe391cee6b83191520a9d0fb62a24e969477a4cc6dd26b29e4da000000004847304402203385b46d676be7f898b316fdcf56a8521bda2224ae891b48be05cd880ae7a0e502201f6de4117623336529e445e0943c519e80150cf0d4a5b1427766d06db2d7a26b01feffffffadd486a6d94629b19713d723301b135c11af92b5ed69e6f0b9ed07d417078b2400000000484730440220575a03c7a331f65defeab66ab1404503a700ece0780889266bd1866ff806096b022069348e446f67f551949267b49861e96904e0b47c75a220aa1cd7ffec3b8fa7d801feffffffb04574d6517ca90a26e07a749ebcde23f67f7ef8a594b23e699fa084529d96e80000000049483045022100948f7ec200d121bdea79b29bf1c608c6d5e007aec62acfb3a5cbcae84ce457490220431802ca646caacfeaf1827e1ceb70f07752413c65bb50db24957166603bab3f01feffffffb2197245ddc53b189c18d05d167210fd6291c6b9116862144c3654da5bb55d06000000004847304402204def3dfa143d5887b4075f45d92a91df9825f1e08bee1c29901c1f117ab30df302207eff300c5347d13f531ec36789a6f4f66c07149ff4c86f21107d0f21dc400d9e01feffffffb4b953583df750085d727027674f69c6ba63513915941e42924a462d5bc15c9b0000000049483045022100a267fdd914d9ce78ca819e08312fb2b3c0f9c395bd30d22b26ea8c6a8af3618f0220548b821abd8f1f1fec1db25fbc277cbfc5840e47185a830174a97b74645af60401feffffffb7f5149ac38efb591ad8c3a46ec9e979d5647c964190a135342435b55484dd570000000049483045022100d1d05a271a8516b9357b0e3e73d5413aa138ae9a10c1ccbe30ba7ef15994c24202203df3584a99260ff637db9515361b258e6cf7fbbfa15278b29173dd2c4f25264901feffffffbfc02225e0c5351bbeb63adb8e3b7859752363a5b85f5b2a6da5240a449e8065000000004948304502210082c85c2c7d8316e9e3cfba9f5bafcdbbeaf0509c3e896bd4121f19e4b82cbfe6022070d7650714cb1975215fe109b8f1da2eea866abbdf05e487eb1d75e12776e52d01feffffffc0def09bb3cbf791c52764cceadd389199be9d7603cc3d6d213ba45ffc98518d0000000049483045022100841df35265191f063a9ad2414ec9b36fe39ef9ae13c9fde0e82d67ec9bc654e302206dd8523cf58547ab425ea55a8d879e75d31558701d4f57d76b0f67736ca5e5ea01feffffffc5c9957c3a3e03204e603c313368d3c01206320beddfd28b850fd17b09a61a410000000049483045022100c3467add04b9e313238376a0d3867bc5b59fca8b2eb76bcc18fbc0b0805e63960220578a2cf379848771a9b13e12559cd130853c7f02d9ab497a74f3305aeaf7b00b01feffffffc64396e634d716a5ae280d9fd821507239d7b25a812eea6751254e462c8a73a50000000048473044022040e5e55b23846cbd5e0af588564e5501d58cf2a18eb485c562352fe2801230d002200c70fcf828a81c1cfb856a2d2cc9de21f2564e6080b2f84f44c65b679f49d09c01feffffffc69c9cdd6825a657be1a06008f73b78cf185a9d195ba771451ca1ec09ce54d4f0000000049483045022100e10488858800081f775278c5d844ba2c2cda71ebb4a822d028637191e13efb2602203f7e7f580dad9d7ed1d4cda38222095d8377917c7d4e90c8abb4b9bf3a40975c01feffffffca6112fdc1db1a441961f6eb62b492c1397732cc5519d40f6aa335612f42d39c000000004948304502210097ed9842254112825356823d7365ce8d0bbc973702be7f25951e21f48fcd6e5702203a0aab0ef62926936815e1d9490b335359f766d0ace9b858d59bbd8ba26cb1d901feffffffcb15dbc245dec1ef8cb8e25ef11921ca804c023e6ad803ebcb2a7b98380b60b30000000049483045022100bb9285cab4a68dcb68b46687b59ab1769a0b5aa1ea6f45488e189f58e698321f02205e6499101ee3b0f005e6d3ba151282c236a79d32488e16b1867c6e70c8f7f51001feffffffcfe47e6ce0780c4594a2d1b76a2906c0a9ea32d39a73c244aa9d5d8dea67248c0000000049483045022100a4681709fd0b79ceaddd9d695bd5c740391970a1feff2dd3a90674d20ca95a2a022076dbad3df0c4f8158eba4a087650feeeb1736b5a8b03aef15f698be4fc668abd01feffffffd0a4d502c22cea7da0d1a3cf99aef598b74fad19a6de35f21c6fd0d1b8cf275600000000494830450221009d8a22fe94f18d0a65e8f188b702b4023948e236ac2efd36bfb20d2054e1d55402201383ab2ed9465790eb9496483f10f54e40ae201fb98358cbdd71a0e650ad1b9701feffffffd25452b8575cafca10255179f95c8c66e255329220b7ff645af522af7b8038320000000048473044022013581d5e4794efb6df6dbe04339478ecf019493814d9d52390b6cc790c998762022006aef7acc10019a8cfd7ae99e11e5877a9cf1a5a6ef084549815435f7b681e1801feffffffd3922dfd1a65216bbcd4646d0cbcfa70cfe587775cf4c673043c57061f48d763000000004847304402200bc9095368e4409c7debdf0871f18af1d36e1a4851e4b948a1ce362926550611022034fb19afe76cf133e4bb561fcd3cfe7f3d49743fd75022c124b6e45bd9f503cd01feffffffd75c777645d534009bc8e7b2c0b58a78cd63f41f47f6cd30868aeaf9b55e477000000000494830450221008f4a11d94e97f02e3226c509c70a3582a280ea3bf33309ec392ceeda7a59567e022044bf0d858442058b7c5fd8c73e47287f9283e957fdb39fc005cef70e22b0c07001feffffffd8f837530faf0d9b50efe1d79aed453b11916d565a2b9c40a380a85f0be2af6b0000000048473044022065ac672cfaffe8f8d02fb8064cb54f4d335e7af222452ee71c9b249602cbfcac02202cdb7e8cc05c52db51b71a05258abaf0810d61199eff9ee0ea37d8c373a876ab01feffffffdbce76e284668c829366dafd00ae4884ea39b2aa597cc1b4d2a37991a9b2ea56000000004847304402204480dd6aac1167bb49f32fc04feaa3a7c19ad6cba48479cb72dc7d0bd71ca279022036e654a48cadceba49dbb097892ce5d90d8f082460fb18776d353e9d832ba83301feffffffe481d9493d67997104c12972b7c8a73fb87b16e228665bb784436fc0f58d7e66000000004847304402203645fe9770f3851392a85b8dc9dd405ab13fd8434122f6763de459129527fd0702204d240e91298a1487d496feb320dee028df7dbb5c9236e5d62a4964347f97279001feffffffe7a22d3d87255e4adaab9a6fd8a72320299a6902426424aa8b2b89b7c3b0c0950000000049483045022100b362e030a6739f020622f0f7e34c48fc4ff6147ed88a194a37a8a04c8e42822a0220755bcc63667eb4cbcd52108d27245765176c6c5b2e9a77013aea4d7474c0a1ec01feffffffe80ac9635b6bd91c1935eca6df80876ac8cdc87a2b91e925cfdcc0f06059b2e5000000004847304402204a2b8c311a11920eef4d64e786c5f26ed82d4c1562f2cc0e73fd5a5374c7061e02203693e77f88372a335d1463df4edd062b6dfe2bb895d56d58f3a404c27757378501feffffffedad3357a1a9aeeb8c2771cc6f284db92a2aa31f458e35bb270216015bb0edd40000000049483045022100abad2415b7c6ca9ccf3c52b4008c4d531360f2d6541d9025ec2caa4d764b46da022054f5d2833704686a860fcf978313a3c6c61f16e9a1cf84a3e4ac76c8950dabb701feffffffee85afefc31a99a4616bfb228e1f48691976b900ecdfe838e1310bf5b33fadcf000000004847304402200f7afc12d43432f5303b892b08417743d43a05bf938719428a88c85e255e5b0d02201a12cc706286a1c9329f9e37e62143866563b3773769def6912494a73c17a9f201fefffffff13e4784de0564595f3b4cce57ec0d8a4b72a798feb65f5fbca5b26a3a91d0760000000049483045022100fd3c9b2e02db889ae2bd43537a308a87a7d701bac19083e3a985a93674239e2802206dd36da12f3f2b222ce4387cb91e1098c5f93d25ce95fed0e5d21e6724af554401fefffffff205212771fd3ca5a68340fa307810e44315ae02464b5d8a235ba6bca691bd710000000048473044022062aa2571a91a7e06f0e96570bb3a348296ce7b756ceed48fe69be91f94a6c5c70220631885aa6fc967e40cd1820c83310143884e175227c5434e33b89245598d5e5c01fefffffff31cea9351fddc36393fa996962e204c461a34ff1c6ad243b3a4902440f165da000000004847304402203355527ee222e6bc756ef30c6ad687a21109a5175b1eb27592e9e1938b9e8f850220206ea10896e9e307ee73d33813048fece04bbeda702e11cae8bd61297b73590601fefffffff3c67e78777cc42ae2834bcf5dce5493fbcfcc6e0aabd7608cf4f9c936a37f49000000004847304402207cd40b7d6ca2b869d3f00c0babb484c7a2896c080c593767e0a293acd1505a9c02203a2f8c191b20fe4fb08958b3bb20411834d17f7fa075deb8b2272d22112ec8b001fefffffff3ddc14df664f6e4f59b1f1e25241a61fc69f13125ea5a67edbd03b37d332eb50000000049483045022100a40f81d4e1791d0253a2484656c27994d1e42aaaf77995e9fa6e0eb02480bde30220669c0bfbd0772ec1ad8ca9357eb3ca1100d7b40ed97bb34e23c8cecb42511c7001fefffffff614bd5d83278ad95d8c5bf6fefe59b3675e832cc1c2349d7952aa734fd20283000000004847304402207709f2089f820012e76eaa6221aa0b9776cbdcd0b0b458d400c7c1ca9ed7eedb02200de75bbdae8100b4b27e5deb164e13d596b6661248be45d817b573cdf8cb2c7c01fefffffff67ef42d75fc5d36ff32ab40f5c9f88f279a1173ee1db227a4706aa0480d66ab0000000049483045022100b09aa2cca247052451537f64801ea561506bff82794a8870c077c32c69d0bebc022013bceb4edd8f126af25c07a74d5c16935b0e916cdcc25d49ee335c430400eb2601fefffffff69f0798ab6de485dcfe72391f4cbb1e5f4d39ee8f852b80fd4bb730eabd8e9300000000494830450221009d91a34a7294250ac5b31bc86a2f7ceac8ce79e49d8ac7b3b02ad0cc278f16d102207b9ea41b03e72746a67e7bedfd1cad7f5055a915abdabc13f8e51815f29e983601fefffffff8dd75e7c674cf7bf15f42fcb1256ef4f16b96e0ff6a359bc24c07ba734f09a30000000049483045022100cf9283df82dc2c0d26c2fc9349d16faf2c961919066798705da4afe6fbf27af202207740172e195f5713eff2aeb39d12923625401dea6a0c4b4aa19be3b973c9077601fefffffffa0c47583d4c6f18e12b93764ccf57d2430a52bdd0ceb611924a79c82daf48b9000000004847304402207b46c5dfb4e65c5f91f9770acca2a1ad24a4cdd7e4f27ac9c5e55b14f8d7c00202203b17ab29bd9be1559d550cae9f79728a644682a8aab5db1a1cc3432bad159f4701fefffffffa5ca0440f302bcf118946714dba6e81036e48477ff3a315084fe682aea6d1d50000000049483045022100929668780086aa4c8945fc6d9aaa340ee8ae2807ff2f6a89623ffa102d2bdf6d0220318d3e075a82195af58a66b47c8d62849d69ed1da2e07402d89440a6a77b63ba01fefffffffef369694bf0493161762e49d7ca16f1ba600250d801a848d0ca8d3f2d677d4a0000000049483045022100f7dd5f966156c81a1d2aa694befa6b19e35aa8d7fa199c37a803cd382836fdbe0220669d85a44632a8ea6093b783693c4626ad8c71be4b82b027c4cdfa63682a9a1601feffffff02c5490f00000000001976a9146843838a0aa11686cd0c01fbf470c9c5f302249488ac40420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000

::

  command:

	./komodo-cli -ac_name=SIDD getrawtransaction "a44feb2e788d0332e283d8ca69c6a20999944dccac93246cbf9b36d841b08c95" 1

  response:

  {
    "hex": "01000000660aeb1fef3f0f6e8e9598a2f4b434466b5ccb95e49aa7c4286bc5392d43fa1f2800000000484730440220234b370cddf91b27e172cb5d6257a9807e63cf680a644229147b39d87e597875022047a58509a11b190107a9ff6e08143bd0d450db233518ed26f123bd739576e9c201feffffff0d204965060600f1e79bfd183e7ee1b5b9b61c6379d6c95984cb7cdf79231c4c000000004847304402202ffed5ef972b01ec4290343ab0bc4cff989d0047f2cbc9e8b69f0f3102824c0e02203c7e3214344e6ac430e4f996a8980e7d9172ea1e8c0c238ba32b8930f4d4119301feffffff0d3eba8ce5b6b6ee7d2e804be57dbe4544d7b7169caf5afd6f207c1275e8977e00000000484730440220096fdd062535f200897de2f2dfb7d782499dc5fc24d8e06805eebed6ec125c07022077e4379409bd7c9052608e8cd52cd83b0c9314c623d9b85012eab28e10f8c13601feffffff04f8b24c1eb3aeb01cc483a5b6922eb341da17fd42c944b0bb18998c04fea67e000000004847304402204a8f45abf51333ec7c4491cd5750e5d46785475ebdb0a13a6a946711f17483a9022075805ee9f2130c3938e273c280b6b14b27640349b537b55348c40ede1508938f01feffffff0360b074597abb6e32c319078ea5f83cdfc85d5c892c0388893d8b66876c077b000000004948304502210089c7919c6e7412a1569434f74caf7110bbb0341361384067265c142c8e033b2d02203d5eaa583d727fad487bbb689bf433bac32d907e707043e8f96f8c50fd3480d501feffffff0e2ae757c446029f5dbea36926883744a2d3fe8ee05381c2b4311e7d58057fd40000000049483045022100a0672d882511b01696192965175f3827e65ef8d45b3217b563d0f97f3cab512602205c568b5c1eda0c149976380b38d2f93ee384500bb5eecf6e9f3f2101d649eace01feffffff149c5bbedff321a7810d5db264829ffa5529a4f29ca3a452b0543736339bf0260000000049483045022100981f7f5210e17e1c73fe5083ca7b29a5b1a9dfbbf5474c109069a4b3eecbb5c5022065e21331260c718788b72902da250418b0091537a540e8f6152ae097632637da01feffffff1f9e6624bb5185f0b51d36a3a94982f0d8a325bdf81db90bf67945354a6f40c6000000004847304402204391d39a88d2f8427396bbbca508bcdb3b6897c25bee4c68d357b878419285a602205da8f54aec5bb9253aeaa9b4c4a1a8a2fe602e894422da0279f21f9799a3540201feffffff22e752f465434c0563a7e0b9d104b8633bdbd6073bbe61d17dee0d53ac8220430000000049483045022100d5a4b70ce4542e30a7cfb09ea259405ee202f99b556c88604b06a86419b2e72602202417376668f93e44b404ec2bfe6e797b699367604de296377dfc6944afce722901feffffff2780816ab4fd0177dfff1a98b7783bbefe8d08f339c964d2438b7e73c8ce614c00000000494830450221009d1878ce69f3a438748bcc73de00d531492cd36d2bf7a292bc5bbf67fcf6c774022066e1705510ed5a5177e78a71ba9891d69e11a7a3bc28599d5d18c29c2033a00e01feffffff2da12ef31d8678120d4961c9090035ae9e8f48dcfe4e2f461fb10437473c2bc90000000049483045022100fe0f6284ddb97b4595d77cf7ad5ef4f5caa67cb7c4b6e6ee9812bac076787377022032991f85e1962140673af04a85a442bca3df931ca52c365d3cf24e79b782b2d101feffffff39a00efcf7f678ecf0252ee2b4998a43121aaad28abe518be06a830fd34ae24e0000000048473044022038759690b62c95f80a54d3bde28abdf7dddae992ee4a18c511a4d442da67d758022016aa7dba3da26aa7531731222a0f66cec25c5026cc4903b51dd3fe5483af4cc401feffffff3c5b78d98b3edf510b003cc5723270854313d51ad40859ba08a622f3a269a66900000000484730440220141e545e4ea0c27a630972d474b7d95dd2c9da1a129a7e680016e4ad70c5579102207a3384d8c988bfa526bea0f7cebfb8a8d81ae4b7272d23e83268791fc8eba2bf01feffffff3ca10423750150708e817fe0020a7fd0a687a0456158db659af112dfefefa299000000004847304402205c4e4f8934cea71191f87208bbbaae36b2b3ac4f7282256cc05446cdd1ccc0980220038db0a46e2b06fd61acdf1b47a5de87b787a62a1b65db823c904efa6223129b01feffffff4005c2dd439c35e3f04384142b66871e15a72149218d66be2ca3b13f7e1604b0000000004847304402206b8854445fdb689929143c8daf33fa52ddee06c360073f6262ffea4db0b8b71102200b4d7a166bfa81e8f2570afcd9de338b9a0d7bc72a3962c775205933690f302901feffffff408d53f3499c6db833b4a9b19aa8cf61c95182775a0539efef9c62a0456520c40000000049483045022100c1f028354c1034e61d59999070a8ab554a97f81583d72f38c0f6b0b7a52fe8ab0220538d6fec3f35a595614602203b360730b2f13c3bd879fdadca06dd8a16b90b9d01feffffff43671a7bd5f31ee1642842027378035d73b06d446fbb1666e95638eb0d55d1c9000000004847304402203fc7529cc7a96726728a4aa6a1698fc31bad94d1eadda2a0f74ea8f22d752869022011983a3c457e5c7ffc87b576d877e6f02ab8e08dbda6a94dfbf245315a3365e201feffffff45ee4a5c7a98f315d26c1020b26576500ecae4d6a6a78b3ad169788006e7c76c000000004847304402207a60671e1d0cd3d5d7b8eb2a1b53a0014f30de45f0e379a30435a47e7f9861eb0220689af75a99876c1d1d206869dca223806c45ad64f32cc08cd624936ec6c0600f01feffffff48244290df0dccc781e7d081c731081c2e7e022176cc7b4b31fd92c1e31d970e000000004847304402201972bc346632bcd5166cecbd9d7ca29583c7ad938640d7db9f4bdc6629fff086022019135d7341ef96813a839c6cc14f47c7d2e42c262abbe8747e16c6869cf2b90a01feffffff48c28c27f8303266e0547b8c453b9823baed7a9e06105c09ba4cf65cb2bd5d2b000000004847304402205e40a09a37c939cfa6b5143a2ce596452ecbbd223400922b0001bda694f4c63602205aad66d989167c9bbca130aa489de6286390e55f9e9ef4c5c043c2f13377c7c701feffffff4b28d567f5933d5992559fb19f90115b145db32bd1b6e52d309021da8e6063cc0000000049483045022100ceb282925d7eac742085d5ac48443e9af8b72873fb7a2f96b4e196a58a4b29d7022074790a63adec4088a5d5c2bf1fa80597be0e17afc7490620163a873a2ef1855d01feffffff4d45006be4acc1bf5c69722cb744b967e615d2d35014fc82cf61c2a4905717a50000000049483045022100c6f42ccf0af44182e144aa925b631cab8d90959fa96eb0453335a970e74910d402205e99e1f1d23813e336a3c96efd6e75490f3b5d807f0f2bbc677499cc0b92f47a01feffffff4d8540fa9e580b140359e0a17aac6415ca80072f9ba26fc2b43914092f4702400000000049483045022100b42e72fdb23f4f50af0222d5e590bcc676d60858583dffc1ba8b35730e1c8eb102207cc50ecd38639100131b4c4950cedaac4c4ee37c7a6f87d3ed7fb7eb165559c101feffffff4ff26de89311f83d65a3936e06937f30a75dd50594246d910035bcbe19c0ea6a00000000484730440220425c41bc88fce16ba54f2611a54737d9b5197abc541c730711157b290486cdc6022003f967d0f98864249d80720c65e04c475cbc12c482104aa7e45a06bc9eb080b901feffffff511e169a83c0c0f8ee7163c34fa0e3b024275892419f11a2bb96d4976d3f9b4700000000484730440220136e776a7bfe3fdb5a5b8db2783452ed7cf1fe3c89ec001ed69455a082337e49022057e7dc0ace7ae100a2f2c26291cfe80352b34dfd9269d07468ee2dfba13fc02001feffffff52325adf85f74f38f467bc3a99657f322988add8aebb371bd080088efb95836f000000004847304402201fafc46f92d80a9b4f71a15113ae8e8182dcaa09cff63645db5b858044f329730220160082cc1a3bb262458a204040c3ecc23b276c4558ea095c1b66e20a4004e26b01feffffff532ff452f8423507348c542063deb6f257de711237ff8d718143358128e2c6470000000049483045022100d8dfe5557eae68e8b3da5cc787b14e85fb4d10d2c8a80eda12e69b807319ff9902200b104ae561f1d9c4f0c1646327686f890aed1ea8fb1c1b411f07059517737d0001feffffff5b0d6fe54dce0515e6947f5170478cabb06d1e855365a6b7dbb0118c4450ff0b000000004847304402207fad37e344180882f9cfa3e36d036282a91467ff15fca2f24278f5fa5283b99d0220325dda0a7c35a85cb617bcac369ec0033023c221771cf02f1f877f693f1059d901feffffff5b7db5b32a8e8e8c6307a7d0afec7062637eec39670f1afb08f0b04a50fbc47400000000484730440220752cc9659edbddc78293b1947f84d2bd69e32ef4d5425d4e55df4ca74a7a962402203a755152ab6d38a7ba91f26f476d611cd9c6b27167d6e20b511c4830038d102c01feffffff5cbecf874fd1996cd4e49cd41c98a586c533eac1ebc37df92cf5a9545203f935000000004847304402203af4f03cfed41a4d8387a0859324ce3c40c953582e8848867d06d3aef096deba0220104c18b2e243cf7f076d2833c4fac30e0f5e62b58bc039cba6ce7fe47ea394a101feffffff5d015b907e23b9c5e00907013f66d258fab2f016842f0c8e69346d72b0221dd70000000049483045022100bc3e1c873f25e1a661ef81c109de1758ab13df3fc591540658c5fc05bb1e8c150220309b87661ce039899d5be3b510fcdbb9464ff8cb47af06c016390d79daa7029c01feffffff65c461a04f571b50ab4fe3e367952bfba755eec9b6ed23cb460ab3bdc873fff80000000048473044022037b231fec860afbac51e3034e1308e1873d87dc586258ad8c7ede04cf0fab97e022012eceff07cf09a2c3d2f6884ee885ff9f8e7526de8c08b54e5e538ab223bb31b01feffffff686da3cbb1a1af26c2c01793345a5fb8ee47829aa907ab95b8144fbeda1707920000000049483045022100a0d89b8331105f34528f2c9687f53897a2a14f57cde1390513b4d0fda530a4200220573800bfa5cba98af2a08fa3e87fd0142fe1db6f391a4d160f70565b1078210d01feffffff6896423421d7e1193a7b88d2fbf1eef1c46f637e7a49217c171a18852d29e8d60000000049483045022100cde87af1eb614761149aef298153c541e24ff45345f99dbef18bf2379d27f347022063115fb6b37842eb7cc4d8910ccd047635a9674e72d9418894614014c19d583a01feffffff6a0f6f77ae1d42dc96c39c620f401f32c9774f18f1a039e97b4b405b8aaa757d0000000049483045022100a82d1afe573bfaf0668b3acbec55f68bcbb58bed7b806d59837c32f3560cd1d70220198904866e0bd9d19cc465cf09e256c439ad5309caffa347b8c416443ed07a0c01feffffff6cfa0bcd2e2689498496dc4b15feb0fc535667a88005f2c88198265bb1f8f3d8000000004847304402207917043acb4879438625ace42109cc1bee16054222473d2f975b3edf27286f3602207413e93cf5e696de7c0d210dfa70cd4dd9e62e78ed86a3d99682ef8ea5c064cd01feffffff705456a54cb0b94ec15890bd957dd778581f606270a331ad5b15ef48684a5fc4000000004847304402206668503174e874bc09d999d7bc47f82a5ac47c3f1bc1c43ffa1cca74c1cde4410220616df31f268371b61d83acdfd394a7bcd8da5817174faa29b51c648786c5405a01feffffff718076a7dd771121e817b98e98f46c7f52722d6cdfca9130203fe5965f0a3c00000000004847304402200f1c2ef04cf5fceacb53724360ce3af3794d14ef8a47d4d09c8e3b95b20e48770220659021ba00a68e5f2f4053ec904cc7e65b5bd5db76ff45a9be4ba35ad1a2d0a201feffffff780ed86aeead9747bc96bf7053b02ada6ac566481763e70c29d3d00162bc7b530000000048473044022027f04c7d149ed6c9c72ce3956917444cb5f943aa95adb694ec30ef53c930cfe202206dc14b5f1d59b6724fea484501e36fe7bf40849614921cf76130ec20665f35d401feffffff7b3ad2352be9169286629dcf064fa769c23a8aabd468c30eec35a0c79b61f1f80000000049483045022100c4a61d02e54b0c0b8a9749d394d6447326bf66f3524388b8854c5585ad71704702200b0e71e178082df01e66d0bb72aad0238b0063018cae190c2f21c0fbd78a462001feffffff7fc4676bc415a467bd10d303eacd54617acfb6876945e3bf1217dfd208c6d58d0000000048473044022064ab0c92b7cb2205f1d7af0a2faa441eac041cbb892b166b8f1f060019301546022066924807801b03876a0ac1830eb355ed26c7a67b9e28fcb0b3c6dc5d3c8ca1db01feffffff80fe96eb05e5fcf89fa7e19b1a653e0b8164cba383e2d2ff5934a61c42698cb100000000484730440220515b9c588036449b326ab8d74679cf65c7fe780a03b23ba8428cf829a070abd402204c71e343cfe18e166b7259509b47dcbec0b5b29a764e4dbd29a39479ef60d34601feffffff875ea454109c4725766d372f0fe395dd4744737378b3a246094dc0db7fb6e95f0000000048473044022039167229a3f6ece80aebdfb425608c855989a0e7934abe0c4fca1175f60d46b5022069f57fb057a537cd95e5ebd6a93709e0bffde3d05bd01322f08d0fecef7c061f01feffffff87b7c1fd810834fdd892975a795b9e6c1b1aa398436ae3ecb19bce62ac11aa4e0000000049483045022100ab701a93c793c182bd54f06f80de91c03e36fa9b33b220a91d028f2196d329b5022020e23cff44abe2510b50ce0a8cab286d3ae17c59d8aebd20b42613b764a128c801feffffff88b22fca9de29db1901e9c8accbf1caf8fd4d5a37802b3bf5142038809ee3c6900000000494830450221008ade6fbaec28bf02b3914ffc62c4e0dd7da3d50b41b1054653826a38573e6c13022032d2528595fad675d3f01aad532bdd5ca64960a9cdec35822bb0e69b57fb78ba01feffffff89e4b0f44e022cf53736520aef84a324100f19f4f0862c9d2150b686e951d3740000000049483045022100e69902cff246e6ae5ae8a502aaf2ecc0f8505b8546b17fef18a6e2dde8703bc60220121b6293f7c24aad7766900a746693b9e30ef4e8cc1ca01b2ed4537b47debd2f01feffffff8e0611807aa639621ca6be13a2eda8d98c32867041f929dbbef7742c7c867db000000000484730440220710257eb2b9f5e7b9517770f81c0999a7fcd5b798d8665e0674abec0909b5bad02207bcbcebecb36661cbc8793575f62524dac431fbee3f9c02fb0d854933357694001feffffff8e77d64182b666e50377b3c9a39395735a89d2c90f5ff62024143f2c25ea51d50000000049483045022100ec5f6927e57df66eefcd1275d4236f38841466cdb29aa9ed8c6f8b8f64e0cc4302200141c090ae22c294844bd0b5179f97fd4b98cee426dfb795c3288f37f67a70e401feffffff8fe0b55ad0e150fbfe8d263c44527b967c44fd79ebbe88a09a91a4318f1c17c40000000049483045022100bbaec071109be2005be905bc0b2877286f24cfdb4d8431a31c8f57d802db31270220345e56f174738a6a191ef0a91c4cdeb686dd552d8992ea6ce7517e0ff9cafad001feffffff91ad86b51f541d480383681c4faa26575f723154ed6e39cb76e03317c8984c610000000048473044022046628accc862ea34ab15232f97505cf673d8bfd23d6316677e524e3643e92a20022078414e64419c96474fe2559c30134ac4c08b5a0617a0dc9bd1ce09e85a8df89001feffffff927673288f7c95f452e035b65c8cd46a57e58451b93dcfecfae0c33f00b4e5350000000049483045022100b9e84841140ae7b9bf08f82e014247a8c270d4073b457fbee74743c413e0b4370220292fc63652cd2fae0d1baf9c705de61478b2ec8d4623b9ecaf2aca715c1e69d801feffffff9477cc8e7dddfa7d183bfe0771def3778e7b2641996a3ea52f42d085d4007d190000000048473044022073842db3431ea57cb4aa05435648817bacb36a623e2528817e399126068fbd8b02206744687cfc5587f07d6a507eeeb2aaff45731b3dd9222c40f2b62b60e4db59b301feffffff948a1e5af04f265b29fd23700d1ac9926b5bed71ed5b2968f29abaa15036848c000000004847304402207c5440b72bc608cdf4c7fad0bccdc19d43877e31b22fe3f5873f558a6068e28c022013e3a5b0b11eeec0bfd5cc8317c8a61ccf28ce19a1b50fd7759502a350b991e401feffffff98a1cd6c74d9d42f88032e74182cfe8e71f125eb7eb1b49e8334d5b17bf4d07e00000000484730440220393955bb76c236467d92d42091a290631cbcd9ef3c3f177ace6f1ce73abe319f0220153d5c0aef39f5cea8ef53822993e374dc6d66a758d599f25d2e934d8c97769601feffffff9a7fefd1b1409dfc23d6be09dab5692cd9f6c59c98b2d7b0231f40b396999c2b000000004847304402201f9d944711c3ee35c47b68ddac1a0e1f728884847d8df788b398157de22e9bbd022005d97ceca294e96f5484420189d7a99b9850ecb2c849223ddb934c6c772e32f401feffffff9b0ed42c0446f8ea3c19b47be97f42d1a546bbd6a5a311cded5c1dd16c3606d40000000049483045022100d42b4c9c6fbcbd65d69f0967cca562227f8fbab7ca2727822eb9eb4d0ce8e77a022049d752916ee19c285675786aa04c37d7025e2cef6907f70849f55cda414f3fb501feffffff9ba78bb678f5b7a289ca37b49835bc6ad383e2089dd3711833383c0c6e6d40cb000000004847304402205d3a652a05971d324947fb9d4d15e98393262498e09a6d8fdde7422af91d341a022070e017f2edf61310cb724401a451c1d2be59175e68b49e5c1f82f20084f0b2e501feffffff9d2bdc85ec46fb0457dd41f02f5f7b203ff8c844062f3376c7f86cf2144dc6a6000000004847304402202f93a774f96364ad8fdf46132f47dde1fac4b833d1cf7c20c6c69f03c605c09702207cf7ef42d8c97b96e349d023efd9e7e0b1fd74c50561290d16f3f122e1ead8fb01feffffff9dc64c498135ebd6c025d7d43ae71120d6477bcbcd9828aebe21911ea21655c80000000049483045022100f72cd391c5dd1bc77de0605a3cb35c246a5c1cc14e7b9b3fc1cdd90fd42cfa4b022069049bca8a2f5100ada2a407a2354d04efa94573a7cd1bfa4130cde66e481a1001feffffffa0c3203666c02ea6f958408c8f2241b4d6e3a8beb9ab54736fe73621feb57ce40000000049483045022100daa9b7a48975348b41dfdf8b5e4614721fd018b950d3cec1d7009386bffddb470220522220c5f3ad8f1f19cb0eafea1aae7a3489cdd3dcb3d64f2ce75bd2066a73dd01feffffffa14e8b18777a8710e58942b56d094243151299f033cc21bb3ad3dfce2b3e77ad0000000049483045022100a9e02b9ad05da478a1cf06a235743d202d1f9e8c2e969ea8b1b7d5fe6778fd9602203880f139bf40766d264c2d7f858eb36dc2257b4cacd116cacca400645f80680401feffffffa262a97a28944d41d47c7f8788528c797d322f7abc0390c20bf22e3b835e127a0000000048473044022059a9da8cb72d3d3967ad3adcfb400ee6043ee088707424728de63cba9361da2102206ca3e6681ff149bff11135315d431e24e05aa3c794b41ef0822b8969b0d1597401feffffffaa3c2496b8237d865f81ff0bb8eb01bf2b69ee806463816ec83b60cace7a5833000000004847304402205637e4e9538fa7489e017da763bce9182c5e78492fe23d5366c0638af15c7eef022034e9a552d342053c4184cea58684ffbd0881467cd0a40f009db155275deae1c001feffffffabfc5cf05834234e1ee8a3c87c8de5d6a07f9530a09f2b34d9303ef30d8646cf0000000049483045022100a68eff499320029204dd73f707d36d65583d21ebfa063d770f55139ed546ea8102206646e141b55f506ed457f24311eeec6e302833f69cd08c9ea3086c78f82dfd3801feffffffa2d1512943366ab64e6d1749b81f993e830e5b546a87b9bd68fe0c5c865da953010000006b483045022100c686f7a4b2e8af7deca60cb20b0c626609548f5426dda6bf33207f82923e0ea202200d9c36dc490f014d0d4970ce8c18621d39b6c0c134c7e43da0f62326725598ba01210360cfa32fd05b4c3bc270fc6e8c891af45a149d34664746ffc67f5cb49c6b5f5bfeffffffad976a10bc9ebe391cee6b83191520a9d0fb62a24e969477a4cc6dd26b29e4da000000004847304402203385b46d676be7f898b316fdcf56a8521bda2224ae891b48be05cd880ae7a0e502201f6de4117623336529e445e0943c519e80150cf0d4a5b1427766d06db2d7a26b01feffffffadd486a6d94629b19713d723301b135c11af92b5ed69e6f0b9ed07d417078b2400000000484730440220575a03c7a331f65defeab66ab1404503a700ece0780889266bd1866ff806096b022069348e446f67f551949267b49861e96904e0b47c75a220aa1cd7ffec3b8fa7d801feffffffb04574d6517ca90a26e07a749ebcde23f67f7ef8a594b23e699fa084529d96e80000000049483045022100948f7ec200d121bdea79b29bf1c608c6d5e007aec62acfb3a5cbcae84ce457490220431802ca646caacfeaf1827e1ceb70f07752413c65bb50db24957166603bab3f01feffffffb2197245ddc53b189c18d05d167210fd6291c6b9116862144c3654da5bb55d06000000004847304402204def3dfa143d5887b4075f45d92a91df9825f1e08bee1c29901c1f117ab30df302207eff300c5347d13f531ec36789a6f4f66c07149ff4c86f21107d0f21dc400d9e01feffffffb4b953583df750085d727027674f69c6ba63513915941e42924a462d5bc15c9b0000000049483045022100a267fdd914d9ce78ca819e08312fb2b3c0f9c395bd30d22b26ea8c6a8af3618f0220548b821abd8f1f1fec1db25fbc277cbfc5840e47185a830174a97b74645af60401feffffffb7f5149ac38efb591ad8c3a46ec9e979d5647c964190a135342435b55484dd570000000049483045022100d1d05a271a8516b9357b0e3e73d5413aa138ae9a10c1ccbe30ba7ef15994c24202203df3584a99260ff637db9515361b258e6cf7fbbfa15278b29173dd2c4f25264901feffffffbfc02225e0c5351bbeb63adb8e3b7859752363a5b85f5b2a6da5240a449e8065000000004948304502210082c85c2c7d8316e9e3cfba9f5bafcdbbeaf0509c3e896bd4121f19e4b82cbfe6022070d7650714cb1975215fe109b8f1da2eea866abbdf05e487eb1d75e12776e52d01feffffffc0def09bb3cbf791c52764cceadd389199be9d7603cc3d6d213ba45ffc98518d0000000049483045022100841df35265191f063a9ad2414ec9b36fe39ef9ae13c9fde0e82d67ec9bc654e302206dd8523cf58547ab425ea55a8d879e75d31558701d4f57d76b0f67736ca5e5ea01feffffffc5c9957c3a3e03204e603c313368d3c01206320beddfd28b850fd17b09a61a410000000049483045022100c3467add04b9e313238376a0d3867bc5b59fca8b2eb76bcc18fbc0b0805e63960220578a2cf379848771a9b13e12559cd130853c7f02d9ab497a74f3305aeaf7b00b01feffffffc64396e634d716a5ae280d9fd821507239d7b25a812eea6751254e462c8a73a50000000048473044022040e5e55b23846cbd5e0af588564e5501d58cf2a18eb485c562352fe2801230d002200c70fcf828a81c1cfb856a2d2cc9de21f2564e6080b2f84f44c65b679f49d09c01feffffffc69c9cdd6825a657be1a06008f73b78cf185a9d195ba771451ca1ec09ce54d4f0000000049483045022100e10488858800081f775278c5d844ba2c2cda71ebb4a822d028637191e13efb2602203f7e7f580dad9d7ed1d4cda38222095d8377917c7d4e90c8abb4b9bf3a40975c01feffffffca6112fdc1db1a441961f6eb62b492c1397732cc5519d40f6aa335612f42d39c000000004948304502210097ed9842254112825356823d7365ce8d0bbc973702be7f25951e21f48fcd6e5702203a0aab0ef62926936815e1d9490b335359f766d0ace9b858d59bbd8ba26cb1d901feffffffcb15dbc245dec1ef8cb8e25ef11921ca804c023e6ad803ebcb2a7b98380b60b30000000049483045022100bb9285cab4a68dcb68b46687b59ab1769a0b5aa1ea6f45488e189f58e698321f02205e6499101ee3b0f005e6d3ba151282c236a79d32488e16b1867c6e70c8f7f51001feffffffcfe47e6ce0780c4594a2d1b76a2906c0a9ea32d39a73c244aa9d5d8dea67248c0000000049483045022100a4681709fd0b79ceaddd9d695bd5c740391970a1feff2dd3a90674d20ca95a2a022076dbad3df0c4f8158eba4a087650feeeb1736b5a8b03aef15f698be4fc668abd01feffffffd0a4d502c22cea7da0d1a3cf99aef598b74fad19a6de35f21c6fd0d1b8cf275600000000494830450221009d8a22fe94f18d0a65e8f188b702b4023948e236ac2efd36bfb20d2054e1d55402201383ab2ed9465790eb9496483f10f54e40ae201fb98358cbdd71a0e650ad1b9701feffffffd25452b8575cafca10255179f95c8c66e255329220b7ff645af522af7b8038320000000048473044022013581d5e4794efb6df6dbe04339478ecf019493814d9d52390b6cc790c998762022006aef7acc10019a8cfd7ae99e11e5877a9cf1a5a6ef084549815435f7b681e1801feffffffd3922dfd1a65216bbcd4646d0cbcfa70cfe587775cf4c673043c57061f48d763000000004847304402200bc9095368e4409c7debdf0871f18af1d36e1a4851e4b948a1ce362926550611022034fb19afe76cf133e4bb561fcd3cfe7f3d49743fd75022c124b6e45bd9f503cd01feffffffd75c777645d534009bc8e7b2c0b58a78cd63f41f47f6cd30868aeaf9b55e477000000000494830450221008f4a11d94e97f02e3226c509c70a3582a280ea3bf33309ec392ceeda7a59567e022044bf0d858442058b7c5fd8c73e47287f9283e957fdb39fc005cef70e22b0c07001feffffffd8f837530faf0d9b50efe1d79aed453b11916d565a2b9c40a380a85f0be2af6b0000000048473044022065ac672cfaffe8f8d02fb8064cb54f4d335e7af222452ee71c9b249602cbfcac02202cdb7e8cc05c52db51b71a05258abaf0810d61199eff9ee0ea37d8c373a876ab01feffffffdbce76e284668c829366dafd00ae4884ea39b2aa597cc1b4d2a37991a9b2ea56000000004847304402204480dd6aac1167bb49f32fc04feaa3a7c19ad6cba48479cb72dc7d0bd71ca279022036e654a48cadceba49dbb097892ce5d90d8f082460fb18776d353e9d832ba83301feffffffe481d9493d67997104c12972b7c8a73fb87b16e228665bb784436fc0f58d7e66000000004847304402203645fe9770f3851392a85b8dc9dd405ab13fd8434122f6763de459129527fd0702204d240e91298a1487d496feb320dee028df7dbb5c9236e5d62a4964347f97279001feffffffe7a22d3d87255e4adaab9a6fd8a72320299a6902426424aa8b2b89b7c3b0c0950000000049483045022100b362e030a6739f020622f0f7e34c48fc4ff6147ed88a194a37a8a04c8e42822a0220755bcc63667eb4cbcd52108d27245765176c6c5b2e9a77013aea4d7474c0a1ec01feffffffe80ac9635b6bd91c1935eca6df80876ac8cdc87a2b91e925cfdcc0f06059b2e5000000004847304402204a2b8c311a11920eef4d64e786c5f26ed82d4c1562f2cc0e73fd5a5374c7061e02203693e77f88372a335d1463df4edd062b6dfe2bb895d56d58f3a404c27757378501feffffffedad3357a1a9aeeb8c2771cc6f284db92a2aa31f458e35bb270216015bb0edd40000000049483045022100abad2415b7c6ca9ccf3c52b4008c4d531360f2d6541d9025ec2caa4d764b46da022054f5d2833704686a860fcf978313a3c6c61f16e9a1cf84a3e4ac76c8950dabb701feffffffee85afefc31a99a4616bfb228e1f48691976b900ecdfe838e1310bf5b33fadcf000000004847304402200f7afc12d43432f5303b892b08417743d43a05bf938719428a88c85e255e5b0d02201a12cc706286a1c9329f9e37e62143866563b3773769def6912494a73c17a9f201fefffffff13e4784de0564595f3b4cce57ec0d8a4b72a798feb65f5fbca5b26a3a91d0760000000049483045022100fd3c9b2e02db889ae2bd43537a308a87a7d701bac19083e3a985a93674239e2802206dd36da12f3f2b222ce4387cb91e1098c5f93d25ce95fed0e5d21e6724af554401fefffffff205212771fd3ca5a68340fa307810e44315ae02464b5d8a235ba6bca691bd710000000048473044022062aa2571a91a7e06f0e96570bb3a348296ce7b756ceed48fe69be91f94a6c5c70220631885aa6fc967e40cd1820c83310143884e175227c5434e33b89245598d5e5c01fefffffff31cea9351fddc36393fa996962e204c461a34ff1c6ad243b3a4902440f165da000000004847304402203355527ee222e6bc756ef30c6ad687a21109a5175b1eb27592e9e1938b9e8f850220206ea10896e9e307ee73d33813048fece04bbeda702e11cae8bd61297b73590601fefffffff3c67e78777cc42ae2834bcf5dce5493fbcfcc6e0aabd7608cf4f9c936a37f49000000004847304402207cd40b7d6ca2b869d3f00c0babb484c7a2896c080c593767e0a293acd1505a9c02203a2f8c191b20fe4fb08958b3bb20411834d17f7fa075deb8b2272d22112ec8b001fefffffff3ddc14df664f6e4f59b1f1e25241a61fc69f13125ea5a67edbd03b37d332eb50000000049483045022100a40f81d4e1791d0253a2484656c27994d1e42aaaf77995e9fa6e0eb02480bde30220669c0bfbd0772ec1ad8ca9357eb3ca1100d7b40ed97bb34e23c8cecb42511c7001fefffffff614bd5d83278ad95d8c5bf6fefe59b3675e832cc1c2349d7952aa734fd20283000000004847304402207709f2089f820012e76eaa6221aa0b9776cbdcd0b0b458d400c7c1ca9ed7eedb02200de75bbdae8100b4b27e5deb164e13d596b6661248be45d817b573cdf8cb2c7c01fefffffff67ef42d75fc5d36ff32ab40f5c9f88f279a1173ee1db227a4706aa0480d66ab0000000049483045022100b09aa2cca247052451537f64801ea561506bff82794a8870c077c32c69d0bebc022013bceb4edd8f126af25c07a74d5c16935b0e916cdcc25d49ee335c430400eb2601fefffffff69f0798ab6de485dcfe72391f4cbb1e5f4d39ee8f852b80fd4bb730eabd8e9300000000494830450221009d91a34a7294250ac5b31bc86a2f7ceac8ce79e49d8ac7b3b02ad0cc278f16d102207b9ea41b03e72746a67e7bedfd1cad7f5055a915abdabc13f8e51815f29e983601fefffffff8dd75e7c674cf7bf15f42fcb1256ef4f16b96e0ff6a359bc24c07ba734f09a30000000049483045022100cf9283df82dc2c0d26c2fc9349d16faf2c961919066798705da4afe6fbf27af202207740172e195f5713eff2aeb39d12923625401dea6a0c4b4aa19be3b973c9077601fefffffffa0c47583d4c6f18e12b93764ccf57d2430a52bdd0ceb611924a79c82daf48b9000000004847304402207b46c5dfb4e65c5f91f9770acca2a1ad24a4cdd7e4f27ac9c5e55b14f8d7c00202203b17ab29bd9be1559d550cae9f79728a644682a8aab5db1a1cc3432bad159f4701fefffffffa5ca0440f302bcf118946714dba6e81036e48477ff3a315084fe682aea6d1d50000000049483045022100929668780086aa4c8945fc6d9aaa340ee8ae2807ff2f6a89623ffa102d2bdf6d0220318d3e075a82195af58a66b47c8d62849d69ed1da2e07402d89440a6a77b63ba01fefffffffef369694bf0493161762e49d7ca16f1ba600250d801a848d0ca8d3f2d677d4a0000000049483045022100f7dd5f966156c81a1d2aa694befa6b19e35aa8d7fa199c37a803cd382836fdbe0220669d85a44632a8ea6093b783693c4626ad8c71be4b82b027c4cdfa63682a9a1601feffffff02c5490f00000000001976a9146843838a0aa11686cd0c01fbf470c9c5f302249488ac40420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000",
    "txid": "a44feb2e788d0332e283d8ca69c6a20999944dccac93246cbf9b36d841b08c95",
    "overwintered": false,
    "version": 1,
    "locktime": 0,
    "vin": [
      {
        "txid": "281ffa432d39c56b28c4a79ae495cb5c6b4634b4f4a298958e6e0f3fef1feb0a",
        "vout": 0,
        "address": "RRqqaWq8QLfpBHtAit4hXfEfV37WXT5Myo",
        "scriptSig": {
          "asm": "30440220234b370cddf91b27e172cb5d6257a9807e63cf680a644229147b39d87e597875022047a58509a11b190107a9ff6e08143bd0d450db233518ed26f123bd739576e9c201",
          "hex": "4730440220234b370cddf91b27e172cb5d6257a9807e63cf680a644229147b39d87e597875022047a58509a11b190107a9ff6e08143bd0d450db233518ed26f123bd739576e9c201"
        },
        "sequence": 4294967294
      }
    ],
    "vout": [
      {
        "value": 0.01001925,
        "valueZat": 1001925,
        "valueSat": 1001925,
        "n": 0,
        "scriptPubKey": {
          "asm": "OP_DUP OP_HASH160 6843838a0aa11686cd0c01fbf470c9c5f3022494 OP_EQUALVERIFY OP_CHECKSIG",
          "hex": "76a9146843838a0aa11686cd0c01fbf470c9c5f302249488ac",
          "reqSigs": 1,
          "type": "pubkeyhash",
          "addresses": [
            "RJnVEQgucK1iwiRjfTZmreXkF49KgTErDn"
          ]
        }
      }
    ],
    "vjoinsplit": [
    ]
  }

::

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getrawtransaction", "params": ["a44feb2e788d0332e283d8ca69c6a20999944dccac93246cbf9b36d841b08c95", 1] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:
  {
    result: {
      "hex": "01000000660aeb1fef3f0f6e8e9598a2f4b434466b5ccb95e49aa7c4286bc5392d43fa1f2800000000484730440220234b370cddf91b27e172cb5d6257a9807e63cf680a644229147b39d87e597875022047a58509a11b190107a9ff6e08143bd0d450db233518ed26f123bd739576e9c201feffffff0d204965060600f1e79bfd183e7ee1b5b9b61c6379d6c95984cb7cdf79231c4c000000004847304402202ffed5ef972b01ec4290343ab0bc4cff989d0047f2cbc9e8b69f0f3102824c0e02203c7e3214344e6ac430e4f996a8980e7d9172ea1e8c0c238ba32b8930f4d4119301feffffff0d3eba8ce5b6b6ee7d2e804be57dbe4544d7b7169caf5afd6f207c1275e8977e00000000484730440220096fdd062535f200897de2f2dfb7d782499dc5fc24d8e06805eebed6ec125c07022077e4379409bd7c9052608e8cd52cd83b0c9314c623d9b85012eab28e10f8c13601feffffff04f8b24c1eb3aeb01cc483a5b6922eb341da17fd42c944b0bb18998c04fea67e000000004847304402204a8f45abf51333ec7c4491cd5750e5d46785475ebdb0a13a6a946711f17483a9022075805ee9f2130c3938e273c280b6b14b27640349b537b55348c40ede1508938f01feffffff0360b074597abb6e32c319078ea5f83cdfc85d5c892c0388893d8b66876c077b000000004948304502210089c7919c6e7412a1569434f74caf7110bbb0341361384067265c142c8e033b2d02203d5eaa583d727fad487bbb689bf433bac32d907e707043e8f96f8c50fd3480d501feffffff0e2ae757c446029f5dbea36926883744a2d3fe8ee05381c2b4311e7d58057fd40000000049483045022100a0672d882511b01696192965175f3827e65ef8d45b3217b563d0f97f3cab512602205c568b5c1eda0c149976380b38d2f93ee384500bb5eecf6e9f3f2101d649eace01feffffff149c5bbedff321a7810d5db264829ffa5529a4f29ca3a452b0543736339bf0260000000049483045022100981f7f5210e17e1c73fe5083ca7b29a5b1a9dfbbf5474c109069a4b3eecbb5c5022065e21331260c718788b72902da250418b0091537a540e8f6152ae097632637da01feffffff1f9e6624bb5185f0b51d36a3a94982f0d8a325bdf81db90bf67945354a6f40c6000000004847304402204391d39a88d2f8427396bbbca508bcdb3b6897c25bee4c68d357b878419285a602205da8f54aec5bb9253aeaa9b4c4a1a8a2fe602e894422da0279f21f9799a3540201feffffff22e752f465434c0563a7e0b9d104b8633bdbd6073bbe61d17dee0d53ac8220430000000049483045022100d5a4b70ce4542e30a7cfb09ea259405ee202f99b556c88604b06a86419b2e72602202417376668f93e44b404ec2bfe6e797b699367604de296377dfc6944afce722901feffffff2780816ab4fd0177dfff1a98b7783bbefe8d08f339c964d2438b7e73c8ce614c00000000494830450221009d1878ce69f3a438748bcc73de00d531492cd36d2bf7a292bc5bbf67fcf6c774022066e1705510ed5a5177e78a71ba9891d69e11a7a3bc28599d5d18c29c2033a00e01feffffff2da12ef31d8678120d4961c9090035ae9e8f48dcfe4e2f461fb10437473c2bc90000000049483045022100fe0f6284ddb97b4595d77cf7ad5ef4f5caa67cb7c4b6e6ee9812bac076787377022032991f85e1962140673af04a85a442bca3df931ca52c365d3cf24e79b782b2d101feffffff39a00efcf7f678ecf0252ee2b4998a43121aaad28abe518be06a830fd34ae24e0000000048473044022038759690b62c95f80a54d3bde28abdf7dddae992ee4a18c511a4d442da67d758022016aa7dba3da26aa7531731222a0f66cec25c5026cc4903b51dd3fe5483af4cc401feffffff3c5b78d98b3edf510b003cc5723270854313d51ad40859ba08a622f3a269a66900000000484730440220141e545e4ea0c27a630972d474b7d95dd2c9da1a129a7e680016e4ad70c5579102207a3384d8c988bfa526bea0f7cebfb8a8d81ae4b7272d23e83268791fc8eba2bf01feffffff3ca10423750150708e817fe0020a7fd0a687a0456158db659af112dfefefa299000000004847304402205c4e4f8934cea71191f87208bbbaae36b2b3ac4f7282256cc05446cdd1ccc0980220038db0a46e2b06fd61acdf1b47a5de87b787a62a1b65db823c904efa6223129b01feffffff4005c2dd439c35e3f04384142b66871e15a72149218d66be2ca3b13f7e1604b0000000004847304402206b8854445fdb689929143c8daf33fa52ddee06c360073f6262ffea4db0b8b71102200b4d7a166bfa81e8f2570afcd9de338b9a0d7bc72a3962c775205933690f302901feffffff408d53f3499c6db833b4a9b19aa8cf61c95182775a0539efef9c62a0456520c40000000049483045022100c1f028354c1034e61d59999070a8ab554a97f81583d72f38c0f6b0b7a52fe8ab0220538d6fec3f35a595614602203b360730b2f13c3bd879fdadca06dd8a16b90b9d01feffffff43671a7bd5f31ee1642842027378035d73b06d446fbb1666e95638eb0d55d1c9000000004847304402203fc7529cc7a96726728a4aa6a1698fc31bad94d1eadda2a0f74ea8f22d752869022011983a3c457e5c7ffc87b576d877e6f02ab8e08dbda6a94dfbf245315a3365e201feffffff45ee4a5c7a98f315d26c1020b26576500ecae4d6a6a78b3ad169788006e7c76c000000004847304402207a60671e1d0cd3d5d7b8eb2a1b53a0014f30de45f0e379a30435a47e7f9861eb0220689af75a99876c1d1d206869dca223806c45ad64f32cc08cd624936ec6c0600f01feffffff48244290df0dccc781e7d081c731081c2e7e022176cc7b4b31fd92c1e31d970e000000004847304402201972bc346632bcd5166cecbd9d7ca29583c7ad938640d7db9f4bdc6629fff086022019135d7341ef96813a839c6cc14f47c7d2e42c262abbe8747e16c6869cf2b90a01feffffff48c28c27f8303266e0547b8c453b9823baed7a9e06105c09ba4cf65cb2bd5d2b000000004847304402205e40a09a37c939cfa6b5143a2ce596452ecbbd223400922b0001bda694f4c63602205aad66d989167c9bbca130aa489de6286390e55f9e9ef4c5c043c2f13377c7c701feffffff4b28d567f5933d5992559fb19f90115b145db32bd1b6e52d309021da8e6063cc0000000049483045022100ceb282925d7eac742085d5ac48443e9af8b72873fb7a2f96b4e196a58a4b29d7022074790a63adec4088a5d5c2bf1fa80597be0e17afc7490620163a873a2ef1855d01feffffff4d45006be4acc1bf5c69722cb744b967e615d2d35014fc82cf61c2a4905717a50000000049483045022100c6f42ccf0af44182e144aa925b631cab8d90959fa96eb0453335a970e74910d402205e99e1f1d23813e336a3c96efd6e75490f3b5d807f0f2bbc677499cc0b92f47a01feffffff4d8540fa9e580b140359e0a17aac6415ca80072f9ba26fc2b43914092f4702400000000049483045022100b42e72fdb23f4f50af0222d5e590bcc676d60858583dffc1ba8b35730e1c8eb102207cc50ecd38639100131b4c4950cedaac4c4ee37c7a6f87d3ed7fb7eb165559c101feffffff4ff26de89311f83d65a3936e06937f30a75dd50594246d910035bcbe19c0ea6a00000000484730440220425c41bc88fce16ba54f2611a54737d9b5197abc541c730711157b290486cdc6022003f967d0f98864249d80720c65e04c475cbc12c482104aa7e45a06bc9eb080b901feffffff511e169a83c0c0f8ee7163c34fa0e3b024275892419f11a2bb96d4976d3f9b4700000000484730440220136e776a7bfe3fdb5a5b8db2783452ed7cf1fe3c89ec001ed69455a082337e49022057e7dc0ace7ae100a2f2c26291cfe80352b34dfd9269d07468ee2dfba13fc02001feffffff52325adf85f74f38f467bc3a99657f322988add8aebb371bd080088efb95836f000000004847304402201fafc46f92d80a9b4f71a15113ae8e8182dcaa09cff63645db5b858044f329730220160082cc1a3bb262458a204040c3ecc23b276c4558ea095c1b66e20a4004e26b01feffffff532ff452f8423507348c542063deb6f257de711237ff8d718143358128e2c6470000000049483045022100d8dfe5557eae68e8b3da5cc787b14e85fb4d10d2c8a80eda12e69b807319ff9902200b104ae561f1d9c4f0c1646327686f890aed1ea8fb1c1b411f07059517737d0001feffffff5b0d6fe54dce0515e6947f5170478cabb06d1e855365a6b7dbb0118c4450ff0b000000004847304402207fad37e344180882f9cfa3e36d036282a91467ff15fca2f24278f5fa5283b99d0220325dda0a7c35a85cb617bcac369ec0033023c221771cf02f1f877f693f1059d901feffffff5b7db5b32a8e8e8c6307a7d0afec7062637eec39670f1afb08f0b04a50fbc47400000000484730440220752cc9659edbddc78293b1947f84d2bd69e32ef4d5425d4e55df4ca74a7a962402203a755152ab6d38a7ba91f26f476d611cd9c6b27167d6e20b511c4830038d102c01feffffff5cbecf874fd1996cd4e49cd41c98a586c533eac1ebc37df92cf5a9545203f935000000004847304402203af4f03cfed41a4d8387a0859324ce3c40c953582e8848867d06d3aef096deba0220104c18b2e243cf7f076d2833c4fac30e0f5e62b58bc039cba6ce7fe47ea394a101feffffff5d015b907e23b9c5e00907013f66d258fab2f016842f0c8e69346d72b0221dd70000000049483045022100bc3e1c873f25e1a661ef81c109de1758ab13df3fc591540658c5fc05bb1e8c150220309b87661ce039899d5be3b510fcdbb9464ff8cb47af06c016390d79daa7029c01feffffff65c461a04f571b50ab4fe3e367952bfba755eec9b6ed23cb460ab3bdc873fff80000000048473044022037b231fec860afbac51e3034e1308e1873d87dc586258ad8c7ede04cf0fab97e022012eceff07cf09a2c3d2f6884ee885ff9f8e7526de8c08b54e5e538ab223bb31b01feffffff686da3cbb1a1af26c2c01793345a5fb8ee47829aa907ab95b8144fbeda1707920000000049483045022100a0d89b8331105f34528f2c9687f53897a2a14f57cde1390513b4d0fda530a4200220573800bfa5cba98af2a08fa3e87fd0142fe1db6f391a4d160f70565b1078210d01feffffff6896423421d7e1193a7b88d2fbf1eef1c46f637e7a49217c171a18852d29e8d60000000049483045022100cde87af1eb614761149aef298153c541e24ff45345f99dbef18bf2379d27f347022063115fb6b37842eb7cc4d8910ccd047635a9674e72d9418894614014c19d583a01feffffff6a0f6f77ae1d42dc96c39c620f401f32c9774f18f1a039e97b4b405b8aaa757d0000000049483045022100a82d1afe573bfaf0668b3acbec55f68bcbb58bed7b806d59837c32f3560cd1d70220198904866e0bd9d19cc465cf09e256c439ad5309caffa347b8c416443ed07a0c01feffffff6cfa0bcd2e2689498496dc4b15feb0fc535667a88005f2c88198265bb1f8f3d8000000004847304402207917043acb4879438625ace42109cc1bee16054222473d2f975b3edf27286f3602207413e93cf5e696de7c0d210dfa70cd4dd9e62e78ed86a3d99682ef8ea5c064cd01feffffff705456a54cb0b94ec15890bd957dd778581f606270a331ad5b15ef48684a5fc4000000004847304402206668503174e874bc09d999d7bc47f82a5ac47c3f1bc1c43ffa1cca74c1cde4410220616df31f268371b61d83acdfd394a7bcd8da5817174faa29b51c648786c5405a01feffffff718076a7dd771121e817b98e98f46c7f52722d6cdfca9130203fe5965f0a3c00000000004847304402200f1c2ef04cf5fceacb53724360ce3af3794d14ef8a47d4d09c8e3b95b20e48770220659021ba00a68e5f2f4053ec904cc7e65b5bd5db76ff45a9be4ba35ad1a2d0a201feffffff780ed86aeead9747bc96bf7053b02ada6ac566481763e70c29d3d00162bc7b530000000048473044022027f04c7d149ed6c9c72ce3956917444cb5f943aa95adb694ec30ef53c930cfe202206dc14b5f1d59b6724fea484501e36fe7bf40849614921cf76130ec20665f35d401feffffff7b3ad2352be9169286629dcf064fa769c23a8aabd468c30eec35a0c79b61f1f80000000049483045022100c4a61d02e54b0c0b8a9749d394d6447326bf66f3524388b8854c5585ad71704702200b0e71e178082df01e66d0bb72aad0238b0063018cae190c2f21c0fbd78a462001feffffff7fc4676bc415a467bd10d303eacd54617acfb6876945e3bf1217dfd208c6d58d0000000048473044022064ab0c92b7cb2205f1d7af0a2faa441eac041cbb892b166b8f1f060019301546022066924807801b03876a0ac1830eb355ed26c7a67b9e28fcb0b3c6dc5d3c8ca1db01feffffff80fe96eb05e5fcf89fa7e19b1a653e0b8164cba383e2d2ff5934a61c42698cb100000000484730440220515b9c588036449b326ab8d74679cf65c7fe780a03b23ba8428cf829a070abd402204c71e343cfe18e166b7259509b47dcbec0b5b29a764e4dbd29a39479ef60d34601feffffff875ea454109c4725766d372f0fe395dd4744737378b3a246094dc0db7fb6e95f0000000048473044022039167229a3f6ece80aebdfb425608c855989a0e7934abe0c4fca1175f60d46b5022069f57fb057a537cd95e5ebd6a93709e0bffde3d05bd01322f08d0fecef7c061f01feffffff87b7c1fd810834fdd892975a795b9e6c1b1aa398436ae3ecb19bce62ac11aa4e0000000049483045022100ab701a93c793c182bd54f06f80de91c03e36fa9b33b220a91d028f2196d329b5022020e23cff44abe2510b50ce0a8cab286d3ae17c59d8aebd20b42613b764a128c801feffffff88b22fca9de29db1901e9c8accbf1caf8fd4d5a37802b3bf5142038809ee3c6900000000494830450221008ade6fbaec28bf02b3914ffc62c4e0dd7da3d50b41b1054653826a38573e6c13022032d2528595fad675d3f01aad532bdd5ca64960a9cdec35822bb0e69b57fb78ba01feffffff89e4b0f44e022cf53736520aef84a324100f19f4f0862c9d2150b686e951d3740000000049483045022100e69902cff246e6ae5ae8a502aaf2ecc0f8505b8546b17fef18a6e2dde8703bc60220121b6293f7c24aad7766900a746693b9e30ef4e8cc1ca01b2ed4537b47debd2f01feffffff8e0611807aa639621ca6be13a2eda8d98c32867041f929dbbef7742c7c867db000000000484730440220710257eb2b9f5e7b9517770f81c0999a7fcd5b798d8665e0674abec0909b5bad02207bcbcebecb36661cbc8793575f62524dac431fbee3f9c02fb0d854933357694001feffffff8e77d64182b666e50377b3c9a39395735a89d2c90f5ff62024143f2c25ea51d50000000049483045022100ec5f6927e57df66eefcd1275d4236f38841466cdb29aa9ed8c6f8b8f64e0cc4302200141c090ae22c294844bd0b5179f97fd4b98cee426dfb795c3288f37f67a70e401feffffff8fe0b55ad0e150fbfe8d263c44527b967c44fd79ebbe88a09a91a4318f1c17c40000000049483045022100bbaec071109be2005be905bc0b2877286f24cfdb4d8431a31c8f57d802db31270220345e56f174738a6a191ef0a91c4cdeb686dd552d8992ea6ce7517e0ff9cafad001feffffff91ad86b51f541d480383681c4faa26575f723154ed6e39cb76e03317c8984c610000000048473044022046628accc862ea34ab15232f97505cf673d8bfd23d6316677e524e3643e92a20022078414e64419c96474fe2559c30134ac4c08b5a0617a0dc9bd1ce09e85a8df89001feffffff927673288f7c95f452e035b65c8cd46a57e58451b93dcfecfae0c33f00b4e5350000000049483045022100b9e84841140ae7b9bf08f82e014247a8c270d4073b457fbee74743c413e0b4370220292fc63652cd2fae0d1baf9c705de61478b2ec8d4623b9ecaf2aca715c1e69d801feffffff9477cc8e7dddfa7d183bfe0771def3778e7b2641996a3ea52f42d085d4007d190000000048473044022073842db3431ea57cb4aa05435648817bacb36a623e2528817e399126068fbd8b02206744687cfc5587f07d6a507eeeb2aaff45731b3dd9222c40f2b62b60e4db59b301feffffff948a1e5af04f265b29fd23700d1ac9926b5bed71ed5b2968f29abaa15036848c000000004847304402207c5440b72bc608cdf4c7fad0bccdc19d43877e31b22fe3f5873f558a6068e28c022013e3a5b0b11eeec0bfd5cc8317c8a61ccf28ce19a1b50fd7759502a350b991e401feffffff98a1cd6c74d9d42f88032e74182cfe8e71f125eb7eb1b49e8334d5b17bf4d07e00000000484730440220393955bb76c236467d92d42091a290631cbcd9ef3c3f177ace6f1ce73abe319f0220153d5c0aef39f5cea8ef53822993e374dc6d66a758d599f25d2e934d8c97769601feffffff9a7fefd1b1409dfc23d6be09dab5692cd9f6c59c98b2d7b0231f40b396999c2b000000004847304402201f9d944711c3ee35c47b68ddac1a0e1f728884847d8df788b398157de22e9bbd022005d97ceca294e96f5484420189d7a99b9850ecb2c849223ddb934c6c772e32f401feffffff9b0ed42c0446f8ea3c19b47be97f42d1a546bbd6a5a311cded5c1dd16c3606d40000000049483045022100d42b4c9c6fbcbd65d69f0967cca562227f8fbab7ca2727822eb9eb4d0ce8e77a022049d752916ee19c285675786aa04c37d7025e2cef6907f70849f55cda414f3fb501feffffff9ba78bb678f5b7a289ca37b49835bc6ad383e2089dd3711833383c0c6e6d40cb000000004847304402205d3a652a05971d324947fb9d4d15e98393262498e09a6d8fdde7422af91d341a022070e017f2edf61310cb724401a451c1d2be59175e68b49e5c1f82f20084f0b2e501feffffff9d2bdc85ec46fb0457dd41f02f5f7b203ff8c844062f3376c7f86cf2144dc6a6000000004847304402202f93a774f96364ad8fdf46132f47dde1fac4b833d1cf7c20c6c69f03c605c09702207cf7ef42d8c97b96e349d023efd9e7e0b1fd74c50561290d16f3f122e1ead8fb01feffffff9dc64c498135ebd6c025d7d43ae71120d6477bcbcd9828aebe21911ea21655c80000000049483045022100f72cd391c5dd1bc77de0605a3cb35c246a5c1cc14e7b9b3fc1cdd90fd42cfa4b022069049bca8a2f5100ada2a407a2354d04efa94573a7cd1bfa4130cde66e481a1001feffffffa0c3203666c02ea6f958408c8f2241b4d6e3a8beb9ab54736fe73621feb57ce40000000049483045022100daa9b7a48975348b41dfdf8b5e4614721fd018b950d3cec1d7009386bffddb470220522220c5f3ad8f1f19cb0eafea1aae7a3489cdd3dcb3d64f2ce75bd2066a73dd01feffffffa14e8b18777a8710e58942b56d094243151299f033cc21bb3ad3dfce2b3e77ad0000000049483045022100a9e02b9ad05da478a1cf06a235743d202d1f9e8c2e969ea8b1b7d5fe6778fd9602203880f139bf40766d264c2d7f858eb36dc2257b4cacd116cacca400645f80680401feffffffa262a97a28944d41d47c7f8788528c797d322f7abc0390c20bf22e3b835e127a0000000048473044022059a9da8cb72d3d3967ad3adcfb400ee6043ee088707424728de63cba9361da2102206ca3e6681ff149bff11135315d431e24e05aa3c794b41ef0822b8969b0d1597401feffffffaa3c2496b8237d865f81ff0bb8eb01bf2b69ee806463816ec83b60cace7a5833000000004847304402205637e4e9538fa7489e017da763bce9182c5e78492fe23d5366c0638af15c7eef022034e9a552d342053c4184cea58684ffbd0881467cd0a40f009db155275deae1c001feffffffabfc5cf05834234e1ee8a3c87c8de5d6a07f9530a09f2b34d9303ef30d8646cf0000000049483045022100a68eff499320029204dd73f707d36d65583d21ebfa063d770f55139ed546ea8102206646e141b55f506ed457f24311eeec6e302833f69cd08c9ea3086c78f82dfd3801feffffffa2d1512943366ab64e6d1749b81f993e830e5b546a87b9bd68fe0c5c865da953010000006b483045022100c686f7a4b2e8af7deca60cb20b0c626609548f5426dda6bf33207f82923e0ea202200d9c36dc490f014d0d4970ce8c18621d39b6c0c134c7e43da0f62326725598ba01210360cfa32fd05b4c3bc270fc6e8c891af45a149d34664746ffc67f5cb49c6b5f5bfeffffffad976a10bc9ebe391cee6b83191520a9d0fb62a24e969477a4cc6dd26b29e4da000000004847304402203385b46d676be7f898b316fdcf56a8521bda2224ae891b48be05cd880ae7a0e502201f6de4117623336529e445e0943c519e80150cf0d4a5b1427766d06db2d7a26b01feffffffadd486a6d94629b19713d723301b135c11af92b5ed69e6f0b9ed07d417078b2400000000484730440220575a03c7a331f65defeab66ab1404503a700ece0780889266bd1866ff806096b022069348e446f67f551949267b49861e96904e0b47c75a220aa1cd7ffec3b8fa7d801feffffffb04574d6517ca90a26e07a749ebcde23f67f7ef8a594b23e699fa084529d96e80000000049483045022100948f7ec200d121bdea79b29bf1c608c6d5e007aec62acfb3a5cbcae84ce457490220431802ca646caacfeaf1827e1ceb70f07752413c65bb50db24957166603bab3f01feffffffb2197245ddc53b189c18d05d167210fd6291c6b9116862144c3654da5bb55d06000000004847304402204def3dfa143d5887b4075f45d92a91df9825f1e08bee1c29901c1f117ab30df302207eff300c5347d13f531ec36789a6f4f66c07149ff4c86f21107d0f21dc400d9e01feffffffb4b953583df750085d727027674f69c6ba63513915941e42924a462d5bc15c9b0000000049483045022100a267fdd914d9ce78ca819e08312fb2b3c0f9c395bd30d22b26ea8c6a8af3618f0220548b821abd8f1f1fec1db25fbc277cbfc5840e47185a830174a97b74645af60401feffffffb7f5149ac38efb591ad8c3a46ec9e979d5647c964190a135342435b55484dd570000000049483045022100d1d05a271a8516b9357b0e3e73d5413aa138ae9a10c1ccbe30ba7ef15994c24202203df3584a99260ff637db9515361b258e6cf7fbbfa15278b29173dd2c4f25264901feffffffbfc02225e0c5351bbeb63adb8e3b7859752363a5b85f5b2a6da5240a449e8065000000004948304502210082c85c2c7d8316e9e3cfba9f5bafcdbbeaf0509c3e896bd4121f19e4b82cbfe6022070d7650714cb1975215fe109b8f1da2eea866abbdf05e487eb1d75e12776e52d01feffffffc0def09bb3cbf791c52764cceadd389199be9d7603cc3d6d213ba45ffc98518d0000000049483045022100841df35265191f063a9ad2414ec9b36fe39ef9ae13c9fde0e82d67ec9bc654e302206dd8523cf58547ab425ea55a8d879e75d31558701d4f57d76b0f67736ca5e5ea01feffffffc5c9957c3a3e03204e603c313368d3c01206320beddfd28b850fd17b09a61a410000000049483045022100c3467add04b9e313238376a0d3867bc5b59fca8b2eb76bcc18fbc0b0805e63960220578a2cf379848771a9b13e12559cd130853c7f02d9ab497a74f3305aeaf7b00b01feffffffc64396e634d716a5ae280d9fd821507239d7b25a812eea6751254e462c8a73a50000000048473044022040e5e55b23846cbd5e0af588564e5501d58cf2a18eb485c562352fe2801230d002200c70fcf828a81c1cfb856a2d2cc9de21f2564e6080b2f84f44c65b679f49d09c01feffffffc69c9cdd6825a657be1a06008f73b78cf185a9d195ba771451ca1ec09ce54d4f0000000049483045022100e10488858800081f775278c5d844ba2c2cda71ebb4a822d028637191e13efb2602203f7e7f580dad9d7ed1d4cda38222095d8377917c7d4e90c8abb4b9bf3a40975c01feffffffca6112fdc1db1a441961f6eb62b492c1397732cc5519d40f6aa335612f42d39c000000004948304502210097ed9842254112825356823d7365ce8d0bbc973702be7f25951e21f48fcd6e5702203a0aab0ef62926936815e1d9490b335359f766d0ace9b858d59bbd8ba26cb1d901feffffffcb15dbc245dec1ef8cb8e25ef11921ca804c023e6ad803ebcb2a7b98380b60b30000000049483045022100bb9285cab4a68dcb68b46687b59ab1769a0b5aa1ea6f45488e189f58e698321f02205e6499101ee3b0f005e6d3ba151282c236a79d32488e16b1867c6e70c8f7f51001feffffffcfe47e6ce0780c4594a2d1b76a2906c0a9ea32d39a73c244aa9d5d8dea67248c0000000049483045022100a4681709fd0b79ceaddd9d695bd5c740391970a1feff2dd3a90674d20ca95a2a022076dbad3df0c4f8158eba4a087650feeeb1736b5a8b03aef15f698be4fc668abd01feffffffd0a4d502c22cea7da0d1a3cf99aef598b74fad19a6de35f21c6fd0d1b8cf275600000000494830450221009d8a22fe94f18d0a65e8f188b702b4023948e236ac2efd36bfb20d2054e1d55402201383ab2ed9465790eb9496483f10f54e40ae201fb98358cbdd71a0e650ad1b9701feffffffd25452b8575cafca10255179f95c8c66e255329220b7ff645af522af7b8038320000000048473044022013581d5e4794efb6df6dbe04339478ecf019493814d9d52390b6cc790c998762022006aef7acc10019a8cfd7ae99e11e5877a9cf1a5a6ef084549815435f7b681e1801feffffffd3922dfd1a65216bbcd4646d0cbcfa70cfe587775cf4c673043c57061f48d763000000004847304402200bc9095368e4409c7debdf0871f18af1d36e1a4851e4b948a1ce362926550611022034fb19afe76cf133e4bb561fcd3cfe7f3d49743fd75022c124b6e45bd9f503cd01feffffffd75c777645d534009bc8e7b2c0b58a78cd63f41f47f6cd30868aeaf9b55e477000000000494830450221008f4a11d94e97f02e3226c509c70a3582a280ea3bf33309ec392ceeda7a59567e022044bf0d858442058b7c5fd8c73e47287f9283e957fdb39fc005cef70e22b0c07001feffffffd8f837530faf0d9b50efe1d79aed453b11916d565a2b9c40a380a85f0be2af6b0000000048473044022065ac672cfaffe8f8d02fb8064cb54f4d335e7af222452ee71c9b249602cbfcac02202cdb7e8cc05c52db51b71a05258abaf0810d61199eff9ee0ea37d8c373a876ab01feffffffdbce76e284668c829366dafd00ae4884ea39b2aa597cc1b4d2a37991a9b2ea56000000004847304402204480dd6aac1167bb49f32fc04feaa3a7c19ad6cba48479cb72dc7d0bd71ca279022036e654a48cadceba49dbb097892ce5d90d8f082460fb18776d353e9d832ba83301feffffffe481d9493d67997104c12972b7c8a73fb87b16e228665bb784436fc0f58d7e66000000004847304402203645fe9770f3851392a85b8dc9dd405ab13fd8434122f6763de459129527fd0702204d240e91298a1487d496feb320dee028df7dbb5c9236e5d62a4964347f97279001feffffffe7a22d3d87255e4adaab9a6fd8a72320299a6902426424aa8b2b89b7c3b0c0950000000049483045022100b362e030a6739f020622f0f7e34c48fc4ff6147ed88a194a37a8a04c8e42822a0220755bcc63667eb4cbcd52108d27245765176c6c5b2e9a77013aea4d7474c0a1ec01feffffffe80ac9635b6bd91c1935eca6df80876ac8cdc87a2b91e925cfdcc0f06059b2e5000000004847304402204a2b8c311a11920eef4d64e786c5f26ed82d4c1562f2cc0e73fd5a5374c7061e02203693e77f88372a335d1463df4edd062b6dfe2bb895d56d58f3a404c27757378501feffffffedad3357a1a9aeeb8c2771cc6f284db92a2aa31f458e35bb270216015bb0edd40000000049483045022100abad2415b7c6ca9ccf3c52b4008c4d531360f2d6541d9025ec2caa4d764b46da022054f5d2833704686a860fcf978313a3c6c61f16e9a1cf84a3e4ac76c8950dabb701feffffffee85afefc31a99a4616bfb228e1f48691976b900ecdfe838e1310bf5b33fadcf000000004847304402200f7afc12d43432f5303b892b08417743d43a05bf938719428a88c85e255e5b0d02201a12cc706286a1c9329f9e37e62143866563b3773769def6912494a73c17a9f201fefffffff13e4784de0564595f3b4cce57ec0d8a4b72a798feb65f5fbca5b26a3a91d0760000000049483045022100fd3c9b2e02db889ae2bd43537a308a87a7d701bac19083e3a985a93674239e2802206dd36da12f3f2b222ce4387cb91e1098c5f93d25ce95fed0e5d21e6724af554401fefffffff205212771fd3ca5a68340fa307810e44315ae02464b5d8a235ba6bca691bd710000000048473044022062aa2571a91a7e06f0e96570bb3a348296ce7b756ceed48fe69be91f94a6c5c70220631885aa6fc967e40cd1820c83310143884e175227c5434e33b89245598d5e5c01fefffffff31cea9351fddc36393fa996962e204c461a34ff1c6ad243b3a4902440f165da000000004847304402203355527ee222e6bc756ef30c6ad687a21109a5175b1eb27592e9e1938b9e8f850220206ea10896e9e307ee73d33813048fece04bbeda702e11cae8bd61297b73590601fefffffff3c67e78777cc42ae2834bcf5dce5493fbcfcc6e0aabd7608cf4f9c936a37f49000000004847304402207cd40b7d6ca2b869d3f00c0babb484c7a2896c080c593767e0a293acd1505a9c02203a2f8c191b20fe4fb08958b3bb20411834d17f7fa075deb8b2272d22112ec8b001fefffffff3ddc14df664f6e4f59b1f1e25241a61fc69f13125ea5a67edbd03b37d332eb50000000049483045022100a40f81d4e1791d0253a2484656c27994d1e42aaaf77995e9fa6e0eb02480bde30220669c0bfbd0772ec1ad8ca9357eb3ca1100d7b40ed97bb34e23c8cecb42511c7001fefffffff614bd5d83278ad95d8c5bf6fefe59b3675e832cc1c2349d7952aa734fd20283000000004847304402207709f2089f820012e76eaa6221aa0b9776cbdcd0b0b458d400c7c1ca9ed7eedb02200de75bbdae8100b4b27e5deb164e13d596b6661248be45d817b573cdf8cb2c7c01fefffffff67ef42d75fc5d36ff32ab40f5c9f88f279a1173ee1db227a4706aa0480d66ab0000000049483045022100b09aa2cca247052451537f64801ea561506bff82794a8870c077c32c69d0bebc022013bceb4edd8f126af25c07a74d5c16935b0e916cdcc25d49ee335c430400eb2601fefffffff69f0798ab6de485dcfe72391f4cbb1e5f4d39ee8f852b80fd4bb730eabd8e9300000000494830450221009d91a34a7294250ac5b31bc86a2f7ceac8ce79e49d8ac7b3b02ad0cc278f16d102207b9ea41b03e72746a67e7bedfd1cad7f5055a915abdabc13f8e51815f29e983601fefffffff8dd75e7c674cf7bf15f42fcb1256ef4f16b96e0ff6a359bc24c07ba734f09a30000000049483045022100cf9283df82dc2c0d26c2fc9349d16faf2c961919066798705da4afe6fbf27af202207740172e195f5713eff2aeb39d12923625401dea6a0c4b4aa19be3b973c9077601fefffffffa0c47583d4c6f18e12b93764ccf57d2430a52bdd0ceb611924a79c82daf48b9000000004847304402207b46c5dfb4e65c5f91f9770acca2a1ad24a4cdd7e4f27ac9c5e55b14f8d7c00202203b17ab29bd9be1559d550cae9f79728a644682a8aab5db1a1cc3432bad159f4701fefffffffa5ca0440f302bcf118946714dba6e81036e48477ff3a315084fe682aea6d1d50000000049483045022100929668780086aa4c8945fc6d9aaa340ee8ae2807ff2f6a89623ffa102d2bdf6d0220318d3e075a82195af58a66b47c8d62849d69ed1da2e07402d89440a6a77b63ba01fefffffffef369694bf0493161762e49d7ca16f1ba600250d801a848d0ca8d3f2d677d4a0000000049483045022100f7dd5f966156c81a1d2aa694befa6b19e35aa8d7fa199c37a803cd382836fdbe0220669d85a44632a8ea6093b783693c4626ad8c71be4b82b027c4cdfa63682a9a1601feffffff02c5490f00000000001976a9146843838a0aa11686cd0c01fbf470c9c5f302249488ac40420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000",
      "txid": "a44feb2e788d0332e283d8ca69c6a20999944dccac93246cbf9b36d841b08c95",
      "overwintered": false,
      "version": 1,
      "locktime": 0,
      "vin": [
        {
          "txid": "281ffa432d39c56b28c4a79ae495cb5c6b4634b4f4a298958e6e0f3fef1feb0a",
          "vout": 0,
          "address": "RRqqaWq8QLfpBHtAit4hXfEfV37WXT5Myo",
          "scriptSig": {
            "asm": "30440220234b370cddf91b27e172cb5d6257a9807e63cf680a644229147b39d87e597875022047a58509a11b190107a9ff6e08143bd0d450db233518ed26f123bd739576e9c201",
            "hex": "4730440220234b370cddf91b27e172cb5d6257a9807e63cf680a644229147b39d87e597875022047a58509a11b190107a9ff6e08143bd0d450db233518ed26f123bd739576e9c201"
          },
          "sequence": 4294967294
        }
      ],
      "vout": [
        {
          "value": 0.01001925,
          "valueZat": 1001925,
          "valueSat": 1001925,
          "n": 0,
          "scriptPubKey": {
            "asm": "OP_DUP OP_HASH160 6843838a0aa11686cd0c01fbf470c9c5f3022494 OP_EQUALVERIFY OP_CHECKSIG",
            "hex": "76a9146843838a0aa11686cd0c01fbf470c9c5f302249488ac",
            "reqSigs": 1,
            "type": "pubkeyhash",
            "addresses": [
              "RJnVEQgucK1iwiRjfTZmreXkF49KgTErDn"
            ]
          }
        }
      ],
      "vjoinsplit": [
      ]
    },
    "error": null,
    "id": "curltest"
  }

sendrawtransaction "hexstring" ( allowhighfees )
------------------------------------------------

The ``sendrawtransction`` method submits raw transaction (serialized, hex-encoded) to local nodes and the network.

Also see ===link=== ``createrawtransaction and ``signrawtransaction`` calls.

Arguments:

::

	"hexstring"    (string, required) the hex string of the raw transaction)
	allowhighfees    (boolean, optional, default=false) allow high fees

Result:

::

	"hex"             (string) the transaction hash in hex

Examples:

Create a transaction

::

  command:

	komodo-cli createrawtransaction '[{"txid" : "a44feb2e788d0332e283d8ca69c6a20999944dccac93246cbf9b36d841b08c95","vout":0}]' '{"RHCXHfXCZQpbUbihNHh5gTwfr7NXmJXmHi":0.01}'

  response:

  0100000001958cb041d8369bbf6c2493accc4d949909a2c669cad883e232038d782eeb4fa40000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000

Sign the transaction, and get back the hex

::

  command:

	komodo-cli signrawtransaction "0100000001958cb041d8369bbf6c2493accc4d949909a2c669cad883e232038d782eeb4fa40000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"

  response:

  {
    "hex": "0100000001958cb041d8369bbf6c2493accc4d949909a2c669cad883e232038d782eeb4fa4000000006a4730440220242c38740261799f9b6ccbde8f941e2567e86c84108c508d108d062ab9677b6e02206fea089b28c6d66d1c8f2343e1de7960dadafa3cf268c00f7dbe391cd8b9365f01210384c0db4f1eaa142a2745742b942f989375dbec32c55310a793225bb5c43cdc98ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000",
    "complete": true
  }

Send the transaction (signed hex)

::

  command:

	./komodo-cli -ac_name=SIDD sendrawtransaction "0100000001958cb041d8369bbf6c2493accc4d949909a2c669cad883e232038d782eeb4fa4000000006a4730440220242c38740261799f9b6ccbde8f941e2567e86c84108c508d108d062ab9677b6e02206fea089b28c6d66d1c8f2343e1de7960dadafa3cf268c00f7dbe391cd8b9365f01210384c0db4f1eaa142a2745742b942f989375dbec32c55310a793225bb5c43cdc98ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"

  response:

  f1e041b2e2f1dafd331535d8277193aa27c33309a801949e0739a6b31c3d8a56

As a json rpc call

::

  command:

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "sendrawtransaction", "params": ["0100000001958cb041d8369bbf6c2493accc4d949909a2c669cad883e232038d782eeb4fa4000000006a4730440220242c38740261799f9b6ccbde8f941e2567e86c84108c508d108d062ab9677b6e02206fea089b28c6d66d1c8f2343e1de7960dadafa3cf268c00f7dbe391cd8b9365f01210384c0db4f1eaa142a2745742b942f989375dbec32c55310a793225bb5c43cdc98ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": "f1e041b2e2f1dafd331535d8277193aa27c33309a801949e0739a6b31c3d8a56",
    "error": null,
    "id": "curltest"
  }

signrawtransaction "hexstring" ( [{"txid":"id","vout":n,"scriptPubKey":"hex","redeemScript":"hex"},...] ["privatekey1",...] sighashtype )
-----------------------------------------------------------------------------------------------------------------------------------------

The ``signrawtransaction`` method signs inputs for a raw transaction (serialized, hex-encoded). The second optional argument (may be null) is an array of previous transaction outputs that this transaction depends on, but may not yet be in the block chain. The third optional argument (may be null) is an array of base58-encoded private keys that, if given, will be the only keys used to sign the transaction.

* Note: For full details, please see https://bitcoin.org/en/developer-reference#signrawtransaction

Arguments:

::

	"hexstring"     (string, required)  the transaction hex string
	"prevtxs"       (string, optional) an json array of previous dependent transaction outputs
	     [
	       {
	         "txid"             (string, required) the transaction id
	         "vout"                  (numeric, required) the output number
	         "scriptPubKey"   (string, required) script key
	         "redeemScript"   (string, required for P2SH) redeem script
	         "amount"            (numeric, required) the amount spent
	       }
	       ,...
	    ]
	"privatekeys"     (string, optional) a json array of base58-encoded private keys for signing
    [
      "privatekey"   (string) private key in base58-encoding
      ,...
    ]
	"sighashtype"     (string, optional, default=ALL) the signature hash type; the following options are available: "ALL" | "NONE" | "SINGLE" | "ALL|ANYONECANPAY" | "NONE|ANYONECANPAY" | "SINGLE|ANYONECANPAY"

Result:

::

	{
	  "hex"                (string) the hex-encoded raw transaction with signature(s)
	  "complete"           (boolean) if the transaction has a complete set of signatures
	  "errors" : [
	    {
	      "txid"           (string) the hash of the referenced, previous transaction
	      "vout"           (numeric) the index of the output to spent and used as input
	      "scriptSig"      (string) the hex-encoded signature script
	      "sequence"       (numeric) script sequence number
	      "error"          (string) verification or signing error related to the input
	    }
	    ,...
	  ]
	}

Examples:

::

  command:

	komodo-cli signrawtransaction "0100000001958cb041d8369bbf6c2493accc4d949909a2c669cad883e232038d782eeb4fa40000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"

  response:

  {
    "hex": "0100000001958cb041d8369bbf6c2493accc4d949909a2c669cad883e232038d782eeb4fa4000000006a4730440220242c38740261799f9b6ccbde8f941e2567e86c84108c508d108d062ab9677b6e02206fea089b28c6d66d1c8f2343e1de7960dadafa3cf268c00f7dbe391cd8b9365f01210384c0db4f1eaa142a2745742b942f989375dbec32c55310a793225bb5c43cdc98ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000",
    "complete": true
  }

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "signrawtransaction", "params": ["0100000001958cb041d8369bbf6c2493accc4d949909a2c669cad883e232038d782eeb4fa40000000000ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": {
      "hex": "0100000001958cb041d8369bbf6c2493accc4d949909a2c669cad883e232038d782eeb4fa4000000006a4730440220242c38740261799f9b6ccbde8f941e2567e86c84108c508d108d062ab9677b6e02206fea089b28c6d66d1c8f2343e1de7960dadafa3cf268c00f7dbe391cd8b9365f01210384c0db4f1eaa142a2745742b942f989375dbec32c55310a793225bb5c43cdc98ffffffff0140420f00000000001976a91456def632e67aa11c25ac16a0ee52893c2e5a2b6a88ac00000000",
      "complete": true
    },
    "error": null,
    "id": "curltest"
  }

Util
====

createmultisig nrequired ["key",...]
------------------------------------

The ``createmultisig`` method creates a multi-signature address with ``n`` signature of ``m`` keys required. The method returns a json object with the address and redeemScript.

Arguments:

::

	number_required        (numeric, required) the number of required signatures out of the ``n`` keys or addresses.
	"keys"                 (string, required) a json array of keys which are KMD/asset-chain addresses or hex-encoded public keys

 [
   "key"                 (string) KMD/asset-chain address or hex-encoded public key
   ,...
 ]

Result:

::

	{
	  "address"            (string) the value of the new multisig address.
	  "redeemScript"       (string) the string value of the hex-encoded redemption script.
	}

Examples:

Create a multisig address from 2 addresses

::

  command:

	komodo-cli -ac_name=SIDD createmultisig 2 "[\"RJnVEQgucK1iwiRjfTZmreXkF49KgTErDn\",\"RCVyjn9MQ8Tw6YRJnDcsx67kfsmfUgLdfw\"]"

  response:

  {
    "address": "bZjsy6bt2ZdyHV5hfCNL2HsuA4eV63s5u6",
    "redeemScript": "52210384c0db4f1eaa142a2745742b942f989375dbec32c55310a793225bb5c43cdc9821021f527b7269ab18da85a50b7f45f572e8b017fce476de06cb80a2550ee7d4b11652ae"
  }

::

  command:

  ===not working yet====

	curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "createmultisig", "params": [2, \'["RJnVEQgucK1iwiRjfTZmreXkF49KgTErDn","RCVyjn9MQ8Tw6YRJnDcsx67kfsmfUgLdfw"]\'] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

estimatefee nblocks
-------------------

The ``estimatefee`` method estimates the approximate fee per kilobyte. The method is needed for a transaction to begin confirmation within ``nblocks`` blocks.

Arguments:

::

	nblocks     (numeric)

Result:

::

	n :    (numeric) estimated fee-per-kilobyte

  The value ``-1.0`` is returned if not enough transactions and blocks have been observed to make an estimate.


Example:

::

  command:

	komodo-cli estimatefee 6

  response:

  0.00019376

estimatepriority nblocks
------------------------

The ``estimatepriority`` method estimates the approximate priority of a zero-fee transaction, when it needs to begin confirmation within ``nblocks`` blocks.

Arguments:

::

	nblocks     (numeric)      a statement indicating within how many blocks the transaction should be confirmed

Result:

::

	n    (numeric) estimated priority

  -1.0 is returned if not enough transactions and blocks have been observed to make an estimate.

Example:

::

  command:

	komodo-cli estimatepriority 6

  response:

  ===need to come back to this, getting -1===

invalidateblock "hash"
----------------------

The ``invalidateblock`` method permanently marks a block as invalid, as if it violated a consensus rule.

Arguments:

::

	1. hash   (string, required) the hash of the block to mark as invalid

Result:

::

  (none)

Examples:

::

  command:

	komodo-cli invalidateblock "02f51fb2793b0728050c5e983ffed669594e0a2dda01dcb7a68d129fd87436e0"

  response:

  (none)

::

  command:

  curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "invalidateblock", "params": ["02f51fb2793b0728050c5e983ffed669594e0a2dda01dcb7a68d129fd87436e0"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

  response:

  {
    "result": null,
    "error": null,
    "id": "curltest"
  }

jumblr_deposit "depositaddress"
-------------------------------

For usage look at :doc:`using-JUMBLR`

jumblr_pause
------------

For usage look at :doc:`using-JUMBLR`

jumblr_resume
-------------

For usage look at :doc:`using-JUMBLR`

jumblr_secret "secretaddress"
-----------------------------

For usage look at :doc:`using-JUMBLR`

reconsiderblock "hash"
----------------------

The ``reconsiderblock`` method removes invalidity status of a block and its descendants, reconsidering them for activation. This can be used to undo the effects of invalidateblock.

Arguments:

::

	hash   (string, required) the hash of the block to reconsider

Result:

  (none)

Examples:

::

	komodo-cli reconsiderblock "02f51fb2793b0728050c5e983ffed669594e0a2dda01dcb7a68d129fd87436e0"

validateaddress "komodoaddress"
-------------------------------

The ``validateaddress`` method returns information about the given KMD/asset-chain address.

Arguments:

::

	"address"     (string, required) The KMD/asset-chain address to validate

Result:

::

	{
	  "isvalid"         (boolean) indicates whether the address is valid. If it is not, this is the only property returned.
	  "address"   (string) the address validated
	  "scriptPubKey"       (string) the hex encoded scriptPubKey generated by the address
	  "ismine"          (boolean) indicates whether the address is yours or not
	  "isscript"    (boolean) if the key is a script
	  "pubkey"           (string) the hex value of the raw public key
	  "iscompressed"     (boolean) if the address is compressed
	  "account"          (string) DEPRECATED. The account associated with the address, "" is the default account
	}

Examples:

::

  command:

	komodo-cli validateaddress "RDNC9mLrN48pVGDQ5jSoPb2nRsUPJ5t2R7"

  response:

  {
    "isvalid": true,
    "address": "RDNC9mLrN48pVGDQ5jSoPb2nRsUPJ5t2R7",
    "scriptPubKey": "76a9142cd2a4e3d1c2738ee4fce61e73ea822dcaacb9b488ac",
    "segid": 9,
    "ismine": true,
    "iswatchonly": false,
    "isscript": false,
    "pubkey": "03c376b00b3a2ae43b8bf103a6c6962b241de684383301fe628a460b68a79ac1d8",
    "iscompressed": true,
    "account": ""
  }

verifymessage "address" "signature" "message"
---------------------------------------------------

Verify a signed message

Arguments:

::

	"address"         (string, required) the address to use for the signature
	"signature"       (string, required) the signature provided by the signer in base 64 encoding (see signmessage)
	"message"         (string, required) the message that was signed

Result:

::

	true|false   (boolean) indicates whether the signature is verified

Examples:

===come back to this after we've done `signmessage` and others in the wallet category===

Unlock the wallet for 30 seconds

::

	komodo-cli walletpassphrase "mypassphrase" 30

Create the signature

::

	komodo-cli signmessage "t14oHp2v54vfmdgQ3v3SNuQga8JKHTNi2a1" "my message"

Verify the signature

::

	komodo-cli verifymessage "t14oHp2v54vfmdgQ3v3SNuQga8JKHTNi2a1" "signature" "my message"

z_validateaddress "zaddr"
-------------------------

The ``z_validateaddress`` method returns information about the given z address.

Arguments:

::

	"zaddr"     (string, required) the z address to validate

Result:

::

	{
	  "isvalid"      (boolean) indicates whether the address is valid; if not, this is the only property returned
	  "address"         (string) the z address validated
	  "ismine"       (boolean) indicates if the address is yours or not
	  "payingkey"         (string) the hex value of the paying key, a_pk
	  "transmissionkey"   (string) the hex value of the transmission key, pk_enc
	}

Examples:

::

  command:

	komodo-cli z_validateaddress "zcWsmqT4X2V4jgxbgiCzyrAfRT1vi1F4sn7M5Pkh66izzw8Uk7LBGAH3DtcSMJeUb2pi3W4SQF8LMKkU2cUuVP68yAGcomL"

  {
    "isvalid": true,
    "address": "ztdChvxs2Z97X7qeBwsnRLbxva1ZVgWhFWZxZTA5bC8XLt9RHF8uXn16MWCU8DhKEt4gTtKqQwzsrk85f5tThWMNoYds2oX",
    "payingkey": "d9c09cb974fbe0bf7e36a2318b46396c5112511f90749531428936867d83bd92",
    "transmissionkey": "5ce3250912758cbb591e3d585ef110992f25ed7694b88f55315b060698b75404",
    "ismine": true
  }
