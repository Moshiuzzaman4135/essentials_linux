# Python
## System python
### Install specific version of python with all the depepdencies after adding repo
```
apt install python3.6 python3.6-dev python3.6-venv
```
### Disclose a location as HTTP server
```
python3 -m http.server
```
### Disclose a location as HTTP server with custom port and ip
```
python -m http.server 8000 --bind 127.0.0.1
```
### Create venev
```
python3.6 -m venv ~/venvs/venv_name
```
### Upgrade pip ,setuptools and wheel
```
pip install --upgrade pip wheel setuptools
```
### Install from requirements text file without cache
```
pip install -r requirements.txt --no-cache-dir
```
## Conda
### See conda environment lists
```
conda env list
```
### Create a conda environment with specific python version
```
conda create --name env_name python=3.6
```
### Crteate environment with other dependencies
```
conda create -n env_name python=3.8 pytorch=1.10 cudatoolkit=11.3 torchvision -c pytorch -y
```
### Activate and environment
```
conda activate env_name
```
### Kernel to install ipython and show up on jupyter notebook
```
ipython kernel install --user --name=env_name
```
### Deactivate conda environment 
```
conda deactivate
```
### Disable base env activation on system start on conda
```
conda config --set auto_active_base false
```
### Show base env activation status
```
conda config --show | grep auto_activate_base
```