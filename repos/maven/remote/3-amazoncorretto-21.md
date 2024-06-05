## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:f770cc92e91cc42f4fd54f8e26df3209e4fb296f4d0cd5937b972ae6a2d09c31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:9908a0dc9ab6d3e80b2a7978d1484c19cdd13b5b47612f137e7d034580d33cae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.8 MB (379802776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bdb4642b6fd52ab5bfc9bb4d0bcf368f9f81a3c9d396132cab94d8fe788e4c1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:25:31 GMT
COPY dir:5f2d6af17649be50804cc4384ca7f8357e947a564ca83834a31e4d94723f7f1e in / 
# Fri, 19 Apr 2024 22:25:31 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:59:55 GMT
ARG version=21.0.3.9-1
# Fri, 19 Apr 2024 23:00:20 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 19 Apr 2024 23:00:20 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 23:00:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0b2952a75473f303233bc1034d63689122b90aa8b8fd5ebd0dced887e1c294e9`  
		Last Modified: Thu, 18 Apr 2024 23:27:02 GMT  
		Size: 62.7 MB (62650735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8891881a7cbcc28dc7a1360887e304d5fa447d2587d82d06bf9645ce1b5a23c9`  
		Last Modified: Fri, 19 Apr 2024 23:12:01 GMT  
		Size: 165.7 MB (165687674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613f10e4017eec78a515837a815ca4cec3de11c19279b4b24461184ff0816314`  
		Last Modified: Tue, 28 May 2024 19:57:06 GMT  
		Size: 141.8 MB (141815424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9cb50c3452d80a0e34c1f29270406a327107e36569bb2a0616ecc6f860b7a0`  
		Last Modified: Tue, 28 May 2024 19:56:54 GMT  
		Size: 9.6 MB (9647563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6408917e79cf11ebd97b7dbe04c984c93eb1c8ab4ce97d80898c9ae9e4c5fbfe`  
		Last Modified: Tue, 28 May 2024 19:56:53 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8acc7eeecf0efb0ad425143d014d45d9af4732e88582dc5d458ede27d2982b9`  
		Last Modified: Tue, 28 May 2024 19:56:53 GMT  
		Size: 356.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d16a9ad8a24eae47086c253864c311e29e475b33ea28f6b9c9777ee1a67fdc3`  
		Last Modified: Tue, 28 May 2024 19:56:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a5527c26ba712f88fd6ff2df4195eefdba047c12fe1b12b48eb83049b468fc82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.6 MB (356600426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:495be33b0b179e787f75fa1de7d194bd5d11db6afb8973049b1ef918f2f12404`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:45 GMT
COPY dir:54a4dd5769afd28377236f84a352a69acfed2ec1d2811885dfafbd62355157a9 in / 
# Wed, 05 Jun 2024 00:47:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:36:03 GMT
ARG version=21.0.3.9-1
# Wed, 05 Jun 2024 02:36:22 GMT
# ARGS: version=21.0.3.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 05 Jun 2024 02:36:24 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:36:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1ef504af8f98d51ec83a2ad2c52ad8ffb1311ee414e6f9f779bc331d20d242c8`  
		Last Modified: Fri, 31 May 2024 00:52:55 GMT  
		Size: 64.6 MB (64575441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22eb46e585a9749ebf27644a669f43b430553a5e83c39e1f6219d51b8a62684a`  
		Last Modified: Wed, 05 Jun 2024 02:45:58 GMT  
		Size: 163.7 MB (163748486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c80d49d9fd679ebec9fb37a44bd287e2bdac6649f6d6c15795e23c80a67e3ff4`  
		Last Modified: Wed, 05 Jun 2024 03:19:49 GMT  
		Size: 118.6 MB (118627601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d72f4a233f2b018f4200eba690a459ca30140e88f752a9f228914673dc68a9c`  
		Last Modified: Wed, 05 Jun 2024 03:19:41 GMT  
		Size: 9.6 MB (9647515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7448df5c0c85a36f70bc5041fece2c1a44995a3325bb07d10d755e5b37cd5e08`  
		Last Modified: Wed, 05 Jun 2024 03:19:40 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac43bb5cd7903200c346fb72cc73f7321b8b2f72081b0c5cbd83d94d2322aa62`  
		Last Modified: Wed, 05 Jun 2024 03:19:40 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04af8726090645355a2a6d123af17a6db35e2e6db8459f0ddb5fa0a2913654bd`  
		Last Modified: Wed, 05 Jun 2024 03:19:40 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
