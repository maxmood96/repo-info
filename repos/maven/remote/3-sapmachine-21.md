## `maven:3-sapmachine-21`

```console
$ docker pull maven@sha256:5e378d43da4ab1f2189a33b8ead190e903cfe998c18a77ee82a4fca909c6f6da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-sapmachine-21` - linux; amd64

```console
$ docker pull maven@sha256:ec92487901e15ba11a048d12aee44e170f236eba2eb6d28028c47dcdbd92b4c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **281.8 MB (281808708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90e731dd3e73dfebf4d2903980fe40b10a2e559957f109acf9f24e804adfc20`
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
# Tue, 14 May 2024 22:42:17 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 14 May 2024 22:42:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Tue, 14 May 2024 22:42:18 GMT
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
	-	`sha256:68902b9f6cb3ac66bf0262fbab64b88e6ad76e72071de090c186a1209762e99d`  
		Last Modified: Tue, 14 May 2024 23:00:42 GMT  
		Size: 215.5 MB (215458889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80d3ac9d030b928724551feaf6621b4b1d4d2867967538892688d3543070ed7`  
		Last Modified: Tue, 28 May 2024 19:59:44 GMT  
		Size: 27.0 MB (26998423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4198ae37d456c0eb6d2d4516442b5d10b1681c0ccb7686400e01b30c9cf9c98`  
		Last Modified: Tue, 28 May 2024 19:59:41 GMT  
		Size: 9.6 MB (9647573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e9c812eba57f2705d961d640aa1b2cef74762b2e5b6aa8b6d9c783da1c8475`  
		Last Modified: Tue, 28 May 2024 19:59:40 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00cbf274c082769e5e8aeccd9d3f034e613e4c1bedb0c7434101259bc68630e`  
		Last Modified: Tue, 28 May 2024 19:59:40 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e19d741d5f04f1ea9bdd57e9b12b27ec28966d4cddedc374af5fdb9dbf2450`  
		Last Modified: Tue, 28 May 2024 19:59:40 GMT  
		Size: 158.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-21` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4ec6b5ecaac9cc07e74b58dc0e7b19c7bfdfd5bc632607040a6f9b1810da9756
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.9 MB (276942196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3336c490d7ad6cd4093e0c4f777486f760c00f7663929461c6b246227a723f47`
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
# Wed, 05 Jun 2024 06:29:28 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 05 Jun 2024 06:29:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 05 Jun 2024 06:29:31 GMT
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
	-	`sha256:d0108d1455602fb0c6eae54a9db0694acb7b942ac2877d1fa0e8bde916160223`  
		Last Modified: Wed, 05 Jun 2024 06:54:00 GMT  
		Size: 213.6 MB (213562774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81d3dd163b1755b8f0aeffd69d4e7db8bb123f00cae2f374c0969e1841564f01`  
		Last Modified: Wed, 05 Jun 2024 08:29:06 GMT  
		Size: 24.7 MB (24686603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092177cde02981278c7b78bd0a861b586790864245e085826e10e0614c1301da`  
		Last Modified: Wed, 05 Jun 2024 08:29:04 GMT  
		Size: 9.6 MB (9647524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8438d6e3014386a6d30874a93793ad0e4202f8d1fb3f903947d68d5a1f4b26fa`  
		Last Modified: Wed, 05 Jun 2024 08:29:03 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d227a0d76176febf3879e5621a91d95475af0532d0502049f77ac83d4abe3dc`  
		Last Modified: Wed, 05 Jun 2024 08:29:03 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a16580134f6a50b461014465b1d81f7eda4c7ae959cf9f139360743d67adbb`  
		Last Modified: Wed, 05 Jun 2024 08:29:03 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-21` - linux; ppc64le

```console
$ docker pull maven@sha256:6554c12c53c7e62fc15fe21f99987e14d7ed63286a8f82260aacfc76cdea074f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.1 MB (290051460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1f519c5ccba6ae4db02e3108e05f1de88bc908f8c3076dab3847f1da9303e45`
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
# Wed, 05 Jun 2024 04:47:44 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jdk=21.0.3     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 05 Jun 2024 04:47:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Wed, 05 Jun 2024 04:47:49 GMT
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
	-	`sha256:2b55359be8a44f6da38087e14363e6b1c07d8863c19ffa93ca2d155a0882e5c3`  
		Last Modified: Wed, 05 Jun 2024 05:26:46 GMT  
		Size: 216.9 MB (216918128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a756c840bbd42b54dc2832363ee1fce9e1f9c197be5994cbd1a059ee67cd0722`  
		Last Modified: Wed, 05 Jun 2024 08:15:28 GMT  
		Size: 28.9 MB (28905253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca89a14b5157f1388a6b8ebb1df8c890d0d15f160c46de94dc6be984b66024a`  
		Last Modified: Wed, 05 Jun 2024 08:15:23 GMT  
		Size: 9.6 MB (9647523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7daab5b48b25ef32b95dbffa448a5f3ae920ce936ca5c7bfecbc97081f435b`  
		Last Modified: Wed, 05 Jun 2024 08:15:23 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832279fc5170a316b2f258edbe37b8311859c832a241927afc622c3a3389455c`  
		Last Modified: Wed, 05 Jun 2024 08:15:22 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92faa97f8706ec89d2cba78897ed1832b287f6c1fcd6521a9122c78196c62c80`  
		Last Modified: Wed, 05 Jun 2024 08:15:23 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
