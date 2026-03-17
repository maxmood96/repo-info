## `maven:3-amazoncorretto-25-debian-trixie`

```console
$ docker pull maven@sha256:3f48dafac5c42e4a62d1a4b125664024050a6d5c41812a8ebfc3cbe5a20cf7ef
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-debian-trixie` - linux; amd64

```console
$ docker pull maven@sha256:95adbc40f9370bd365cb6093bb15e2ea81b0b9381636dd2ee2b90b8f8b7244ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.4 MB (274364921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a33e3ca76306cf45f4ad31aa8769b2ccca235091d802319277cfe4f9cea636eb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:49:23 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:49:24 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 03:49:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 17 Mar 2026 03:49:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:49:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:49:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:49:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:49:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:49:24 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:49:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:49:24 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:49:24 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:49:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:49:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:49:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d8a3e3c24705de3b08c6e6b13c8dc0577b64c695695e239c8d9039f4d324a0`  
		Last Modified: Tue, 17 Mar 2026 03:49:49 GMT  
		Size: 235.3 MB (235277214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9a6dd831fdd3d6c2287f84444a05d483cfa2365be671147aa5e04106a6233d`  
		Last Modified: Tue, 17 Mar 2026 03:49:44 GMT  
		Size: 9.3 MB (9311177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ac6bd5cc1497a66432a5dec8bf69f55ea6c9a2072a2cd34e6f13364c73a5132`  
		Last Modified: Tue, 17 Mar 2026 03:49:44 GMT  
		Size: 845.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:751e1854a0c118aba46c471231c774bc4bf668e768af7a58fc18bb77ec62185f`  
		Last Modified: Tue, 17 Mar 2026 03:49:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:cef2619b1d2d06f232ece07d8b6f519152055b377299a48b17bb18dbec31afa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a5dd1bf08aaf7d566ba237c0afba61d63af1dd5e775f1b85ec3c563b573121`

```dockerfile
```

-	Layers:
	-	`sha256:7332b11530b2d42f27a3d89e4f8ba3bf8c1bd438bef9860e075d5193c426ca6f`  
		Last Modified: Tue, 17 Mar 2026 03:49:44 GMT  
		Size: 3.1 MB (3113090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f15d068c81f0f2c6ca6baeff0ab2f4f037a6f71d074e2d9d511ff005b5934308`  
		Last Modified: Tue, 17 Mar 2026 03:49:44 GMT  
		Size: 19.2 KB (19199 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-debian-trixie` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:440bd507dcf92d4374c71531669af662a27845daf43981e3fcc8f3639d9116a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **272.5 MB (272478995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c40a91b34dcd4fe79a076f4ce0903ec3662e513be8eea2d916bcd5e32f49e4a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 03:49:45 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '6db32832d82839d368181ae730df7d642b0bff161277f0ab6023359d347cca6b *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-25-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 03:49:45 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 03:49:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 17 Mar 2026 03:49:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:49:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:49:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:49:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:49:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:49:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:49:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:49:45 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:49:45 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:49:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:49:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:49:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e8d03310d109e723371b83c4c1fdc6721a56885f22175fa42557368ea20415b`  
		Last Modified: Tue, 17 Mar 2026 03:50:11 GMT  
		Size: 233.0 MB (233028368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dcb88b939c931dcc31800c8b29bbf37fd6d8d7fde2397a6a1360a32f06497b9`  
		Last Modified: Tue, 17 Mar 2026 03:50:07 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed8eb3210781af6d2d99227baf8da1823eb08f937722e89917d4196270bfc0`  
		Last Modified: Tue, 17 Mar 2026 03:50:06 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fda75b5e59e6a7dfc1cbe215143558c2483ad78f7f36ea37e62e2904d7d6d4b`  
		Last Modified: Tue, 17 Mar 2026 03:50:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-debian-trixie` - unknown; unknown

```console
$ docker pull maven@sha256:031dcc5f8206e5f91348b4245860e5e08638f76f91ec7d54a33eceb7f2dc70ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3132119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ecb446ba85c77ff99af84a97c9cf65d3cffc8aae7721ac15dec0964fd2422d`

```dockerfile
```

-	Layers:
	-	`sha256:244e40f0ed8f18fbd2f2038d9e033032ea9ac6479bfa5f418f0e60b52fbe31f8`  
		Last Modified: Tue, 17 Mar 2026 03:50:07 GMT  
		Size: 3.1 MB (3112750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82838a45948d0cf8be2323776b9cb4f14510bc726be7eeb6e19d2f71439d4f0d`  
		Last Modified: Tue, 17 Mar 2026 03:50:06 GMT  
		Size: 19.4 KB (19369 bytes)  
		MIME: application/vnd.in-toto+json
