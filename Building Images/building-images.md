# Building Spring Boot Java Application
1. Hello-World-Spring-Master
    * User Dockerfile to build an Image `docker build -t my-image .`
    * Use Docker Run with Parameters to start Container `docker run -d -p 8080:8080 --name myImageTest my-image`
    * Test Rest Endpoint [Test](http://localhost:8080)
    * Stop Container `docker stop myImageTest`
    * Remove Container `docker rm myImageTest`
2. Multi Stage Build
    * Write Multi Stage Build Dockerfile
        * Use maven Based image 
        * Define a workdir 
        * copy necessary files to the workdir
        * execute maven build
        * define a second stage with FROM
        * define a new Workdir
        * Copy generated Jar into Workdir
        * Define Entrypoint
    * Build the Image `docker build -t my-image-multi .`
    * Run the Container with correct Params `docker run -d -p 8080:8080 --name myImageTest my-image-multi`
    * Test the RestEndpoint [Test](http://localhost:8080)
    * Cleanup `docker stop myImageTest` `docker rm myImageTest`