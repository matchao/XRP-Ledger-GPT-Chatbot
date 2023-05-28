[View code on GitHub](https://github.com/solana-labs/solana/blob/master/transaction-status/src/token_balances.rs)

The `token_balances.rs` file in the `solana/transaction-status/src` directory contains code that defines a `TransactionTokenBalancesSet` struct and a `TransactionTokenBalances` type alias. The purpose of this code is to represent the token balances of a transaction before and after it is executed.

The `TransactionTokenBalances` type alias is defined as a vector of vectors of `TransactionTokenBalance` structs. Each inner vector represents the token balances of a single account, and each `TransactionTokenBalance` struct contains information about a speci