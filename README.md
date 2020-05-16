# Docker, NGINX, PHP 7.4.x, Symfony 5.x and MySQL (almost) from scratch!

So yes, I'm back to the stack I thought I would never work with again. But this time I want to "dockerize" it and use 
the last current versions. And well, I'm back to Windows, even with the brand new WSL2! 

Everything may change in a little while.

However, I'll try to work some more mature architecture or... Whatever, just master this tech stack.

## Current goals:

### Infrastructure goals:
- [x] Use docker (in my case, for Windows)
- [x] Use Last NGINX version on docker
- [x] Use Last PHP version on docker
- [x] Use last Symfony version on the PHP container
- [ ] Use Monolog as logger mechanism 
- [ ] Use some MySQL-like database (MariaDB, Percona, Oracle) on Docker
- [ ] Use a Continuous Integration tool
- [ ] Use some cache mechanism (Redis?)
- [ ] Use RabbitMQ on Docker
- [ ] [MAYBE] Fool around with Elasticsearch and Kibana for Monitoring
- [ ] [MAYBE] Fool around with GraphQL as an anti-corruption Layer

### Architectural goals
- [ ] Create a simple SPA Web Application with authentication & authorization and database access
- [ ] Use third-party authentication
- [ ] Create services integration using a Message Broker
- [ ] Create a monitoring mechanism to check application health

### Development goals 
- [ ] Use a Jetbrains IDE to develop on the containers  
- [ ] Be able to debug directly on the IDE

### Academic goals:
- [ ] Use this environment to finish several online courses to help me master infrastructure and architectural goals
  - [ ] Theory - Symfony core features
  - [ ] First application (CRUD)
  - [ ] Doctrine entities, relations, fixtures, and console commands
  - [ ] Doctrine and LifecycleCallbacks, repositories
  - [ ] Redis for database session 
  - [ ] Unit tests
  - [ ] Functional tests
  - [ ] Login and authorization
  - [ ] Upload files
  - [ ] Events & listeners
  - [ ] Sending emails
  - [ ] i18n
  - [ ] Cache
  - [ ] REST API Platform
  - [ ] Symfony Messenger (RabbitMQ & CQRS)
 
## Index

1. [Infrastructure: Create your Docker containers - NGINX and PHP-FPM with Symfony](README.files/DOCKER.md);
2. [Development: Create your Symfony application](README.files/SYMFONY-PROJECT.md) 
3. [Development: Controllers](README.files/SYMFONY-CONTROLLER.md)
4. [Development: Views](README.files/SYMFONY-VIEW.md)
5. [Development: Entities](README.files/SYMFONY-ENTITY.md)
5. [Development: Services](README.files/SYMFONY-SERVICE.md)
6. TBD
