# @Plusid/typescript-peers

<p align="center">
    <img src="https://raw.githubusercontent.com/ARKEcosystem/peers/master/banner.png" />
</p>

## Installation

```bash
yarn add @Plusid/typescript-peers
```

## Usage

### Peers via GitHub

```ts
import { PeerDiscovery } from "@Plusid/typescript-peers";

peerDiscovery = await PeerDiscovery.new({
	networkOrHost: "devnet"
})

peers = peerDiscovery
	.withVersion(">=2.4.0-next.0")
	.withLatency(300)
	.sortBy("latency")
	.findPeersWithPlugin("core-api");
```

### Peers via Relay

```ts
import { PeerDiscovery } from "@Plusid/typescript-peers";

peerDiscovery = await PeerDiscovery.new({
	networkOrHost: "",
})

peers = peerDiscovery
	.withVersion(">=2.4.0-next.0")
	.withLatency(300)
	.sortBy("latency")
	.findPeersWithPlugin("core-api");
```

## Testing

```bash
yarn test
```

## Security

If you discover a security vulnerability within this package, please send an e-mail to security@infinitysolutions.io. All security vulnerabilities will be promptly addressed.

## Credits

This project exists thanks to all the people who [contribute](../../contributors).

## License

[MIT](LICENSE) © [Infinity](https://infinitysolutions.io)
