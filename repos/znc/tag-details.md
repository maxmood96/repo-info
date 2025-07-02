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
$ docker pull znc@sha256:94d20a453cb9f831371a557f1148f68377200bca2d7546cc08cff542da8f490b
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
$ docker pull znc@sha256:b5977bef2f98a51f42af4116865a21e4a5c743cf76bdd95d0543a3ede0df41e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163125472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bade079fc6e38030a6adc18e6939c8ef9ce3a6aac285cebc50244a4d58d29793`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154c1d21532aa209257d70744f0b01b1d8e7921f42219cad940056ce4361c17`  
		Last Modified: Wed, 02 Jul 2025 02:44:08 GMT  
		Size: 45.8 MB (45817276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5509588fe9fd114a19342f0792dd3ee8d9639a82476f089677f8ac6e0f979d`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd028a2febfde0baf6a60cb6318a60c44aad9230ee763792a6fbe66ec2bab14`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febee016daa37ab027ced6c64e4d5f0f84429eb58d2d564b0687e7bf01fab37`  
		Last Modified: Wed, 02 Jul 2025 04:16:16 GMT  
		Size: 113.2 MB (113171005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37cee817cff2068d94e20e8ecb64d6b424cbf002b2cd9e5e78a9e118da52271`  
		Last Modified: Wed, 02 Jul 2025 04:16:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:aec07c35cc7d7a705ad8e9e78c53ed938277f1474e3ce72adcea224b25012871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76c3f763db23c842dd7fa55a42984f33408f6ee9a4d471f51eb2c6560c48870`

```dockerfile
```

-	Layers:
	-	`sha256:d8a9d4dd176c0a39d7c9617a3f9a68530bb0d0f38bdcfe279c5eb28ff484bd24`  
		Last Modified: Wed, 02 Jul 2025 06:35:24 GMT  
		Size: 6.9 MB (6942455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae66605edd22ed28db820a31dbfab1c1fd637ef676db0bb5a508c43db3b6880d`  
		Last Modified: Wed, 02 Jul 2025 06:35:25 GMT  
		Size: 9.7 KB (9695 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10-slim`

```console
$ docker pull znc@sha256:3f2337d1d958c792250b65f5add0e84a6509f33cb05dc0f3e0f25a5af1c03418
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
$ docker pull znc@sha256:06112d58fabc065f2556506045d56a9e39af0f6abaad3bf8bdccaa43ae8b3acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49954138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecef7aae1a6cc10b959dbb26adea8d134d3acb59f19180081da4b39bc09d6da`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154c1d21532aa209257d70744f0b01b1d8e7921f42219cad940056ce4361c17`  
		Last Modified: Wed, 02 Jul 2025 02:44:08 GMT  
		Size: 45.8 MB (45817276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5509588fe9fd114a19342f0792dd3ee8d9639a82476f089677f8ac6e0f979d`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd028a2febfde0baf6a60cb6318a60c44aad9230ee763792a6fbe66ec2bab14`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:299be990cc22d96e2cade99c484989cf5cb72ac3d286d5d0236045ed54867c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1768952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91c672e464b3c171fafe67ce5d7ff062de078ff6ffc4f16ded7e82f7ebd1581`

```dockerfile
```

-	Layers:
	-	`sha256:ce959d80a9d6a2bc34fbdaeedc425ba936406f51b7e44321d1544f1231b5d8db`  
		Last Modified: Wed, 02 Jul 2025 03:35:24 GMT  
		Size: 1.8 MB (1754829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b3cc6522fb27074edf7c7e58546598f865b65b132630110d148baa3ba6d5d3`  
		Last Modified: Wed, 02 Jul 2025 03:35:24 GMT  
		Size: 14.1 KB (14123 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.1`

```console
$ docker pull znc@sha256:94d20a453cb9f831371a557f1148f68377200bca2d7546cc08cff542da8f490b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
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

### `znc:1.10.1` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:b5977bef2f98a51f42af4116865a21e4a5c743cf76bdd95d0543a3ede0df41e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163125472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bade079fc6e38030a6adc18e6939c8ef9ce3a6aac285cebc50244a4d58d29793`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154c1d21532aa209257d70744f0b01b1d8e7921f42219cad940056ce4361c17`  
		Last Modified: Wed, 02 Jul 2025 02:44:08 GMT  
		Size: 45.8 MB (45817276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5509588fe9fd114a19342f0792dd3ee8d9639a82476f089677f8ac6e0f979d`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd028a2febfde0baf6a60cb6318a60c44aad9230ee763792a6fbe66ec2bab14`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febee016daa37ab027ced6c64e4d5f0f84429eb58d2d564b0687e7bf01fab37`  
		Last Modified: Wed, 02 Jul 2025 04:16:16 GMT  
		Size: 113.2 MB (113171005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37cee817cff2068d94e20e8ecb64d6b424cbf002b2cd9e5e78a9e118da52271`  
		Last Modified: Wed, 02 Jul 2025 04:16:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1` - unknown; unknown

```console
$ docker pull znc@sha256:aec07c35cc7d7a705ad8e9e78c53ed938277f1474e3ce72adcea224b25012871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76c3f763db23c842dd7fa55a42984f33408f6ee9a4d471f51eb2c6560c48870`

```dockerfile
```

-	Layers:
	-	`sha256:d8a9d4dd176c0a39d7c9617a3f9a68530bb0d0f38bdcfe279c5eb28ff484bd24`  
		Last Modified: Wed, 02 Jul 2025 06:35:24 GMT  
		Size: 6.9 MB (6942455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae66605edd22ed28db820a31dbfab1c1fd637ef676db0bb5a508c43db3b6880d`  
		Last Modified: Wed, 02 Jul 2025 06:35:25 GMT  
		Size: 9.7 KB (9695 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.1-slim`

```console
$ docker pull znc@sha256:3f2337d1d958c792250b65f5add0e84a6509f33cb05dc0f3e0f25a5af1c03418
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
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

### `znc:1.10.1-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:06112d58fabc065f2556506045d56a9e39af0f6abaad3bf8bdccaa43ae8b3acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49954138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecef7aae1a6cc10b959dbb26adea8d134d3acb59f19180081da4b39bc09d6da`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154c1d21532aa209257d70744f0b01b1d8e7921f42219cad940056ce4361c17`  
		Last Modified: Wed, 02 Jul 2025 02:44:08 GMT  
		Size: 45.8 MB (45817276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5509588fe9fd114a19342f0792dd3ee8d9639a82476f089677f8ac6e0f979d`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd028a2febfde0baf6a60cb6318a60c44aad9230ee763792a6fbe66ec2bab14`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:299be990cc22d96e2cade99c484989cf5cb72ac3d286d5d0236045ed54867c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1768952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91c672e464b3c171fafe67ce5d7ff062de078ff6ffc4f16ded7e82f7ebd1581`

```dockerfile
```

-	Layers:
	-	`sha256:ce959d80a9d6a2bc34fbdaeedc425ba936406f51b7e44321d1544f1231b5d8db`  
		Last Modified: Wed, 02 Jul 2025 03:35:24 GMT  
		Size: 1.8 MB (1754829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b3cc6522fb27074edf7c7e58546598f865b65b132630110d148baa3ba6d5d3`  
		Last Modified: Wed, 02 Jul 2025 03:35:24 GMT  
		Size: 14.1 KB (14123 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:latest`

```console
$ docker pull znc@sha256:94d20a453cb9f831371a557f1148f68377200bca2d7546cc08cff542da8f490b
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
$ docker pull znc@sha256:b5977bef2f98a51f42af4116865a21e4a5c743cf76bdd95d0543a3ede0df41e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163125472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bade079fc6e38030a6adc18e6939c8ef9ce3a6aac285cebc50244a4d58d29793`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154c1d21532aa209257d70744f0b01b1d8e7921f42219cad940056ce4361c17`  
		Last Modified: Wed, 02 Jul 2025 02:44:08 GMT  
		Size: 45.8 MB (45817276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5509588fe9fd114a19342f0792dd3ee8d9639a82476f089677f8ac6e0f979d`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd028a2febfde0baf6a60cb6318a60c44aad9230ee763792a6fbe66ec2bab14`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6febee016daa37ab027ced6c64e4d5f0f84429eb58d2d564b0687e7bf01fab37`  
		Last Modified: Wed, 02 Jul 2025 04:16:16 GMT  
		Size: 113.2 MB (113171005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a37cee817cff2068d94e20e8ecb64d6b424cbf002b2cd9e5e78a9e118da52271`  
		Last Modified: Wed, 02 Jul 2025 04:16:11 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:aec07c35cc7d7a705ad8e9e78c53ed938277f1474e3ce72adcea224b25012871
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6952150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a76c3f763db23c842dd7fa55a42984f33408f6ee9a4d471f51eb2c6560c48870`

```dockerfile
```

-	Layers:
	-	`sha256:d8a9d4dd176c0a39d7c9617a3f9a68530bb0d0f38bdcfe279c5eb28ff484bd24`  
		Last Modified: Wed, 02 Jul 2025 06:35:24 GMT  
		Size: 6.9 MB (6942455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae66605edd22ed28db820a31dbfab1c1fd637ef676db0bb5a508c43db3b6880d`  
		Last Modified: Wed, 02 Jul 2025 06:35:25 GMT  
		Size: 9.7 KB (9695 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:slim`

```console
$ docker pull znc@sha256:3f2337d1d958c792250b65f5add0e84a6509f33cb05dc0f3e0f25a5af1c03418
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
$ docker pull znc@sha256:06112d58fabc065f2556506045d56a9e39af0f6abaad3bf8bdccaa43ae8b3acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49954138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ecef7aae1a6cc10b959dbb26adea8d134d3acb59f19180081da4b39bc09d6da`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
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
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5154c1d21532aa209257d70744f0b01b1d8e7921f42219cad940056ce4361c17`  
		Last Modified: Wed, 02 Jul 2025 02:44:08 GMT  
		Size: 45.8 MB (45817276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5509588fe9fd114a19342f0792dd3ee8d9639a82476f089677f8ac6e0f979d`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd028a2febfde0baf6a60cb6318a60c44aad9230ee763792a6fbe66ec2bab14`  
		Last Modified: Wed, 02 Jul 2025 02:44:00 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:299be990cc22d96e2cade99c484989cf5cb72ac3d286d5d0236045ed54867c82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1768952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91c672e464b3c171fafe67ce5d7ff062de078ff6ffc4f16ded7e82f7ebd1581`

```dockerfile
```

-	Layers:
	-	`sha256:ce959d80a9d6a2bc34fbdaeedc425ba936406f51b7e44321d1544f1231b5d8db`  
		Last Modified: Wed, 02 Jul 2025 03:35:24 GMT  
		Size: 1.8 MB (1754829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14b3cc6522fb27074edf7c7e58546598f865b65b132630110d148baa3ba6d5d3`  
		Last Modified: Wed, 02 Jul 2025 03:35:24 GMT  
		Size: 14.1 KB (14123 bytes)  
		MIME: application/vnd.in-toto+json
