# ts3-rtos

Umbrella for the TS3-RTOS project: a TeamSpeak 3 client for RTOS / cellular
handheld PoC radios. Two segments, pulled as submodules:

- `core/`   -> [ts3-core](https://github.com/cipheraenys/ts3-core) - portable C++17 client core (crypto, TS3 protocol, ports, tests)
- `python/` -> [ts3-quecpython](https://github.com/cipheraenys/ts3-quecpython) - QuecPython device layer (BQ280 / EC600M)

## Clone

```sh
git clone --recurse-submodules https://github.com/cipheraenys/ts3-rtos
# or, after a plain clone:
git submodule update --init --recursive
```

`core/` nests its own `third_party/` submodules (mbedtls, opus, ed25519), so
`--recursive` matters.
