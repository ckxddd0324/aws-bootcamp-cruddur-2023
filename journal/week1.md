# Week 1 — App Containerization

##### Build both backend and frontend app

- create docker for FE
- create docker for BE
- create docker-compose.yaml for building both FE and BE

- create gitpod
- create aws cloud9 for debugging/running code
  - learn some of the billing regarding the use of cloud9
- setup cloudtrail
  - which log all the api requests from the aws acounts
  - log requests for 90 days
  - disable kms to save costs
  - data and insight events can be expensive because it is logging activity from the resources

container security

- reducing impack of breach
- docker image/container is helping people to development or share similar env to development
  - people able to share the docker file to development on similar env
- managed container services like
  - AWS ECS, ECR

##### cloud security component

- Docker & host config
- securing images
- secret management
- application secruity
- data security
- monitoring containers
- compliance framework

##### security best pracitice

- keep host and docker updated to latest security patches
- docker daemon and container should not run in root user mode
- image vulnerability scanning(3rd party tool)
- trusting a private vs public image registry
- no sensitive data in docker images/file/docker-compose file
- user secret management service
- read only file system and volume for docker
- separate database for long term storage
- use DevSecOps practices
- ensure all code is tested for vulnerabilites before prod use

##### Synk

- setup integration with Synkio with github
- use a sample repo from synk lab to look at scanning info from snyk dashboard
- breakdown of the vulnerability or security patches for the repo

##### Synk cli

cmd

- snyk container test [image_name]

##### AWS Secure Manager

- to store secret
- only certain services can be use with AWS Secure manager
- alternative secret management
  - hashicorp vault(free/paid)
- setup secret manager
  ```
    1. create key/value pair
    2. setup secret name
    3. add tags
    4. automatic rotation(can be setup)
    5. once created, you can access through api call
  ```

##### AWS inspector/clair

- secruity analyzer/ scanning docker image
- how to use aws inspector
  ```
    - can be use to scan images, instance, repo, lambda func
  ```
