# php-quickstart
hello world using php 
Learn PHP

## What is PHP?
- PHP is a server side scripting(which means that it’s used with other software and isn’t stand alone. For example, it can be embedded into HTML code or other web template systems) language used for static and Dynamic websites. 
- It stands for HyperText Pre-processor but used to stand for Personal Home Page
- It can only be used with servers that have PHP installed 
- Client computers need a web browser to access PHP scripts

## Why PHP?
- Large community
- Simple to learn
- Supported by most web hosting servers 
- Regularly updated to keep up with trends
- Server side meaning clients do not need PHP installed
- Built in support for MySQL and can be used with other database management systems
- It is also cross platform so it can be deployed on windows, Linux and Mac OS etc.
- It is used by Facebook, Wikipedia and Wordpress

## PHP Usage Tips
- Case sensitive
- Servers interpret PHP code and outputs the results as HTML code to web browsers
- To be identified, the PHP code has to be enclosed in PHP  tags.

## Installation 
- For PHP, Apache , a widely used web server software, is required. 
- To use Apache on Mac type in  <sudo apachectl start >/<sudo apachectl stop>/<sudo apachectl restart>
- <httpd -v> to get apache version
- Open localhost and you get a message
- Create /Sites folder in username <sudo mkdir ~/Sites>
- Create username.conf <cd /etc/apache2/users>
- sudo <text editor> username.conf
- Add the text below 
<Directory "/Users/username/Sites/">
AllowOverride All
Options Indexes MultiViews FollowSymLinks
Require all granted
</Directory>
- Open the httpd.conf </etc/apache2/httpd.conf>
- Uncomment these lines 
LoadModule authz_core_module libexec/apache2/mod_authz_core.so
LoadModule authz_host_module libexec/apache2/mod_authz_host.so
LoadModule userdir_module libexec/apache2/mod_userdir.so
LoadModule include_module libexec/apache2/mod_include.so
LoadModule rewrite_module libexec/apache2/mod_rewrite.so
LoadModule php7_module libexec/apache2/libphp7.so
Include /private/etc/apache2/extra/httpd-userdir.conf

- In the same file, Override .htaccess and allow URL rewrites, like in the text below 
    --AllowOverride controls what directives may be placed in .htaccess files.
    --It can be "All", "None", or any combination of the keywords:
    --AllowOverride FileInfo AuthConfig Limit
     
    --AllowOverride All

    --Controls who can get stuff from this server.
    
    --Require all granted
    
    
- Open the http-userdir.conf file  using <sudo <text editor> /etc/apache2/extra/httpd-userdir.conf> and uncomment the txt below 
Include /private/etc/apache2/users/*.conf

- Restart apache <sudo apachectl restart>

- To check if PHP is actually running create a index.php file using <sudo touch /Library/WebServer/Documents/index.php> and open it up with a text editor.
- Then add  and save this PHP code

--<?php
--Echo “Hello World”;
--?>

-Then open it up using localhost/index.php
