```bash
echo -e "---------------------------------------------------------------------------------"
echo "Step 1 - Installing MySQL"
echo -e "---------------------------------------------------------------------------------"

# update the package index on your server if you’ve not done so recently
sudo apt update

# install the mysql-server package
sudo apt install mysql-server -y

# ensure that the server is running using the systemctl start command
sudo systemctl start mysql.service

# open up the MySQL prompt
sudo mysql

# run the following ALTER USER command to change the root user’s authentication method to one that uses a password
# following example changes the authentication method to mysql_native_password
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

# exit the MySQL prompt
exit

# you can run the mysql_secure_installation script without issue
mysql -u root -p
```

```bash
# install mysql on Ubuntu
sudo apt install mysql-server -y

# ensure that the server is running using the systemctl start command
sudo systemctl start mysql.service

# open up the MySQL prompt
sudo mysql

# run the following ALTER USER command to change the root user’s authentication method to one that uses a password
# following example changes the authentication method to mysql_native_password
mysql> ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';

# exit the MySQL prompt
mysql> exit
```