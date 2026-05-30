## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:2c78b52549115426dbd1545748f2d1eea947c6d1e87d8dc44b0a4687d818f66c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:618c3c68bcb73bc61d9bdb5c3346c9ec6dfb6eddd734bdfc7cd6eb0c492ac272
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **430.5 MB (430456524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db7650dc4c1f64f304969a5add881e6cec143f7ac8652b090ed09ed64d3e35a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:08 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:08 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:11:08 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 30 May 2026 02:14:14 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 30 May 2026 02:14:21 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 30 May 2026 02:14:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 30 May 2026 02:14:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 30 May 2026 02:14:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 30 May 2026 02:14:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 30 May 2026 02:14:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 30 May 2026 02:14:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 30 May 2026 02:14:21 GMT
ARG USER_HOME_DIR=/root
# Sat, 30 May 2026 02:14:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 30 May 2026 02:14:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 30 May 2026 02:14:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a8a811ccc5f505f502891437310aab6cf24318c64c71d122347978d3549c18b`  
		Last Modified: Sat, 30 May 2026 01:11:29 GMT  
		Size: 148.2 MB (148197690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874e1e14e5e638b1d999067ffdedbd8d0bcf5481343a3eb07907ca039d1c5b6`  
		Last Modified: Sat, 30 May 2026 02:14:49 GMT  
		Size: 179.9 MB (179885616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bbb0d334b363ae9e9440db765b9ab1ea3339c07f0b12bb7056f3a146995bf31`  
		Last Modified: Sat, 30 May 2026 02:14:45 GMT  
		Size: 30.1 MB (30070281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c765d6f5ae646694f2561fc8ec711fc2fd148fdab17045539d708a680a77d1b`  
		Last Modified: Sat, 30 May 2026 02:14:44 GMT  
		Size: 9.4 MB (9359975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd5c4d4831a83185e9e8e47904a99aa547a6eebdc1a0ff2ff912cbaa65b121a1`  
		Last Modified: Sat, 30 May 2026 02:14:43 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c7a778582d3566c0bf64fadc8adc677023a656846765e6381762115bfd4cdea`  
		Last Modified: Sat, 30 May 2026 02:14:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:9e52d641d0b3f13e07fc9206291509d4e0f0781eee856abe1dcdd483e298a2df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6955854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e75c9a47534e3d356097ad95e0cab84d019002e45ca4a26da7c1630c23fe372`

```dockerfile
```

-	Layers:
	-	`sha256:cf7d578764a02d0658bc2d1e2c6129019faaa11770ed3a9ce1271da692b0d4a6`  
		Last Modified: Sat, 30 May 2026 02:14:44 GMT  
		Size: 6.9 MB (6939658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbdc2e81eff5c2b3704ce2f7d0a938da1afb86beb8165822c81c8582f7c0a8f2`  
		Last Modified: Sat, 30 May 2026 02:14:43 GMT  
		Size: 16.2 KB (16196 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:039764e42c089d06bc5b4230dd1c6151ddf5b348db546a49d21574965399046d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.2 MB (406192472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c6673fd2980802d2ee5c00771de9ea75e1a8bd50a856e3c3ecb47c3d8d82a8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:16 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:16 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:11:16 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 30 May 2026 02:13:56 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 30 May 2026 02:14:04 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 30 May 2026 02:14:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 30 May 2026 02:14:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 30 May 2026 02:14:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 30 May 2026 02:14:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 30 May 2026 02:14:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 30 May 2026 02:14:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 30 May 2026 02:14:04 GMT
ARG USER_HOME_DIR=/root
# Sat, 30 May 2026 02:14:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 30 May 2026 02:14:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 30 May 2026 02:14:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d707445c7950dfdc5fa79967c81ddc7d73770f2577e23a9b177a71ad082a73`  
		Last Modified: Sat, 30 May 2026 01:11:37 GMT  
		Size: 145.4 MB (145374459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e491c50dbff3d22895cc96528b4187b391fc17cc7116b486794f814e580193ae`  
		Last Modified: Sat, 30 May 2026 02:14:35 GMT  
		Size: 155.5 MB (155461755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83190ce93ce9b3fa540cd952234a45c6819c83333ae5660483dc9e720f18363`  
		Last Modified: Sat, 30 May 2026 02:14:30 GMT  
		Size: 31.2 MB (31204565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ce6d50072bfa79376a87dc6941cc7dd90ea7187e8722de98e8e2729e1928761`  
		Last Modified: Sat, 30 May 2026 02:14:29 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cac6a99338660bbf6d7d67d56c1438daf8d922e2cd9884d53828b39f93d784f`  
		Last Modified: Sat, 30 May 2026 02:14:29 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53f4a15c3a08bc7071b539a7648b61247de9aa9992994dda1eda8209800cfecb`  
		Last Modified: Sat, 30 May 2026 02:14:30 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:2cf3f7539e72c02aed1391e365403d69c2bb0870e772ef6c15f0640213bcda9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6954206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abba58ef429262ccf0d4130a2fdef639050f2a2661acfe5004f062fea3cd96d4`

```dockerfile
```

-	Layers:
	-	`sha256:514e7217452f6e7982d1076861d36ba105aa1d1fb6804f40c5ad5e9dd29c043b`  
		Last Modified: Sat, 30 May 2026 02:14:29 GMT  
		Size: 6.9 MB (6937862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1668ea28c7d4fff706357de773c5919783d7e99bce637b7c825d97df15147a93`  
		Last Modified: Sat, 30 May 2026 02:14:29 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
