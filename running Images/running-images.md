## Running Images
* Docker Hub
    * [Link](https://hub.docker.com/)
    * [CheatSheet](https://github.com/collabnix/dockerlabs/blob/master/docker/cheatsheet/README.md)
* Hello World Example
    * Run the hello world docker image  `docker run -t --name example hello-world`
    * stop the example container `docker stop example`
    * see also stopped containers `docker ps -a`
    * cleanup the stopped container `docker rm example`
* Demo DB Setup
    * See documentation for an mySql DB [MySql](https://hub.docker.com/_/mysql)
    * Persisting Data with Volumes `-v HOSTDIR:TARGETDIR`
    * Opening Ports to Connect `-p HOSTPORT:CONTAINERPORT`
    * Setting ENV Variables `-e KEY=VALUE`
    * Run `docker run --name mysqlExample -e MYSQL_ROOT_PASSWORD=somepw  -p 3306:3306 -d mysql`
    * show the current running containers `docker ps`
    * shoe cpu usage `docker stats`
    * Login & Check using a tool of choice
    * Cleanup `docker stop mysqlExample` `docker rm mysqlExample`