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

List all banned IPs/Subnets.

Examples:

::

	> komodo-cli listbanned
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "listbanned", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

ping
----

Requests that a ping be sent to all other nodes, to measure ping time.
Results provided in getpeerinfo, pingtime and pingwait fields are decimal seconds.
Ping command is handled in queue with all other commands, so it measures processing backlog, not just network ping.

Examples:

::

	> komodo-cli ping
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "ping", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

setban "ip(/netmask)" "add|remove" (bantime) (absolute)
-------------------------------------------------------

Attempts add or remove a IP/Subnet from the banned list.

Arguments:

::

	1. "ip(/netmask)" (string, required) The IP/Subnet (see getpeerinfo for nodes ip) with a optional netmask (default is /32 = single ip)
	2. "command"      (string, required) 'add' to add a IP/Subnet to the list, 'remove' to remove a IP/Subnet from the list
	3. "bantime"      (numeric, optional) time in seconds how long (or until when if [absolute] is set) the ip is banned (0 or empty means using the default time of 24h which can also be overwritten by the -bantime startup argument)
	4. "absolute"     (boolean, optional) If set, the bantime must be a absolute timestamp in seconds since epoch (Jan 1 1970 GMT)

Examples:

	> komodo-cli setban "192.168.0.6" "add" 86400
	> komodo-cli setban "192.168.0.0/24" "add"
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "setban", "params": ["192.168.0.6", "add" 86400] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

Rawtransactions
===============

createrawtransaction [{"txid":"id","vout":n},...] {"address":amount,...}
------------------------------------------------------------------------

Create a transaction spending the given inputs and sending to the given addresses.
Returns hex-encoded raw transaction.
*Note that the transaction's inputs are not signed, and
it is not stored in the wallet or transmitted to the network.*

Arguments:

::

	1. "transactions"        (string, required) A json array of json objects
	     [
	       {
	         "txid":"id",  (string, required) The transaction id
	         "vout":n        (numeric, required) The output number
	       }
	       ,...
	     ]
	2. "addresses"           (string, required) a json object with addresses as keys and amounts as values
	    {
	      "address": x.xxx   (numeric, required) The key is the Zcash address, the value is the ZEC amount
	      ,...
	    }

Result:

::

	"transaction"            (string) hex string of the transaction

