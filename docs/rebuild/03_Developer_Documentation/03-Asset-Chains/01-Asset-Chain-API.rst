**********************
The Komodo Asset Chain
**********************

About Asset Chains
==================

A "Komodo asset chain" is an independent blockchain that is based on Komodo technology and has the option of using Komodo's many services, including security and scalability.

We use the term, "asset chain," because the coins in the blockchain are assets owned by you and your blockchain's users.

The unique combination of technology in a Komodo asset chain grants businesses and developers an increased level of freedom.

While creating and developing the asset chain does not require contact with or payment to the Komodo team, utilizing many of our ancillary services does.

Most importantly, an asset chain is not secure until it has received the Komodo connection to the Bitcoin hash rate (dPoW). Please reach out to our team whenever you are ready to enlist our services.

For a full description of the nature of a Komodo asset chain, please ===link=== refer to our white paper.

*************************
Creating A New Assetchain
*************************

Requirements
============

* 2 computers (nodes) with the ability to open ports
* At least 4gb RAM each
* At least 2 CPU cores each
* 64-bit Operating System (Ubuntu 16.04 recommended)
* ``komodod`` built on each, see :ref:`Installing Komodo Manually` (No need to download the Komodo blockchain)

Notes on the Computers (Nodes) Used to Create an Asset Chain
=============================================================

If you are interested in testing a Komodo asset chain for yourself, please do not hesitate to reach out to us when you are stuck. We frequently have support agents available in our ===link https://komodoplatform.com/discord === Discord #support channel, and for off hours you can file a ticket on ===link https://support.komodoplatform.com/support/home === our support page.

If you are ready to press forward now with your first test asset chain, some basic knowledge about how to connect two nodes (computers) is recommended for the initial setup.

