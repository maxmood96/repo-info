<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `znc`

-	[`znc:1.10`](#znc110)
-	[`znc:1.10-slim`](#znc110-slim)
-	[`znc:1.10.2`](#znc1102)
-	[`znc:1.10.2-slim`](#znc1102-slim)
-	[`znc:latest`](#znclatest)
-	[`znc:slim`](#zncslim)

## `znc:1.10`

```console
$ docker pull znc@sha256:e0501a44a45a625c4255f1470cbd57436c03a9592a3f6668278a0fdfe43bf8c5
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
$ docker pull znc@sha256:d0185bcd671a3ff2f41f573e051d91cc17145d7b688a0231859c584a2a6dd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183058364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e69d8e47bb3b0f91df95c3f9bc0add834847b60807e21221fcabe8eb9700444`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 17:52:54 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 08 May 2026 17:52:54 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 08 May 2026 17:52:54 GMT
ARG MAKEFLAGS=
# Fri, 08 May 2026 17:52:54 GMT
ENV ZNC_VERSION=1.10.2
# Fri, 08 May 2026 17:52:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 08 May 2026 17:52:55 GMT
COPY entrypoint.sh / # buildkit
# Fri, 08 May 2026 17:52:55 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 08 May 2026 17:52:55 GMT
VOLUME [/znc-data]
# Fri, 08 May 2026 17:52:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 18:08:20 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 08 May 2026 18:08:20 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17805908309b550cb5b33fa259d5e8743e60de1e7d22cb62f94f05ee8d4d315e`  
		Last Modified: Fri, 08 May 2026 17:53:05 GMT  
		Size: 46.2 MB (46177432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ac3f0e0e00e6145a3ec8b7c30f78865b198c1590a72f91c4fbc083842a81e8`  
		Last Modified: Fri, 08 May 2026 17:53:03 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df7e007158cef5cd805aebfaf84202e6fb63bec5082548efffb95e19d66ad0a`  
		Last Modified: Fri, 08 May 2026 17:53:03 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bb52af13636ab9a4b57ea6ce8e6958fbb62a7d1217062889eaddcc22cd326a`  
		Last Modified: Fri, 08 May 2026 18:08:46 GMT  
		Size: 133.0 MB (133015493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdcee6f9ad7a281591b87a322f52c42e9557e9530b5ddb27312701f6f67859e`  
		Last Modified: Fri, 08 May 2026 18:08:43 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:9e241f6ccc7973225022b544df516b552aeedf6c219705d24f2c31a53d0f0c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7031418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de02932181cd90ffbcb7f6a6deed7821b193ef91147871c12f8a89c14326c57`

```dockerfile
```

-	Layers:
	-	`sha256:b25530675a42720fc04635173036271ad22b9a172d86815d6ebb67cba43665a7`  
		Last Modified: Fri, 08 May 2026 18:08:44 GMT  
		Size: 7.0 MB (7021858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacb5afe5e3f6b0cfe5e678c6e80cac6f23a8fec3822ebe644c0d18a348b9307`  
		Last Modified: Fri, 08 May 2026 18:08:43 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm variant v6

```console
$ docker pull znc@sha256:15fb7ec3fd0644f8e43190c78d60d5983d8503a7958292f448956465d239dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (154999023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeb94e7bc6835683af334cd57dd768c80f2927f8d22ba6fc66e13c627fb5188`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 17:56:51 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 08 May 2026 17:56:51 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 08 May 2026 17:56:51 GMT
ARG MAKEFLAGS=
# Fri, 08 May 2026 17:56:51 GMT
ENV ZNC_VERSION=1.10.2
# Fri, 08 May 2026 17:56:51 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 08 May 2026 17:56:51 GMT
COPY entrypoint.sh / # buildkit
# Fri, 08 May 2026 17:56:51 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 08 May 2026 17:56:51 GMT
VOLUME [/znc-data]
# Fri, 08 May 2026 17:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 18:11:13 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 08 May 2026 18:11:13 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e185a19efcb8cb8ac9bbab8dac4e35d584467251e7cacf69456c3adcc5b7f82`  
		Last Modified: Fri, 08 May 2026 17:56:59 GMT  
		Size: 44.8 MB (44826756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340a3457742c6ccf9171147453dc1a8572ba186e343b41a662009f7d45a91c82`  
		Last Modified: Fri, 08 May 2026 17:56:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f2a8d3602de6a737f19f2866f149adb1bf6feec3485e36e117693cc6725a88`  
		Last Modified: Fri, 08 May 2026 17:56:58 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5851237d0d683192021b1a084769a0d734373e19b8c8d7b4f84031b0c4cf55`  
		Last Modified: Fri, 08 May 2026 18:11:31 GMT  
		Size: 106.6 MB (106599149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54ca204d7bb74049d2f2717c7bbf921391772fbc90e21d33cec0830893508db`  
		Last Modified: Fri, 08 May 2026 18:11:27 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:a3ecc9f2385cab5b2f8e9351678e8a3b2751e8a8fcaf8cf36faff01795eac732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb1a1d28d149bcab3525e13cfc61df7058dc9e14969f2563a627b42442a5db4`

```dockerfile
```

-	Layers:
	-	`sha256:9b2bf0cf0b7d3948fbb74274a393ac84cf7bbf9586fb6a2d24f1c091c2ba336d`  
		Last Modified: Fri, 08 May 2026 18:11:27 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:4454be961baf35e2372cea7101bf584f68d8934c912e15d3ef1585f61e0cdc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171291321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a645479417d5e877904ebe24d095554e0160d5804314a85f108196ed0f264f87`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 17:54:08 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 08 May 2026 17:54:08 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 08 May 2026 17:54:08 GMT
ARG MAKEFLAGS=
# Fri, 08 May 2026 17:54:08 GMT
ENV ZNC_VERSION=1.10.2
# Fri, 08 May 2026 17:54:08 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 08 May 2026 17:54:08 GMT
COPY entrypoint.sh / # buildkit
# Fri, 08 May 2026 17:54:08 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 08 May 2026 17:54:08 GMT
VOLUME [/znc-data]
# Fri, 08 May 2026 17:54:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 18:07:58 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 08 May 2026 18:07:58 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5d93bc98de2c8d20fc082f7f0af39e8aeb190ea5399a3727d08ce83da078b5`  
		Last Modified: Fri, 08 May 2026 17:54:19 GMT  
		Size: 46.0 MB (46009004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab837d60f9621cc216b9fe7349e94d4f97c0e529e86539df4b31a663d853e96`  
		Last Modified: Fri, 08 May 2026 17:54:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e2453729d56153e081ca202babc85c94339529c8816da0726e3be1e11130a8`  
		Last Modified: Fri, 08 May 2026 17:54:18 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606da9e79dd48f454621595dd474ea9ccd734048d6af823c69e7627870100e6`  
		Last Modified: Fri, 08 May 2026 18:08:21 GMT  
		Size: 121.1 MB (121081195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d62e710aef8f5781fe2bb4ffcae55862c19910c760f93c8a2fd58def6c6903`  
		Last Modified: Fri, 08 May 2026 18:08:18 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:19418dc3d0caa753d2ead3952176fa308a198f5461228486f5cdc9c191e0eef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7090619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee44e8082dfe87a22ee9eebed3d1c50ce8c7419841f7a0d1a82780a4fc6bb099`

```dockerfile
```

-	Layers:
	-	`sha256:92f584396bfff848b7613cf14d2f5f2823d20dba32a2e4c065758bff4c619900`  
		Last Modified: Fri, 08 May 2026 18:08:18 GMT  
		Size: 7.1 MB (7080967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6949b506e180b6b88cc3b9a403ae6f4a5576ddb259aa19870c3f65c6e03aea`  
		Last Modified: Fri, 08 May 2026 18:08:18 GMT  
		Size: 9.7 KB (9652 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10-slim`

```console
$ docker pull znc@sha256:629b2a4d29724a4f2242384cf964e1afd06117f0ead9703a9353b20211899b3e
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
$ docker pull znc@sha256:96c1f6162c5e952a2f7b174c140853df39f2323f08bd2e2b1ef276d1e6df34cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49968300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada1451e1c9b62cf36a17f5c926ec3035b042d249935ee0fed977fbc4380a7f7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Sun, 28 Jun 2026 07:49:56 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sun, 28 Jun 2026 07:49:56 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Sun, 28 Jun 2026 07:49:56 GMT
ARG MAKEFLAGS=
# Sun, 28 Jun 2026 07:49:56 GMT
ENV ZNC_VERSION=1.10.2
# Sun, 28 Jun 2026 07:49:56 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Sun, 28 Jun 2026 07:49:56 GMT
COPY entrypoint.sh / # buildkit
# Sun, 28 Jun 2026 07:49:56 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Sun, 28 Jun 2026 07:49:56 GMT
VOLUME [/znc-data]
# Sun, 28 Jun 2026 07:49:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddcebdc4749f0a7b2c3471d989f2bedc63c01e97da6c9734bbaea38bf5a3979`  
		Last Modified: Sun, 28 Jun 2026 07:50:07 GMT  
		Size: 46.1 MB (46122960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f493c752bf74a5824be29ccbc850c8e9a72bca51b11108eb2b3264070fca5`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad35b5dc67bec3f97ea5e199cb448ad4c4f4bf56924c25da7568402ca844b329`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:c99c31291200376df6d78b31d514d42f341c58884d088f220adf5fc2d95c81ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1747898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0eec12dc62ee581c4d4c59312537db71bb35ec636659af222548c5363d882ab`

```dockerfile
```

-	Layers:
	-	`sha256:500259fd3e286bd3b0f58e1e1b05c2afb286481bc830e2d9f8bb62bf33fa7ece`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 1.7 MB (1733910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d25b2f4146df5bcf4b014a8809634d21cc93234c322c6de724737124e349a1f`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:beb58fb0e7539ede17017f44fe126c7e0af6afe4ee4cd2594e6c0e140f6ad879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48344651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9fc2a3164aa172017a7f49ad0c9e5c248f06a2b2cb854cbfed7185b19ef966`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Sun, 28 Jun 2026 07:10:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sun, 28 Jun 2026 07:10:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Sun, 28 Jun 2026 07:10:07 GMT
ARG MAKEFLAGS=
# Sun, 28 Jun 2026 07:10:07 GMT
ENV ZNC_VERSION=1.10.2
# Sun, 28 Jun 2026 07:10:07 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Sun, 28 Jun 2026 07:10:07 GMT
COPY entrypoint.sh / # buildkit
# Sun, 28 Jun 2026 07:10:07 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Sun, 28 Jun 2026 07:10:07 GMT
VOLUME [/znc-data]
# Sun, 28 Jun 2026 07:10:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e924c376684e8be7deffac361742cbbb2b367aaa41f9e38ca53979c17de87`  
		Last Modified: Sun, 28 Jun 2026 07:10:16 GMT  
		Size: 44.8 MB (44791136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db69c3368821c424ac308b3f34806b42a5c66b8d75c95a6fe5f22642e7ba0a`  
		Last Modified: Sun, 28 Jun 2026 07:10:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eadd5795ba58edf0de21641f21be1aebfdcc90a50bb9674c3a04f2d25a2d7d`  
		Last Modified: Sun, 28 Jun 2026 07:10:15 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:0a7f3b9730c0470a6e09ddf3f883d20f1705c5ea94cbc47c475c91acf2e6da68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75ad6bdd0bd3e5f0553041ffb2f1e0eadad6d1b63c3e18480843a2352e584c`

```dockerfile
```

-	Layers:
	-	`sha256:861ce414ba379051c72b0da3c8ab827e7cedaca1017c8a094f5ddd5bb938d7b9`  
		Last Modified: Sun, 28 Jun 2026 07:10:14 GMT  
		Size: 13.8 KB (13845 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:31dca0347f93557f044433142b8a1083bf592a839cae59a59b22794842fee94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50145128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cea40b803a6827d16049d3d16ff2b4f17b630d4959b615cead71722ddfdad95`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Sun, 28 Jun 2026 07:55:26 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sun, 28 Jun 2026 07:55:26 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Sun, 28 Jun 2026 07:55:26 GMT
ARG MAKEFLAGS=
# Sun, 28 Jun 2026 07:55:26 GMT
ENV ZNC_VERSION=1.10.2
# Sun, 28 Jun 2026 07:55:26 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Sun, 28 Jun 2026 07:55:26 GMT
COPY entrypoint.sh / # buildkit
# Sun, 28 Jun 2026 07:55:26 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Sun, 28 Jun 2026 07:55:26 GMT
VOLUME [/znc-data]
# Sun, 28 Jun 2026 07:55:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f184a343cbd6cf95d9ff42c670491aad6613b6891867807484311745e4831b4d`  
		Last Modified: Sun, 28 Jun 2026 07:55:38 GMT  
		Size: 46.0 MB (45962348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecea1ca60db324cf4369ffaa608e7dc21266172afa880c42245e19f8eb5aade`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a5693988ba771425ae78d0aa341b8ca2b62fe78171854fea6cb56862d324a`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:5172e817f09637e0d17ddfd4704a50215ba7bd37cf0b9100eb7c04aa96d1c6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1747470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5e52b77829f3ded0836d52ead9634ef4b0145f5b8e34eec9f49041bbf9f3be`

```dockerfile
```

-	Layers:
	-	`sha256:a8373bc4f446c7c8a247045bffeda76e5d69f321c9e02cbab3cf3e7af46a7075`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 1.7 MB (1733390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7662719e148d59545457f677a88fb4b0a97dc2c64214582226f69eabf5047297`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.2`

```console
$ docker pull znc@sha256:e0501a44a45a625c4255f1470cbd57436c03a9592a3f6668278a0fdfe43bf8c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10.2` - linux; amd64

```console
$ docker pull znc@sha256:d0185bcd671a3ff2f41f573e051d91cc17145d7b688a0231859c584a2a6dd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183058364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e69d8e47bb3b0f91df95c3f9bc0add834847b60807e21221fcabe8eb9700444`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 17:52:54 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 08 May 2026 17:52:54 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 08 May 2026 17:52:54 GMT
ARG MAKEFLAGS=
# Fri, 08 May 2026 17:52:54 GMT
ENV ZNC_VERSION=1.10.2
# Fri, 08 May 2026 17:52:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 08 May 2026 17:52:55 GMT
COPY entrypoint.sh / # buildkit
# Fri, 08 May 2026 17:52:55 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 08 May 2026 17:52:55 GMT
VOLUME [/znc-data]
# Fri, 08 May 2026 17:52:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 18:08:20 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 08 May 2026 18:08:20 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17805908309b550cb5b33fa259d5e8743e60de1e7d22cb62f94f05ee8d4d315e`  
		Last Modified: Fri, 08 May 2026 17:53:05 GMT  
		Size: 46.2 MB (46177432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ac3f0e0e00e6145a3ec8b7c30f78865b198c1590a72f91c4fbc083842a81e8`  
		Last Modified: Fri, 08 May 2026 17:53:03 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df7e007158cef5cd805aebfaf84202e6fb63bec5082548efffb95e19d66ad0a`  
		Last Modified: Fri, 08 May 2026 17:53:03 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bb52af13636ab9a4b57ea6ce8e6958fbb62a7d1217062889eaddcc22cd326a`  
		Last Modified: Fri, 08 May 2026 18:08:46 GMT  
		Size: 133.0 MB (133015493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdcee6f9ad7a281591b87a322f52c42e9557e9530b5ddb27312701f6f67859e`  
		Last Modified: Fri, 08 May 2026 18:08:43 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.2` - unknown; unknown

```console
$ docker pull znc@sha256:9e241f6ccc7973225022b544df516b552aeedf6c219705d24f2c31a53d0f0c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7031418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de02932181cd90ffbcb7f6a6deed7821b193ef91147871c12f8a89c14326c57`

```dockerfile
```

-	Layers:
	-	`sha256:b25530675a42720fc04635173036271ad22b9a172d86815d6ebb67cba43665a7`  
		Last Modified: Fri, 08 May 2026 18:08:44 GMT  
		Size: 7.0 MB (7021858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacb5afe5e3f6b0cfe5e678c6e80cac6f23a8fec3822ebe644c0d18a348b9307`  
		Last Modified: Fri, 08 May 2026 18:08:43 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.2` - linux; arm variant v6

```console
$ docker pull znc@sha256:15fb7ec3fd0644f8e43190c78d60d5983d8503a7958292f448956465d239dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (154999023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeb94e7bc6835683af334cd57dd768c80f2927f8d22ba6fc66e13c627fb5188`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 17:56:51 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 08 May 2026 17:56:51 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 08 May 2026 17:56:51 GMT
ARG MAKEFLAGS=
# Fri, 08 May 2026 17:56:51 GMT
ENV ZNC_VERSION=1.10.2
# Fri, 08 May 2026 17:56:51 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 08 May 2026 17:56:51 GMT
COPY entrypoint.sh / # buildkit
# Fri, 08 May 2026 17:56:51 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 08 May 2026 17:56:51 GMT
VOLUME [/znc-data]
# Fri, 08 May 2026 17:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 18:11:13 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 08 May 2026 18:11:13 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e185a19efcb8cb8ac9bbab8dac4e35d584467251e7cacf69456c3adcc5b7f82`  
		Last Modified: Fri, 08 May 2026 17:56:59 GMT  
		Size: 44.8 MB (44826756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340a3457742c6ccf9171147453dc1a8572ba186e343b41a662009f7d45a91c82`  
		Last Modified: Fri, 08 May 2026 17:56:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f2a8d3602de6a737f19f2866f149adb1bf6feec3485e36e117693cc6725a88`  
		Last Modified: Fri, 08 May 2026 17:56:58 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5851237d0d683192021b1a084769a0d734373e19b8c8d7b4f84031b0c4cf55`  
		Last Modified: Fri, 08 May 2026 18:11:31 GMT  
		Size: 106.6 MB (106599149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54ca204d7bb74049d2f2717c7bbf921391772fbc90e21d33cec0830893508db`  
		Last Modified: Fri, 08 May 2026 18:11:27 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.2` - unknown; unknown

```console
$ docker pull znc@sha256:a3ecc9f2385cab5b2f8e9351678e8a3b2751e8a8fcaf8cf36faff01795eac732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb1a1d28d149bcab3525e13cfc61df7058dc9e14969f2563a627b42442a5db4`

```dockerfile
```

-	Layers:
	-	`sha256:9b2bf0cf0b7d3948fbb74274a393ac84cf7bbf9586fb6a2d24f1c091c2ba336d`  
		Last Modified: Fri, 08 May 2026 18:11:27 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.2` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:4454be961baf35e2372cea7101bf584f68d8934c912e15d3ef1585f61e0cdc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171291321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a645479417d5e877904ebe24d095554e0160d5804314a85f108196ed0f264f87`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 17:54:08 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 08 May 2026 17:54:08 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 08 May 2026 17:54:08 GMT
ARG MAKEFLAGS=
# Fri, 08 May 2026 17:54:08 GMT
ENV ZNC_VERSION=1.10.2
# Fri, 08 May 2026 17:54:08 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 08 May 2026 17:54:08 GMT
COPY entrypoint.sh / # buildkit
# Fri, 08 May 2026 17:54:08 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 08 May 2026 17:54:08 GMT
VOLUME [/znc-data]
# Fri, 08 May 2026 17:54:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 18:07:58 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 08 May 2026 18:07:58 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5d93bc98de2c8d20fc082f7f0af39e8aeb190ea5399a3727d08ce83da078b5`  
		Last Modified: Fri, 08 May 2026 17:54:19 GMT  
		Size: 46.0 MB (46009004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab837d60f9621cc216b9fe7349e94d4f97c0e529e86539df4b31a663d853e96`  
		Last Modified: Fri, 08 May 2026 17:54:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e2453729d56153e081ca202babc85c94339529c8816da0726e3be1e11130a8`  
		Last Modified: Fri, 08 May 2026 17:54:18 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606da9e79dd48f454621595dd474ea9ccd734048d6af823c69e7627870100e6`  
		Last Modified: Fri, 08 May 2026 18:08:21 GMT  
		Size: 121.1 MB (121081195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d62e710aef8f5781fe2bb4ffcae55862c19910c760f93c8a2fd58def6c6903`  
		Last Modified: Fri, 08 May 2026 18:08:18 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.2` - unknown; unknown

```console
$ docker pull znc@sha256:19418dc3d0caa753d2ead3952176fa308a198f5461228486f5cdc9c191e0eef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7090619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee44e8082dfe87a22ee9eebed3d1c50ce8c7419841f7a0d1a82780a4fc6bb099`

```dockerfile
```

-	Layers:
	-	`sha256:92f584396bfff848b7613cf14d2f5f2823d20dba32a2e4c065758bff4c619900`  
		Last Modified: Fri, 08 May 2026 18:08:18 GMT  
		Size: 7.1 MB (7080967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6949b506e180b6b88cc3b9a403ae6f4a5576ddb259aa19870c3f65c6e03aea`  
		Last Modified: Fri, 08 May 2026 18:08:18 GMT  
		Size: 9.7 KB (9652 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.2-slim`

```console
$ docker pull znc@sha256:629b2a4d29724a4f2242384cf964e1afd06117f0ead9703a9353b20211899b3e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `znc:1.10.2-slim` - linux; amd64

```console
$ docker pull znc@sha256:96c1f6162c5e952a2f7b174c140853df39f2323f08bd2e2b1ef276d1e6df34cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49968300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada1451e1c9b62cf36a17f5c926ec3035b042d249935ee0fed977fbc4380a7f7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Sun, 28 Jun 2026 07:49:56 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sun, 28 Jun 2026 07:49:56 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Sun, 28 Jun 2026 07:49:56 GMT
ARG MAKEFLAGS=
# Sun, 28 Jun 2026 07:49:56 GMT
ENV ZNC_VERSION=1.10.2
# Sun, 28 Jun 2026 07:49:56 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Sun, 28 Jun 2026 07:49:56 GMT
COPY entrypoint.sh / # buildkit
# Sun, 28 Jun 2026 07:49:56 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Sun, 28 Jun 2026 07:49:56 GMT
VOLUME [/znc-data]
# Sun, 28 Jun 2026 07:49:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddcebdc4749f0a7b2c3471d989f2bedc63c01e97da6c9734bbaea38bf5a3979`  
		Last Modified: Sun, 28 Jun 2026 07:50:07 GMT  
		Size: 46.1 MB (46122960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f493c752bf74a5824be29ccbc850c8e9a72bca51b11108eb2b3264070fca5`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad35b5dc67bec3f97ea5e199cb448ad4c4f4bf56924c25da7568402ca844b329`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.2-slim` - unknown; unknown

```console
$ docker pull znc@sha256:c99c31291200376df6d78b31d514d42f341c58884d088f220adf5fc2d95c81ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1747898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0eec12dc62ee581c4d4c59312537db71bb35ec636659af222548c5363d882ab`

```dockerfile
```

-	Layers:
	-	`sha256:500259fd3e286bd3b0f58e1e1b05c2afb286481bc830e2d9f8bb62bf33fa7ece`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 1.7 MB (1733910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d25b2f4146df5bcf4b014a8809634d21cc93234c322c6de724737124e349a1f`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.2-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:beb58fb0e7539ede17017f44fe126c7e0af6afe4ee4cd2594e6c0e140f6ad879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48344651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9fc2a3164aa172017a7f49ad0c9e5c248f06a2b2cb854cbfed7185b19ef966`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Sun, 28 Jun 2026 07:10:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sun, 28 Jun 2026 07:10:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Sun, 28 Jun 2026 07:10:07 GMT
ARG MAKEFLAGS=
# Sun, 28 Jun 2026 07:10:07 GMT
ENV ZNC_VERSION=1.10.2
# Sun, 28 Jun 2026 07:10:07 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Sun, 28 Jun 2026 07:10:07 GMT
COPY entrypoint.sh / # buildkit
# Sun, 28 Jun 2026 07:10:07 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Sun, 28 Jun 2026 07:10:07 GMT
VOLUME [/znc-data]
# Sun, 28 Jun 2026 07:10:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e924c376684e8be7deffac361742cbbb2b367aaa41f9e38ca53979c17de87`  
		Last Modified: Sun, 28 Jun 2026 07:10:16 GMT  
		Size: 44.8 MB (44791136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db69c3368821c424ac308b3f34806b42a5c66b8d75c95a6fe5f22642e7ba0a`  
		Last Modified: Sun, 28 Jun 2026 07:10:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eadd5795ba58edf0de21641f21be1aebfdcc90a50bb9674c3a04f2d25a2d7d`  
		Last Modified: Sun, 28 Jun 2026 07:10:15 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.2-slim` - unknown; unknown

```console
$ docker pull znc@sha256:0a7f3b9730c0470a6e09ddf3f883d20f1705c5ea94cbc47c475c91acf2e6da68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75ad6bdd0bd3e5f0553041ffb2f1e0eadad6d1b63c3e18480843a2352e584c`

```dockerfile
```

-	Layers:
	-	`sha256:861ce414ba379051c72b0da3c8ab827e7cedaca1017c8a094f5ddd5bb938d7b9`  
		Last Modified: Sun, 28 Jun 2026 07:10:14 GMT  
		Size: 13.8 KB (13845 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.2-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:31dca0347f93557f044433142b8a1083bf592a839cae59a59b22794842fee94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50145128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cea40b803a6827d16049d3d16ff2b4f17b630d4959b615cead71722ddfdad95`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Sun, 28 Jun 2026 07:55:26 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sun, 28 Jun 2026 07:55:26 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Sun, 28 Jun 2026 07:55:26 GMT
ARG MAKEFLAGS=
# Sun, 28 Jun 2026 07:55:26 GMT
ENV ZNC_VERSION=1.10.2
# Sun, 28 Jun 2026 07:55:26 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Sun, 28 Jun 2026 07:55:26 GMT
COPY entrypoint.sh / # buildkit
# Sun, 28 Jun 2026 07:55:26 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Sun, 28 Jun 2026 07:55:26 GMT
VOLUME [/znc-data]
# Sun, 28 Jun 2026 07:55:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f184a343cbd6cf95d9ff42c670491aad6613b6891867807484311745e4831b4d`  
		Last Modified: Sun, 28 Jun 2026 07:55:38 GMT  
		Size: 46.0 MB (45962348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecea1ca60db324cf4369ffaa608e7dc21266172afa880c42245e19f8eb5aade`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a5693988ba771425ae78d0aa341b8ca2b62fe78171854fea6cb56862d324a`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.2-slim` - unknown; unknown

```console
$ docker pull znc@sha256:5172e817f09637e0d17ddfd4704a50215ba7bd37cf0b9100eb7c04aa96d1c6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1747470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5e52b77829f3ded0836d52ead9634ef4b0145f5b8e34eec9f49041bbf9f3be`

```dockerfile
```

-	Layers:
	-	`sha256:a8373bc4f446c7c8a247045bffeda76e5d69f321c9e02cbab3cf3e7af46a7075`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 1.7 MB (1733390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7662719e148d59545457f677a88fb4b0a97dc2c64214582226f69eabf5047297`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:latest`

```console
$ docker pull znc@sha256:e0501a44a45a625c4255f1470cbd57436c03a9592a3f6668278a0fdfe43bf8c5
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
$ docker pull znc@sha256:d0185bcd671a3ff2f41f573e051d91cc17145d7b688a0231859c584a2a6dd88e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **183.1 MB (183058364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e69d8e47bb3b0f91df95c3f9bc0add834847b60807e21221fcabe8eb9700444`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 17:52:54 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 08 May 2026 17:52:54 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 08 May 2026 17:52:54 GMT
ARG MAKEFLAGS=
# Fri, 08 May 2026 17:52:54 GMT
ENV ZNC_VERSION=1.10.2
# Fri, 08 May 2026 17:52:54 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 08 May 2026 17:52:55 GMT
COPY entrypoint.sh / # buildkit
# Fri, 08 May 2026 17:52:55 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 08 May 2026 17:52:55 GMT
VOLUME [/znc-data]
# Fri, 08 May 2026 17:52:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 18:08:20 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 08 May 2026 18:08:20 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17805908309b550cb5b33fa259d5e8743e60de1e7d22cb62f94f05ee8d4d315e`  
		Last Modified: Fri, 08 May 2026 17:53:05 GMT  
		Size: 46.2 MB (46177432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2ac3f0e0e00e6145a3ec8b7c30f78865b198c1590a72f91c4fbc083842a81e8`  
		Last Modified: Fri, 08 May 2026 17:53:03 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df7e007158cef5cd805aebfaf84202e6fb63bec5082548efffb95e19d66ad0a`  
		Last Modified: Fri, 08 May 2026 17:53:03 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2bb52af13636ab9a4b57ea6ce8e6958fbb62a7d1217062889eaddcc22cd326a`  
		Last Modified: Fri, 08 May 2026 18:08:46 GMT  
		Size: 133.0 MB (133015493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdcee6f9ad7a281591b87a322f52c42e9557e9530b5ddb27312701f6f67859e`  
		Last Modified: Fri, 08 May 2026 18:08:43 GMT  
		Size: 329.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:9e241f6ccc7973225022b544df516b552aeedf6c219705d24f2c31a53d0f0c8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (7031418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de02932181cd90ffbcb7f6a6deed7821b193ef91147871c12f8a89c14326c57`

```dockerfile
```

-	Layers:
	-	`sha256:b25530675a42720fc04635173036271ad22b9a172d86815d6ebb67cba43665a7`  
		Last Modified: Fri, 08 May 2026 18:08:44 GMT  
		Size: 7.0 MB (7021858 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dacb5afe5e3f6b0cfe5e678c6e80cac6f23a8fec3822ebe644c0d18a348b9307`  
		Last Modified: Fri, 08 May 2026 18:08:43 GMT  
		Size: 9.6 KB (9560 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:15fb7ec3fd0644f8e43190c78d60d5983d8503a7958292f448956465d239dd05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.0 MB (154999023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aeb94e7bc6835683af334cd57dd768c80f2927f8d22ba6fc66e13c627fb5188`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 17:56:51 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 08 May 2026 17:56:51 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 08 May 2026 17:56:51 GMT
ARG MAKEFLAGS=
# Fri, 08 May 2026 17:56:51 GMT
ENV ZNC_VERSION=1.10.2
# Fri, 08 May 2026 17:56:51 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 08 May 2026 17:56:51 GMT
COPY entrypoint.sh / # buildkit
# Fri, 08 May 2026 17:56:51 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 08 May 2026 17:56:51 GMT
VOLUME [/znc-data]
# Fri, 08 May 2026 17:56:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 18:11:13 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 08 May 2026 18:11:13 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e185a19efcb8cb8ac9bbab8dac4e35d584467251e7cacf69456c3adcc5b7f82`  
		Last Modified: Fri, 08 May 2026 17:56:59 GMT  
		Size: 44.8 MB (44826756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340a3457742c6ccf9171147453dc1a8572ba186e343b41a662009f7d45a91c82`  
		Last Modified: Fri, 08 May 2026 17:56:58 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1f2a8d3602de6a737f19f2866f149adb1bf6feec3485e36e117693cc6725a88`  
		Last Modified: Fri, 08 May 2026 17:56:58 GMT  
		Size: 751.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5851237d0d683192021b1a084769a0d734373e19b8c8d7b4f84031b0c4cf55`  
		Last Modified: Fri, 08 May 2026 18:11:31 GMT  
		Size: 106.6 MB (106599149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54ca204d7bb74049d2f2717c7bbf921391772fbc90e21d33cec0830893508db`  
		Last Modified: Fri, 08 May 2026 18:11:27 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:a3ecc9f2385cab5b2f8e9351678e8a3b2751e8a8fcaf8cf36faff01795eac732
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb1a1d28d149bcab3525e13cfc61df7058dc9e14969f2563a627b42442a5db4`

```dockerfile
```

-	Layers:
	-	`sha256:9b2bf0cf0b7d3948fbb74274a393ac84cf7bbf9586fb6a2d24f1c091c2ba336d`  
		Last Modified: Fri, 08 May 2026 18:11:27 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:4454be961baf35e2372cea7101bf584f68d8934c912e15d3ef1585f61e0cdc88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **171.3 MB (171291321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a645479417d5e877904ebe24d095554e0160d5804314a85f108196ed0f264f87`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 17:54:08 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 08 May 2026 17:54:08 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 08 May 2026 17:54:08 GMT
ARG MAKEFLAGS=
# Fri, 08 May 2026 17:54:08 GMT
ENV ZNC_VERSION=1.10.2
# Fri, 08 May 2026 17:54:08 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Fri, 08 May 2026 17:54:08 GMT
COPY entrypoint.sh / # buildkit
# Fri, 08 May 2026 17:54:08 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Fri, 08 May 2026 17:54:08 GMT
VOLUME [/znc-data]
# Fri, 08 May 2026 17:54:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 08 May 2026 18:07:58 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3 # buildkit
# Fri, 08 May 2026 18:07:58 GMT
COPY 30-build-modules.sh /startup-sequence/ # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5d93bc98de2c8d20fc082f7f0af39e8aeb190ea5399a3727d08ce83da078b5`  
		Last Modified: Fri, 08 May 2026 17:54:19 GMT  
		Size: 46.0 MB (46009004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ab837d60f9621cc216b9fe7349e94d4f97c0e529e86539df4b31a663d853e96`  
		Last Modified: Fri, 08 May 2026 17:54:18 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e2453729d56153e081ca202babc85c94339529c8816da0726e3be1e11130a8`  
		Last Modified: Fri, 08 May 2026 17:54:18 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606da9e79dd48f454621595dd474ea9ccd734048d6af823c69e7627870100e6`  
		Last Modified: Fri, 08 May 2026 18:08:21 GMT  
		Size: 121.1 MB (121081195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d62e710aef8f5781fe2bb4ffcae55862c19910c760f93c8a2fd58def6c6903`  
		Last Modified: Fri, 08 May 2026 18:08:18 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:19418dc3d0caa753d2ead3952176fa308a198f5461228486f5cdc9c191e0eef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7090619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee44e8082dfe87a22ee9eebed3d1c50ce8c7419841f7a0d1a82780a4fc6bb099`

```dockerfile
```

-	Layers:
	-	`sha256:92f584396bfff848b7613cf14d2f5f2823d20dba32a2e4c065758bff4c619900`  
		Last Modified: Fri, 08 May 2026 18:08:18 GMT  
		Size: 7.1 MB (7080967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca6949b506e180b6b88cc3b9a403ae6f4a5576ddb259aa19870c3f65c6e03aea`  
		Last Modified: Fri, 08 May 2026 18:08:18 GMT  
		Size: 9.7 KB (9652 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:slim`

```console
$ docker pull znc@sha256:629b2a4d29724a4f2242384cf964e1afd06117f0ead9703a9353b20211899b3e
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
$ docker pull znc@sha256:96c1f6162c5e952a2f7b174c140853df39f2323f08bd2e2b1ef276d1e6df34cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49968300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ada1451e1c9b62cf36a17f5c926ec3035b042d249935ee0fed977fbc4380a7f7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Sun, 28 Jun 2026 07:49:56 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sun, 28 Jun 2026 07:49:56 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Sun, 28 Jun 2026 07:49:56 GMT
ARG MAKEFLAGS=
# Sun, 28 Jun 2026 07:49:56 GMT
ENV ZNC_VERSION=1.10.2
# Sun, 28 Jun 2026 07:49:56 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Sun, 28 Jun 2026 07:49:56 GMT
COPY entrypoint.sh / # buildkit
# Sun, 28 Jun 2026 07:49:56 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Sun, 28 Jun 2026 07:49:56 GMT
VOLUME [/znc-data]
# Sun, 28 Jun 2026 07:49:56 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dddcebdc4749f0a7b2c3471d989f2bedc63c01e97da6c9734bbaea38bf5a3979`  
		Last Modified: Sun, 28 Jun 2026 07:50:07 GMT  
		Size: 46.1 MB (46122960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e15f493c752bf74a5824be29ccbc850c8e9a72bca51b11108eb2b3264070fca5`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad35b5dc67bec3f97ea5e199cb448ad4c4f4bf56924c25da7568402ca844b329`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:c99c31291200376df6d78b31d514d42f341c58884d088f220adf5fc2d95c81ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1747898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0eec12dc62ee581c4d4c59312537db71bb35ec636659af222548c5363d882ab`

```dockerfile
```

-	Layers:
	-	`sha256:500259fd3e286bd3b0f58e1e1b05c2afb286481bc830e2d9f8bb62bf33fa7ece`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 1.7 MB (1733910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d25b2f4146df5bcf4b014a8809634d21cc93234c322c6de724737124e349a1f`  
		Last Modified: Sun, 28 Jun 2026 07:50:06 GMT  
		Size: 14.0 KB (13988 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:beb58fb0e7539ede17017f44fe126c7e0af6afe4ee4cd2594e6c0e140f6ad879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48344651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f9fc2a3164aa172017a7f49ad0c9e5c248f06a2b2cb854cbfed7185b19ef966`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.23.5-armhf.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Sun, 28 Jun 2026 07:10:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sun, 28 Jun 2026 07:10:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Sun, 28 Jun 2026 07:10:07 GMT
ARG MAKEFLAGS=
# Sun, 28 Jun 2026 07:10:07 GMT
ENV ZNC_VERSION=1.10.2
# Sun, 28 Jun 2026 07:10:07 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Sun, 28 Jun 2026 07:10:07 GMT
COPY entrypoint.sh / # buildkit
# Sun, 28 Jun 2026 07:10:07 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Sun, 28 Jun 2026 07:10:07 GMT
VOLUME [/znc-data]
# Sun, 28 Jun 2026 07:10:07 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:e10b64a07fc8ab4702bfbad629edb6572f190358cdb4b2b7392040bdef454c0f`  
		Last Modified: Mon, 22 Jun 2026 19:20:25 GMT  
		Size: 3.6 MB (3552595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2e924c376684e8be7deffac361742cbbb2b367aaa41f9e38ca53979c17de87`  
		Last Modified: Sun, 28 Jun 2026 07:10:16 GMT  
		Size: 44.8 MB (44791136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0db69c3368821c424ac308b3f34806b42a5c66b8d75c95a6fe5f22642e7ba0a`  
		Last Modified: Sun, 28 Jun 2026 07:10:14 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01eadd5795ba58edf0de21641f21be1aebfdcc90a50bb9674c3a04f2d25a2d7d`  
		Last Modified: Sun, 28 Jun 2026 07:10:15 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:0a7f3b9730c0470a6e09ddf3f883d20f1705c5ea94cbc47c475c91acf2e6da68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 KB (13845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d75ad6bdd0bd3e5f0553041ffb2f1e0eadad6d1b63c3e18480843a2352e584c`

```dockerfile
```

-	Layers:
	-	`sha256:861ce414ba379051c72b0da3c8ab827e7cedaca1017c8a094f5ddd5bb938d7b9`  
		Last Modified: Sun, 28 Jun 2026 07:10:14 GMT  
		Size: 13.8 KB (13845 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:31dca0347f93557f044433142b8a1083bf592a839cae59a59b22794842fee94d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50145128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cea40b803a6827d16049d3d16ff2b4f17b630d4959b615cead71722ddfdad95`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Sun, 28 Jun 2026 07:55:26 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sun, 28 Jun 2026 07:55:26 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Sun, 28 Jun 2026 07:55:26 GMT
ARG MAKEFLAGS=
# Sun, 28 Jun 2026 07:55:26 GMT
ENV ZNC_VERSION=1.10.2
# Sun, 28 Jun 2026 07:55:26 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src # buildkit
# Sun, 28 Jun 2026 07:55:26 GMT
COPY entrypoint.sh / # buildkit
# Sun, 28 Jun 2026 07:55:26 GMT
COPY startup-sequence /startup-sequence/ # buildkit
# Sun, 28 Jun 2026 07:55:26 GMT
VOLUME [/znc-data]
# Sun, 28 Jun 2026 07:55:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f184a343cbd6cf95d9ff42c670491aad6613b6891867807484311745e4831b4d`  
		Last Modified: Sun, 28 Jun 2026 07:55:38 GMT  
		Size: 46.0 MB (45962348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecea1ca60db324cf4369ffaa608e7dc21266172afa880c42245e19f8eb5aade`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316a5693988ba771425ae78d0aa341b8ca2b62fe78171854fea6cb56862d324a`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:5172e817f09637e0d17ddfd4704a50215ba7bd37cf0b9100eb7c04aa96d1c6a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 MB (1747470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5e52b77829f3ded0836d52ead9634ef4b0145f5b8e34eec9f49041bbf9f3be`

```dockerfile
```

-	Layers:
	-	`sha256:a8373bc4f446c7c8a247045bffeda76e5d69f321c9e02cbab3cf3e7af46a7075`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 1.7 MB (1733390 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7662719e148d59545457f677a88fb4b0a97dc2c64214582226f69eabf5047297`  
		Last Modified: Sun, 28 Jun 2026 07:55:36 GMT  
		Size: 14.1 KB (14080 bytes)  
		MIME: application/vnd.in-toto+json
