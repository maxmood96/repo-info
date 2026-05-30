## `maven:3-amazoncorretto-21`

```console
$ docker pull maven@sha256:9e8aa99b4a55060004696aea04eb698ffaf3098752d682f56dd73cca0ed7dae4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21` - linux; amd64

```console
$ docker pull maven@sha256:707c77065852ed381920789a5ca2b955798c7b05d88d263ac98e06b56ed5670a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **448.0 MB (448011506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ed2bbc49eaa77b04a9d3b8e04f3c0dd74b54d62bf733781b1dd349dc725631`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:27:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:27:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:12 GMT
ARG version=21.0.11.10-1
# Sat, 30 May 2026 01:12:12 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:12:12 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 30 May 2026 02:14:37 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 30 May 2026 02:14:44 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 30 May 2026 02:14:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 30 May 2026 02:14:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 30 May 2026 02:14:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 30 May 2026 02:14:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 30 May 2026 02:14:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 30 May 2026 02:14:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 30 May 2026 02:14:45 GMT
ARG USER_HOME_DIR=/root
# Sat, 30 May 2026 02:14:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 30 May 2026 02:14:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 30 May 2026 02:14:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c385119c2f2941b8af70a64eacbaf2f0ddf73bcef9afe5084b40aca94bccda`  
		Last Modified: Sat, 30 May 2026 01:12:32 GMT  
		Size: 165.8 MB (165760940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e921beed0c385998724023f50ed99d4d2517ffb578a6ec15e84d699fed9bafff`  
		Last Modified: Sat, 30 May 2026 02:15:14 GMT  
		Size: 179.9 MB (179891972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2204f8c07870e3bcefa3dfeb5f0736cb6a4d9b12de1adddfbf37a6fd3ba0db`  
		Last Modified: Sat, 30 May 2026 02:15:10 GMT  
		Size: 30.1 MB (30055652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12848a9b36a4b2a0253f35149517968aec50cf29331434d08f61b2d1374fdc84`  
		Last Modified: Sat, 30 May 2026 02:15:09 GMT  
		Size: 9.4 MB (9359981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e33c1f4009aed6f792a36fcacafebe384cbf1f6c61f9cb5b7d1179a6c785e7a`  
		Last Modified: Sat, 30 May 2026 02:15:08 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698ec05c9cfa3e6aedfc61946c001b9b275fa738480b6542a26386b6efbedab2`  
		Last Modified: Sat, 30 May 2026 02:15:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:d5d047c7a0f8afe6f94383b15686080599b616fc5cf5251bcb60dd8f095499ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6949286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77a46342af8f92169c4527ca2edbda09ab27d53eab012b86c16740bb9525a230`

```dockerfile
```

-	Layers:
	-	`sha256:74c23112f090c1bf1434b4e38c3535eb36692bcd4b9c17c7dd111072ac0523fc`  
		Last Modified: Sat, 30 May 2026 02:15:08 GMT  
		Size: 6.9 MB (6933068 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7225b073147e93818aa5765ba126af80770ac5b47bebfc02cdbd08d799a2a72c`  
		Last Modified: Sat, 30 May 2026 02:15:08 GMT  
		Size: 16.2 KB (16218 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d65de6446c5c026727b8a5952f6e6bef272336c5f7b056920edc47f40006dc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.7 MB (424714588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b3a2c4faf2cc11c21e27c4c4d93cac593e252568f3aad4a5121aa559021fd0e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:29:01 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:01 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:12:12 GMT
ARG version=21.0.11.10-1
# Sat, 30 May 2026 01:12:12 GMT
# ARGS: version=21.0.11.10-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-21-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-21-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Sat, 30 May 2026 01:12:12 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:12:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sat, 30 May 2026 02:14:28 GMT
RUN yum install -y tar which gzip # TODO remove # buildkit
# Sat, 30 May 2026 02:14:36 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 30 May 2026 02:14:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 30 May 2026 02:14:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 30 May 2026 02:14:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 30 May 2026 02:14:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 30 May 2026 02:14:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 30 May 2026 02:14:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 30 May 2026 02:14:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 30 May 2026 02:14:36 GMT
ARG USER_HOME_DIR=/root
# Sat, 30 May 2026 02:14:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 30 May 2026 02:14:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 30 May 2026 02:14:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c908ecabd64b5f3b79616b6d1005e436e80ea25c80a15abfc8cf5fd74147060`  
		Last Modified: Sat, 30 May 2026 01:12:35 GMT  
		Size: 163.9 MB (163903189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76deb5d2b0c1c50e8bad27a51ec30bb16da7beff83459c0b98195d95fe276cac`  
		Last Modified: Sat, 30 May 2026 02:15:03 GMT  
		Size: 155.5 MB (155461170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650004edad0c22354f9cb267e05431573c6faf1ae07ccc9c8de56de75e5df731`  
		Last Modified: Sat, 30 May 2026 02:15:00 GMT  
		Size: 31.2 MB (31198542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc4781aa5af9130b7af7c1b665bc3c816ab7d741dd8eda6240e96333fa4e7f4f`  
		Last Modified: Sat, 30 May 2026 02:14:59 GMT  
		Size: 9.4 MB (9359969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b0222720a4083971892dd1b1085abd5eb651b046fc1a7ad472447fe0a84c433`  
		Last Modified: Sat, 30 May 2026 02:14:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e05662352b2ef8fdd570c3a59affbdd65ff1cb53b1865c7363e5a1baa3914bb6`  
		Last Modified: Sat, 30 May 2026 02:15:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21` - unknown; unknown

```console
$ docker pull maven@sha256:9daebc8a72ada971af9c5c3065f2de7af05f2ba73c217fb73b07e681e4c09ca6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6946833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7e4d6990a91f4d9c5a096ca47457b3b7761ed300ce715736efeacfc8ae387b`

```dockerfile
```

-	Layers:
	-	`sha256:a8b4d80fb78c2de000a2b8728ab251e94f65506bb34f6406424b9631bf6c7e20`  
		Last Modified: Sat, 30 May 2026 02:14:59 GMT  
		Size: 6.9 MB (6930467 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81a891afacb45021e9a1d447c4cb37f9e9852b1fc0fa92503c239e993327f12f`  
		Last Modified: Sat, 30 May 2026 02:14:58 GMT  
		Size: 16.4 KB (16366 bytes)  
		MIME: application/vnd.in-toto+json
