## `maven:3-amazoncorretto-11-alpine`

```console
$ docker pull maven@sha256:31bf5284ebe617203a414716c17b5235730a2d09b7b233c32bccd830c545f29c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:8966bcca4c0befac6c4825b28b68c449f6f3357bca08f401002fbf99baf51d3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.2 MB (159181210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe34d43696130e006600cdfe3c5292aa8971c081910d69ba70ed5e7bdcf4a69a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:46:21 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:46:21 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:46:21 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:46:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:46:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 17 Feb 2026 22:29:08 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 17 Feb 2026 22:29:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:29:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:29:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:29:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:29:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:29:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:29:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:29:08 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:29:08 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:29:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:29:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:29:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d986d7e858d6100508f42bc906b71c57de3eadb7c1b125079ed3f059f3f83221`  
		Last Modified: Wed, 28 Jan 2026 02:46:38 GMT  
		Size: 143.6 MB (143585877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5f49ab0d9d190ef10e4375c8ba83eb54ed5348d06454cd1be9db16710863d76`  
		Last Modified: Tue, 17 Feb 2026 22:29:16 GMT  
		Size: 2.4 MB (2420240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a9862abba18371078521a81ea1dddd8ac87f0ded32991d4d16b1c26c2aab9d4`  
		Last Modified: Tue, 17 Feb 2026 22:29:16 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b685e50e01cd293cb3967966b9bad218645687f75e2e6400ac05f89574d4671e`  
		Last Modified: Tue, 17 Feb 2026 22:29:16 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43d9d656b3020b19c46f74375ec8dad271de9f8c18a6384cc3c56aba6d1913a`  
		Last Modified: Tue, 17 Feb 2026 22:29:16 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:7633ca6059058501f451441da4b098b722b0855f6a9a01fb5ff7a9907d9a58ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.9 KB (749878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9555c759e532b3b7bb041c58db7a112065cb2ce72d0876405b26e487bbad8b0d`

```dockerfile
```

-	Layers:
	-	`sha256:85e80d2a25eb8e449f601750562e1320c5455659a560a641ae9dd6477ab7ca38`  
		Last Modified: Tue, 17 Feb 2026 22:29:16 GMT  
		Size: 733.5 KB (733516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8902f107e96de0688b92884e459f71bf85cecea64b0f65d915f285bbf97fa9fe`  
		Last Modified: Tue, 17 Feb 2026 22:29:16 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4cdfd783c18b4d2300f375916caafdf36d2ba5f1bcbff8170ab4cae9b92c7202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.8 MB (157827453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5057e68685968103751b6ec34bcf99c5f005dec3f6914e07369ad15767e4fd73`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:47:01 GMT
ARG version=11.0.30.7.1
# Wed, 28 Jan 2026 02:47:01 GMT
# ARGS: version=11.0.30.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:47:01 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:47:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:47:01 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 17 Feb 2026 22:17:22 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 17 Feb 2026 22:17:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:17:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:17:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:17:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:17:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:17:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:17:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:17:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:17:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:17:23 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:17:23 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:17:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:17:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:17:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d552dd13d8c7000c34c67e3db376e66141f2a096e4c79b9abd594731ea071a2d`  
		Last Modified: Wed, 28 Jan 2026 02:47:19 GMT  
		Size: 141.9 MB (141855734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fdb419b14066de538044a199a140be36a53df745a48daba9ad4c3c6b354e908`  
		Last Modified: Tue, 17 Feb 2026 22:17:30 GMT  
		Size: 2.5 MB (2461345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d28def2fc70814503577d4db4ec7aca67d1aa884e343bc147b7be127c8566ea0`  
		Last Modified: Tue, 17 Feb 2026 22:17:31 GMT  
		Size: 9.3 MB (9312242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a4d9b189450788c66209553c2c7d59cf51cb307ff2548d18d390f3f5ba8f82`  
		Last Modified: Tue, 17 Feb 2026 22:17:30 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eda6a4575c3a890546553df93aa5c376c01d0183c1154324ebf94b088f660cac`  
		Last Modified: Tue, 17 Feb 2026 22:17:30 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:2713da94bfeacd677e41698999cb63a3c39d73f6797dfc04d8d13fb31ec73dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **749.4 KB (749405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:400627a1c30e05ae0bb278b2aef9caceeff8896e454e1dc9ba6bbb4b4bb7ac8c`

```dockerfile
```

-	Layers:
	-	`sha256:c3ccea8f57bbdde195a3361339a57bf8bf4de442cfd9c0c620435feb6c9e843d`  
		Last Modified: Tue, 17 Feb 2026 22:17:30 GMT  
		Size: 732.9 KB (732910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b4689efeaf4c4a18350684aa215ed2e70ec5ebf8d290047ba878fb149041d28`  
		Last Modified: Tue, 17 Feb 2026 22:17:30 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
