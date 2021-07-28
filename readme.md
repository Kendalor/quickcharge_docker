1. Introduction/TLDR
2. Installation
    * [Get Docker](https://docs.docker.com/get-docker/) 
3. Running Images
    * Docker Hub
        * [Link](https://hub.docker.com/)
        * [CheatSheet](https://github.com/collabnix/dockerlabs/blob/master/docker/cheatsheet/README.md)
    * Docker Run
       * Pull Image `docker pull hello-world`
       * Run Image  `docker run -t --name example hello-world`
       * Show Containers `docker ps`
       * Stop Containers `docker stop example`
       * Remove Containers `docker rm example`
    * Demo DB Setup
        * [MySql](https://hub.docker.com/_/mysql)
        * Persisting Data with Volumes `-v HOSTDIR:TARGETDIR`
        * Opening Ports to Connect `-p HOSTPORT:CONTAINERPORT`
        * Setting ENV Variables `-e KEY=VALUE`
        * Run `docker run --name some-mysql -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:tag`
4. Building Images
    * Dockerfile
        * [CheatSheet](https://raw.githubusercontent.com/sangam14/dockercheatsheets/master/dockercheatsheet7.png)
    * Demo
5. Docker Compose
    * Docker Compose Files
    * Docker Compose Up/Down
    * Networks
    * Demo
