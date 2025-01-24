## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:62cb9416c2dd0269d7c759f46fadccd895e2e6416d8025e8e24ab18fc992d77a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:cf11b6dc591e18a743a9016c53db246f0d3bf21dce450e6bd3be9711736491c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.7 MB (330732078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a2aa5f3268796e0bbf484a84e0efc6b49ebc5796cd6acb0de1e5f7a2c144d3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_442.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_442.b06-1
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
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ff49cdf0051001697eb997ff2a321133bbf5d184ed54b92c88e3d268844908`  
		Last Modified: Thu, 23 Jan 2025 18:27:10 GMT  
		Size: 75.6 MB (75572040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e24c3d1df952c789d99c9596c4ecfe6ad3457382d06b3583085b64832450d97`  
		Last Modified: Thu, 23 Jan 2025 19:27:32 GMT  
		Size: 153.3 MB (153293123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6593d00b485390a9653154e0a5d4f9ce5a5949ca60ca276db679e5a62547f105`  
		Last Modified: Thu, 23 Jan 2025 19:27:30 GMT  
		Size: 30.1 MB (30059608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02533194fe2c520aff865eb8895297da6df699be675c8b0f86b87c4008a34254`  
		Last Modified: Thu, 23 Jan 2025 19:27:30 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6ddb1ce76986f28c594572d49d2cccdc3feab4f8f6e9135fa32bbee4d97716`  
		Last Modified: Thu, 23 Jan 2025 19:27:29 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2979139418c600971d30934e070caee8e0b08577f2085d98d8806d314fe66a94`  
		Last Modified: Thu, 23 Jan 2025 19:27:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:38a72cef3a4dc6214d8a11cc9439b7d67a59f372079872a5093885c215eae2a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:022e1e0ba54738b69d12a04c2cf8af70b81c104efdf6bf15af89bccf84a7a8f1`

```dockerfile
```

-	Layers:
	-	`sha256:03d0c0f677c6934491197f0c913c635e25d849475c1d314766371214f792bbe2`  
		Last Modified: Thu, 23 Jan 2025 19:27:29 GMT  
		Size: 6.7 MB (6749321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e27e733de6f49b958de4fac5017be9a740562aaa3b911748b0846b2bd8f30634`  
		Last Modified: Thu, 23 Jan 2025 19:27:29 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:67e8c525369c0bf4d30505c24da242048d4185b5bbce70c18a8465b15cf48e95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293905307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3f0c50980c43ba201d2f0c3c522e1ff52a02135f5f128838e1117e530cd4f6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_442.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_442.b06-1
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
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a40fc02393a849ecb556016054b90c4bb62c50d5ac13a9617e59cc0d2b432b8`  
		Last Modified: Thu, 23 Jan 2025 18:28:55 GMT  
		Size: 59.7 MB (59671150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:090e77607b4c6e18a54335c3621f29f0cc0172cff6237c20f681caab894f1057`  
		Last Modified: Thu, 23 Jan 2025 20:02:21 GMT  
		Size: 129.3 MB (129285442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6605e1c5a1fa56f0b4ecec7020782bb3a54302d9ffe356c58d0119d2ca0f5ea`  
		Last Modified: Thu, 23 Jan 2025 20:02:17 GMT  
		Size: 31.2 MB (31186937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:508066fd96da7ecab33beb40d0c5119b560471f6965db2251da0b5d1bbc4d25c`  
		Last Modified: Thu, 23 Jan 2025 20:02:16 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1655923154a69b991fa808cc07ca73be338baf583ddba735bef9983d9aaad47`  
		Last Modified: Thu, 23 Jan 2025 20:02:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc642febadd890cfd6adcea3dba861f93263046791c58904818c39eed51b6a10`  
		Last Modified: Thu, 23 Jan 2025 20:02:18 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:1b3dc54e06e965ac47a7328c46638a96e3f45d0986eb0c908cddd31ed97e959b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6744885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31331beb4b0aafb7fa8b9782ca9ae947ec155bd85ab676a388012d55b780fc7`

```dockerfile
```

-	Layers:
	-	`sha256:453bb96f2a137da2d52947ac08c8a8f395f6ff438fd4dc3fd8f653305ea70abc`  
		Last Modified: Thu, 23 Jan 2025 20:02:16 GMT  
		Size: 6.7 MB (6726518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5de8ca764eff889e6db349af3e14fc5bc64d94877dbf6088738daf68348de247`  
		Last Modified: Thu, 23 Jan 2025 20:02:15 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json
