## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:bb1bb44af5eb43e19df640a32be96549d7978264f6216742a6253b8514d3dda7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:c5a8be7fdd65f5114a2cfc6e8ff6eb4e11b91385417597a870486818f6540765
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196466539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80c5dcf43d1d3daa558a853ee9888d6256a35c8dc597ad0b9aab5dc975642fb1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:16:05 GMT
ARG version=25.0.3.9.1
# Wed, 10 Jun 2026 20:16:05 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:16:05 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:16:05 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 10 Jun 2026 20:32:11 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 10 Jun 2026 20:32:11 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 10 Jun 2026 20:32:11 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:32:11 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:32:11 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 10 Jun 2026 20:32:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 10 Jun 2026 20:32:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 10 Jun 2026 20:32:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 10 Jun 2026 20:32:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 10 Jun 2026 20:32:11 GMT
ARG USER_HOME_DIR=/root
# Wed, 10 Jun 2026 20:32:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 10 Jun 2026 20:32:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 10 Jun 2026 20:32:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ce265cb26b20d8816a2ad0602632269a02258516905a827f2bae164e7d962f`  
		Last Modified: Wed, 10 Jun 2026 20:16:28 GMT  
		Size: 181.0 MB (181022287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c0c437cd508b7fe81c178bd19348e05439a2f80c441cfc68dc945dd510b5bfb`  
		Last Modified: Wed, 10 Jun 2026 20:32:20 GMT  
		Size: 2.2 MB (2216524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dbc8944e6dc860bd83013af8687293085e0e39facaea6b2a277015892d0b500`  
		Last Modified: Wed, 10 Jun 2026 20:32:20 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:054f861641ba8ebed5738b47d00be7572b80f4552d2f4683b60b1582fcdd8cd6`  
		Last Modified: Wed, 10 Jun 2026 20:32:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9fa7b8fe945fa6b9d9ce097858a4e15242f30a7b2ca5703c1a68d6100c860d`  
		Last Modified: Wed, 10 Jun 2026 20:32:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:c57be6db2c5694fda00e5acf2c36b23930237cb58906a46d51bd1335146703a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.0 KB (751951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ea6a51477b152fc56587a4cdd1dc9298868d5516bd93721ad3149881f34f3e4`

```dockerfile
```

-	Layers:
	-	`sha256:6006092c0921618cbed3d44fbd1b8a0b3d7256d116274711895b1a1303b9075a`  
		Last Modified: Wed, 10 Jun 2026 20:32:20 GMT  
		Size: 737.4 KB (737425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0dd5cbca9b5b2fc8186a8720908b9c24c39b9ec539c519a075adf8840206c0e`  
		Last Modified: Wed, 10 Jun 2026 20:32:19 GMT  
		Size: 14.5 KB (14526 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:1a435bdb1979d7f62d34644b0199c0439726fce5639058c6227338b380581347
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.5 MB (194456828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2a96a76d0ba8efbfa9910a29a57dbd474e7192e56893fd78509e082f00342e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:42 GMT
ARG version=25.0.3.9.1
# Wed, 10 Jun 2026 20:15:42 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:42 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Wed, 10 Jun 2026 20:32:15 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Wed, 10 Jun 2026 20:32:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 10 Jun 2026 20:32:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:32:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 10 Jun 2026 20:32:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 10 Jun 2026 20:32:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 10 Jun 2026 20:32:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 10 Jun 2026 20:32:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 10 Jun 2026 20:32:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 10 Jun 2026 20:32:15 GMT
ARG USER_HOME_DIR=/root
# Wed, 10 Jun 2026 20:32:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 10 Jun 2026 20:32:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 10 Jun 2026 20:32:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d33b730143411dce15bf64440e97c83cf93ed7493459fab653be6afcf61dbb46`  
		Last Modified: Wed, 10 Jun 2026 20:16:04 GMT  
		Size: 178.6 MB (178637638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df81745df3011264473ca4c4500659f611feb5c258ddd24de8a57d4b2f3ccefb`  
		Last Modified: Wed, 10 Jun 2026 20:32:23 GMT  
		Size: 2.3 MB (2255879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741ba8f27e2c1ddc5e6213f312d58885cf19a279e2dad7869b758f54d654d9aa`  
		Last Modified: Wed, 10 Jun 2026 20:32:24 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cc9acd0a71e0c3b6c983369fb956be980a9700be1d0c5c47f87842d6e24dc11`  
		Last Modified: Wed, 10 Jun 2026 20:32:23 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdd8571a775a2c73d108d5064aa645b009e566f626230566eb8740447bdfaf60`  
		Last Modified: Wed, 10 Jun 2026 20:32:23 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:ba39a0af2cd33aca81a413353c4005f98536f65576be637dcec242b6e4c1e936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **750.8 KB (750838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc8569a4e30d62e19ea0508429f47cbd679bf690a71df3abef80a201dfadb8af`

```dockerfile
```

-	Layers:
	-	`sha256:fe33dceb7bc4deca4aebf46076f0d395b918b17ead2a4ebe8c25b02f35bd6f76`  
		Last Modified: Wed, 10 Jun 2026 20:32:23 GMT  
		Size: 736.2 KB (736179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bec1d74117574dfaade5ddef2e4e376897c38c460a9ebb99f8923cab7dced52`  
		Last Modified: Wed, 10 Jun 2026 20:32:23 GMT  
		Size: 14.7 KB (14659 bytes)  
		MIME: application/vnd.in-toto+json
