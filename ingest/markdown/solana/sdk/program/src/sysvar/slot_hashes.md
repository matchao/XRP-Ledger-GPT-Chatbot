[View code on GitHub](https://github.com/solana-labs/solana/blob/master/sdk/program/src/sysvar/slot_hashes.rs)

The `slot_hashes.rs` file contains code for the _slot hashes sysvar_, which provides access to the most recent hashes of a slot's parent banks. This sysvar cannot be accessed on-chain because it is too large to process on-chain. However, it can be accessed off-chain through RPC. 

The file contains an implementation of the `Sysvar` trait for the `SlotHashes` type. The `size_of()` method is overridden to return a hard