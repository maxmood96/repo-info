## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:44f717d88bc6bcb64a42b5dab67e7feec0d1edaefb339ad2de3a60d31be9400b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:95fa2c4d3631995489348e8998886803e2e3341badde6b5c1ec5ecf61e3295aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.5 MB (327526961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f497842d1ee53830e9b1432026467bb8b8591312295bba9617fe3f118ea83d4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_432.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:32c87c6464b59c63781462d4129c84f2806c57bdb75e94414a62f13a51d7b113`  
		Last Modified: Thu, 17 Oct 2024 08:34:33 GMT  
		Size: 62.7 MB (62679539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dcde7c572465b0c2044d390c8c2af0e3814567c28a2fd6ce2525c3968db45fd`  
		Last Modified: Mon, 21 Oct 2024 18:56:44 GMT  
		Size: 75.6 MB (75579823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c25a5509dcb32789576ba0ce5fbdc61c3995299cbed753c8a2cbd17f8b13dc6`  
		Last Modified: Thu, 24 Oct 2024 02:56:10 GMT  
		Size: 150.0 MB (150042039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1eb66906d179eddf908c4bb4f20b92f7b68f822ae19d7b6bfb679b5860cef84`  
		Last Modified: Thu, 24 Oct 2024 02:56:09 GMT  
		Size: 30.1 MB (30054085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fca3302761c3efa68ace778eceff70e20b67f8b4e252aba2b7bc3a666a39a80`  
		Last Modified: Thu, 24 Oct 2024 02:56:09 GMT  
		Size: 9.2 MB (9170436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ea130109d5eec6bafe45e2191f3d37b73093f49ae2ffc3be754d541e315fc7`  
		Last Modified: Thu, 24 Oct 2024 02:56:08 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6cf5f9de79b5b2d80c92fc5e1e3efc1b58ad8a27905a187e8c2f6f2cf63832`  
		Last Modified: Thu, 24 Oct 2024 02:56:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:716173076b1858f24583a22e6f0f17cc68e8027846730cd20fe7a33ccbf88d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6781787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72a48abd130f9369d57c4dcaab2aef752832c20a46d08ad7f2981954d4752692`

```dockerfile
```

-	Layers:
	-	`sha256:236adc743e5a5bdf92a3bade0ebb9428f24b951e4070bd6f534e9c17869ae53f`  
		Last Modified: Thu, 24 Oct 2024 02:56:09 GMT  
		Size: 6.8 MB (6763568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13bd9b9dd78dd3c2e9347d1d6e6127bf077c03ea919392dbcb7d9c2dd8659166`  
		Last Modified: Thu, 24 Oct 2024 02:56:08 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2ffc2325e8e93ab0c00b0e41c1857a0556e6abbb91993e52a2065366e83edc96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290720372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:622035586b8f3d6b0f8f68ac866383253d9818f2f7deb8b77f72fcd8921e3746`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_432.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_432.b06-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:c05d42ff0b796ff4b1055b91676cb7e4b68389f23472cfdf987fa036f88561a9`  
		Last Modified: Thu, 17 Oct 2024 14:51:33 GMT  
		Size: 64.6 MB (64587089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4630336f3060e79bf64076b281308ad599aaaba9d1d9b474ae38126c908edf98`  
		Last Modified: Mon, 21 Oct 2024 19:13:59 GMT  
		Size: 59.7 MB (59668582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d55a7eba2d6cdd53b7c7624f7ba3fbb85269156f351c1e230052b2999b3d316`  
		Last Modified: Thu, 24 Oct 2024 13:32:23 GMT  
		Size: 126.1 MB (126115511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd53114b239d24c7e126c69caa2607be9a97570160959b54a874f0c6c54ced4f`  
		Last Modified: Thu, 24 Oct 2024 13:32:22 GMT  
		Size: 31.2 MB (31177718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85aa54345da4796e6d2f0ecaf290fe54d79bd2ad6d2a3ebd05cfa8f1e3251b07`  
		Last Modified: Thu, 24 Oct 2024 13:32:21 GMT  
		Size: 9.2 MB (9170430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cf567d3aeb4aec0c12386f0ad9f407a53cab1a7642593ec094353b2c640d41`  
		Last Modified: Thu, 24 Oct 2024 13:32:20 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa4b3762faee09eeac6317dc4da78ae1395ce80518f550bb1c3e51dfb88bf91`  
		Last Modified: Thu, 24 Oct 2024 13:32:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:7585d3f05fbb31d3bf17e83c1c6b1a650fbffb4adca56e53a1b7a9b3e87e7190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6759158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63cd089e254c15b0e644cc0e7442fb7109110500adda852565a306b02361defb`

```dockerfile
```

-	Layers:
	-	`sha256:7147d213616a44eac6abd771295abc4f58ef81d23e2a90514e6119964b091dd5`  
		Last Modified: Thu, 24 Oct 2024 13:32:20 GMT  
		Size: 6.7 MB (6740791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:facd3652846e97bdbf9771663d4efd3a08c2b086e6dbb444857fe1ac79a4c765`  
		Last Modified: Thu, 24 Oct 2024 13:32:20 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json
