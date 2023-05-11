[View code on GitHub](https://github.com/solana-labs/solana/tree/master/na/sdk/macro/src)

The `autodoc/solana/sdk/macro/src` folder contains a Rust library that provides a set of procedural macros to simplify the handling of public keys and program IDs in the Solana project. These macros allow developers to easily declare and interact with public keys and program IDs in their code, reducing boilerplate and improving readability.

The main functionality is provided through the following macros:

- `pubkey`: Takes a base58 string representation of a public key and returns a `Pubkey` object. For example:

  ``