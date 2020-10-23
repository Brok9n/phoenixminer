# Quick setup PhoenixMiner on Ubuntu with AMD


1. Do a fresh installation of Ubuntu 16.04

2. Download the latest AMD drivers and install


```
cd ~/Downloads

wget --referer http://support.amd.com/ https://www2.ati.com/drivers/linux/ubuntu/amdgpu-pro-17.50-511655.tar.xz

tar xvf amdgpu-pro-17.50-511655.tar.xz 

cd amdgpu-pro-17.50-511655/

sudo ./amdgpu-pro-install -y --opencl=legacy
```

Next we’ll install PhoenixMiner

cd ~/Downloads

wget https://github.com/Miners-dev/phoenixminer/releases/download/5.1c/PhoenixMiner_5.1c_Linux.zip

mkdir ~/Phoenix

cd ~/Phoenix

tar -xvpzf ~/Downloads/PhoenixMiner_5.1c_Linux.zip

chmod u+s PhoenixMiner
The command everyone recommends using looks something like this

~/Phoenix/PhoenixMiner -epool us2.ethermine.org:4444 -ewal <wallet>.<worker> -epsw x -mode 1 -tt 68 -allpools 1
What happened is we got an error about miner doesn’t have root acecss

ETH - Total Speed: 44.209 Mh/s, Total Shares: 13, Rejected: 0, Time: 00:22
ETH: GPU0 22.107 Mh/s, GPU1 22.102 Mh/s
Failed to set new fan speed, check if miner has root access!
Failed to set new fan speed, check if miner has root access!
Failed to set new fan speed, check if miner has root access!
Failed to set new fan speed, check if miner has root access!
ETH: 01/26/18-13:35:54 - New job from us2.ethermine.org:4444

With default setting the AMD Radeon RX570‘s do about 22 Mh/s, give it a week to make sure things are stable and we’ll tweak them up to hopefully around 30 Mh/s.  I’ll give you another post once we make those changes.

In the mean time, to get rid of that annoying error message, I just removed the -tt for now which is Target Temperature so PhoenixMiner stops trying to make calls to adjust fan speeds automatically.   However you really want to increase the fan speeds manually to keep the GPUs cooler. Check out this post, this is what I had done, near the bottom gives you the settings you’ll want to add to your miner.sh script to keep your RX570’s cool, Adjusting RX570 Fans Speed.