# CUDA
## `Try to follow Nvidia_install_process.md file procedure instead of this`  
> ## `Best to install Cuda dependencies using conda`  
## Nvidia
### Remove all previous cuda , cudnn and nvidia dependencies
```
sudo apt-get --purge remove "*nvidia*"
sudo apt-get --purge remove "*cuda*"
sudo apt-get --purge remove "*cudnn*"
sudo apt-get autoremove
sudo apt-get autoclean
sudo rm -rf /usr/local/cuda*
sudo reboot
```
## Linux Setup
> Tested onUbuntu 18.04 (CUDA 10.0)
### Add NVIDIA package repositories
```
cd Downloads    
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/cuda-repo-ubuntu1804_10.0.130-1_amd64.deb
sudo dpkg -i cuda-repo-ubuntu1804_10.0.130-1_amd64.deb
sudo apt-key adv --fetch-keys https://developer.download.nvidia.com/compute/cuda/repos/ubuntu1804/x86_64/7fa2af80.pub
sudo apt-get update
wget http://developer.download.nvidia.com/compute/machine-learning/repos/ubuntu1804/x86_64/nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb
sudo apt install ./nvidia-machine-learning-repo-ubuntu1804_1.0.0-1_amd64.deb
sudo apt-get update
```
### Install NVIDIA driver
```
sudo apt-get install --no-install-recommends nvidia-driver-430
sudo reboot
```

#### Check that GPUs are visible using the command: ```nvidia-smi```

### Install development and runtime libraries
```
sudo apt-get install --no-install-recommends cuda-10-0 libcudnn7=7.6.2.24-1+cuda10.0 libcudnn7-dev=7.6.2.24-1+cuda10.0
sudo reboot 
```
#### Check that GPUs are visible using the command: ```nvidia-smi```
#### Check output of ```nvcc --version``` command. Output should be "Cuda compilation tools, release 10.0, V10.0.130" 
> ### Troubleshoot 
> If `nvcc` command not found, add the following lines at the bottom of your ~/.bashrc file

```
export PATH=/usr/local/cuda/bin:$PATH
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/cuda/lib64
```
### Watch GPU usage update every second
```
watch -n 1 -d nvidia-smi
```