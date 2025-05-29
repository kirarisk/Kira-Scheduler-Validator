<p align="center">
  <a href="https://solana.com">
    <img alt="Solana" src="https://i.imgur.com/0vfIMHo.png" width="250" />
  </a>
</p>

# Kira-Scheduler-Validator

A fork of [Agave](https://github.com/anza-xyz/agave) (Solana's validator client) featuring the **KiraScheduler** - a custom transaction scheduler implementation.

## 🚀 What's New: KiraScheduler

The **KiraScheduler** is a new transaction scheduling algorithm that joins the existing scheduler options in Solana's banking stage.

### Available Schedulers
- **Central Scheduler** (`central-scheduler`) - Priority graph-based scheduler (default)
- **Greedy Scheduler** (`central-scheduler-greedy`) - Fast greedy scheduling algorithm  
- **🆕 Kira Scheduler** (`kira-scheduler`) - Custom scheduler implementation

### KiraScheduler Details
**TBA** - Implementation details and performance characteristics will be documented here.

## 📋 Usage

### Running the Validator with KiraScheduler

```bash
# Using KiraScheduler
$ agave-validator --block-production-method kira-scheduler [other-options...]

# Other available schedulers:
$ agave-validator --block-production-method central-scheduler [other-options...]
$ agave-validator --block-production-method central-scheduler-greedy [other-options...]
```

### View Available Options

```bash
$ agave-validator --help | grep -A 10 "block-production-method"
```

## 🏁 Benchmarking

### Run All Scheduler Benchmarks

```bash
$ cargo +nightly bench --bench scheduler
```

### Run Specific Scheduler Benchmarks

```bash
# KiraScheduler only
$ cargo +nightly bench --bench scheduler -- kira_scheduler

# Compare all schedulers
$ cargo +nightly bench --bench scheduler -- "scheduler"
```

The benchmark suite tests all schedulers across various scenarios with different transaction counts, instruction counts, and conflict types.

## 🔧 Building

```bash
$ git clone https://github.com/kirarisk/Kira-Scheduler-Validator.git
$ cd Kira-Scheduler-Validator
$ cargo build --release
```

## 🧪 Testing

```bash
# Run all tests
$ cargo test

# Test scheduler components
$ cargo test --package solana-core scheduler
```

## 📁 Implementation Files

- **KiraScheduler**: `core/src/banking_stage/transaction_scheduler/kira_scheduler.rs`
- **Integration**: `core/src/banking_stage.rs`
- **Benchmarks**: `core/benches/scheduler.rs`

## 📄 License

Apache-2.0 license (same as original Agave project)

## 🔗 Links

- **Original Agave Repository**: [anza-xyz/agave](https://github.com/anza-xyz/agave)
- **Solana Documentation**: [docs.solanalabs.com](https://docs.solanalabs.com)

---

> **Note**: This is a research fork. For production use, ensure thorough testing in devnet/testnet environments first.
