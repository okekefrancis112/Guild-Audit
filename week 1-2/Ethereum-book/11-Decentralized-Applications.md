## Decentralized Applications

Decentralized Applications (Dapps) unlike its counterpart in the web2 world is all about decentralization with no central point of failure, though they share similar technology used in building the user interface, dapps have the added functionality of been resilient as the business logic is controlled by smart contract, it is also transparent as everyone can inspect the code and be sure of its function. Also by not been controlled by a centralized body, it is censorship resistant hence user can always interact with it at all times without any fear of interference.

Basically a full fledged dapp would consist of the following:
* Backend Software
* Frontend Software
* Data Storage mechanism
* Name Resolution

For the most part, the backend of many decentralized applications is written in solidity which dictates the business logic and the core functionality such an application will have.

The Frontend can be designed with numerous technology out there ranging from basic HTML, CSS, Javascript to frameworks such as React, Vue and NextJs. Linking this frontend to the backend is done with libraries such as Ethersjs and web3js, but recently there are solutions like WAGMI and connectkit that offers easy to start templates for connecting the frontend to the backend.

For Data Storage, decentralized data storage solution such as IPFS and Filecoin exist to store data, due to the nature and expense of the blockchain, it is impractical to store huge amount of data onchain as this can be slow and expensive to access. so it makes more sense to use offchain solutions. A good thing with these decentralized storage solutions is data hiding as they use hashes to identify files stored on them.

Other aspect of a dapp include inter message communication which is can be handle by services such as "whisper" and name resolution which is often provided by the Ethereum's name service popularly known as ENS

Although advancements and development is working towards creating fully decentralized systems and applications, we are not quite there yet, as most solutions rely on a form of centralizaton or two. This is due to the ease and low cost of setting up centralized system be it servers or storage mechanism. But as time goes on and more people embrace the web3 innovation it will become common to see fully decentralized systems