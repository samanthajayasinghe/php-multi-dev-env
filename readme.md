
## PHP Multiple Dev Environment

### Introduction
This project will facilitate developers to setup multiple dev environment to execute unit test and browse the site via deferent ports

#### Technology 
 - Docker
 - Docker compose 
 
#### Env information 

| PHP Version  | DB Version | DB-Host | DB-User | DB-Password |
| ------------- | ------------- |------------- | ------------- | ------------- |
| PHP 7.1  | Mysql 5.7.x  | db-mysql | root | root  |
| PHP 7.1  | MariaDB 10.x  | db-mariadb | root | root  |
| PHP 7.1  | Postgres 9.x  | db-postgress |postgres | postgres  |
| PHP 7.0  | Mysql 5.7.x  | db-mysql | root | root  |
| PHP 7.0  | MariaDB 10.x  | db-mariadb | root | root  |
| PHP 7.0  | Postgres 9.x  | db-postgress | postgres | postgres  |
| PHP 5.6  | Mysql 5.7.x  | db-mysql | root | root  |
| PHP 5.6  | MariaDB 10.x  | db-mariadb | root | root  |
| PHP 5.6  | Postgres 9.x  | db-postgress | postgres | postgres  |


#### How to spin PHP 5.6
    docker-compose -f env/php5-6/docker-compose.yml up -d
    docker-compose -f env/php5-6/docker-compose.yml stop

#### How to spin PHP 7.0
    docker-compose -f env/php7-0/docker-compose.yml up -d
    docker-compose -f env/php7-0/docker-compose.yml stop
    
#### How to spin PHP 7.1
    docker-compose -f env/php7-1/docker-compose.yml up -d
    docker-compose -f env/php7-1/docker-compose.yml stop  

#### How to browse the projects 
 - php 5.6 : http://localhost:8081/testme.php
 - php 7.0 : http://localhost:8082/testme.php
 - php 7.1 : http://localhost:8083/testme.php
 
#### How to execute unit tests
    docker exec -it dev_web_php70 /bin/bash
    phpunit
