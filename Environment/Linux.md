# Linux/Mac commands

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
```
