## Navigating filesystem
- ### Present working directory
```
pwd
```
> To see where we are in the filesystem.
- ### List all files
```
ls
```
> By default it lists multiple files on multiple lines.
```
ls -1
```
> To see them 1 item per line.
```
ls -l
```
> To see long listing which includes more details.
Output:
```
lrwxrwxrwx   1 root root    7 Mar  8 02:05 bin -> usr/bin
drwxr-xr-x   2 root root 4096 Apr 18  2022 boot
drwxr-xr-x   5 root root  360 Apr 12 04:04 dev
drwxr-xr-x   1 root root 4096 Apr 12 04:35 etc
drwxr-xr-x   2 root root 4096 Apr 18  2022 home
lrwxrwxrwx   1 root root    7 Mar  8 02:05 lib -> usr/lib
lrwxrwxrwx   1 root root    9 Mar  8 02:05 lib32 -> usr/lib32
lrwxrwxrwx   1 root root    9 Mar  8 02:05 lib64 -> usr/lib64
lrwxrwxrwx   1 root root   10 Mar  8 02:05 libx32 -> usr/libx32
drwxr-xr-x   2 root root 4096 Mar  8 02:05 media
drwxr-xr-x   2 root root 4096 Mar  8 02:05 mnt
drwxr-xr-x   2 root root 4096 Mar  8 02:05 opt
dr-xr-xr-x 420 root root    0 Apr 12 04:04 proc
drwx------   1 root root 4096 Apr 12 04:35 root
drwxr-xr-x   5 root root 4096 Mar  8 02:08 run
lrwxrwxrwx   1 root root    8 Mar  8 02:05 sbin -> usr/sbin
drwxr-xr-x   2 root root 4096 Mar  8 02:05 srv
dr-xr-xr-x  13 root root    0 Apr 12 04:04 sys
drwxrwxrwt   1 root root 4096 Apr 12 04:35 tmp
drwxr-xr-x   1 root root 4096 Mar  8 02:05 usr
drwxr-xr-x   1 root root 4096 Mar  8 02:08 var
```
To explain 
```
lrwxrwxrwx   1 root root    7 Mar  8 02:05 bin -> usr/bin
```
> 'lrwxrwxrwx' permissions of the file/directory
> 'root' means who owns the directory
> '7' is the size
> '7 Mar  8 02:05' means last modified
