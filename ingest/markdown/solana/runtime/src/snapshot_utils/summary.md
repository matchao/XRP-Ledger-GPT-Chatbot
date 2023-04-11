[View code on GitHub](https://github.com/solana-labs/solana/tree/master/na/runtime/src/snapshot_utils)

The `snapshot_utils` folder in the Solana runtime contains a file named `archive_format.rs`, which is responsible for handling different archive formats used for snapshots in the Solana project. The primary component of this file is the `ArchiveFormat` enum, which represents the various archive formats supported by the project. These formats include `TarBzip2`, `TarGzip`, `TarZstd`, `TarLz4`, 