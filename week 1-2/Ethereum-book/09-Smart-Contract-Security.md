## Smart Contract Security

Smart contract security is important to secure millions locked up in smart contracts and decentralized finance protocols. With the growing number of hacks and exploits, it has become paramount to advance and strengthen the security of smart contracts and return trust to the blockchain ecosystem.

To this effect, it is important to take note of some security best practices such as:

- Ensure to keep code simple and avoid complexity
- Whenever possible, reuse codes, there are trusted and popular codebases like the ones from openzeppelin, this represent a good example of code reuse
- Ensure that the code is readable for proper auditing
- Carry out proper tests, test everything you can

Some common Security risks and patterns have been observed, amongst such includes:

#### Reentrancy

Reentrancy in smart contracts occurs when states changes are not made before sending out value to an external source. Then this external source maybe an address can be one of a smart contracts which has a fallback function with call that keeps returning back to the contract where the value originated from thereby possibly draining such of all its fund.

solutions such as the checks and effect interaction pattern exist to curb reentrancy attacks.
Also openzeppelin provides a "lock" modifier that ensures that a function runs fully to avoid reentrancy at any given point.

#### Arithmetic Over/Underflows

prior to solidity version 0.8, there existed the problem of arithmetic overflows and underflows. This exist when the maximum value a variable of a kind can hold is exceeded thereby causing it to default to zero. A variable of uint8 for example, can only store numbers from 0 to 255, now attempting to store any number higher than the maximum it can take will cause that value to become 0 which can give unintended results.

libraries such As safemath from openzeppelin were created to solve such problems and have been effective in doing so.

#### Default Visibilities

Functions in solidity have visibility restrictions that tells who can call a contract and where a contract can be called from. A contract with a default visibilty (i.e specifying no visibility such as private, public, external or internal) automatically defaults to public and hence becomes callable by anyone and can be called from the outside. This is a poor design pattern as an external caller can change variable state from outside and get ownership of such a contract thereby wreaking havoc.

A key way to prevent this is to always specify the visibility of functions

#### Entropy Illusion

Entropy refers to the degree of randomness, it is a word existing before the advent of the blockchain and it use to denote how random an event or outcome can be. scientist all over the years have worked hard to find the perfect state of randomness, while it may exist, it becomes difficult and costly to implement. In blockchain technology such randomness play a vital role in the design of dapps such as games and lotteries.

A common way to go about creating randomness in application development would be to use hashes of blockchain data like the block.timestamp, block.difficulty and all, but due to the deterministic nature of the blockchain, miners can manipulate such values thereby finding a way to beat systems built on it.

A popular solution approach would be to use source of randomness that are generated offchain via oracles. one popular approach is Chainlink VRF (Verifiable Random Functions). which utilize a proper means for randomness. though this approach is expensive, its result has been shown to be better of.

#### Race Condition/ Front Running

Race conditions or Front Running involves the ability to manipulate the order of transactions for gain. Due to the asynchronous nature of the blockchain it is possible for a transaction that is supposed to be executed before another transaction finally gets to be executed after the later transaction. this can happen when the second transaction sends a higher gas fee along with its call thereby incentivizing the miner to pick it first for processing.

in this kind of situation, an attacker can view details of a pending transaction with monetary value and use this technique to go ahead (front run) of it thereby using the information extracted from it to its own advantage.

One solution to this is to improve the way gas prices are set so that actors can't increase it for their gain. Another method is to hash transaction data and only reveal them after they have been added to the block


Other vulnerability exists such as tx.origin authentication, Denial of service by spamming the network, block.timestamp manipulation, unchecked constructors and lots more

To handle most smart contract vulnerabilities, it is paramount that thorough auditing of the smart contract codes be carried out and also constant research be done to fish out more sophisticatd and improved method of attacks
