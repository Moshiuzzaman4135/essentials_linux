# Python

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