Examples:

	> komodo-cli createrawtransaction "[{\"txid\":\"myid\",\"vout\":0}]" "{\"address\":0.01}"
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "createrawtransaction", "params": ["[{\"txid\":\"myid\",\"vout\":0}]", "{\"address\":0.01}"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

decoderawtransaction "hexstring"
--------------------------------

Return a JSON object representing the serialized, hex-encoded transaction.

Arguments:

::

	1. "hex"      (string, required) The transaction hex string

Result:

::

	{
	  "txid" : "id",        (string) The transaction id
	  "overwintered" : bool   (boolean) The Overwintered flag
	  "version"          (numeric) The version
	  "versiongroupid": "hex"   (string, optional) The version group id (Overwintered txs)
	  "locktime"        (numeric) The lock time
	  "expiryheight"     (numeric, optional) Last valid block height for mining transaction (Overwintered txs)
	  "vin" : [               (array of json objects)
	     {
	       "txid": "id",    (string) The transaction id
	       "vout"         (numeric) The output number
	       "scriptSig": {     (json object) The script
	         "asm": "asm",  (string) asm
	         "hex": "hex"   (string) hex
	       },
	       "sequence"     (numeric) The script sequence number
	     }
	     ,...
	  ],
	  "vout" : [             (array of json objects)
	     {
	       "value"            (numeric) The value in ZEC
	       "n"                    (numeric) index
	       "scriptPubKey" : {          (json object)
	         "asm"          (string) the asm
	         "hex"          (string) the hex
	         "reqSigs"            (numeric) The required sigs
	         "type"  (string) The type, eg 'pubkeyhash'
	         "addresses" : [           (json array of string)
	           "t12tvKAXCxZjSmdNbao16dKXC8tRWfcF5oc"   (string) zcash address
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

	> komodo-cli decoderawtransaction "hexstring"
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "decoderawtransaction", "params": ["hexstring"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

decodescript "hex"
------------------

Decode a hex-encoded script.

Arguments:

::

	1. "hex"     (string) the hex encoded script

Result:

::

	{
	  "asm":"asm",   (string) Script public key
	  "hex":"hex",   (string) hex encoded public key
	  "type":"type", (string) The output type
	  "reqSigs"    (numeric) The required signatures
	  "addresses": [   (json array of string)
	     "address"     (string) Zcash address
	     ,...
	  ],
	  "p2sh","address" (string) script address
	}

Examples:

::

	> komodo-cli decodescript "hexstring"
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "decodescript", "params": ["hexstring"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

fundrawtransaction "hexstring"
------------------------------

Add inputs to a transaction until it has enough in value to meet its out value.
This will not modify existing inputs, and will add one change output to the outputs.
Note that inputs which were signed may need to be resigned after completion since in/outputs have been added.
The inputs added will not be signed, use signrawtransaction for that.

Arguments:

::

	1. "hexstring"    (string, required) The hex string of the raw transaction

Result:

::

	{
	  "hex":       "value", (string)  The resulting raw transaction (hex-encoded string)
	  "fee":       n,         (numeric) The fee added to the transaction
	  "changepos": n          (numeric) The position of the added change output, or -1
	}
	"hex"

Examples:

Create a transaction with no inputs

::

	> komodo-cli createrawtransaction "[]" "{\"myaddress\":0.01}"

Add sufficient unsigned inputs to meet the output value

::

	> komodo-cli fundrawtransaction "rawtransactionhex"

Sign the transaction

::

	> komodo-cli signrawtransaction "fundedtransactionhex"

Send the transaction

::

	> komodo-cli sendrawtransaction "signedtransactionhex"

getrawtransaction "txid" ( verbose )
------------------------------------

**NOTE**: By default this function only works sometimes. This is when the tx is in the mempool
or there is an unspent output in the utxo for this transaction. To make it always work,
you need to maintain a transaction index, using the ``-txindex`` command line option.

Return the raw transaction data.

If ``verbose=0``, returns a string that is serialized, hex-encoded data for 'txid'.
If ``verbose`` is non-zero, returns an Object with information about 'txid'.

Arguments:

::

	1. "txid"      (string, required) The transaction id
	2. verbose       (numeric, optional, default=0) If 0, return a string, other return a json object

Result (if verbose is not set or set to 0):

::

	"data"      (string) The serialized, hex-encoded data for 'txid'

Result (if verbose > 0):

::

	{
	  "hex" : "data",       (string) The serialized, hex-encoded data for 'txid'
	  "txid" : "id",        (string) The transaction id (same as provided)
	  "version"          (numeric) The version
	  "locktime"        (numeric) The lock time
	  "expiryheight"    (numeric, optional) The block height after which the transaction expires
	  "vin" : [               (array of json objects)
	     {
	       "txid": "id",    (string) The transaction id
	       "vout"         (numeric)
	       "scriptSig": {     (json object) The script
	         "asm": "asm",  (string) asm
	         "hex": "hex"   (string) hex
	       },
	       "sequence": n      (numeric) The script sequence number
	     }
	     ,...
	  ],
	  "vout" : [              (array of json objects)
	     {
	       "value"            (numeric) The value in ZEC
	       "n"                    (numeric) index
	       "scriptPubKey" : {          (json object)
	         "asm"          (string) the asm
	         "hex"          (string) the hex
	         "reqSigs"            (numeric) The required sigs
	         "type"  (string) The type, eg 'pubkeyhash'
    	     "addresses" : [           (json array of string)
    	       "zcashaddress"          (string) Zcash address
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
	  "blockhash" : "hash",   (string) the block hash
	  "confirmations"      (numeric) The confirmations
	  "time"              (numeric) The transaction time in seconds since epoch (Jan 1 1970 GMT)
	  "blocktime"         (numeric) The block time in seconds since epoch (Jan 1 1970 GMT)
	}

Examples:

::

	> komodo-cli getrawtransaction "mytxid"
	> komodo-cli getrawtransaction "mytxid" 1
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getrawtransaction", "params": ["mytxid", 1] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

sendrawtransaction "hexstring" ( allowhighfees )
------------------------------------------------

Submits raw transaction (serialized, hex-encoded) to local node and network.

Also see createrawtransaction and signrawtransaction calls.

Arguments:

::

	1. "hexstring"    (string, required) The hex string of the raw transaction)
	2. allowhighfees    (boolean, optional, default=false) Allow high fees

Result:

::

	"hex"             (string) The transaction hash in hex

Examples:

Create a transaction

::

	> komodo-cli createrawtransaction "[{\"txid\" : \"mytxid\",\"vout\":0}]" "{\"myaddress\":0.01}"

Sign the transaction, and get back the hex

::

	> komodo-cli signrawtransaction "myhex"

Send the transaction (signed hex)

::

	> komodo-cli sendrawtransaction "signedhex"

As a json rpc call

::

	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "sendrawtransaction", "params": ["signedhex"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/


signrawtransaction "hexstring" ( [{"txid":"id","vout":n,"scriptPubKey":"hex","redeemScript":"hex"},...] ["privatekey1",...] sighashtype )
-----------------------------------------------------------------------------------------------------------------------------------------

Sign inputs for raw transaction (serialized, hex-encoded).
The second optional argument (may be null) is an array of previous transaction outputs that
this transaction depends on but may not yet be in the block chain.
The third optional argument (may be null) is an array of base58-encoded private
keys that, if given, will be the only keys used to sign the transaction.


Arguments:

::

	1. "hexstring"     (string, required) The transaction hex string
	2. "prevtxs"       (string, optional) An json array of previous dependent transaction outputs
	     [               (json array of json objects, or 'null' if none provided)
	       {
	         "txid":"id",             (string, required) The transaction id
	         "vout":n,                  (numeric, required) The output number
	         "scriptPubKey": "hex",   (string, required) script key
	         "redeemScript": "hex",   (string, required for P2SH) redeem script
	         "amount": value            (numeric, required) The amount spent
	       }
	       ,...
	    ]
	3. "privatekeys"     (string, optional) A json array of base58-encoded private keys for signing
	    [                  (json array of strings, or 'null' if none provided)
	      "privatekey"   (string) private key in base58-encoding
	      ,...
	    ]
	4. "sighashtype"     (string, optional, default=ALL) The signature hash type. Must be one of
	       "ALL"
	       "NONE"
	       "SINGLE"
	       "ALL|ANYONECANPAY"
	       "NONE|ANYONECANPAY"
	       "SINGLE|ANYONECANPAY"

Result:

::

	{
	  "hex" : "value",           (string) The hex-encoded raw transaction with signature(s)
	  "complete" : true|false,   (boolean) If the transaction has a complete set of signatures
	  "errors" : [                 (json array of objects) Script verification errors (if there are any)
	    {
	      "txid" : "hash",           (string) The hash of the referenced, previous transaction
	      "vout"                (numeric) The index of the output to spent and used as input
	      "scriptSig"       (string) The hex-encoded signature script
	      "sequence"            (numeric) Script sequence number
	      "error" : "text"           (string) Verification or signing error related to the input
	    }
	    ,...
	  ]
	}

Examples:

::

	> komodo-cli signrawtransaction "myhex"
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "signrawtransaction", "params": ["myhex"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

Util
====

createmultisig nrequired ["key",...]
------------------------------------

Creates a multi-signature address with n signature of m keys required.
It returns a json object with the address and redeemScript.

Arguments:

::

	1. nrequired      (numeric, required) The number of required signatures out of the n keys or addresses.
	2. "keys"       (string, required) A json array of keys which are Zcash addresses or hex-encoded public keys

::

     [
       "key"    (string) Zcash address or hex-encoded public key
       ,...
     ]

Result:

::

	{
	  "address":"multisigaddress",  (string) The value of the new multisig address.
	  "redeemScript":"script"       (string) The string value of the hex-encoded redemption script.
	}

Examples:

Create a multisig address from 2 addresses

::

	> komodo-cli createmultisig 2 "[\"t16sSauSf5pF2UkUwvKGq4qjNRzBZYqgEL5\",\"t171sgjn4YtPu27adkKGrdDwzRTxnRkBfKV\"]"

As a json rpc call

::

	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "createmultisig", "params": [2, "[\"t16sSauSf5pF2UkUwvKGq4qjNRzBZYqgEL5\",\"t171sgjn4YtPu27adkKGrdDwzRTxnRkBfKV\"]"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

estimatefee nblocks
-------------------

Estimates the approximate fee per kilobyte
needed for a transaction to begin confirmation
within nblocks blocks.

Arguments:

::

	1. nblocks     (numeric)

Result:

::

	n :    (numeric) estimated fee-per-kilobyte

	-1.0 is returned if not enough transactions and blocks have been observed to make an estimate.

Example:

::

	> komodo-cli estimatefee 6

estimatepriority nblocks
------------------------

Estimates the approximate priority
a zero-fee transaction needs to begin confirmation
within nblocks blocks.

Arguments:

::

	1. nblocks     (numeric)

Result:

::

	n :    (numeric) estimated priority

	-1.0 is returned if not enough transactions and blocks have been observed to make an estimate.

Example:

::

	> komodo-cli estimatepriority 6

invalidateblock "hash"
----------------------

Permanently marks a block as invalid, as if it violated a consensus rule.

Arguments:

::

	1. hash   (string, required) the hash of the block to mark as invalid

Result:

Examples:

::

	> komodo-cli invalidateblock "blockhash"
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "invalidateblock", "params": ["blockhash"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

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

Removes invalidity status of a block and its descendants, reconsider them for activation.
This can be used to undo the effects of invalidateblock.

Arguments:

::

	1. hash   (string, required) the hash of the block to reconsider

Result:

Examples:

::

	> komodo-cli reconsiderblock "blockhash"
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "reconsiderblock", "params": ["blockhash"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

validateaddress "komodoaddress"
-------------------------------

Return information about the given Zcash address.

Arguments:

::

	1. "zcashaddress"     (string, required) The Zcash address to validate

Result:

::

	{
	  "isvalid" : true|false,         (boolean) If the address is valid or not. If not, this is the only property returned.
	  "address" : "zcashaddress",   (string) The Zcash address validated
	  "scriptPubKey"       (string) The hex encoded scriptPubKey generated by the address
	  "ismine" : true|false,          (boolean) If the address is yours or not
	  "isscript" : true|false,        (boolean) If the key is a script
	  "pubkey" : "publickeyhex",    (string) The hex value of the raw public key
	  "iscompressed" : true|false,    (boolean) If the address is compressed
	  "account" : "account"         (string) DEPRECATED. The account associated with the address, "" is the default account
	}

Examples:

::

	> komodo-cli validateaddress "1PSSGeFHDnKNxiEyFrD1wcEaHr9hrQDDWc"
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "validateaddress", "params": ["1PSSGeFHDnKNxiEyFrD1wcEaHr9hrQDDWc"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

verifymessage "komodoaddress" "signature" "message"
---------------------------------------------------

Verify a signed message

Arguments:

::

	1. "zcashaddress"    (string, required) The Zcash address to use for the signature.
	2. "signature"       (string, required) The signature provided by the signer in base 64 encoding (see signmessage).
	3. "message"         (string, required) The message that was signed.

Result:

::

	true|false   (boolean) If the signature is verified or not.

Examples:

Unlock the wallet for 30 seconds

::

	> komodo-cli walletpassphrase "mypassphrase" 30

Create the signature

::

	> komodo-cli signmessage "t14oHp2v54vfmdgQ3v3SNuQga8JKHTNi2a1" "my message"

Verify the signature

::

	> komodo-cli verifymessage "t14oHp2v54vfmdgQ3v3SNuQga8JKHTNi2a1" "signature" "my message"

As json rpc

::

	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "verifymessage", "params": ["t14oHp2v54vfmdgQ3v3SNuQga8JKHTNi2a1", "signature", "my message"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/

z_validateaddress "zaddr"
-------------------------

Return information about the given z address.

Arguments:

::

	1. "zaddr"     (string, required) The z address to validate

Result:

::

	{
	  "isvalid" : true|false,      (boolean) If the address is valid or not. If not, this is the only property returned.
	  "address" : "zaddr",         (string) The z address validated
	  "ismine" : true|false,       (boolean) If the address is yours or not
	  "payingkey"         (string) The hex value of the paying key, a_pk
	  "transmissionkey"   (string) The hex value of the transmission key, pk_enc
	}

Examples:

::

	> komodo-cli z_validateaddress "zcWsmqT4X2V4jgxbgiCzyrAfRT1vi1F4sn7M5Pkh66izzw8Uk7LBGAH3DtcSMJeUb2pi3W4SQF8LMKkU2cUuVP68yAGcomL"
	> curl --user user138763741:pass5ff9f6434ed6405b884fc24ee41e590a64fcf163ee9f9c44e973124935aed7a9fc     --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "z_validateaddress", "params": ["zcWsmqT4X2V4jgxbgiCzyrAfRT1vi1F4sn7M5Pkh66izzw8Uk7LBGAH3DtcSMJeUb2pi3W4SQF8LMKkU2cUuVP68yAGcomL"] }' -H 'content-type: text/plain;' http://127.0.0.1:9801/
