# cargo-near-new-project-name

cargo-near-new-project-description

## Quickstart Guide

You can start coding on the NEAR Rust stack in less than a minute, thanks to [NEAR Devcontainers](https://github.com/near/near-devcontainers). How?

1. Click **Use this template** > **Create a new repository**

<img width="750" alt="Create a new repository" src="https://github.com/njelich/cargo-near-new-project-template/assets/12912633/d59d89f1-8bc4-42f1-8e0d-842521d87768">

2. In your newly created repo, click **Code** > **Codespaces** > **Create codespace on main**

<img width="750" alt="Create Codespace" src="https://github.com/njelich/cargo-near-new-project-template/assets/12912633/352566cf-2eca-4d42-8232-6136ea8ec9d3">

## Where to Get Started?

Start writing your contract logic in [src/lib.rs](src/lib.rs) and integration tests in [tests/test_basics.rs](tests/test_basics.rs).

## How to Build Locally?

Install [`cargo-near`](https://github.com/near/cargo-near) and run:

```bash
cargo near build non-reproducible-wasm
```

## How to Test Locally?

```bash
cargo test
```

## How to Deploy?

Deployment is automated with GitHub Actions CI/CD pipeline.
To deploy manually, install [`cargo-near`](https://github.com/near/cargo-near) and run:

```bash
cargo near deploy build-non-reproducible-wasm <account-id>
```

## Updating rustup

Currently 1.86.0 is maximum version, supported by Nearcore for running compiled wasm contracts.

So, updating version to a newer toolchain is not recommended. 

If, for whaterver reason, one needs to update rust in Codespaces environment,

it's possible to set password in codespaces container:

```bash
sudo passwd $(whoami)
```

then, update `rustup` folder permissions 

```bash
sudo chown -R $(whoami):$(whoami) /usr/local/rustup
```

then maybe remove some `cargo-clippy` conflicting binary:
```bash
rm $CARGO_HOME/bin/cargo-clippy
```

and then run 

```bash
rustup update
```

to completion.


## Useful Links

- [cargo-near](https://github.com/near/cargo-near) - NEAR smart contract development toolkit for Rust
- [near CLI](https://near.cli.rs) - Iteract with NEAR blockchain from command line
- [NEAR Rust SDK Documentation](https://docs.near.org/sdk/rust/introduction)
- [NEAR Documentation](https://docs.near.org)
- [NEAR StackOverflow](https://stackoverflow.com/questions/tagged/nearprotocol)
- [NEAR Discord](https://near.chat)
- [NEAR Telegram Developers Community Group](https://t.me/neardev)
- NEAR DevHub: [Telegram](https://t.me/neardevhub), [Twitter](https://twitter.com/neardevhub)
