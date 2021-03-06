## JBoss Fuse Docker container

90-days trial JBoss Fuse Docker Image


## Docker container for newly released JBoss Fuse ESB server

This container installs on first start-up following features:

* JBoss Fuse 6.3.0 integration on JBoss EAP 6.4.0
* JBoss Fuse 6.3.0 over Apache Karaf


Available Docker image versions :

* JBoss Fuse 6.3.0 Docker LATEST ([latest/Dockerfile](https://github.com/fabriziotorelli-wipro/docker-jboss-fuse/tree/master/Dockerfile))
* JBoss Fuse 6.3.0 Docker ([3.6.0/Dockerfile](https://github.com/fabriziotorelli-wipro/docker-jboss-fuse/tree/6.3.0/Dockerfile))


Source Repositories :

* [docker-jboss-fuse](https://github.com/fabriziotorelli-wipro/docker-jboss-fuse)


Docker Hub :

* [jboss-fuse docker-hub page](https://hub.docker.com/r/builditftorelli/jboss-fuse/)


### Goals

This project realises a sample 90-days trial version of JBoss Fuse 6.3.0, in order to evaluate one of latest ReadHat eficient ESB server based on osgi and Apache Camel technologies. This project define a StandAlone environment for test purposes only.

*Caution* : No warranties are extended to production or business use of this container, and we are not responsible for illegal or inappropriate use of this project outcomes or any damage on business or digital crime, derived for third-parties use of provided artefacts.


### Our Philosophy

`Try it. Determine business value, derived from product features. Then you consider to buy a license and/or implement a production-ready docker image, accordingly to Product Provider trading or commercial rules.`

*Assumptions* : All our docker images are continuous delivery process ready, and all of them have been tested on `Kubernetes`, `MESOS`, `Portainer.IO`, `Rancher` and `Spinnaker` delivery frameworks, before we released on Docker Hub.


### About JBoss Fuse

Here a list of RehHat related pages :

* [Homepage](https://www.redhat.com/en/technologies/jboss-middleware/fuse)

* [Getting Started](https://access.redhat.com/documentation/en/red-hat-jboss-fuse/?version=6.3)


### Docker Environment

Docker container exposes following ports:

* `8009` :

JBoss EAP 6.4.0 AJP port

* `8080` :

JBoss EAP 6.4.0 HTTP port

* `8181` :

JBoss Fuse 6.3.0 HTTP port

* `8101` :

JBoss Fuse 6.3.0 JMX port

* `9990` :

JBoss EAP 6.4.0 Management HTTP port

* `9443` :

JBoss EAP 6.4.0 Management HTTPS port

* `9999` :

JBoss EAP 6.4.0 Management Native port

* `4447` :

JBoss EAP 6.4.0 Remoting port

* `8443` :

JBoss EAP 6.4.0 Management HTTPS port

* `4712` :

JBoss EAP 6.4.0 Transaction Recovery Environment port

* `4713` :

JBoss EAP 6.4.0 Transaction Status Manager port


Docker container exposes following volumes:

*No exposed valume for this docker image*



Docker container defines following environment variables:

*No defined environment variables for this docker image*


### Build Docker image

In order to build this docker image, in project root, you can use following command :

```bash
docker build --rm --force-rm --tag jboss-fuse:6.3.0 .
```

Or you can simply dowload the Docker hub built one, using following command :

```bash
docker pull hellgate75/jboss-fuse:6.3.0
```


### Execute Docker image

In order to execute this docker image, after you have built it with docker, you can use following command :

```bash
docker run -d --name jboss-fuse-6.3.0 -p 8009:8009 -p 8080:8080 -p 9999:9999 -p 9990:9990 -p 9443:9443 -p 4447:4447 -p 8443:8443 \
            -p 4712:4712 -p 4713:4713 -p 8181:8181 -p 8101:8101 jboss-fuse:6.3.0
```

In order to execute Docker Hub image, without any prior docker build, you can use following command :

```bash
docker run -d --name jboss-fuse-6.3.0 -p 8009:8009 -p 8080:8080 -p 9999:9999 -p 9990:9990 -p 9443:9443 -p 4447:4447 -p 8443:8443 \
            -p 4712:4712 -p 4713:4713 -p 8181:8181 -p 8101:8101 hellgate75/jboss-fuse:6.3.0
```


### Access Docker container features

In order to access docker container shell, after container ran, you can use following command :

```bash
docker exec -it jboss-fuse-6.3.0 bash
```

When you login to container you will display service health information and console access urls


In access to JBoss Fuse 6.3.0 management web console you can type on your browser following address:

```bash
http://[ container-ip or localhost ]:8181/
```

Web Console credentials in current sampler are : admin/P4$$w0rd123


In access to JBoss EAP 6.4.0 management web console you can type on your browser following address:

```bash
http://[ container-ip or localhost ]:9990/
```

Web Console credentials in current sampler are : admin/P4$$w0rd123


### Issues

Please report any issue on project Issue Tracker at :

[docker-jboss-fuse Issue Tracker](https://github.com/fabriziotorelli-wipro/docker-jboss-fuse/issues)


### License

Copyright (c) 2016-2017 [BuildIt, Inc.](http://buildit.digital)

Licensed under the [MIT](https://github.com/fabriziotorelli-wipro/docker-jboss-fuse/tree/master/LICENSE) License (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
