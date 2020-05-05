# Linux/Mac

## Commands

```sh
# Check ports in use
netstat -vanp tcp | egrep <port number>

# List the latest file in a folder
ls -1l | tail -1

# Uncompress WAR file
jar -xf <war file>

# Compress with tar
tar -cvf <filename>.tar <directory>

# Create multiple directories
mkdir -p /folder1/folder2/folder3

# Bash with trace
bash -x <script file name>

# Sleep
sleep <seconds>

# Remove carriage returns and control-z characters from windows file
tr -d '\15\32' < winfile.txt > unixfile.txt

# Find files that contains a given text
grep -iRl "your-text-to-find" ./

# Find a text in a given file and its line
grep -c <text> <filnename>

# Check ports
sudo lsof -i -P -n
netstat -tulpn

# List USB devices
lsusb

# Force kill

kill -9 <PID>

# check Ubuntu version
lsb_release -a

# check linux version
uname -a
cat /etc/*-release

# watch the newest file with tail
watch “ls -t1 <filename> | sed q | xargs tail -300”

# Find and replace text in file(s)
sed -i 's/old-text/new-text/g' file(s)

# Check memory
free

# Check process with ps when you have ps aux truncated
ps -ef

# Check default umask
umask

# Set umask default
umask 022 # example

# Get last system reboot
who -b

# List devices connected
# dmesg (diagnostic message)
dmesg
```

### Linux chmod and umask option

0 – ler, escrever e executar
1 – ler e escrever
2 – ler e executar
3 – somente ler
4 – escrever e executar
5 – somente escrever
6 – somente executar
7 – sem permissões

### Linux file system definition

https://en.wikipedia.org/wiki/Filesystem_Hierarchy_Standard

### Linux /boot (full size)

https://gist.github.com/ipbastola/2760cfc28be62a5ee10036851c654600

### Vi editor

```sh
# Go to last file line
<ESC> GA

# Search
<ESC>/
```
## Definitions 

* PPA: It's the Personal Package Archive for Ubuntu distributions where you can create your own archive and users can install your packagers using the apt.
