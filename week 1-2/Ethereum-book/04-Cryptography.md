## Cryptography

Cryptography is the study of secure communications that allow only the sender and intended receipient of a message to view its content. it is applied in ethereum and blockchain to build secured applications. Of particular interest is public key cryptography which is usde to protect ownership of funds and is applied in private keys and addresses.

Public key cryptography uses unique keys to secure information. these keys are based on mathematical functions that have special properties, it is easy to calculate them but hard to calculate their inverse. In essence they represent a one way function

In ethereum, the Public key cryptography is used to create the public-private key pair used accross ethereum accounts. private keys are not stored on the blockchain but instead controls access by being the unique piece of information needed to create digital signatures which are required to sign transactions to spend any fund in the account.

Elliptic curve cryptography is applied in digital signature creation by providing a way for the transaction data to be combined with the private key to create a code that can only be produced with the knowledge of the private key. because public keys are gotten from private key, a message can be verified from the transaction data and all accompanying address to ensure that it originates from the said account.

### Generation
Private keys are generated through a unique source of randomness and suitably between 1 and 2^256. the public key is then generated from the private key using elliptic curve that satifies the equation K = k * G where k is the private key and G is point on the elliptic curve. After the public key is calculated,  keccak256 algorithm is then used to calculate the hash of the public key. (keccak256 is the cryptographic hash function that ethereum uses. hash functions are one way functions which are deterministic and always produce the same length, they are collision resistant too)

After the hash is generated, the last 20 bytes is taken, which then becomes our ethereum address. conventionally 0x is prefixed to it, to form the pattern of the ethereum address we have come to know