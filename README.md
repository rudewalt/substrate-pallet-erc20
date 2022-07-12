# Implementation of ERC-20 functionality in Substrate

## Node

Build
```bash
cargo build --release
```

Test
```bash
cargo test
```

Run dev chain
```bash
./target/release/node --dev
```

## Benchmarking
Build
```bash
cargo build --release --features runtime-benchmarks
```

Run
```bash
./target/release/node benchmark pallet --chain=dev --execution=wasm --wasm-execution=compiled --pallet=pallet_erc20 --extrinsic=* --steps=20 --repeat=50 --output=./runtime/src/weights/pallet_erc20
```