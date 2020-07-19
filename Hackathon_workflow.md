*Hi guys, here we are in the middle of week2 of this hackathon, and we have another 20 days to bring our idea out.*
*In this hackathon, we'll make a more feasible plan on the technical side to make sure we will get practical deliverables under limited time and engineering force.*
*This documents would be a functionality specification.*

#### Introduction
Ethcribe is a decentralized pay-per-view media release platform built on Ethereum and Filecoin. Ethcribe is a set of smart-contracts in the backend, it serves the frontend to achieve certain functionality. In this hackathon, we may just copy the form of THE Block website, and replace it's account system into our system as a final demo.

#### How it works
There are two types of character involved in this dapp, **the publisher** and **the reader**.
- The publisher should be able to upload their posts(say it's in PDF form) on the website, and this file will be encrypted and stored in the Filecoin(IPFS).
- The publisher could set a price for whom want to view his post. The price would serve as a parameter in the purchase smart-contract.
- The reader will choose one posts to buy, and the website tells the reader to login with ethereum account and pay a certain amount of ether to the purchase smart-contract.
- The reader now could open the post and get the content.

#### Technical details
1. Use a whitelist. When someone pays in the smart-contract, the smart-contract will add its address into the whitelist.
2. The encryption/decryption is different to ethsign which use PGP decrypt the file, because the file is published, and the payer for the post has no motivation to keep this PGP key secret. So here we will use a more complicated cryptography function such as IBE to achieve one key encryption, multi-keys decryption function.
3. Use the erc-1155 standard nft. Compared to use a whitelist to manage who has paid and has the accessibility to the post, nft is a more nimble way, one can transfer the accessibility. But in this way, we must make sure that once someone sent its nft to another guy, he cannot access the post any more, which means in this case we must use a one-time-key.
4. One-time-key could be a key related to the block height, or use the ethotp(https://www.npmjs.com/package/ethotp).
I personally think we have a lot of work in cryptography here, I'll keep digging more information.

#### Time line
###### Jack and Can
Week2: 
- Discussion on the architecture, settle the SRS
- Deploy related environment


Week3: 
- Development on the smart-contract
- Copy the website frontend from the block
- Get familiar with the Filecoin


Week4:
- finish the demo
###### Xin and Potter
Week2: 
- Discussion on the architecture
- Start to prepare the logo, picture and other things need to be shown in the demo


Week3:
- Prepare a deck and finish other paperwork


Week4:
- Video demo presentation



