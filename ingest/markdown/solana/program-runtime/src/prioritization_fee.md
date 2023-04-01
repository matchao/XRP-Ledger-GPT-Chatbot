[View code on GitHub](https://github.com/solana-labs/solana/blob/master/program-runtime/src/prioritization_fee.rs)

The `prioritization_fee.rs` file contains code that calculates the prioritization fee for a given transaction. The prioritization fee is a fee paid by the transaction submitter to prioritize their transaction in the mempool. The higher the fee, the higher the priority of the transaction. 

The code defines a `PrioritizationFeeType` enum that can take two values: `ComputeUnitPrice` and `Deprecated`. The `ComputeUnitPrice` variant takes a `u64` value that represents the fee per compute unit, while the `Deprecated` variant takes a `u64` value that represents the total fee. The `Deprecated` variant is marked as deprecated and will be removed in the future.

The `PrioritizationFeeDetails` struct contains two fields: `fee` and `priority`. The `fee` field represents the total fee paid by the transaction submitter, while the `priority` field represents the priority of the transaction. 

The `PrioritizationFeeDetails` struct has a `new` method that takes a `PrioritizationFeeType` value and a `compute_unit_limit` value. The `compute_unit_limit` value represents the maximum number of compute units that the transaction can use. The `new` method calculates the `fee` and `priority` fields based on the `PrioritizationFeeType` value and the `compute_unit_limit` value. 

If the `PrioritizationFeeType` value is `ComputeUnitPrice`, the `fee` field is calculated by multiplying the `compute_unit_limit` value by the fee per compute unit and rounding up to the nearest lamport. The `priority` field is set to the fee per compute unit. 

If the `PrioritizationFeeType` value is `Deprecated`, the `fee` field is set to the total fee, and the `priority` field is calculated by dividing the fee by the `compute_unit_limit` value and rounding down to the nearest 