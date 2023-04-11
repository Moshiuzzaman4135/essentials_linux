﻿# Linux

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
$ echo hello
hello
```
- ### To see who is the user
```
$ whoami
root
```
- ### To see location of the shell program
```
$ echo $0
/bin/bash
```
> 'bin' is a directory inside the directory we have a program 'bash' which runs the shell
- ### Linux is case sensitive
> So writing without considering case will result in command not working as below
```
$ Echo $0
bash: Echo: command not found
```
- ### Using up or down arrow we can navigate through previously used commands
- ### To see history of previously ran commands
```
$ history
    1  clear
    2  echo hello
    3  whoami
    4  echo $0
    5  Echo $0
    6  history
```
- ### To run previously ran commands from history using index
```
$ !2
echo hello
hello
```

