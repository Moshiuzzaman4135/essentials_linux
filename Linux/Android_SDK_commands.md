# Android SDK
### Install android-sdk
```
sudo apt update
sudo apt install android-sdk
```
### add `./bashrc`  with following lines
```
export ANDROID_HOME="/usr/lib/android-sdk"
export PATH="$ANDROID_HOME/cmdline-tools/bin:$PATH"
export PATH="$ANDROID_HOME/tools:$PATH"
export PATH="$ANDROID_HOME/platform-tools:$PATH"
export PATH="$ANDROID_HOME/emulator:$PATH"
```
### Then do the following
```
latest/bin/sdkmanager --update
sdkmanager --list
sudo apt-get install -y android-sdk-platform-tools
./sdkmanager platform-tools emulator
```

### Start ADB Server
```
adb start-server
```
### Kill ADB Server
```
adb kill-server
```