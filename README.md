
## CAS Overlay with Docker
 
 This is sample implementation of CAS SSO framework web application. We also have a Docker Container build file here which can be used to build and run this app as Docker Container.
   
#### Gradle Commands:

- Build
    ```bash
    ./gradlew clean build
    ```

- To see what other tasks are available;
    ```bash
    ./gradlew tasks
    ```

#### Docker Commands:
 
- To build Docker Container Image

    ```bash
    docker build -t passport-webapp docker/.
    ```

- To run container
    ```bash
    docker run -it -d --name passport-webapp -p 8080:8080 -p 8443:8443  passport-webapp
    ```
    
- To stop container
    ```bash
    docker stop passport-webapp
    ```
    
- To remove container
    ```bash
    docker rm passport-webapp
    ```
    
- To remove container image
    ```bash
     docker rmi passport-webapp
    ```