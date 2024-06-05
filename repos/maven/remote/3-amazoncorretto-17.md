## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:14f9912d91bba3f39d851c584a7736109be59a247604bce62c2223b61a253c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:359818baa99c1a5966140b70f7714daa829f4d513df2a80fee2591f8131958e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.3 MB (366275207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a95387755d1a94216dbe33e8ee87f0516755cde4ecfed497f71d8dbfc8124746`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:25:31 GMT
COPY dir:5f2d6af17649be50804cc4384ca7f8357e947a564ca83834a31e4d94723f7f1e in / 
# Fri, 19 Apr 2024 22:25:31 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:55:54 GMT
ARG version=17.0.11.9-1
# Fri, 19 Apr 2024 22:56:19 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Fri, 19 Apr 2024 22:56:19 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:56:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:82163d7b5f2d8ac14bdb2c95cce6c8fba25243f2db1436397cdf263ab324652b`  
		Last Modified: Fri, 19 Apr 2024 23:09:24 GMT  
		Size: 152.2 MB (152169653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15edb4f9462a356852c65c28558b53c2e33e22dc3bcf959fb11d750f7e65d916`  
		Last Modified: Tue, 28 May 2024 19:55:56 GMT  
		Size: 141.8 MB (141805875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192e7aeb7ebdbc64bcdb2d6e204ef813b431f9e4a2d489fbfca616de2386c942`  
		Last Modified: Tue, 28 May 2024 19:55:43 GMT  
		Size: 9.6 MB (9647564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7634a5d8eedb640f33bf2d2d36d84797469f76f959064ce95319f9afadec79c`  
		Last Modified: Tue, 28 May 2024 19:55:43 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cadd5e2dd608a1ee7f6d9544655cc50a1d308232e95b815dbb31e8c6025fa36`  
		Last Modified: Tue, 28 May 2024 19:55:42 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15de656dd5b79b757d84ac65e030e2437f8db049f3c7b6e4688804fc69d07806`  
		Last Modified: Tue, 28 May 2024 19:55:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9760ba51ea4988b864a266a22d87830bb85ed2efb27b6b4ec1f3deb4d549df30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343648714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ac35b1aeb4912defefda2dd869535728d032b771a7a567b0723e1dd86bf232`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:45 GMT
COPY dir:54a4dd5769afd28377236f84a352a69acfed2ec1d2811885dfafbd62355157a9 in / 
# Wed, 05 Jun 2024 00:47:46 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:33:01 GMT
ARG version=17.0.11.9-1
# Wed, 05 Jun 2024 02:33:19 GMT
# ARGS: version=17.0.11.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all
# Wed, 05 Jun 2024 02:33:21 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:33:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:5ab3c637a564c65c75ae813e2f950aa58a12afb7e860d4acd055a45c8698317c`  
		Last Modified: Wed, 05 Jun 2024 02:43:45 GMT  
		Size: 150.8 MB (150797207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52682081cf6337da10d634e79844ad75cb7b235418357c3071c7402f9906218c`  
		Last Modified: Wed, 05 Jun 2024 03:19:16 GMT  
		Size: 118.6 MB (118627145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:866094b35d93407e465dcce3b29fa544bf82ea7f3eec31b803adde31d22ef649`  
		Last Modified: Wed, 05 Jun 2024 03:19:06 GMT  
		Size: 9.6 MB (9647532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63397777918ca262c0a0547b9b7f524f3fe01046d2b9d5e3db36f6cc57ef3cc8`  
		Last Modified: Wed, 05 Jun 2024 03:19:05 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2464f8af728182c69e399f03f9a6349a57d5fbafe3e3fa00971aea51167f713e`  
		Last Modified: Wed, 05 Jun 2024 03:19:05 GMT  
		Size: 363.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7f316ff9af25050793e8576793f5696af417d6a56598aa872ba0a73f82587a`  
		Last Modified: Wed, 05 Jun 2024 03:19:05 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
