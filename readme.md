
## PHP Multiple Dev Environment

### Introduction
This project will facilitate developers to setup multiple dev environment to execute unit test and browse the site via deferent ports

#### Technology 
 - Docker
 - Docker compose 

#### How to spin up all env
    docker-compose -f env/php5-6/docker-compose.yml up -d
    docker-compose -f env/php7/docker-compose.yml up -d

#### How to spin down all env
    docker-compose -f env/php5-6/docker-compose.yml stop
    docker-compose -f env/php7/docker-compose.yml stop

#### How to browse the projects 
 - php 5.6 : http://localhost:8081/testme.php
 - php 7 : http://localhost:8082/testme.php
 
#### How to execute unit tests
    docker exec -it dev_web_php5_6 /bin/bash
    phpunit
