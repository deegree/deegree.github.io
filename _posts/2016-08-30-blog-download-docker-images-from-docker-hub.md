---
layout: page
#
# Content
#
#subheadline: "Dummy"
title: "Download Docker images from Docker Hub"
#teaser: "...."
categories:
  - blog
tags:
  - deegree
  - java
  - cloud
  - docker
---
Get current deegree release versions from [Docker Hub](https://hub.docker.com/r/deegree/deegree3-docker/):

* 3.6 - `docker pull deegree/deegree3-docker:3.6`
* 3.5 - `docker pull deegree/deegree3-docker:3.5`
* 3.4 - `docker pull deegree/deegree3-docker:3.4`

To pull the latest Docker image use `docker pull deegree/deegree3-docker:latest`. This will pull the latest image which is currently 3.6.x! To stick with a specific bugfix version use `docker pull deegree/deegree3-docker:3.5.10`. Only the tags for the last recent versions are updated.

To start a Docker container with the name deegree on port 8080 run the following command:

`docker run -p 8080:8080 --name deegree --rm deegree/deegree3-docker`

The Dockerfile is available at [https://github.com/deegree/deegree3-docker](https://github.com/deegree/deegree3-docker).

Older versions of deegree Docker images are available from [https://hub.docker.com/r/tfr42/deegree/](https://hub.docker.com/r/tfr42/deegree/). The related Dockerfile is available at [https://github.com/tfr42/deegree-docker](https://github.com/tfr42/deegree-docker).

---

_Update 2019-10-26:_ 
Updated links to official deegree Docker repository and versions.   

_Update 2023-08-17:_ 
Updated image tags and versions for 3.5.  

_Update 2025-03-11:_
Updated image tags and versions for 3.6.