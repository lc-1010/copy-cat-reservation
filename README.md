# serve

simple-dns
cargo new / use template   to crate

```shell
touch Cargo.toml
touch deny.toml
touch  _typos.toml
touch .pre-commit-config.yaml
touch  build.yaml
mkdir .github/workflows
git init
pre-commit install
```
## grpc - crate
cargo new abi --lib
## reservation
cargo new reservation --lib

```shell
.
├── Cargo.toml
├── README.md
├── _typos.toml
├── abi
│   ├── Cargo.toml
│   └── src
│       └── lib.rs
├── deny.toml
├── reservation
│   ├── Cargo.toml
│   └── src
│       └── lib.rs
├── service
│   ├── Cargo.toml
│   └── src
│       └── main.rs
└── viesion.drawio.png
```

## rename service cargo.toml

```shell
 cargo build
   Compiling reservation v0.1.0 (/Developer/rustPL/livecode/reservation)
   Compiling abi v0.1.0 (/Developer/rustPL/livecode/abi)
   Compiling copy-reservation-service v0.1.0 (/Developer/rustPL/livecode/service)
    Finished dev [unoptimized + debuginfo] target(s) in 7.62s

 cargo install --locked cargo-deny
cargo install cargo-nextest --locked

```
git commit -a
```
git commit -a
Check for byte-order marker..............................................Passed
Check for case conflicts.................................................Passed
Check for merge conflicts................................................Passed
Check for broken symlinks............................(no files to check)Skipped
Check Yaml...............................................................Passed
Fix End of Files.........................................................Passed
Mixed line ending........................................................Passed
Trim Trailing Whitespace.................................................Passed
black................................................(no files to check)Skipped
typos....................................................................Passed
cargo fmt................................................................Passed
cargo deny check.........................................................Passed
cargo check..............................................................Passed
cargo clippy.............................................................Passed
cargo test...............................................................Passed
[master (root-commit) 66ec34a] init
```
报错 因为没有安装cargo 包
删除target 后
--------------------
## rfc
