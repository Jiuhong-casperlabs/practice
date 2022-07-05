`make build-contract` -> worked


`make clippy` -> errors
```
jh@DESKTOP-RMF966H:~/learning/rust/contracts/dictionary$ make clippy
cd contract && cargo clippy --all-targets -- -D warnings
    Checking dictionary v0.1.0 (/home/jh/learning/rust/contracts/dictionary/contract)
error: duplicate lang item in crate `std` (which `test` depends on): `panic_impl`.
  |
  = note: the lang item is first defined in crate `casper_contract` (which `dictionary` depends on)
  = note: first definition in `casper_contract` loaded from /home/jh/learning/rust/contracts/dictionary/contract/target/wasm32-unknown-unknown/debug/deps/libcasper_contract-731f552d0f1529fc.rmeta
  = note: second definition in `std` loaded from /home/jh/.rustup/toolchains/nightly-2022-01-13-x86_64-unknown-linux-gnu/lib/rustlib/wasm32-unknown-unknown/lib/libstd-8431e8f0a2dad879.rlib

error: duplicate lang item in crate `std` (which `test` depends on): `oom`.
  |
  = note: the lang item is first defined in crate `casper_contract` (which `dictionary` depends on)
  = note: first definition in `casper_contract` loaded from /home/jh/learning/rust/contracts/dictionary/contract/target/wasm32-unknown-unknown/debug/deps/libcasper_contract-731f552d0f1529fc.rmeta
  = note: second definition in `std` loaded from /home/jh/.rustup/toolchains/nightly-2022-01-13-x86_64-unknown-linux-gnu/lib/rustlib/wasm32-unknown-unknown/lib/libstd-8431e8f0a2dad879.rlib

error: could not compile `dictionary` due to 2 previous errors
make: *** [Makefile:14: clippy] Error 101
```
