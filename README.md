
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

- To build mysql db
    ```bash
    docker build -t passport-db docker/db/.
    ```

- To start mysql db
    ```bash
    docker run --name passport-db -p 13306:3306 -d passport-db
    ```

- To stop container then remove image and container
    ```bash
    docker stop passport-db && docker rm passport-db && docker rmi passport-db
    ```

- To build Docker Container Image
    ```bash
    docker build -t passport-webapp docker/webapp/.
    ```

- To run container
    ```bash
    docker run -it -d --name passport-webapp --link passport-db -p 8080:8080 -p 8443:8443  passport-webapp
    ```
    
- To stop container then remove image and container
    ```bash
    docker stop passport-webapp && docker rm passport-webapp && docker rmi passport-webapp
    ```
