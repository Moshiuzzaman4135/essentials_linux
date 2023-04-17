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
- ### To print something in the terminal
```
echo hello
```
Output:
```
/bin/bash
```
- ### To see who is the user
```
whoami
```
Output:
```
root
```

- ### To see location of the shell program
```
echo $0
```
Output:
```
/bin/bash
```

> 'bin' is a directory inside the directory we have a program 'bash' which runs the shell
- ### Linux is case sensitive
> So writing without considering case will result in command not working as below
```
Echo $0
```
Output:
```
bash: Echo: command not found
```
- ### Using up or down arrow we can navigate through previously used commands
- ### To see history of previously ran commands
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
- ### To run previously ran commands from history using index
```
!2
```
Output:
```
echo hello
hello
```
- ### file count in a directory
```
ls -A | wc -l
```
- ### Watch file count in a directory that updates every second
```
watch -n 1 "ls -A | wc -l"
```
- ### Directory size 
```
du -sh
```
- ### Watch directory size that updates every second
```
watch -n 1 'du -sh'
```
- ### Find similar file type and copy to a specific directory
```
find FIND_DIR -name "*.jpg" -exec cp "{}" COPY_TO_DIR  \;
```
- ### To check status of a specific port
```
ss -antpl | grep 1935
```
- ### Connect using ssh
```
ssh username@password@server_ip
```
- ### Copy file from server using SCP
```
scp -r username@server_ip:path/to/dir ./dir
```
