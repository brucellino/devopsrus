# Docker README

This is the README for the Docker part.
Docker Compose is used to provision the Jenkins instance itself, as well as the reverse proxy which serves as the public interface.
The services are described in the `docker-compose.yml` file, with Dockerfiles for specific services in the relevant subdirectories.

## Services

The services are described in brief below. They are:

- jenkins (the jenkins instance)
- nginx (reverse-proxy HTTP server for the jenkins application)

### Nginx

Nginx is used to serve the application and act as the reverse proxy to Jenkins.
The application is based off of an existing Nginx Docker image, and configured by the addition of a configuration file at build time.

### Jenkins

Jenkins itself runs behind the Nginx server and provides the continuous integration and deployment pipeline service.
Jenkins is configured at build time using a two-phase configuration as code approach.

1. The first phase involves the addition of the relevant plugins, including the configuration as code plugin, which is persisted to a volume.
2. The second phase starts the Jenkins server, triggering the configuration based on the definition in `jenkins.yml`.
   

Almost all aspects of Jenkins can be configured:

- Jenkins system, credentials, tools