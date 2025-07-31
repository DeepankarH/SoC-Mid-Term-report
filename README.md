# SoC-Mid-Term-report
Blockchain Technology is a type of ledger that stores information about all transactions.  

In blockchain data is stored in a block and each block is connected to its previous and next block, like in linked list.  

Types of blockchain network:  

Public – Public blockchains are open to all participants allowing anyone to view modify and authenticate the blockchain.  

Private - A private blockchain is a type of blockchain network where access and participation are restricted to a specific group of authorized individuals or organizations.  

Consortium - A consortium blockchain is a type of blockchain network that is managed by a group of organizations instead of just one company or being open to everyone. Only selected members (like companies or institutions) can join, share data, and help validate transactions.  

Hybrid - A hybrid blockchain combines the features of both public and private blockchains, offering a 
a private, permissioned network while also integrating with public, permissionless systems.  

Cryptography is the technique of securing information by converting it into a code that can only be read by those who are permitted to do so.  
Encryption − Conversion of plaintext into ciphertext, making it unreadable to unauthorized parties.  
Decryption – Conversion of encoded message to readable form.  

Types of Network Systems:  
Centralized Systems: One central authority manages all operations and data (e.g., Google, Amazon).  
Decentralized Systems: Control is spread among several nodes, reducing reliance on a central server.  
Distributed Systems: Data and computation are spread across many nodes, increasing resilience and scalability.  

Smart contracts – They are computer programs stored on a blockchain that automatically carry out the terms of a contract when predefined conditions are met.  
Autonomous Agents - Artificially intelligent software that work to accomplish certain objectices without much human intervention.  
Decentralized Organizations (DOs): Software-based organizations running on blockchain, where rules and interactions are encoded in smart contracts.  
D-apps – D-apps are software solutions that operate on a blockchain or a peer-to-peer (P2P) network of computers, rather than being hosted on a single machine.  
DeFi - DeFi stands for decentralized finance, representing a new wave of blockchain applications that offer innovative solutions to conventional financial services.  
Ricardian contracts - Ricardian contracts are legally binding agreements designed to be both human-readable and machine-readable.  

Double-spending is  where the sender spends the same money at more than one place for obtaining services or goods from multiple vendors.  



Public Key Cryptography, also called asymmetric cryptography uses a pair of keys: a public key and a private key. Public key is used for encryption while private key is used for description.  
Core Functions of Public Key Cryptography:  
•	Authentication: Ensures that the sender of a message is genuine.  
•	Message Privacy (Encryption/Decryption): Ensures that only the intended recipient can read the message.  

A hash function maps the data of any arbitrary size to data of fixed size. Hash is considered unique for the contents of the data. If the data is changed slightly, the hash value will change significantly.  

When a trnsaction is done the transaction is broadcasted to the entire network not just between the receiver snd sender.  
Miners (special nodes) gather multiple pending transactions from the network into a temporary block and combine transactions into a single block. 
The process of finding the right Nonce and hash is called mining.  
The first miner to find a valid solution broadcasts the new block to the network, and that block becomes the latest in the chain.  

Proof of Work (PoW) is a method used in blockchains like Bitcoin to make sure transactions are secure and blocks are added fairly to the chain.  
Each block includes a special number called a Nonce. The goal is to find a Nonce that, when combined with the block’s data and run through a hash function, produces a hash value that meets a specific requirement

Solidity:  
Various datatypes: Arrays, struct, unsigned integer, string.  
Declaring, defining and calling functions, returning values in function.  
Difference between private, public, external and internal functions.  
Smart contract inheritance allows developers to create new smart contracts based on existing ones, reusing code and functionality.  
Events are a way for contract to communicate to the frontend of the app.  
A mapping is essentially a key-value store for storing and looking up data.  
 To communicate to another contract on the blockchain that we don't own, first we need to define an interface.  

# SoC End Term Report  
To create a certifate verification dapp, we follow these steps. We create a contract in that we define a struct that has all the important information regarding the certificate. Now we use mapping to store certificates named certificates. Every certificate is indexed with unique identifier. An event is emitted(certificateGenerated) after every certificate generation, frontend apps or dApps can listen to this to know when a certificate is issued. Then we write a function(generateCertificate) to generate a certificate, it checks if a certificate with the given ID already exists and, if not, creates a new certificate and stores it in the mapping. It also emits the certificateGenerated event. Then we write a function (getCertificate), it retrives the details it returns the information associated with the certificate, it also checks if certifiacte with the given id exists or not. We write a function to check if certificate with given id exists, by checking the length of the IPFS hash associated with it. If the length is non-zero, the certificate is considered verified.  

Metamask - MetaMask allows users to configure their wallet for the Sepolia network. This involves holding and managing Sepolia testnet ETH, which can be obtained for free from testnet faucets. These funds are strictly for testing and have no real-world value. During contract deployment or function execution, MetaMask presents a confirmation popup for the user to review and sign the transaction. Once approved, the signed transaction is broadcasted to the Sepolia network for inclusion in a block.  

After deployment of our contract on testnet we can verify it using etherscan, this can be done by using a plugin on remix. then writing api key in the etherscan access token in settings.
