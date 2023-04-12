# Package manager

## APT - Advanced package manager

- ### To show bunch of sub commands
```
apt
```
Output:
```
apt 2.4.8 (amd64)
Usage: apt [options] command

apt is a commandline package manager and provides commands for
searching and managing as well as querying information about packages.
It provides the same functionality as the specialized APT tools,
like apt-get and apt-cache, but enables options more suitable for
interactive use by default.

Most used commands:
  list - list packages based on package names
  search - search in package descriptions
  show - show package details
  install - install packages
  reinstall - reinstall packages
  remove - remove packages
  autoremove - Remove automatically all unused packages
  update - update list of available packages
  upgrade - upgrade the system by installing/upgrading packages
  full-upgrade - upgrade the system by removing/installing/upgrading packages
  edit-sources - edit the source information file
  satisfy - satisfy dependency strings

See apt(8) for more information about the available commands.
Configuration options and syntax is detailed in apt.conf(5).
Information about how to configure sources can be found in sources.list(5).
Package and version choices can be expressed via apt_preferences(5).
Security details are available in apt-secure(8).
                                        This APT has Super Cow Powers.
```
> Shows version of apt and all the most used commands for apt

- ### To see all the packages in apt database
```
apt list
```
Output:
```
Listing... Done
adduser/now 3.118ubuntu5 all [installed,local]
apt/now 2.4.8 amd64 [installed,local]
base-files/now 12ubuntu4.3 amd64 [installed,local]
base-passwd/now 3.5.52build1 amd64 [installed,local]
bash/now 5.1-6ubuntu1 amd64 [installed,local]
bsdutils/now 1:2.37.2-4ubuntu3 amd64 [installed,local]
coreutils/now 8.32-4.1ubuntu1 amd64 [installed,local]
dash/now 0.5.11+git20210903+057cd650a4ed-3build1 amd64 [installed,local]
debconf/now 1.5.79ubuntu1 all [installed,local]
debianutils/now 5.5-1ubuntu2 amd64 [installed,local]
diffutils/now 1:3.8-0ubuntu2 amd64 [installed,local]
dpkg/now 1.21.1ubuntu2.1 amd64 [installed,local]
e2fsprogs/now 1.46.5-2ubuntu1.1 amd64 [installed,local]
findutils/now 4.8.0-1ubuntu3 amd64 [installed,local]
gcc-12-base/now 12.1.0-2ubuntu1~22.04 amd64 [installed,local]
gpgv/now 2.2.27-3ubuntu2.1 amd64 [installed,local]
grep/now 3.7-1build1 amd64 [installed,local]
gzip/now 1.10-4ubuntu4.1 amd64 [installed,local]
hostname/now 3.23ubuntu2 amd64 [installed,local]
init-system-helpers/now 1.62 all [installed,local]
libacl1/now 2.3.1-1 amd64 [installed,local]
libapt-pkg6.0/now 2.4.8 amd64 [installed,local]
libattr1/now 1:2.5.1-1build1 amd64 [installed,local]
libaudit-common/now 1:3.0.7-1build1 all [installed,local]
libaudit1/now 1:3.0.7-1build1 amd64 [installed,local]
libblkid1/now 2.37.2-4ubuntu3 amd64 [installed,local]
libbz2-1.0/now 1.0.8-5build1 amd64 [installed,local]
libc-bin/now 2.35-0ubuntu3.1 amd64 [installed,local]
libc6/now 2.35-0ubuntu3.1 amd64 [installed,local]
libcap-ng0/now 0.7.9-2.2build3 amd64 [installed,local]
libcap2/now 1:2.44-1build3 amd64 [installed,local]
libcom-err2/now 1.46.5-2ubuntu1.1 amd64 [installed,local]
libcrypt1/now 1:4.4.27-1 amd64 [installed,local]
libdb5.3/now 5.3.28+dfsg1-0.8ubuntu3 amd64 [installed,local]
libdebconfclient0/now 0.261ubuntu1 amd64 [installed,local]
libext2fs2/now 1.46.5-2ubuntu1.1 amd64 [installed,local]
libffi8/now 3.4.2-4 amd64 [installed,local]
libgcc-s1/now 12.1.0-2ubuntu1~22.04 amd64 [installed,local]
libgcrypt20/now 1.9.4-3ubuntu3 amd64 [installed,local]
libgmp10/now 2:6.2.1+dfsg-3ubuntu1 amd64 [installed,local]
libgnutls30/now 3.7.3-4ubuntu1.2 amd64 [installed,local]
libgpg-error0/now 1.43-3 amd64 [installed,local]
libgssapi-krb5-2/now 1.19.2-2ubuntu0.1 amd64 [installed,local]
libhogweed6/now 3.7.3-1build2 amd64 [installed,local]
libidn2-0/now 2.3.2-2build1 amd64 [installed,local]
libk5crypto3/now 1.19.2-2ubuntu0.1 amd64 [installed,local]
libkeyutils1/now 1.6.1-2ubuntu3 amd64 [installed,local]
libkrb5-3/now 1.19.2-2ubuntu0.1 amd64 [installed,local]
libkrb5support0/now 1.19.2-2ubuntu0.1 amd64 [installed,local]
liblz4-1/now 1.9.3-2build2 amd64 [installed,local]
liblzma5/now 5.2.5-2ubuntu1 amd64 [installed,local]
libmount1/now 2.37.2-4ubuntu3 amd64 [installed,local]
libncurses6/now 6.3-2 amd64 [installed,local]
libncursesw6/now 6.3-2 amd64 [installed,local]
libnettle8/now 3.7.3-1build2 amd64 [installed,local]
libnsl2/now 1.3.0-2build2 amd64 [installed,local]
libp11-kit0/now 0.24.0-6build1 amd64 [installed,local]
libpam-modules-bin/now 1.4.0-11ubuntu2.3 amd64 [installed,local]
libpam-modules/now 1.4.0-11ubuntu2.3 amd64 [installed,local]
libpam-runtime/now 1.4.0-11ubuntu2.3 all [installed,local]
libpam0g/now 1.4.0-11ubuntu2.3 amd64 [installed,local]
libpcre2-8-0/now 10.39-3ubuntu0.1 amd64 [installed,local]
libpcre3/now 2:8.39-13ubuntu0.22.04.1 amd64 [installed,local]
libprocps8/now 2:3.3.17-6ubuntu2 amd64 [installed,local]
libseccomp2/now 2.5.3-2ubuntu2 amd64 [installed,local]
libselinux1/now 3.3-1build2 amd64 [installed,local]
libsemanage-common/now 3.3-1build2 all [installed,local]
libsemanage2/now 3.3-1build2 amd64 [installed,local]
libsepol2/now 3.3-1build1 amd64 [installed,local]
libsmartcols1/now 2.37.2-4ubuntu3 amd64 [installed,local]
libss2/now 1.46.5-2ubuntu1.1 amd64 [installed,local]
libssl3/now 3.0.2-0ubuntu1.8 amd64 [installed,local]
libstdc++6/now 12.1.0-2ubuntu1~22.04 amd64 [installed,local]
libsystemd0/now 249.11-0ubuntu3.7 amd64 [installed,local]
libtasn1-6/now 4.18.0-4build1 amd64 [installed,local]
libtinfo6/now 6.3-2 amd64 [installed,local]
libtirpc-common/now 1.3.2-2ubuntu0.1 all [installed,local]
libtirpc3/now 1.3.2-2ubuntu0.1 amd64 [installed,local]
libudev1/now 249.11-0ubuntu3.7 amd64 [installed,local]
libunistring2/now 1.0-1 amd64 [installed,local]
libuuid1/now 2.37.2-4ubuntu3 amd64 [installed,local]
libxxhash0/now 0.8.1-1 amd64 [installed,local]
libzstd1/now 1.4.8+dfsg-3build1 amd64 [installed,local]
login/now 1:4.8.1-2ubuntu2.1 amd64 [installed,local]
logsave/now 1.46.5-2ubuntu1.1 amd64 [installed,local]
lsb-base/now 11.1.0ubuntu4 all [installed,local]
mawk/now 1.3.4.20200120-3 amd64 [installed,local]
mount/now 2.37.2-4ubuntu3 amd64 [installed,local]
ncurses-base/now 6.3-2 all [installed,local]
ncurses-bin/now 6.3-2 amd64 [installed,local]
passwd/now 1:4.8.1-2ubuntu2.1 amd64 [installed,local]
perl-base/now 5.34.0-3ubuntu1.1 amd64 [installed,local]
procps/now 2:3.3.17-6ubuntu2 amd64 [installed,local]
sed/now 4.8-1ubuntu2 amd64 [installed,local]
sensible-utils/now 0.0.17 all [installed,local]
sysvinit-utils/now 3.01-1ubuntu1 amd64 [installed,local]
tar/now 1.34+dfsg-1ubuntu0.1.22.04.1 amd64 [installed,local]
ubuntu-keyring/now 2021.03.26 all [installed,local]
usrmerge/now 25ubuntu2 all [installed,local]
util-linux/now 2.37.2-4ubuntu3 amd64 [installed,local]
zlib1g/now 1:1.2.11.dfsg-2ubuntu9.2 amd64 [installed,local]
```
> Shows installed packages of apt database initially before running update

- ### Installing specific package
If the desired package is not in the apt database
```
apt install nano
```
Output:
```
E: Package 'nano' has no installation candidate
```
> As the database has not been updated with nano package

- #### Update the package database
```
apt update
```
> If we run 'apt list' now we will be able to see all the updated list of apt package database
Now if we use after *update*
```
apt install nano
```
The nano package will be installed.
> So before installing a package 'apt update' must be used

We can check if nano is installed by opening nano with following command
```
nano
```
Nano editor should be opened