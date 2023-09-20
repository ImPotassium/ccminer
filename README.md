# CCminer for Termux

Based on: https://github.com/Oink70/CCminer-ARM-optimized

Install latest arm64-v8a Termux: https://github.com/termux/termux-app/releases

Proceed with installation and compilation:

```
pkg update -y && pkg upgrade -y
pkg install libjansson build-essential clang binutils git -y
cp /data/data/com.termux/files/usr/include/linux/sysctl.h /data/data/com.termux/files/usr/include/sys
git clone https://github.com/Darktron/ccminer.git
cd ccminer
chmod +x build.sh configure.sh autogen.sh start.sh
CXX=clang++ CC=clang ./build.sh
```

Change your pools, address, and miner name with: `nano config.json`

Run the miner with: `~/ccminer/start.sh`
