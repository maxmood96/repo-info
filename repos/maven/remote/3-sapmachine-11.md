## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:7a92c73095aa48425c4ead435781e8f369d95daf4f4a68ac1293280a46b78b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-sapmachine-11` - linux; amd64

```console
$ docker pull maven@sha256:6542110ee45cdb876483a032bfa6b3a9a22964bdae07a7430db975b53aff9a4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.4 MB (267423834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405e485aa986b0d672bc2052f1f30e63b66948cf558167b35c5ef1adb6b2e83d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Apr 2024 16:38:00 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:38:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:38:01 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:38:02 GMT
ADD file:ac9d5a9d5b9b1217a6b26f1069a16bc48fa9c2ed76f3eaf28a8e643ae2058d11 in / 
# Mon, 29 Apr 2024 16:38:03 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 22:49:49 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 14 May 2024 22:49:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 14 May 2024 22:49:50 GMT
CMD ["jshell"]
# Mon, 27 May 2024 15:57:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ad8384cb7b1cac0192e1b130cd938a1a3096bf52dc4b8094dd97fbce62c502`  
		Last Modified: Tue, 14 May 2024 23:07:38 GMT  
		Size: 201.1 MB (201073974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c619310fefc37ed977bc378057fce8e69dab2101cd2ebb39a88e01a2037e7cef`  
		Last Modified: Tue, 28 May 2024 19:59:15 GMT  
		Size: 27.0 MB (26998482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d33c2be4637b0e6e8ed113ce0bdf561037147a11119d4197fbcd5a47406691b`  
		Last Modified: Tue, 28 May 2024 19:59:11 GMT  
		Size: 9.6 MB (9647556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:340d1f2d01eedd3a3f4b0ed07176e02c442df65d945130703877be61aaca68c5`  
		Last Modified: Tue, 28 May 2024 19:59:10 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d6c661b2bad93d5a5f09565a0af7ba55949457213b9797af6e7bb2ba591208`  
		Last Modified: Tue, 28 May 2024 19:59:10 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ab6c510509c183336a9d38f2d07f973d0720ae39a99cda296f7bed5b5c262c`  
		Last Modified: Tue, 28 May 2024 19:59:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:67984dc41310f128ce3d5da1a522b83b98a51863c4525c31fe80405fc5bb7e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.0 MB (262984438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ed1cfa225bd5773a35fa816ce8bf69874a5b873c85a3fc2054c88ac04e6548`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 May 2024 06:06:31 GMT
ARG RELEASE
# Thu, 30 May 2024 06:06:31 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:06:31 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:06:33 GMT
ADD file:d001dd0dc3bb087b5d1110989f01b095d8dbe5e96c7df1f37ed15da7efad320a in / 
# Thu, 30 May 2024 06:06:34 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 06:40:53 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:40:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 05 Jun 2024 06:40:55 GMT
CMD ["jshell"]
# Mon, 27 May 2024 15:57:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6641c561838de8ad618aef3d8dc42a8a779db34736a55935b741015475180417`  
		Last Modified: Fri, 31 May 2024 11:22:47 GMT  
		Size: 29.0 MB (29043922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301c76a9e5b4fa4ef8eaaf782c8be26f27ac69c2da8927f554c198ad41ab49c7`  
		Last Modified: Wed, 05 Jun 2024 07:04:02 GMT  
		Size: 199.6 MB (199604854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0f1ae571f2773d7dcdf5cbdea540375b196197961dced5259c23e1e03f9af1b`  
		Last Modified: Wed, 05 Jun 2024 08:28:39 GMT  
		Size: 24.7 MB (24686770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc89d79ddf679e86e60b31bc47238da8baf41ceb6545881988eb9ac8693d988a`  
		Last Modified: Wed, 05 Jun 2024 08:28:37 GMT  
		Size: 9.6 MB (9647526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f354ce50d6700ddce5732409ab0685758bdbd6bf6a1a8dac065fa03aa13a6ae`  
		Last Modified: Wed, 05 Jun 2024 08:28:36 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2909b3268f062a17fb9028d82a943eb650a9d93e4167e26ddb9bbbaee2a7d49f`  
		Last Modified: Wed, 05 Jun 2024 08:28:36 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e773e60781d49430c4394d8bc1531b2543793fef1d467b2f3f22102458f8c3`  
		Last Modified: Wed, 05 Jun 2024 08:28:36 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-11` - linux; ppc64le

```console
$ docker pull maven@sha256:bf9c5ee3ae830e9b6a46d7cb13fb0290f267eaf11b012f554076e0df12df96bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.0 MB (261006009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b93287195893b1195cacee9239e5ac6340fa7432b6f0598774fb2cf9b3b4632`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 May 2024 06:03:19 GMT
ARG RELEASE
# Thu, 30 May 2024 06:03:19 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 30 May 2024 06:03:19 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 30 May 2024 06:03:22 GMT
ADD file:3d2d3a18d4f4a1567fc0564572f74e0601522492c4d8ca8614999dda64995e61 in / 
# Thu, 30 May 2024 06:03:22 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 05:08:48 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 05 Jun 2024 05:08:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 05 Jun 2024 05:08:51 GMT
CMD ["jshell"]
# Mon, 27 May 2024 15:57:48 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:bfc0d112768e1e28c0c23d62efaae836e46b237aa988781b18fb80319506dab6`  
		Last Modified: Wed, 05 Jun 2024 03:50:27 GMT  
		Size: 34.6 MB (34579185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc8afc2cf340bc0042d6f5dce81447bedaa667cf2071cbf2075724012d7ca51`  
		Last Modified: Wed, 05 Jun 2024 05:39:24 GMT  
		Size: 187.9 MB (187872501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a7d15a52ffdb196210418dd92a8bb95770445ca0c8df97b5d1bfbe8b0cc961`  
		Last Modified: Wed, 05 Jun 2024 08:14:58 GMT  
		Size: 28.9 MB (28905436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0486505a8713d7e77e5852a9b6152766e5b271101b7dc8b28a090db6bd9e56b8`  
		Last Modified: Wed, 05 Jun 2024 08:14:53 GMT  
		Size: 9.6 MB (9647517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c6fb5721da88fc0f20aa0f7e0083e2d8fe9a1e2fb44f852629f171274810d1b`  
		Last Modified: Wed, 05 Jun 2024 08:14:52 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5026a4cf2cf9540664874c6da6c00fd3566d7f37d2cf8fa7a6a0ff846bf5b836`  
		Last Modified: Wed, 05 Jun 2024 08:14:52 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2000fcc1817afdec574db07537896f549c8efa2e1681f5bc9c9b35053269a55`  
		Last Modified: Wed, 05 Jun 2024 08:14:53 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
