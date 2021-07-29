# Building Spring Boot Java Application
1. Hello-World-Spring-Master
    * User Dockerfile to build an Image
    * Use Docker Run with Parameters to start Container
    * Test Rest Endpoint [Test](http://localhost:8080)
    * Stop Container 
    * Remove Container
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
    * Build the Image 
    * Run the Container with correct Params
    * Test the RestEndpoint [Test](http://localhost:8080)
    * Cleanup