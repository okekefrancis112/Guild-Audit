## Ethereum Clients
An ethereum client is a software application that implements the ethereum specification and communicates over the peer to peer network with other ethereum clients. Ethereum clients can be implemented in various languages and as long as they follow the formal specification, they can listen and communicate with each other. examples of such implementations include:

* parity which is written in rust
* Geth which is written in Go
* Harmony which is written in java

In ethereum and blockchain development, a full node holds the state of the blockchain and can carry out activities such as verifying transactions and mining blocks. this operation are quite heavy and performance intensive.

To run such a node, a user would need a computer that have a large storage space and good processing power. Luckily access to such nodes are provided by third parties like Alchemy, Infura and Quicknode so users subscribe and gain access to the ethereum node for a fee.

Also with the option of running fullnodes, users can also choose to run remote clients which often connects to full nodes for communication and sending transactions. such clients also pass as wallets. examples include metamask and myetherwallet.

Full nodes have numerous advantages such as 

* ability to validate transactions
* communicate directly with any contract on the public blockchain
* can directly deploy contract to the public blockchain amongst others

it also has the disadvantage of been expensive and require longer time to fully synchronize with the blockchain.

For most use cases, it is advised for developers to run nodes as public testnet node or private local blockchain, these have the advantage of

* faster synchronization and less computing resources
* using test ether such as goerli eth to pay for transaction fees; this has no real value and hence accrue no loss.

the downside to using such testnet node include:
* As real money isn't involved, it's hard to test security against real adversaries as no one is incentivized to deliberately attack the network
* Lack of congestion gives a false sense of network usage

Asides from using clients to communicate peer to peer over the network, there exist an interface that allows developers to write programs that use client as gateways to communicate on the blockchain, this interface is the JSON-RPC; A set of remote procedure call (RPC) embedded as Javascript Object Notation (JSON). They vary from different blockchains and serves as interfaces for communication.

Remote ethereum clients as opposed to full clients do not store the full blockchain data, and hence they are easy to setup and use. they can:

* Manage private keys
* create and sign transactions
* interact with dapps
* inject a web3 instance into the web browser as javascript object
* Access RPC servers and lots more

They typically exist as web browser extension and smartphone applications, examples are:
Metamask, MyEtherWallet, Mist and Jaxx.