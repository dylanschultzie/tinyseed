# TerranSeed

## TerranSeed is a fork of [TinySeed](https://github.com/notional-labs/tinyseed), which is a fork of Binary Holding's Tenderseed, which is a fork of Polychain's Tenderseed

This tool runs a seed node for any tendermint based blockchain (i.e. Terra, Cosmos, Akash, etc, thanks to TinySeed), crawls the network and generates a map with the geolocalisation of the peers.
It is used to pinpoint centralization of network in common infrastructure hosts like AWS, GCP etc.

###Configuration

```bash
git clone https://github.com/Terran-Stakers/terranseed
go mod tidy
go install .
tenderseed
```

Then you'll become a seed node on Osmosis-1. Let's do Cosmoshub-4, shall we? We've made Osmosis zeroconf, but hey this
thing here reads 2 env vars!

```bash
export ID=cosmoshub-4
export SEEDS=bf8328b66dceb4987e5cd94430af66045e59899f@public-seed.cosmos.vitwit.com:26656,cfd785a4224c7940e9a10f6c1ab24c343e923bec@164.68.107.188:26656,d72b3011ed46d783e369fdf8ae2055b99a1e5074@173.249.50.25:26656,ba3bacc714817218562f743178228f23678b2873@public-seed-node.cosmoshub.certus.one:26656,3c7cad4154967a294b3ba1cc752e40e8779640ad@84.201.128.115:26656,366ac852255c3ac8de17e11ae9ec814b8c68bddb@51.15.94.196:26656
terranseed
```

## Docker

```bash
docker run -e ID=cosmoshub-4 -e SEEDS=bf8328b66dceb4987e5cd94430af66045e59899f@public-seed.cosmos.vitwit.com:26656,cfd785a4224c7940e9a10f6c1ab24c343e923bec@164.68.107.188:26656,d72b3011ed46d783e369fdf8ae2055b99a1e5074@173.249.50.25:26656,ba3bacc714817218562f743178228f23678b2873@public-seed-node.cosmoshub.certus.one:26656,3c7cad4154967a294b3ba1cc752e40e8779640ad@84.201.128.115:26656,366ac852255c3ac8de17e11ae9ec814b8c68bddb@51.15.94.196:26656 ghcr.io/notional-labs/tinyseed
```


## License

[Blue Oak Model License 1.0.0](https://blueoakcouncil.org/license/1.0.0)
