## `maven:3-amazoncorretto-17-alpine`

```console
$ docker pull maven@sha256:ae0008f1d11ff74bbf39ec9de3e5d84b2ff3a671bf9594dd1270d049e0009deb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-alpine` - linux; amd64

```console
$ docker pull maven@sha256:0d5d5733299eea7978eb7540c60e9c15d053b3fd45f075a74cfcb8f88295b010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (163962713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea7f56bc8a89c127052fc3d51550ba155beca6c6166df7105f4a1fc1a7f99b35`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:32:59 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:32:59 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:32:59 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:32:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 05 Feb 2026 23:29:47 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Thu, 05 Feb 2026 23:29:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:29:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:29:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:29:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:29:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:29:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:29:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:29:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:29:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:29:48 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:29:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:29:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:29:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:29:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed6290ed2724dad5b9d68e62935d09eb0e1dbd86d11cc766d6d0c81d0e3a60fe`  
		Last Modified: Thu, 29 Jan 2026 21:33:15 GMT  
		Size: 148.4 MB (148367541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f7980e7535e81ae728eb0839dfcaa27a0195b77cac99bee596d4da081426f37`  
		Last Modified: Thu, 05 Feb 2026 23:29:55 GMT  
		Size: 2.4 MB (2420060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc3c50072f82de070c2e6a2fdbb40cc728965519693af6348e706c12a267a4d3`  
		Last Modified: Thu, 05 Feb 2026 23:29:55 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393f30dc2977256adf063d0d91eedc2417526f93c55f99bc40419a097f7273ac`  
		Last Modified: Thu, 05 Feb 2026 23:29:55 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ba29a5b5ef170a96176c7994398dabed35a66336ceb33e407de67484ef5db1`  
		Last Modified: Thu, 05 Feb 2026 23:29:55 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:e993e835fd0692ce54c60fa374a55ed58f11154dfb9eb64098732ce7090668db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **744.1 KB (744086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f1d5f590dbfec1868703d31d88eeae98415b4be3c0f400db25f44027913d69e`

```dockerfile
```

-	Layers:
	-	`sha256:b48bb9192ca7c61d984860959b9abef8e4c382742a5be6d34b280409e5271361`  
		Last Modified: Thu, 05 Feb 2026 23:29:55 GMT  
		Size: 727.7 KB (727724 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbb4f00edf168555459b88cf5f20b0dede9d4ca6a752fca61282c3e14f63c4a1`  
		Last Modified: Thu, 05 Feb 2026 23:29:55 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7b3e30a66a06851604150442f92b6400f442f2fe96939415bf07366130b3925d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.7 MB (162683766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5877ffa0ab659f072865c4f3f8a1c0abbcc6c321784cc519bd8e7fc79f00a3b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Thu, 29 Jan 2026 21:32:51 GMT
ARG version=17.0.18.9.1
# Thu, 29 Jan 2026 21:32:51 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 29 Jan 2026 21:32:51 GMT
ENV LANG=C.UTF-8
# Thu, 29 Jan 2026 21:32:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 29 Jan 2026 21:32:51 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Thu, 05 Feb 2026 23:40:45 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Thu, 05 Feb 2026 23:40:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:40:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:40:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:40:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:40:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:40:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:40:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:40:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:40:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:40:45 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:40:45 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:40:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:40:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:40:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0a1b2b27fdd6627a7a5ca56c15c20d0c298fbaa72189065a764f30f5dd81e08`  
		Last Modified: Thu, 29 Jan 2026 21:33:10 GMT  
		Size: 146.7 MB (146712279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:720dea2b787563c74a3c562d3b6364623ba8baf2304f3968f9166de5aeb06a9a`  
		Last Modified: Thu, 05 Feb 2026 23:40:53 GMT  
		Size: 2.5 MB (2461118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb7ef5d4f640bfcdce04380b089af618b95b18ddb3c6827ee2fd9ebbc047b11`  
		Last Modified: Thu, 05 Feb 2026 23:40:53 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b20ffe602e10589d1f82459fc87bb3c1628e37f5f953bdf49377a8848ea92873`  
		Last Modified: Thu, 05 Feb 2026 23:40:53 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36001c064299b1261c14beccd49dd2b23442d5db5b73b80bbcebd8ccca83d000`  
		Last Modified: Thu, 05 Feb 2026 23:40:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:ceb1385137f2f770dc4b267c6d60dfda0b0a0b6c9197f5673253f3da4923f891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **743.0 KB (742976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61e692c5f10dc050e6e401389e3105bef7ec75d320269a10b43cdf60677e9423`

```dockerfile
```

-	Layers:
	-	`sha256:cc459f8e9a3101840eb66d592c61371e3beb6c9c303ed955a1f6bdc6e1db6423`  
		Last Modified: Thu, 05 Feb 2026 23:40:53 GMT  
		Size: 726.5 KB (726481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54af11bd02eafec7afc55cc7a8fe04a0bd3720da8d4f563d1552e053f0e3a33a`  
		Last Modified: Thu, 05 Feb 2026 23:40:53 GMT  
		Size: 16.5 KB (16495 bytes)  
		MIME: application/vnd.in-toto+json
