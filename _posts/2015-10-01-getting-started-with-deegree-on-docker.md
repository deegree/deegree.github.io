---
layout: page
#
# Content
#
#subheadline: "Dummy"
title: "Getting started with deegree on docker"
#teaser: "...."
categories:
  - blog
tags:
  - deegree
  - java
  - docker
  - cloud
  - postgis
---

This blog post is meant to be the starting point for a series of posts about the usage of docker as a platform to build comprehensive geospatial webservices based on deegree. The first step to get started with docker and deegree is to think about deegree's system requirements. Well, that question has a very short answer: java and a servlet container. So I began to search for possible solutions to have a docker image fulfilling these prerequisities. I found the official tomcat container image on docker hub (<a href="http://hub.docker.com">http://hub.docker.com</a>). This acts as blueprint for my new deegree docker container. My two favorite things about docker are: there are tons of docker images to be used as blueprints to setup your own containers and it is really easy to use. Using the tomcat image leads into the following dockerfile:


~~~~~~ docker
FROM tomcat
MAINTAINER Sebastian Goerke &lt;goerke@lat-lon.de&gt;
# set deegree version
ENV DEEGREE_VERSION 3.3.14
# download deegree
RUN wget http://repo.deegree.org/content/repositories/public/org/deegree/deegree-webservices/${DEEGREE_VERSION}/deegree-webservices-${DEEGREE_VERSION}.war -O /usr/local/tomcat/webapps/deegree-webservices.war
CMD ["catalina.sh", "run"]
~~~~~~

With only these few lines it is possible to build and run a blank stable deegree webservices 3.3.14 on docker. But for a more advanced environment I want to add a PostGIS database to use it as a datasource. There is a nice image on the web which is built upon the official Postgres docker container (<a href="https://registry.hub.docker.com/u/mdillon/postgis/">https://registry.hub.docker.com/u/mdillon/postgis/</a>). Okay, now we have the dockerfile for the deegree container and we've got an image for running a PostGIS container. What I did next, to make things easier for users, was to add an image built from the dockerfile above to the docker hub. Now it is pretty easy to get that image using:

~~~~~~ bash
docker pull segoerke/deegree

# For the postgis image you can do exactly the same:
docker pull mdillon/postgis

# Now, it is pretty easy to startup a nice environment with a database server container and a web application container:
docker run -p 5432:5432 --name db -d mdillon/postgis
docker run --name deegree --link db:db -p 8080:8080 -d segoerke/deegree
~~~~~~ 


I already added port forwarding to the containers to be able to connect to them from my own server machine through these. So I am able to work on the database through localhost:5432 and I can access the tomcat through localhost:8080 on my local machine to work with the docker apps. Now it is possible to configure the deegree webservices and fill the database with data to be published with deegree webservices. I hope this short introduction is helpful to get started with deegree on docker. My idea is to have some more blog posts regarding a full INSPIRE setup with docker and orchestrated deegree containers.
