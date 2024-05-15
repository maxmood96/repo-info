## `maven:3-sapmachine-11`

```console
$ docker pull maven@sha256:af534919d9b9155a9ef63cee2c94132c83d8cf61c3497c43aa1fdd2277ddebe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `maven:3-sapmachine-11` - linux; amd64

```console
$ docker pull maven@sha256:33cad5b38427f51b34e3b3cf44c38dee9a6f2b071e02a4543b4c80b175e17f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.8 MB (264842499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b008725a52b4f82cb4d5160ddb0ad82697be67c04847f212daff7764dbfdb3c`
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
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
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
	-	`sha256:6e6f57b26d702d5a4be46427cb648abe93d5a3456705c13f920c346fe2f84cc3`  
		Last Modified: Tue, 14 May 2024 23:38:17 GMT  
		Size: 24.6 MB (24584723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b8c0abdce477eb35ae88d164a89f439a7cad5bd419c202732dfc475a51d59`  
		Last Modified: Tue, 14 May 2024 23:38:15 GMT  
		Size: 9.5 MB (9479973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a020ed183ff4b75b6a90ce7ecc0e40eb1435807277cfd328c932519395a556b7`  
		Last Modified: Tue, 14 May 2024 23:38:13 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c543eb0c33e83bbc7f97a1e98f320d751029552028ced05c9b2cae6478994365`  
		Last Modified: Tue, 14 May 2024 23:38:13 GMT  
		Size: 364.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d59bd4c8fbad2354eea2a1446b21d6fd183dcc606b2a0c6462ab318800c7010c`  
		Last Modified: Tue, 14 May 2024 23:38:14 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-11` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8331d11ff5d80f07d52dffe6b649537c544266de022cfa51860393daca87f55e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **262.8 MB (262800535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05ebfac7c3675c9f895a88256d4203809e99b7ff596169f8f7472c5def0b15e1`
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
# Tue, 14 May 2024 22:14:47 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Tue, 14 May 2024 22:14:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Tue, 14 May 2024 22:14:49 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ca6fd4ca81e04c073f1c2caac4de56748f56d5ff8b6eb9e1c781888109e50383`  
		Last Modified: Thu, 02 May 2024 02:33:15 GMT  
		Size: 29.0 MB (29038670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15bcfac16f333a9c4dab473aaef831c2268c19171f668592794b3bf048ad305`  
		Last Modified: Tue, 14 May 2024 22:31:17 GMT  
		Size: 199.6 MB (199603751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447fbe35ad124ff7cb03b3ff0987fe4a4935f1b6282302937fbd705206f06686`  
		Last Modified: Tue, 14 May 2024 23:02:04 GMT  
		Size: 24.7 MB (24676800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5979001d8b79cd06f874ff14fa3d8e9b08019eb763b5526e2e728328278ae81`  
		Last Modified: Tue, 14 May 2024 23:02:02 GMT  
		Size: 9.5 MB (9479941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c336ab346bce7a7718cc335ba84405e2d1b7d882876b656c64fa8c7f1048d0b`  
		Last Modified: Tue, 14 May 2024 23:02:01 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72bad72c3469cd3f282d380a2c5c65193eddaf856ce34cb4e1ac9eef45fa7e38`  
		Last Modified: Tue, 14 May 2024 23:02:01 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e79fd80739be5bd0da4a21acedac48bfbcb2f1f79184cb5d1b6b317e7e81518`  
		Last Modified: Tue, 14 May 2024 23:02:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-sapmachine-11` - linux; ppc64le

```console
$ docker pull maven@sha256:ad08cdecf8ab29ee2545036b5a946c3b4e540e6ac2f54b61a6c9375f07214d01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **256.8 MB (256757731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c436ab2f6834ec719f193abb594c48dded29fe568c1f18d46b043569872d9d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 27 Apr 2024 13:18:13 GMT
ARG RELEASE
# Sat, 27 Apr 2024 13:18:13 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 27 Apr 2024 13:18:13 GMT
LABEL org.opencontainers.image.version=22.04
# Sat, 27 Apr 2024 13:18:17 GMT
ADD file:3ab2760f4e449111dcca3f0816583c72999e1ce2ec20beac068dccfd6c9d8b81 in / 
# Sat, 27 Apr 2024 13:18:17 GMT
CMD ["/bin/bash"]
# Thu, 02 May 2024 02:58:46 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.23     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Thu, 02 May 2024 02:58:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 02 May 2024 02:58:51 GMT
CMD ["jshell"]
# Mon, 18 Dec 2023 19:11:15 GMT
RUN apt-get update   && apt-get install -y ca-certificates curl git --no-install-recommends   && rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ef1313ed517c6def5644ab70e25cc66f1c4cd52b1e81c07fb33bfb8850b39c25`  
		Last Modified: Thu, 02 May 2024 01:40:15 GMT  
		Size: 35.6 MB (35588524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45b25bd4cb4c9317c42eb9494ea60849687d0fcb8aaca8453bc977c140ead62`  
		Last Modified: Thu, 02 May 2024 03:22:52 GMT  
		Size: 187.4 MB (187356035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b29d0650bed1f60f22e0a17e942c822464a8140dc1987a02c7d86b50f8da212`  
		Last Modified: Thu, 02 May 2024 04:34:54 GMT  
		Size: 24.3 MB (24331869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c108007a5c6fac260e8dd92a5a0da0694d920fd42b18dabca266a416d6eada39`  
		Last Modified: Thu, 02 May 2024 04:34:49 GMT  
		Size: 9.5 MB (9479938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801e4b793ec3413a4c37c3023e62ebbfe606d2e70a8ef79b5e3672404a317b4b`  
		Last Modified: Thu, 02 May 2024 04:34:49 GMT  
		Size: 851.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eef150a7b3f7b610985afcdad9ef04a9a3bc71dcd8ffc83c55e2a4466c894e`  
		Last Modified: Thu, 02 May 2024 04:34:48 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e93604689e3b8ccd9e4ca756857253856e77618b58a86d8164629235009cca`  
		Last Modified: Thu, 02 May 2024 04:34:48 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
