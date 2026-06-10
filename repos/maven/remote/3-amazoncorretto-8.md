## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:27b7c8790439dd3306c690893cca5259b4284624f931cfff2cacc6c0d5773899
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:7541d44ace90c382e214aed7acdb4e67ed03dc98fb40524c6c7439143355b4b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.3 MB (360279448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ec9097f60eca5fc4159bb3cc0db4b6ab4af4a0680c4b3c7c30d78891dd0d839`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:20 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:10:20 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:10:20 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 09 Jun 2026 22:09:10 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 09 Jun 2026 22:09:18 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 09 Jun 2026 22:09:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:09:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:09:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:09:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:09:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:09:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:09:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:09:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:09:18 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:09:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:09:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:09:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0bf15654d32f2aceaed25c8e6fe45e5ad1cffefed578eb90f9bfe011cb9cf20`  
		Last Modified: Tue, 09 Jun 2026 21:10:35 GMT  
		Size: 76.1 MB (76114496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf5b83b1da94c289038778dfe75ee15c5ae0341862fc04dc2ea1e228afe97f6b`  
		Last Modified: Tue, 09 Jun 2026 22:09:47 GMT  
		Size: 181.8 MB (181798166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1feb64f61a3c0da0408fe0f3e1674629811e90884a39b8d7a04d4c37ee70d8bc`  
		Last Modified: Tue, 09 Jun 2026 22:09:44 GMT  
		Size: 30.1 MB (30063851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c15dfe5f8cf37993749e0790039ee93c4aed0f2d86e8dd6b3753ff0f02369723`  
		Last Modified: Tue, 09 Jun 2026 22:09:43 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4502e488aa4b741df7f086e40fa17e6e1ecb6de5174c83f340bf33f41bd3114b`  
		Last Modified: Tue, 09 Jun 2026 22:09:42 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c8c6c45e2741448f6b607535d239e8a5a7d0f30ca125647210a85ac120d7d2`  
		Last Modified: Tue, 09 Jun 2026 22:09:44 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:d552df3446748fa6b4fe65800789d40760ccc9696ba5d8dcc6226b46d3174b23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6789891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5b6b9a0185d20029e11f0df2b1d532be9bd8e20362770c9423e00205dac780d`

```dockerfile
```

-	Layers:
	-	`sha256:edfd67db619a7b07f5e7214a3f50b019f9102631a2e4280f5ba229e229cb8f42`  
		Last Modified: Tue, 09 Jun 2026 22:09:43 GMT  
		Size: 6.8 MB (6773705 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f112defee53db416d17cac1b101cb16967db92bd048b69bf8dafd42b45883787`  
		Last Modified: Tue, 09 Jun 2026 22:09:42 GMT  
		Size: 16.2 KB (16186 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d8cf67cd3575d9f4db3881bdc85d5910df4761a2197d437663d5c3d90f0b41a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.6 MB (322632107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776ce8a1dab842c5292490d4d97506c6708a5244273bfe41c40b5f4f0ea8c3f1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:13 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:10:13 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:10:13 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 09 Jun 2026 22:10:16 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 09 Jun 2026 22:10:23 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 09 Jun 2026 22:10:23 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:10:23 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:10:23 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:10:23 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:10:23 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:10:23 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:10:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:10:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:10:23 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:10:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:10:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:10:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2306dfd68bf489e4f593bbbc4e6fb78de86bc797383a3302342a651eb104b94c`  
		Last Modified: Tue, 09 Jun 2026 21:10:28 GMT  
		Size: 59.9 MB (59947990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcb6b12cdb7a4e86f27078a26bf206747d489bf2a7fc6867dc56bd162f44c4c`  
		Last Modified: Tue, 09 Jun 2026 22:10:50 GMT  
		Size: 157.3 MB (157342476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff79fdd0cd74406f4d0b323462f09fbbb006b2f00f70836d96d5cc74237bb00`  
		Last Modified: Tue, 09 Jun 2026 22:10:48 GMT  
		Size: 31.2 MB (31189939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a87531333ef7b8dbd38dbe2f5fd9b0076d32b420fc6f2e754aa70404d58de5`  
		Last Modified: Tue, 09 Jun 2026 22:10:47 GMT  
		Size: 9.4 MB (9359980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ac2366e234231b93f730d1f8c9434fa344c7cff4b8b33c4a6be6335d1afb4cf`  
		Last Modified: Tue, 09 Jun 2026 22:10:46 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0eee1ecabb109c5fca031094282ce71fde2d92c8fb7693cbf53c460708db963`  
		Last Modified: Tue, 09 Jun 2026 22:10:48 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:29bc4e11dd2b0e59267f2867c2bd688969871e8b6b0b53c97c8a0252f83c2c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:130defc4fa100cc2ad4a8c3e3b853fe8ed697d8249f6196512f99bbf3452dec0`

```dockerfile
```

-	Layers:
	-	`sha256:8efce8f365d1470f696b4b6d8a3977ec70c46985c2fbcadf5c4b67a3724744d8`  
		Last Modified: Tue, 09 Jun 2026 22:10:46 GMT  
		Size: 6.8 MB (6750902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9828b194c0f96a523e577ecf8bf936aaeb85882da08d56f445879031b74f2160`  
		Last Modified: Tue, 09 Jun 2026 22:10:46 GMT  
		Size: 16.3 KB (16334 bytes)  
		MIME: application/vnd.in-toto+json
