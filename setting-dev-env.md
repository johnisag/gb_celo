---
description: Celo Developer Environment
---

# Setting Dev Env

Since Celo is an EVM based chain, most of the development tooling used for Celo is the same as Ethereum. **We can continue to use Solidity** as our smart contracts programming language, and **also use Hardhat** to automate deployments for us. 🎉

### Wallets

The main differences between Celo and Ethereum development have to do with wallets. Remember, Celo is a mobile-first blockchain, with features such as their lightweight identity protocol and stablecoin support.

Typically the easiest option to get started developing is by adding a network to any compatible Ethereum wallet - for e.g. Metamask. But, since Metamask wasn't explicitly designed for Celo, it doesn't support all Celo-native features.

So if you want to use things like Phone Number to Wallet Address mapping and using stablecoins to pay gas for transactions, you're going to need a Celo mobile wallet.

<figure><img src=".gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

Therefore, for development purposes, if you want access to the full suite of what Celo has to offer, you should sign up for the official [Celo Developer Wallet](https://celo.org/developers/wallet). Alternatively, you can just add the Celo chain information to Metamask. While you can use it on the web, the full features are only available on mobile, so we recommend installing it on your Android or iOS device.

* NOTE: For iOS, you will also have to enroll your phone into Apple's Testflight program, used for testing apps. When you go to install the iOS app from the above link, it will walk you through how to do that.\


![](<.gitbook/assets/image (3).png>)



Once you have set up your wallet, it should look something like the above screenshot. Pull the sidebar from the left, and click on the `Supercharge` button to start linking your phone number with your wallet address. The app will guide you through the process, and can take a few minutes while it sets you up with everything.

By the end, you should have your phone number linked to your wallet. If you were unable to get any of the confirmation codes, try a bit later or try resending the codes.

### Testnets

The testnet that is used for development on Celo is called **Alfajores (Pronounced 'ahl-fah-hohres') Testnet**. We will be using this for all development.

If you are using the mobile wallet we mentioned above, the developer version of it is also designed for use with the Alfajores Testnet, and you cannot change networks. The mainnet version of the same wallet is called Valora Wallet, and can be found in the App Store/Play Store.

Before we proceed, let's get set up with some tokens to play around with.

Visit the [Celo Faucet](https://celo.org/developers/faucet), and input your wallet address there to request some tokens. This will send the CELO token, but also one of cUSD and cEUR each - the USD and EUR stablecoins.

### Conclusion

Great, now you have a Celo wallet and some funds on the Alfojores testnet to play with!

Move on to continue building on Celo, and learn more.
