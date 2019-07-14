# MySQL Installation Steps for Ubuntu

```bash
# Install
sudo apt-get update
sudo apt-get install mysql-server

# Allow remote access
sudo ufw allow mysql

# Start the service
systemctl start mysql

# Start the mysql shell
/usr/bin/mysql -u root -p

# Set the root password
UPDATE mysql.user SET Password = PASSWORD('password') WHERE User = 'root';

# Flush the changes
FLUSH PRIVILEGES;

```
