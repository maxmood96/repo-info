## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:2dfe74fb000491b2e96b7f25f09e605f9cd952d994fb132378fc3cd1e708c78d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:6e1f30618a76a90284afe13e8cf027438a30ae98020a92b273b1aee95d4d328b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.7 MB (407693550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2968cf83c14acc199ab1f6657a60354731f28fb4b8d283c5e2ab2cacd82ea1a0`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.14.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:2ddc0aa2636ed19b988b4176374929a92f5862f6c6e88ea255d352140af781e6`  
		Last Modified: Fri, 17 Jan 2025 20:13:56 GMT  
		Size: 62.6 MB (62648554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39229bd85c07c66cd7b15b5de8d7dc5a37f286c63e2ce9d9ab365c8eda7b2a7`  
		Last Modified: Thu, 23 Jan 2025 23:08:20 GMT  
		Size: 151.6 MB (151648757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c0711978f9223abc0e71ccdbf13a636aad8062a58e4b709b4d958e83f4b3c`  
		Last Modified: Fri, 31 Jan 2025 03:14:13 GMT  
		Size: 154.2 MB (154159854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0549f742a52fb851d598eaf256ab38025ef8defff7f693a7c8b0683980d3af1`  
		Last Modified: Fri, 31 Jan 2025 03:14:11 GMT  
		Size: 30.1 MB (30064909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a3949d1a4abb72d19287a93fe9f82dee4d8c5d1080231fb07918457ecaf545`  
		Last Modified: Fri, 31 Jan 2025 03:14:11 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5f711aa8763a5b6676778ece3dd48374664fc2ba7d3ca091c862ecf1d932a01`  
		Last Modified: Fri, 31 Jan 2025 03:14:10 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a22f4fd6df671632cca895af4a2b784d4381d622ce3c0e29a3e96154860f77c`  
		Last Modified: Fri, 31 Jan 2025 03:14:11 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:130ab16cedaa432039afc14e1fb555f3c502cb0c58823e98ff349936bc3a340b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6927935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d8b185649dc000a16bb3973779c87f6c26bde0d0b2037ae3fcf651627ea3843`

```dockerfile
```

-	Layers:
	-	`sha256:297d13d2c98a4a2adaf7ab46c718655dd141300b338b774ac4d804a9daec013e`  
		Last Modified: Fri, 31 Jan 2025 03:14:10 GMT  
		Size: 6.9 MB (6908433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7441012dbe71fa597cf06b6ae6ad360e580c4ce15a755b7013134e28cff155`  
		Last Modified: Fri, 31 Jan 2025 03:14:10 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:35127ef6cc68afc0c4a04a85530e19f16a8e4f71e5bb46b9fde02bacecc8084f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.6 MB (384562011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0883e5b06d6684ac67fddf63075fbd01e3471889c67fb4ba90db18f3bd969b65`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.14.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:dc3d403853487343f06bffefe21e65d842f88da2d7a1073ba2820fdb1b7ece72`  
		Last Modified: Fri, 17 Jan 2025 20:14:11 GMT  
		Size: 64.6 MB (64590432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b468ded855152a51ff345275786ae77f6a6f85b0744143c0144b705e9f0bee4`  
		Last Modified: Thu, 23 Jan 2025 23:16:16 GMT  
		Size: 150.3 MB (150315354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7438b01c59e2729807a2e27d9d38dbfb85493efc881068ad60827bb057acab`  
		Last Modified: Fri, 24 Jan 2025 00:32:21 GMT  
		Size: 129.3 MB (129288525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b201a46b73dd6e94327507bd41ba40970e73620be44fea317902126bc4e725`  
		Last Modified: Fri, 24 Jan 2025 00:32:18 GMT  
		Size: 31.2 MB (31196224 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a02bb7067dd8895fdb5135b541f2897a381d862c6f46453e7307d57052d3273`  
		Last Modified: Fri, 24 Jan 2025 00:32:19 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25d2fb79affadef97163b0b0f019a5f710955fb7bdeaa1cf44e67daf78aea8ea`  
		Last Modified: Fri, 24 Jan 2025 00:32:18 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d0186a77cb28bf8de604584c465b6ae06de857ae8d2c14c078b64a967640df`  
		Last Modified: Fri, 24 Jan 2025 00:32:19 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:83c22a2c450bd488565034e55628353ca0beff35a8c5c3f2e906dc99d3c165fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6925577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e35641bd804a77452f352a48a73d4c48cdff9eb5bc80dbb4ebc2b2f0164b5f55`

```dockerfile
```

-	Layers:
	-	`sha256:abbc1dd6a44a521df57802a578eed7bb482d5d31bca876d4cc18084bc78ecfd0`  
		Last Modified: Fri, 24 Jan 2025 00:32:18 GMT  
		Size: 6.9 MB (6905880 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:738dad01fe25cef75eebdb78ea25e82c31f9a323c608e6a20af8461d49481375`  
		Last Modified: Fri, 24 Jan 2025 00:32:17 GMT  
		Size: 19.7 KB (19697 bytes)  
		MIME: application/vnd.in-toto+json
