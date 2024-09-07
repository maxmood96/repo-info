## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:8c87d2da3d805ee31352798aa5ca5f450d987b52a3481b7ed650e2504d06ef1d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:bc6b4b78bd0d7dbc8b44771cc5d61606c323c73d8fedff252bad45376a7d6adf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.0 MB (416017530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6711f4bf903c13c4a6a4d4e88c80eebaf5758331c2fca251cc3714edb5419432`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7f8efc14a219454ff8f309d236d31a55327a6ff05dda42df51689619d9a34fdc`  
		Last Modified: Fri, 06 Sep 2024 18:59:36 GMT  
		Size: 62.7 MB (62695547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31392d7ddaaf1b0a5a2312e768716ba381912bc41f814ef2a3e7e3a0ea9f9f5`  
		Last Modified: Sat, 07 Sep 2024 01:05:55 GMT  
		Size: 165.8 MB (165819543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416846df0d82c161d067fcdc6039aac48448e8836bf1f9c2cf4f2bbf32ce01d0`  
		Last Modified: Sat, 07 Sep 2024 01:56:36 GMT  
		Size: 148.2 MB (148245152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577ed38c7d7be7d9b1c90a6bd91c6575a092b5964e18edae58b83ff53ceb98e8`  
		Last Modified: Sat, 07 Sep 2024 01:56:34 GMT  
		Size: 30.1 MB (30085802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec59d18906085d64c6b89252c75d60f0005f4daa5703154ed2d13aff22e5da75`  
		Last Modified: Sat, 07 Sep 2024 01:56:34 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c93a5dae60dd86e5e07975f587775b8acba68dff326be47be0f28114b111c15`  
		Last Modified: Sat, 07 Sep 2024 01:56:34 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cd43ead86a24b761b718d9b44c6888b6396fdfe1a56226355489987d9c653fa`  
		Last Modified: Sat, 07 Sep 2024 01:56:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:705ede62560e64ac1f64f9928bf4376c9e7a9c7de344dacea0f73405cf297194
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6934888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97d2206fe0793112de738a4377a047ed853e94c416aae9ec55ea0c42bdf0b2be`

```dockerfile
```

-	Layers:
	-	`sha256:780802249261ce3c792292b0c60f111abc54df8e639b5d785c6ab053c7d48f88`  
		Last Modified: Sat, 07 Sep 2024 01:56:34 GMT  
		Size: 6.9 MB (6916692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5edfd2657e6d6505f91441321b978ff6ac23247f1d765d3ca595ffa2543faeea`  
		Last Modified: Sat, 07 Sep 2024 01:56:34 GMT  
		Size: 18.2 KB (18196 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5f460f9988eb8d62775d80e8c2712d3af285621822fb4c02bc6a34d3c952ea55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.2 MB (392155089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208ec04762419f809a054dde7f21f6166eda0fa93023407eaaa0db068c6bec9c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:90f49a0942af5d23537faf4773696e5a1ede92273c5b8379a6acc52111436bb8`  
		Last Modified: Tue, 20 Aug 2024 21:34:48 GMT  
		Size: 64.6 MB (64587135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7419c382a2192974eb056ae70293b0c9f1ad26440b4505342e026bc0919485b7`  
		Last Modified: Fri, 23 Aug 2024 02:33:27 GMT  
		Size: 163.8 MB (163820715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31547b0c536ad55e1ce8981a8de1e78223f10899b485da342648c0c6c8a22e7`  
		Last Modified: Fri, 23 Aug 2024 03:03:21 GMT  
		Size: 123.4 MB (123407441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac30330a997778a9d5ed1b5c2a3387552c171eff4ef4050b5790a5f1acfd595f`  
		Last Modified: Fri, 23 Aug 2024 03:03:19 GMT  
		Size: 31.2 MB (31168325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0941c74157cacd9c4a52914ef7a0e84ae0c0886ca55b0e946064782bd5e7d08d`  
		Last Modified: Fri, 23 Aug 2024 03:03:19 GMT  
		Size: 9.2 MB (9170430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e270bf25ea22e95b22c770e06fdc8db5e549bc1806d143a8d788c9e1090806ab`  
		Last Modified: Fri, 23 Aug 2024 03:03:18 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74c603e57781f796566f70286cec13adc47ba46cb109febc548170a50bb225ab`  
		Last Modified: Fri, 23 Aug 2024 03:03:19 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:e82d9b26fe8f88e67ff7ce342d0c6367c5b4c9889d8c2de053d20a5110ec2aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6933008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae014c1683739ae3e467437bf2c72c815945650f2587c4fecdf045d31322104`

```dockerfile
```

-	Layers:
	-	`sha256:12e75b1b814858ad9da4c9946ef53f899e68fcbbcc280e04e8943997acbf4476`  
		Last Modified: Sat, 24 Aug 2024 03:20:43 GMT  
		Size: 6.9 MB (6914087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b10951cf635ebd46c7df3c3ab36e40035d764c124bb26eb3027bd1c1c36248f0`  
		Last Modified: Sat, 24 Aug 2024 03:20:42 GMT  
		Size: 18.9 KB (18921 bytes)  
		MIME: application/vnd.in-toto+json
