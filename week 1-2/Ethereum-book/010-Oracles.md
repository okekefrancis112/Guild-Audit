## Oracles

Oracles in blockchain provides informations from outside sources needed to perform certain task and feed it to smart contracts to enable certain ideas or process function properly and as intended without the limitation of the blockchain. 

This becomes useful in situations where data needed to execute certain task is often required, querying the blockchain at intervals would be expensive for such or due to the deterministic nature of the blockchain such wouldn't be ideal as in the case of randomization.

Oracles are useful for provided data that are best handled offchain such as:

* Random number generation
* Price feeds for exchanges
* Time and interval data
* weather data and political events
* Flight statistics and Geolocation amongst others

All these represents use cases where oracles come in handy by getting such data and making them readily availble for use by smart contracts thereby increasing speed and security.

The Basic design and function of oracles can be seen as the collection of data from off-chain sources, the transference of such data with and signed message and making such data available by putting it into a smart contract's storage. from thence, once this data is received and available in a smart contracts storage, it can then be accessed by other contract via message calls that invoke a retrieve function of the oracles smart contract to get what is needed.

Most oracles exist as centralized systems meaning a centralized system is used to get such data needed by the smart contract for proper functionality, but decentralized oracle providers such as chainlink also exists to cater for the proper idea of decentralization. Examples of functionality provided by chainlink include verifiable random functions and price feed oracle. One can visit the chainlink documentation to get started with these.
