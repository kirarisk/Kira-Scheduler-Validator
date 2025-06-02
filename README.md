<p align="center">
  <a href="https://solana.com">
    <img alt="Solana" src="https://i.imgur.com/0vfIMHo.png" width="250" />
  </a>
</p>

# Kira-Scheduler-Validator

A fork of [Agave](https://github.com/anza-xyz/agave) (Solana's validator client) featuring the **KiraScheduler** - a custom transaction scheduler implementation.

## 🚀 What's New: KiraScheduler

The **KiraScheduler** is a new transaction scheduling algorithm that joins the existing scheduler options in Solana's banking stage.



### KiraScheduler Details
**TBA** - Implementation details and performance characteristics will be documented here.

## 📋 Usage

### Running the Validator with KiraScheduler

```bash

```



## 🏁 Benchmarking

### Run All Scheduler Benchmarks

```bash
$ cargo +nightly bench --bench scheduler
```



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


## 📄 License

Apache-2.0 license (same as original Agave project)

## 🔗 Links

- **Original Agave Repository**: [anza-xyz/agave](https://github.com/anza-xyz/agave)
- **Solana Documentation**: [docs.solanalabs.com](https://docs.solanalabs.com)

---

> **Note**: This is a research fork. For production use, ensure thorough testing in devnet/testnet environments first.
