**The Interplanetary File System — a New Internet Protocol, Designed to Upgrade the Web and Maybe Even Replace HTTP**

The Hypertext Transfer Protocol (HTTP) has unified the entire world into a single global information protocol, standardizing how we distribute and present information to eachother. 

HTTP has achieved many things, it's usefulness as a foundation for the distribution and persistence of the sum of human knowledge. The way HTTP distributes content is fundamentally flawed, and no amount of performance tuneups or forcing broken CA SSL or whatever is going to fix that. 

Apart from this, today's internet has lots of downsides. 
- Increase bandwidth cost as user downloads a file from a single computer at a time. 
- It relays on centralized servers. 
- HTTP is great for loading websites but **not designed to transfer a large amount of data**.


# Storing Files on InterPlanetary File System 

Rocket.Chat enables integration with InterPlanetary File System (IPFS) as data storage.
InterPlanetary File System (IPFS) is a protocol and network designed to create a content-addressable, peer-to-peer method of storing and sharing hypermedia in a distributed file system. IPFS was initially designed by Juan Benet and is now an open-source project developed with help from the community.

It helps in storing the file on the decentralized data storage network. 
Files stored on the IPFS network can be accessed on any device using your login details.

# About

## Storing Files
- Like any other storage provider, whenever a new file uploaded on the Rocket.chat, the stored file get encrypted by using the provided password. It uses AES encryption to encrypt the data. 
- The encrypted file is stored on the IPFS network. IPFS use **Distributed Hash Tables**, it stores the information as key/value pairs. 
- Using the DHT, data is spread across a network of computers, and efficiently coordinated to enable efficient access and lookup between nodes. It also provides fault tolerance and scalability.
- IPFS network provides a key (HASH), that uniquely identifies the stored file on the IPFS network. 

## Retrieving Files
- When we add a file on the IPFS network, it provides a **key** that help in retrieving the file from the IPFS network. 
- By providing the *key* and the password we can retrieve the files or the information stored on the IPFS network. 

# Need for Encryption 
- IPFS is a public network, where anyone can add and view the stored data, which require encrypting the data before storing it on IPFS network, as the stored data is been encrypted some password, only authorized user can decrypt it. 

# Using IPFS in Rocket.chat 

## Registration 

A user needs to register on the Rocket.Chat [Register](https://github.com/RocketChat/docs/tree/master/user-guides/registration)
After registration. 

Once you are registered, It requires login details to [Log in](https://github.com/RocketChat/docs/tree/master/user-guides/login) in Rocket.chat.

## Adding files on InterPlanetary File System 

Whenever we upload a file on the rocket.chat server we can add the file to the IPFS network. 
Uploaded file stores on the IPFS, network and can uniquely identify by using the **IPFS Hash**
IPFS is a public network, the stored file can be accessed by using any IPFS enabled application. 
Rocket.chat use encryption so that the stored file can only be accessible by the authorized user and protects privacy.

Storing file on the IPFS network require: 

- File (that to be stored)
- A strong password (help in encrypting the file, that make your private file accessible to only authorized user)

Whenever we store a file it gets encrypted using your password and stored on the network.
When you retrieve that file it required the password (*To decrypt the file*) that used while adding the file on the IPFS network. 

# Developer guide 

Enabling IPFS in rocket.chat requires an interaction with the IPFS network, for that we can use 
- IPFS Daemon 
- Using infura (It provide a secure and reliable access to the IPFS gateways)

Communication with IPFS network can be done by using package [IPFS mini](https://www.npmjs.com/package/ipfs-mini)


# Work in progress 

- Managing a user directory on the IPFS network, that can add files and manage them. 
- Enabling the secure private key/public key encryption so that files can be shared for specific duration. 
- Managing the version history
