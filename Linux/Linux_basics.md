# Linux

## Shell
Shell is a program that takes our command and passes them to the operating system.
> Let's understand the shell prompt
### What does the below prompt mean?
```
root@874df82e1d5c:/# 
```
**'root' :** Currently logged in user, **'874df82e1d5c' :** Name of the machine , **'/' :** Where we are in the file system , **'#' :** Represents the highest privileges 

## Some basic commands
### To print something in the terminal
```
echo hello
```
Output:
```
/bin/bash
```
### To see who is the user
```
whoami
```
Output:
```
root
```

### To see location of the shell program
```
echo $0
```
Output:
```
/bin/bash
```

> 'bin' is a directory inside the directory we have a program 'bash' which runs the shell
### Linux is case sensitive
> So writing without considering case will result in command not working as below
```
Echo $0
```
Output:
```
bash: Echo: command not found
```
### Using up or down arrow we can navigate through previously used commands
### To see history of previously ran commands
```
history
```
Output:
```
    1  clear
    2  echo hello
    3  whoami
    4  echo $0
    5  Echo $0
    6  history
```
### To run previously ran commands from history using index
```
!2
```
Output:
```
echo hello
hello
```
### file count in a directory
```
ls -A | wc -l
```
### Watch file count in a directory that updates every second
```
watch -n 1 "ls -A | wc -l"
```
### System size and disk usage of each partition
```
du -H
```
### System size,used,available usage of current partition
```
df -H --output=source,size,used,avail .
```
### Directory size 
```
du -sh
```
### Every component size in a directory
```
du -h
```
### Watch directory size that updates every second
```
watch -n 1 'du -sh'
```
### Find similar file type and copy to a specific directory
```
find FIND_DIR -name "*.jpg" -exec cp "{}" COPY_TO_DIR  \;
```
### To check status of a specific port
```
ss -antpl | grep 1935
```
### Connect using ssh
```
ssh username@password@server_ip
```
### Copy file from server using SCP
```
scp -r username@server_ip:path/to/dir ./dir
```
### Add hostname and ip in hotsfile 
Open host file using nano
```
sudo nano /etc/hosts
```
Edit by putting the followings
```
192.168.0.1   test01
192.168.0.2   test02
192.168.0.3   test03
```
### Set enviroment varibles
```
export VARIABLE_NAME=value
```
### Run a bash file
```
./basfile.sh
```
### Pkill a python process
```
pkill -f code.py
```
### Pkill a  process
```
pkill -9 process_id
```
### Grep a string from a file
```
grep -i'String to find' log_file.log
```
### To see number of similar types of file in a directory
```
ls *.extension | wc -l
```
### See system resource usage using HTOP
```
htop
```
### See system resource usage using TOP
```
top
```
### To see linux distro version
```
lsb_release -a
```
### To see machine ip 
```
hostname -I
```
### See machine summary using neofetch
```
sudo apt install neofetch
neofetch
```
### See manual of a command
```
man 'cmd_name'
```