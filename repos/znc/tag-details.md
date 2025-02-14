<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `znc`

-	[`znc:1.9`](#znc19)
-	[`znc:1.9-slim`](#znc19-slim)
-	[`znc:1.9.1`](#znc191)
-	[`znc:1.9.1-slim`](#znc191-slim)
-	[`znc:latest`](#znclatest)
-	[`znc:slim`](#zncslim)

## `znc:1.9`

```console
$ docker pull znc@sha256:e37d13c047f4207db35efaeece7ed59cef596ad1eb2580d2c84342ea1e54735c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.9` - linux; amd64

```console
$ docker pull znc@sha256:5a944262203a86b7718c588a2a86fec4da580b2c08c670839c57542113982368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157971536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edd9a65cd97ccf9e41d22728d0e056b78e04d9941b5949f4413a52cb52c3c03`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae76b2fcf81b8680aa431031e515303cfc99349b5f33a998915004641237c88`  
		Last Modified: Wed, 15 Jan 2025 00:04:43 GMT  
		Size: 46.7 MB (46652892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17983fa9cf4a573489f11488806100e3141cd5c12e9a6c63aedd3f9858fe8f9`  
		Last Modified: Tue, 14 Jan 2025 21:14:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29adc681b398338655b197d340f1d612e71fb1a6062b02041e839e930959f82b`  
		Last Modified: Wed, 15 Jan 2025 01:03:29 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb674f858a42281704871a954043e11ca262add8fa75335de5b47e6ba778fb61`  
		Last Modified: Wed, 15 Jan 2025 01:03:32 GMT  
		Size: 107.9 MB (107897147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c3018ca3d6c8d792dc6e34ec27af0fbda22d24f71c1c12ffb6e23981ad74f3`  
		Last Modified: Tue, 14 Jan 2025 23:13:32 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9` - unknown; unknown

```console
$ docker pull znc@sha256:ea06121947ec7bdf3b3910b9be2cf0fd10b18df2209cf794091cb9513756be72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6755463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a88fa3c10f75a964e5c1925ef21616091a155d0c443822e6dd668d378b885`

```dockerfile
```

-	Layers:
	-	`sha256:80e4f167463a53c5769336a943949eee43b6b78371ea17acf37e99b8d3e16ca4`  
		Last Modified: Fri, 07 Feb 2025 23:08:44 GMT  
		Size: 6.7 MB (6745865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca1e8e3589f6978024b6f22b342cbec4c7637041366ff0eeb9e4947ff28bbd85`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9` - linux; arm variant v6

```console
$ docker pull znc@sha256:396f3b8f3f4fa40d0eb21c58d0fc63d80decf44c72415cdeeed55da12d0cbc2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140375110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4d8b589680311f09e8a5394f08496605e8558416f402afb566ebb86ee30532`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 15 Jan 2025 00:02:14 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01dd87b3e6e2a51188f6a9afaa21a7c146b0796da99f121182f21a05e122e3c`  
		Last Modified: Wed, 15 Jan 2025 00:03:28 GMT  
		Size: 45.3 MB (45306574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c6412cbb9a286f04871877b0c6a6cc4698b94dd5915f8049ddf8ea554882a`  
		Last Modified: Tue, 07 Jan 2025 23:04:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d05039a5cdcbaa65d4cedb361439d0e8668daf04ff705cc107ba34ce05866d`  
		Last Modified: Tue, 07 Jan 2025 22:35:36 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e67f92f6800541d7bb91cd51118121e625d4eaf47105599343f382fa5cdcb`  
		Last Modified: Fri, 07 Feb 2025 23:08:49 GMT  
		Size: 91.9 MB (91890282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5f832a98b88b4e603c297c8ef175a6fc560c9d91c65d85121416d49a96ffa`  
		Last Modified: Fri, 07 Feb 2025 23:08:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9` - unknown; unknown

```console
$ docker pull znc@sha256:9d8799414ca2a4bb70e1786d29d24067cf05e68f2eafb0ecf6e34d96576d594d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01662c36f4d6f855d662f31a10c50daebaa2b9d341d4b164f7b60234036a71e8`

```dockerfile
```

-	Layers:
	-	`sha256:1c9bccca50521545a4b5546e4951b9ee321f6ec02e6b884fb172431e01e55b3b`  
		Last Modified: Thu, 09 Jan 2025 09:15:32 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:7c4c62330c710ea74cf6840020ce38b90aec21ebbd0a7850effa044f9025fca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152472568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391ffff2510854a20e8d396cc1e9d3bcbc614f844b9d07995a521d8e91699eea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3af5b4a9e68048bc28c635c6cdd2bf674e036e30150d45c98f57dadf501bc38`  
		Last Modified: Wed, 15 Jan 2025 15:49:14 GMT  
		Size: 46.7 MB (46722139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7c168bfe8c8a324b20ba48b48284526d090888b95d50676ce20f9c819ae9b`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be7b705b54726046dc93a27171026cd0aa29e2a934cb73362afbc0b5d4c4a6`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869883eb3420f56e41aac41eb0ba498ef58903037bd0f6007c16b8e3b7b0ad94`  
		Last Modified: Wed, 15 Jan 2025 15:49:19 GMT  
		Size: 102.4 MB (102388644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b39fe3bc830c39330448b99d3258f3c4f0c9519d3a4403c3777e4d1901527`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9` - unknown; unknown

```console
$ docker pull znc@sha256:a91a85ab1e0dd01e3ebc913815b7fc9564f8681b1b4c1484d206221a48901711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d478003427c6eb9b3364ef03e1b5e72c752b9ba3200e1ee9b14ee72850b807`

```dockerfile
```

-	Layers:
	-	`sha256:ff67f273a7b9dd760a011f78bed9c0e862e5a770bc0ede18768c22a94556fbd3`  
		Last Modified: Fri, 07 Feb 2025 23:08:59 GMT  
		Size: 6.8 MB (6781681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9ad91de32543a1d3c14a30e7a94f3b213d630cbbabde6c8143e8f8d73b3f0b`  
		Last Modified: Thu, 09 Jan 2025 06:46:27 GMT  
		Size: 9.7 KB (9690 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.9-slim`

```console
$ docker pull znc@sha256:a9035bb6d22bd8accd05fe28eca7fc3bfc322f95c34c23afd16a12c4a3718b1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.9-slim` - linux; amd64

```console
$ docker pull znc@sha256:fe12636aec83e177211c772b5988deaaca47278d6c0221be03be903667f5d409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50073971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333e8eb2f84f788d77fd37a1d0a2a9abb1e1fc4ace4a6694c2abb94f6f5e65f5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dd897bb9f390fdace3409f78a16204ce07e190b92547b429657efc6a98a88b`  
		Last Modified: Fri, 14 Feb 2025 20:34:04 GMT  
		Size: 46.7 MB (46652179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa846dea2614b7e7c64e4a4564f8e47098ef71fd9f8c4f5b63b98827269b71c7`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770c8f0aeb9f47e12240bc5ef97eb997483724e19a6c86a4afee4d1413be9693`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9-slim` - unknown; unknown

```console
$ docker pull znc@sha256:bc3636ee5f653a57b7c288c068932440a5e185a591b15bb1aa9881d2e1be2f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2634fe31c13f8b21e87b312a1407dd0db56109c083e450a9e3fcaef90e7ec`

```dockerfile
```

-	Layers:
	-	`sha256:b491aa210bed841161b8f46f1587305a3683d1cdb325c0d00056c7d1942a4ea9`  
		Last Modified: Fri, 14 Feb 2025 22:35:20 GMT  
		Size: 2.1 MB (2136695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60ad5154ae3cb1f26174574f0bb46d531ab35f6aa37bb0a7b658cb6f5aa7e98`  
		Last Modified: Fri, 14 Feb 2025 22:35:20 GMT  
		Size: 14.0 KB (14026 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:cb6392c0d504488302e42162f224054ac97e41f13f17f0b5513f1e333c578094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48486387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba102551766ebe81cd35f44e3eaee9f4969ff928ae5abeabc7b43cb39ea78ec5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 19:25:37 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376a7544d345f9c09b5eaa181509524a03932c1287abe74ad6e7f56f1887201f`  
		Last Modified: Fri, 14 Feb 2025 22:35:34 GMT  
		Size: 45.3 MB (45307932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc95fd6963eaa2fb3ff3536c296e611ca0c47b6bea5ce2b773e948e7b6265d5c`  
		Last Modified: Fri, 14 Feb 2025 22:35:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030126f47f27f3ce38e0888c66d72341fc50612628c65d7cc1113e9f24719a25`  
		Last Modified: Fri, 14 Feb 2025 22:35:30 GMT  
		Size: 748.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9-slim` - unknown; unknown

```console
$ docker pull znc@sha256:b213cfde217f870e9053d76609c339daf28bb74540095e230f46ae28138bcdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5904279525564e80da0f08c89ca11c526772a86d23fb9b02a04379c1070689e7`

```dockerfile
```

-	Layers:
	-	`sha256:e65a751e4ebbe01c489945b75af022bbf730739f9461d53e7fe1582897613883`  
		Last Modified: Fri, 14 Feb 2025 22:35:22 GMT  
		Size: 13.9 KB (13879 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:c47cd4e858cc011a15c1552adf5b597b48d5a4e5397b316984f49e0276915b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50083594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8407a3f298f2eb072038604241ba675278f7dfee7dc8711d94aa6211024f4fe5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3af5b4a9e68048bc28c635c6cdd2bf674e036e30150d45c98f57dadf501bc38`  
		Last Modified: Wed, 15 Jan 2025 15:49:14 GMT  
		Size: 46.7 MB (46722139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7c168bfe8c8a324b20ba48b48284526d090888b95d50676ce20f9c819ae9b`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be7b705b54726046dc93a27171026cd0aa29e2a934cb73362afbc0b5d4c4a6`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9-slim` - unknown; unknown

```console
$ docker pull znc@sha256:93d8da96e4cd0f5ee0c2c7a615697f97dcd00f5d85a818e3ce3613d80f78d43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c1b6597675f703946ec5902a9e8bd2709e0d595c153c67d571fdb0f0f5db90`

```dockerfile
```

-	Layers:
	-	`sha256:411b819abd849c70298d82bc2d4050b5628a8f08e8e1a11f73bd3c87be13ff82`  
		Last Modified: Fri, 14 Feb 2025 22:35:23 GMT  
		Size: 2.1 MB (2136824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a937b18244718d4a5bbee3f92927c370d7bc7d9f2da5f45f557cf70c123a755c`  
		Last Modified: Fri, 14 Feb 2025 22:35:23 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.9.1`

```console
$ docker pull znc@sha256:e37d13c047f4207db35efaeece7ed59cef596ad1eb2580d2c84342ea1e54735c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.9.1` - linux; amd64

```console
$ docker pull znc@sha256:5a944262203a86b7718c588a2a86fec4da580b2c08c670839c57542113982368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157971536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edd9a65cd97ccf9e41d22728d0e056b78e04d9941b5949f4413a52cb52c3c03`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae76b2fcf81b8680aa431031e515303cfc99349b5f33a998915004641237c88`  
		Last Modified: Wed, 15 Jan 2025 00:04:43 GMT  
		Size: 46.7 MB (46652892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17983fa9cf4a573489f11488806100e3141cd5c12e9a6c63aedd3f9858fe8f9`  
		Last Modified: Tue, 14 Jan 2025 21:14:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29adc681b398338655b197d340f1d612e71fb1a6062b02041e839e930959f82b`  
		Last Modified: Wed, 15 Jan 2025 01:03:29 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb674f858a42281704871a954043e11ca262add8fa75335de5b47e6ba778fb61`  
		Last Modified: Wed, 15 Jan 2025 01:03:32 GMT  
		Size: 107.9 MB (107897147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c3018ca3d6c8d792dc6e34ec27af0fbda22d24f71c1c12ffb6e23981ad74f3`  
		Last Modified: Tue, 14 Jan 2025 23:13:32 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1` - unknown; unknown

```console
$ docker pull znc@sha256:ea06121947ec7bdf3b3910b9be2cf0fd10b18df2209cf794091cb9513756be72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6755463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a88fa3c10f75a964e5c1925ef21616091a155d0c443822e6dd668d378b885`

```dockerfile
```

-	Layers:
	-	`sha256:80e4f167463a53c5769336a943949eee43b6b78371ea17acf37e99b8d3e16ca4`  
		Last Modified: Fri, 07 Feb 2025 23:08:44 GMT  
		Size: 6.7 MB (6745865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca1e8e3589f6978024b6f22b342cbec4c7637041366ff0eeb9e4947ff28bbd85`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1` - linux; arm variant v6

```console
$ docker pull znc@sha256:396f3b8f3f4fa40d0eb21c58d0fc63d80decf44c72415cdeeed55da12d0cbc2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140375110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4d8b589680311f09e8a5394f08496605e8558416f402afb566ebb86ee30532`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 15 Jan 2025 00:02:14 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01dd87b3e6e2a51188f6a9afaa21a7c146b0796da99f121182f21a05e122e3c`  
		Last Modified: Wed, 15 Jan 2025 00:03:28 GMT  
		Size: 45.3 MB (45306574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c6412cbb9a286f04871877b0c6a6cc4698b94dd5915f8049ddf8ea554882a`  
		Last Modified: Tue, 07 Jan 2025 23:04:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d05039a5cdcbaa65d4cedb361439d0e8668daf04ff705cc107ba34ce05866d`  
		Last Modified: Tue, 07 Jan 2025 22:35:36 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e67f92f6800541d7bb91cd51118121e625d4eaf47105599343f382fa5cdcb`  
		Last Modified: Fri, 07 Feb 2025 23:08:49 GMT  
		Size: 91.9 MB (91890282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5f832a98b88b4e603c297c8ef175a6fc560c9d91c65d85121416d49a96ffa`  
		Last Modified: Fri, 07 Feb 2025 23:08:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1` - unknown; unknown

```console
$ docker pull znc@sha256:9d8799414ca2a4bb70e1786d29d24067cf05e68f2eafb0ecf6e34d96576d594d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01662c36f4d6f855d662f31a10c50daebaa2b9d341d4b164f7b60234036a71e8`

```dockerfile
```

-	Layers:
	-	`sha256:1c9bccca50521545a4b5546e4951b9ee321f6ec02e6b884fb172431e01e55b3b`  
		Last Modified: Thu, 09 Jan 2025 09:15:32 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:7c4c62330c710ea74cf6840020ce38b90aec21ebbd0a7850effa044f9025fca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152472568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391ffff2510854a20e8d396cc1e9d3bcbc614f844b9d07995a521d8e91699eea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3af5b4a9e68048bc28c635c6cdd2bf674e036e30150d45c98f57dadf501bc38`  
		Last Modified: Wed, 15 Jan 2025 15:49:14 GMT  
		Size: 46.7 MB (46722139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7c168bfe8c8a324b20ba48b48284526d090888b95d50676ce20f9c819ae9b`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be7b705b54726046dc93a27171026cd0aa29e2a934cb73362afbc0b5d4c4a6`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869883eb3420f56e41aac41eb0ba498ef58903037bd0f6007c16b8e3b7b0ad94`  
		Last Modified: Wed, 15 Jan 2025 15:49:19 GMT  
		Size: 102.4 MB (102388644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b39fe3bc830c39330448b99d3258f3c4f0c9519d3a4403c3777e4d1901527`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1` - unknown; unknown

```console
$ docker pull znc@sha256:a91a85ab1e0dd01e3ebc913815b7fc9564f8681b1b4c1484d206221a48901711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d478003427c6eb9b3364ef03e1b5e72c752b9ba3200e1ee9b14ee72850b807`

```dockerfile
```

-	Layers:
	-	`sha256:ff67f273a7b9dd760a011f78bed9c0e862e5a770bc0ede18768c22a94556fbd3`  
		Last Modified: Fri, 07 Feb 2025 23:08:59 GMT  
		Size: 6.8 MB (6781681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9ad91de32543a1d3c14a30e7a94f3b213d630cbbabde6c8143e8f8d73b3f0b`  
		Last Modified: Thu, 09 Jan 2025 06:46:27 GMT  
		Size: 9.7 KB (9690 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.9.1-slim`

```console
$ docker pull znc@sha256:a9035bb6d22bd8accd05fe28eca7fc3bfc322f95c34c23afd16a12c4a3718b1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.9.1-slim` - linux; amd64

```console
$ docker pull znc@sha256:fe12636aec83e177211c772b5988deaaca47278d6c0221be03be903667f5d409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50073971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333e8eb2f84f788d77fd37a1d0a2a9abb1e1fc4ace4a6694c2abb94f6f5e65f5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dd897bb9f390fdace3409f78a16204ce07e190b92547b429657efc6a98a88b`  
		Last Modified: Fri, 14 Feb 2025 20:34:04 GMT  
		Size: 46.7 MB (46652179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa846dea2614b7e7c64e4a4564f8e47098ef71fd9f8c4f5b63b98827269b71c7`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770c8f0aeb9f47e12240bc5ef97eb997483724e19a6c86a4afee4d1413be9693`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:bc3636ee5f653a57b7c288c068932440a5e185a591b15bb1aa9881d2e1be2f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2634fe31c13f8b21e87b312a1407dd0db56109c083e450a9e3fcaef90e7ec`

```dockerfile
```

-	Layers:
	-	`sha256:b491aa210bed841161b8f46f1587305a3683d1cdb325c0d00056c7d1942a4ea9`  
		Last Modified: Fri, 14 Feb 2025 22:35:20 GMT  
		Size: 2.1 MB (2136695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60ad5154ae3cb1f26174574f0bb46d531ab35f6aa37bb0a7b658cb6f5aa7e98`  
		Last Modified: Fri, 14 Feb 2025 22:35:20 GMT  
		Size: 14.0 KB (14026 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:cb6392c0d504488302e42162f224054ac97e41f13f17f0b5513f1e333c578094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48486387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba102551766ebe81cd35f44e3eaee9f4969ff928ae5abeabc7b43cb39ea78ec5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 19:25:37 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376a7544d345f9c09b5eaa181509524a03932c1287abe74ad6e7f56f1887201f`  
		Last Modified: Fri, 14 Feb 2025 22:35:34 GMT  
		Size: 45.3 MB (45307932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc95fd6963eaa2fb3ff3536c296e611ca0c47b6bea5ce2b773e948e7b6265d5c`  
		Last Modified: Fri, 14 Feb 2025 22:35:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030126f47f27f3ce38e0888c66d72341fc50612628c65d7cc1113e9f24719a25`  
		Last Modified: Fri, 14 Feb 2025 22:35:30 GMT  
		Size: 748.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:b213cfde217f870e9053d76609c339daf28bb74540095e230f46ae28138bcdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5904279525564e80da0f08c89ca11c526772a86d23fb9b02a04379c1070689e7`

```dockerfile
```

-	Layers:
	-	`sha256:e65a751e4ebbe01c489945b75af022bbf730739f9461d53e7fe1582897613883`  
		Last Modified: Fri, 14 Feb 2025 22:35:22 GMT  
		Size: 13.9 KB (13879 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:c47cd4e858cc011a15c1552adf5b597b48d5a4e5397b316984f49e0276915b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50083594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8407a3f298f2eb072038604241ba675278f7dfee7dc8711d94aa6211024f4fe5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3af5b4a9e68048bc28c635c6cdd2bf674e036e30150d45c98f57dadf501bc38`  
		Last Modified: Wed, 15 Jan 2025 15:49:14 GMT  
		Size: 46.7 MB (46722139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7c168bfe8c8a324b20ba48b48284526d090888b95d50676ce20f9c819ae9b`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be7b705b54726046dc93a27171026cd0aa29e2a934cb73362afbc0b5d4c4a6`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:93d8da96e4cd0f5ee0c2c7a615697f97dcd00f5d85a818e3ce3613d80f78d43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c1b6597675f703946ec5902a9e8bd2709e0d595c153c67d571fdb0f0f5db90`

```dockerfile
```

-	Layers:
	-	`sha256:411b819abd849c70298d82bc2d4050b5628a8f08e8e1a11f73bd3c87be13ff82`  
		Last Modified: Fri, 14 Feb 2025 22:35:23 GMT  
		Size: 2.1 MB (2136824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a937b18244718d4a5bbee3f92927c370d7bc7d9f2da5f45f557cf70c123a755c`  
		Last Modified: Fri, 14 Feb 2025 22:35:23 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:latest`

```console
$ docker pull znc@sha256:e37d13c047f4207db35efaeece7ed59cef596ad1eb2580d2c84342ea1e54735c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:5a944262203a86b7718c588a2a86fec4da580b2c08c670839c57542113982368
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157971536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2edd9a65cd97ccf9e41d22728d0e056b78e04d9941b5949f4413a52cb52c3c03`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae76b2fcf81b8680aa431031e515303cfc99349b5f33a998915004641237c88`  
		Last Modified: Wed, 15 Jan 2025 00:04:43 GMT  
		Size: 46.7 MB (46652892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17983fa9cf4a573489f11488806100e3141cd5c12e9a6c63aedd3f9858fe8f9`  
		Last Modified: Tue, 14 Jan 2025 21:14:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29adc681b398338655b197d340f1d612e71fb1a6062b02041e839e930959f82b`  
		Last Modified: Wed, 15 Jan 2025 01:03:29 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb674f858a42281704871a954043e11ca262add8fa75335de5b47e6ba778fb61`  
		Last Modified: Wed, 15 Jan 2025 01:03:32 GMT  
		Size: 107.9 MB (107897147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c3018ca3d6c8d792dc6e34ec27af0fbda22d24f71c1c12ffb6e23981ad74f3`  
		Last Modified: Tue, 14 Jan 2025 23:13:32 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:ea06121947ec7bdf3b3910b9be2cf0fd10b18df2209cf794091cb9513756be72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6755463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:296a88fa3c10f75a964e5c1925ef21616091a155d0c443822e6dd668d378b885`

```dockerfile
```

-	Layers:
	-	`sha256:80e4f167463a53c5769336a943949eee43b6b78371ea17acf37e99b8d3e16ca4`  
		Last Modified: Fri, 07 Feb 2025 23:08:44 GMT  
		Size: 6.7 MB (6745865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca1e8e3589f6978024b6f22b342cbec4c7637041366ff0eeb9e4947ff28bbd85`  
		Last Modified: Wed, 08 Jan 2025 18:23:08 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:396f3b8f3f4fa40d0eb21c58d0fc63d80decf44c72415cdeeed55da12d0cbc2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140375110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4d8b589680311f09e8a5394f08496605e8558416f402afb566ebb86ee30532`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-armhf.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:bfff14c232517ab149a6524fba444f7b5a336feab49d08abd27455f12ceb2efc`  
		Last Modified: Wed, 15 Jan 2025 00:02:14 GMT  
		Size: 3.2 MB (3176999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d01dd87b3e6e2a51188f6a9afaa21a7c146b0796da99f121182f21a05e122e3c`  
		Last Modified: Wed, 15 Jan 2025 00:03:28 GMT  
		Size: 45.3 MB (45306574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c6412cbb9a286f04871877b0c6a6cc4698b94dd5915f8049ddf8ea554882a`  
		Last Modified: Tue, 07 Jan 2025 23:04:05 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d05039a5cdcbaa65d4cedb361439d0e8668daf04ff705cc107ba34ce05866d`  
		Last Modified: Tue, 07 Jan 2025 22:35:36 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254e67f92f6800541d7bb91cd51118121e625d4eaf47105599343f382fa5cdcb`  
		Last Modified: Fri, 07 Feb 2025 23:08:49 GMT  
		Size: 91.9 MB (91890282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c5f832a98b88b4e603c297c8ef175a6fc560c9d91c65d85121416d49a96ffa`  
		Last Modified: Fri, 07 Feb 2025 23:08:55 GMT  
		Size: 334.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:9d8799414ca2a4bb70e1786d29d24067cf05e68f2eafb0ecf6e34d96576d594d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01662c36f4d6f855d662f31a10c50daebaa2b9d341d4b164f7b60234036a71e8`

```dockerfile
```

-	Layers:
	-	`sha256:1c9bccca50521545a4b5546e4951b9ee321f6ec02e6b884fb172431e01e55b3b`  
		Last Modified: Thu, 09 Jan 2025 09:15:32 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:7c4c62330c710ea74cf6840020ce38b90aec21ebbd0a7850effa044f9025fca9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152472568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:391ffff2510854a20e8d396cc1e9d3bcbc614f844b9d07995a521d8e91699eea`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3af5b4a9e68048bc28c635c6cdd2bf674e036e30150d45c98f57dadf501bc38`  
		Last Modified: Wed, 15 Jan 2025 15:49:14 GMT  
		Size: 46.7 MB (46722139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7c168bfe8c8a324b20ba48b48284526d090888b95d50676ce20f9c819ae9b`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be7b705b54726046dc93a27171026cd0aa29e2a934cb73362afbc0b5d4c4a6`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869883eb3420f56e41aac41eb0ba498ef58903037bd0f6007c16b8e3b7b0ad94`  
		Last Modified: Wed, 15 Jan 2025 15:49:19 GMT  
		Size: 102.4 MB (102388644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6b39fe3bc830c39330448b99d3258f3c4f0c9519d3a4403c3777e4d1901527`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:a91a85ab1e0dd01e3ebc913815b7fc9564f8681b1b4c1484d206221a48901711
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6791371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88d478003427c6eb9b3364ef03e1b5e72c752b9ba3200e1ee9b14ee72850b807`

```dockerfile
```

-	Layers:
	-	`sha256:ff67f273a7b9dd760a011f78bed9c0e862e5a770bc0ede18768c22a94556fbd3`  
		Last Modified: Fri, 07 Feb 2025 23:08:59 GMT  
		Size: 6.8 MB (6781681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c9ad91de32543a1d3c14a30e7a94f3b213d630cbbabde6c8143e8f8d73b3f0b`  
		Last Modified: Thu, 09 Jan 2025 06:46:27 GMT  
		Size: 9.7 KB (9690 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:slim`

```console
$ docker pull znc@sha256:a9035bb6d22bd8accd05fe28eca7fc3bfc322f95c34c23afd16a12c4a3718b1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:fe12636aec83e177211c772b5988deaaca47278d6c0221be03be903667f5d409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50073971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:333e8eb2f84f788d77fd37a1d0a2a9abb1e1fc4ace4a6694c2abb94f6f5e65f5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45dd897bb9f390fdace3409f78a16204ce07e190b92547b429657efc6a98a88b`  
		Last Modified: Fri, 14 Feb 2025 20:34:04 GMT  
		Size: 46.7 MB (46652179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa846dea2614b7e7c64e4a4564f8e47098ef71fd9f8c4f5b63b98827269b71c7`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:770c8f0aeb9f47e12240bc5ef97eb997483724e19a6c86a4afee4d1413be9693`  
		Last Modified: Fri, 14 Feb 2025 20:34:01 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:bc3636ee5f653a57b7c288c068932440a5e185a591b15bb1aa9881d2e1be2f80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00f2634fe31c13f8b21e87b312a1407dd0db56109c083e450a9e3fcaef90e7ec`

```dockerfile
```

-	Layers:
	-	`sha256:b491aa210bed841161b8f46f1587305a3683d1cdb325c0d00056c7d1942a4ea9`  
		Last Modified: Fri, 14 Feb 2025 22:35:20 GMT  
		Size: 2.1 MB (2136695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d60ad5154ae3cb1f26174574f0bb46d531ab35f6aa37bb0a7b658cb6f5aa7e98`  
		Last Modified: Fri, 14 Feb 2025 22:35:20 GMT  
		Size: 14.0 KB (14026 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:cb6392c0d504488302e42162f224054ac97e41f13f17f0b5513f1e333c578094
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48486387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba102551766ebe81cd35f44e3eaee9f4969ff928ae5abeabc7b43cb39ea78ec5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.7-armhf.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:f5c2e5a96485e4eaf16caa456bdd06c183f55bf5a43c2e4532d5e8db8bfacaad`  
		Last Modified: Fri, 14 Feb 2025 19:25:37 GMT  
		Size: 3.2 MB (3177535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:376a7544d345f9c09b5eaa181509524a03932c1287abe74ad6e7f56f1887201f`  
		Last Modified: Fri, 14 Feb 2025 22:35:34 GMT  
		Size: 45.3 MB (45307932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc95fd6963eaa2fb3ff3536c296e611ca0c47b6bea5ce2b773e948e7b6265d5c`  
		Last Modified: Fri, 14 Feb 2025 22:35:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:030126f47f27f3ce38e0888c66d72341fc50612628c65d7cc1113e9f24719a25`  
		Last Modified: Fri, 14 Feb 2025 22:35:30 GMT  
		Size: 748.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:b213cfde217f870e9053d76609c339daf28bb74540095e230f46ae28138bcdc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5904279525564e80da0f08c89ca11c526772a86d23fb9b02a04379c1070689e7`

```dockerfile
```

-	Layers:
	-	`sha256:e65a751e4ebbe01c489945b75af022bbf730739f9461d53e7fe1582897613883`  
		Last Modified: Fri, 14 Feb 2025 22:35:22 GMT  
		Size: 13.9 KB (13879 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:c47cd4e858cc011a15c1552adf5b597b48d5a4e5397b316984f49e0276915b8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50083594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8407a3f298f2eb072038604241ba675278f7dfee7dc8711d94aa6211024f4fe5`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
CMD ["/bin/sh"]
# Wed, 03 Jul 2024 16:05:23 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 03 Jul 2024 16:05:23 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Wed, 03 Jul 2024 16:05:23 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:05:23 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:05:23 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY entrypoint.sh / # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Wed, 03 Jul 2024 16:05:23 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:05:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3af5b4a9e68048bc28c635c6cdd2bf674e036e30150d45c98f57dadf501bc38`  
		Last Modified: Wed, 15 Jan 2025 15:49:14 GMT  
		Size: 46.7 MB (46722139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eea7c168bfe8c8a324b20ba48b48284526d090888b95d50676ce20f9c819ae9b`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64be7b705b54726046dc93a27171026cd0aa29e2a934cb73362afbc0b5d4c4a6`  
		Last Modified: Wed, 15 Jan 2025 15:49:11 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:93d8da96e4cd0f5ee0c2c7a615697f97dcd00f5d85a818e3ce3613d80f78d43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2150942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c1b6597675f703946ec5902a9e8bd2709e0d595c153c67d571fdb0f0f5db90`

```dockerfile
```

-	Layers:
	-	`sha256:411b819abd849c70298d82bc2d4050b5628a8f08e8e1a11f73bd3c87be13ff82`  
		Last Modified: Fri, 14 Feb 2025 22:35:23 GMT  
		Size: 2.1 MB (2136824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a937b18244718d4a5bbee3f92927c370d7bc7d9f2da5f45f557cf70c123a755c`  
		Last Modified: Fri, 14 Feb 2025 22:35:23 GMT  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.in-toto+json
