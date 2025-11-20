## Steps for Setup

1. Create VM and changed to UBUNTU 
 - Instance type Small
2. Open TCP ports 22 and 3306
3. Open SSH and instal necessary packages
    -sudo apt-get update
    -sudo apt install mysql-server mysql-client
    -mysql
4. Setup username and password
    - Create user 'example'@'%' identified by 'example"
    -CONFIRM: select user from mysql.user
    -GRANT ALL PRIVILEGES ON *.* TO 'example'@'%' WITH GRANT
OPTION;
    -CONFIRM: show grants for example;

5. Add database
    -create database example;
    -show databases;

6. sudo nano
    -then restart

7. Should be able to acces now: Test locally in Google Shell
    -mysql -u example -h 00.00.00/0 -p
    - enter password
    -should show databases

