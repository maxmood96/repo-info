## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:0fbfdef102229e1888b2043bd21c42dfdb783500158d8be1c2b376f04a1c4aa9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:16cc3056c16caff28db6391e901f0951884b407e43a375f7b1bbfa641f4a219c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.6 MB (339616544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49f39b0fa70aa88f75559f77f44f7d7c028faab3b595dc64f8397ad7fa985194`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_452.b09-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:553ed992015a76bd7bd2b975b84fb4bb8d9fd1cc5d7f3cc5814806bd014114d7`  
		Last Modified: Wed, 14 May 2025 22:47:15 GMT  
		Size: 62.8 MB (62759985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4b15b43a755f5b3489059fac24427c746a648e8f29c5e43a21de2fad777ab0`  
		Last Modified: Mon, 19 May 2025 23:36:48 GMT  
		Size: 75.6 MB (75627662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06a7ce1d02df0c7045e4217ed79482b3bfe7f43aa2ac04db4d12a2cfbe42961`  
		Last Modified: Tue, 03 Jun 2025 06:12:58 GMT  
		Size: 162.0 MB (161979971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2267e3b981b29c8849ec9d698c9439b01715cfbd8d817a9287d47aaa588ae6`  
		Last Modified: Tue, 03 Jun 2025 06:12:56 GMT  
		Size: 30.1 MB (30077446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696a456a98d7f2102abb746042f249920a0b7debe87cbcd85f79b1d39a56bdde`  
		Last Modified: Tue, 03 Jun 2025 06:12:56 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:772e3a0c77eefa98480b90545fa36d4aa6fc5417e0e7bd70805980482792fdf0`  
		Last Modified: Tue, 03 Jun 2025 06:12:56 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fe1118cbc3ebc8a6503dbcf2a29417502ffc226c324160e84c7b073645fcee`  
		Last Modified: Tue, 03 Jun 2025 06:12:56 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:dac31227088838e2cfa73b9afa366d8034532ebaeef777d67debb446b9911f25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6781140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66fa64fd3298eaba5410adaa6506983fed73c59f33b8be89f1ea4c8e75ff148`

```dockerfile
```

-	Layers:
	-	`sha256:a302ef4f7fb92e91bd10fefb6d2f4f2164c5b495454ea7ff11e9c6a4ddc768c8`  
		Last Modified: Tue, 03 Jun 2025 06:12:56 GMT  
		Size: 6.8 MB (6762923 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dcd28ae5ff40942343a6be30d1e53e54313ed088167ff05d706991ab7b769757`  
		Last Modified: Tue, 03 Jun 2025 06:12:55 GMT  
		Size: 18.2 KB (18217 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f331c20c58f0d8022ba2a5fee639aedb6492ac60adc654c5dcd91419fa21104f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301591883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ae65823a4fd4148a8b8fae043bb43bfc392bfaf1bbec6e0505954eecc94eba`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_452.b09-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_452.b09-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b914e688cac327114c45b9a58220765af260230389654eb4d8798d0a7d9676d`  
		Last Modified: Wed, 14 May 2025 22:47:33 GMT  
		Size: 64.6 MB (64607481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fb3b2712e189e0631ebe7dd80180ee04b03d459ad71401283a9ad0ad1561536`  
		Last Modified: Mon, 19 May 2025 23:46:58 GMT  
		Size: 59.7 MB (59669889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a7619bda2336bbcbb3d0f5a20acad0c5e4a8fded78f0a6009a21c6c2068e21`  
		Last Modified: Tue, 20 May 2025 00:55:31 GMT  
		Size: 137.0 MB (136952277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b48acd85df83b212f2f3a3dd970902e1b15f346537460e4d636939279a3af2c6`  
		Last Modified: Tue, 20 May 2025 00:55:28 GMT  
		Size: 31.2 MB (31190768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21163ad594f0c3016594b1617e8373ff7abd16fd9078902e489d3a3743c472c0`  
		Last Modified: Tue, 20 May 2025 00:55:28 GMT  
		Size: 9.2 MB (9170426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648c0b37f5e4d55aaa5b799e222e13a1f57e9d6d388c322def576a49580a5f99`  
		Last Modified: Tue, 20 May 2025 00:55:27 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1771b042d12c585fb0d88beedfeda0fedec4131f688816327a769fa77115f621`  
		Last Modified: Tue, 20 May 2025 00:55:28 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:f6ad40cc57a3457f73ddd062c587bcd83304ccc893ce5325359629a12840f590
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6758486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e2c6e09465c24b71363fa3cb45fd3621f1dc70a851f453e53053f19fd39b24c`

```dockerfile
```

-	Layers:
	-	`sha256:ede4808b5668feb6b998e71889640d66e68677d29a73f6c3ff713cac7d160f14`  
		Last Modified: Tue, 20 May 2025 00:55:28 GMT  
		Size: 6.7 MB (6740120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73992d3a785237ae352700e704838a66e56494548538822bd52f4679ec34e4b0`  
		Last Modified: Tue, 20 May 2025 00:55:27 GMT  
		Size: 18.4 KB (18366 bytes)  
		MIME: application/vnd.in-toto+json
