---
layout: page
#
# Content
#
#subheadline: "Dummy"
title: "Quo vadis deegree?"
#teaser: "...."
categories:
  - blog
tags:
  - deegree
  - java
  - cloud
  - enterprise
---
*And why we still stick with Java*

deegree has proven in productive environments to comply to the [OGC standards for geospatial web services](https://www.opengeospatial.org/docs/is) as well as to tackle even the complex INSPIRE regulations. Including the performance requirements specified in the [INSPIRE Technical Guidance for network services](https://inspire.ec.europa.eu/Technical-Guidelines2/Network-Services/41). Saying this also implies to have a closer look how this relates to the technology stack chosen for deegree web services and how to benefit from it when we think about the future development of deegree. 

From the beginning of the open source project deegree was designed to run on the [Java Virtual Machine (JVM)](https://docs.oracle.com/javase/specs/jvms/se8/html/index.html) the most used runtime environment for business critical applications. Using Java as a programming language has for sure one big advantage in using an object-oriented programming language to design internal domain models such as the one for GML and to leverage the rich API’s provided by Java SE and EE. But the main advantage for developing full-fledged SDI solutions is to have a mature runtime environment which also supports multiple languages out of the box. Today with Java SE 8 you can write your code in Java, but also use [other languages such as Scala, Groovy, Clojure or JRuby and Jython](https://docs.oracle.com/javase/8/docs/technotes/guides/vm/multiple-language-support.html). The JVM makes that happen. You can even develop extensions in JavaScript using modern frameworks such as [node.js](https://nodejs.org/en/) where projects like [nodyn](https://www.nodyn.io) come into place. When developing extensions for deegree you have the choice which language to use. And the deegree community will be pleased to guide you through the steps to incorporate extensions written in other languages than Java.
 
Microservices are another approach which got a lot of attention recently when discussing the development of cross-language applications - which means mixing different programming languages together. Main characteristics of a microservice architecture are decentralized governance and data management and most important design for failure. Synchronous calls are considered harmful and microservices take into account that a service call could fail due to unavailability of the remote service provider and the consuming client has to respond to this as tolerant as possible. The decentralized governance opens the door to use the right tool for the job. Regardless if you want to use node.js or C++, to build for example a fast and reliable map projection service, a tool such as [RabbitMQ](https://www.rabbitmq.com) provides the lightweight infrastructure to plug it into deegree. Or you use RESTish protocols to incorporate smart endpoints with a more coarse-grained communication structure compared to chatty RCP or SOAP calls. To transform the monolithic approach of deegree into a more microservice architectural style is a very challenging task and contributions from the community are welcome. And finally we don’t have to forget that deegree web services are running on every [Java EE 5 or higher compliant](https://www.oracle.com/java/technologies/java-ee-glance.html) application server such as [JBoss Wildfly](https://wildfly.org), [GlassFish](https://javaee.github.io/glassfish/), [Oracle WebLogic Server](https://www.oracle.com/middleware/technologies/weblogic.html) and still on the [Apache Tomcat](http://tomcat.apache.org) servlet container. Within the IT the Java Enterprise Edition (Java EE) platform has been adopted by millions of developers and companies providing business services in large-scale environments. As a geodata provider you can setup a technical infrastructure running multiple Tomcat or WebLogicServer instances within a cluster to meet demanding performance requirements.

Our goal is to get deegree ready for the enterprise and that it will meet the needs of data center provider and DevOps. And operations in the area of cloud computing is quite crucial. Support for cloud computing in Java EE was planned for version 7 but has been moved to Java EE 8 where we can expect the JCP experts group will publish the final draft for [JSR 366](https://jcp.org/en/jsr/detail?id=366) by the end of 2015. There are early implementations available such as a deegree tilestore to use storage back-ends such as [Apache Cassandra](http://cassandra.apache.org) to provide access to tiles stored in the cloud which can be served by [deegree’s OGC WMTS implementation](https://github.com/martin-vi/deegree-tilestore-cassandra). 

We are quite curious how and when this will be adopted by users and developers. We are looking forward to discuss further at one of the next user meetings or on our mailing list. 

---

_Update 2019-10-26:_
[Jakarta EE](https://jakarta.ee) is focused on enabling Open Source Cloud Native Java.