## Description
Linux kernel 4.15.0 with ath9k driver modified to support the Atheros-CSI-Tool developed by xieyaxiongfly https://github.com/xieyaxiongfly/Atheros-CSI-Tool. 

## kernel Compilation Instructions
```
sudo apt-get install git libncurses5-dev libncursesw5-dev libelf-dev libnl-3-dev libssl-dev  
git clone https://github.com/kdkalvik/Atheros-CSI-Tool.git
cd Atheros-CSI-Tool
make menuconfig
make -j16
make modules
sudo make modules_install
sudo make install 
sudo reboot
```

Make sure the following kernel build flags are enabled for the CSI tool to work properly. 
```
CONFIG_ATH9K=m
CONFIG_ATH9K_AHB=y
CONFIG_ATH9K_DEBUGFS=y
CONFIG_ATH9K_STATION_STATISTICS=y
CONFIG_ATH9K_WOW=y
CONFIG_ATH9K_CHANNEL_CONTEXT=y
CONFIG_ATH9K_HTC=m
CONFIG_ATH9K_HTC_DEBUGFS=y
```
