## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:ecbf9d06b68dd9b0f4623ee73c44f25b9cd66144f410ad7ccb46c30eaa92974e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:ea76f208129f9923a3b21b39e0e819624a002ed671498d3b506d6b6995b11bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 MB (403405832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63dd139d07b6fcebbef6c5f5588418850ed567c4836b1188430d70816900acc9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=11.0.26.4-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:a0bed05b284dbd715f006bbe67ce36cf5c8dcf0dba36221991f7c151c4180a36`  
		Last Modified: Thu, 23 Jan 2025 23:08:02 GMT  
		Size: 148.2 MB (148205763 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26db5914c0524ae200240e49b1b93226fc988b4ebb367c1c7cc29edb8c672df2`  
		Last Modified: Fri, 24 Jan 2025 00:08:37 GMT  
		Size: 153.3 MB (153305978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10f25279330dee7f3507c1e05a2e53253da2d82e3f390b2315ff106f489ff670`  
		Last Modified: Fri, 24 Jan 2025 00:08:35 GMT  
		Size: 30.1 MB (30074063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feb953a039ad18b1ba03860d7337b7a6abe98b88a272882ffc4bd21f3cc2de91`  
		Last Modified: Fri, 24 Jan 2025 00:08:35 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd8e84732cac83de6023b72baf96285d9fe58cb40b350fa4139b3e70bc2093c`  
		Last Modified: Fri, 24 Jan 2025 00:08:35 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cc2d98f60f6b29d96320ab71fa6368bc8274d64c3caf0569aafb2ab8d4bde48`  
		Last Modified: Fri, 24 Jan 2025 00:08:36 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:43ccd6819aa3db48c643db2741392d9c2c307e8b040bdf702449dc6d1503bc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6932696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b711aeea2f2960ecc868a1490dac768f491154e473e5d465f4368355dd58ed3b`

```dockerfile
```

-	Layers:
	-	`sha256:e401ef598ef693e401d0c30e6fa2e633621a93b3542fe9ddcb0020e542a0b6c1`  
		Last Modified: Fri, 24 Jan 2025 00:08:34 GMT  
		Size: 6.9 MB (6914466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4993f737565e8c70262b7aaabd6c07221c2b427da7a4b004e4aa2f9a4640bf5`  
		Last Modified: Fri, 24 Jan 2025 00:08:34 GMT  
		Size: 18.2 KB (18230 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fd737d3ea9d1d08b30e62b50559f7b78b300dab856966ea068a3ebe2d5abf544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **379.5 MB (379547727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94e1419a368866962eabe7995daf2dd3cb5fe6869e8793d1348b41f9275df63a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=11.0.26.4-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:7565c0eea8654257aa19eee89a0ade7feae3f8747be533441b5e6cf5dd5430a7`  
		Last Modified: Thu, 23 Jan 2025 23:11:03 GMT  
		Size: 145.3 MB (145302602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dea9d73edcac1080acc63820cf693b3f574d56e836898afca5faaf9ced5a034`  
		Last Modified: Fri, 24 Jan 2025 00:30:37 GMT  
		Size: 129.3 MB (129288713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f23efc583f126e220f7062e7624106da5576605b051734753edaae04e982e2c9`  
		Last Modified: Fri, 24 Jan 2025 00:30:33 GMT  
		Size: 31.2 MB (31194500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59eb61c35c4bb02977a036893238f5e8a0018dbd2ec5db78ada47f453f3c273f`  
		Last Modified: Fri, 24 Jan 2025 00:30:33 GMT  
		Size: 9.2 MB (9170438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48fea343e6989b3e7ccf875c533a4e1a97695e8f934935149f0ac92d45d00f83`  
		Last Modified: Fri, 24 Jan 2025 00:30:32 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:246fb752289c3bd1da2fe478ca681f05aac1029500c948ca2adc1c897b2fcc8f`  
		Last Modified: Fri, 24 Jan 2025 00:30:33 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:903912324a5b0771f50041c1710a9a5e34548433668ad493f604550eb3d5ff76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6931048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc87ecee904e4d6b3cdfaf4a04371948e07ddeda4369e6ca734f92d9258e124b`

```dockerfile
```

-	Layers:
	-	`sha256:53f03ecbea64eab06b631b1cb18ecc6e5d8cb021844a9c617f507881c09c7aef`  
		Last Modified: Fri, 24 Jan 2025 00:30:32 GMT  
		Size: 6.9 MB (6912670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a851e7602ae235ffab927a7485381925b1527e77b3b7725513311eff6409475`  
		Last Modified: Fri, 24 Jan 2025 00:30:31 GMT  
		Size: 18.4 KB (18378 bytes)  
		MIME: application/vnd.in-toto+json
