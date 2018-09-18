-addressindex and -spentindex are needed to run an insight explorer
also need for crypto condition chains, but they're both enabled by just having ac_cc
using ac_ccactivate, you need to set both manually(edited)
these rpc commands require both
== Addressindex ==
getaddressbalance
getaddressdeltas
getaddressmempool
getaddresstxids
getaddressutxos
getsnapshot


kv - asset chains only
jumblr - kmd only 
the -donation and -exchange and -notary are KMD specific
-genproclimit=0 is specifically for ac_staked chains
