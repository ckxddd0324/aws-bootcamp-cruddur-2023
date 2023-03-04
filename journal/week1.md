# Week 1 — App Containerization

##### Build both backend and frontend app

- create docker for FE
- create docker for BE
- create docker-compose.yaml for building both FE and BE
- add notifcation page in flask and react

add postegres and dynamo db

- create dynamo items and table
  - for dynamodb, https://github.com/100DaysOfCloud/challenge-dynamodb-local
- add postgres to gitpod

  - cmd to connect on gitpod `psql --host localhost -Upostgres`

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

###### Homework

- Run the dockerfile CMD as an external script
- Push and tag a image to DockerHub (they have a free tier)
  - https://hub.docker.com/repository/docker/gn018681442/frontend-react-js/general
  - https://hub.docker.com/repository/docker/gn018681442/backend-flask/general
  - `docker build -g username:image/repo .`
  - `docker push username:image_name`
- Use multi-stage building for a Dockerfile build
- Implement a healthcheck in the V3 Docker compose file
- Research best practices of Dockerfiles and attempt to implement it in your Dockerfile
  - create different build for different environemnt such as local dev, staging, production
  - use multi stage build for production etc
  - use offical docker iamge as base image
    - - use smaller image
  - vulnerability for image build
  - not to use latest tag for image to deploy, use semantic versioning or image name:version/ hash
  - optimizing for cache build
  - use dockerignore file for node_modules, or cache
  - use least privilieged user in image

FLASK_ADDRESS="https://4567-${GITPOD_WORKSPACE_ID}.${GITPOD_WORKSPACE_CLUSTER_HOST}"
aws xray create-group \
 --group-name "Cruddur" \
 --filter-expression "service(\"backend-flask\")
