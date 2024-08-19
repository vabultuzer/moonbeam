# Moonbeam Node on Akash
[Moonbeam](https://moonbeam.network/) is a smart contract platform that provides a seamless, Ethereum-compatible environment for developers to build cross-chain dApps on Polkadot.

Running a full node on a Moonbeam-based network allows you to connect to the network, sync with a bootnode, obtain local access to RPC endpoints, author blocks on the parachain, and more.

## Getting Started
Deploy Moonbeam Node with deploy.yaml file on [Akash Console](https://console.akash.network/) or [CLI](https://akash.network/docs/deployments/akash-cli/overview/).

Specify the network and node name in your deployment:
- --chain - specifies the chain specification to use. It can be a predefined chainspec such as moonbeam, moonriver, or alphanet.
- --name - specifies a human-readable name for the node, which can be seen on [telemetry](https://telemetry.polkadot.io/), if enabled.

More detail about flags in [Moonbeam Docs](https://docs.moonbeam.network/node-operators/networks/run-a-node/flags/).

## JSON-RPC APIs
Moonbeam Node supports standard Ethereum RPC methods. More details in [Moonbeam Docs](https://docs.moonbeam.network/builders/ethereum/json-rpc/eth-rpc/).
Example RPC request:
```
curl -H "Content-Type: application/json" -X POST --data '{
  "jsonrpc": "2.0",
  "id": "1",
  "method": "eth_chainId",
  "params": []
}' http://localhost:9944/
```
Where http://localhost:9944/ is forwarded port from your deployment.

## Dockerfile
Dockerfile on [GitHub](https://github.com/moonbeam-foundation/moonbeam/blob/master/docker/moonbeam.Dockerfile). Image on [Docker Hub](https://hub.docker.com/layers/moonbeamfoundation/moonbeam/v0.39.0/images/sha256-c68f37d89986ea83d6fe9a392a849b0870547bac07d1d1f806f07d55311a147b?context=explore).
