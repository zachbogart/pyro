# Base Docker Images
- Each branch is a different base image, which can be used for different things. They are available on DockerHub.

## Reasoning
- Wanted a way to work in a common environment
- Wanted people to be able to execute/try out code 
- Wanted to run it all in Jupyter
- Wanted to work in R and Python

## Create Image Locally
Execute at root of project directory:
```
docker build . -t pyrex:latest
```
