[View code on GitHub](https://github.com/solana-labs/solana/blob/master/sdk/bpf/c/inc/sol/inc/cpi.inc)

# Solana Cross-Program Invocation

The `cpi.inc` file contains the implementation of the Solana Cross-Program Invocation (CPI) API. The CPI API allows one Solana program to invoke another Solana program. This is useful when a program needs to perform an operation that requires the functionality of another program. 

The file defines several constants and data structures that are used by the CPI API. The `MAX_CPI_INSTRUCTION_DATA_LEN` constant defines the maximum size of the data that can be passed to a CPI instruction. The `MAX_CPI_INSTRUCTION_ACCOUNTS` constant defines the maximum number of accounts that can be passed to a CPI instruction. The `MAX_CPI_ACCOUNT_INFOS` constant defines the maximum number of account info structs that can be used in a single CPI invocation.

The `SolAccountMeta` struct defines the metadata for an account that is passed to a CPI instruction. It contains the account's public key, whether the account is