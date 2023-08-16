## `sapmachine:jre-headless-ubuntu-17`

```console
$ docker pull sapmachine@sha256:d47e20b014445b9a08367d04a70e424bc0ca4289a07a55bccbf70a4f8c0373de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `sapmachine:jre-headless-ubuntu-17` - linux; amd64

```console
$ docker pull sapmachine@sha256:429fe1d0de24fed563ec02720626121018ef77925d1e354f7e322bdc5c2710f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.9 MB (82867607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a761e7405fce1beed7c64caf9bd497cb3ab2ec4b8abdbee2ff7491118eac978`
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
# Wed, 19 Jul 2023 23:24:25 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.8     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 19 Jul 2023 23:24:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 19 Jul 2023 23:24:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9d19ee268e0d7bcf6716e6658ee1b0384a71d6f2f9aa1ae2085610cf7c7b316f`  
		Last Modified: Wed, 28 Jun 2023 11:50:41 GMT  
		Size: 30.4 MB (30431229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:621e6b9d7d3794e71a4922357869ad929a288a2efb1a459d486ef2ddbded28c9`  
		Last Modified: Wed, 19 Jul 2023 23:30:17 GMT  
		Size: 52.4 MB (52436378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-headless-ubuntu-17` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ae2583c0e52e62f093fe9c4d0d59c3b732fe1ea8db309e98ed6b009df402022c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.2 MB (80161122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3abde5a6a1d1635d208c7a52cf28d71d8169ce915e08471427c1285f6d015d7`
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
# Wed, 16 Aug 2023 14:53:40 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.8     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 16 Aug 2023 14:53:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 16 Aug 2023 14:53:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9ea365e1e52efb9567c56f02f2200f0e95ddffd579225cc5b20a6333119d2811`  
		Last Modified: Fri, 04 Aug 2023 13:35:19 GMT  
		Size: 28.4 MB (28391903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1902518a02393c4f183583461a5d703ebc2a5ea94299d6e3c34bce55dbc552`  
		Last Modified: Wed, 16 Aug 2023 14:59:17 GMT  
		Size: 51.8 MB (51769219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `sapmachine:jre-headless-ubuntu-17` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:3c80cf91208714fed39290391f9344aae97408df26d64bb289dfd180fef1fed4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.5 MB (89451976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:240576bb433aa73ef95d7d7acf4f5d7fa5b3394cbbec527e52ecf94694ab933e`
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
# Wed, 19 Jul 2023 22:46:32 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jre-headless=17.0.8     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/*
# Wed, 19 Jul 2023 22:46:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Wed, 19 Jul 2023 22:46:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7faa46ce6b6f5c34485980029504c3995e38149d0bca67d8b976c5dbb3673644`  
		Last Modified: Tue, 04 Jul 2023 04:42:31 GMT  
		Size: 35.7 MB (35711469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f27898c1b53836f4b0590f8bb7de2b8200ec9a02ccb4481523a7a4f9b1d1dc`  
		Last Modified: Wed, 19 Jul 2023 23:00:38 GMT  
		Size: 53.7 MB (53740507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
