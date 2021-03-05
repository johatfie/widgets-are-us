# Widgets Are Us

A microservices demonstration project

I've only been working on it for two weeks, but I've got most of the infrastructure running, locally at least.
I'll be moving it to Amazon EKS in the near future, but so far I'm just running it locally with docker-compose.
It includes these 5 projects, plus an ELK stack and Zipkin.  I'm building it from scratch and handling everything
myself.  I plan to have a Jenkins machine on an EC2 instance and full CI/CD.

- https://github.com/johatfie/config-server
- https://github.com/johatfie/eureka-server
- https://github.com/johatfie/gateway-server
- https://github.com/johatfie/microservices-properties
- https://github.com/johatfie/customers-service
- https://github.com/johatfie/hosts-file


I would be remiss if I didn't cite my sources.  I learned a lot from these five books.  
- https://www.manning.com/books/spring-microservices-in-action by John Carnell, Illary Huaylupo Sánchez
- https://www.manning.com/books/spring-microservices-in-action-second-edition by John Carnell, Illary Huaylupo Sánchez
- https://www.manning.com/books/microservices-patterns by Chris Richardson
- https://www.manning.com/books/spring-in-action-fifth-edition by Craig Walls
- https://www.manning.com/books/spring-in-action-fourth-edition by Craig Walls 