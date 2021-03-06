# Delivering software continuously

This article highlights the value of delivering software continuously.

1. Build container image
2. Deploy container image into a testing cloud environment
3. Test reliability
4. If tests are passed, deploy into production

## Build container images

Containers (Docker containers) allow us to run software predictably on any workstation and in any cloud environment.

The first step upon pushing source code into a remote version control repository is to build the image, or convert source code (Dockerfile) into executable machine code (Docker container image).

## Deploy container images into a testing deployment environment

Once the image is built, we deploy the software into a deployment environment that simulates production so that we can test its reliability.

## Test software's reliabilty

Reliability is tested via unit tests (low-level tests) and integration tests (end-to-end, high-level tests).

Scalability and security should be tested as well.

## Deploy into production

If the release candidate meets our quality requirements, we are ready to ship it into production, which is the deployment environment our end customers can access.

## Up next

[Monitoring and alerting](/monitoring)
