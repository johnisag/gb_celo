---
description: Ship a true NFT Marketplace on Celo - Part 3
---

# NFT - dApp

<figure><img src=".gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Finally it's time to build the part of our project folks can interact with!

Smart Contracts ✅ Deployment Scripts ✅ Subgraph ✅ Frontend ☑️

It's time to build our frontend now. As always, we will be using [Next.js](https://nextjs.org/) to do so.

### Website Development

#### 👨‍🔬 Setting Up

1.  Open up your terminal, and enter the `celo-nft-marketplace` directory

    ```
    cd celo-nft-marketplace
    ```
2.  Initialize a new Next.js app by running the following command

    ```
    npx create-next-app@latest frontend
    ```

We now have a fresh new Next.js project ready to go!

#### 😎 Git Good

The `create-next-app` tool also initializes a Git repo when it sets up the project. However, since our parent directory `celo-nft-marketplace` is already a Git repo, we don't want to keep the `frontend` folder as a separate Git repo to avoid having one Git repo inside another Git repo (Git submodules).

Run the following command in your terminal

```
# Linux / macOScd 
frontend
rm -rf .git

# Windowscd 
frontend
rmdir /s /q .git
```

#### 🥅 The Goal

