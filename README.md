# Widgets Are Us 
## A microservices demonstration project

It includes these 7 projects, plus an ELK stack, Zipkin, RabbitMQ, and Jenkins.  I'm building it from scratch and handling
everything myself.  

I've only been working on it for three weeks, but I've got most of the infrastructure running locally with docker-compose.
I have a Kubernetes cluster set up on Amazon EKS. I've got an ELK stack with Zipkin on an EC2 instance running.  I've got
the four running services pushed to ECR, and now running on my EKS instance.  I just finished setting up a Jenkins machine
on an EC2 instance and now have full CI/CD for the 4 running services.


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