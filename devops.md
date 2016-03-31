# An Introduction to DevOps
---
## Courtney Faulkner
### March 30, 2016



## Agenda
- What is DevOps?
- Containerization
- Continuous Integration (CI)
- Cloud Services
- DCOS/Swarm/DDC
- Infrastructure Automation
- Spring Boot and service registry



## What is DevOps?
> "DevOps (a clipped compound of "development" and "operations") is a culture, movement or practice that emphasizes the collaboration and communication of both software developers and other information-technology (IT) professionals while automating the process of software delivery and infrastructure changes. It aims at establishing a culture and environment where building, testing, and releasing software, can happen rapidly, frequently, and more reliably."
>
> &mdash; https://en.wikipedia.org/wiki/DevOps


## What is DevOps?
- Expansion of agile and CI to pipeline improvement and collaboration
    - Code development with CI
    - Infrastructure automation
    - Deployment automation

Note:


## What is DevOps?
### Collaboration Areas
- Dev
- QA
- Operations



## Containerization
- Docker

Note:
Enables configuration of a complete operating system in a virual machine, purpose-built to run a piece of software, such as a Spring Boot web application. It allows machines to be testable and repeatable independent of the piece of software being written to run on it. Docker hosts are linux machines that have kernel extensions to share their resources with docker containers at a low level, with programmatic hooks to deploy the docker containers. Docker containers are the transient instantiation of docker images. Docker images are inheritable machines, that are packages as slices to allow artifact resolution and slice reuse.



## Continuous Integration
- Jenkins
- Travis
- Spinnaker
- many others

Note:
http://techblog.netflix.com/2015/11/global-continuous-delivery-with.html
https://en.wikipedia.org/wiki/Comparison_of_continuous_integration_software



## Cloud Services
- Amazon Web Services
- Microsoft Azure
- Google Compute Engine
- On premises



## DCOS/Swarm/DDC
DCOS: Data Center Operating System

abstracts CPU, memory, storage, and other compute resources away from machines (physical or virtual), enabling fault-tolerant and elastic distributed systems to easily be built and run effectively


## DCOS/Swarm/DDC
Mesosphere:
- Apache Mesos (http://mesos.apache.org/)
- Marathon (https://mesosphere.github.io/marathon/)
- Chronos (https://mesos.github.io/chronos/)
- DCOS services (ex. Spark, Kafka, Hadoop, and Cassandra)

Note:
FOSS framework that packages Mesos, Marathon, Chronos, DCOS services. Marathon is a container orchestration product that identifies where in the Mesos cluster to deploy containers based on CPU and RAM availability. Marathon uses Chronos to actually schedule the deploys to the cluster. Chronos is a fault-tolerant cron replacement for job orchestration.


## DCOS/Swarm/DDC
Docker Swarm (https://docs.docker.com/swarm/overview/) is a node discovery and clustering solution, conceptually similar to DCOS. It works with many tools that also work against a single docker host:
- Docker
- Dokku
- Docker Compose
- Krane
- Jenkins



## Infrastructure Automation
- Ansible
- Puppet
- Chef
- Terraform
- SaltStack
- Vagrant



## Spring Boot and service registry
- Spring Boot (http://projects.spring.io/spring-boot/)
- Spring Cloud Consul (http://cloud.spring.io/spring-cloud-consul/spring-cloud-consul.html)
- Netflix Ribbon (https://github.com/Netflix/ribbon)
- Consul (https://www.consul.io/)
- Netflix Zuul (https://github.com/Netflix/zuul/wiki)

Note:
Spring Boot is an opinionated set of configurations for Spring apps, encapsulating much of the boilerplate configuration code for web applications, and exposing it as annotations. Spring Cloud provides and API to interacting with cloud services, such as service registries. Spring Cloud Consul is a specific plugin to interact with consul.io as a service registry. Ribbon implements client side load balancing. Consul is for service registry, service discovery, and key/value store that is exposed through a DNS interface. Zuul is a Java-based service request routing engine that is able to intergrate with Consul.
