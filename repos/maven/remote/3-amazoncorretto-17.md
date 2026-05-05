## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:1eee59f4b432adb263fe414c95122ea5776161b6dfd53983f19a038dcfefc70e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:c3e27f11cf24d8ff3f1ab857b948ed0be25dcdeb6aff5a6b58b14534fe811257
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **431.8 MB (431836675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b61cba18bc31a4fcbdd760c41f4b1e3fda137dc2834bc179d4fe38ef4fd93a7b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:24 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:24 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:11:24 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 04 May 2026 20:44:13 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 04 May 2026 20:44:21 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 04 May 2026 20:44:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 04 May 2026 20:44:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 04 May 2026 20:44:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 04 May 2026 20:44:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 04 May 2026 20:44:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 04 May 2026 20:44:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 04 May 2026 20:44:22 GMT
ARG USER_HOME_DIR=/root
# Mon, 04 May 2026 20:44:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 04 May 2026 20:44:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 04 May 2026 20:44:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:032cabcbac193a16c2253875c88ae2e3f74dab118518bde463f31531ad16461d`  
		Last Modified: Mon, 04 May 2026 20:11:45 GMT  
		Size: 152.6 MB (152609646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20496db3195fed1ae5648055e0648aba3994ffcd4067022d9dfc5f2b3d0231e3`  
		Last Modified: Mon, 04 May 2026 20:44:50 GMT  
		Size: 177.0 MB (176970475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a75d7395aa78146fa1ded11a7665c999c7701ea8907367f905f2db0618fad3a`  
		Last Modified: Mon, 04 May 2026 20:44:47 GMT  
		Size: 30.1 MB (30083333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:079254656c07798e3f4d66e9e970ebd5f2065f8f5d91c76f8f668e22ac6fffac`  
		Last Modified: Mon, 04 May 2026 20:44:46 GMT  
		Size: 9.3 MB (9312203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:394c1dd4027678fd96675a84327661a2ed0cb181c3ed3a219c28dcefbdff41c7`  
		Last Modified: Mon, 04 May 2026 20:44:45 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28e2cae2974e044d480e5fea3b975776b51e7f50d1f7935b608c905881fcbb1b`  
		Last Modified: Mon, 04 May 2026 20:44:47 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:482702d31a1adbd39e27048cd6568f3fc27d3bafe7298ce11ad701c2465a0006
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e3d0228ba206829aaaf268a0ef621996a63160f97af52b7fc466b3e2abb7440`

```dockerfile
```

-	Layers:
	-	`sha256:c14c65dca6ec541176013bd19329ccd03e2f6db588750967c42ac114bb1c46f6`  
		Last Modified: Mon, 04 May 2026 20:44:46 GMT  
		Size: 6.9 MB (6933162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c26701efbdc46b60a5195fb9c64bf3e02dca97ca3c4068cc1751319cb0c517a`  
		Last Modified: Mon, 04 May 2026 20:44:45 GMT  
		Size: 16.2 KB (16196 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0a51d238aea5ac34a5d4ecc8f724dbb0c60319ab8da3300fc63be675cd0f5991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.2 MB (409158020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4c7b1370657830e071b391ff8f2c7cc83807a0a40fb6a84a67b8d724098a648`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:41 GMT
ARG version=17.0.19.10-1
# Mon, 04 May 2026 20:11:41 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:11:41 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 04 May 2026 20:44:33 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 04 May 2026 20:44:39 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 04 May 2026 20:44:40 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 04 May 2026 20:44:40 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:40 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:40 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 04 May 2026 20:44:40 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 04 May 2026 20:44:40 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 04 May 2026 20:44:40 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 04 May 2026 20:44:40 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 04 May 2026 20:44:40 GMT
ARG USER_HOME_DIR=/root
# Mon, 04 May 2026 20:44:40 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 04 May 2026 20:44:40 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 04 May 2026 20:44:40 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da04cd62a6e78a94f951948f9a5bd7a651c4178ddc92f9efa3473eab2c4fdbe9`  
		Last Modified: Mon, 04 May 2026 20:12:03 GMT  
		Size: 151.3 MB (151316746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db49d8e1a4fbfebea51eef6dbb4bcfd1c3a4127dc4510aaa7682d985fbd92720`  
		Last Modified: Mon, 04 May 2026 20:45:08 GMT  
		Size: 152.5 MB (152526130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750aa895ec897fbea0e0fa730d13223b14450914db1319de3c88e287c37f3d91`  
		Last Modified: Mon, 04 May 2026 20:45:05 GMT  
		Size: 31.2 MB (31206346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4b9819511884000df79ec1c1db1635397e180f0826b61010c53500ac8fb27bc`  
		Last Modified: Mon, 04 May 2026 20:45:04 GMT  
		Size: 9.3 MB (9312257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193bde4e7a7f884637cc5e03bbb8256adec58f5643e42a84f73931d961ab7b9b`  
		Last Modified: Mon, 04 May 2026 20:45:04 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5480f1755eb1ef402bad3da378ac51c700eb6ffd44bc62a066569d68d7fdebaf`  
		Last Modified: Mon, 04 May 2026 20:45:05 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:27a11837cf6cc2a5f776e75714e48e6bbffb6e48fcda1a4be1156d03d8a954a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d19c71ca77d8c3d90e19a2a990d419a3593bada5559535f0309a838aa14749`

```dockerfile
```

-	Layers:
	-	`sha256:224dc82457869a5a39e8fb881474b3a7b5ac755a0352a455bee71c95c3317bfb`  
		Last Modified: Mon, 04 May 2026 20:45:04 GMT  
		Size: 6.9 MB (6930561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:550b639e5a79cee4169cfaa0a00d35559776330a50f5f092f8d40cb5dab198bb`  
		Last Modified: Mon, 04 May 2026 20:45:03 GMT  
		Size: 16.3 KB (16343 bytes)  
		MIME: application/vnd.in-toto+json
