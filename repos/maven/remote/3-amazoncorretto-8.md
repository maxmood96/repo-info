## `maven:3-amazoncorretto-8`

```console
$ docker pull maven@sha256:8377510ae2e2004171d15b2358055a0322e0f9b74e6f7f7aed0dee536849c81f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8` - linux; amd64

```console
$ docker pull maven@sha256:93bc42205c7b423a093b866214074521bf771c592c5e0f03b92a6fdfb4ceddf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330801573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24e40ebad44cd2a7b8fa06ea8adeb127e467610d52a6e97e3d11890f95de2f00`
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
	-	`sha256:2ddc0aa2636ed19b988b4176374929a92f5862f6c6e88ea255d352140af781e6`  
		Last Modified: Fri, 17 Jan 2025 20:13:56 GMT  
		Size: 62.6 MB (62648554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857466e9d40e7d7de6e3e5fa7d4f2af30505a7d901e19a6df289cbce9d57ba75`  
		Last Modified: Thu, 23 Jan 2025 23:07:57 GMT  
		Size: 75.6 MB (75592068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ff517ea351ecad261cc5b1dba6d52b2757cdddf863b5a1a67a4a19675564fc`  
		Last Modified: Fri, 24 Jan 2025 00:08:43 GMT  
		Size: 153.3 MB (153314031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53c4862840fcb2c1ae3cbaea5493c1fb6fad01836fd5e2ef6eb293dfa4f94483`  
		Last Modified: Fri, 24 Jan 2025 00:08:40 GMT  
		Size: 30.1 MB (30075447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4362d49ef0a9978d0c154407cd69671e33826335c411dc07fd15b98b4e3e0a0`  
		Last Modified: Fri, 24 Jan 2025 00:08:39 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473f6718f23f6ef6f6272c5a12007815ff9dd17c6480d2912c3d4aec4f26d60b`  
		Last Modified: Fri, 24 Jan 2025 00:08:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:698d9d1b94b31f1fd20124c89e128b777733f6845f808dc0d5e798a052ccfdbe`  
		Last Modified: Fri, 24 Jan 2025 00:08:40 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:9aa2d79605db62aeb5d2e8d92e17cadf7087982dc0b2defea0315453a4b0866c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6767540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a71dc16e7e800d5ef42cc77a37d00181312ef57a3f9ba7518e1f70a087afe2ca`

```dockerfile
```

-	Layers:
	-	`sha256:da9e69a163ade416db318a15db226fe0582fdf34af4b9ac9ecfaf4b9a4ab797c`  
		Last Modified: Fri, 24 Jan 2025 00:08:39 GMT  
		Size: 6.7 MB (6749321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45359be4e80fed886d76cd90942e77d8f6f91fb79c2f901c5c684893046915ce`  
		Last Modified: Fri, 24 Jan 2025 00:08:38 GMT  
		Size: 18.2 KB (18219 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b138a0483408b50fd7dd787f43aada2dfb6bc6b3c2f1e5d8cf94aea99d2b7cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.9 MB (293905336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be00f64c1b9af86f5b36920fe6d08afdd528aeab039392b5d63b476e66890cc3`
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
	-	`sha256:dc3d403853487343f06bffefe21e65d842f88da2d7a1073ba2820fdb1b7ece72`  
		Last Modified: Fri, 17 Jan 2025 20:14:11 GMT  
		Size: 64.6 MB (64590432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f60d3a27242629037dafdbc0af3eeee6045ae663cafb36f1e43b48efbe4fd5`  
		Last Modified: Thu, 23 Jan 2025 23:07:53 GMT  
		Size: 59.7 MB (59671140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:072947990c1a5c8a4725a5945780ceaf630816acf591e8dc2c4fba689e912293`  
		Last Modified: Fri, 24 Jan 2025 00:36:56 GMT  
		Size: 129.3 MB (129285321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d290c7e285aea9a0ce089f18a71eb59bef785a39593b49c1d542967e81d1fd00`  
		Last Modified: Fri, 24 Jan 2025 00:36:53 GMT  
		Size: 31.2 MB (31186967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8d81f79ab3bc77cd1d1bd44c2727caeba0e18571b71de42d706ef440121001`  
		Last Modified: Fri, 24 Jan 2025 00:36:53 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e5a5ff59ab4a5c8d0c1c24b2b1f3ed7cfa26da56fa3a57f4e8777db85b2eac`  
		Last Modified: Fri, 24 Jan 2025 00:36:52 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cea81ee35f09e97e96c21fd03c6811f785b33da0f5e9f37f54e0b06423c9daf`  
		Last Modified: Fri, 24 Jan 2025 00:36:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8` - unknown; unknown

```console
$ docker pull maven@sha256:88ab5e9d76da9d371d620d522d6f8c9217a07339d6cb65e6a996f37d6a6300c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6744885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac16a5b96e39fd2d9527820d269036f7dddbd746d2d0cb04c74fda3ca39dc899`

```dockerfile
```

-	Layers:
	-	`sha256:92917e0b553cdc444ec52e4c9af0db3bcb7f2a3622f3584ec57d2285bf2be9b3`  
		Last Modified: Fri, 24 Jan 2025 00:36:53 GMT  
		Size: 6.7 MB (6726518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4e3bcbf8b5f57ff95d89ccf58d494f81e33a080e7e081911846f4c8c613c9a2`  
		Last Modified: Fri, 24 Jan 2025 00:36:52 GMT  
		Size: 18.4 KB (18367 bytes)  
		MIME: application/vnd.in-toto+json
