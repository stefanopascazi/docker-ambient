# MySQL image

## How to use

* Navigate to folder where docker-compose.yml is located
* Open your terminal
* Digit: `$ docker-compose up` or use `$ docker-compose up -d`

Read: [](https://hub.docker.com/_/mysql)

And for all enviroments variable to configure your MySQL server

If you want to rebuild this image:
* Stop your container: `$ docker-compose stop`
* Kill container: `$ docker-compose kill`
* Rebuild container: `$ docker-compose up -d --build`

## Connect to MySQL Server via web/app

This is most important if you want to connect all your web project or app to MySQL server that use different docker container

First of all, when MySQL server is running, find IPAddress.

* Locate MySQL container name: `$ docker ps`
* Now use: `$ docker inspect mysql_name` where "mysql_name" is your container name
* Find IPAddress or Gataway, now you able to connect to MySQL server

## Execute command via mysql>

* Locate MySQL container name: `$ docker ps`
* Access to a docker bash inside a MySQL image: `$ docker exec -it mysql_name` where "mysql_name" is your container name
* Now digit: `$ mysql -u root -p` insert your root password.
* Digit quit or exit for exit to bash.
* Digit exit for exit to a container's bash