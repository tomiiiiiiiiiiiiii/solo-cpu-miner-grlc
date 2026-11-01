# GRLC CPU Miner Solo

An easy-to-use CPU miner for Garlicoin (GRLC) on Windows 64-bit.

Mine Garlicoin solo using the [GRLC.eu mining node](https://grlc.eu/miner), without running your own Garlicoin Core node or synchronizing the blockchain.

## Download

**[Download the latest release](https://github.com/tomiiiiiiiiiiiiii/solo-cpu-miner-grlc/releases/latest)**

## Getting started

1. Download and extract the ZIP archive.
2. Open `config.txt` and enter your GRLC wallet address and mining settings.
3. Run the executable compatible with your CPU:

   - `cpuminer-allium-avx2.exe`: Newer Intel and AMD processors supporting AVX2 and AES-NI.
   - `cpuminer-allium-sse2.exe`: Older 64-bit Intel and AMD processors supporting SSE2.

Keep the included DLL files in the same folder as the miner.

## Solo mining

The included configuration is intended for solo mining through the [GRLC.eu mining node](https://grlc.eu/miner). You do not need to run your own Garlicoin Core node.

In solo mode, you receive a block reward only when your miner successfully finds a block. Rewards are not guaranteed and depend on your hashrate and network difficulty.

## Pool mining

The included `cpuminer-allium-avx2.exe` and `cpuminer-allium-sse2.exe` are not limited to solo mining. You can also run them directly from Command Prompt with a Stratum pool.

Example using the AVX2 version:

```bat
cpuminer-allium-avx2.exe -a allium -o stratum+tcp://POOL_HOST:PORT -u WALLET.WORKER -p x
```

Replace `POOL_HOST`, `PORT`, `WALLET` and `WORKER` with the settings required by your pool. For older CPUs, use `cpuminer-allium-sse2.exe` instead. Pool payouts depend on the pool's rules.

## Based on cpuminer-opt-allium

This miner is based on **[cpuminer-opt-allium](https://github.com/tomiiiiiiiiiiiiii/cpuminer-opt-allium)**, an optimized CPU miner with support for Garlicoin's Allium proof-of-work algorithm.

## Mining node

https://grlc.eu/miner
