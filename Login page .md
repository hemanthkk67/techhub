### created login web page using php,mysql database.  
***
#### steps to to follow

#### Install apache2 and mysql server
 
 sudo apt-get install apache2
 
 sudo apt-get mysql-server

### Start apache2 and mysql server

sudo service apache2 start

sudo service mysql start

####  Download the Code :

   git clone https://github.com/anir0y/verzeo-webapp 

#Here the verzeo-webapp folder path should be change to /var/www/html

#I changed webapp name as hemanthk

#Give permissions to hemanthk 

chmod -R 777 hemanthk

#### connect to mysql

sudo mysql -u root

#### create new database

~ create database hemanthdb;

~ show databases;  #to check database

~ use hemanthdb;   #to create tables &columns inside db

#### Create table and insert in to database

CREATE TABLE IF NOT EXISTS `users` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `username` varchar(200) NOT NULL,
  `password` varchar(33) NOT NULL,
  PRIMARY KEY (`id`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=66 ;

#### Now insert columns in to table

~ INSERT INTO `users` (`id`, `username`, `password`) VALUES
(1, 'admin', '21232f297a57a5a743894a0e4a801fc3');

#### To see created clounmns inside the table

~ select * from users  

#### create new user for mysql 

~ create user 'username'@'localhost' identified by 'password';

### Grant permissions to this user

~ grant all privileges on hemanthdb.* to 'username'@'localhost' identified by 'password';

#### Now configuire your own credentials in dbconf.php

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



# checking localhost status of my created page .  

![image2](https://github.com/hemanthkk67/pethub/blob/master/WAPT%20from%20Scratch/Day2(create%20login%20page)/Screenshot_2020-09-21_11-46-45.png)

***
### changing server name local host to virtual host
***
Go to sites-available directory it shows the default config files

$ cd /etc/apache2/sites-available/

000-default.conf  default-ssl.conf

#### Here we can change the '000-default.conf' to your required name

$cp 000-default.conf to hemanth.host.conf

#### Now edit the .conf file 

~vim hemanth.host.conf   

        #ServerName www.example.com

        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/html


#### (change server name  to your desired host name,give the path of the webapp name)

        ServerName hemanth.host
        ServerAdmin webmaster@localhost
        DocumentRoot /var/www/html/hemanthk/

#### mention the virtual host name in hosts 

In this case my host name is hemanth.host

$vim /etc/hosts    
                    
127.0.0.1       localhost hemanth.host 
127.0.1.1       kali
127.0.0.1       mydvwa.com
#The following lines are desirable for IPv6 capable hosts
::1     localhost ip6-localhost ip6-loopback
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters

#### To enable site hosted with Apache ,use the 'a2ensite and reload apache2 

$a2ensite hemanth.host.conf

$systemctl reload apache2

#### check the host status

$ ping  hemanth.host

$curl hemanth.host -I
 
 now we can check localhost with virtual host name ie. 'hemanth.host' was succesfully loaded. 

***
Bypassed login page 
tested with below credentials

 admin' or 1=1#

 ![image1](https://github.com/hemanthkk67/pethub/blob/master/WAPT%20from%20Scratch/Day2(create%20login%20page)/Screenshot_2020-09-21_09-59-12.png)
