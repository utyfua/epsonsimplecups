# epsonsimplecups
A simple CUPS driver for the Epson TM-T20 POS printer.
Epson provides a driver for this printer, but they only provide x86 and x64 linux binary builds instead of source. As a result, the driver can't be used on ARM systems, such as the Raspberry PI.

This is a very simple driver that provides buffered raster printing and paper cutting at end of page or end of job.

To compile this on a raspberry pi, you will first need to install two cups dev packages:
sudo apt-get install libcups2-dev
sudo apt-get install libcupsimage2-dev

## Install script(or just paste to console)

```
#!/bin/sh
# install Epson printer TM-88 / TM-20
sudo apt install libcups2-dev libcupsimage2-dev
sudo mkdir /tmp/install/
cd /tmp/install/
sudo wget https://codeload.github.com/utyfua/epsonsimplecups/zip/master
sudo unzip master
cd epsonsimplecups-master
sudo make
sudo make install
```
