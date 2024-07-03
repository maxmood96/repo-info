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
$ docker pull znc@sha256:58f44e7e7bfccd2a242ce9277453abe0edf2ce79a00154eb4607cb5a2e7ffecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.9` - linux; amd64

```console
$ docker pull znc@sha256:9f005c499c46cbb94860d486c14ed051390b127438c41ba6552c1b367a702a9a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160052624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09ced1c4aa8abf3507139fa9915ff24c8561a6a20e1fac4926280062b2526e4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:37:02 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:37:02 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:37:02 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:40 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:34:10 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:34:11 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:34:11 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:34:11 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:34:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:34:26 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 03 Jul 2024 16:34:27 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0689ade954ed751ec3753a47ba592aef3b27ce8108695f88ac3f65e43be4d452`  
		Last Modified: Wed, 03 Jul 2024 16:34:44 GMT  
		Size: 48.7 MB (48738318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab3a63dedf09abf22def150aa802cfb2ad85b93a8a09584da94dc88976970f5`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc64c738338fead501fe8b8945f9b751372d852c902acaab0e4b7957cd76c6`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be52d63d7334a8af0243fadd40818a46936d674c1452cd9204ae0ac4169f4901`  
		Last Modified: Wed, 03 Jul 2024 16:35:08 GMT  
		Size: 107.9 MB (107895718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a569bddc9f3d2a1bfadad4aa81df1cd6ee89d3e2962160db161530fb148bb88`  
		Last Modified: Wed, 03 Jul 2024 16:34:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.9` - linux; arm variant v6

```console
$ docker pull znc@sha256:21cfc243ee90a505ed788fe7dda5e93fa3815cb2d00f9a41abcf2c3cf69cdb43
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142114258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c111ec5813dbd30a3e7c73f6911a91d84ac15afadcd5110140fb3b253dfe05`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:00:58 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:00:58 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:00:59 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:25:06 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:29:50 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:29:51 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:29:51 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:29:51 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:29:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:30:08 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 03 Jul 2024 16:30:10 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba435b73adbcc84b885316736a834b558eb49d3eb58bdb27e67773b5e764c8f`  
		Last Modified: Wed, 03 Jul 2024 16:30:27 GMT  
		Size: 47.0 MB (47043099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960888a62058d68ecbbbf9ca99501c32e047d316bb5923d63aa028288c19a1f`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61450a00438a5dec614f819522ab4e2b3882997a3920aa57748a1014e419110`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4c80a70b183fd10e0acaa69924f82a9bad6842bf46e8d509c24fe7b30f8134`  
		Last Modified: Wed, 03 Jul 2024 16:30:56 GMT  
		Size: 91.9 MB (91895992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e6a177948d4eb7793ac5df8a7595af0991964b6485b71f8daf92d8782736d1`  
		Last Modified: Wed, 03 Jul 2024 16:30:41 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.9` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:56ee38ba5184ebbb1553f2f9169f21638494f97696e30ce890fe9c766c52ea86
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154410049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e393bdb7485d9585da6de310eefbafd5289d6611181aff4dcbde3b57a2361511`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:14:40 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 01:14:40 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 01:14:40 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:00 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:32:51 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:32:52 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:32:52 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:32:52 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:32:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:33:13 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 03 Jul 2024 16:33:15 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266b0af012afdf74d76deed54585824e29bf2f23bab214ce2ccd5f171fa03d56`  
		Last Modified: Wed, 03 Jul 2024 16:33:30 GMT  
		Size: 48.7 MB (48675511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1467b163421999dcb01504a93ab7425527ebf888cacf0e978c6a212f39acc75a`  
		Last Modified: Wed, 03 Jul 2024 16:33:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12eada70c981c5a75d135dc077f78c7b0ad72ae898619f3ffa028119391c2cf`  
		Last Modified: Wed, 03 Jul 2024 16:33:24 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aff1982f7ce645309fe933450549c80170df20971ee87c311899e229da3b3e8`  
		Last Modified: Wed, 03 Jul 2024 16:33:53 GMT  
		Size: 102.4 MB (102376079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300651a32b8a35e2dfcee22809395e151a02f49c8f795ad8b364c9a584b0221`  
		Last Modified: Wed, 03 Jul 2024 16:33:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.9-slim`

```console
$ docker pull znc@sha256:fcc741b41ce0141f61ababbabab3245b64ccd79eb1299c7ea82d4aabfccce9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.9-slim` - linux; amd64

```console
$ docker pull znc@sha256:09d49e75f77d21fbc7baead597ec7c9e7f245ee8a02d4e904572c3dbce1fe729
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52156574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888cd694179c30693c76092493d5e46cf172b060039124ab8a5530fd842bec48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:37:02 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:37:02 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:37:02 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:40 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:34:10 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:34:11 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:34:11 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:34:11 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:34:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0689ade954ed751ec3753a47ba592aef3b27ce8108695f88ac3f65e43be4d452`  
		Last Modified: Wed, 03 Jul 2024 16:34:44 GMT  
		Size: 48.7 MB (48738318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab3a63dedf09abf22def150aa802cfb2ad85b93a8a09584da94dc88976970f5`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc64c738338fead501fe8b8945f9b751372d852c902acaab0e4b7957cd76c6`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.9-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:76734439a0da077a2a0564dae08819c171163a3f43af9dc5ee95c5255d7826fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50217935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bdbf4e7b18cbe41ca369d002ed964061f8d47cf7e099529129e2c375a19d8a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:00:58 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:00:58 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:00:59 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:25:06 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:29:50 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:29:51 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:29:51 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:29:51 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:29:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba435b73adbcc84b885316736a834b558eb49d3eb58bdb27e67773b5e764c8f`  
		Last Modified: Wed, 03 Jul 2024 16:30:27 GMT  
		Size: 47.0 MB (47043099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960888a62058d68ecbbbf9ca99501c32e047d316bb5923d63aa028288c19a1f`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61450a00438a5dec614f819522ab4e2b3882997a3920aa57748a1014e419110`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.9-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:edf8589d738d479d06e748fc9fb6e69ea28869686208b0b3d380452f4f53835d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52033638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81447dab97eaecff2920bdd6ed6eda90bf798cc22fca063c1fd5ac703fd58cfc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:14:40 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 01:14:40 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 01:14:40 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:00 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:32:51 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:32:52 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:32:52 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:32:52 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:32:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266b0af012afdf74d76deed54585824e29bf2f23bab214ce2ccd5f171fa03d56`  
		Last Modified: Wed, 03 Jul 2024 16:33:30 GMT  
		Size: 48.7 MB (48675511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1467b163421999dcb01504a93ab7425527ebf888cacf0e978c6a212f39acc75a`  
		Last Modified: Wed, 03 Jul 2024 16:33:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12eada70c981c5a75d135dc077f78c7b0ad72ae898619f3ffa028119391c2cf`  
		Last Modified: Wed, 03 Jul 2024 16:33:24 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.9.1`

```console
$ docker pull znc@sha256:58f44e7e7bfccd2a242ce9277453abe0edf2ce79a00154eb4607cb5a2e7ffecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.9.1` - linux; amd64

```console
$ docker pull znc@sha256:9f005c499c46cbb94860d486c14ed051390b127438c41ba6552c1b367a702a9a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160052624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09ced1c4aa8abf3507139fa9915ff24c8561a6a20e1fac4926280062b2526e4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:37:02 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:37:02 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:37:02 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:40 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:34:10 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:34:11 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:34:11 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:34:11 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:34:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:34:26 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 03 Jul 2024 16:34:27 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0689ade954ed751ec3753a47ba592aef3b27ce8108695f88ac3f65e43be4d452`  
		Last Modified: Wed, 03 Jul 2024 16:34:44 GMT  
		Size: 48.7 MB (48738318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab3a63dedf09abf22def150aa802cfb2ad85b93a8a09584da94dc88976970f5`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc64c738338fead501fe8b8945f9b751372d852c902acaab0e4b7957cd76c6`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be52d63d7334a8af0243fadd40818a46936d674c1452cd9204ae0ac4169f4901`  
		Last Modified: Wed, 03 Jul 2024 16:35:08 GMT  
		Size: 107.9 MB (107895718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a569bddc9f3d2a1bfadad4aa81df1cd6ee89d3e2962160db161530fb148bb88`  
		Last Modified: Wed, 03 Jul 2024 16:34:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.9.1` - linux; arm variant v6

```console
$ docker pull znc@sha256:21cfc243ee90a505ed788fe7dda5e93fa3815cb2d00f9a41abcf2c3cf69cdb43
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142114258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c111ec5813dbd30a3e7c73f6911a91d84ac15afadcd5110140fb3b253dfe05`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:00:58 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:00:58 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:00:59 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:25:06 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:29:50 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:29:51 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:29:51 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:29:51 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:29:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:30:08 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 03 Jul 2024 16:30:10 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba435b73adbcc84b885316736a834b558eb49d3eb58bdb27e67773b5e764c8f`  
		Last Modified: Wed, 03 Jul 2024 16:30:27 GMT  
		Size: 47.0 MB (47043099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960888a62058d68ecbbbf9ca99501c32e047d316bb5923d63aa028288c19a1f`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61450a00438a5dec614f819522ab4e2b3882997a3920aa57748a1014e419110`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4c80a70b183fd10e0acaa69924f82a9bad6842bf46e8d509c24fe7b30f8134`  
		Last Modified: Wed, 03 Jul 2024 16:30:56 GMT  
		Size: 91.9 MB (91895992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e6a177948d4eb7793ac5df8a7595af0991964b6485b71f8daf92d8782736d1`  
		Last Modified: Wed, 03 Jul 2024 16:30:41 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.9.1` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:56ee38ba5184ebbb1553f2f9169f21638494f97696e30ce890fe9c766c52ea86
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154410049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e393bdb7485d9585da6de310eefbafd5289d6611181aff4dcbde3b57a2361511`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:14:40 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 01:14:40 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 01:14:40 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:00 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:32:51 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:32:52 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:32:52 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:32:52 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:32:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:33:13 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 03 Jul 2024 16:33:15 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266b0af012afdf74d76deed54585824e29bf2f23bab214ce2ccd5f171fa03d56`  
		Last Modified: Wed, 03 Jul 2024 16:33:30 GMT  
		Size: 48.7 MB (48675511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1467b163421999dcb01504a93ab7425527ebf888cacf0e978c6a212f39acc75a`  
		Last Modified: Wed, 03 Jul 2024 16:33:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12eada70c981c5a75d135dc077f78c7b0ad72ae898619f3ffa028119391c2cf`  
		Last Modified: Wed, 03 Jul 2024 16:33:24 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aff1982f7ce645309fe933450549c80170df20971ee87c311899e229da3b3e8`  
		Last Modified: Wed, 03 Jul 2024 16:33:53 GMT  
		Size: 102.4 MB (102376079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300651a32b8a35e2dfcee22809395e151a02f49c8f795ad8b364c9a584b0221`  
		Last Modified: Wed, 03 Jul 2024 16:33:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.9.1-slim`

```console
$ docker pull znc@sha256:fcc741b41ce0141f61ababbabab3245b64ccd79eb1299c7ea82d4aabfccce9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.9.1-slim` - linux; amd64

```console
$ docker pull znc@sha256:09d49e75f77d21fbc7baead597ec7c9e7f245ee8a02d4e904572c3dbce1fe729
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52156574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888cd694179c30693c76092493d5e46cf172b060039124ab8a5530fd842bec48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:37:02 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:37:02 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:37:02 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:40 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:34:10 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:34:11 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:34:11 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:34:11 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:34:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0689ade954ed751ec3753a47ba592aef3b27ce8108695f88ac3f65e43be4d452`  
		Last Modified: Wed, 03 Jul 2024 16:34:44 GMT  
		Size: 48.7 MB (48738318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab3a63dedf09abf22def150aa802cfb2ad85b93a8a09584da94dc88976970f5`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc64c738338fead501fe8b8945f9b751372d852c902acaab0e4b7957cd76c6`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.9.1-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:76734439a0da077a2a0564dae08819c171163a3f43af9dc5ee95c5255d7826fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50217935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bdbf4e7b18cbe41ca369d002ed964061f8d47cf7e099529129e2c375a19d8a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:00:58 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:00:58 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:00:59 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:25:06 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:29:50 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:29:51 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:29:51 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:29:51 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:29:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba435b73adbcc84b885316736a834b558eb49d3eb58bdb27e67773b5e764c8f`  
		Last Modified: Wed, 03 Jul 2024 16:30:27 GMT  
		Size: 47.0 MB (47043099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960888a62058d68ecbbbf9ca99501c32e047d316bb5923d63aa028288c19a1f`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61450a00438a5dec614f819522ab4e2b3882997a3920aa57748a1014e419110`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.9.1-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:edf8589d738d479d06e748fc9fb6e69ea28869686208b0b3d380452f4f53835d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52033638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81447dab97eaecff2920bdd6ed6eda90bf798cc22fca063c1fd5ac703fd58cfc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:14:40 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 01:14:40 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 01:14:40 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:00 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:32:51 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:32:52 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:32:52 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:32:52 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:32:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266b0af012afdf74d76deed54585824e29bf2f23bab214ce2ccd5f171fa03d56`  
		Last Modified: Wed, 03 Jul 2024 16:33:30 GMT  
		Size: 48.7 MB (48675511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1467b163421999dcb01504a93ab7425527ebf888cacf0e978c6a212f39acc75a`  
		Last Modified: Wed, 03 Jul 2024 16:33:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12eada70c981c5a75d135dc077f78c7b0ad72ae898619f3ffa028119391c2cf`  
		Last Modified: Wed, 03 Jul 2024 16:33:24 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:latest`

```console
$ docker pull znc@sha256:58f44e7e7bfccd2a242ce9277453abe0edf2ce79a00154eb4607cb5a2e7ffecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:9f005c499c46cbb94860d486c14ed051390b127438c41ba6552c1b367a702a9a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160052624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09ced1c4aa8abf3507139fa9915ff24c8561a6a20e1fac4926280062b2526e4`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:37:02 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:37:02 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:37:02 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:40 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:34:10 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:34:11 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:34:11 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:34:11 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:34:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:34:26 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 03 Jul 2024 16:34:27 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0689ade954ed751ec3753a47ba592aef3b27ce8108695f88ac3f65e43be4d452`  
		Last Modified: Wed, 03 Jul 2024 16:34:44 GMT  
		Size: 48.7 MB (48738318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab3a63dedf09abf22def150aa802cfb2ad85b93a8a09584da94dc88976970f5`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc64c738338fead501fe8b8945f9b751372d852c902acaab0e4b7957cd76c6`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be52d63d7334a8af0243fadd40818a46936d674c1452cd9204ae0ac4169f4901`  
		Last Modified: Wed, 03 Jul 2024 16:35:08 GMT  
		Size: 107.9 MB (107895718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a569bddc9f3d2a1bfadad4aa81df1cd6ee89d3e2962160db161530fb148bb88`  
		Last Modified: Wed, 03 Jul 2024 16:34:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:21cfc243ee90a505ed788fe7dda5e93fa3815cb2d00f9a41abcf2c3cf69cdb43
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142114258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61c111ec5813dbd30a3e7c73f6911a91d84ac15afadcd5110140fb3b253dfe05`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:00:58 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:00:58 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:00:59 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:25:06 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:29:50 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:29:51 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:29:51 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:29:51 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:29:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:30:08 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 03 Jul 2024 16:30:10 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba435b73adbcc84b885316736a834b558eb49d3eb58bdb27e67773b5e764c8f`  
		Last Modified: Wed, 03 Jul 2024 16:30:27 GMT  
		Size: 47.0 MB (47043099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960888a62058d68ecbbbf9ca99501c32e047d316bb5923d63aa028288c19a1f`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61450a00438a5dec614f819522ab4e2b3882997a3920aa57748a1014e419110`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4c80a70b183fd10e0acaa69924f82a9bad6842bf46e8d509c24fe7b30f8134`  
		Last Modified: Wed, 03 Jul 2024 16:30:56 GMT  
		Size: 91.9 MB (91895992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e6a177948d4eb7793ac5df8a7595af0991964b6485b71f8daf92d8782736d1`  
		Last Modified: Wed, 03 Jul 2024 16:30:41 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:56ee38ba5184ebbb1553f2f9169f21638494f97696e30ce890fe9c766c52ea86
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154410049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e393bdb7485d9585da6de310eefbafd5289d6611181aff4dcbde3b57a2361511`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:14:40 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 01:14:40 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 01:14:40 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:00 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:32:51 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:32:52 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:32:52 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:32:52 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:32:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Jul 2024 16:33:13 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 03 Jul 2024 16:33:15 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266b0af012afdf74d76deed54585824e29bf2f23bab214ce2ccd5f171fa03d56`  
		Last Modified: Wed, 03 Jul 2024 16:33:30 GMT  
		Size: 48.7 MB (48675511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1467b163421999dcb01504a93ab7425527ebf888cacf0e978c6a212f39acc75a`  
		Last Modified: Wed, 03 Jul 2024 16:33:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12eada70c981c5a75d135dc077f78c7b0ad72ae898619f3ffa028119391c2cf`  
		Last Modified: Wed, 03 Jul 2024 16:33:24 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aff1982f7ce645309fe933450549c80170df20971ee87c311899e229da3b3e8`  
		Last Modified: Wed, 03 Jul 2024 16:33:53 GMT  
		Size: 102.4 MB (102376079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b300651a32b8a35e2dfcee22809395e151a02f49c8f795ad8b364c9a584b0221`  
		Last Modified: Wed, 03 Jul 2024 16:33:42 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:slim`

```console
$ docker pull znc@sha256:fcc741b41ce0141f61ababbabab3245b64ccd79eb1299c7ea82d4aabfccce9ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:09d49e75f77d21fbc7baead597ec7c9e7f245ee8a02d4e904572c3dbce1fe729
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52156574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888cd694179c30693c76092493d5e46cf172b060039124ab8a5530fd842bec48`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:37:02 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:37:02 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:37:02 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:40 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:34:10 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:34:11 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:34:11 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:34:11 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:34:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0689ade954ed751ec3753a47ba592aef3b27ce8108695f88ac3f65e43be4d452`  
		Last Modified: Wed, 03 Jul 2024 16:34:44 GMT  
		Size: 48.7 MB (48738318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ab3a63dedf09abf22def150aa802cfb2ad85b93a8a09584da94dc88976970f5`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9fc64c738338fead501fe8b8945f9b751372d852c902acaab0e4b7957cd76c6`  
		Last Modified: Wed, 03 Jul 2024 16:34:37 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:76734439a0da077a2a0564dae08819c171163a3f43af9dc5ee95c5255d7826fc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50217935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2bdbf4e7b18cbe41ca369d002ed964061f8d47cf7e099529129e2c375a19d8a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:49:18 GMT
ADD file:8a9a8699eda49e02bf479cd01e71af80d721e91898a1c053620f39f99069de0a in / 
# Thu, 20 Jun 2024 17:49:18 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 02:00:58 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 02:00:58 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 02:00:59 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:25:06 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:29:50 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:29:51 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:29:51 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:29:51 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:29:51 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba435b73adbcc84b885316736a834b558eb49d3eb58bdb27e67773b5e764c8f`  
		Last Modified: Wed, 03 Jul 2024 16:30:27 GMT  
		Size: 47.0 MB (47043099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5960888a62058d68ecbbbf9ca99501c32e047d316bb5923d63aa028288c19a1f`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b61450a00438a5dec614f819522ab4e2b3882997a3920aa57748a1014e419110`  
		Last Modified: Wed, 03 Jul 2024 16:30:20 GMT  
		Size: 757.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:edf8589d738d479d06e748fc9fb6e69ea28869686208b0b3d380452f4f53835d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (52033638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81447dab97eaecff2920bdd6ed6eda90bf798cc22fca063c1fd5ac703fd58cfc`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Fri, 21 Jun 2024 01:14:40 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Fri, 21 Jun 2024 01:14:40 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Fri, 21 Jun 2024 01:14:40 GMT
ARG MAKEFLAGS=
# Wed, 03 Jul 2024 16:29:00 GMT
ENV ZNC_VERSION=1.9.1
# Wed, 03 Jul 2024 16:32:51 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 03 Jul 2024 16:32:52 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 03 Jul 2024 16:32:52 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 03 Jul 2024 16:32:52 GMT
VOLUME [/znc-data]
# Wed, 03 Jul 2024 16:32:52 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266b0af012afdf74d76deed54585824e29bf2f23bab214ce2ccd5f171fa03d56`  
		Last Modified: Wed, 03 Jul 2024 16:33:30 GMT  
		Size: 48.7 MB (48675511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1467b163421999dcb01504a93ab7425527ebf888cacf0e978c6a212f39acc75a`  
		Last Modified: Wed, 03 Jul 2024 16:33:25 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c12eada70c981c5a75d135dc077f78c7b0ad72ae898619f3ffa028119391c2cf`  
		Last Modified: Wed, 03 Jul 2024 16:33:24 GMT  
		Size: 754.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
