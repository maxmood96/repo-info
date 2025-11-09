## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:11ff369582b3d77072992da80244faaddc0675427992b50880d320205c148f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:ba66a78e31c6f0b0d75b3e9f9aecd222e4f8fd3f24b28b9ac07c09fb4045b384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **421.4 MB (421400951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:588f3b3fc19d45fee149266f5f44e3d801c8b7c7c66f5c2ac08df6665da10042`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:03:23 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:03:23 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:11:43 GMT
ARG version=11.0.29.7-1
# Thu, 06 Nov 2025 22:11:43 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:11:43 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:11:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 08 Nov 2025 19:22:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 08 Nov 2025 19:22:46 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 08 Nov 2025 19:22:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:22:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:22:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:22:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:22:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:22:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:22:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:22:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:22:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:22:47 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:22:47 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:22:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:22:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:22:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0936bd52c996ecee97f4dd53982e2e986383d631b1506cd33fb60fb70bef48bb`  
		Last Modified: Thu, 06 Nov 2025 07:20:38 GMT  
		Size: 62.9 MB (62934134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d698af529dfc04b48b4625b22e044bbbbde679eaff562a9eac50396c1bb0c1b7`  
		Last Modified: Thu, 06 Nov 2025 23:13:03 GMT  
		Size: 148.0 MB (148044753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b6ddaede1f0c93f84a3a681a24d3c940212ed97be76bd266a70ca48b27d065`  
		Last Modified: Sat, 08 Nov 2025 22:23:28 GMT  
		Size: 171.1 MB (171107986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7df3456934b2737e9d8ea35a771dffe24703bcb0d97437d8e4360e64bc8dde2e`  
		Last Modified: Sat, 08 Nov 2025 20:51:18 GMT  
		Size: 30.1 MB (30070470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c3a5ed613ccc4167be969a87ef876b2e92e52d3c51fb181ab793df9abc558ca`  
		Last Modified: Sat, 08 Nov 2025 20:51:16 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe511cd4fe7dfa0639ff5327669fce8ddeb39b03acc953cbc9afb8b37d852c49`  
		Last Modified: Sat, 08 Nov 2025 20:51:16 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456f7fd06c618d648eb159eeb692e4a55557384f5fa09760438a90ed06fe3a7e`  
		Last Modified: Sat, 08 Nov 2025 20:51:16 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:c7c7177fef3ab9c981b71c7ef3306a1ca111bbc5cd6d858fc908c4f8f6ec9249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6957753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4ba50ac246689461577e160813453a7b1a36a66e5f13d462f80de98a601e58d`

```dockerfile
```

-	Layers:
	-	`sha256:cc164156522f43b2a9aa9af1342f0703e0f0622bf56c8d5ef633e41151f2b46a`  
		Last Modified: Sat, 08 Nov 2025 21:27:46 GMT  
		Size: 6.9 MB (6939559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec662bdceae90e21c68c3825839bbaf9ca54752cd3eafdd9f61de734096843b9`  
		Last Modified: Sat, 08 Nov 2025 21:27:47 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c3ac5a09014cebea72d9191a235745f23c896fce880d8272b1c2ef94b7dbcf94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397416920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd35870c11c6d6b7864151a8011ab3b952fb0d159bfaf616ec079cce8871a097`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:02:17 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:02:17 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:09 GMT
ARG version=11.0.29.7-1
# Thu, 06 Nov 2025 22:13:09 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Thu, 06 Nov 2025 22:13:09 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Sat, 08 Nov 2025 19:22:10 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
RUN yum install -y openssh-clients # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:22:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:22:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:22:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:22:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:22:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:22:18 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:22:18 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:22:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:22:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:22:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a7c3aef254f38f8d9dc0b33a459e16cf71365801ec3cea141d9ae2909de17717`  
		Last Modified: Thu, 06 Nov 2025 03:12:00 GMT  
		Size: 64.8 MB (64793296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b3dbbf9942d831705af842b5b4d8637f885aef547dbffbb26a5f48f413b10f`  
		Last Modified: Thu, 06 Nov 2025 23:11:18 GMT  
		Size: 145.1 MB (145144507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcbfe27e5e6f36b4542f86a049818a762930cd15030751db20f7beeffe36327c`  
		Last Modified: Sun, 09 Nov 2025 04:04:12 GMT  
		Size: 147.0 MB (147043442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51a89698692f5e2d283b93124a97c8bebe018f238cacc77c5619924e56962a6d`  
		Last Modified: Sat, 08 Nov 2025 19:22:56 GMT  
		Size: 31.2 MB (31192057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90ca684ed1a7a4070ee689f6497cfe50471888a88243562b69b6426956bfe1e8`  
		Last Modified: Sat, 08 Nov 2025 19:22:51 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfc55e3ac7cf23c8239803b6c13a573e44d753ae2f5c6677b0de86bf1949343`  
		Last Modified: Sat, 08 Nov 2025 19:22:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:682507f50b22c2c7d75e95adcf5d4e5b4923aaa0886a1ab02c9d64252c7e1320`  
		Last Modified: Sat, 08 Nov 2025 19:22:49 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:075c62153eb99cafa7a34898b009ba1732709675abb4b5fc16bfc7b530c4c4a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b16c816c38771ed2065f4d8c955c3199a8bf81f317b58c0820746feec1bce69`

```dockerfile
```

-	Layers:
	-	`sha256:5f197a87b3eeb5ac10cdf511318b3ccf6ad1c32de8ca659894e74bb85134183d`  
		Last Modified: Sat, 08 Nov 2025 21:27:52 GMT  
		Size: 6.9 MB (6937763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:085f8f401cdc1d84ea031841bab74cf7923fb4e683c3b9980ce6f9371eb7e2ff`  
		Last Modified: Sat, 08 Nov 2025 21:27:53 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
