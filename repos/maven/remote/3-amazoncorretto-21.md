## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:f226521a1e1ecd9b0494f7d9090af261e2d358dd65327155098ab5dcd4490473
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:55c1a3453dc75c4c83dfca41f62726aab5797196524914bb2b6dafa5b972777f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **444.9 MB (444918271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc835c213309484c0b25c565b1932ffa1757ccf92c97f6f2c0fe773c22f0a3e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:39:12 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:39:12 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:29 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:29 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:12:29 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 04 May 2026 20:44:16 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Mon, 04 May 2026 20:44:25 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 04 May 2026 20:44:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 04 May 2026 20:44:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 04 May 2026 20:44:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 04 May 2026 20:44:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 04 May 2026 20:44:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 04 May 2026 20:44:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 04 May 2026 20:44:26 GMT
ARG USER_HOME_DIR=/root
# Mon, 04 May 2026 20:44:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 04 May 2026 20:44:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 04 May 2026 20:44:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1deb63baef8049d37b87192670264bba74a0207718cc43a1c66077f5bf81a3c8`  
		Last Modified: Sat, 02 May 2026 04:14:38 GMT  
		Size: 62.9 MB (62860009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34427ac8245f2bc54ae2269830d743a78c73c94138af0501660e55c8b91be1ff`  
		Last Modified: Mon, 04 May 2026 20:12:51 GMT  
		Size: 165.7 MB (165695557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:211b78fba2d264b8d98c22334854d1aa21ae5c1ca85ecb05cadd53ab0a7986ec`  
		Last Modified: Mon, 04 May 2026 20:44:54 GMT  
		Size: 177.0 MB (176970982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fd2bfd955e7d36e98be960444a758c9f6eb2382a87d62e37640fc5b914d3f19`  
		Last Modified: Mon, 04 May 2026 20:44:51 GMT  
		Size: 30.1 MB (30078496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea69994d339bd93bbd7b077ca98380371006ffce8ae1a33ef64e4e1235e5d29f`  
		Last Modified: Mon, 04 May 2026 20:44:50 GMT  
		Size: 9.3 MB (9312218 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6b1f9f14793149c65421c09b76c5adac09a6e5456bbb291d437a6ad1f37286`  
		Last Modified: Mon, 04 May 2026 20:44:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96f95fe54c6c45538a2239f6765aeee2d356281c4948ef1dcbf20f88b62c5443`  
		Last Modified: Mon, 04 May 2026 20:44:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:f1c1ec9b4301a48829854c70bc82f4986dc7e233a1baaab06869bfe4058920d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95caa3835964cc208ede8b46cf4839c91c2e60e809bdee3b383dd6778af8a7e4`

```dockerfile
```

-	Layers:
	-	`sha256:a559b1e5c5e8265069a8ec2072fad267ce7a010ce0e679e7eeab5abf9e542b83`  
		Last Modified: Mon, 04 May 2026 20:44:49 GMT  
		Size: 6.9 MB (6933065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9264e1734fb5496ae7304e7b94f6bc541da06df5bbd04b3f35dee1d2a79ffc1e`  
		Last Modified: Mon, 04 May 2026 20:44:49 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:58a3ab16add052ea85a07fc4af3c7f961e5119160bcc46661d1661e6b8bb4af3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.6 MB (422589105 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d94b432535b067277cc648989234b60a154f3c5942c863a9101a411bd0a4459`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:40:38 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:38 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:07 GMT
ARG version=21.0.11.10-1
# Mon, 04 May 2026 20:12:07 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 04 May 2026 20:12:07 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 08 May 2026 00:29:28 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 08 May 2026 00:29:36 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 08 May 2026 00:29:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:29:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:29:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:29:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:29:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:29:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:29:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:29:36 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:29:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:29:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:29:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d78bec86efed585192790ef27ca98e5305604b02ec838239205e149e3aff726c`  
		Last Modified: Mon, 04 May 2026 10:12:23 GMT  
		Size: 64.8 MB (64795531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdfcdf3bd2c92c2567fd8412ee72fbd46db7b157b9d64a0f969635bd1431a4a`  
		Last Modified: Mon, 04 May 2026 20:12:31 GMT  
		Size: 163.9 MB (163902837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:397f18e4a1a3282be6e954f7d7a96d063404c8a065060c1de35f3aca66c4e371`  
		Last Modified: Fri, 08 May 2026 00:30:05 GMT  
		Size: 153.4 MB (153370177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:268423e87bb1295424fafef04b2948b2f39470795019791f8f4c8ad9803f611a`  
		Last Modified: Fri, 08 May 2026 00:30:02 GMT  
		Size: 31.2 MB (31207298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3e2ac5b9f2b44e7c5441196398605a0793115ef4633884e25ec1c5a6086ff9`  
		Last Modified: Fri, 08 May 2026 00:30:06 GMT  
		Size: 9.3 MB (9312256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c753d647f2afdea87ae40e97f798af76259cf7ee2d94aa7cb7e83f258ae92867`  
		Last Modified: Fri, 08 May 2026 00:30:01 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733ef5e0f5bab98e3ce4bdc1c65651cbff691557c0fbbd672d94553ab2199747`  
		Last Modified: Fri, 08 May 2026 00:30:02 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:542fcc7a7e00173d8279fb89ee0e26caa09aeba67b22f36bb1b680244dd07835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153c31a115b1da72c93afa2a3b5b5ae222c147f6e437ace518d5feba34804b31`

```dockerfile
```

-	Layers:
	-	`sha256:018e47d8bc5832b1e57ee6395053d0d93c6c10ba0970c61953bd44dc09ec9675`  
		Last Modified: Fri, 08 May 2026 00:30:07 GMT  
		Size: 6.9 MB (6930464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead486309fa34491e2e4d759fe0e9e93d00071891eced7202dda8a02d8bebfdd`  
		Last Modified: Fri, 08 May 2026 00:30:00 GMT  
		Size: 16.5 KB (16520 bytes)  
		MIME: application/vnd.in-toto+json
