# Docker

Docker is an open-source project for **automating the deployment of applications**

I will assume that you know what is Open-source mean..

So we left with..

1. automating
2. deployment
3. application

## I will start with "What is deployment?"

which is the whole prepuce of docker, and we can use different tools to do it.

So we left with..

1. automating
2. application

## I will go with "What application means here?"

It means here Docker Image

### Docker Image

When a developer uses Docker, they create an app or service and package it and its dependencies into a container image. An image is a static representation of the app or service and its configuration and dependencies

**Docker containers** are the live, running instances of Docker images. 

*Image and container are not a separate concept, Container is a running Image*

So we left with..

1. automating

## Automating

and it is done by Dockerfile. A Dockerfile is a text file that contains instructions on how to build a Docker image. 

## What is DockerHub

To create a Docker image containing your application, you'll typically begin by identifying **a base image** to which you add more files and configuration. We can get the base images from DockerHub