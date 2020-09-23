### created login web page using php,mysql database.  
***
#### steps to to follow

#Install apache2 and mysql server
 
 sudo apt-get install apache2
 
 sudo apt-get mysql-server

#Start apache2 and mysql server

sudo service apache2 start

sudo service mysql start

#connect to mysql

sudo mysql -u root

#create new database

create database hemanthdb;

show databases;  #to check database

use hemanthdb;   #to create tables &columns inside db

#Create table and insert in to database

CREATE TABLE IF NOT EXISTS `users` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `username` varchar(200) NOT NULL,
  `password` varchar(33) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=66 ;

#Now insert columns in to table

INSERT INTO `users` (`id`, `username`, `password`) VALUES
(1, 'admin', '21232f297a57a5a743894a0e4a801fc3');

#to see created clounmns inside the table

~ select * from users  

#create new user for mysql 

~ create user 'username'@'localhost' identified by 'password';

#Grant permissions to this user

~ grant all privileges on hemanthdb.* to 'username'@'localhost' identified by 'password';

~Now configuire credentials in dbconf.php

<?php
$con = new mysqli("127.0.0.1", "username", "password", "hemanthdb");
if ($con -> connect_error){
    die("Database Not Congigured Properly");
}
else{
   // echo ("DB connection is established sir");
}
?>

#Restart apache2 server

~sudo service apache2 restart

#### Note: Things to be do before starting localhost

#Here the webapp folder path should be in /var/www/html

#my webapp name is hemanthk 

#Give permissions to hemanthk 
chmod -R 777 hemanthk

# checking localhost status of my created page .  

![image2](https://github.com/hemanthkk67/pethub/blob/master/WAPT%20from%20Scratch/Day2(create%20login%20page)/Screenshot_2020-09-21_11-46-45.png)

***
### changing server name local host to virtual host
***
~cd /etc/apache2/sites-available/

~cp default.conf to hemanth.host.conf

~vim hemanth.host.conf   

(add required path, host name)

~vim /etc/hosts    
(add server name) 

~ a2ensite hemanth.host.conf

~ systemctl reload apache2

~ ping  hemanth.host

~ curl hemanth.host -I
 
 now checked localhost with virtual host name ie. hemanth.host was succesfully loaded. 

***
Bypassed login page 
tested with below credentials

 admin' or 1=1#

 ![image1](https://github.com/hemanthkk67/pethub/blob/master/WAPT%20from%20Scratch/Day2(create%20login%20page)/Screenshot_2020-09-21_09-59-12.png)
