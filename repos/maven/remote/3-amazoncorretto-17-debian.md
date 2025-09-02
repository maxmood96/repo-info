## `maven:3-amazoncorretto-17-debian`

```console
$ docker pull maven@sha256:fac2b67bace45ca2f8fea7136085c394891e4212eaa257db634263efb9fff2e2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-debian` - linux; amd64

```console
$ docker pull maven@sha256:53c542541a3b8ea9b966f16a5825bb616adce7e7fd1d9baccf1d90d7767133d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.9 MB (239900422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1e57350808fd210958b37e3f0adec2fe9e02bc232b514bf243ba6c92b287fe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 14:41:45 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 14:41:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 19 Aug 2025 14:41:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 19 Aug 2025 14:41:45 GMT
ARG USER_HOME_DIR=/root
# Tue, 19 Aug 2025 14:41:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 19 Aug 2025 14:41:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 19 Aug 2025 14:41:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:396b1da7636e2dcd10565cb4f2f952cbb4a8a38b58d3b86a2cacb172fb70117c`  
		Last Modified: Tue, 12 Aug 2025 20:45:08 GMT  
		Size: 29.8 MB (29773285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9af713715e4e650d9a68ce149312d2636eb31307887529e799e1f0759035f9d0`  
		Last Modified: Tue, 02 Sep 2025 02:34:29 GMT  
		Size: 200.9 MB (200883525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203fe249e727c4db9e62e883e6cee973ae28f3abd0575b7edd3c6bd033b017aa`  
		Last Modified: Tue, 02 Sep 2025 02:34:30 GMT  
		Size: 9.2 MB (9242575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487a001a71f21e35f52c2af7a53cc80975f96010c43bdf5a0aec5ba64a0a0201`  
		Last Modified: Tue, 02 Sep 2025 02:34:09 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbcedaee45a6721be889c8dc0a2db484f5626225421ce42c6892f530077cfc3`  
		Last Modified: Tue, 02 Sep 2025 02:34:09 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:8ea4dfd3b24b9229a590106843852293810c91c64671d23e1b0b495099c4fea2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3119752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a8a3d1d8a66856a7b464eb52087a24605c0b30e824ca21054538de6b8291c1`

```dockerfile
```

-	Layers:
	-	`sha256:24aad4b88179183e59244a52d0a094888ed9598eb77a1411f7c1b6594bf1ec4a`  
		Last Modified: Tue, 02 Sep 2025 02:28:06 GMT  
		Size: 3.1 MB (3100509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5fea9124df17c4bc4cc6160ba06c7ddfbcd148e4fe0f18862f2873c79ff3706`  
		Last Modified: Tue, 02 Sep 2025 02:28:07 GMT  
		Size: 19.2 KB (19243 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-debian` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0c2ad26fde23895b723e17d4e49e88fb8a8ff671999bcbbbb7f8fc1373aae567
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.7 MB (238690901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b36ed120707857d07d533c1836020615ee8db73a39f33c02dbbf46cdc7300d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1754870400'
# Tue, 19 Aug 2025 14:41:45 GMT
RUN apt-get update   && apt-get install -y curl gnupg openssh-client   && export GNUPGHOME="$(mktemp -d)"   && curl -fL https://apt.corretto.aws/corretto.key -o corretto.key   && echo '5fdaed0a262b975776b1d5c0170d2e86b1be1e98b27ef97114b04ec9ac7f011d *corretto.key' | sha256sum -c -   && gpg --batch --import corretto.key   && rm corretto.key   && gpg --batch --export '6DC3636DAE534049C8B94623A122542AB04F24E3' > /usr/share/keyrings/corretto.gpg   && unset GNUPGHOME   && echo "deb [signed-by=/usr/share/keyrings/corretto.gpg] https://apt.corretto.aws stable main" > /etc/apt/sources.list.d/corretto.list   && apt-get update   && apt-get remove --purge --autoremove -y curl gnupg   && apt-get install -y java-17-amazon-corretto-jdk   && rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ENV LANG=C.UTF-8
# Tue, 19 Aug 2025 14:41:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 19 Aug 2025 14:41:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 19 Aug 2025 14:41:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 19 Aug 2025 14:41:45 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 19 Aug 2025 14:41:45 GMT
ARG USER_HOME_DIR=/root
# Tue, 19 Aug 2025 14:41:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 19 Aug 2025 14:41:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 19 Aug 2025 14:41:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9a6263cdeaa5d408640880103ee36920ef814974ca8e2674412ad6460e8968c9`  
		Last Modified: Tue, 12 Aug 2025 22:12:42 GMT  
		Size: 30.1 MB (30136044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4279da9e2faf9d6d0e9c34cd393b86a36f36453abdd70714f3dd8ae160cddb46`  
		Last Modified: Wed, 20 Aug 2025 20:29:23 GMT  
		Size: 199.3 MB (199311227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a24b587ae41b33119195a41f416defcf373111200689681ba8a9d2b1c6cc51a`  
		Last Modified: Wed, 20 Aug 2025 18:40:01 GMT  
		Size: 9.2 MB (9242592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b52f00d6f64ed429e0fef36ae8dad6fa62cb8800765752baaee9c4c52e147c52`  
		Last Modified: Wed, 20 Aug 2025 18:39:59 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8ec4ab50e0335a3b1edad8f98f2fd43c0a2b9db02ead368a0474873c2839581`  
		Last Modified: Wed, 20 Aug 2025 18:40:01 GMT  
		Size: 155.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-debian` - unknown; unknown

```console
$ docker pull maven@sha256:e190dbb6e2be95846ee16401d03606e454d425e247811fd016ab82f72741edba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3119584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3586d3a1b0ebfcea62f635802402f38d12cb431f7441c63837a3be7cdc2da563`

```dockerfile
```

-	Layers:
	-	`sha256:3a9266f9d3d3348fd8f1a2d82ef526812405c5042ba9c623fa192d92ab481c38`  
		Last Modified: Wed, 20 Aug 2025 20:27:42 GMT  
		Size: 3.1 MB (3100172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27aa2644fef146c301139a054b8bac461f1e1ae4580d5f18173877091419e21d`  
		Last Modified: Wed, 20 Aug 2025 20:27:42 GMT  
		Size: 19.4 KB (19412 bytes)  
		MIME: application/vnd.in-toto+json
