# Storing Files on InterPlanetary File System 

Rocket.Chat enable integration with InterPlanetary File System (IPFS) as data storage.
InterPlanetary File System (IPFS) is a protocol and network designed to create a content-addressable, peer-to-peer method of storing and sharing hypermedia in a distributed file system. IPFS was initially designed by Juan Benet, and is now an open-source project developed with help from the community.

It help in storing the file on the decentralized data storage network. 
File stored on the IPFS network can be accessable on any device using your login details.

## Registration 

A user need to be register on the Rocket.Chat [Register](https://github.com/RocketChat/docs/tree/master/user-guides/registration)
After registration. 

Once you are register, It require login details to [Login](https://github.com/RocketChat/docs/tree/master/user-guides/login) in Rocket.chat .

## Adding files on InterPlanetary File System 

Whenever we upload a file on the rocket.chat server we can add the file to the IPFS network. 
Uploaded file stores on the IPFS, network and can uniquely identified by using the **IPFS Hash**
IPFS is a public network, the stored file can be access by using any IPFS enabled application. 
Rocket.chat use encryption so that the stored file can only be accessable by authorize user and protact privacy.

Storing file on the IPFS network require: 

- File (that to be stored)
- A strong password (help in encrypting file, that make your private file accessible to only authorize user)

Whenever we store a file it get encrypted using your password and stored on the network.
When you retrieve that file it required the password (*To decrypt the file*) that used while adding file on the IPFS network. 




