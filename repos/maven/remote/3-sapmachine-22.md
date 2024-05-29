## `maven:3-sapmachine-22`

```console
$ docker pull maven@sha256:4f5aad3991144e5abe9f6345ee8615f0c039203d7860fa83840a489b4399bedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-sapmachine-22` - linux; amd64

```console
$ docker pull maven@sha256:720d31d5c7b50f3fe8b6d6f6da53d20719b836db940c857676b52a577e84e180
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.1 MB (280144114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2efcd5f8aded9eaa0324d8fe21aa443b4f70e930b3411de366efe7d36d3cbee1`
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
# Tue, 14 May 2024 22:35:52 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 14 May 2024 22:35:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Tue, 14 May 2024 22:35:53 GMT
CMD ["jshell"]
# Wed, 29 May 2024 20:51:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 29 May 2024 20:51:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 29 May 2024 20:51:55 GMT
ARG MAVEN_VERSION=3.9.7
# Wed, 29 May 2024 20:51:55 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 May 2024 20:51:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 May 2024 20:51:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:683717517814a7e5abc1086ac638706a33e20d12621de123d0d4041d703a8736`  
		Last Modified: Thu, 02 May 2024 00:53:54 GMT  
		Size: 29.7 MB (29702452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbba354d0d51a36bed14a2ebcff621e85ae1ed3f356fd927d1ccf487ce32bcd0`  
		Last Modified: Tue, 14 May 2024 22:55:55 GMT  
		Size: 213.8 MB (213794274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af12633e3b68b0d28f13f96dd8928bf751195b789acb888d607e2d49af0bbe3`  
		Last Modified: Wed, 29 May 2024 22:16:53 GMT  
		Size: 27.0 MB (26998444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165ad9a58ecfc29fa4210802eac0a0139153b6d0e7af5034d2ca623552946308`  
		Last Modified: Wed, 29 May 2024 22:16:49 GMT  
		Size: 9.6 MB (9647573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:566e97efce98ab3079013aa07c7f87a95ddf95a4c01d1c3f75847318869eaccd`  
		Last Modified: Wed, 29 May 2024 22:16:48 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79826539d705e690b77b24c0465c40719529ac9e4788e45220c0551896671546`  
		Last Modified: Wed, 29 May 2024 22:16:48 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcce6569af530b2d3af285e58649ebdf741d043f552dc4cd060ed8b1a41a0aaf`  
		Last Modified: Wed, 29 May 2024 22:16:48 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-22` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d9ea19b67ea4af7ad1bab227c3ba9c6320b72d3d57445e6b30f8e9c2bde2b091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.4 MB (277368835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75bb168d80dc5ff2dbde9323ad335ba654b9e8800b7f54f173980338e669c0e3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 29 Apr 2024 16:39:55 GMT
ARG RELEASE
# Mon, 29 Apr 2024 16:39:55 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 29 Apr 2024 16:39:55 GMT
LABEL org.opencontainers.image.version=24.04
# Mon, 29 Apr 2024 16:39:58 GMT
ADD file:d1bd5209fbd828a2a6f6ad537f0eb77154890b9445411715281122300f5bb21e in / 
# Mon, 29 Apr 2024 16:39:58 GMT
CMD ["/bin/bash"]
# Tue, 14 May 2024 22:03:14 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jdk=22.0.1     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 14 May 2024 22:03:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Tue, 14 May 2024 22:03:16 GMT
CMD ["jshell"]
# Wed, 29 May 2024 20:51:55 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 29 May 2024 20:51:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 29 May 2024 20:51:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 29 May 2024 20:51:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 29 May 2024 20:51:55 GMT
ARG MAVEN_VERSION=3.9.7
# Wed, 29 May 2024 20:51:55 GMT
ARG USER_HOME_DIR=/root
# Wed, 29 May 2024 20:51:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 29 May 2024 20:51:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 29 May 2024 20:51:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c51bf4692bafd38103484421472ddf4ce0cba9dacdf493cdb980ec07f089786`  
		Last Modified: Tue, 14 May 2024 22:20:12 GMT  
		Size: 211.8 MB (211783625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af275bab9aab576cfb6bfd4f889bada5781f902a486b76da15cd766d8767ac4a`  
		Last Modified: Wed, 29 May 2024 21:54:54 GMT  
		Size: 26.9 MB (26897594 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ccd2f995ab1aa47389961184cb40866f25c1b3bb67a1170500c43f2a9bc1485`  
		Last Modified: Wed, 29 May 2024 21:54:52 GMT  
		Size: 9.6 MB (9647572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c697bde30857f4300221dc5c7c1dd123f1bada1eed0b001a007ef74624d7f38`  
		Last Modified: Wed, 29 May 2024 21:54:51 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b118321920bbdda08bbde5f51c5ed0df7208a3b93009121a5db63ad1116daffb`  
		Last Modified: Wed, 29 May 2024 21:54:51 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd749c01cbeedb1f56b2b26636a08135c924b086321c86259ce681d7953aba4`  
		Last Modified: Wed, 29 May 2024 21:54:51 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
