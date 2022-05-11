

```

### Build

Once you have prepared your local development environment, you can build the node template. Use this
command to build the [Wasm](https://substrate.dev/docs/en/knowledgebase/advanced/executor#wasm-execution)
and [native](https://substrate.dev/docs/en/knowledgebase/advanced/executor#native-execution) code:

```bash
cargo build --release
```


[The Substrate Playground](https://playground-staging.substrate.dev/?deploy=node-template) is an
online development environment that allows you to take advantage of a pre-configured container
with pre-compiled build artifacts :woman_cartwheeling:

## Run

### Single Node Development Chain

Purge any existing developer chain state:

```bash
./target/release/node-template purge-chain --dev
```

Start a development chain with:

```bash
./target/release/node-template --dev
```

Detailed logs may be shown by running the node with the following environment variables set:
`RUST_LOG=debug RUST_BACKTRACE=1 cargo run -- --dev`.

### Multi-Node Local Testnet

If you want to see the multi-node consensus algorithm in action, refer to
[our Start a Private Network tutorial](https://substrate.dev/docs/en/tutorials/start-a-private-network/).

