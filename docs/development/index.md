# Developer tasks

This article focuses on how project managers, DevOps engineers, and developers
can go from an idea to pushing out a Git commit:

1. Idea
2. Plan
3. Code
4. Commit and push to remote

## What tools are used during software development?

### Project management frameworks (Agile)

- Agile
- Kanban
- Scrum

!!! tip
    Read more about project management frameworks:

    [Frameworks and methodologies of developing and delivering software](/development/frameworks)

#### Tools for generating ideas

- Whiteboard
- Paper and pen
- Mind maps and diagrams

#### Tools for writing project plans

- Cucumber (feature specifications)
- GitHub discussions
- READMEs for feature proposals

### DevOps tools on the Dev side: set up reliable and consistent development environments

The only thing developers should be required to have installed on their workstations is Docker and Docker Compose.

If you use macOS, you should only need the lastest version of [Docker for Mac](https://docs.docker.com/docker-for-mac/install/).

If you use Windows, you should only need the lastest version of [Docker for Windows](https://docs.docker.com/docker-for-windows/install/).

The rest is run on the Docker platform via Docker containers. Usually, in order to start a local server for any kind of web application (in any programming language), just do this:

```sh
git clone https://github.com/${GITHUB_OWNER}/${WEB_APP_NAME}
cd ${WEB_APP_NAME}
docker-compose up
```

!!! tip
    I also recommend adding `alias dc=docker-compose` to your `~/.bashrc` to make it easier to type in:

    ```sh
    cd /path/to/${WEB_APP_NAME} && dc up
    ```
So, instead of having to install local copies of NodeJS, Ruby, or Python as runtimes for your applications and managing versions through some type of proprietary language version manager, you can manage all of this via a single, transparent and configurable interface of [Dockerfiles](https://github.com/ilyasotkov/rails-react-boilerplate) and [Docker Compose files](https://github.com/ilyasotkov/rails-react-boilerplate).

Docker containers are awesome because they are *cheap to create* -- they require much less resources than creating VMs. That means that all your software can be deployed in container images that you will never have to maintain or fix -- they're killed and recreated instead.

!!! important
    We don't ever want to **waste our time fixing or maintaining things**, it's a lot easier to just give up on a failed container and create a container using the same container image (that hopefully won't fail any more).


!!! example

    To find our what happens when you run `dc up`, just look inside the Docker Compose file:

    ```yaml
    image: ilyasotkov/rails-react-boilerplate:1.0.0-dev
    ```

    <small>Source: <https://github.com/ilyasotkov/rails-react-boilerplate></small>

To find out which port your web application is running on, you just have to look inside a straight-forward and transparent API of a Docker Compose file (`docker-compose.yaml`) file.

That means that you can be a developer without managing any of the dependencies for the project -- because the developers (or DevOps engineers) already took care of it in a transparent way ("Infrastructure as Code"), via the Dockerfile (container image definition file) and the Docker Compose file (local development environment definition file).

### Tools for authoring code

- A text editor (Atom, Vim, Sublime, etc.)

### Distributed version control systems

- A Git client (Git CLI, GitUp, Sourcetree)

!!! question "What is the value of learning and using a version control system?"

    - A distributed version control system allows developers to work on any part of the project at the same time
    - Ability to roll back to a previous version of a file or whole project
    - Ability to track changes and who made them

## Up next

[Delivering software continuously](/delivery)
