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

# Check ports
sudo lsof -i -P -n
netstat -tulpn

# List USB devices
lsusb

# Force kill

kill -9 <PID>
```

### Vi editor

```sh
# Go to last file line
<ESC> GA

# Search
<ESC>/
```
## Definitions

* PPA: It's the Personal Package Archive for Ubuntu distributions where you can create your own archive and users can install your packagers using the apt.
