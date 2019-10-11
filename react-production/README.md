# Production ready docker image for React js application
![reactjsdocker](https://user-images.githubusercontent.com/56213306/66462093-fbfaf500-ea97-11e9-9e70-4fe4684b2948.png)

This repository helps how to run a react application in `docker(https://www.docker.com/)`.

## Build a docker image
`docker build -t react:v1 .`

## Run docker container
`docker run -d --name reactjs -p 80:80 react:v1` and Navigate to `http://localhost/`

![Nodejs](https://user-images.githubusercontent.com/56213306/66650073-5be6cc80-ec4d-11e9-8ac9-465844e1d4e0.png)
## Create a Service
`docker service create --name reactjs --publish 80:80/tcp react:v1` and Navigate to `http://localhost/`

## Docker inspect provides detailed information --pretty will show short
`docker service inspect reactjs --pretty`

## Scale the reactjs Service
`docker service scale reactjs=2`

