# Nvidia
> ## `Best to install Cuda dependencies using conda inside environment`  
## Never do this as the OS suggested
```
sudo apt install nvidia-cuda-toolkit
```
## 1. Cleanup
Follow these for updated instruction : [here](https://docs.nvidia.com/cuda/cuda-installation-guide-linux/index.html#removing-cuda-toolkit-and-driver)

First make sure to uninstall previous installation for clean install
### To remove CUDA Toolkit: 
```
sudo apt-get --purge remove "*cuda*" "*cublas*" "*cufft*" "*cufile*" "*curand*" \
 "*cusolver*" "*cusparse*" "*gds-tools*" "*npp*" "*nvjpeg*" "nsight*" "*nvvm*"
```
### To remove NVIDIA Drivers:
```
sudo apt-get --purge remove "*nvidia*" "libxnvctrl*"
```
### To clean up the uninstall:
```
sudo apt-get autoremove
```
#### `No Restart needed`

## 2. Package manager
Follow these for updated instruction : [here](https://docs.nvidia.com/datacenter/tesla/tesla-installation-notes/index.html#package-manager)
#### `nvidia-smi` command should worl after `restart`