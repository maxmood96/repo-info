## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:faceaefc36ca7b29ce599ab179e1b1b2dc9063b70a7d2e5530296f229ff1a43a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:6feabfde17656763211ae131f05e3f2467c2518c04e0856da4f5dca1e2ae2e94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406741095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f184538339475349c2c4d890be92a4976f32f6e079b28ec5294fc58a0f46f81`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.13.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Tue, 14 Jan 2025 20:33:04 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ff001010b923a0181362a7f37e350a3085467a2b774e124a0214de57212325`  
		Last Modified: Tue, 14 Jan 2025 20:34:19 GMT  
		Size: 151.6 MB (151604378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:144c286d0b375cd8733a6a0a75418c09c786d1d5b3388ef4ceadefbcac2d2111`  
		Last Modified: Tue, 14 Jan 2025 20:35:38 GMT  
		Size: 153.3 MB (153279668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d121e1800e9914522afbf432fd145a6f990e26acdadd5587b21f136e88cb4df`  
		Last Modified: Sat, 11 Jan 2025 03:09:16 GMT  
		Size: 30.0 MB (30049737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62948598726336adc91456c5a90fb78fdd412be9f207c8a6127e4efb510dc04`  
		Last Modified: Sat, 11 Jan 2025 03:09:15 GMT  
		Size: 9.2 MB (9170438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb156ac2b07cc08379d61104ad099e3e4ac971156595791ffa8e3093dc26963`  
		Last Modified: Sat, 11 Jan 2025 03:09:14 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ac6af8ee600c5a4cfde1a92b628bb2bba373eb93c29d1b5e3c45c7eadc1a2c`  
		Last Modified: Tue, 14 Jan 2025 20:37:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:05f8e7f4419017c848e38d634d0ca2fc410fab6afb5e6e4028829bec307631d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6927939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2790f40f74fd1b323118ff8c87e5d7476217383f4cb315bec79f88628b0b3c03`

```dockerfile
```

-	Layers:
	-	`sha256:f87cf03db4ebd689dabf11a205c9ad892d4eb8e097908ebf427bc955e753cd2b`  
		Last Modified: Sat, 11 Jan 2025 03:09:15 GMT  
		Size: 6.9 MB (6908437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e4ab8ead3522f56f64e5c9f892f8de5abb5e604530c6af1fb98734c701a32a5`  
		Last Modified: Sat, 11 Jan 2025 03:09:14 GMT  
		Size: 19.5 KB (19502 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5130d6aa44fd4f69d9946eed810ead2cb93c53d9e06ac6dbf4f95eaabfa79344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384478250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a80e80f8a8b272e2577e8a885bb28aee30978c38f8376a8dcf992dcc73240c4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.13.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export GNUPGHOME="$(mktemp -d)"     && curl -fL -o corretto.key https://yum.corretto.aws/corretto.key     && gpg --batch --import corretto.key     && gpg --batch --export --armor '6DC3636DAE534049C8B94623A122542AB04F24E3' > corretto.key     && rpm --import corretto.key     && rm -r "$GNUPGHOME" corretto.key     && curl -fL -o /etc/yum.repos.d/corretto.repo https://yum.corretto.aws/corretto.repo     && grep -q '^gpgcheck=1' /etc/yum.repos.d/corretto.repo     && echo "priority=9" >> /etc/yum.repos.d/corretto.repo     && yum install -y java-17-amazon-corretto-devel-$version     && (find /usr/lib/jvm/java-17-amazon-corretto -name src.zip -delete || true)     && yum install -y fontconfig     && yum clean all # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
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
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Tue, 14 Jan 2025 20:35:27 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d3c3d5e7dd2769ec34c8a6782da13cd2fb91d9f2b7326bd873b4ffb1120d5f`  
		Last Modified: Tue, 14 Jan 2025 20:38:32 GMT  
		Size: 150.2 MB (150244756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80262a9d7aae077157cfc3d984816eb191e5323f9185eecad73d5173b21bc36`  
		Last Modified: Sat, 11 Jan 2025 03:58:42 GMT  
		Size: 129.3 MB (129275314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c206e2a3f1de41d281f80d6571324c90722a70f0631c59f5bb7949a367f932c0`  
		Last Modified: Tue, 14 Jan 2025 21:59:49 GMT  
		Size: 31.2 MB (31196395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5115403ff5d4a355b93dada24b1253e0354e27e626759ad8cdb1c3817e8dab`  
		Last Modified: Tue, 14 Jan 2025 20:50:55 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebcfe95ae80b7975f833cbc80fdde4c8900d43ee7fe1c43e6a59e4309de755a`  
		Last Modified: Sat, 11 Jan 2025 03:58:39 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cb389487b2fd0509d53542c80592d65db047f439ff17c0ae737c45cd8ea420`  
		Last Modified: Tue, 14 Jan 2025 22:26:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:bbaf06e04406b6e1eeb09f62aa8a8633b84e6f6bfd564589a7977f7743b4783a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6925582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7b59126ac29a755cfb3c6db56bf4d6a20b743ab6965de8f262d14b22cc77a95`

```dockerfile
```

-	Layers:
	-	`sha256:9eb79a8f0cdbb4244b1e46c8ea4d1c374eb0fc58d0c0661034281b37094abf02`  
		Last Modified: Sat, 11 Jan 2025 03:58:40 GMT  
		Size: 6.9 MB (6905884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3533ae5945a5fbc5c2c7926fdc0775af83bf7da6de89173f8bf9f20aec4219ca`  
		Last Modified: Sat, 11 Jan 2025 03:58:39 GMT  
		Size: 19.7 KB (19698 bytes)  
		MIME: application/vnd.in-toto+json
