# Production ready docker image for React js application

This repository helps how to run a react application in `docker(https://www.docker.com/)`.

## Build a docker image
`docker build -t react:v1 .`

## Run docker container
`docker run -d -p --name=reactjs 80:80 react:v1` and Navigate to `http://localhost/`
