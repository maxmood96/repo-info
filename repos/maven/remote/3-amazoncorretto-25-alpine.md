## `maven:3-amazoncorretto-25-alpine`

```console
$ docker pull maven@sha256:0437187207c8466d4efb733230acc67b7de72f702dbcd89500c843018d887072
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-alpine` - linux; amd64

```console
$ docker pull maven@sha256:e45b7c80e634c184692a54c202a2ea594cac2d0171055ed8efa276e49cd10d4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196354753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1af4f23e8b3cb7817fea95607a5c4bf81a70aa844380130b03e5041cc6c6fb61`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:52:59 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:52:59 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:52:59 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:52:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:52:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 17 Feb 2026 22:29:50 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 17 Feb 2026 22:29:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:29:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:29:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:29:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:29:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:29:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:29:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:29:50 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:29:50 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:29:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:29:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:29:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce024e0c1fc281f3f61f3cf3a1e72dcd0c8f1a01d7b36ccd799f9d0d0de6c041`  
		Last Modified: Wed, 28 Jan 2026 02:53:20 GMT  
		Size: 180.8 MB (180759289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12cf08ba7ac054b0351f3623bf0423193e4c0ea2a4cdebbb652ae2af9156a477`  
		Last Modified: Tue, 17 Feb 2026 22:29:58 GMT  
		Size: 2.4 MB (2420371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fae0109e43d747e78d4d5c76eb1899ab06fc56f8ee2f3ed3b91e885f933b166`  
		Last Modified: Tue, 17 Feb 2026 22:29:58 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43bf87418f556cdc62a103859f4f91c76f526891762c9752cf239eaf39218a5e`  
		Last Modified: Tue, 17 Feb 2026 22:29:58 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d873f5b2032ec43a8383a31e559bc0d38ad592a38f6e17741edbd9c1977a44`  
		Last Modified: Tue, 17 Feb 2026 22:29:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:e792398016c6118653f3b1b87448b8851491d6d4938bb4baa266cf7362938936
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **753.1 KB (753089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36b153def9271a9d3802f6fb3af71499927cef0ba60668b247d7c769aa50f7b`

```dockerfile
```

-	Layers:
	-	`sha256:f08ea1fcf112cb2b6560abb9bb42dd992851e84ecd400ffd50a0729d147353cd`  
		Last Modified: Tue, 17 Feb 2026 22:29:58 GMT  
		Size: 736.7 KB (736727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0783dc091864a4745a37be47b23242a8033a0605b38f79bdda050519ce0502f8`  
		Last Modified: Tue, 17 Feb 2026 22:29:58 GMT  
		Size: 16.4 KB (16362 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-alpine` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:73a68a8cf3ab71704eeac2c62013b5dbf45a4641dcf25a493da519a7d0961875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194384394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6506aec00a500b5650a25a7722f8f6fb162ecc8f41105b1a6a47ff1928fbfdc1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:54:31 GMT
ARG version=25.0.2.10.1
# Wed, 28 Jan 2026 02:54:31 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:54:31 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:54:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Jan 2026 02:54:31 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
# Tue, 17 Feb 2026 22:18:22 GMT
RUN apk add --no-cache bash openssh-client # buildkit
# Tue, 17 Feb 2026 22:18:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:18:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:18:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:18:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:18:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:18:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:18:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:18:22 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:18:22 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:18:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:18:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:18:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea00285b52f6f6c9e088cd08bc54a41499c353ac64712efcaf2aff682f021f1a`  
		Last Modified: Wed, 28 Jan 2026 02:54:52 GMT  
		Size: 178.4 MB (178412260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:418da885ed33ad3e5c43925fcd21a3ab258c0158f930c111c08664e08899fdb2`  
		Last Modified: Tue, 17 Feb 2026 22:18:30 GMT  
		Size: 2.5 MB (2461756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3415508c92d5acf6932fc2a5761bf1bbbd34221869427f1de73fcf6b16659b`  
		Last Modified: Tue, 17 Feb 2026 22:18:30 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef5869b44473dca4e1aa48a72e1acf8b71c9ab2d7a1e8d39b93ff65bfe67537`  
		Last Modified: Tue, 17 Feb 2026 22:18:30 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c54e3b1490dee9bf7e391a659e3f04fa53d9b733e5e7a9baae56a352f91df016`  
		Last Modified: Tue, 17 Feb 2026 22:18:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:d26bc0c218dc7e9d86f88115361840a3a2ee02020af35e5c764f1a10f4731d56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **752.0 KB (751975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:675679e9a61ec6a61243496ff8819a821a282f85db22d3d3fd6b24fae1847dbe`

```dockerfile
```

-	Layers:
	-	`sha256:b16b8e5f6f60ca7ab9cadc93fa8c1e8c93c1774157985486481bbdb0b8831708`  
		Last Modified: Tue, 17 Feb 2026 22:18:30 GMT  
		Size: 735.5 KB (735481 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8162045b79a0874f5a812c0e9a57ef7439f72f967219db34c6d84536b441816f`  
		Last Modified: Tue, 17 Feb 2026 22:18:30 GMT  
		Size: 16.5 KB (16494 bytes)  
		MIME: application/vnd.in-toto+json
