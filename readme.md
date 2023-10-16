# Spring PetClinic Sample Application [![Build Status](https://github.com/spring-projects/spring-petclinic/actions/workflows/maven-build.yml/badge.svg)](https://github.com/spring-projects/spring-petclinic/actions/workflows/maven-build.yml)


## About the Project

This is a fork of the spring-petclinic project, with an emphasis on integrating Github actions to build, test and release to a JFROG artificatory. In my workflow, I have included the compiling of the source code, testing of dependancies with Maven central and succesfully building a docker image which is then published as a build to artifactory. 

More details can be doing by following the link to the project via the following:  <a href="https://speakerdeck.com/michaelisvy/spring-petclinic-sample-application">See the presentation here</a>

I've also left the link to the main project, should you wish to contribute or fork the project for your own purposes.

<img width="1679" alt="Screenshot 2023-10-16 at 14 41 38" src="https://github.com/zakirali1/spring-petclinic-Zak/assets/50696365/806f17d3-5a77-4863-b4d6-388c2be86e2e">

<img width="1675" alt="Screenshot 2023-10-16 at 14 40 36" src="https://github.com/zakirali1/spring-petclinic-Zak/assets/50696365/8548ef44-80bd-4563-8a16-9f83d46a9ac5">

## Steps to view the workflow in action

The github action I have created acts on any commit on this repo, and will work through the steps highlighted above, automating the CI phase of compiling, testing and building an image, which can then be augmented through additional features provided by JFROG Xray, such as scanning the artifacts or build for threats, config exposures such as secrets or policy violations. Additional approval paths can be introduced to move images from test to prod by promoting a build. This enables an organisation to have the upmost reasurrance that anything running in prod has been through CI/CD pipelines and passed all phases before delivery of the application binary, images, dependancies and so on. 

<img width="1673" alt="Screenshot 2023-10-16 at 14 43 19" src="https://github.com/zakirali1/spring-petclinic-Zak/assets/50696365/70fd4755-63b1-4dc9-a3ec-1063db4bb9ce">


## Pulling the image and running as a container

Once the build has been pushed to JFROG artifactory, you can pull image with the following command: 

```
docker pull zaktest.jfrog.io/petclinic-docker/spring-pet-clinic:latest

```

```
docker run -it spring-pet-clinic:latest bash

```


4) Navigate to Petclinic

    Visit [http://localhost:8080](http://localhost:8080) in your browser.


## Interesting Spring Petclinic branches and forks

The Spring Petclinic "main" branch in the [spring-projects](https://github.com/spring-projects/spring-petclinic)
GitHub org is the "canonical" implementation based on Spring Boot and Thymeleaf. There are
[quite a few forks](https://spring-petclinic.github.io/docs/forks.html) in the GitHub org
[spring-petclinic](https://github.com/spring-petclinic). If you are interested in using a different technology stack to implement the Pet Clinic, please join the community there.


