## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:49acab6774d2964b3f7df00f548726bedd8fc59e9b496450f222ac15fa00642e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:4abf40a66b9f70cd44d7552eeffa287c60fec84f2b06a276b5d67d14acd3223e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **429.8 MB (429781191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9237921c212bfeaf69036df529fd07ab01ddb8fa12f4ec989d6389a9f9c9f92`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:26 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:26 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:12:50 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:12:50 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:12:50 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:12:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:14:18 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 03 Mar 2026 00:14:27 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 03 Mar 2026 00:14:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 03 Mar 2026 00:14:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:14:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:14:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 03 Mar 2026 00:14:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 03 Mar 2026 00:14:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 03 Mar 2026 00:14:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 03 Mar 2026 00:14:27 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 03 Mar 2026 00:14:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 03 Mar 2026 00:14:27 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 03 Mar 2026 00:14:27 GMT
ARG USER_HOME_DIR=/root
# Tue, 03 Mar 2026 00:14:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 03 Mar 2026 00:14:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 03 Mar 2026 00:14:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:369d025c034936d3f19b9a4b859b983f355f304e2e95b16c4cbeb64c69d301c0`  
		Last Modified: Thu, 19 Feb 2026 18:52:05 GMT  
		Size: 63.0 MB (62960229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89257e0640a148754b27ea19438c565af935054d2354ace1f7ecc2c7e2d9b538`  
		Last Modified: Mon, 02 Mar 2026 23:13:08 GMT  
		Size: 152.5 MB (152455379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec0ebae23fb7948b4cce7891f06e32160b174598c58ee205200d3facdbf276fc`  
		Last Modified: Tue, 03 Mar 2026 00:14:56 GMT  
		Size: 175.0 MB (174969679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072e6eb21dac4fad0f0901d82ea9c0ebac401b4047ce1aa3dce0a0c2ed1e5b19`  
		Last Modified: Tue, 03 Mar 2026 00:14:53 GMT  
		Size: 30.1 MB (30082608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9155963911d873bd8ad323ac19271a49d2596e8a92a27f6a60b0d05b60994db6`  
		Last Modified: Tue, 03 Mar 2026 00:14:52 GMT  
		Size: 9.3 MB (9312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5046abef48e58f03e07ee7b5f0f0da93eec82f1a41a086a661049634e83160ff`  
		Last Modified: Tue, 03 Mar 2026 00:14:52 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c6654222a38d325245fe36e19174f46728e7ed6839201297826f2577792f8c`  
		Last Modified: Tue, 03 Mar 2026 00:14:53 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:7ad97d42e2f0de14d596892fe5d7c2378c8bc1f6764d74fee7fe6b1da54e2991
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c895b3702053d3a6cc062a5945aa7edc1d0848919b786e1c0320f028077d78`

```dockerfile
```

-	Layers:
	-	`sha256:2e581459070b1879d53fad6a2a7e3abe17ac801ea82798a5fff319e4f4c7ad18`  
		Last Modified: Tue, 03 Mar 2026 00:14:52 GMT  
		Size: 6.9 MB (6932261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbad449c87aaac9914df1d55ae5ee49104db627e810caf133f5d1f049d9e4756`  
		Last Modified: Tue, 03 Mar 2026 00:14:52 GMT  
		Size: 18.2 KB (18194 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b30feb1e3c6da006bd5dcd87cd4bdd8010969a89f62ecd15cf3d1bf435464f65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.9 MB (406929642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b3f4634e7d351861c82ed1492565fe3d5b5f1b18b9041a888bc71ef6b858adb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:30 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:30 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:14:46 GMT
ARG version=17.0.18.9-1
# Mon, 02 Mar 2026 23:14:46 GMT
# ARGS: version=17.0.18.9-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Mon, 02 Mar 2026 23:14:46 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:14:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 03 Mar 2026 00:14:42 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Tue, 03 Mar 2026 00:14:50 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 03 Mar 2026 00:14:50 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 03 Mar 2026 00:14:50 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:14:50 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 03 Mar 2026 00:14:50 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 03 Mar 2026 00:14:50 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 03 Mar 2026 00:14:50 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 03 Mar 2026 00:14:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 03 Mar 2026 00:14:50 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 03 Mar 2026 00:14:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 03 Mar 2026 00:14:50 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 03 Mar 2026 00:14:50 GMT
ARG USER_HOME_DIR=/root
# Tue, 03 Mar 2026 00:14:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 03 Mar 2026 00:14:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 03 Mar 2026 00:14:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ce260c9faa157afc8e59fa056130319824fd1c549b337649ecc964c38a8d7b19`  
		Last Modified: Fri, 20 Feb 2026 15:17:29 GMT  
		Size: 64.8 MB (64811411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66a6f64c6c904e9ef9b020d55ef2c8e5977ab0ae43c95f0454e34c21342702b`  
		Last Modified: Mon, 02 Mar 2026 23:15:09 GMT  
		Size: 151.0 MB (150975227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eb5073510426403afc8d0e50d92405badc3dc362f4cd18adacdbe1a9e5d06e`  
		Last Modified: Tue, 03 Mar 2026 00:15:16 GMT  
		Size: 150.6 MB (150611776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b2944207643f2983acda18f477f166ff2bb914dd9ae162a2b00c62eaa8c7ed`  
		Last Modified: Tue, 03 Mar 2026 00:15:13 GMT  
		Size: 31.2 MB (31217928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a5dc7b2120f111d3faab30d109fc19f2cb2470f1987d2e5a06902f1cca540a`  
		Last Modified: Tue, 03 Mar 2026 00:15:12 GMT  
		Size: 9.3 MB (9312257 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f26b0fccfc84a2b03a4bba1cb7f1e81db92df2d0dcb4976753aa7a51750484`  
		Last Modified: Tue, 03 Mar 2026 00:15:11 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a6bf1abd0b22edb75a6807532f161ed9cbe471a0db26d90ebb4235dcbb4134`  
		Last Modified: Tue, 03 Mar 2026 00:15:13 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:3825663377ec703ee6d310a3f97d922c92e0d197d6db8899949a0e20a066fbe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6948002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ff2535fd78d9c7963ca0d0b17090a174c4073ac5a48f7e2b8b2d8d839057b7`

```dockerfile
```

-	Layers:
	-	`sha256:7bf5a8eda1fea6cfa01c934aa7fa3b900d67520fb3c9344bd93eed7e45880b4a`  
		Last Modified: Tue, 03 Mar 2026 00:15:12 GMT  
		Size: 6.9 MB (6929660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77153075b1d8600fd100a0b93d4093b94281fb4f364e55f0e182535888b583db`  
		Last Modified: Tue, 03 Mar 2026 00:15:11 GMT  
		Size: 18.3 KB (18342 bytes)  
		MIME: application/vnd.in-toto+json
