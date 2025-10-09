## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:21f42db114f5c7505a5e28cf257463dd656dfd31a4ddcdd5be56124741ba3062
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:7de5d6de96764e4111354186dc379e7d9a3b602f6e468db8ce9fd3faaef08b6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.9 MB (193931588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8189dea18a12e3eee2020128cc363be937417d422862621e4c7c8b2e2e807ca7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 19 Sep 2025 12:56:50 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 12:56:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 12:56:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6c1fe4088fbbb049c51655abeadbf9a8ffa173bf595c0ec46c4f3813dafcb7`  
		Last Modified: Wed, 08 Oct 2025 23:50:54 GMT  
		Size: 178.5 MB (178521094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4f2c9364c9d76f8775e73270279d134c229412ec139e9a429ed05693f9e2023`  
		Last Modified: Wed, 08 Oct 2025 23:51:14 GMT  
		Size: 2.4 MB (2364420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e749eb0fc447ab391fe3bb6e755682b3c717957e6ce7c505d977db8e872cd45`  
		Last Modified: Wed, 08 Oct 2025 23:51:15 GMT  
		Size: 9.2 MB (9242583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:926135f9182fd66795920470ea8ff225c58c759788e37df9be8fc6b6d87d0fbe`  
		Last Modified: Wed, 08 Oct 2025 23:51:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b672cf8b2fa298f6037d09d3913a33641b13fd505113782abb079050d2ea14d0`  
		Last Modified: Wed, 08 Oct 2025 23:51:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:dff79bf53d32ca281331f4108e51fd972238fc68f5509e104415cb03e02fc933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.4 KB (549437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09f08e7944caef78b492196a4b0aca39d8483876cd7bb4229e5602641a2a0ca2`

```dockerfile
```

-	Layers:
	-	`sha256:96973a87d5246ac308228d2c7eab7f40f0583de0ab41943b88b8e7f600b25966`  
		Last Modified: Thu, 09 Oct 2025 02:28:08 GMT  
		Size: 533.0 KB (533032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68337e0e571c952d16dd5eb64f90098a77741a55a55bd685f3951d0147867691`  
		Last Modified: Thu, 09 Oct 2025 02:28:09 GMT  
		Size: 16.4 KB (16405 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b59d461a93fc8da5c0fd280a4577dbe3a81617414aa85847e62ebe364f75c173
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.8 MB (191848841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d189ba28e3264d5787dae07065be373a62e40677b5799b15d1b786060fc9ed19`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Fri, 19 Sep 2025 12:56:50 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 19 Sep 2025 12:56:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 19 Sep 2025 12:56:50 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 19 Sep 2025 12:56:50 GMT
ARG USER_HOME_DIR=/root
# Fri, 19 Sep 2025 12:56:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 19 Sep 2025 12:56:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 19 Sep 2025 12:56:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bebaba7c9073910ccc58702f77f884b8d201987fef89ce731ab6e34711fcfb4`  
		Last Modified: Wed, 08 Oct 2025 23:18:02 GMT  
		Size: 176.1 MB (176070720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a51df314833373fdcf06a0982c3f8e2553dea20aa39c4afcc2247fb998afe45`  
		Last Modified: Wed, 08 Oct 2025 23:18:24 GMT  
		Size: 2.4 MB (2396438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2a95272217cf366fb2239e87efb617bb1339eaa3273ca19b51c54e1ef423092`  
		Last Modified: Wed, 08 Oct 2025 23:18:25 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eea1ee91c9f66b15de4e13919d66f8a5066014ffed7a384e460d49116693e0b`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac751962be3d3de17f82d670efb260b517c1483ff401b791ddb8ac93c4564d7`  
		Last Modified: Wed, 08 Oct 2025 23:18:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:01843de1f3921439b0df36abaf85262466d2f9c771fed2c3ce30bb8c720e2be0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **549.0 KB (548974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58a15ba176afaaa2ce82e29dfd672465f9e2bbc6ed7c4678d573c751204f74f0`

```dockerfile
```

-	Layers:
	-	`sha256:285111370a4739d340e0c7365e034312cc8e1b01f3b893afdee4a6355a451db7`  
		Last Modified: Thu, 09 Oct 2025 02:28:12 GMT  
		Size: 532.4 KB (532436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be939c65c5711f8bfbacd049b288fa4e0409b43ffc2d9d4447cab21a1058041b`  
		Last Modified: Thu, 09 Oct 2025 02:28:13 GMT  
		Size: 16.5 KB (16538 bytes)  
		MIME: application/vnd.in-toto+json
