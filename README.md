Assignmet [Netent Employee Service]

#### Prerequisite

Installed: [Docker](https://www.docker.com/), [Java 1.8 or 1.11](https://www.oracle.com/technetwork/java/javase/overview/index.html), [Maven 3.x](https://maven.apache.org/install.html), [git](https://www.digitalocean.com/community/tutorials/how-to-contribute-to-open-source-getting-started-with-git), optional [Docker-Compose](https://docs.docker.com/compose/install/)

#### Steps

##### Clone source code from git
```
$  git clone https://github.com/prabhakaran302/assignment.git
```

##### Build Docker image
```
$ cd assignment
$ cd employee-service
$ docker build -t="netent-employee-service" .
```
This will first run maven build to create jar package and then build employee-microservice image using built jar package.

##### Run Docker Container
```
$ docker run -p 8773:8773 -it --rm netent-employee-service
```

##### Test application

```
$ http://localhost:8773/swagger-ui.html
```

##### Monitoring application
```
$ http://localhost:8773/monitoring
```

#### Actuator
```
$ http://localhost:8773/actuator
```
