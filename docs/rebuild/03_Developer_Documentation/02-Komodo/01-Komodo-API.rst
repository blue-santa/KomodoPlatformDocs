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
``addressindex`` is a coin daemon parameter that instructs a KMD-based coin daemon to maintain an index of all addresses and balances. It is initiated at run time and it is used to query address balances across the entire chain.

The user should manually delete the blockchain data before initiating this parameter ===link to manual deletion instructions above===.

The ``-reindex`` parameter is not a viable alternative method for resyncing the blockchain in this circumstance.

Usage:

To initiate the ``addressindex`` command at runtime, include ``-addressindex=1`` as a parameter.

::

  ``./komodod -addressindex=1``

To set the ``addressindex`` feature as a default parameter, include the parameter in the coin's ``.conf`` configuration file.

::

  ``addressindex=1``

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
	  "balance_string"  		       // (number)   the current confirmed balance of satoshis
	  "received_string" 		       // (number)   the total confirmed number of satoshis received (including change)
	}

Examples:
===italics===(the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

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

  {"result":{"balance":40000,"received":1011916229},"error":null,"id":"curltest"}

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
===italics=== (the myrpcuser, myrpcpassword, and myrpcport data can be found in the coin's local .conf file)

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

  {"result":[{"address":"RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb","txid":"17474b73ec5a985c78a46435a021a1ad3ebd5609724ffd23d9c787c30f661342","index":1,"satoshis":50000000,"timestamp":1536364105}],"error":null,"id":"curltest"}

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

  curl --user myrpcuser:myrpcpassword --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getaddressutxos", "params": [{"addresses": ["RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb"]}] }' -H 'content-type: text/plain;' http://127.0.0.1:myrpcport/

  response:

  {"result":[{"address":"RTTg3izdeVnqkTTxjzsPFrdUQexgqCy1qb","txid":"2a3c3664851370ff762b47d735cc661e3dbce4cf36b6c1b74799f3b1c847bd52","outputIndex":0,"script":"2102e0d9ea73a391400ed2cb090e029d3f03eda0efaf371da11f436c076d817025e4ac","satoshis":10000,"height":3}],"error":null,"id":"curltest"}

  Blockchain
  ==========

  MoMoMdata symbol kmdheight notarized_height
  -------------------------------------------

  ``COMING SOON``

  allMoMs kmdstarti kmdendi
  -------------------------

  ``COMING SOON``

  calc_MoM height MoMdepth
  ------------------------

  ``COMING SOON``

  getbestblockhash
  ----------------

  Returns the hash of the best (tip) block in the longest block chain.

  Result:

  ::

  	"hex"      (string) the block hash hex encoded

  Examples:

  ::

  	> komodo-cli getbestblockhash
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getbestblockhash", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  getblock "hash|height" ( verbose )
  ----------------------------------

  * If verbose is ``false``, returns a string that is serialized, hex-encoded data for block 'hash|height'.
  * If verbose is ``true``, returns an Object with information about block <hash|height>.

  Arguments:

  ::

  	1. "hash|height"     (string, required) The block hash or height
  	2. verbose           (boolean, optional, default=true) true for a json object, false for the hex encoded data

  Result (for verbose = ``true``):

  ::

          {
              "hash": "hash",       (string) the block hash (same as provided hash)
    "confirmations": n,   (numeric) The number of confirmations, or -1 if the block is not on the main chain
    "size": n,            (numeric) The block size
    "height": n,          (numeric) The block height or index (same as provided height)
    "version": n,         (numeric) The block version
    "merkleroot": "xxxx", (string) The merkle root
    "tx": [               (array of string) The transaction ids
       "transactionid"     (string) The transaction id
       ,...
              ],
              "time": ttt,          (numeric) The block time in seconds since epoch (Jan 1 1970 GMT)
    "nonce": n,           (numeric) The nonce
    "bits": "1d00ffff",   (string) The bits
    "difficulty": x.xxx,  (numeric) The difficulty
    "previousblockhash": "hash",  (string) The hash of the previous block
    "nextblockhash": "hash"       (string) The hash of the next block
          }

  Result (for verbose=``false``):

  ::

  	"data"             (string) A string that is serialized, hex-encoded data for block 'hash'.

  Examples:
  ::

  	> komodo-cli getblock "00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09"
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": ["00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09"] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/
  	> komodo-cli getblock 12800
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblock", "params": [12800] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/


  getblockchaininfo
  -----------------

  Returns an object containing various state info regarding block chain processing.

   *Note that when the chain tip is at the last block before a network upgrade activation,* ``consensus.chaintip != consensus.nextblock``.

  Result:

  ::

      {
          "chain": "xxxx",        (string) current network name as defined in BIP70 (main, test, regtest)
    "blocks": xxxxxx,         (numeric) the current number of blocks processed in the server
    "headers": xxxxxx,        (numeric) the current number of headers we have validated
    "bestblockhash": "...", (string) the hash of the currently best block
    "difficulty": xxxxxx,     (numeric) the current difficulty
    "verificationprogress": xxxx, (numeric) estimate of verification progress [0..1
          ]
    "chainwork": "xxxx"     (string) total amount of work in active chain, in hexadecimal
    "commitments": xxxxxx,    (numeric) the current number of note commitments in the commitment tree
    "softforks": [            (array) status of softforks in progress
       {
                  "id": "xxxx",        (string) name of softfork
          "version": xx,         (numeric) block version
          "enforce": {           (object) progress toward enforcing the softfork rules for new-version blocks
             "status": xx,       (boolean) true if threshold reached
             "found": xx,        (numeric) number of blocks with the new version found
             "required": xx,     (numeric) number of blocks required to trigger
             "window": xx,       (numeric) maximum size of examined window of recent blocks
                  },
                  "reject": { ...
                  }      (object) progress toward rejecting pre-softfork blocks (same fields as "enforce")
              }, ...
          ],
          "upgrades": {                (object) status of network upgrades
       "xxxx": {                (string) branch ID of the upgrade
          "name": "xxxx",        (string) name of upgrade
          "activationheight": xxxxxx,  (numeric) block height of activation
          "status": "xxxx",      (string) status of upgrade
          "info": "xxxx",        (string) additional information about upgrade
              }, ...
          },
          "consensus": {               (object) branch IDs of the current and upcoming consensus rules
       "chaintip": "xxxxxxxx",   (string) branch ID used to validate the current chain tip
       "nextblock": "xxxxxxxx"   (string) branch ID that the next block will be validated under
          }
      }

  Examples:

  ::

  	> komodo-cli getblockchaininfo
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockchaininfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/


  getblockcount
  -------------

  Returns the number of blocks in the best valid block chain.

  Result:

  ::

  	n    (numeric) The current block count

  Examples:

  ::

  	> komodo-cli getblockcount
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockcount", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  getblockhash index
  ------------------

  Returns hash of block in best-block-chain at index provided.

  Arguments:

  ::

  	1. index         (numeric, required) The block index

  Result:

  ::

  	"hash"         (string) The block hash

  Examples:

  ::

  	> komodo-cli getblockhash 1000
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockhash", "params": [1000] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  getblockhashes timestamp
  ------------------------

  Returns array of hashes of blocks within the timestamp range provided.

  Arguments:

  ::

  	1. high         (numeric, required) The newer block timestamp
  	2. low          (numeric, required) The older block timestamp
  	3. options      (string, required) A json object
      {
        "noOrphans":true   (boolean) will only include blocks on the main chain
        "logicalTimes":true   (boolean) will include logical timestamps with hashes
      }

  Result:

  ::

  	[
  		  "hash"         (string) The block hash
  	]
  	[
  	  {
  	    "blockhash": (string) The block hash
  	    "logicalts": (numeric) The logical timestamp
  	  }
  	]

  Examples:

  ::

  	> komodo-cli getblockhashes 1231614698 1231024505
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockhashes", "params": [1231614698, 1231024505] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/
  	> komodo-cli getblockhashes 1231614698 1231024505 '{"noOrphans":false, "logicalTimes":true}'

  getblockheader "hash" ( verbose )
  ---------------------------------

  If verbose is false, returns a string that is serialized, hex-encoded data for blockheader 'hash'.
  If verbose is true, returns an Object with information about blockheader <hash>.

  Arguments:

  ::

  	1. "hash"          (string, required) The block hash
  	2. verbose           (boolean, optional, default=true) true for a json object, false for the hex encoded data

  Result (for verbose = true):

  ::

  	{
  	  "hash" : "hash",     (string) the block hash (same as provided)
  	  "confirmations" : n,   (numeric) The number of confirmations, or -1 if the block is not on the main chain
  	  "height" : n,          (numeric) The block height or index
  	  "version" : n,         (numeric) The block version
  	  "merkleroot" : "xxxx", (string) The merkle root
  	  "time" : ttt,          (numeric) The block time in seconds since epoch (Jan 1 1970 GMT)
  	  "nonce" : n,           (numeric) The nonce
  	  "bits" : "1d00ffff", (string) The bits
  	  "difficulty" : x.xxx,  (numeric) The difficulty
  	  "previousblockhash" : "hash",  (string) The hash of the previous block
  	  "nextblockhash" : "hash"       (string) The hash of the next block
  	}

  Result (for verbose=false):

  ::

  	"data"             (string) A string that is serialized, hex-encoded data for block 'hash'.

  Examples:

  ::

  	> komodo-cli getblockheader "00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09"
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getblockheader", "params": ["00000000c937983704a73af28acdec37b049d214adbda81d7e2a3dd146f6ed09"] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  getchaintips
  ------------

  Return information about all known tips in the block tree, including the main chain as well as orphaned branches.

  Result:

  ::

  	[
  	  {
  	    "height": xxxx,         (numeric) height of the chain tip
  	    "hash": "xxxx",         (string) block hash of the tip
  	    "branchlen": 0          (numeric) zero for main chain
  	    "status": "active"      (string) "active" for the main chain
  	  },
  	  {
  	    "height": xxxx,
  	    "hash": "xxxx",
  	    "branchlen": 1          (numeric) length of branch connecting the tip to the main chain
  	    "status": "xxxx"        (string) status of the chain (active, valid-fork, valid-headers, headers-only, invalid)
  	  }
  	]

  Possible values for status:

  ::

  	1.  "invalid"               This branch contains at least one invalid block
  	2.  "headers-only"          Not all blocks for this branch are available, but the headers are valid
  	3.  "valid-headers"         All blocks are available for this branch, but they were never fully validated
  	4.  "valid-fork"            This branch is not part of the active chain, but is fully validated
  	5.  "active"                This is the tip of the active main chain, which is certainly valid

  Examples:

  ::

  	> komodo-cli getchaintips
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getchaintips", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/


  getdifficulty
  -------------

  Returns the proof-of-work difficulty as a multiple of the minimum difficulty.

  Result:

  ::

  	n.nnn       (numeric) the proof-of-work difficulty as a multiple of the minimum difficulty.

  Examples:

  ::

  	> komodo-cli getdifficulty
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getdifficulty", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  getmempoolinfo
  --------------

  Returns details on the active state of the TX memory pool.

  Result:

  ::

  	{
  	  "size": xxxxx                (numeric) Current tx count
  	  "bytes": xxxxx               (numeric) Sum of all tx sizes
  	  "usage": xxxxx               (numeric) Total memory usage for the mempool
  	}

  Examples:

  ::

  	> komodo-cli getmempoolinfo
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getmempoolinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  getrawmempool ( verbose )
  -------------------------

  Returns all transaction ids in memory pool as a json array of string transaction ids.

  Arguments:

  ::

  	1. verbose           (boolean, optional, default=false) true for a json object, false for array of transaction ids

  Result: (for verbose = false):

  ::

  	[                     (json array of string)
  	  "transactionid"     (string) The transaction id
  	  ,...
  	]

  Result: (for verbose = true):

  ::

  	{                           (json object)
  	  "transactionid" : {       (json object)
  	    "size" : n,             (numeric) transaction size in bytes
  	    "fee" : n,              (numeric) transaction fee in ZEC
      	"time" : n,             (numeric) local time transaction entered pool in seconds since 1 Jan 1970 GMT
      	"height" : n,           (numeric) block height when transaction entered pool
      	"startingpriority" : n, (numeric) priority when transaction entered pool
      	"currentpriority" : n,  (numeric) transaction priority now
      	"depends" : [           (array) unconfirmed transactions used as inputs for this transaction
          "transactionid",    (string) parent transaction id
  	       ...]
  	  }, ...
  	}

  Examples:

  ::

  	> komodo-cli getrawmempool true
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getrawmempool", "params": [true] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  getspentinfo
  ------------

  Returns the txid and index where an output is spent.

  Arguments:

  ::

  	{
  	  "txid" (string) The hex string of the txid
  	  "index" (number) The start block height
  	}

  Result:

  ::

  	{
  	  "txid"  (string) The transaction id
  	  "index"  (number) The spending input index
  	  ,...
  	}

  Examples:

  ::

  	> komodo-cli getspentinfo '{"txid": "0437cd7f8525ceed2324359c2d0ba26006d92d856a9c20fa0241106ee5a597c9", "index": 0}'
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "getspentinfo", "params": [{"txid": "0437cd7f8525ceed2324359c2d0ba26006d92d856a9c20fa0241106ee5a597c9", "index": 0}] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  gettxout "txid" n ( includemempool )
  ------------------------------------

  Returns details about an unspent transaction output.

  Arguments:

  ::

  	1. "txid"       (string, required) The transaction id
  	2. n              (numeric, required) vout value
  	3. includemempool  (boolean, optional) Whether to include the mempool

  Result:

  ::

  	{
  	  "bestblock" : "hash",    (string) the block hash
  	  "confirmations" : n,       (numeric) The number of confirmations
  	  "value" : x.xxx,           (numeric) The transaction value in ZEC
    	"scriptPubKey" : {         (json object)
      	 "asm" : "code",       (string)
      	 "hex" : "hex",        (string)
      	 "reqSigs" : n,          (numeric) Number of required signatures
      	 "type" : "pubkeyhash", (string) The type, eg pubkeyhash
      	 "addresses" : [          (array of string) array of Zcash addresses
      	    "zcashaddress"        (string) Zcash address
      	    ,...
      	 ]
    	},
    	"version" : n,              (numeric) The version
    	"coinbase" : true|false     (boolean) Coinbase or not
  	}

  Examples:

  Get unspent transactions

  ::

  	> komodo-cli listunspent

  View the details

  ::

  	> komodo-cli gettxout "txid" 1

  As a json rpc call

  ::

  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "gettxout", "params": ["txid", 1] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  gettxoutproof ["txid",...] ( blockhash )
  ----------------------------------------

  Returns a hex-encoded proof that "txid" was included in a block.

  **NOTE:** By default this function only works sometimes. This is when there is an
  unspent output in the utxo for this transaction. To make it always work,
  you need to maintain a transaction index, using the -txindex command line option or
  specify the block in which the transaction is included in manually (by blockhash).

  Return the raw transaction data.

  Arguments:

  ::

  	1. "txids"       (string) A json array of txids to filter
  	    [
  	      "txid"     (string) A transaction hash
  	      ,...
  	    ]
  	2. "block hash"  (string, optional) If specified, looks for txid in the block with this hash

  Result:

  ::

  	"data"           (string) A string that is a serialized, hex-encoded data for the proof.

  gettxoutsetinfo
  ---------------

  Returns statistics about the unspent transaction output set.
  Note this call may take some time.

  Result:

  ::

  	{
  	  "height":n,     (numeric) The current block height (index)
  	  "bestblock": "hex",   (string) the best block hash hex
  	  "transactions": n,      (numeric) The number of transactions
  	  "txouts": n,            (numeric) The number of output transactions
   	 "bytes_serialized": n,  (numeric) The serialized size
  	  "hash_serialized": "hash",   (string) The serialized hash
  	  "total_amount": x.xxx          (numeric) The total amount
  	}

  Examples:

  ::

  	> komodo-cli gettxoutsetinfo
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "gettxoutsetinfo", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  height_MoM height
  -----------------

  ``COMING SOON``

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

  paxpending needs no args
  ------------------------

  ``DEPRECATED``

  paxprice "base" "rel" height
  ----------------------------

  ``DEPRECATED``

  paxprices "base" "rel" maxsamples
  ---------------------------------

  ``DEPRECATED``

  txMoMproof needs a txid
  -----------------------

  ``COMING SOON``

  verifychain ( checklevel numblocks )
  ------------------------------------

  Verifies blockchain database.

  Arguments:

  ::

  	1. checklevel   (numeric, optional, 0-4, default=3) How thorough the block verification is.
  	2. numblocks    (numeric, optional, default=288, 0=all) The number of blocks to check.

  Result:

  ::

  	true|false       (boolean) Verified or not

  Examples:

  ::

  	> komodo-cli verifychain
  	> curl --user myusername --data-binary '{"jsonrpc": "1.0", "id":"curltest", "method": "verifychain", "params": [] }' -H 'content-type: text/plain;' http://127.0.0.1:7771/

  verifytxoutproof "proof"
  ------------------------

  Verifies that a proof points to a transaction in a block, returning the transaction it commits to
  and throwing an RPC error if the block is not in our best chain

  Arguments:

  ::

  	1. "proof"    (string, required) The hex-encoded proof generated by gettxoutproof

  Result:

  ::

  	["txid"]      (array, strings) The txid(s) which the proof commits to, or empty array if the proof is invalid
