[View code on GitHub](https://github.com/solana-labs/solana/tree/master/na/core)

The `autodoc/solana/core` folder contains essential components and benchmarking modules for the Solana project, a high-performance blockchain platform. The folder is organized into two subfolders: `benches` and `src`.

### benches

The `benches` folder contains benchmarking modules that measure the performance of various components and processes in the Solana project. These benchmarks help developers identify bottlenecks and optimize the system. Some examples of benchmarking modules include:

- `banking_stage.rs`: Benchmarks the `BankingStage`, which processes transactions and manages account states. Functions like `bench_consume_buffered` measure packet buffering performance, while `bench_banking_stage_multi_accounts` tests transaction processing involving multiple accounts.

```rust
// Example usage of bench_consume_buffered
bench_consume_buffered(&mut banking_stage, &bank, &poh_recorder