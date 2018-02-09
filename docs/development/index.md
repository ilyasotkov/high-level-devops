# Developer tasks

This article focuses on how project managers, DevOps engineers, and developers
can go from an idea to pushing out a commit of a pull request:

1. Idea
2. Plan
3. Code
4. Commit and push to remote

## What tools are used during software development?

### Using a software project management frameworks (Agile)

!!! important
    Read more about project management frameworks: https://devops.exekube.com/frameworks

#### Tools for generating ideas

- Whiteboard
- Paper and pen
- Mind maps and diagrams

#### Tools for writing project plans

- Cucumber (feature specifications)
- GitHub discussions
- READMEs for feature proposals

### DevOps: set up development environments

The only thing developers should be required to have installed on their workstations is Docker and Docker Compose.

The rest is run via Docker containers. Usually, in order to start a local server for any kind of web application (in any sort of language), you would have to:

```sh
git clone https://github.com/<user>/<web-app-name>
cd <web-app-name>
docker-compose up
```

I recommend adding `alias dc=docker-compose` to your `~/.bashrc` so that you can just:

```sh
git clone https://github.com/<user>/<web-app-name>
cd <web-app-name>
dc up
```

when you want to start a local server (with automatic browser reloading) your application. So, instead of having to install local copies of NodeJS, Ruby, or Python as runtimes for your applications and managing versions through some type of proprietary language version manager, you can manage all of this via a single, transparent and configurable interface of Docker images and Docker Compose files.

Docker containers are awesome because they are "cheap to create" and require much less resources than creating VMs. That means that all your software should be deployed in container images that you never have to fix -- they're consistently killed and recreated instead.

!!! important
    We don't ever want to **waste our time fixing things**, we should just be able to give up on a failed container and create a new one (that hopefully won't fail any more).


!!! example

    To find our what happens when your `dc up`, just look inside the Docker Compose file:

    ```yaml
    image: ilyasotkov/rails-react-boilerplate:1.0.0-dev
    ```

    <small>Source: <https://github.com/ilyasotkov/rails-react-boilerplate></small>

That way you always know what happens when you run `dc up` -- that is defined in the local `docker-compose.yaml` file and in the Dockerfile of the image that you will find in the `docker-compose.yaml` file.

You might wonder how you'd find which port your web application is running on. To find out, you just have to look inside a straight-forward and transparent API of a `docker-compose.yaml` file.



That means that you can become a developer without managing any of the dependencies for the project -- because the developers (and DevOps engineers) already took care of it in a transparent way ("Infrastructure as Code"), via the Dockerfile (container image definition file) and Docker Compose file (local development environment definition file).

### Code

- Text editor / IDE (Atom, Vim, Sublime, etc.)

### Commit and push to remote

- A Git client (Git CLI, GitUp, Sourcetree)

## What is the value of learning and using a version control system?

- A distributed version control system allows developers to work on any part of the project at the same time
- Ability to roll back to a previous version of a file or whole project
- Ability to track changes and who made them

## Read also

[Frameworks and methodologies of developing and delivering software](/development/frameworks)

## Up next

[Delivering software continuously](/delivery)
