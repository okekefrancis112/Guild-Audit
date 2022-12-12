## Wallets
wallets serves as the primary user interface to the ethereum network. A wallet is a piece of software that is used to manage users private keys and initiates transactions, it serves as an interface to connect to the blockchain and conveniently allows users view information about their accounts holdings. In practical the balance of a user fund is stored and recorded on the blockchain, A wallet helps view and access such funds. They can also provide further services like allowing users to connect and interact with decentralized applications (dapps).

On the low level, a wallet most important function is the management of private keys

### wallet types
wallets are often differentiated or categorized into two: the Non-deterministic and deterministic wallet. in the non-deterministic wallet, each private keys is independently generated from a different random number and hence not related to each other. where as in the deterministic wallet all the keys are derived from a single master key known as the seed.

most wallets use the deterministic approach which allows users to have multiple accounts all originating from one wallet. to make these wallets more secured, the seeds are often encoded as a list of words for you to write down as a recovery backup. this is commonly known as mnemonic words and ranges between some 12 to 24 words.

The generation of mnemonic code words follow a standard which is described and inline with the Bip39 and defines how to go about it. from this, mnemonic words are generated which seeds are then derived from.