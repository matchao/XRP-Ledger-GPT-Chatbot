[View code on GitHub](https://github.com/solana-labs/solana/blob/master/sdk/program/src/message/sanitized.rs)

The `sanitized.rs` file contains code for handling sanitized messages in the Solana project. It provides a way to create and manipulate sanitized messages, which are a cleaned and validated version of the original messages. The main purpose of this code is to ensure that the messages are safe to use and do not contain any invalid data or duplicate account keys.

There are two types of sanitized messages: `LegacyMessage` and `SanitizedMessage`. The `Lega