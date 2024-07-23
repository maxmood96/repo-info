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
$ docker pull znc@sha256:133897532bad2dbfb85a650d9fed957d8b262798d3e2d82c59d380486ebd71a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.9` - linux; amd64

```console
$ docker pull znc@sha256:43ba74b0f04ac8a8c6944e552f47461d3c1fb6885216eae9c753686a444fdc1a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157975780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136d16edc33023de7ddc138e13d2fd67ca2ab496fe900f4830487825c6a97f73`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:27:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 23 Jul 2024 00:27:13 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 23 Jul 2024 00:27:13 GMT
ARG MAKEFLAGS=
# Tue, 23 Jul 2024 00:27:13 GMT
ENV ZNC_VERSION=1.9.1
# Tue, 23 Jul 2024 00:31:40 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 23 Jul 2024 00:31:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 23 Jul 2024 00:31:41 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Tue, 23 Jul 2024 00:31:41 GMT
VOLUME [/znc-data]
# Tue, 23 Jul 2024 00:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Jul 2024 00:31:58 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Tue, 23 Jul 2024 00:31:59 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4911405cd03927756f93b2700d49261f8bc6933b05720f05d93eb5f8336a7d0`  
		Last Modified: Tue, 23 Jul 2024 00:32:15 GMT  
		Size: 46.7 MB (46659727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54ae4a9a08ce9c9a90821422abc79e98d7dd8effe379e7ab7d24f009482853a`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891eb3d763b6c516a5e404c83070e2e96687f749aef10f6cbdec88af8a3e200`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2ff230e1f0179da0c0fefdc20821a98d906de6738e98f8f443199bc23884fb`  
		Last Modified: Tue, 23 Jul 2024 00:32:39 GMT  
		Size: 107.9 MB (107895758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c2c30dec9b8962e65501ac8a462bc26ee6e6024f50ce558062de9ae4ebd66c`  
		Last Modified: Tue, 23 Jul 2024 00:32:24 GMT  
		Size: 330.0 B  
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
$ docker pull znc@sha256:3beb10b9d6c8c3a9f07da58869e1ec1b4a7523eebfa650da6e29bb96423b3bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.9-slim` - linux; amd64

```console
$ docker pull znc@sha256:8ea12b7d0b47cb9ba358a91dd92b2f25896e1c8ae07770f7cb6684a6e5a5856f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50079692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fbb080156e2b9a5a4c5f8067b47ee5d5a4b185db2615d60fe760252c504931`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:27:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 23 Jul 2024 00:27:13 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 23 Jul 2024 00:27:13 GMT
ARG MAKEFLAGS=
# Tue, 23 Jul 2024 00:27:13 GMT
ENV ZNC_VERSION=1.9.1
# Tue, 23 Jul 2024 00:31:40 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 23 Jul 2024 00:31:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 23 Jul 2024 00:31:41 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Tue, 23 Jul 2024 00:31:41 GMT
VOLUME [/znc-data]
# Tue, 23 Jul 2024 00:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4911405cd03927756f93b2700d49261f8bc6933b05720f05d93eb5f8336a7d0`  
		Last Modified: Tue, 23 Jul 2024 00:32:15 GMT  
		Size: 46.7 MB (46659727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54ae4a9a08ce9c9a90821422abc79e98d7dd8effe379e7ab7d24f009482853a`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891eb3d763b6c516a5e404c83070e2e96687f749aef10f6cbdec88af8a3e200`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 752.0 B  
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
$ docker pull znc@sha256:133897532bad2dbfb85a650d9fed957d8b262798d3e2d82c59d380486ebd71a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.9.1` - linux; amd64

```console
$ docker pull znc@sha256:43ba74b0f04ac8a8c6944e552f47461d3c1fb6885216eae9c753686a444fdc1a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157975780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136d16edc33023de7ddc138e13d2fd67ca2ab496fe900f4830487825c6a97f73`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:27:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 23 Jul 2024 00:27:13 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 23 Jul 2024 00:27:13 GMT
ARG MAKEFLAGS=
# Tue, 23 Jul 2024 00:27:13 GMT
ENV ZNC_VERSION=1.9.1
# Tue, 23 Jul 2024 00:31:40 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 23 Jul 2024 00:31:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 23 Jul 2024 00:31:41 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Tue, 23 Jul 2024 00:31:41 GMT
VOLUME [/znc-data]
# Tue, 23 Jul 2024 00:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Jul 2024 00:31:58 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Tue, 23 Jul 2024 00:31:59 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4911405cd03927756f93b2700d49261f8bc6933b05720f05d93eb5f8336a7d0`  
		Last Modified: Tue, 23 Jul 2024 00:32:15 GMT  
		Size: 46.7 MB (46659727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54ae4a9a08ce9c9a90821422abc79e98d7dd8effe379e7ab7d24f009482853a`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891eb3d763b6c516a5e404c83070e2e96687f749aef10f6cbdec88af8a3e200`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2ff230e1f0179da0c0fefdc20821a98d906de6738e98f8f443199bc23884fb`  
		Last Modified: Tue, 23 Jul 2024 00:32:39 GMT  
		Size: 107.9 MB (107895758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c2c30dec9b8962e65501ac8a462bc26ee6e6024f50ce558062de9ae4ebd66c`  
		Last Modified: Tue, 23 Jul 2024 00:32:24 GMT  
		Size: 330.0 B  
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
$ docker pull znc@sha256:3beb10b9d6c8c3a9f07da58869e1ec1b4a7523eebfa650da6e29bb96423b3bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.9.1-slim` - linux; amd64

```console
$ docker pull znc@sha256:8ea12b7d0b47cb9ba358a91dd92b2f25896e1c8ae07770f7cb6684a6e5a5856f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50079692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fbb080156e2b9a5a4c5f8067b47ee5d5a4b185db2615d60fe760252c504931`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:27:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 23 Jul 2024 00:27:13 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 23 Jul 2024 00:27:13 GMT
ARG MAKEFLAGS=
# Tue, 23 Jul 2024 00:27:13 GMT
ENV ZNC_VERSION=1.9.1
# Tue, 23 Jul 2024 00:31:40 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 23 Jul 2024 00:31:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 23 Jul 2024 00:31:41 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Tue, 23 Jul 2024 00:31:41 GMT
VOLUME [/znc-data]
# Tue, 23 Jul 2024 00:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4911405cd03927756f93b2700d49261f8bc6933b05720f05d93eb5f8336a7d0`  
		Last Modified: Tue, 23 Jul 2024 00:32:15 GMT  
		Size: 46.7 MB (46659727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54ae4a9a08ce9c9a90821422abc79e98d7dd8effe379e7ab7d24f009482853a`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891eb3d763b6c516a5e404c83070e2e96687f749aef10f6cbdec88af8a3e200`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 752.0 B  
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
$ docker pull znc@sha256:133897532bad2dbfb85a650d9fed957d8b262798d3e2d82c59d380486ebd71a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:43ba74b0f04ac8a8c6944e552f47461d3c1fb6885216eae9c753686a444fdc1a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157975780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:136d16edc33023de7ddc138e13d2fd67ca2ab496fe900f4830487825c6a97f73`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:27:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 23 Jul 2024 00:27:13 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 23 Jul 2024 00:27:13 GMT
ARG MAKEFLAGS=
# Tue, 23 Jul 2024 00:27:13 GMT
ENV ZNC_VERSION=1.9.1
# Tue, 23 Jul 2024 00:31:40 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 23 Jul 2024 00:31:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 23 Jul 2024 00:31:41 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Tue, 23 Jul 2024 00:31:41 GMT
VOLUME [/znc-data]
# Tue, 23 Jul 2024 00:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 23 Jul 2024 00:31:58 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Tue, 23 Jul 2024 00:31:59 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4911405cd03927756f93b2700d49261f8bc6933b05720f05d93eb5f8336a7d0`  
		Last Modified: Tue, 23 Jul 2024 00:32:15 GMT  
		Size: 46.7 MB (46659727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54ae4a9a08ce9c9a90821422abc79e98d7dd8effe379e7ab7d24f009482853a`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891eb3d763b6c516a5e404c83070e2e96687f749aef10f6cbdec88af8a3e200`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 752.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2ff230e1f0179da0c0fefdc20821a98d906de6738e98f8f443199bc23884fb`  
		Last Modified: Tue, 23 Jul 2024 00:32:39 GMT  
		Size: 107.9 MB (107895758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2c2c30dec9b8962e65501ac8a462bc26ee6e6024f50ce558062de9ae4ebd66c`  
		Last Modified: Tue, 23 Jul 2024 00:32:24 GMT  
		Size: 330.0 B  
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
$ docker pull znc@sha256:3beb10b9d6c8c3a9f07da58869e1ec1b4a7523eebfa650da6e29bb96423b3bfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:8ea12b7d0b47cb9ba358a91dd92b2f25896e1c8ae07770f7cb6684a6e5a5856f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50079692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fbb080156e2b9a5a4c5f8067b47ee5d5a4b185db2615d60fe760252c504931`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Mon, 22 Jul 2024 22:26:49 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Mon, 22 Jul 2024 22:26:49 GMT
CMD ["/bin/sh"]
# Tue, 23 Jul 2024 00:27:13 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Tue, 23 Jul 2024 00:27:13 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES
# Tue, 23 Jul 2024 00:27:13 GMT
ARG MAKEFLAGS=
# Tue, 23 Jul 2024 00:27:13 GMT
ENV ZNC_VERSION=1.9.1
# Tue, 23 Jul 2024 00:31:40 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Tue, 23 Jul 2024 00:31:41 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Tue, 23 Jul 2024 00:31:41 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Tue, 23 Jul 2024 00:31:41 GMT
VOLUME [/znc-data]
# Tue, 23 Jul 2024 00:31:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4911405cd03927756f93b2700d49261f8bc6933b05720f05d93eb5f8336a7d0`  
		Last Modified: Tue, 23 Jul 2024 00:32:15 GMT  
		Size: 46.7 MB (46659727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54ae4a9a08ce9c9a90821422abc79e98d7dd8effe379e7ab7d24f009482853a`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a891eb3d763b6c516a5e404c83070e2e96687f749aef10f6cbdec88af8a3e200`  
		Last Modified: Tue, 23 Jul 2024 00:32:09 GMT  
		Size: 752.0 B  
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
