## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:9dec50c8aae3217159b5c632dee2234668aa28e1541dca8dd781cd2943ee2ed4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:bd5e4eb01e084b0b382a3189a8de8da7470045d45aa53862d4b0807849630924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.4 MB (349356600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f5f2f8b6106f7a18c51c0c5689ec85240d71ba7dc40df00971d47c733e5e8b1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:10:31 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:10:31 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:10:31 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:10:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:16:13 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 31 Oct 2025 01:16:21 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:16:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:16:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:16:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:16:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:16:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:16:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:16:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:16:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:16:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:16:22 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:16:22 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:16:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:16:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:16:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d20f169c4ab9c5b596302c6e78d09dc97ac1a459af646782f43c571ba613820`  
		Last Modified: Fri, 31 Oct 2025 00:11:11 GMT  
		Size: 76.0 MB (76043905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c60de2dd8a4784c39c598c305add397884bcc35bb69bb82d12553d9d32a94ae`  
		Last Modified: Fri, 31 Oct 2025 02:30:58 GMT  
		Size: 171.1 MB (171067219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2029176d246772c42f88e4226484cfe4fa166a71be821e5e1ce52c6f4105311`  
		Last Modified: Fri, 31 Oct 2025 01:16:58 GMT  
		Size: 30.1 MB (30067778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e70924cba4ebf06f98434ab5bc656c1404a1f88061873d5c5cd027486ea77e94`  
		Last Modified: Fri, 31 Oct 2025 01:16:55 GMT  
		Size: 9.2 MB (9242587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e909186713ac9e690fc431a7e12e378ba6ad46173778bb53f94f9cc3cbcb79a`  
		Last Modified: Fri, 31 Oct 2025 01:16:54 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158680a50d5ddcf76982c8a6fa7ee3b464fa8d61cbae70cedc6272f5514b471f`  
		Last Modified: Fri, 31 Oct 2025 01:16:55 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:1ce97c78ff623b6dcb5c0df8777f108b102c063027ac2b6044d734d92d8f637d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dc4a8608c31dcd3b8aa4dcbdaebaf2b250d981c9f60d9af0293c3c150f42669`

```dockerfile
```

-	Layers:
	-	`sha256:a797a7f6b1d892ff7b8fca1eda2eae727cdd7d6cd428c155aa8e2b75d886f7a1`  
		Last Modified: Fri, 31 Oct 2025 02:28:41 GMT  
		Size: 6.8 MB (6773610 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81153ebaa03722725284ecbfaee3bdd6eedfbf2bdd780cb1079349192bf7f825`  
		Last Modified: Fri, 31 Oct 2025 02:28:42 GMT  
		Size: 18.2 KB (18186 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:22d48f7b32c2b6332a263d268473546004fb286c4b32a9a978acd27fa27514d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312371419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa0da7d8d36cbc86db7a50ca1188459f21da8d69f3ee381e5bdb09151613d03`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:10:58 GMT
ARG version=1.8.0_472.b08-1
# Fri, 31 Oct 2025 00:10:58 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-1.8.0-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 31 Oct 2025 00:10:58 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:10:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 31 Oct 2025 01:15:31 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:15:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:15:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:15:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:15:39 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:15:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:15:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:15:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0d96ed5cf7cdd43c028ca3ffb2b3c794c53305e80d242b1a23649bd6d4c7ac`  
		Last Modified: Fri, 31 Oct 2025 00:11:39 GMT  
		Size: 60.1 MB (60118918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203648f02d176347ad6531be08c9b6319e5fe9bb53ad46091fa57548b485a063`  
		Last Modified: Fri, 31 Oct 2025 01:16:04 GMT  
		Size: 147.0 MB (147019921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b326ed4911d7da605c4db1ec79e024524f5b1d8ccd0fd086344b2600d7e3c4c2`  
		Last Modified: Fri, 31 Oct 2025 01:16:11 GMT  
		Size: 31.2 MB (31195490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f89ff20e7bb32ed2ce43085f3b02afdc64e4ffce943a19daec7f37a538e154f`  
		Last Modified: Fri, 31 Oct 2025 01:16:08 GMT  
		Size: 9.2 MB (9242587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0109b13024dbf88c6f4d6e9f72ccec0af76342cd0e510adb745df7b48d760ef3`  
		Last Modified: Fri, 31 Oct 2025 01:16:07 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e711b1cd6206c0041fcec07510489cb1252f25a0af6f600cabd9b9ddd3073b12`  
		Last Modified: Fri, 31 Oct 2025 01:16:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:8086bc5025bbcb87c9e307b623a3f55bbef3fcac6c4a18bfbb3d1719002d07dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6769142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cafa051fc2c90f69e1786ab9ec85592e2380a0f5d41ed0ba36e9e9eb4d78342`

```dockerfile
```

-	Layers:
	-	`sha256:25e482d285d264d6121531917f49277bc4ea65517f7597d3ca4e0218918a947d`  
		Last Modified: Fri, 31 Oct 2025 02:28:48 GMT  
		Size: 6.8 MB (6750807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f646d9be17ebb0c9adedf10165adc851c307d8577df761b6ffddc46ebc5d84c`  
		Last Modified: Fri, 31 Oct 2025 02:28:49 GMT  
		Size: 18.3 KB (18335 bytes)  
		MIME: application/vnd.in-toto+json
