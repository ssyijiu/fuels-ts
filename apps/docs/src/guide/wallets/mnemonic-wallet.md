# Creating a wallet from mnemonic phrases

A mnemonic phrase is a cryptographically-generated sequence of words that's used to derive a private key. For instance: `"oblige salon price punch saddle immune slogan rare snap desert retire surprise";` would generate the address `0xf18b6446deb8135544ba60333e5b7522685cd2cf64aa4e4c75df725149850b65`.

In addition to that, we also support [Hierarchical Deterministic Wallets](https://www.ledger.com/academy/crypto/what-are-hierarchical-deterministic-hd-wallets) and [derivation paths](https://learnmeabitcoin.com/technical/derivation-paths). You may recognize the string `"m/44'/60'/0'/0/0"` from somewhere; that's a derivation path. In simple terms, it's a way to derive many wallets from a single root wallet.

The SDK gives you two wallets from mnemonic instantiation methods: one that takes a derivation path and one that uses the default derivation path, in case you don't want or don't need to configure that.

Here's how you can create wallets with both mnemonic phrases and derivation paths:

<<< @/../../../packages/account/src/wallet-manager/wallet-manager.test.ts#wallet-manager-mnemonic{ts:line-numbers}
