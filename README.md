# GRLC CPU Miner Solo

An easy-to-use CPU miner for Garlicoin (GRLC) on Windows 64-bit.

Mine Garlicoin solo using the [GRLC.eu mining node](https://grlc.eu/miner), without running your own Garlicoin Core node or synchronizing the blockchain.

## Download

**[Download the latest release](https://github.com/tomiiiiiiiiiiiiii/solo-cpu-miner-grlc/releases/download/v.1.1/solo-grlc-cpu-miner_v1.1.zip)**

## Getting started: solo mining

1. Download and extract the ZIP archive.
2. Open `config.txt` and enter your GRLC wallet address and mining settings.
3. Run **`miner_grlc.exe`** to start solo mining through the [GRLC.eu mining node](https://grlc.eu/miner).

The package keeps the CPU miner executables and required DLL libraries in the `bin` directory. Keep `bin`, `etc` and the other included files in their original locations.

## Solo mining

**`miner_grlc.exe` is the launcher for the included solo mining setup.** You do not need to run your own Garlicoin Core node.

In solo mode, you receive a block reward only when your miner successfully finds a block. Rewards are not guaranteed and depend on your hashrate and network difficulty.

## Pool mining

For pool mining, run a CPU miner executable from the `bin` directory directly from Command Prompt with your pool's Stratum settings, instead of using the `miner_grlc.exe` solo launcher.

- `bin\cpuminer-allium-avx2.exe`: Newer Intel and AMD processors supporting AVX2 and AES-NI.
- `bin\cpuminer-allium-sse2.exe`: Older 64-bit Intel and AMD processors supporting SSE2.

From Command Prompt in the extracted package's main directory, for example:

```bat
bin\cpuminer-allium-avx2.exe -a allium -o stratum+tcp://POOL_HOST:PORT -u WALLET.WORKER -p x
```

Replace `POOL_HOST`, `PORT`, `WALLET` and `WORKER` with the settings required by your pool. For older CPUs, use `bin\cpuminer-allium-sse2.exe` instead. Keep the DLL files alongside the miner executables in `bin`. Pool payouts depend on the pool's rules.

## Based on cpuminer-opt-allium

This miner is based on **[cpuminer-opt-allium](https://github.com/tomiiiiiiiiiiiiii/cpuminer-opt-allium)**, an optimized CPU miner with support for Garlicoin's Allium proof-of-work algorithm.

## Mining node

https://grlc.eu/miner
