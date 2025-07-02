<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `znc`

-	[`znc:1.10`](#znc110)
-	[`znc:1.10-slim`](#znc110-slim)
-	[`znc:1.10.1`](#znc1101)
-	[`znc:1.10.1-slim`](#znc1101-slim)
-	[`znc:latest`](#znclatest)
-	[`znc:slim`](#zncslim)

## `znc:1.10`

```console
$ docker pull znc@sha256:6e78590534c0875e2feb9feb0d5c2cbaaffadbcb717666adbd0084443cf0308a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10` - linux; amd64

```console
$ docker pull znc@sha256:9bfd7bbfd8fef0877eef1ca9a05b3090e1c751714ea7e9f75510fecc2ad443e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169352200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20411f5c040aafa41f3e0eb9d81f97947a4da83cf491900d7c73426b17824898`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df499bc9dda0609cc5f11532cef79b59108b2b3dcca2e9e0c750886c099398e`  
		Last Modified: Tue, 01 Jul 2025 21:54:06 GMT  
		Size: 46.0 MB (46023617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffa66b3655b43c16f211fc86fa2afcef505a3fb983be90c2338f8d30a779a02`  
		Last Modified: Tue, 01 Jul 2025 22:08:39 GMT  
		Size: 119.5 MB (119530488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ec6990e1fad0f02541c2b51032d0baeceb941fb77dd06b33119c0d107373fb`  
		Last Modified: Tue, 01 Jul 2025 22:08:33 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:04a9ad50a593cf31a59ad7be8dd261f05a72cfb912fbb47ae14f30a2a14d4376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6872634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0826493d6d3acc11d26ff76924629f728c3b94e0f3e42e2af99bbc1167c62b`

```dockerfile
```

-	Layers:
	-	`sha256:a52d7d27923458ee29df135d50df9905029deca72d51d0b45f4b1fd9d7aadf73`  
		Last Modified: Wed, 02 Jul 2025 00:35:24 GMT  
		Size: 6.9 MB (6863031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8086dada75cab3873258f7814b29c4ee3b70525489be9c43b355fc3b2b41d62`  
		Last Modified: Wed, 02 Jul 2025 00:35:24 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm variant v6

```console
$ docker pull znc@sha256:c6a9b205dbdeeee827766035a4e223081d4b17a80352349d89fd45d4e4b4051b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148645333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c519fb8a7ee86f9d36f5b61d32ab0721c451a8c38eda926e47c72280103dcc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10583d44fa52446e3667662f7fa18afa8e72ed70be5212b1b8c1d0495fb02a0a`  
		Last Modified: Tue, 01 Jul 2025 21:54:50 GMT  
		Size: 44.6 MB (44603073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a65504a93e4d3ce9dbb66b3a1a8980814fd253719e8d3a5ecd96c80541b064`  
		Last Modified: Tue, 01 Jul 2025 22:08:04 GMT  
		Size: 100.5 MB (100540083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5859dbc55100dcc7662e04201987908b83f6df7019585cc1edb17762ce88e2e`  
		Last Modified: Tue, 01 Jul 2025 22:07:58 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:da9977ec50a9c1f5a1d579ab9a0b5cb79017174603cfe6ad205ea419fc478527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67580526c07443e4ea4ed99f2645e07dbcf3c27f7fb816d307334f6f3b0f62d4`

```dockerfile
```

-	Layers:
	-	`sha256:92747ba8d36319c049556e2a43c773c485d468c9e0f591e5217fa9308f143f5a`  
		Last Modified: Wed, 02 Jul 2025 00:35:30 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:8a4391b8bcd0a1296f8fa6ae4aca280b0c05efb65ddc186e1c153edb8c42bb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163112726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447f20ce1c6d12369a6b82c90a8d11abbe73a2aeabefa4061077f6abc1aa67ba`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:22:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 09 Jun 2025 21:22:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Mon, 09 Jun 2025 21:22:37 GMT
ARG MAKEFLAGS=
# Mon, 09 Jun 2025 21:22:37 GMT
ENV ZNC_VERSION=1.10.0
# Mon, 09 Jun 2025 21:22:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY entrypoint.sh / # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
VOLUME [/znc-data]
# Mon, 09 Jun 2025 21:22:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jun 2025 21:22:37 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b787480e5244847f399b065a5f466afafbdfa7754832a387cd2374dab6d0126`  
		Last Modified: Mon, 09 Jun 2025 22:25:03 GMT  
		Size: 45.8 MB (45804478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e983a7f6498c03a0e28c4d4bc3295109971ab0d247b76c1d407258b6f52b25`  
		Last Modified: Mon, 09 Jun 2025 22:25:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c22321b9fbea5a7461b17ebd38c8ca2d8f594cbccc2e166ea6898d9fcd92a`  
		Last Modified: Mon, 09 Jun 2025 22:25:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cc3d62fdace1ab793badc1c3f8b9cf01f66ad34c4b693e8603ff3d8c1ca72`  
		Last Modified: Mon, 09 Jun 2025 23:09:11 GMT  
		Size: 113.2 MB (113171056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ceabd94a1ced1ad9164056f9bad37506df8c1ed3c331def4f708f8cb59e7e`  
		Last Modified: Mon, 09 Jun 2025 23:09:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:ae369fb520866723ddfe10ef081cce3a6c7384de52904f78760fd38940f80339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfbe38f716e377c55be7b4cdf425fa7b345bcd3e760c9ebdc89a06bc0d27943`

```dockerfile
```

-	Layers:
	-	`sha256:a7fbdb34fdd2e05b5d137553178e463ad01648c1496cc99eb83677380af601ac`  
		Last Modified: Tue, 10 Jun 2025 00:35:36 GMT  
		Size: 6.9 MB (6942455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17c031e491f584635177de81f9fe4bd94f2716dd48318a66a59191073c9e9352`  
		Last Modified: Tue, 10 Jun 2025 00:35:37 GMT  
		Size: 9.7 KB (9695 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10-slim`

```console
$ docker pull znc@sha256:62154240d1fc0df8aaa23e63d52ebff721c405d3ea43c5c31c1b6ef9594bec39
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10-slim` - linux; amd64

```console
$ docker pull znc@sha256:54b398535edaccbc56382728bfd6e18de703d700a373a3919c66b2749509176a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49821382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df576f91616b3ffe10e2cad9831e645eda67cf73c6ce140f71a41e4511278d1a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df499bc9dda0609cc5f11532cef79b59108b2b3dcca2e9e0c750886c099398e`  
		Last Modified: Tue, 01 Jul 2025 21:54:06 GMT  
		Size: 46.0 MB (46023617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:995d4cb4a3d996681244fa39f301c09cd2de1493c38b255ee4a0c9db4cf50d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1768730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6864343a9bd1b3346af8e429e14b7a98c4335bcfe70d7a43226d25f7d762f96d`

```dockerfile
```

-	Layers:
	-	`sha256:0d560a81d59bda3753bb76d419ccc282733fcc7218efc54fea44efd728a361bb`  
		Last Modified: Wed, 02 Jul 2025 00:35:29 GMT  
		Size: 1.8 MB (1754699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ca23a53376efdf0463bb4a159f0119b7597d9e119475638fb09700dbb8b2c9`  
		Last Modified: Wed, 02 Jul 2025 00:35:29 GMT  
		Size: 14.0 KB (14031 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:95e8fbb7518369d9e8803ea8ad6650e3b839f77681893157476858af61915d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48104921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768bb0d61fd0486cf3377db66109dbd9bdb0ed1300588ca0169cab802e7da657`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10583d44fa52446e3667662f7fa18afa8e72ed70be5212b1b8c1d0495fb02a0a`  
		Last Modified: Tue, 01 Jul 2025 21:54:50 GMT  
		Size: 44.6 MB (44603073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:aebf7974735485374bb0486f3ae767a0f455e02faffe69c91554b6862b649772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c13f2a3f0b1e043bb836817ea137dcbd184cde1d7b1981cc70dd41c031c9e23`

```dockerfile
```

-	Layers:
	-	`sha256:179aab84875f81586b683126de6fd069d2a5debf8870652c3d15b04ab296546c`  
		Last Modified: Wed, 02 Jul 2025 00:35:33 GMT  
		Size: 13.9 KB (13884 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:e13fdfc131f86dbf0d09922b989a80dacbec08988f5fd08b457ad8ae726b4999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49941339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58499efbd94fde1b46f248536d1e6d44ad8b802a64b2070649f3d6ae4b3ffd15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:22:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 09 Jun 2025 21:22:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Mon, 09 Jun 2025 21:22:37 GMT
ARG MAKEFLAGS=
# Mon, 09 Jun 2025 21:22:37 GMT
ENV ZNC_VERSION=1.10.0
# Mon, 09 Jun 2025 21:22:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY entrypoint.sh / # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
VOLUME [/znc-data]
# Mon, 09 Jun 2025 21:22:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b787480e5244847f399b065a5f466afafbdfa7754832a387cd2374dab6d0126`  
		Last Modified: Mon, 09 Jun 2025 22:25:03 GMT  
		Size: 45.8 MB (45804478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e983a7f6498c03a0e28c4d4bc3295109971ab0d247b76c1d407258b6f52b25`  
		Last Modified: Mon, 09 Jun 2025 22:25:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c22321b9fbea5a7461b17ebd38c8ca2d8f594cbccc2e166ea6898d9fcd92a`  
		Last Modified: Mon, 09 Jun 2025 22:25:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:6defd414b1ccd0c21f52e66e36ac551bb41e074d3beba3f8b7cc8f09ace6826f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1768952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a0f605c2f5fb11cc018bbf3e7172bb3d6168e83936789a1b1fbac6c7331d5d`

```dockerfile
```

-	Layers:
	-	`sha256:83c36e4d16368632447e3fe669b338d5f6d53af31c40ebecd16e60a335ca5161`  
		Last Modified: Tue, 10 Jun 2025 00:35:42 GMT  
		Size: 1.8 MB (1754829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa1fcf2608848c5da159105860488d6ae30cc6fe12d3a48f1d5124ba4a3bc02`  
		Last Modified: Tue, 10 Jun 2025 00:35:43 GMT  
		Size: 14.1 KB (14123 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.1`

```console
$ docker pull znc@sha256:68de0cb1a84068415f6b9e999d1bcc5506130d50bbd13758706341b5b2726c17
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown

### `znc:1.10.1` - linux; amd64

```console
$ docker pull znc@sha256:9bfd7bbfd8fef0877eef1ca9a05b3090e1c751714ea7e9f75510fecc2ad443e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169352200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20411f5c040aafa41f3e0eb9d81f97947a4da83cf491900d7c73426b17824898`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df499bc9dda0609cc5f11532cef79b59108b2b3dcca2e9e0c750886c099398e`  
		Last Modified: Tue, 01 Jul 2025 21:54:06 GMT  
		Size: 46.0 MB (46023617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffa66b3655b43c16f211fc86fa2afcef505a3fb983be90c2338f8d30a779a02`  
		Last Modified: Tue, 01 Jul 2025 22:08:39 GMT  
		Size: 119.5 MB (119530488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ec6990e1fad0f02541c2b51032d0baeceb941fb77dd06b33119c0d107373fb`  
		Last Modified: Tue, 01 Jul 2025 22:08:33 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1` - unknown; unknown

```console
$ docker pull znc@sha256:04a9ad50a593cf31a59ad7be8dd261f05a72cfb912fbb47ae14f30a2a14d4376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6872634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0826493d6d3acc11d26ff76924629f728c3b94e0f3e42e2af99bbc1167c62b`

```dockerfile
```

-	Layers:
	-	`sha256:a52d7d27923458ee29df135d50df9905029deca72d51d0b45f4b1fd9d7aadf73`  
		Last Modified: Wed, 02 Jul 2025 00:35:24 GMT  
		Size: 6.9 MB (6863031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8086dada75cab3873258f7814b29c4ee3b70525489be9c43b355fc3b2b41d62`  
		Last Modified: Wed, 02 Jul 2025 00:35:24 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1` - linux; arm variant v6

```console
$ docker pull znc@sha256:c6a9b205dbdeeee827766035a4e223081d4b17a80352349d89fd45d4e4b4051b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148645333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c519fb8a7ee86f9d36f5b61d32ab0721c451a8c38eda926e47c72280103dcc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10583d44fa52446e3667662f7fa18afa8e72ed70be5212b1b8c1d0495fb02a0a`  
		Last Modified: Tue, 01 Jul 2025 21:54:50 GMT  
		Size: 44.6 MB (44603073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a65504a93e4d3ce9dbb66b3a1a8980814fd253719e8d3a5ecd96c80541b064`  
		Last Modified: Tue, 01 Jul 2025 22:08:04 GMT  
		Size: 100.5 MB (100540083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5859dbc55100dcc7662e04201987908b83f6df7019585cc1edb17762ce88e2e`  
		Last Modified: Tue, 01 Jul 2025 22:07:58 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1` - unknown; unknown

```console
$ docker pull znc@sha256:da9977ec50a9c1f5a1d579ab9a0b5cb79017174603cfe6ad205ea419fc478527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67580526c07443e4ea4ed99f2645e07dbcf3c27f7fb816d307334f6f3b0f62d4`

```dockerfile
```

-	Layers:
	-	`sha256:92747ba8d36319c049556e2a43c773c485d468c9e0f591e5217fa9308f143f5a`  
		Last Modified: Wed, 02 Jul 2025 00:35:30 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.1-slim`

```console
$ docker pull znc@sha256:8af683486a5e11a563689b70f0e9787d640d4e664c4de8c1ec1aeea083f80229
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown

### `znc:1.10.1-slim` - linux; amd64

```console
$ docker pull znc@sha256:54b398535edaccbc56382728bfd6e18de703d700a373a3919c66b2749509176a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49821382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df576f91616b3ffe10e2cad9831e645eda67cf73c6ce140f71a41e4511278d1a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df499bc9dda0609cc5f11532cef79b59108b2b3dcca2e9e0c750886c099398e`  
		Last Modified: Tue, 01 Jul 2025 21:54:06 GMT  
		Size: 46.0 MB (46023617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:995d4cb4a3d996681244fa39f301c09cd2de1493c38b255ee4a0c9db4cf50d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1768730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6864343a9bd1b3346af8e429e14b7a98c4335bcfe70d7a43226d25f7d762f96d`

```dockerfile
```

-	Layers:
	-	`sha256:0d560a81d59bda3753bb76d419ccc282733fcc7218efc54fea44efd728a361bb`  
		Last Modified: Wed, 02 Jul 2025 00:35:29 GMT  
		Size: 1.8 MB (1754699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ca23a53376efdf0463bb4a159f0119b7597d9e119475638fb09700dbb8b2c9`  
		Last Modified: Wed, 02 Jul 2025 00:35:29 GMT  
		Size: 14.0 KB (14031 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:95e8fbb7518369d9e8803ea8ad6650e3b839f77681893157476858af61915d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48104921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768bb0d61fd0486cf3377db66109dbd9bdb0ed1300588ca0169cab802e7da657`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10583d44fa52446e3667662f7fa18afa8e72ed70be5212b1b8c1d0495fb02a0a`  
		Last Modified: Tue, 01 Jul 2025 21:54:50 GMT  
		Size: 44.6 MB (44603073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:aebf7974735485374bb0486f3ae767a0f455e02faffe69c91554b6862b649772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c13f2a3f0b1e043bb836817ea137dcbd184cde1d7b1981cc70dd41c031c9e23`

```dockerfile
```

-	Layers:
	-	`sha256:179aab84875f81586b683126de6fd069d2a5debf8870652c3d15b04ab296546c`  
		Last Modified: Wed, 02 Jul 2025 00:35:33 GMT  
		Size: 13.9 KB (13884 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:latest`

```console
$ docker pull znc@sha256:6e78590534c0875e2feb9feb0d5c2cbaaffadbcb717666adbd0084443cf0308a
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
$ docker pull znc@sha256:9bfd7bbfd8fef0877eef1ca9a05b3090e1c751714ea7e9f75510fecc2ad443e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169352200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20411f5c040aafa41f3e0eb9d81f97947a4da83cf491900d7c73426b17824898`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df499bc9dda0609cc5f11532cef79b59108b2b3dcca2e9e0c750886c099398e`  
		Last Modified: Tue, 01 Jul 2025 21:54:06 GMT  
		Size: 46.0 MB (46023617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dffa66b3655b43c16f211fc86fa2afcef505a3fb983be90c2338f8d30a779a02`  
		Last Modified: Tue, 01 Jul 2025 22:08:39 GMT  
		Size: 119.5 MB (119530488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45ec6990e1fad0f02541c2b51032d0baeceb941fb77dd06b33119c0d107373fb`  
		Last Modified: Tue, 01 Jul 2025 22:08:33 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:04a9ad50a593cf31a59ad7be8dd261f05a72cfb912fbb47ae14f30a2a14d4376
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6872634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c0826493d6d3acc11d26ff76924629f728c3b94e0f3e42e2af99bbc1167c62b`

```dockerfile
```

-	Layers:
	-	`sha256:a52d7d27923458ee29df135d50df9905029deca72d51d0b45f4b1fd9d7aadf73`  
		Last Modified: Wed, 02 Jul 2025 00:35:24 GMT  
		Size: 6.9 MB (6863031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8086dada75cab3873258f7814b29c4ee3b70525489be9c43b355fc3b2b41d62`  
		Last Modified: Wed, 02 Jul 2025 00:35:24 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:c6a9b205dbdeeee827766035a4e223081d4b17a80352349d89fd45d4e4b4051b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148645333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c519fb8a7ee86f9d36f5b61d32ab0721c451a8c38eda926e47c72280103dcc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10583d44fa52446e3667662f7fa18afa8e72ed70be5212b1b8c1d0495fb02a0a`  
		Last Modified: Tue, 01 Jul 2025 21:54:50 GMT  
		Size: 44.6 MB (44603073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a65504a93e4d3ce9dbb66b3a1a8980814fd253719e8d3a5ecd96c80541b064`  
		Last Modified: Tue, 01 Jul 2025 22:08:04 GMT  
		Size: 100.5 MB (100540083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5859dbc55100dcc7662e04201987908b83f6df7019585cc1edb17762ce88e2e`  
		Last Modified: Tue, 01 Jul 2025 22:07:58 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:da9977ec50a9c1f5a1d579ab9a0b5cb79017174603cfe6ad205ea419fc478527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67580526c07443e4ea4ed99f2645e07dbcf3c27f7fb816d307334f6f3b0f62d4`

```dockerfile
```

-	Layers:
	-	`sha256:92747ba8d36319c049556e2a43c773c485d468c9e0f591e5217fa9308f143f5a`  
		Last Modified: Wed, 02 Jul 2025 00:35:30 GMT  
		Size: 9.5 KB (9456 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:8a4391b8bcd0a1296f8fa6ae4aca280b0c05efb65ddc186e1c153edb8c42bb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163112726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447f20ce1c6d12369a6b82c90a8d11abbe73a2aeabefa4061077f6abc1aa67ba`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:22:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 09 Jun 2025 21:22:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Mon, 09 Jun 2025 21:22:37 GMT
ARG MAKEFLAGS=
# Mon, 09 Jun 2025 21:22:37 GMT
ENV ZNC_VERSION=1.10.0
# Mon, 09 Jun 2025 21:22:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY entrypoint.sh / # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
VOLUME [/znc-data]
# Mon, 09 Jun 2025 21:22:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 09 Jun 2025 21:22:37 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b787480e5244847f399b065a5f466afafbdfa7754832a387cd2374dab6d0126`  
		Last Modified: Mon, 09 Jun 2025 22:25:03 GMT  
		Size: 45.8 MB (45804478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e983a7f6498c03a0e28c4d4bc3295109971ab0d247b76c1d407258b6f52b25`  
		Last Modified: Mon, 09 Jun 2025 22:25:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c22321b9fbea5a7461b17ebd38c8ca2d8f594cbccc2e166ea6898d9fcd92a`  
		Last Modified: Mon, 09 Jun 2025 22:25:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057cc3d62fdace1ab793badc1c3f8b9cf01f66ad34c4b693e8603ff3d8c1ca72`  
		Last Modified: Mon, 09 Jun 2025 23:09:11 GMT  
		Size: 113.2 MB (113171056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1ceabd94a1ced1ad9164056f9bad37506df8c1ed3c331def4f708f8cb59e7e`  
		Last Modified: Mon, 09 Jun 2025 23:09:03 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:ae369fb520866723ddfe10ef081cce3a6c7384de52904f78760fd38940f80339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcfbe38f716e377c55be7b4cdf425fa7b345bcd3e760c9ebdc89a06bc0d27943`

```dockerfile
```

-	Layers:
	-	`sha256:a7fbdb34fdd2e05b5d137553178e463ad01648c1496cc99eb83677380af601ac`  
		Last Modified: Tue, 10 Jun 2025 00:35:36 GMT  
		Size: 6.9 MB (6942455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17c031e491f584635177de81f9fe4bd94f2716dd48318a66a59191073c9e9352`  
		Last Modified: Tue, 10 Jun 2025 00:35:37 GMT  
		Size: 9.7 KB (9695 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:slim`

```console
$ docker pull znc@sha256:62154240d1fc0df8aaa23e63d52ebff721c405d3ea43c5c31c1b6ef9594bec39
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
$ docker pull znc@sha256:54b398535edaccbc56382728bfd6e18de703d700a373a3919c66b2749509176a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49821382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df576f91616b3ffe10e2cad9831e645eda67cf73c6ce140f71a41e4511278d1a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2df499bc9dda0609cc5f11532cef79b59108b2b3dcca2e9e0c750886c099398e`  
		Last Modified: Tue, 01 Jul 2025 21:54:06 GMT  
		Size: 46.0 MB (46023617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:995d4cb4a3d996681244fa39f301c09cd2de1493c38b255ee4a0c9db4cf50d35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1768730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6864343a9bd1b3346af8e429e14b7a98c4335bcfe70d7a43226d25f7d762f96d`

```dockerfile
```

-	Layers:
	-	`sha256:0d560a81d59bda3753bb76d419ccc282733fcc7218efc54fea44efd728a361bb`  
		Last Modified: Wed, 02 Jul 2025 00:35:29 GMT  
		Size: 1.8 MB (1754699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31ca23a53376efdf0463bb4a159f0119b7597d9e119475638fb09700dbb8b2c9`  
		Last Modified: Wed, 02 Jul 2025 00:35:29 GMT  
		Size: 14.0 KB (14031 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:95e8fbb7518369d9e8803ea8ad6650e3b839f77681893157476858af61915d61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48104921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:768bb0d61fd0486cf3377db66109dbd9bdb0ed1300588ca0169cab802e7da657`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 01 Jul 2025 21:26:43 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 01 Jul 2025 21:26:43 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 01 Jul 2025 21:26:43 GMT
ARG MAKEFLAGS=
# Tue, 01 Jul 2025 21:26:43 GMT
ENV ZNC_VERSION=1.10.1
# Tue, 01 Jul 2025 21:26:43 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY entrypoint.sh / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
VOLUME [/znc-data]
# Tue, 01 Jul 2025 21:26:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10583d44fa52446e3667662f7fa18afa8e72ed70be5212b1b8c1d0495fb02a0a`  
		Last Modified: Tue, 01 Jul 2025 21:54:50 GMT  
		Size: 44.6 MB (44603073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54f67000c7abdc9c04119702032ad314da673d105a8a7e7638e126b932c3fbb8`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ca7d26fe0d2837501aeaaf2d70e473c63626503c411a6d4bd7f68d3d9ebb4d`  
		Last Modified: Tue, 01 Jul 2025 21:53:59 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:aebf7974735485374bb0486f3ae767a0f455e02faffe69c91554b6862b649772
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c13f2a3f0b1e043bb836817ea137dcbd184cde1d7b1981cc70dd41c031c9e23`

```dockerfile
```

-	Layers:
	-	`sha256:179aab84875f81586b683126de6fd069d2a5debf8870652c3d15b04ab296546c`  
		Last Modified: Wed, 02 Jul 2025 00:35:33 GMT  
		Size: 13.9 KB (13884 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:e13fdfc131f86dbf0d09922b989a80dacbec08988f5fd08b457ad8ae726b4999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49941339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58499efbd94fde1b46f248536d1e6d44ad8b802a64b2070649f3d6ae4b3ffd15`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Mon, 09 Jun 2025 21:22:37 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Mon, 09 Jun 2025 21:22:37 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Mon, 09 Jun 2025 21:22:37 GMT
ARG MAKEFLAGS=
# Mon, 09 Jun 2025 21:22:37 GMT
ENV ZNC_VERSION=1.10.0
# Mon, 09 Jun 2025 21:22:37 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY entrypoint.sh / # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Mon, 09 Jun 2025 21:22:37 GMT
VOLUME [/znc-data]
# Mon, 09 Jun 2025 21:22:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b787480e5244847f399b065a5f466afafbdfa7754832a387cd2374dab6d0126`  
		Last Modified: Mon, 09 Jun 2025 22:25:03 GMT  
		Size: 45.8 MB (45804478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9e983a7f6498c03a0e28c4d4bc3295109971ab0d247b76c1d407258b6f52b25`  
		Last Modified: Mon, 09 Jun 2025 22:25:00 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d6c22321b9fbea5a7461b17ebd38c8ca2d8f594cbccc2e166ea6898d9fcd92a`  
		Last Modified: Mon, 09 Jun 2025 22:25:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:6defd414b1ccd0c21f52e66e36ac551bb41e074d3beba3f8b7cc8f09ace6826f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1768952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15a0f605c2f5fb11cc018bbf3e7172bb3d6168e83936789a1b1fbac6c7331d5d`

```dockerfile
```

-	Layers:
	-	`sha256:83c36e4d16368632447e3fe669b338d5f6d53af31c40ebecd16e60a335ca5161`  
		Last Modified: Tue, 10 Jun 2025 00:35:42 GMT  
		Size: 1.8 MB (1754829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaa1fcf2608848c5da159105860488d6ae30cc6fe12d3a48f1d5124ba4a3bc02`  
		Last Modified: Tue, 10 Jun 2025 00:35:43 GMT  
		Size: 14.1 KB (14123 bytes)  
		MIME: application/vnd.in-toto+json
