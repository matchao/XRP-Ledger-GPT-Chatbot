[View code on GitHub](https://github.com/solana-labs/solana/blob/master/sdk/program/src/program_stubs.rs)

The `program_stubs.rs` file contains implementations of syscalls used when `solana-program` is built for non-SBF targets. It defines a trait `SyscallStubs` that provides default implementations for various system calls. The default im