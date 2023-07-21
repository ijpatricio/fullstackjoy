# Full Stack Joy

Welcome.

Chances are you heard of Docker, but never used it. It can seem complex to use as a developer, just many other concepts, but in fact, this repo is not about that.

The fact we're using Docker it's just a detail. We are just using it as a consumer.

### Key concepts: Containers, Volumes and Ports (networking)

- Containers. Think of this as a single unit of a service, like an executable. By using containers, installing a piece of software, is just like adding a PHP or JS dependency to the `composer.json` or `package.json` file. Instead, we add it to a `docker-compose.yml` file, and everything happens for us.

- Volumes are "units of storage". A volume can be just an existing folder in our user land, or can be just a name in our Docker system, and we reference it always by name, for simplicity. Of course, it's a folder that lives in our disk, we just don't get to see it in front of us.

- Ports (or networking). A container lives in isolation. If we want to connect to a container, we need to make a "binding" between the host machine and the container. Say, we can have 3 containers running Nginx, and they all run on port 80 - isolated in their own world. If we want to expose them for accessing through our browser, we need to map ports from our machine to each one. So that a container can speak to other container, they need to be a Docker network or be explicitly linked to each other. 

Just with these 3 concepts alone, we can assemble a "definition file", just like in Composer or NPM, and have a piece of software running, while taking care of the persistence and networking.

### Installing Docker

```
# Install Docker
curl -sSL https://get.docker.com | sh
# Enable a non-root user to run docker commands
usermod -aG docker <username-to-enable>
```

#### TLDR;

Simple concepts in mind, not learning all the inners, we can benefit a lot by using services and self-hosted infrastructure, sometimes for production or for evaluation only, before using a hosted service.

Happy deploying!
