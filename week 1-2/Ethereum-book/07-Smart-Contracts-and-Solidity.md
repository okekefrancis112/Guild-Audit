## Smart Contracts and Solidity

Smart contracts can be seen as a piece of computer code that are written and run on the Ethereum blockchain. They are  automatically executed once set conditions are met.
As computer programs they have various characteristics which includes been deterministic and they also immutable.

With regards to the life cycle of a smart contract it is mostly written in high level languages such as solidity, when written they get compiled and then deployed on to the blockchain. To call this smart contract the call has to originate from an externally owned account only. Basically contract addresses are formed by using details from the transaction itself these include combining the originating account address and the nonce to form a new contract address. Now smart contracts will lie dormant until being activated by transaction which of course must come from an externally owned account. when this happens they can be said to come alive. 

most contract can also be destroyed or ended by calling a special opcode which is the self destruct, It is imperative that this functionality be added into this smart contract to enable deleting the code from the blockchain. in practice calling self destruct does not remove the contracts history from the blockchain, it just renders such a contract unusable.

When a transaction is triggered on a smart contract, this transaction has to run to finish before any state's changes can be recorded on the blockchain. if by any means transaction fails, changes are rolled back and it will seem as though transaction never happened. Fee will be collected for its execution until that point, but changes wouldn't be recorded since its transaction never succeeded.

Solidity is the major language used for writing smart contracts on ethereum along with the solidity projects is the solidity compiler which is also used for converting codes written in solidity to EVM bytecode.  

 With this functionality comes the ability to also generate ABI (application binary interface) which contains a JSON format of the functions and variables that exist in this smart contract.

For writing smart contracts it is advised to use the recent version of solidity as it contains updated changes and improvement from past versions there by bringing more functionality to smart contracts.

As a developer it is advised to use the Linux operating system for writing and developing smart contracts accompanied with any simple test editor such as atom or vs code.

#### Data types

Some of Ethereum data type includes Bool which have the values of true or false we have integers signed and unsigned, these also include addresses which are 20 bytes

 we also have struct that contains user defined variables, we also have mapping that represent hash lookup table in form of key value pairs and arrays in form of fixed and dynamic

Predefined variables include such like global variables like msg.sender, msg.value, TX.origin and much more

Solidity offers objects types like interfaces and libraries. interfaces are similar to contracts only that they don't have the function implemented. The functions are only defined but not implemented. A library contract is one that is meant to be deployed only once and used by other contracts, it can contain additional functionalities that can be imported and used in other contracts.

Solidity also makes use of functions that are similar to other programming language with some visibility structures such as private, public, internal and external. Private functions are native to the contracts where public functions can be called outside the contract

It also make use of keywords that affects the behavior of contracts, such as marking a function as view, pure or payable. view functions promised not to modify the state while a pure function can neither read nor write to state. payable is just a keyword that is used to allow a function to be able to accept ether

Solidity also makes use of constructors. inheritance and modifiers. It handles error using assets require and revert.

When transactions completes, it produces transaction receipts which correlates to  events. This event can be emitted to denote the action that havve been performed by this smart Contract. moreso this can be used in development dapps that regularly require data from the blockchain. using events can solve this.

Some tips to watch out for while developing smart contract is gas consideration. a contract properly written with gas optimization becomes user friendly and is encouraged by the ethereum community. now to avoid consumming too much gas some tips should be noted example is to avoid calls to other contracts and avoid using dynamically sized arrays