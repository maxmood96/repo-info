## `maven:3-amazoncorretto-17`

```console
$ docker pull maven@sha256:16eed6e8e75b4f599068965fc71098414cde44f32347ea0645607fd21f19b988
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17` - linux; amd64

```console
$ docker pull maven@sha256:7ecb83c2c0d7016081dd1d8d4441e87339641560b12a4126fe617d099d65da92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406745989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75aff4845819f26a5fe764dc900214e99269af18b15a8e00fb1cc82bd180f7c1`
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
	-	`sha256:8fab1cd53a92a9e8bbd717880f65104f330d69b3b7bc74d2439deb4798c25ba6`  
		Last Modified: Wed, 15 Jan 2025 16:59:20 GMT  
		Size: 62.6 MB (62633179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b25e5a5e8184efd859efeed63e15791b161f258c3a330bd9c6a7e13dc3e4e2`  
		Last Modified: Wed, 15 Jan 2025 18:31:16 GMT  
		Size: 151.6 MB (151606628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb6bdbcad1b70654a5695bc9b45b8b2aa4efe0c2a438ad93f8c95108bbb58049`  
		Last Modified: Wed, 15 Jan 2025 19:10:09 GMT  
		Size: 153.3 MB (153283743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8ebdedbfcd6a2bcd7cccd2c21329cbef843a48ca6a722564be0f4a1509ee00f`  
		Last Modified: Wed, 15 Jan 2025 19:10:07 GMT  
		Size: 30.1 MB (30050957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6accac6c2c10e5f5e2b408e05ced595c986b736715fee9f873bb1e23d34e1225`  
		Last Modified: Wed, 15 Jan 2025 19:10:06 GMT  
		Size: 9.2 MB (9170438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47869d75e2fcb50f28f243902ca475e70f3a38f6e8552c75ebfd1574e950a50e`  
		Last Modified: Wed, 15 Jan 2025 19:10:06 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b812b7ddcac6d8aa88a35fa11512cdee07c112f7291c67c676e17f5e9013c4ed`  
		Last Modified: Wed, 15 Jan 2025 19:10:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

```console
$ docker pull maven@sha256:5b53ff57717d5cffb66c313c3fce6a77a33763f67384d16891cab966b582419d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6927938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d21f8d69d6553d2079910d69529a5bed6ef9b86e2875f421cf4c27ecb0ad34f3`

```dockerfile
```

-	Layers:
	-	`sha256:fa5c2ef2dbf15e667e490fd60e81490f9864a249ee0f27a07e27678962e14942`  
		Last Modified: Wed, 15 Jan 2025 19:10:06 GMT  
		Size: 6.9 MB (6908437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5ce7472d3c51ac67d47b12e737145b2651244dd900351017a04aad0bcd8cc05f`  
		Last Modified: Wed, 15 Jan 2025 19:10:06 GMT  
		Size: 19.5 KB (19501 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17` - linux; arm64 variant v8

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
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d3c3d5e7dd2769ec34c8a6782da13cd2fb91d9f2b7326bd873b4ffb1120d5f`  
		Last Modified: Sat, 11 Jan 2025 03:03:46 GMT  
		Size: 150.2 MB (150244756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80262a9d7aae077157cfc3d984816eb191e5323f9185eecad73d5173b21bc36`  
		Last Modified: Sat, 11 Jan 2025 03:58:42 GMT  
		Size: 129.3 MB (129275314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c206e2a3f1de41d281f80d6571324c90722a70f0631c59f5bb7949a367f932c0`  
		Last Modified: Sat, 11 Jan 2025 03:58:41 GMT  
		Size: 31.2 MB (31196395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5115403ff5d4a355b93dada24b1253e0354e27e626759ad8cdb1c3817e8dab`  
		Last Modified: Sat, 11 Jan 2025 03:58:40 GMT  
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
		Last Modified: Sat, 11 Jan 2025 03:58:41 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17` - unknown; unknown

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
