## `sapmachine:jre-ubuntu-17.0.8`

```console
$ docker pull sapmachine@sha256:a9b9ad8d6a1b5afd4082536cc2c787aec8773d6100bcb36166731ae46e571ad4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:jre-ubuntu-17.0.8` - linux; amd64

```console
$ docker pull sapmachine@sha256:282739f8d22e20e8d51e8a36fbd5318889b3ef196fa5739afd7afc8fe1887ebe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.1 MB (84083831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2ff6b52841f1dcdacd45fe2bd9824afbdc0d60ed346ed72cc764f44d1c53fd`
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
# Wed, 19 Jul 2023 23:24:47 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.8     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 19 Jul 2023 23:24:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 19 Jul 2023 23:24:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd204046f640b75b083497ae95aacc78be37f14a99187b466881c5f2ee33762b`  
		Last Modified: Wed, 19 Jul 2023 23:30:35 GMT  
		Size: 53.7 MB (53652602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-ubuntu-17.0.8` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:b692a5a130046a5a50fdb9ea3e64dcfe29b8dd180352f0025203e5d4f69aa692
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.4 MB (81365675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1292d7a455a1a62b6b67aaf13404b5692ee3ba8febd0bf51a1d2330cb780a15e`
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
# Wed, 16 Aug 2023 14:54:00 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.8     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:54:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Aug 2023 14:54:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fc91a1e8006d5201417afae050ccdfbd224a94855cd261935d0223bb69dbad4`  
		Last Modified: Wed, 16 Aug 2023 14:59:32 GMT  
		Size: 53.0 MB (52973772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-ubuntu-17.0.8` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:0107e285ca8fe8f4c32e7d84dafd34f1da40408fbf05c8854d55877fb94cc14a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.8 MB (90840686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8bcee90e025f3ed169f24f60527c006f66cf8e920374884a457d46c1c00c4b0`
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
# Wed, 19 Jul 2023 22:47:34 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre=17.0.8     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 19 Jul 2023 22:47:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 19 Jul 2023 22:47:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be194c023bc4683ce262d1f8f0d994fb279233fee7283e2fa6ae77511a89b25f`  
		Last Modified: Wed, 19 Jul 2023 23:01:06 GMT  
		Size: 55.1 MB (55129217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