In the most ideal circumstance, the new Komodo developer will already have two virtual private server boxes (VPS's) available for testing. VPS's can be cheap and easy to manage. A typical VPS will automatically have a static external IP that is easily reachable, making connection between two VPS nodes simple.

If the new developer does not have two VPS's available, setting up a test asset chain on two local machines in a home or office-type setting is still achievable, but it may require a little more troubleshooting.

The challenge lies in the way the network is created, and there are myriad network setups. For example, if the developers are operating on a local router, where the two machines are connected via wi-fi, the local ip addresses of the machines are a bit harder to find; the router assigns new local ip addresses to the machines each time they connect. In this situation, the developer must log into the router's software interface and search for their currently assigned local ip addresses.

This latter scenario can suffice, if you're just looking to test an asset chain and don't want to spend money on a VPS. However, don't be surprised if you need to ask for help. We'll be here for you, when you need us.

You will know that your machines have succesfully connected when you can run this command in the shell of one of your machines:

::

	ping <insert ip address of your other machine here>

This command will generate a response every second, indicating the `ping` speed with which your machines are able to connect.

::

	ping 192.168.1.101
	PING 192.168.1.101 (192.168.1.101) 56(84) bytes of data.
	64 bytes from 192.168.1.101: icmp_seq=1 ttl=64 time=131 ms
	64 bytes from 192.168.1.101: icmp_seq=2 ttl=64 time=2.40 ms
	...

If you do not see a continuing response in the shell, your machines are not yet connected. Please reach out to our team and we will do our best to assist you.

Part I: Creating a New Komodo Asset Chain
=========================================

With your machines successfully able to `ping` each other, you are prepared to create your first asset chain.

The following instructions use the simplest possible set of parameters in creating a new asset chain: a coin with the ticker symbol ``EXAMPLECHAIN``, ``1000000`` premined coins, and a block reward of ``.0001``.

On your first node, change into ===link=== the directory where Komodo's ``komodod`` and ``komodo-cli`` is installed and execute the following commands in the terminal:

(Mac & GNU/Linux)

.. code-block:: shell

	./komodod -ac_name=EXAMPLECHAIN -ac_supply=1000000 -addnode=<IP address of the second node> &

(Windows)

.. code-block:: shell

	./komodod.exe -ac_name=EXAMPLECHAIN -ac_supply=1000000 -addnode=<IP address of the second node> &

After issuing this command in the terminal, you will find the p2p port in the terminal window.

.. code-block:: shell

	>>>>>>>>>> EXAMPLECHAIN: p2p.8096 rpc.8097 magic.c89a5b16 3365559062 1000000 coins

In this case, the p2p port is ``8096``.

This completes the first half of the asset-chain creation process.

	* Note: please refer to :ref:`Asset Chain Parameters` for a full list of parameters to customize your initial blockchain state. Please also note the requirements for ===link=== ``ac_supply``, and instructions for using link ``addnode`` under various network conditions, including firewalls and LANs.

Part II: Connecting on the Second Node
========================================

On the second node you issue the same command, but with the first node's IP address, and an additional setting that initiates mining on this machine: ``-gen -genproclimit=$(nproc)``.

.. code-block:: shell

	./komodod -ac_name=EXAMPLECHAIN -ac_supply=1000000 -addnode=<IP address of the first node> -gen -genproclimit=$(nproc)

When this second node connects it will begin to mine blocks.

The indicated number of premined coins will be deposited into to the wallet of the node that executed ``-gen -genproclimit=$(nproc)``.

You can check the contents of the wallet by executing the following command in another terminal:

.. code-block:: shell

	./komodo-cli -ac_name=EXAMPLECHAIN getwalletinfo

More info can be found in the debug.log of the chain found at:

``~/.komodo/EXAMPLECHAIN/debug.log`` (Mac & GNU/Linux)

``%appdata%\komodo\EXAMPLECHAIN\debug.log`` (Windows)

Querying the Asset Chain
========================

Using the pre-installed ``komodo-cli`` software, you can execute many RPC calls and other API commands to your new asset chain, enabling you to perform transactions, create and execute smart contracts, store data in KV storage, create cross-chain compatible contracts, etc.

Since the Komodo software began as a fork of Zcash and BTC, essentially all commands that are available on these two upstream blockchains are also available on your new asset chain. Many more commands that we have created to enhance your creative tool set and development process are available as well. Please see our ===link=== API documentation for more information.

Example commands
----------------

On a KMD-based blockchain, the entire coin supply is mined in the first block. As soon as your machines connected in the steps above, your coin supply was distributed into the ``wallet.dat`` file of the machine that mined the first block. You can view this balance by executing the following command on the mining machine:

.. code-block:: shell

	./komodo-cli -ac_name=EXAMPLECHAIN getbalance

These are the coins that you will sell to your future customers, in exchange for whatever cryptocurrency you desire. Also, since you are built on a KMD-based blockchain, you have easy access to our decentralized exchange, and our decentralized-ICO software.

To see general information about your new asset chain, execute this command:

.. code-block:: shell

	./komodo-cli -ac_name=EXAMPLECHAIN getinfo

This command returns information about all available RPC and API commands:

.. code-block:: shell

	./komodo-cli -ac_name=EXAMPLECHAIN help

Secure this Asset Chain with Delayed Proof of Work
==================================================

Your new chain can receive the same security of the Bitcoin hash rate with a simple service from our KMD notary nodes, called "delayed Proof of Work" (dPoW).

There are two aspects to the cost for dPoW services. The first comes from the cost of making records in your asset chain's database, and in the records of the KMD main chain. These records are called "notarizations," and the Komodo software automatically knows how to create and track them once you are connected to our services.

Notarizations are performed as transactions on your blockchain and on the main KMD blockchain. The transactions have messages included inside that indicate the most recent and secure state of your asset chain. Your blockchain will know how to recognize and rely on notarizations automatically. Every ten to twenty minutes, all of the information in the KMD chain (including your asset chain's history) is hashed and inserted into the BTC blockchain. Once your information is pushed into BTC, your blockchain will consider all notarized information completely settled and immutable; only the recent, un-notarized transactions are still relying on your asset chain's consensus mechanism (which can be PoW, PoS, or a hybrid of both). Thus, your asset chain will have all the power of Bitcoin securing your blockchain's history.

As the notarizations are transactions, they have a cost to perform, and this cost is covered by the asset-chain developer. Over the course of a year, the cost for performing these transactions is 300 KMD, and 800 of your asset chain's coins.

The second part of the cost of notarization is the payment to the actual Komodo team, which is given in exchange for our services. We have not yet published this rate, as we are still in the discovery phase. Please reach out to us to receive a quote.

Several teams have already signed up for our services and are developing on our platform. From our experience with them we can confidently say that our pricing is generally very (very) affordable, compared to other blockchain services. In many cases, creating a fully independent blockchain on Komodo costs but a small fraction of what it would cost to execute just one smart contract on other blockchain platforms.

In our ecosystem, there are third-party businesses that can help you to initiate and develop your blockchain. @siu (Discord: @siu#3920) runs the ChainMakers business, and @PTYX (Discord: @PTYX#6840) runs Chainzilla. Both can provide different levels of service in asset-chain creation, electrum server setup and maintenance, explorer setup, and other decentralized-technology services.

Please send any critique or feedback of this documnetation to either @siddhartha-komodo, @Alright, or @gcharang on matrix or discord.

`Discord Invite <https://discord.gg/SCdf4eh>`_

**********************
Asset Chain Parameters
**********************

For examples see :doc:`example-asset-chains`

-ac_name
========

This is the ticker symbol for the coin you wish to create. We recommended it consist only of numbers and uppercase letters.

-ac_supply
==========

This is the amount of premined coins you would like the chain to have.

The node that sets ``-gen`` during the creation process will mine these coins in the genesis block.

If ``-ac_supply`` is not set, ``-ac_reward`` must be set, and the default value of 10 coins will be used. If ``-ac_pubkey`` is set, the  premined coins will be mined to the address of the corresponding pubkey. This parameter should be set to a whole number without any decimals places. This should be to set to less than ``2000000000`` to avoid 64 bit overflows.

Note: An additional fraction of a coin will be added to this based on the chain's parameters. This is used by nodes to verify the genesis block. For example, the DEX chain's ``-ac_supply`` parameter is set to ``999999``, but in reality the genesis block was ``999999.13521376``.

-ac_reward
==========
This is the block reward for each mined block in satoshis. If this is not set, the block reward will be ``10000`` satoshis, and blocks will be on-demand after block 127 (a new block will not be mined unless there is a transaction in the mempool.)

-ac_end
=======
This is the block height in which block rewards will end. Every block after this height will have 0 block reward.

-ac_halving
===========
This is the number of blocks between each block reward halving. This parameter will have no effect if ``-ac_reward`` is not set. The lowest possible value is ``1440`` (~1 day). If this parameter is set, but ``-ac_decay`` is not, the reward will decrease by 50% each halving.

-ac_decay
=========
This is the percentage the block reward will decrease by each block reward halving. For example, if this is set to ``750000000``, the block reward will drop 25% from the previous block reward each halving. This parameter will have no effect if ``-ac_reward`` is not set.
This is the formula that ``-ac_decay`` follows:

.. code-block:: shell

	numhalvings = (height / -ac_halving);
	for (i=0; i<numhalvings; i++)
	reward = (reward * -ac_decay) / 100000000;


-ac_perc
========

The ``-ac_perc`` parameter is the percentage added to the block reward and transactions that will be sent to the ``-ac_pubkey`` address. If this parameter is set, ``-ac_pubkey`` must also be set. For example, if ``-ac_reward=100000000`` and ``-ac_perc=10000000``, for each block mined, the miner receives 1 coin along with the ``-ac_pubkey`` address receiving 0.1 coin. For every transaction sent, the pubkey address will receive 10% of the overall transaction value. This 10% is not taken from the user, rather it is created at this point. Each transaction inflates the overall supply.

Note: Vout 1 of each coinbase transaction must be the correct amount sent to the corresponding pubkey. The ``vout`` type for all coinbase vouts must be ``pubkey`` as opposed to ``pubkeyhash``. This only affects a miner trying to use a stratum. Z-nomp is currently incompatible.

-ac_pubkey
==========

If ``-ac_pubkey`` is set, but ``-ac_perc`` is not, this simply means the genesis block will be mined to the set pubkey's address. This must be set to a 33 byte hex string. You can get the pubkey of an address by using the ``validateaddress`` command in ``komodod``. The address must be imported to the wallet before using ``validateaddress``.

-ac_cc
======

This is the network cluster on which the chain can interact with other chains via cross chain smart contracts. This functionality is still in testing. If this is set to 1, the chain will have smart contracts enabled, but it will not be able to interact with other chains. If this is set to any number other than 0 or 1, the chain can interact with other chains on the same network cluster. For example, all ``-ac_cc=2`` chains can interact with each other but may not interact with ``-ac_cc=3`` chains.
If you'd like to explicitly disable smart contracts set this value to ``0``.

-ac_staked
==========

.. note::

	This feature is currently only available in the `jl777 branch <https://github.com/jl777/komodo/tree/jl777>`_.

This is the percentage of blocks the chain will aim to have as POS. For example, a ``ac_staked=90`` chain will have 90% POS blocks/10% POW blocks. This isn't exact, but the POW difficulty will automatically adjust based on the overall percentage of POW mined blocks.

Each staked block will have an additional transaction added to the coinbase in which the coins that staked the block are sent back to the same address. This is used to verify which coins staked the block, and this allows for compatibility with existing Komodo infrastructure such as Agama, BarterDEX and explorers. If ``-ac_staked`` is used in conjunction with ``-ac_perc``, the ``-ac_pubkey`` address will receive slightly more coins for each staked block compared to a mined block because of this extra transaction.

The following are the (current) rules for staking a block:

	#. Block timestamps are used as the monotonically increasing timestamp. It is important to have a synced system clock.

	#. In order to stake, you must use ``-gen -genproclimit=0`` while launching the daemon or ``komodo-cli -ac_name=<CHAINNAME> setgenerate true 0`` after launching the daemon.

	#. A utxo is not eligible without ``nLockTime`` set and until 6000 seconds has passed from this lock time. ``(100 * expected blocktimes) to be exact``

	#. There are 64 different segments(``segids``) of addresses, based on the hash of the destination address. ``((nHeight + addrhash.uints[0]) & 0x3f)`` The segid of an address can be found with the ``validateaddress`` command. Each segid will take turns being segid0 at each height. ``(height % 64) = the segid0 for that height.`` All other segid will adjust the elapsed time by ``segid`` seconds.

	#. A new block is eligible to be staked 2 seconds after median blocktime. For example, segid0 for a given height will be eligible to submit a block 2 seconds after median blocktime, whereas segid1 will be eligible to submit a block 4 seconds after median blocktime. For the next block, segid0 from the previous block will now be segid63 and will be eligible to submit a block 128 seconds after median blocktime. This means by 128 seconds after the median blocktime, all segids are eligible.

	#. Coinage calculated from the adjusted time is used to divide hash(address + pastblockhash) to create the value compared against the difficulty to determine if a block is won or not. This means a UTXO is more likely to win a block within a segid based on age of the UTXO and amount of coins.

To create a chain using this parameter, start the first node with ``-gen -genproclimit=0``. Start the second node with ``-gen -genproclimit=$(nproc)``. Send coins from the second node to the first node, and it will begin staking. The first 100 blocks will allow POW regardless of the ``ac_staked`` value. On a chain using a high percentage for POS, it's vital to have coins staking by block 100. It is also vital to stake coins in all 64 segids. For the time being, you can use the `genaddresses.py` script in `this repo <https://github.com/alrighttt/dockersegid>`_ to generate an address for each segid. This functionality will soon be integrated directly into the daemon. You can use the ``getbalance64`` command to get the balance you currently have in each segid you are staking in.


-ac_public
==========

.. note::
	This feature is currently only available in the `jl777 branch <https://github.com/jl777/komodo/tree/jl777>`_.

If ``ac_public`` is set to 1, zkSNARKs will be disabled. All z address functionalilty is disabled. Therefore, all transactions on the blockchain are public.

-ac_private
===========

.. note::
	This feature is currently only available in the `jl777 branch <https://github.com/jl777/komodo/tree/jl777>`_.

If ``ac_private`` is set to 1, all transactions other than coinbase transactions(block rewards) must use zkSNARKs. All transparent address functionality other than sending mined coins from transparent addresses is disabled.


Please send any critiques or feedback to Alright or gcharang on matrix or discord.

`Discord Invite <https://discord.gg/SCdf4eh>`_


********************
Example Asset Chains
********************

The purpose of this document is to give a better understanding of asset chain parameters via examples. These chains are grouped simply by the number of parameters used in customizing each. As new parameters are added, the new combinations will be tested and added here.

Please see :doc:`create-Komodo-Assetchain` and :doc:`assetchain-params` if you haven't already.

All chains must have at least ``ac_name`` and ``ac_supply`` set. The ``ac_pubkey`` parameter can be used with any of these chains. If ``ac_perc`` is not set, the only effect ``ac_pubkey`` has  is to have the genesis block be mined to the pubkey that has been specified. The parameters ``ac_name`` , ``ac_supply`` , ``ac_pubkey`` are not counted when grouping based on the ``Number of parameters``.

The values of parameters other than ``ac_name`` in these examples are completely arbitrary. The names of these example-asset-chains are assigned based on how a chain is customized and its grouping.

Number of parameters: 1
***********************

ac_reward
=========

``./komodod -ac_name=1REW -ac_supply=999999 -ac_reward=100000000``

999999 coin premine

1 coin block reward that does not end.

ac_halving
==========

``./komodod -ac_name=1HALV -ac_supply=999999 -ac_halving=2000``

999999 coin premine

Default block reward of 0.0001 coin; On demand blocks after block 128

``ac_halving`` has no effect unless ``ac_reward`` is set

ac_decay
========
``./komodod -ac_name=1DECAY -ac_supply=999999 -ac_decay=50000000``

999999 coin premine

Default block reward of 0.0001 coin; On demand blocks after block 128

``ac_decay`` has no effect unless ``ac_reward`` is set

ac_end
======

``./komodod -ac_name=1END -ac_supply=999999 -ac_end=25000``

999999 coin premine

Default block reward of 0.0001 coin; On demand blocks after block 128

Block reward ends at block 25000.


ac_perc ac_pubkey
=================

``./komodod -ac_name=1PERC -ac_supply=999999 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.


ac_staked
=========

``./komodod -ac_name=1STAKE -ac_supply=999999 -ac_reward=100000000 -ac_staked=90``

999999 coin premine

1 coin block reward

Chain adjusts difficulty so 90% of blocks are proof of stake, 10% proof of work

It’s important to start staking immediately for high percentages of POS. If too many POW blocks are mined consecutively at the start of the chain, the POW difficulty may increase enough to stop the chain entirely, meaning you can’t send a transaction to staking nodes.

Number of parameters: 2
***********************

ac_reward ac_halving
====================

``./komodod -ac_name=2REWHALV -ac_supply=999999 -ac_reward=500000000 -ac_halving=2000``

999999 coin premine

5 coin block reward.

Block reward decreases by 50% every 2000 blocks.

ac_reward ac_decay
==================

``./komodod -ac_name=2REWDECAY -ac_supply=999999 -ac_reward=500000000 -ac_decay=75000000``

999999 coin premine

5 coin block reward

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

ac_reward ac_end
================

``./komodod -ac_name=2REWEND -ac_supply=999999 -ac_reward=500000000 -ac_end=200``

999999 coin premine

5 coin block reward

Block reward ends at block 200.

ac_reward ac_perc ac_pubkey
===========================

``./komodod -ac_name=2REWPERC -ac_supply=999999 -ac_reward=500000000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

999999 coin premine

5 coin block reward

Pubkey address receives 0.25 coin for every mined block.(an additional 5% of block reward)

Pubkey address receives an additional 5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins
are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_staked
===================

``./komodod -ac_name=2REWSTAKE -ac_supply=100000 -ac_reward=1000000000 -ac_staked=2``

100000 coin premine

10 coin block reward

Chain adjusts difficulty so 2% of blocks are proof of stake, 98% proof of work.

ac_halving ac_decay
===================

``./komodod -ac_name=2HALVDECAY -ac_supply=999999 -ac_halving=2000 -ac_decay=50000000``

999999 coin premine

Default block reward of 0.0001 coin; On demand blocks after block 128

``ac_halving`` and ``ac_decay`` have no effect if ``ac_reward`` is not set.

ac_halving ac_end
=================

``./komodod -ac_name=2HALVEND -ac_supply=999999 -ac_halving=2000 -ac_end=10000``

999999 coin premine

Default block reward of 0.0001 coin; Blocks are on-demand after block 128

Block reward ends at block 10000

``ac_halving`` has no effect without ``ac_reward`` being set.

ac_halving ac_perc ac_pubkey
============================

``./komodod -ac_name=2HALVPERC -ac_supply=999999 -ac_halving=2000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_halving`` has no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

ac_halving ac_staked
====================

``./komodod -ac_name=2HALVSTAKE -ac_supply=999999 -ac_halving=2000 -ac_staked=10``

Default block reward of 0.0001 coin

Chain adjusts difficulty so 10% of blocks are proof of stake, 90% proof of work.

``ac_halving`` has no effect without ``ac_reward`` being set.

ac_decay ac_end
===============

``./komodod -ac_name=2DECEND -ac_supply=999999 -ac_decay=5000000 -ac_end=10000``

999999 coin premine

Default block reward of 0.0001 coin; Blocks are on-demand after block 128

Block reward ends at block 10000.

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

ac_decay ac_perc ac_pubkey
==========================

``./komodod -ac_name=2DECPERC -ac_supply=999999 -ac_decay=75000000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_decay`` has no effect without setting ``ac_reward`` and ``ac_halving`` both set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

ac_decay ac_staked
==================

``./komodod -ac_name=2DECAYSTAKE -ac_supply=999999 -ac_decay=5000000 -ac_staked=50``

999999 coin premine

Default block reward of 0.0001 coin

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

Chain adjusts difficulty so 50% of blocks are proof of stake, 50% proof of work.

ac_end ac_perc ac_pubkey
========================

``./komodod -ac_name=2ENDPERC -ac_supply=999999 -ac_end=10000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

ac_end ac_staked
================

``./komodod -ac_name=2ENDSTAKE -ac_supply=999999 -ac_end=10000 -ac_staked=5``

999999 coin premine

Default block reward of 0.0001 coin

Block reward ends at block 10000.

Chain adjusts difficulty so 5% of blocks are proof of stake, 95% proof of work.

ac_perc ac_pubkey ac_staked
===========================

``./komodod -ac_name=2PERCSTAKE -ac_supply=999999 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=50``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.


Number of parameters: 3
***********************

ac_reward ac_halving ac_decay
=============================

``./komodod -ac_name=3REWHALVDEC -ac_supply=999999 -ac_reward=1000000000 -ac_halving=2000 -ac_decay=75000000``

999999 coin premine

10 coin block reward

Block reward decreases by 25% every 2000 blocks.

ac_reward ac_halving ac_end
===========================

``./komodod -ac_name=3REWHALVEND -ac_supply=999999 -ac_reward=500000000 -ac_halving=2000 -ac_end=10000``

999999 coin premine

5 coin block reward

Block reward decreases by 50% every 2000 blocks

Block reward ends at block 10000

ac_reward ac_halving ac_perc ac_pubkey
======================================

``./komodod -ac_name=3REWHALVPERC -ac_supply=999999 -ac_reward=500000000 -ac_halving=1440 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_perc=50000000``

999999 coin premine

5 coin block reward

Block reward decreases by 50% every 1440 blocks.

The pubkey address receives an additional 50% of the block reward for each mined block. For example, before the first halving the pubkey address will receive 2.5 coins(50% of 5 coin block reward) for every mined block. After the first halving, the pubkey address will receive 1.25 coins.

The pubkey address receives an additional 50% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 50 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.


ac_reward ac_halving ac_staked
==============================

``./komodod -ac_name=3REWHALVSTAKE -ac_supply=999999 -ac_reward=100000000 -ac_havling=2000 -ac_staked=10``

999999 coin premine

1 coin block reward

Block reward decreases by 50% every 2000 blocks

Chain adjusts difficulty so 10% of blocks are proof of stake, 90% proof of work.

ac_reward ac_decay ac_end
=========================

``./komodod -ac_name=3REWDECEND -ac_supply=999999 -ac_reward=500000000 -ac_decay=75000000 -ac_end=5000``

999999 coin premine

5 coin block reward

Block reward ends at block 5000.

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

ac_reward ac_decay ac_perc ac_pubkey
====================================

``./komodod -ac_name=3REWDECPERC -ac_supply=999999 -ac_reward=500000000  -ac_decay=75000000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

999999 coin premine

5 coin block reward

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

Pubkey address receives 0.5 coin for every mined block(an additional 10% of block reward)

Pubkey address receives an additional 10% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 10 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_decay ac_staked
============================

``./komodod -ac_name=3REWDECSTAKE -ac_supply=999999 -ac_reward=1000000000 -ac_decay=25000000 -ac_staked=50``

999999 coin premine

10 coin block reward

``ac_decay`` has no effect if ``ac_halving`` is not set

Chain adjusts difficulty so 50% of blocks are proof of stake, 50% proof of work.


ac_reward ac_end ac_perc ac_pubkey
==================================

``./komodod -ac_name=3ENDPERCREW -ac_supply=999999 -ac_reward=5000000000 -ac_end=10000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

999999 coin premine

50 coin block reward

Block reward ends at block 10000.

Pubkey address receives 2.5 coins(an additional 5% of block reward) for every mined block before block 10000.

Pubkey address receives an additional 5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be pubkey as opposed to pubkeyhash.

ac_reward ac_end ac_staked
==========================

``./komodod -ac_name=3REWENDSTAKE -ac_supply=500000 -ac_reward=10000000000 -ac_end=15000 -ac_staked=60``

500000 coin premine

100 coin block reward

Block reward ends at block 15000.

Chain adjusts difficulty so 60% of blocks are proof of stake, 40% proof of work.

ac_reward ac_perc ac_pubkey ac_staked
=====================================

``./komodod -ac_name=3REWPERCSTAKE -ac_supply=1000000 -ac_reward=1000000000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=50``

1000000 coin premine

10 coin block reward

Chain adjusts difficulty so 50% of blocks are proof of stake, 50% proof of work.

Pubkey address receives 1 coin for every mined block.(an additional 10% of block reward)

Pubkey address receives an additional 10% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins are created and sent to the pubkey address. This includes the additional verification transaction in POS blocks, meaning the pubkey address receives more coins for every POS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_halving ac_decay ac_end
==========================

``./komodod -ac_name=3HALVDECEND -ac_supply=999999 -ac_end=100000 -ac_halving=5000 -ac_end=100000``

999999 coin premine

Default block reward of .0001; Blocks are on-demand after block 128.

Block reward ends at block 100000.

``ac_halving`` has no effect if ``ac_reward`` is not set.

ac_halving ac_decay ac_perc ac_pubkey
=====================================

``./komodod -ac_name=3HALVDECPERC -ac_supply=999999 -ac_halving=2000 -ac_decay=25000000 -ac_perc=90000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_halving`` has no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.


ac_halving ac_decay ac_staked
=============================

``./komodod -ac_name=3HALVDECSTAKE -ac_supply=50000 -ac_halving=2000 -ac_decay=45000000 -ac_staked=40``

50000 coin premine

``ac_halving`` and ``ac_decay`` have no effect if ``ac_reward`` is not set

Chain adjusts difficulty so 40% of blocks are proof of stake, 60% proof of work.


ac_halving ac_end ac_perc ac_pubkey
===================================
``./komodod -ac_name=3HALVENDPERC -ac_supply=999 -ac_halving=1441 -ac_end=20000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_halving`` has no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.


ac_halving ac_end ac_staked
===========================
``./komodod -ac_name=3HALVENDSTAKE -ac_supply=50000 -ac_halving=2000 -ac_end=10000 -ac_staked=50``

50000 coin premine

Default block reward of 0.0001 coin

``ac_halving` has no effect if ``ac_reward`` is not set.

Block reward ends at block 10000.

Chain adjusts difficulty so 50% of blocks are proof of stake, 50% proof of work.


ac_halving ac_perc ac_pubkey ac_staked
======================================
``./komodod -ac_name=3HALVPERCSTAKE -ac_supply=99999 -ac_halving=2000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=10``

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

ac_decay ac_end ac_perc ac_pubkey
=================================
``./komodod -ac_name=3DECENDPERC -ac_supply=10000 -ac_decay=75000000 -ac_end=100000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.


ac_decay ac_end ac_staked
=========================
``./komodod -ac_name=3DECENDSTAKE -ac_supply=800000 -ac_decay=20000000 -ac_end=20000 -ac_staked=60``

800000 coin premine

Default block reward of 0.0001 coin

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

Block reward ends at block 20000.

Chain adjusts difficulty so 60% of blocks are proof of stake, 40% proof of work.

ac_decay ac_perc ac_pubkey ac_staked
====================================
``./komodod -ac_name=3DECPERCSTAKE -ac_supply=77777 -ac_decay=40000000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.


ac_end ac_perc ac_pubkey ac_staked
==================================
``./komodod -ac_name=3ENDPERCSTAKE -ac_supply=999999 -ac_end=70000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=10``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

Number of parameters: 4
***********************

ac_reward ac_halving ac_decay ac_end
====================================

``./komodod -ac_name=4REWHALVDECEND -ac_supply=1000000 -ac_reward=10000000000 -ac_halving=10000 -ac_decay=25000000 -ac_end=100000``

1000000 coin premine

100 coin block reward

Block reward decreases by 75% every 10000 blocks.

Block reward ends at block 100000.

ac_reward ac_halving ac_decay ac_perc ac_pubkey
===============================================

``./komodod -ac_name=4REWHALVDECPERC -ac_supply=999999 -ac_reward=1000000000 -ac_halving=5000 -ac_decay=60000000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

999999 coin premine

10 coin block reward

Block reward decreases 40% every 5000 blocks

The pubkey address receives an additional 5% of the block reward for each mined block. For example, before the first halving, the pubkey address will receive 0.5 coin(5% of 10 coin block reward) for every mined block. After the first halving, the pubkey address will receive 0.3 coin for every mined block.(5% of 6 coin block reward)

Pubkey address receives an additional 5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins
are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_halving ac_decay ac_staked
=======================================

``./komodod -ac_name=4REWHALVDECSTAKE -ac_supply=99999 -ac_reward=1000000000000 -ac_halving=2000 -ac_decay=60000000 -ac_staked=50``

99999 coin premine

10000 coin block reward

Block reward decreases by 40% every 2000 blocks.

Chain adjusts difficulty so 50% of blocks are proof of stake, 50% proof of work.

ac_reward ac_halving ac_end ac_perc ac_pubkey
=============================================

``./komodod -ac_name=4REWPERCENDHALV -ac_supply=999999 -ac_reward=1000000000 -ac_halving=2000 -ac_end=60005 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_perc=10000000``

999999 coin premine

10 coin block reward

Block reward decreases by 50% every 2000 blocks.

Block reward ends at block 60005.

The pubkey address receives an additional 10% of the block reward for each mined block. For example, before the first halving, the pubkey address will receive 1 coin(10% of 10 coin block reward) for every mined block. After the first halving, the pubkey address will receive 0.5 coin for every mined block.

Pubkey address receives an additional 10% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 10 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_halving ac_end ac_staked
=====================================

``./komodod -ac_name=4REWHALVENDSTAKE -ac_supply=99999 -ac_reward=10000000 -ac_halving=5000 -ac_end=50000 -ac_staked=40``

99999 coin premine

0.1 coin block reward

Block reward decreases by 50% every 5000 blocks.

Block reward ends at block 50000.

Chain adjusts difficulty so 40% of blocks are proof of stake, 60% proof of work.

ac_reward ac_halving ac_perc ac_pubkey ac_staked
================================================

``./komodod -ac_name=4PERCREWHALVSTAKE -ac_supply=999999 -ac_reward=1000000000 -ac_halving=2000 -ac_perc=5000000 -ac_staked=50 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

999999 coin premine

10 coin block reward

Block reward decreases by 50% every 2000 blocks.

Chain adjusts difficulty so 50% of blocks are proof of stake, 50% proof of work.

The pubkey address receives an additional 5% of the block reward for each mined block. For example, before the first halving, the pubkey address will receive 0.5 coin(5% of 10 coin block reward) for every mined block. After the first halving, the pubkey address will receive 0.25 coin for every mined block.

Pubkey address receives an additional 5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_decay ac_end ac_perc ac_pubkey
===========================================
``./komodod -ac_name=4REWDECENDPERC -ac_supply=70000 -ac_reward=700000000 -ac_decay=80000000 -ac_end=10000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

70000 coin premine

7 coin block reward

Block reward ends at block 10000.

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

Pubkey address receives .07 coin for every mined block.(an additional 1% of block reward)

Pubkey address receives an additional 1% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 1 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_decay ac_end ac_staked
===================================
``./komodod -ac_name=4REWDECENDSTAKE -ac_supply=999999 -ac_reward=500000000 -ac_decay=75000000 -ac_end=12000 -ac_staked=40``

999999 coin premine

5 coin block reward

Block rewards ends at block 12000.

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

Chain adjusts difficulty so 40% of blocks are proof of stake, 60% proof of work.

ac_reward ac_decay ac_perc ac_pubkey ac_staked
==============================================
``./komodod -ac_name=4REWDECPERCSTAKE -ac_supply=9000 -ac_reward=1000000000 -ac_decay=80000000 -ac_perc=2000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=80``

9000 coin premine

10 coin block reward.

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

Pubkey address receives 0.2 coin for every mined block.(an additional 2% of block reward)

Pubkey address receives an additional 2% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 2 coins are created and sent to the pubkey address. This includes the additional verification transaction in POS blocks, meaning the pubkey address receives more coins for every POS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.


ac_reward ac_end ac_perc ac_pubkey ac_staked
============================================

``./komodod -ac_name=4REWENDPERCSTAKE -ac_supply=999999 -ac_reward=5000000000 -ac_end=10000 -ac_staked=33 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

999999 coin premine

50 coin block reward

Block rewards ends at block 10000.

Chain adjusts difficulty so 33% of blocks are proof of stake, 67% proof of work.

Pubkey address receives 0.5 coin for every mined block(an additional 1% of block reward)

Pubkey address receives an additional 1% for every transaction made on the chain. For example, if a transaction sends 100 coins, 1 additional coin is created and sent to the pubkey address. This includes the additional verification transaction in POS blocks, meaning the pubkey address receives more coins for every POS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_halving ac_decay ac_end ac_perc ac_pubkey
============================================
``./komodod -ac_name=4HALVDECENDPERC -ac_supply=11 -ac_halving=5000000 -ac_decay=1000000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_halving`` has no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

ac_halving ac_decay ac_end ac_staked
====================================
``./komodod -ac_name=4HALVDECENDSTAKE -ac_supply=999999 -ac_halving=5000 -ac_decay=60000000 -ac_end=25000 -ac_staked=10``

999999 coin premine

Default block reward of .0001 coin.

Block reward ends at block 25000

``ac_halving`` and ``ac_decay`` have no effect if ``ac_reward`` is not set

Chain adjusts difficulty so 10% of blocks are proof of stake, 90% proof of work.

ac_halving ac_decay ac_perc ac_pubkey ac_staked
===============================================
``./komodod -ac_name=4HALVDECPERCSTAKE -ac_supply=40000 -ac_halving=5000 -ac_decay=75000000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=60``

``ac_halving`` and ``ac_decay`` have no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

ac_halving ac_end ac_perc ac_pubkey ac_staked
=============================================
``./komodod -ac_name=4HALVENDPERCSTAKE -ac_supply=99999 -ac_halving=6000 -ac_end=60000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=30``

``ac_halving`` has no effect if ``ac_reward`` is not set

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

ac_decay ac_end ac_perc ac_pubkey ac_staked
===========================================
``./komodod -ac_name=4DECENDPERCSTAKE -ac_supply=999999 -ac_decay=75000000 -ac_end=100000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=40``

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

Number of parameters: 5
***********************

ac_reward ac_halving ac_decay ac_end ac_perc ac_pubkey
======================================================

``./komodod -ac_name=5REWHALVDECENDPERC -ac_supply=999999 -ac_reward=10000000000 -ac_halving=10000 -ac_decay=75000000 -ac_end=100000 -ac_perc=2000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

999999 coin premine

100 coin block reward

Block reward reduces by 25% every 10000 blocks.

Block reward ends at block 100000.

The pubkey address receives an additional 2% of the block reward for each mined block. For example, before the first halving, the pubkey address will receive 2 coins(2% of 100 coin block reward) for every mined block. After the first halving, the pubkey address will receive 1.5 coins for every mined block.(2% of 75 coin block reward)

Pubkey address receives an additional 2% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 2 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_halving ac_decay ac_end ac_staked
==============================================

``./komodod -ac_name=5REWHALVDECENDSTAKE -ac_supply=50000 -ac_reward=500000000 -ac_halving=5000 -ac_decay=70000000 -ac_end=100000 -ac_staked=80``

50000 coin premine

5 coin block reward

Block reward decreases by 30% every 5000 blocks.

Block reward ends at block 100000.

Chain adjusts difficulty so 80% of blocks are proof of stake, 20% proof of work.


ac_reward ac_halving ac_decay ac_perc ac_pubkey ac_staked
=========================================================

``./komodod -ac_name=5REWHALVDECPERCSTAKE -ac_supply=1 -ac_reward=50000000000 -ac_halving=2000 -ac_decay=25000000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=50``

1 coin premine

500 coin block reward

Block reward decreases by 75% every 2000 blocks.

Chain adjusts difficulty so 50% of blocks are proof of stake, 50% proof of work.

The pubkey address receives an additional 1% of the block reward for each mined block. For example, before the first halving, the pubkey address will receive 5 coins(1% of 500 coin block reward) for every mined block. After the first halving, the pubkey address will receive 1.25 coins for every mined block.(1% of 125 block reward)

Pubkey address receives an additional 1% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 1 coins are created and sent to the pubkey address. This includes the additional verification transaction in POS blocks, meaning the pubkey address receives more coins for every POS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.


ac_reward ac_halving ac_end ac_perc ac_pubkey ac_staked
=======================================================

``./komodod -ac_name=5REWHALVENDPERCSTAKE -ac_supply=100 -ac_reward=100000000 -ac_halving=20000 -ac_end=100000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=90``

100 coin premine

1 coin block reward

Block reward decreases by 50% every 20000 blocks.

Block reward ends at block 100000.

Chain adjusts difficulty so 90% of blocks are proof of stake, 10% proof of work.

The pubkey address receives an additional 1% of the block reward for each mined block. For example, before the first halving, the pubkey address will receive 0.01 coin(1% of 1 coin block reward) for every mined block. After the first halving, the pubkey address will receive 0.005 coin for every mined block.(1% of 0.5 block reward)

Pubkey address receives an additional 1% for every transaction made on the chain. For example, if a transaction sends 100 coins, 1 additional coin is created and sent to the pubkey address. This includes the additional verification transaction in POS blocks, meaning the pubkey address receives more coins for every POS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_decay ac_end ac_perc ac_pubkey ac_staked
=====================================================
``./komodod -ac_name=5REWDECENDPERCSTAKE -ac_supply=1000 -ac_reward=500000000 -ac_decay=75000000 -ac_end=10000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=60``

1000 coin premine

5 coin block reward

Block reward ends at block 10000.

``ac_decay`` has no effect without ``ac_halving`` and ``ac_reward`` both set.

Chain adjusts difficulty so 60% of blocks are proof of stake, 40% proof of work.

Pubkey address receives 0.5 coin for every mined block.(an additional 10% of block reward)

Pubkey address receives an additional 10% for every transaction made on the chain. For example, if a transaction sends 100 coins, 10 additional coin is created and sent to the pubkey address. This includes the additional verification transaction in POS blocks, meaning the pubkey address receives more coins for every POS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_halving ac_decay ac_end ac_perc ac_pubkey ac_staked
======================================================
``./komodod -ac_name=5HALVDECENDPERCSTAKE -ac_supply=1000000 -ac_halving=10000 -ac_decay=75000000 -ac_end=100000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=50``

``ac_halving`` and ``ac_decay``have no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not work at all because ``ac_reward`` is not set.

Number of parameters: 6
***********************

ac_reward ac_halving ac_decay ac_end ac_perc ac_pubkey ac_staked
=================================================================

``./komodod -ac_name=6REWHALVDECENDPERCSTAKE -ac_supply=100000000 -ac_reward=100000000000 -ac_halving=100000 -ac_decay=75000000 -ac_end=1000000 -ac_perc=500000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=1``

100000000 coin premine

1000 coin block reward

Block reward decreases by 25% every 100000 blocks

Block reward ends at block 1000000

Chain adjusts difficulty so 1% of blocks are proof of stake, 99% proof of work.

The pubkey address receives an additional 0.5% of the block reward for each mined block. For example, before the first halving, the pubkey address will receive 5 coins(0.5% of 1000 coin block reward) for every mined block. After the first halving, the pubkey address will receive 3.75 coins for every mined block.(0.5% of 750 block reward)
Pubkey address receives an additional 0.5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 0.5 coin are created and sent to the pubkey address. This includes the additional verification transaction in POS blocks, meaning the pubkey address receives more coins for every POS block.
``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.
