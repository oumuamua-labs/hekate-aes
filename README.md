# hekate-aes

AES-128 / AES-256 AIR chiplet for the [Hekate](https://github.com/oumuamua-labs/hekate) ZK proving system.

Implements FIPS 197 round function (SubBytes, ShiftRows, MixColumns, AddRoundKey) as a binary-field AIR with an
S-box ROM chiplet for the GF(2^8) inversion. Round-AIR trace is wired to the CPU AIR via LogUp bus.

```
Per-block proving cost (Apple M3 Max, 31,250 blocks per run):
  AES-128: ~69 µs/block, 772 MB peak, 3,405 KiB proof
  AES-256: ~73 µs/block, 1,005 MB peak, 3,706 KiB proof
```

## License

Apache-2.0. See [LICENSE](LICENSE) and [NOTICE](NOTICE).