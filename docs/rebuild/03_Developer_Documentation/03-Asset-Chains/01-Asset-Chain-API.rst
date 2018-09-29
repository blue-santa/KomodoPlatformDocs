===need an index here===

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

* 2 nodes with the ability to open ports (a node can be either a computer or a VPS)
* At least 4gb RAM each
* At least 2 CPU cores each
* 64-bit Operating System (Ubuntu 16.04 recommended)
* ``komodod`` built on each, see :ref:`Installing Komodo Manually` (no need to download the Komodo blockchain)

Notes on the Computers (Nodes) Used to Create an Asset Chain
=============================================================

If you are interested in testing a Komodo asset chain for yourself, please do not hesitate to reach out to us when you are stuck. We frequently have support agents available in our ===link https://komodoplatform.com/discord === Discord #support channel, and for off hours you can file a ticket on ===link https://support.komodoplatform.com/support/home === our support page.

If you are ready to press forward now with your first test asset chain, some basic knowledge about how to connect two nodes (computers) is recommended for the initial setup.

In the most ideal circumstance, the new Komodo developer will already have two virtual private server boxes (VPS's) available for testing. VPS's can be cheap and easy to manage. A typical VPS will automatically have a static external IP that is easily reachable, making connection between two VPS nodes simple.

If the new developer does not have two VPS's available, setting up a test asset chain on two local machines in a home or office-type setting is still achievable, but it may require a little more troubleshooting.

The challenge lies in the way the network is created, and there are myriad network setups. For example, if the developers are operating on a local router, where the two machines are connected via wi-fi, the local ip addresses of the machines are a bit harder to find; the router assigns new local ip addresses to the machines each time they connect. It is not possible to see them from the internet. In this situation, the developer must log into the router's software interface and search for their currently assigned local ip addresses.

This latter scenario can suffice, if you're just looking to test an asset chain quickly and don't want to spend money on a VPS. However, don't be surprised if you need to ask for help. We'll be here for you, when you need us.

You will know that your machines have successfully connected when you can run this command in the shell of one of your machines:

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

With your machines successfully able to ``ping`` each other, you are prepared to create your first asset chain.

The following instructions use the simplest possible set of parameters in creating a new asset chain: a coin with the ticker symbol ``EXAMPLECHAIN``, ``1000000`` pre-mined coins, and a block reward of ``.0001``.

On your first node, change into ===link=== the directory where Komodo's ``komodod`` and ``komodo-cli`` are installed and execute the following commands in the terminal:

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

Part II: Connecting the Second Node
===================================

On the second node you issue the same command, but with the first node's IP address, and an additional setting that initiates mining on this machine: ``-gen -genproclimit=$(nproc)``.

.. code-block:: shell

	./komodod -ac_name=EXAMPLECHAIN -ac_supply=1000000 -addnode=<IP address of the first node> -gen -genproclimit=$(nproc)

When this second node connects it will begin to mine blocks.

The indicated number of pre-mined coins will be deposited into to the wallet of the node that executed ``-gen -genproclimit=$(nproc)``.

You can check the contents of the wallet by executing the following command in another terminal:

.. code-block:: shell

	./komodo-cli -ac_name=EXAMPLECHAIN getwalletinfo

More info can be found in the debug.log of the chain found at:

``~/.komodo/EXAMPLECHAIN/debug.log`` (Mac & GNU/Linux)

``%appdata%\komodo\EXAMPLECHAIN\debug.log`` (Windows)

Querying the Asset Chain
========================

Using the pre-installed ``komodo-cli`` software, you can execute many RPC calls and other API commands to your new asset chain, enabling you to perform transactions, create and execute smart contracts, store data in KV storage, create cross-chain compatible contracts, etc.

Since the Komodo software began as a fork of Zcash and BTC, essentially all commands that are available on these two upstream blockchains are also available on your new asset chain. We have also created many more commands to enhance your creative tool set and development process. Please see our ===link=== API documentation for more information.

Example commands
----------------

On a KMD-based blockchain, the entire coin supply is mined in the first block. As soon as your machines connect in the steps above, your coin supply is distributed into the ``wallet.dat`` file of the machine that mines the first block. You can view this balance by executing the following command on the mining machine:

.. code-block:: shell

	./komodo-cli -ac_name=EXAMPLECHAIN getbalance

These are the coins that you will sell to your future customers, in exchange for whatever cryptocurrency you desire. Also, since you are building on a KMD-based blockchain, you have easy access to our decentralized exchange, and our decentralized-ICO software, and our future upgrades.

To see general information about your new asset chain, execute this command:

.. code-block:: shell

	./komodo-cli -ac_name=EXAMPLECHAIN getinfo

This command returns information about all available RPC and API commands:

.. code-block:: shell

	./komodo-cli -ac_name=EXAMPLECHAIN help

Secure this Asset Chain with Delayed Proof of Work
==================================================

Your new chain can receive the same security of the Bitcoin hash rate with a simple service from our KMD notary nodes, called "delayed Proof of Work" (dPoW).

There are two aspects to the cost for dPoW services. The first comes from the cost of making records in your asset chain's database, and in the records of the KMD main chain. These records are called "notarizations."

Notarizations are performed as transactions on your blockchain and on the main KMD blockchain. The transactions have messages included inside that indicate the most recent and secure state of your asset chain. Your blockchain will know how to recognize and rely on notarizations automatically. Every ten to twenty minutes, all of the information in the KMD chain (including your asset chain's history) is hashed and inserted into the BTC blockchain. Once your information is pushed into BTC, your blockchain will consider all notarized information completely settled and immutable; only the recent, un-notarized transactions are still relying on your asset chain's raw consensus mechanism (===link=== click here to learn more about the types of consensus mechanisms you can choose on a KMD asset chain). Thus, your asset chain will have all the power of Bitcoin securing your blockchain's history.

As the notarizations are transactions, they have a cost to perform, and this cost is covered by the asset-chain developer. Over the course of a year, the cost for performing these transactions is 300 KMD, and 800 of your asset chain's coins.

The second part of the cost of notarization is the payment to the actual Komodo team, which is given in exchange for our services. We have not yet published this rate, as we are still in the discovery phase. Please reach out to us to receive a quote.

Several teams have already signed up for our services and are developing on our platform. From our experience with them we can confidently say that our pricing is generally very (very) affordable, compared to other blockchain services. In many cases, creating a fully independent blockchain on Komodo costs but a small fraction of what it would cost to execute just one smart contract on other blockchain platforms.

In our ecosystem, there are third-party businesses that can help you to initiate and develop your blockchain. @siu (Discord: @siu#3920) is the head of ===link=== ChainMakers, and @PTYX (Discord: @PTYX#6840) is the head of ===link=== Chainzilla. Both can provide different levels of service in asset-chain creation, electrum-server (SPV) setup and maintenance, explorer setup, and other decentralized-technology services.

Please send any critique or feedback of this documentation to either @Alright or @gcharang on matrix or discord.

`Discord Invite <https://discord.gg/SCdf4eh>`_

**********************
Asset Chain Parameters
**********************

The Komodo platform offers various default customizations for determining the underlying nature of your asset chain. The desired combination of parameters should be included with the ``komodod`` execution every time the asset-chain daemon is launched.

Changing these customizations at a later time is possible, but in some circumstances it can require a hard fork of your asset chain. In general, it is best to have your asset chain's parameters finalized before decentralizing the ownership of your coin. Should you discover a need to change these parameters after the fact, please reach out to our development team for assistance.

* Note: for examples of various asset-chain types, see :doc:`example-asset-chains`

-ac_name
========

This is the ticker symbol for the coin you wish to create. We recommended it consist only of numbers and uppercase letters.

All asset chains are required to set ``-ac_name``.

-ac_supply
==========

This is the amount of pre-mined coins you would like the chain to have.

The node that sets ``-gen`` during the creation process will mine these coins in the genesis block.

If ``-ac_supply`` is not set, ``-ac_reward`` must be set, and a default value of 10 coins will be used in the genesis block. If ``-ac_pubkey`` is set, the  pre-mined coins will be mined to the address of the corresponding pubkey.

The ``-ac_supply`` parameter should be set to a whole number without any decimals places. It should also be to set to less than ``2000000000`` to avoid 64-bit overflows.

Note: An additional fraction of a coin will be added to this based on the asset chain's parameters. This is used by nodes to verify the genesis block. For example, the DEX chain's ``-ac_supply`` parameter is set to ``999999``, but in reality the genesis block was ``999999.13521376``.

All chains are required to set ``-ac_supply``.

-ac_reward
==========
This is the block reward for each mined block, given in satoshis. If this is not set, the block reward will be ``10000`` satoshis, and blocks will be on-demand after block 127 (a new block will not be mined unless there is a transaction in the mempool.)

-ac_end
=======
This is the block height in which block rewards will end. Every block after this height will have 0 block reward.

-ac_halving
===========
This is the number of blocks between each block reward halving. This parameter will have no effect if ``-ac_reward`` is not set. The lowest possible value is ``1440`` (~1 day). If this parameter is set, but ``-ac_decay`` is not, the reward will decrease by 50% each halving.

-ac_decay
=========

This is the percentage the block reward will decrease by each block-reward halving. This parameter will have no effect if ``-ac_reward`` is not set.

This is the formula that ``-ac_decay`` follows:

.. code-block:: shell

	numhalvings = (height / -ac_halving);
	for (i=0; i<numhalvings; i++)
	reward_after = reward_before * ac_decay / 100000000;

For example, if this is set to ``750000000``, the block reward will drop 25% from the previous block reward each halving.

-ac_perc
========

The ``-ac_perc`` parameter is the percentage added to both the block reward and to the transactions that will be sent to the ===link=== ``-ac_pubkey`` address. If the ``-ac_perc`` parameter is set, ``-ac_pubkey`` must also be set.

For example, if ``-ac_reward=100000000`` and ``-ac_perc=10000000``, for each block mined, the miner receives 1 coin along with the ``-ac_pubkey`` address receiving 0.1 coin. For every transaction sent, the pubkey address will receive 10% of the overall transaction value. This 10% is not taken from the user, rather it is created at this point. Each transaction inflates the overall supply.

	Note: Vout 1 of each coinbase transaction must be the correct amount sent to the corresponding ``pubkey``. The ``vout`` type for all coinbase vouts must be ``pubkey`` as opposed to ``pubkeyhash``. This only affects a miner trying to use a stratum. Z-nomp is currently incompatible.

-ac_pubkey
==========

The ``-ac_pubkey`` parameter designates a public address for receiving payments from the network. These payments can come in the genesis block, in all blocks mined thereafter, and from every transaction on the network.

It is used in combination with ===link=== ``-ac_perc``, which sets the amount that is sent to the address. If ``ac_perc`` is not set, the only effect of ``ac_pubkey`` is to have the genesis block be mined to the ``pubkey`` specified.

If ``-ac_pubkey`` is set, but ===link=== ``-ac_perc`` is not, this simply means the genesis block will be mined to the set ``pubkey``'s address, and no blocks or transactions thereafter will mine payments into the ``pubkey``.

``pubkey`` must be set to a 33 byte hex string. You can get the pubkey of an address by using the ===link=== ``validateaddress`` command in ``komodod``, and searching for the returned ``pubkey`` property. The address must be imported to the wallet before using ``validateaddress``.

-ac_cc
======

 * **NOTE:** This parameter is still in testing.

The ``-ac_cc`` parameter sets the network cluster on which the chain can interact with other chains via ===link=== cross-chain smart contracts and ===link=== MoMoM technology.

Under most circumstances, this parameter requires the Komodo notarization service to achieve functionality, as it relies on the ``pubkey`` of the trusted notary nodes to ensure coin-supply stability.

Once activated, the ``ac_cc`` parameter can allow features such as cross-chain fungibility -- meaning that coins on one asset chain can be directly transferred to another asset chain that has the same ``ac_cc`` setting and notary nodes with the same ``pubkey``.

-ac_cc=0
--------

Setting ``-ac_cc=0`` disables smart contracts on the asset chain entirely.

-ac_cc=1
--------

Setting ``-ac_cc=1`` permits smart contracts on the asset chain, but will not allow the asset chain to interaction in cross-chain smart contracts with other asset chains.

-ac_cc=2 to 100
---------------

The values of ``2`` through ``100`` indicate asset chains that can import functions across asset chains, but their coins are not fungible.

For example, an asset chain may be able to query another asset chain on the same ``ac_cc`` cluster for details about a transaction.

However, coins may not be transferred between blockchains.

-ac_cc=101 to 9999
------------------

Setting the value of ``ac_cc`` to any value greater than or equal to ``101`` will permit cross-chain interaction with any asset chain that has the same ``ac_cc`` value and is secured by notary nodes with the same ``pubkey``. For example, an asset chain set to ``ac_cc=2`` in its parameters can interact with other asset chains with ``ac_cc=2``, on the same notary-node network, but cannot interact with an asset chain set to ``ac_cc=3``.

-ac_staked
==========

.. note::

	This feature is currently only available in the `jl777 branch <https://github.com/jl777/komodo/tree/jl777>`_.

This is the percentage of blocks the chain will aim to have mined via Proof of Stake (PoS), with the remainder via Proof of Work (PoW). For example, an ``ac_staked=90`` chain will have ~90% PoS blocks/10% PoW blocks. Measurements of the PoS:PoW ratio are approximate; the PoW difficulty will automatically adjust based on the overall percentage of PoW-mined blocks to adhere to the approximate ``PoS`` value.

Each staked block will have an additional transaction added to the coinbase in which the coins that staked the block are sent back to the same address. This is used to verify which coins staked the block, and this allows for compatibility with existing Komodo infrastructure. If ``-ac_staked`` is used in conjunction with ``-ac_perc``, the ``-ac_pubkey`` address will receive slightly more coins for each staked block compared to a mined block because of this extra transaction.

The following are the (current) rules for staking a block:

	#. Block timestamps are used as the monotonically increasing timestamp. It is important to have a synced system clock.

	#. In order to stake, you must use ``-gen -genproclimit=0`` while launching the daemon or ``komodo-cli -ac_name=<CHAINNAME> setgenerate true 0`` after launching the daemon.

	#. A utxo is not eligible without ``nLockTime`` set and until 6000 seconds has passed from this lock time. ``(100 * expected blocktimes) to be exact``

	#. There are 64 different segments(``segids``) of addresses, based on the hash of the destination address. ``((nHeight + addrhash.uints[0]) & 0x3f)`` The segid of an address can be found with the ``validateaddress`` command. Each segid will take turns being segid0 at each height. ``(height % 64) = the segid0 for that height.`` All other segid will adjust the elapsed time by ``segid`` seconds.

	#. A new block is eligible to be staked 2 seconds after median blocktime. For example, segid0 for a given height will be eligible to submit a block 2 seconds after median blocktime, whereas segid1 will be eligible to submit a block 4 seconds after median blocktime. For the next block, segid0 from the previous block will now be segid63 and will be eligible to submit a block 128 seconds after median blocktime. This means by 128 seconds after the median blocktime, all segids are eligible.

	#. Coinage calculated from the adjusted time is used to divide hash(address + pastblockhash) to create the value compared against the difficulty to determine if a block is won or not. This means a UTXO is more likely to win a block within a segid based on age of the UTXO and amount of coins.

To create a chain using this parameter, start the first node with ``-gen -genproclimit=0``. Start the second node with ``-gen -genproclimit=$(nproc)``. Send coins from the second node to the first node, and it will begin staking. The first 100 blocks will allow PoW regardless of the ``ac_staked`` value.

	Note: On a chain using a high percentage for PoS, it's vital to have coins staking by block 100.  If too many PoW blocks are mined consecutively at the start of the chain, the PoW difficulty may increase enough to stop the chain entirely. This can prevent users from sending transactions to staking nodes.

	Note: It is also vital to stake coins in all 64 segids. For the time being, you can use the `genaddresses.py` script in `this repo <https://github.com/alrighttt/dockersegid>`_ to generate an address for each segid. This functionality will soon be integrated directly into the daemon. You can use the ``getbalance64`` command to get the balance you currently have in each segid you are staking in.

-ac_public
==========

.. note::
	This feature is currently only available in the `jl777 branch <https://github.com/jl777/komodo/tree/jl777>`_.

If ``ac_public`` is set to ``1``, zk-SNARKs are disabled, and all z address functionalilty is disabled. Therefore, all transactions on the blockchain are public.

-ac_private
===========

.. note::
	This feature is currently only available in the `jl777 branch <https://github.com/jl777/komodo/tree/jl777>`_.

If ``ac_private`` is set to ``1``, all transactions other than coinbase transactions (block rewards) must use zk-SNARKs. All transparent address functionality other than sending mined coins from transparent addresses is disabled.

Please send any critiques or feedback to Alright or gcharang on matrix or discord.

`Discord Invite <https://discord.gg/SCdf4eh>`_

********************
Example Asset Chains
********************

The following are a collection of example asset chains, for educational purposes.

The parameters ``ac_name`` , ``ac_supply`` , ``ac_pubkey`` are not counted when grouping based on the ``Number of parameters``.

Number of parameters: 1
***********************

ac_reward
=========

``./komodod -ac_name=1REW -ac_supply=999999 -ac_reward=100000000``

A ``999999`` coin pre-mine, with a 1 coin block reward that does not end. (Recall that ``ac_supply`` is given in coins, while ``ac_reward`` is given in satoshis.)

ac_halving
==========

``./komodod -ac_name=1HALV -ac_supply=999999 -ac_halving=2000``

A 999999-coin pre-mine, with a default block reward of 0.0001 coin, and on-demand blocks after block 128

The ``ac_halving`` value has no effect on the asset chain, as ``ac_reward`` is not set.

ac_decay
========
``./komodod -ac_name=1DECAY -ac_supply=999999 -ac_decay=50000000``

A 999999-coin pre-mine, with a default block reward of 0.0001 coin, and on-demand blocks after block 128.

The ``ac_decay`` value has no effect as ``ac_reward`` is not set.

ac_end
======

``./komodod -ac_name=1END -ac_supply=999999 -ac_end=25000``

A 999999-coin pre-mine, with a default block reward of 0.0001 coin, and on-demand blocks after block 128.

The block reward ends at block 25000.

Number of parameters: 2
***********************

ac_reward ac_staked
===================

``./komodod -ac_name=1STAKE -ac_supply=999999 -ac_reward=100000000 -ac_staked=90``

A 999999-coin pre-mine with a 1-coin block reward. The chain adjusts difficulty to keep 90% of blocks mined via PoS, and 10% mined via PoW.

ac_perc ac_pubkey
=================

``./komodod -ac_name=1PERC -ac_supply=999999 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain will not function because ``ac_reward`` is not set.

ac_reward ac_halving
====================

``./komodod -ac_name=2REWHALV -ac_supply=999999 -ac_reward=500000000 -ac_halving=2000``

A 999999-coin pre-mine, with a 5-coin block reward, and the block reward decreases by 50% every 2000 blocks.

ac_reward ac_decay
==================

``./komodod -ac_name=2REWDECAY -ac_supply=999999 -ac_reward=500000000 -ac_decay=75000000``

A 999999-coin pre-mine, with a 5-coin block reward.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

ac_reward ac_end
================

``./komodod -ac_name=2REWEND -ac_supply=999999 -ac_reward=500000000 -ac_end=200``

A 999999-coin pre-mine, with a 5-coin block reward, and the block reward ends at block 200.

ac_reward ac_perc ac_pubkey
===========================

``./komodod -ac_name=2REWPERC -ac_supply=999999 -ac_reward=500000000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

A 999999-coin pre-mine with a 5-coin block reward. The pubkey address receives 0.25-coin for every mined block (an additional 5% above the baseline block reward).

The pubkey address also receives an additional 5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins are added to the coin supply and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_staked
===================

``./komodod -ac_name=2REWSTAKE -ac_supply=100000 -ac_reward=1000000000 -ac_staked=2``

A 100000 coin pre-mine with a 10-coin block reward. The chain adjusts difficulty so 2% of blocks are mined via PoS, 98% via PoW.

ac_halving ac_decay
===================

``./komodod -ac_name=2HALVDECAY -ac_supply=999999 -ac_halving=2000 -ac_decay=50000000``

A 999999-coin pre-mine, with the default block reward of 0.0001 coin, and on-demand blocks after block 128.

``ac_halving`` and ``ac_decay`` have no effect if ``ac_reward`` is not set.

ac_halving ac_end
=================

``./komodod -ac_name=2HALVEND -ac_supply=999999 -ac_halving=2000 -ac_end=10000``

A 999999-coin pre-mine, with the default block reward of 0.0001 coin, blocks are on-demand after block 128k, and the block reward ends at block 10000.

``ac_halving`` has no effect without ``ac_reward`` being set.

ac_halving ac_perc ac_pubkey
============================

``./komodod -ac_name=2HALVPERC -ac_supply=999999 -ac_halving=2000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.

Also, ``ac_halving`` has no effect if ``ac_reward`` is not set.

ac_halving ac_staked
====================

``./komodod -ac_name=2HALVSTAKE -ac_supply=999999 -ac_halving=2000 -ac_staked=10``

A 999999-coin pre-mine, with the default block reward of 0.0001 coin, and the chain adjusts difficulty so 10% of blocks are mined via PoS, 90% via PoW.

``ac_halving`` has no effect without ``ac_reward`` being set.

ac_decay ac_end
===============

``./komodod -ac_name=2DECEND -ac_supply=999999 -ac_decay=5000000 -ac_end=10000``

A 999999-coin pre-mine, with the default block reward of 0.0001 coin, blocks are on-demand after block 128, and the block reward ends at block 10000.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

ac_decay ac_perc ac_pubkey
==========================

``./komodod -ac_name=2DECPERC -ac_supply=999999 -ac_decay=75000000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not function, because ``ac_reward`` is not set.

Also, ``ac_decay`` has no effect when either of ``ac_reward`` and ``ac_halving`` are not set.

ac_decay ac_staked
==================

``./komodod -ac_name=2DECAYSTAKE -ac_supply=999999 -ac_decay=5000000 -ac_staked=50``

A 999999-coin pre-mine, with the default block reward of 0.0001 coin, and the chain adjusts difficulty so 50% of blocks are mined via PoS, 50% via PoW.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

ac_end ac_perc ac_pubkey
========================

``./komodod -ac_name=2ENDPERC -ac_supply=999999 -ac_end=10000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.

ac_end ac_staked
================

``./komodod -ac_name=2ENDSTAKE -ac_supply=999999 -ac_end=10000 -ac_staked=5``

A 999999-coin pre-mine, with the default block reward of 0.0001 coin, the block reward ends at block 10000, and the chain adjusts difficulty so 5% of blocks are mined via PoS, 95% via PoW.

ac_perc ac_pubkey ac_staked
===========================

``./komodod -ac_name=2PERCSTAKE -ac_supply=999999 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=50``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain does not function, because ``ac_reward`` is not set.

ac_reward ac_halving ac_decay
=============================

``./komodod -ac_name=3REWHALVDEC -ac_supply=999999 -ac_reward=1000000000 -ac_halving=2000 -ac_decay=75000000``

A 999999-coin pre-mine, with a 10-coin block reward, and the block reward decreases by 25% every 2000 blocks.

ac_reward ac_halving ac_end
===========================

``./komodod -ac_name=3REWHALVEND -ac_supply=999999 -ac_reward=500000000 -ac_halving=2000 -ac_end=10000``

A 999999-coin pre-mine, with a 5-coin block reward, the block reward decreases by 50% every 2000 blocks, and the block reward ends at block 10000.

ac_reward ac_halving ac_perc ac_pubkey
======================================

``./komodod -ac_name=3REWHALVPERC -ac_supply=999999 -ac_reward=500000000 -ac_halving=1440 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_perc=50000000``

A 999999-coin pre-mine, with a 5-coin block reward, and the block reward decreases by 50% every 1440 blocks. The pubkey address receives an additional 50% above the block reward for each mined block. For example, before the first halving the pubkey address will receive 2.5 coins (50% above the 5-coin block reward, for a total of 7.5 coins) for every mined block. After the first halving, the pubkey address will receive 1.25 coins (for a total of 3.75 coins).

The pubkey address receives an additional 50% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 50 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.


ac_reward ac_halving ac_staked
==============================

``./komodod -ac_name=3REWHALVSTAKE -ac_supply=999999 -ac_reward=100000000 -ac_havling=2000 -ac_staked=10``

A 999999-coin pre-mine, with a 1-coin block reward, block reward decreases by 50% every 2000 blocks, and the chain adjusts difficulty so 10% of blocks are mined via PoS, 90% via PoW.

ac_reward ac_decay ac_end
=========================

``./komodod -ac_name=3REWDECEND -ac_supply=999999 -ac_reward=500000000 -ac_decay=75000000 -ac_end=5000``

A 999999-coin pre-mine, with a 5-coin block reward, and the block reward ends at block 5000.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

ac_reward ac_decay ac_perc ac_pubkey
====================================

``./komodod -ac_name=3REWDECPERC -ac_supply=999999 -ac_reward=500000000  -ac_decay=75000000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

A 999999-coin pre-mine with a 5-coin block reward. The pubkey address receives 0.5 coin for every mined block (an additional 10% above the block reward). The pubkey address receives an additional 10% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 10 coins are created and sent to the pubkey address.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_decay ac_staked
============================

``./komodod -ac_name=3REWDECSTAKE -ac_supply=999999 -ac_reward=1000000000 -ac_decay=25000000 -ac_staked=50``

A 999999-coin pre-mine, with a 10-coin block reward, and the chain adjusts difficulty so 50% of blocks are mined via PoS, 50% via PoW.

``ac_decay`` has no effect if ``ac_halving`` is not set.

ac_reward ac_end ac_perc ac_pubkey
==================================

``./komodod -ac_name=3ENDPERCREW -ac_supply=999999 -ac_reward=5000000000 -ac_end=10000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

A 999999-coin pre-mine, with a 50-coin block reward, and the block reward ends at block 10000. The pubkey address receives 2.5 coins (an additional 5% above the block reward) for every mined block before block 10000. The pubkey address receives an additional 5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be pubkey as opposed to pubkeyhash.

ac_reward ac_end ac_staked
==========================

``./komodod -ac_name=3REWENDSTAKE -ac_supply=500000 -ac_reward=10000000000 -ac_end=15000 -ac_staked=60``

A 500000 coin pre-mine, with a 100-coin block reward, the block reward ends at block 15000, and the chain adjusts difficulty so 60% of blocks are mined via PoS, 40% via PoW.

ac_reward ac_perc ac_pubkey ac_staked
=====================================

``./komodod -ac_name=3REWPERCSTAKE -ac_supply=1000000 -ac_reward=1000000000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=50``

A 1000000-coin pre-mine, a 10-coin block reward, the chain adjusts difficulty so 50% of blocks are mined via PoS, 50% via PoW. The pubkey address receives 1 coin for every mined block (an additional 10% above the block reward). The pubkey address receives an additional 10% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins are created and sent to the pubkey address. This includes the additional verification transaction in PoS blocks, meaning the pubkey address receives more coins for every PoS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_halving ac_decay ac_end
==========================

``./komodod -ac_name=3HALVDECEND -ac_supply=999999 -ac_end=100000 -ac_halving=5000 -ac_end=100000``

A 999999-coin pre-mine, with the default block reward of .0001, blocks are on-demand after block 128, and the block reward ends at block 100000.

``ac_halving`` has no effect if ``ac_reward`` is not set.

ac_halving ac_decay ac_perc ac_pubkey
=====================================

``./komodod -ac_name=3HALVDECPERC -ac_supply=999999 -ac_halving=2000 -ac_decay=25000000 -ac_perc=90000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_halving`` has no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.


ac_halving ac_decay ac_staked
=============================

``./komodod -ac_name=3HALVDECSTAKE -ac_supply=50000 -ac_halving=2000 -ac_decay=45000000 -ac_staked=40``

A 50000-coin pre-mine, and the hain adjusts difficulty so 40% of blocks are mined via PoS, 60% via PoW.

``ac_halving`` and ``ac_decay`` have no effect if ``ac_reward`` is not set

ac_halving ac_end ac_perc ac_pubkey
===================================
``./komodod -ac_name=3HALVENDPERC -ac_supply=999 -ac_halving=1441 -ac_end=20000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_halving`` has no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.


ac_halving ac_end ac_staked
===========================
``./komodod -ac_name=3HALVENDSTAKE -ac_supply=50000 -ac_halving=2000 -ac_end=10000 -ac_staked=50``

A 50000-coin pre-mine, with a default block reward of 0.0001 coin, the block reward ends at block 10000, and chain adjusts difficulty so 50% of blocks are mined via PoS, 50% via PoW.

``ac_halving` has no effect if ``ac_reward`` is not set.

ac_halving ac_perc ac_pubkey ac_staked
======================================
``./komodod -ac_name=3HALVPERCSTAKE -ac_supply=99999 -ac_halving=2000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=10``

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.

ac_decay ac_end ac_perc ac_pubkey
=================================
``./komodod -ac_name=3DECENDPERC -ac_supply=10000 -ac_decay=75000000 -ac_end=100000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.


ac_decay ac_end ac_staked
=========================
``./komodod -ac_name=3DECENDSTAKE -ac_supply=800000 -ac_decay=20000000 -ac_end=20000 -ac_staked=60``

A 800000-coin pre-mine, the default block reward of 0.0001 coin, the block reward ends at block 20000, chain adjusts difficulty so 60% of blocks are mined via PoS, 40% via PoW.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

ac_decay ac_perc ac_pubkey ac_staked
====================================
``./komodod -ac_name=3DECPERCSTAKE -ac_supply=77777 -ac_decay=40000000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.


ac_end ac_perc ac_pubkey ac_staked
==================================
``./komodod -ac_name=3ENDPERCSTAKE -ac_supply=999999 -ac_end=70000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=10``

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.

ac_reward ac_halving ac_decay ac_end
====================================

``./komodod -ac_name=4REWHALVDECEND -ac_supply=1000000 -ac_reward=10000000000 -ac_halving=10000 -ac_decay=25000000 -ac_end=100000``

A 1000000-coin pre-mine, a 100-coin block reward, the block reward decreases by 75% every 10000 blocks, and the block reward ends at block 100000.

ac_reward ac_halving ac_decay ac_perc ac_pubkey
===============================================

``./komodod -ac_name=4REWHALVDECPERC -ac_supply=999999 -ac_reward=1000000000 -ac_halving=5000 -ac_decay=60000000 -ac_perc=5000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

A 999999-coin pre-mine, a 10-coin block reward, and the block reward decreases 40% every 5000 blocks. The pubkey address receives an additional 5% above the block reward for each mined block. For example, before the first halving, the pubkey address will receive 0.5 coin (5% of the 10-coin block reward) for every mined block. After the first halving, the pubkey address will receive 0.3 coin for every mined block (5% of the 6-coin block reward). The pubkey address receives an additional 5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_halving ac_decay ac_staked
=======================================

``./komodod -ac_name=4REWHALVDECSTAKE -ac_supply=99999 -ac_reward=1000000000000 -ac_halving=2000 -ac_decay=60000000 -ac_staked=50``

A 99999-coin pre-mine, a 10000-coin block reward, the block reward decreases by 40% every 2000 blocks, and the chain adjusts difficulty so 50% of blocks are mined via PoS, 50% via PoW.

ac_reward ac_halving ac_end ac_perc ac_pubkey
=============================================

``./komodod -ac_name=4REWPERCENDHALV -ac_supply=999999 -ac_reward=1000000000 -ac_halving=2000 -ac_end=60005 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_perc=10000000``

A 999999-coin pre-mine, a 10-coin block reward, the block reward decreases by 50% every 2000 blocks, and the block reward ends at block 60005. The pubkey address receives an additional 10% above the block reward for each mined block. For example, before the first halving, the pubkey address will receive 1 coin (10% of 10-coin block reward) for every mined block. After the first halving, the pubkey address will receive 0.5 coin for every mined block. The pubkey address receives an additional 10% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 10 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_halving ac_end ac_staked
=====================================

``./komodod -ac_name=4REWHALVENDSTAKE -ac_supply=99999 -ac_reward=10000000 -ac_halving=5000 -ac_end=50000 -ac_staked=40``

A 99999-coin pre-mine, a 0.1 coin block reward, the block reward decreases by 50% every 5000 blocks, the block reward ends at block 50000, and the chain adjusts difficulty so 40% of blocks are mined via PoS, 60% via PoW.

ac_reward ac_halving ac_perc ac_pubkey ac_staked
================================================

``./komodod -ac_name=4PERCREWHALVSTAKE -ac_supply=999999 -ac_reward=1000000000 -ac_halving=2000 -ac_perc=5000000 -ac_staked=50 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

A 999999-coin pre-mine, a 10-coin block reward, block reward decreases by 50% every 2000 blocks, and the chain adjusts difficulty so 50% of blocks are mined via PoS, 50% via PoW. The pubkey address receives an additional 5% above the block reward for each mined block. For example, before the first halving, the pubkey address will receive 0.5 coin (5% above the 10-coin block reward) for every mined block. After the first halving, the pubkey address will receive 0.25-coin for every mined block. The pubkey address receives an additional 5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 5 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_decay ac_end ac_perc ac_pubkey
===========================================
``./komodod -ac_name=4REWDECENDPERC -ac_supply=70000 -ac_reward=700000000 -ac_decay=80000000 -ac_end=10000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

A 70000-coin pre-mine, with a 7-coin block reward, and the block reward ends at block 10000. The pubkey address receives .07-coin for every mined block. (an additional 1% above the block reward). The pubkey address receives an additional 1% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 1 coin is created and sent to the pubkey address.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_decay ac_end ac_staked
===================================
``./komodod -ac_name=4REWDECENDSTAKE -ac_supply=999999 -ac_reward=500000000 -ac_decay=75000000 -ac_end=12000 -ac_staked=40``

A 999999-coin pre-mine, with a 5-coin block reward, the block reward ends at block 12000, and the chain adjusts difficulty so 40% of blocks are mined via PoS, 60% via PoW.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

ac_reward ac_decay ac_perc ac_pubkey ac_staked
==============================================
``./komodod -ac_name=4REWDECPERCSTAKE -ac_supply=9000 -ac_reward=1000000000 -ac_decay=80000000 -ac_perc=2000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=80``

A 9000-coin pre-mine, and a 10-coin block reward. The pubkey address receives 0.2 coin for every mined block (an additional 2% above the block reward). The pubkey address receives an additional 2% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 2 coins are created and sent to the pubkey address. This includes the additional verification transaction in PoS blocks, meaning the pubkey address receives more coins for every PoS block.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_end ac_perc ac_pubkey ac_staked
============================================

``./komodod -ac_name=4REWENDPERCSTAKE -ac_supply=999999 -ac_reward=5000000000 -ac_end=10000 -ac_staked=33 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

A 999999-coin pre-mine, a 50-coin block reward, the block rewards ends at block 10000, and the chain adjusts difficulty so 33% of blocks are mined via PoS, 67% via PoW.

The pubkey address receives 0.5 coin for every mined block (an additional 1% above the block reward). The pubkey address receives an additional 1% for every transaction made on the chain. For example, if a transaction sends 100 coins, 1 additional coin is created and sent to the pubkey address. This includes the additional verification transaction in PoS blocks, meaning the pubkey address receives more coins for every PoS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_halving ac_decay ac_end ac_perc ac_pubkey
============================================
``./komodod -ac_name=4HALVDECENDPERC -ac_supply=11 -ac_halving=5000000 -ac_decay=1000000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

``ac_halving`` has no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.

ac_halving ac_decay ac_end ac_staked
====================================
``./komodod -ac_name=4HALVDECENDSTAKE -ac_supply=999999 -ac_halving=5000 -ac_decay=60000000 -ac_end=25000 -ac_staked=10``

A 999999-coin pre-mine, the default block reward of .0001 coin, the block reward ends at block 25000, and the chain adjusts difficulty so 10% of blocks are mined via PoS, 90% via PoW.

``ac_halving`` and ``ac_decay`` have no effect if ``ac_reward`` is not set

ac_halving ac_decay ac_perc ac_pubkey ac_staked
===============================================
``./komodod -ac_name=4HALVDECPERCSTAKE -ac_supply=40000 -ac_halving=5000 -ac_decay=75000000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=60``

``ac_halving`` and ``ac_decay`` have no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.

ac_halving ac_end ac_perc ac_pubkey ac_staked
=============================================
``./komodod -ac_name=4HALVENDPERCSTAKE -ac_supply=99999 -ac_halving=6000 -ac_end=60000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=30``

``ac_halving`` has no effect if ``ac_reward`` is not set

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.

ac_decay ac_end ac_perc ac_pubkey ac_staked
===========================================
``./komodod -ac_name=4DECENDPERCSTAKE -ac_supply=999999 -ac_decay=75000000 -ac_end=100000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=40``

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.

Number of parameters: 5
***********************

ac_reward ac_halving ac_decay ac_end ac_perc ac_pubkey
======================================================

``./komodod -ac_name=5REWHALVDECENDPERC -ac_supply=999999 -ac_reward=10000000000 -ac_halving=10000 -ac_decay=75000000 -ac_end=100000 -ac_perc=2000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392``

A 999999-coin pre-mine, a 100-coin block reward, the block reward reduces by 25% every 10000 blocks, and the block reward ends at block 100000. The pubkey address receives an additional 2% above the block reward for each mined block. For example, before the first halving, the pubkey address will receive 2 coins (2% of 100-coin block reward) for every mined block. After the first halving, the pubkey address will receive 1.5 coins for every mined block (2% of 75-coin block reward).

The pubkey address receives an additional 2% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 2 coins are created and sent to the pubkey address.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_halving ac_decay ac_end ac_staked
==============================================

``./komodod -ac_name=5REWHALVDECENDSTAKE -ac_supply=50000 -ac_reward=500000000 -ac_halving=5000 -ac_decay=70000000 -ac_end=100000 -ac_staked=80``

A 50000-coin pre-mine, a 5-coin block reward, the block reward decreases by 30% every 5000 blocks, the block reward ends at block 100000, and the chain adjusts difficulty so 80% of blocks are mined via PoS, 20% via PoW.


ac_reward ac_halving ac_decay ac_perc ac_pubkey ac_staked
=========================================================

``./komodod -ac_name=5REWHALVDECPERCSTAKE -ac_supply=1 -ac_reward=50000000000 -ac_halving=2000 -ac_decay=25000000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=50``

A 1-coin pre-mine, a 500-coin block reward, the block reward decreases by 75% every 2000 blocks, and the chain adjusts difficulty so 50% of blocks are mined via PoS, 50% via PoW. The pubkey address receives an additional 1% above the block reward for each mined block. For example, before the first halving, the pubkey address will receive 5 coins (1% of 500 coin block reward) for every mined block. After the first halving, the pubkey address will receive 1.25 coins for every mined block (1% of 125 block reward).

The pubkey address receives an additional 1% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 1 coin is created and sent to the pubkey address. This includes the additional verification transaction in PoS blocks, meaning the pubkey address receives more coins for every PoS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_halving ac_end ac_perc ac_pubkey ac_staked
=======================================================

``./komodod -ac_name=5REWHALVENDPERCSTAKE -ac_supply=100 -ac_reward=100000000 -ac_halving=20000 -ac_end=100000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=90``

A 100-coin pre-mine, a 1-coin block reward, the block reward decreases by 50% every 20000 blocks, the block reward ends at block 100000, and chain adjusts difficulty so 90% of blocks are mined via PoS, 10% via PoW.

The pubkey address receives an additional 1% above the block reward for each mined block. For example, before the first halving, the pubkey address will receive 0.01 coin (1% of the 1-coin block reward) for every mined block. After the first halving, the pubkey address will receive 0.005-coin for every mined block. (1% of 0.5 block reward)

The pubkey address receives an additional 1% for every transaction made on the chain. For example, if a transaction sends 100 coins, 1 additional coin is created and sent to the pubkey address. This includes the additional verification transaction in PoS blocks, meaning the pubkey address receives more coins for every PoS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_reward ac_decay ac_end ac_perc ac_pubkey ac_staked
=====================================================
``./komodod -ac_name=5REWDECENDPERCSTAKE -ac_supply=1000 -ac_reward=500000000 -ac_decay=75000000 -ac_end=10000 -ac_perc=10000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=60``

A 1000-coin pre-mine, a 5-coin block reward, the block reward ends at block 10000, and the chain adjusts difficulty so 60% of blocks are mined via PoS, 40% via PoW.

The pubkey address receives 0.5 coin for every mined block (an additional 10% above the block reward). The pubkey address receives an additional 10% for every transaction made on the chain. For example, if a transaction sends 100 coins, 10 additional coins are created and sent to the pubkey address. This includes the additional verification transaction in PoS blocks, meaning the pubkey address receives more coins for every PoS block.

For ``ac_decay`` to have an effect, both ``ac_halving`` and ``ac_reward`` must be set.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.

ac_halving ac_decay ac_end ac_perc ac_pubkey ac_staked
======================================================
``./komodod -ac_name=5HALVDECENDPERCSTAKE -ac_supply=1000000 -ac_halving=10000 -ac_decay=75000000 -ac_end=100000 -ac_perc=1000000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=50``

``ac_halving`` and ``ac_decay``have no effect if ``ac_reward`` is not set.

If ``ac_perc`` is set, ``ac_reward`` must be set also. This chain is not functional, because ``ac_reward`` is not set.

ac_reward ac_halving ac_decay ac_end ac_perc ac_pubkey ac_staked
=================================================================

``./komodod -ac_name=6REWHALVDECENDPERCSTAKE -ac_supply=100000000 -ac_reward=100000000000 -ac_halving=100000 -ac_decay=75000000 -ac_end=1000000 -ac_perc=500000 -ac_pubkey=027dc7b5cfb5efca96674b45e9fda18df069d040b9fd9ff32c35df56005e330392 -ac_staked=1``

A 100000000-coin pre-mine, a 1000-coin block reward, the block reward decreases by 25% every 100000 blocks, the block reward ends at block 1000000, and the chain adjusts difficulty so 1% of blocks are mined via PoS, 99% via PoW.

The pubkey address receives an additional 0.5% above the block reward for each mined block. For example, before the first halving, the pubkey address will receive 5 coins (0.5% of 1000 coin block reward) for every mined block. After the first halving, the pubkey address will receive 3.75 coins for every mined block (0.5% of 750-block reward). The pubkey address receives an additional 0.5% for every transaction made on the chain. For example, if a transaction sends 100 coins, an additional 0.5 coins are created and sent to the pubkey address. This includes the additional verification transaction in PoS blocks, meaning the pubkey address receives more coins for every PoS block.

``ac_perc`` chains are currently incompatible with z-nomp. The coinbase transaction vout type must be ``pubkey`` as opposed to ``pubkeyhash``.
