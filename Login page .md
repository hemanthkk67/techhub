### created login web page using php,mysql database.  
***

~connect to mysql 

~creating database

~create user ,password and ~granted permissions 

~created table inside database , inserting user, passwd coloumns  in to table 

~configuired dbconfig.php file 


~connect to apache2 server 

whwere my file name is hemanthk ie. path /var/www/html

~uploaded folder inside visual code 

commit changes to my github 

~checking localhost status of my created page .  

![image2](https://github.com/hemanthkk67/pethub/blob/master/WAPT%20from%20Scratch/Day2(create%20login%20page)/Screenshot_2020-09-21_11-46-45.png)

***
### created virtual host for local host changing server name
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
