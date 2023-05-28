[View code on GitHub](https://github.com/solana-labs/solana/blob/master/transaction-status/src/parse_system.rs)

The `parse_system` function in the `solana/transaction-status/src/parse_system.rs` file is responsible for parsing system instructions in the Solana blockchain. It takes a `CompiledInstruction` and `AccountKeys` as input and returns a `Result` containing a `ParsedInstructionEnum` or a `ParseInstructionError`.

The function first deserializes the instruction data into a `SystemInstruction` enum. It then checks if the maximum account index in the instruction is within the bounds of the account keys. If not, it returns an error.

Next, the function matches the `SystemInstruction` enum variant and processes each case accordingly. For each case, it checks the number of accounts involved in the instruction and constructs a `ParsedInstructionEnum` containing the instruction type and relevant information in JSON format. The information includes details such as source and destination accounts, lamports, space, owner, seed, and other relevant fields depending on the instruction type.

Some of the supported instruction types include:

- `createAccount`: Creates a new account with the specified lamports, space, and owner.
- `assign`: Assigns an owner to an account.
- `transfer`: Transfers lampo