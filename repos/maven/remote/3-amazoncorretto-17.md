## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:e081f58fa013d5cdbfe1139d250557d8417189658a6c12090a8fd70e123d58b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:a29c1b59d763f5a2068b923d7d197f43044fde3637947551449e58cca483d890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.8 MB (436847332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ab758375984df377edd45991ca509ebb91bfb868f32569e121f534df483d18`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:36 GMT
ARG version=17.0.19.10-1
# Tue, 09 Jun 2026 21:11:36 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:11:36 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 09 Jun 2026 22:07:59 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:08:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:08:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:08:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:08:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:08:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:08:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:08:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:08:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:08:06 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316fa5b231bdf53d77ebf835e30302f1cbbf13c3517e7e2d0bce3256af944f33`  
		Last Modified: Tue, 09 Jun 2026 21:11:57 GMT  
		Size: 152.7 MB (152678370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fed676331adace14be982b26a525aa6e1e9638d651c2a001663d37035950a9a`  
		Last Modified: Tue, 09 Jun 2026 22:08:31 GMT  
		Size: 181.8 MB (181795719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35927bf3674e1399a4f4113ffe1087188cbb3f69d86cd3c5e29dbb37181e7242`  
		Last Modified: Tue, 09 Jun 2026 22:08:28 GMT  
		Size: 30.1 MB (30070314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8575efe6507757b944b7aad0426e60ecac696871e014c3109abc62391c17fa3b`  
		Last Modified: Tue, 09 Jun 2026 22:08:27 GMT  
		Size: 9.4 MB (9359967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18edbaf6f873df5d96b87040d9531bb14eda77ea427e70f863c9b76766796f2e`  
		Last Modified: Tue, 09 Jun 2026 22:08:27 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9786d5d2868e1b2f1259de3f0b6b6c6708710ceac468bbd7c67cf24726cfa5e`  
		Last Modified: Tue, 09 Jun 2026 22:08:28 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:5933e3479480216cda345b8d95694ed5b97ddc0eda5ff935081f08a11ed4f154
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:735f88de85260f0b12eaec72a7ff6611d7e7cd68ce3b0663e05cd97c9faf77c0`

```dockerfile
```

-	Layers:
	-	`sha256:7f895884e183b9eb69aa1c27dfb53039b5df96a164295e646be536377ed9e735`  
		Last Modified: Tue, 09 Jun 2026 22:08:27 GMT  
		Size: 6.9 MB (6933165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32028b8936f7d749a8db6b358c56f893c37f21012213ef0e76eab48898d8e3ae`  
		Last Modified: Tue, 09 Jun 2026 22:08:27 GMT  
		Size: 16.2 KB (16195 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:edd1a53401eca074ad9f1a4a07802e7a05ba5ea050c860b79ee00f1306378473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.0 MB (414018944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6890ebe390acb5976049c7d03779778b1b136b8d16429c7e77cc76114718f6ef`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:48 GMT
ARG version=17.0.19.10-1
# Tue, 09 Jun 2026 21:10:48 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 09 Jun 2026 21:10:48 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 09 Jun 2026 22:09:17 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:09:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:09:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:09:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:09:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:09:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:09:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:09:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:09:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e66bd9d6c257f672a922e2070654cb7f7696ad8d077d0c316b105f7d35314fde`  
		Last Modified: Tue, 09 Jun 2026 21:11:09 GMT  
		Size: 151.3 MB (151318700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7f522b9a548b1a15a46ae79affd7ec2d1e96396eae2b87a4b703170da2818e`  
		Last Modified: Tue, 09 Jun 2026 22:09:52 GMT  
		Size: 157.3 MB (157343530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7e2d6d49282dc3b18a9ffdd8db765d5eb2426c08c3107b3a372c8691360e271`  
		Last Modified: Tue, 09 Jun 2026 22:09:50 GMT  
		Size: 31.2 MB (31205023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562a0db6b70ddba05cf51b9c33e6262e027fc7429055f039f0aedc5c228548f3`  
		Last Modified: Tue, 09 Jun 2026 22:09:49 GMT  
		Size: 9.4 MB (9359970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa3a0d00f17ebdc6b88d3653171b1f7d5ab69d7bdd3b4c4ef5610f6de8f155f`  
		Last Modified: Tue, 09 Jun 2026 22:09:48 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe67d46c1efd5305e6c6595c353655bdfbbf730eaaba33fb25db73e2986f8c7`  
		Last Modified: Tue, 09 Jun 2026 22:09:49 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:9e0f622dedebbe82636d8a901cba28718cc43178e4b067869e9a32e9b453e2bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc12520f3f8c1d430044adb16f2e8328951180da2d4f45893a05e51a124ebcb7`

```dockerfile
```

-	Layers:
	-	`sha256:4b0c6b846d8413bf63ef3aaa4b50e273021bb40c080267f56647aa1749a37e40`  
		Last Modified: Tue, 09 Jun 2026 22:09:48 GMT  
		Size: 6.9 MB (6930564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5007500f98b7577bdc11419de220952e7e97d0f0b561a8da3806941a84d1157`  
		Last Modified: Tue, 09 Jun 2026 22:09:48 GMT  
		Size: 16.3 KB (16344 bytes)  
		MIME: application/vnd.in-toto+json
