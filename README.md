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
```
cargo install --locked cargo-deny
cargo install cargo-nextest --locked