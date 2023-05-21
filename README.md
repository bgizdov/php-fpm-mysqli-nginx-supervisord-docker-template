# Docker compose template with php-fpm 8.x mysqli nginx supervisord and crontab

This Docker compose template is designed to streamline your web development process, providing all the necessary services in one go. With php-fpm 8.x, mysqli extension, nginx, supervisord and crontab all included, you’ll have everything you need to get your application up and running. 

The project contains:
- Nginx container for the web server
- PHP-FPM container for PHP execution
- PHP MySQLi extension
- Supervisord
- Crontab

## Setup
To use this template for your own application, simply put your php code in the app/ directory and make any changes to the config files as needed. For example, if you don’t require crontab functionality then it can be disabled, while server_name example.com; within nginx/site.conf should be changed to match your own domain name. Additionally, there may be other settings that need adjusting such as php variables within .user.ini.

## Start containers
When you’re ready to get started with your application development or testing environment simply run docker-compose up command!
```
docker-compose up
```






