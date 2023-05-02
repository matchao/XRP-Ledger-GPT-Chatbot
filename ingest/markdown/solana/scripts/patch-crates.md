[View code on GitHub](https://github.com/solana-labs/solana/blob/master/scripts/patch-crates.sh)

The `patch-crates.sh` script is used to update the dependencies of the Solana project. The script contains two functions: `update_solana_dependencies` and `patch_crates_io_solana`.

The `update_solana_dependencies` function takes two arguments: `project_root` and `solana_ver`. The `project_root` argument is the root directory of the Solana project, and the `solana_ver` argument is the version of Solana to update the dependencies to. The function first finds all `Cargo.toml` files in the project directory and its subdirectories. It then uses `sed` to replace the version of Solana dependencies in each `Cargo.t