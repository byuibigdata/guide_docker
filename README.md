## I. Installation

![Docker + VSCode](https://user-images.githubusercontent.com/59627216/159537585-d0b008e7-e9c6-4faf-9700-26fd5642f491.png)


### Tools
- Docker: https://docs.docker.com/get-docker/
- VSCode: https://code.visualstudio.com/download
- Docker Extension: https://code.visualstudio.com/docs/containers/overview

### Troubleshooting
- https://github.com/docker/docker.github.io/issues
- https://github.com/microsoft/vscode/issues
- https://www.youtube.com/watch?v=E5ezkYSiNiE

## 1. Introduction - Josh Phillips

### 1.1 Docker Setup

- 
-
-
-

### 1.2 What is a Docker Image?

-
-
-

### 1.3 What is a Docker Container?

-
-
-

## 2. Creating the Docker File - Spencer Williams

### 2.1 What is a docker file?

![Docker File](https://user-images.githubusercontent.com/59627216/159536551-599e8e2a-f4e5-4a3d-8d49-42ede1d9a365.png)


- A text file with instructions for creating your docker image, which is a file with executable code. It is similar to a makefile for other programming languages and  their compliers but is used for the file to work with docker. 
- This in turn provides a form of automation for creating the docker image when creating for the first time and afterwards.
- A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image.

### 2.2 Creating a docker file

![Creating file](https://user-images.githubusercontent.com/59627216/159536991-19afc878-0b4e-43cd-9df4-f25f1b17aaf1.gif)


- Via VS code extension, ... F1 while using the docker extension and selecting the type of file we want and its entry point (the main file it will execute)
- Via command line, touch DockerFile and vim Dockerfile to then edit it 
- docker list to view created docker files

### 2.3 Editing the docker file

- *Selecting which python version to use (The FROM instruction initializes a new build stage and sets the Base Image for subsequent instructions)*
- FROM python:3.7
- *Path to the image file* 
- WORKDIR /app 
- *Copying our requirements.txt*
- COPY requirements.txt ./requirements.txt 
- *To install the necessary dependencies for your application to run*
- RUN pip install -r requirements.txt 
- *The EXPOSE instruction tells Docker to get all its information required during the runtime from a specified Port. These ports can be either TCP or UDP, but it's TCP by default.*
- EXPOSE 8501 
- *Copy everything under the directory*
- COPY . /app 
- *Setting the entry point or where your application will start*
- ENTRYPOINT ["streamlit", "run"] 
- *CMD allows you to input execute command lines when using your docker file (i.e. run main.py)*
- CMD ["main.py"] 

## 3. Docker Build - Hera Yang

### 3.1

-
-
-

### 3.2

-
-
-

### 3.3

-
-
-

## 4. Running the Container - Mireya Vera Loo

### 4.1

-
-
-

### 4.2

-
-
-

### 4.3

-
-
-

## 5. Pushing to the Docker Hub - Ben Hinchman 

### 5.1 docker push [OPTIONS] NAME[:TAG]
- docker push behaves much like Github push does. It will push any changes made up to the image it is said to push to.
- for the [OPTIONS], you have -a, -q, and --disable-content-trust
- -a pushes all tagged images up to either your local repo or your cloud repo.
- NAME is the name of your image. [:TAG] is whatever tag you want to give it, like a version number.

### 5.2 docker push
- docker push MYIMAGE:VERSION // docker push myimage:1.0
- If you push myimage:1.0, make a change, and then make a new one, myimage:1.1, you will be able to grab both versions, and run the differences in them. Remember, each push is a unique, read-only image. Keeping track of Version History is helpful, much like Github Commits

### 5.3 Docker Hub
- docker login --username=yourhubusername --email=youremail@company.com
- After that, you'd be prompted to login. It'll save your password through the command line.
- docker tag [IMAGEID] [DOCKERUSERNAME]/[IMAGENAME]:[VERSION] //// docker tag myimage tujianis/image:1.5.5
- docker push [DOCKERUSERNAME]/[IMAGE] will //// docker push tujianis/centos
- docker pull [IMAGE] //// docker pull centos

## 6. Docker Application - Caden Franc

### 6.1

-
-
-

### 6.2

-
-
-

### 6.3

-
-
-

## Questions and Answers

- [Interview Questions for jobs that use Docker?](https://hackr.io/blog/docker-interview-questions)
- [What are the pros and cons of Docker?](https://blog.iron.io/docker-containers-the-pros-and-cons-of-docker/)
- [How to debug when using Docker in VSCode?](https://code.visualstudio.com/docs/containers/debug-common)
- [How to optimize Docker?](https://circleci.com/blog/tips-for-optimizing-docker-builds/)
- [How is Docker secure?](https://docs.docker.com/engine/security/#:~:text=Conclusions,or%20another%20appropriate%20hardening%20system.)

## Videos about and on using Docker

- [What is Docker in 5 mins](https://www.youtube.com/watch?v=_dfLOzuIg2o)
- [How to create and build Dockerfile](https://www.youtube.com/watch?v=LQjaJINkQXY)
- [Run Your App in a Container](https://www.youtube.com/watch?v=jtBVppyfDbE)

## Resources
- [Deploying Streamlit via Docker](https://www.section.io/engineering-education/how-to-deploy-streamlit-app-with-docker/)
- [Docker Containers](https://www.docker.com/resources/what-container/)
- [Docker Containers and Azure](https://github.com/BYUI451/cloud_guide/blob/main/azure.md) 
- [Using Spark for exploratory data analysis](https://github.com/BYUI451/spark_guide)
- [Docker](https://github.com/BYUI451/docker_guide)
- [Rocker Guide](https://github.com/BYUI451/rocker_guide)

## Additional Resources to Explore

- [Docker Volumes](https://docs.docker.com/storage/volumes/)
- [Docker Networks](https://docs.docker.com/network/)
- [Container Registries](https://docs.docker.com/registry/)
- [Docker Compose](https://docs.docker.com/compose/) 
- [Docker vs. Kubernetes](https://semaphoreci.com/blog/kubernetes-vs-docker)



