## `sapmachine:jdk-ubuntu-11.0.20`

```console
$ docker pull sapmachine@sha256:409d8b26c3dd00d080cfd705b823c48c041fafb9d50628c28a040a48938d8169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:jdk-ubuntu-11.0.20` - linux; amd64

```console
$ docker pull sapmachine@sha256:138c410bc6c2baa48b7a477259ec546c4b5f6da9b75c6863fdabbd881d73ad1c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.7 MB (230685846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed8e5107d5c32bda733a6ace85fa3f0446ba152b643d0e28c2b20e1845c4b25`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:37:40 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:37:40 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:37:40 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:37:42 GMT
ADD file:140fb5108b4a2861b5718ad03b4a5174bba03589ea8d4c053e6a0b282f439ff3 in / 
# Wed, 28 Jun 2023 08:37:42 GMT
CMD ["/bin/bash"]
# Wed, 19 Jul 2023 23:23:58 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.20     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 19 Jul 2023 23:23:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 19 Jul 2023 23:23:59 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336c934e6a008b6c6d27cb8c2a3d06e608bb1cd7f7430b2a81a21c9dde957600`  
		Last Modified: Wed, 19 Jul 2023 23:29:56 GMT  
		Size: 200.3 MB (200254617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jdk-ubuntu-11.0.20` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:db3f4a9f91c8d058ae00f448fdac8ad77f387c2b672e83f2089c666bd4750d3f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.0 MB (227026547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff21b4feb7f8d16d6b2670c3fad755d9b752a0445f4c4bdab544ec6d60166bae`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 04 Aug 2023 04:51:14 GMT
ARG RELEASE
# Fri, 04 Aug 2023 04:51:14 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 04 Aug 2023 04:51:14 GMT
LABEL org.opencontainers.image.version=22.04
# Fri, 04 Aug 2023 04:51:18 GMT
ADD file:5cf7797cf86362218d2bd85debeff136ee897af7eef95a0b8baab9f9457c3e89 in / 
# Fri, 04 Aug 2023 04:51:18 GMT
CMD ["/bin/bash"]
# Wed, 16 Aug 2023 14:53:13 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.20     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:53:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Aug 2023 14:53:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f561fb47fbda97db84a08706e7a8a48996ef5b0c13bb47a1d98c3c5d1296f3a6`  
		Last Modified: Wed, 16 Aug 2023 14:58:58 GMT  
		Size: 198.6 MB (198634644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jdk-ubuntu-11.0.20` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:5062efb355d1cadf1ea122bb41fa6754bc253de31fa8b87300d211dc3c614556
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **222.5 MB (222539968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:114d0d50304033be5f6927c3cfc2c2a08c93434782f4dd3f39863175eff9aac0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 28 Jun 2023 08:45:53 GMT
ARG RELEASE
# Wed, 28 Jun 2023 08:45:53 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 28 Jun 2023 08:45:53 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 28 Jun 2023 08:45:54 GMT
LABEL org.opencontainers.image.version=22.04
# Wed, 28 Jun 2023 08:45:56 GMT
ADD file:8c2fc380378944326d602742fde0e30458cd3e82012847b0f7e09c7184bfd135 in / 
# Wed, 28 Jun 2023 08:45:57 GMT
CMD ["/bin/bash"]
# Wed, 19 Jul 2023 22:45:27 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.20     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 19 Jul 2023 22:45:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 19 Jul 2023 22:45:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8105ba0eaa4fe96e17193aceaa8c8de1394cb852339bd37b6ede522cf5c73759`  
		Last Modified: Wed, 19 Jul 2023 23:00:01 GMT  
		Size: 186.8 MB (186828499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
