---
description: Ship a true NFT Marketplace on Celo - Part 1
---

# NFT - Contract

We've all heard of OpenSea, and maybe even of other marketplaces such as LooksRare. These platforms allow users to buy and sell all sorts of NFTs on their platforms, bringing a decentralized market to these digital mediums.

In this level, we will be building **OUR OWN** NFT marketplace, similar to OpenSea, completely from scratch on Celo!

We will use a bunch of developer tools to make this possible, and this is going to be an amazing level!

* Hardhat
* NextJS (React)
* Celo
* The Graph
* Rainbowkit
* Wagmi
* Ethers.js
* Metamask / Alfajores Wallet

This level will also help solidify your understanding of **events** on the blockchain, as once we get around to building the frontend, indexing events through The Graph will become extremely important.

For developers who are new to the Wagmi space, things might get a bit tough, but bear with us. After this course, you will be pro Wagmi/Rainbowkit developer!

We will divide this lesson into three parts - Smart contracts, Subgraph, and Frontend.

### 🤩 Final Output

This is what we will be building, by the end of this lesson series:

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>



<figure><img src=".gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### Smart Contracts

Let's create a new directory on your computer, and initialize a Git repo there (which will house all our code) by running the following command :

```
mkdir celo-nft-marketplace
cd celo-nft-marketplace
git init
```

Now, let's think about what we need in the NFT marketplace smart contract. We will create the following functions to allow for different actions:

1. `createListing`: Create a listing to put an NFT up for sale
2. `cancelListing`: Cancel a listing you previously created
3. `updateListing` Update a listing you previously created
4. `purchaseListing`: Purchase a listing from someone else

This is a minimalistic version of what goes on in a decentralized NFT marketplace, but it fits well for our purpose.

#### 👨‍🔬 Setting Up

Let's set up a new Hardhat project to write our smart contracts.

1. Open up a terminal, and create a folder for Hardhat within the directory you just created

```
cd celo-nft-marketplacemkdir hardhatcd hardhat
```

2. To set up the project, execute these commands

```
npm init --yesnpm install --save-dev hardhat
```

3. If you are on Windows, please do this extra step and install these libraries as well :)

```
npm install --save-dev @nomicfoundation/hardhat-toolbox @nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers ethers
```

4. Finally, run the following command and go through the interactive prompt

```
npx hardhat
```

* Select `Create a JavaScript project`
* Press enter for the already specified `Hardhat project root`
* Press enter for the question on `Do you want to add a .gitignore`
* If prompted, press enter for `Do you want to install this sample project's dependencies with npm (@nomiclabs/hardhat-waffle ethereum-waffle chai @nomiclabs/hardhat-ethers ethers)?`

We now have our Hardhat project ready to go!

5. Let's also install OpenZeppelin contracts library while we're here, as we will use `IERC721.sol` later

```
npm install @openzeppelin/contracts
```

### 🎨 Building Contract

Before we build our marketplace, we need to build a simple NFT contract so you actually have some NFTs on testnet you can test this out with. We will not go into too much detail for this, as by this point it should be fairly straightforward.

If you are not familiar with writing NFT contracts, check out the [NFT Collection tutorial in the Sophomore track](https://learnweb3.io/).

Open up the folder in your code editor, and create a new file under `hardhat/contracts` called `CeloNFT.sol`. We will use this file to write a simple NFT contract

```solidity
// SPDX-License-Identifier: UNLICENSED
pragma solidity ^0.8.17;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";

contract celoNFT is ERC721 {
    constructor() ERC721("CeloNFT","cNFT"){
        // mint 5 NFTs to yourself
        for (uint i = 0; i < 5; i++) {
            _mint(msg.sender, i);
        }
    }

    // Hardcoded token URI will return the same metadata
    // for each NFT
    function tokenURI(uint) public pure override returns (string memory) {
        return "ipfs://QmTy8w65yBXgyfG2ZBg5TrfB2hPjrDQH3RCQFJGkARStJb";
    }
}
```





