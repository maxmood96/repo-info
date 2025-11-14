## `maven:3-amazoncorretto-11`

```console
$ docker pull maven@sha256:7b4e3b9244f68c21178b6d047b6635746e40c6feeb161a9f876aa683ef210c9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11` - linux; amd64

```console
$ docker pull maven@sha256:299d5e89c705bdd2954099a43d37113b880fdae5cec52787f9f9aa4b4dbcd6ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.4 MB (422431585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef8e19a84960a9f41d396f18f8c9a2d542f3097ce11c39d01aba9fe5ab1f2f7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:59 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:59 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:14:47 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:14:47 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:14:47 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:14:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 14 Nov 2025 03:17:38 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 14 Nov 2025 03:17:46 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:17:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:17:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:17:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:17:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:17:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:17:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:17:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:17:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:17:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:17:46 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:17:46 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:17:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:17:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:17:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7934f821253e9f29ddbcfd161c2f1db5873bd4c1e81009525a6ae3c651f4bbad`  
		Last Modified: Wed, 12 Nov 2025 05:29:44 GMT  
		Size: 62.9 MB (62930572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43fb62205c806751bb98d48643e1aa992f329848298980df7d635af114aa7a9a`  
		Last Modified: Fri, 14 Nov 2025 03:14:58 GMT  
		Size: 148.0 MB (148046029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc63a140a49eb224ec5bc236f88326c68db031a836feda97fc8c7b5095cd47e`  
		Last Modified: Fri, 14 Nov 2025 06:34:35 GMT  
		Size: 172.2 MB (172151124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae0c4476f045d169eb90a71d039064c45975e70d15da8329def44eb9db894d5`  
		Last Modified: Fri, 14 Nov 2025 03:18:25 GMT  
		Size: 30.1 MB (30060251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de4ab1f1fbcd2a9c9a44026c459fd9c3cfbaf4293a65a3dbce02259cf3f6129`  
		Last Modified: Fri, 14 Nov 2025 03:18:22 GMT  
		Size: 9.2 MB (9242571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25b071694098823b68f83348f2eb5b9415a3e4ce26a44b3c8f6d2fbb412db69`  
		Last Modified: Fri, 14 Nov 2025 03:18:21 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ee3c88481412fceb563b56320c110804a9b7b901f50d51854235d6f924f38a`  
		Last Modified: Fri, 14 Nov 2025 03:18:21 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:ac694f194c0c5b6e46ceb83395db6bbb61691a167c9102d789160df7fcb61a78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6957757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf67f3b5193fdf3ad5e6744e42d396421fd303ae30e6a2e042680dc163abb31`

```dockerfile
```

-	Layers:
	-	`sha256:5c46681ba71c74f1eb8d48643a26c6484d32f26cb9f91a6c12064b22311eea87`  
		Last Modified: Fri, 14 Nov 2025 06:27:36 GMT  
		Size: 6.9 MB (6939563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b8e62579258084ef290d593c13c2485a18658153792ee1a1d2ae98a40661c27`  
		Last Modified: Fri, 14 Nov 2025 06:27:37 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2d425637a96756476b135a3bec16fa2895d1c75fdfccbbe97215a8eb3f8b5199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 MB (398395343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:494e8afd4921c335052027c94632ee469484186b2babe6403c179e2790d487c9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:55 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:55 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:15:26 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:15:26 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-11-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-11-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Fri, 14 Nov 2025 02:15:26 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:15:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 14 Nov 2025 03:17:35 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Fri, 14 Nov 2025 03:17:43 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 14 Nov 2025 03:17:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 14 Nov 2025 03:17:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:17:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 14 Nov 2025 03:17:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 14 Nov 2025 03:17:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 14 Nov 2025 03:17:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 14 Nov 2025 03:17:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 14 Nov 2025 03:17:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 14 Nov 2025 03:17:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 14 Nov 2025 03:17:43 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 14 Nov 2025 03:17:43 GMT
ARG USER_HOME_DIR=/root
# Fri, 14 Nov 2025 03:17:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 14 Nov 2025 03:17:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 14 Nov 2025 03:17:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f728e13297b99168d3a417733ff68e277b63760d51b5d9f072d2619319458c56`  
		Last Modified: Thu, 13 Nov 2025 18:37:46 GMT  
		Size: 64.8 MB (64792801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac9edde79542b8043f205bea08ae238c30a1ca98123823ddf3b2f089a63d8ee`  
		Last Modified: Fri, 14 Nov 2025 03:16:38 GMT  
		Size: 145.1 MB (145144926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cff16a018410207649e51a3ae251234b9ed2a7da4b2b1341ba18279797de3536`  
		Last Modified: Fri, 14 Nov 2025 09:41:22 GMT  
		Size: 148.0 MB (148023731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2418efca1b7ed25e1f871e80d72a82e00782c0c9ff6a044b902ea548367eb8`  
		Last Modified: Fri, 14 Nov 2025 03:18:18 GMT  
		Size: 31.2 MB (31190275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79db2f3253978c8490c7096d843a48da79a85762466807c7bbbd9951357867a9`  
		Last Modified: Fri, 14 Nov 2025 03:18:17 GMT  
		Size: 9.2 MB (9242570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7bb1b4f1376b47cdc849bd8725898928516c570fa570b53816280bfefd5089d`  
		Last Modified: Fri, 14 Nov 2025 03:18:14 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a76302563b90499d76d6f684f22bec72fcc83fb8bdb70408ccb1d0d62f47e1a`  
		Last Modified: Fri, 14 Nov 2025 03:18:15 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11` - unknown; unknown

```console
$ docker pull maven@sha256:ca98e47bb3ba0de8be3f59a0e01e09248967a2b8e123d4a439d3c9c7ecffd5c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6956109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5920cb68a8b80ff1ce1472b849a4cfa0db37088eee1a4aefa08de3415858a45`

```dockerfile
```

-	Layers:
	-	`sha256:8435d0ca3ac45acebe2508708b9baca6502732f68630c250de9e982a330b2eb5`  
		Last Modified: Fri, 14 Nov 2025 06:27:45 GMT  
		Size: 6.9 MB (6937767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8d33e6c079eeaedb2b8ef20636babbfe6133c38c1158c902c5bb301b38cb75`  
		Last Modified: Fri, 14 Nov 2025 06:27:45 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
