# Widgets Are Us 
## A microservices demonstration project

It includes these 7 projects so far, plus an Elasticsearch, Logstash, and Kibana (ELK) stack, Zipkin, RabbitMQ, and
Jenkins.  I'm building it from scratch and handling all the configuration myself.  

This project is little more than three weeks old now, but I think I have my infrastructure set up on AWS just the way I 
want it.  I started setting it up and running it locally with docker-compose, but now I've pretty much switched to
running it on AWS exclusively.  I've got a Jenkins build machine running on an EC2 instance with full CI/CD.  I need
only push a commit to my Github repo to get it built, tested, containerized, pushed, and deployed to Kubernetes running on EKS.

I have a Github webhook in each repo for the four running services.  They trigger Jenkins to kick off a build.  It pulls
the latest code.  Jenkins then compiles the code, runs all the tests, builds a docker image, pushes that image to my AWS Elastic
Container Repository, and gives Kubernetes the command to pull and run the new image.  It takes under a minute from pushing
the commit to Github to having it running on AWS.


- https://github.com/johatfie/widgets-are-us - Main repo with project set up, Docker, and Kubernetes files
  

- https://github.com/johatfie/config-server - Configuration server running in EKS
- https://github.com/johatfie/eureka-server - Eureka service discovery service running in EKS
- https://github.com/johatfie/gateway-server - Spring Cloud Gateway server running in EKS
- https://github.com/johatfie/customers-service - Customer information microservice running in EKS

  
- https://github.com/johatfie/microservices-properties - Configuration files served by config-server
- https://github.com/johatfie/hosts-file - Utility repo for easy switching between localhost, docker, and EKS via the hosts file


I would be remiss if I didn't cite my sources.  I learned a LOT from reading these five books.  
- https://www.manning.com/books/spring-microservices-in-action by John Carnell
- https://www.manning.com/books/spring-microservices-in-action-second-edition by John Carnell, Illary Huaylupo Sánchez
- https://www.manning.com/books/microservices-patterns by Chris Richardson
- https://www.manning.com/books/spring-in-action-fifth-edition by Craig Walls
- https://www.manning.com/books/spring-in-action-fourth-edition by Craig Walls 