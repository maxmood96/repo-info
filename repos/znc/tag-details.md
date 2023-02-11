<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `znc`

-	[`znc:1.8`](#znc18)
-	[`znc:1.8-slim`](#znc18-slim)
-	[`znc:1.8.2`](#znc182)
-	[`znc:1.8.2-slim`](#znc182-slim)
-	[`znc:latest`](#znclatest)
-	[`znc:slim`](#zncslim)

## `znc:1.8`

```console
$ docker pull znc@sha256:b5f81268045fe0f9f6da3ecbd8ec0f13858be87063e40bd0416c116c940fc9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8` - linux; amd64

```console
$ docker pull znc@sha256:5294d3e7cf6ed092ae08fe10d035d3dd0588abd5253df9a0f20cdaeeea677cbf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164462131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4bbe32133512dc21b0bafbb6a54f5ae62e499b11eaa02a5e0dea481fff537d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:54:45 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 13:54:45 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 13:54:45 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 13:54:45 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 13:58:31 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 13:58:32 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 13:58:32 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 13:58:32 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 13:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 13:58:44 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 11 Feb 2023 13:58:45 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c1fb32d5b69cfb6ca8a4740b181b388598feea6d60c1b53f115e63b65fef0`  
		Last Modified: Sat, 11 Feb 2023 13:59:04 GMT  
		Size: 46.6 MB (46588099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd00d73a66e8304f42e67390ace34a478b4eb0aab6741066c52b5638a4e099`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb2152cbcae7ef77e4fa6a065607e8b2d32716cb3b24bdf18f9fa4a8677f73`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360f862f8c6a8720c094ee12d52e7c08359860310df96b218e334bdae0558727`  
		Last Modified: Sat, 11 Feb 2023 13:59:30 GMT  
		Size: 114.5 MB (114498303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ae80113afb2fdd70e4e74526ea293aab36abf3db344b6e88e5285ec7ce2ecd`  
		Last Modified: Sat, 11 Feb 2023 13:59:14 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm variant v6

```console
$ docker pull znc@sha256:72b91d57eaaac7019727c542ab556ef29433c67ae6f864ee9a5b8aa620a921fe
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144038791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae5136b99d5040832c77bc29a4170e6842ed073222a24fdfb8e2598206e3c76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 03:38:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 03:38:07 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 03:38:08 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 03:42:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 03:42:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 03:42:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 03:42:40 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 03:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 03:43:00 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 11 Feb 2023 03:43:01 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d99e5fbf0d5bbc554790b9b6f8139ad8a5c2d439cf8ada388c4dc07f3ef49`  
		Last Modified: Sat, 11 Feb 2023 03:43:35 GMT  
		Size: 44.8 MB (44791788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be077d44b9b301689f79ab3664eb481753d39da8082dfdf8c543c566a80c8fa9`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b389aac55b7e2893117b933180c7e49e5e8b6350871f05c581583d2266a57`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918549232d2460eb19a3c3ab854b119163e59423ea2ab9b896f889715039499`  
		Last Modified: Sat, 11 Feb 2023 03:44:07 GMT  
		Size: 96.1 MB (96134860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c791ed9239c7201a295fda8604cf8ec3d475f98e64d29d927b70cb5950e1856`  
		Last Modified: Sat, 11 Feb 2023 03:43:49 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:37cd94bb391753daf8119c220463ce73ffe921f292c1269c8ea5a56cb5031a55
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153313402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf1e209934bc1faa5d927e431d05dfdfb28529a4f23623bbced43cc5c1d9c3e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:34:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 06:34:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 06:34:11 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 06:34:11 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 06:37:26 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 06:37:27 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 06:37:27 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 06:37:27 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 06:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:37:39 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 11 Feb 2023 06:37:41 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b04ab7b5a12f57cb1cf8331a3288badf7a1a021775168e01400a895b2dd31b`  
		Last Modified: Sat, 11 Feb 2023 06:38:00 GMT  
		Size: 46.2 MB (46173500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e880eb099c01c2b6dfa9c3ef24d26f1130f5ce992eb4cf07a14499f3fa8d719`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6168449e9ccea607d3114ee348301a27d25dc49cb8d5368759d363cdb25366fe`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24212c2f471202286d4720f41278b1817ccd6c921a5f93729525ccd83a8ca66`  
		Last Modified: Sat, 11 Feb 2023 06:38:22 GMT  
		Size: 103.9 MB (103876661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729689fd2d06bce9d80b512d3d152e5378dc7ca4f2157e20049f7dd8222e172`  
		Last Modified: Sat, 11 Feb 2023 06:38:10 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8-slim`

```console
$ docker pull znc@sha256:f77f37846b911c30b821c84471501fda38e96e839eea00ab052ad801dd4838e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8-slim` - linux; amd64

```console
$ docker pull znc@sha256:04e14af599760c8852b86ecacf424f50cf9b3fe4735818537ffda39f108ad3f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49963497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2aa8a1a6b97954b23688b5f3e11ef1959263dae4a84dc86b9799539095b6b2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:54:45 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 13:54:45 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 13:54:45 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 13:54:45 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 13:58:31 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 13:58:32 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 13:58:32 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 13:58:32 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 13:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c1fb32d5b69cfb6ca8a4740b181b388598feea6d60c1b53f115e63b65fef0`  
		Last Modified: Sat, 11 Feb 2023 13:59:04 GMT  
		Size: 46.6 MB (46588099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd00d73a66e8304f42e67390ace34a478b4eb0aab6741066c52b5638a4e099`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb2152cbcae7ef77e4fa6a065607e8b2d32716cb3b24bdf18f9fa4a8677f73`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:6af40c9e744dc2cdd371b2058409d618844e8fea832ed62502ab476a24163568
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47903598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16c272fad6f85350300c57df766f0637565d94f07fef111882b8b715365e5ed`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 03:38:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 03:38:07 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 03:38:08 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 03:42:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 03:42:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 03:42:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 03:42:40 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 03:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d99e5fbf0d5bbc554790b9b6f8139ad8a5c2d439cf8ada388c4dc07f3ef49`  
		Last Modified: Sat, 11 Feb 2023 03:43:35 GMT  
		Size: 44.8 MB (44791788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be077d44b9b301689f79ab3664eb481753d39da8082dfdf8c543c566a80c8fa9`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b389aac55b7e2893117b933180c7e49e5e8b6350871f05c581583d2266a57`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:4f06f80d62b360c9a24d53011b2323f80193703fc449e42fe99271afd3b52777
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49436410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb6eaa2eebfc1965a231aaf6219d630a1c53ed6c2d79adee94280d83b7a1c2f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:34:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 06:34:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 06:34:11 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 06:34:11 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 06:37:26 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 06:37:27 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 06:37:27 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 06:37:27 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 06:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b04ab7b5a12f57cb1cf8331a3288badf7a1a021775168e01400a895b2dd31b`  
		Last Modified: Sat, 11 Feb 2023 06:38:00 GMT  
		Size: 46.2 MB (46173500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e880eb099c01c2b6dfa9c3ef24d26f1130f5ce992eb4cf07a14499f3fa8d719`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6168449e9ccea607d3114ee348301a27d25dc49cb8d5368759d363cdb25366fe`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2`

```console
$ docker pull znc@sha256:b5f81268045fe0f9f6da3ecbd8ec0f13858be87063e40bd0416c116c940fc9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2` - linux; amd64

```console
$ docker pull znc@sha256:5294d3e7cf6ed092ae08fe10d035d3dd0588abd5253df9a0f20cdaeeea677cbf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164462131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4bbe32133512dc21b0bafbb6a54f5ae62e499b11eaa02a5e0dea481fff537d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:54:45 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 13:54:45 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 13:54:45 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 13:54:45 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 13:58:31 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 13:58:32 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 13:58:32 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 13:58:32 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 13:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 13:58:44 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 11 Feb 2023 13:58:45 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c1fb32d5b69cfb6ca8a4740b181b388598feea6d60c1b53f115e63b65fef0`  
		Last Modified: Sat, 11 Feb 2023 13:59:04 GMT  
		Size: 46.6 MB (46588099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd00d73a66e8304f42e67390ace34a478b4eb0aab6741066c52b5638a4e099`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb2152cbcae7ef77e4fa6a065607e8b2d32716cb3b24bdf18f9fa4a8677f73`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360f862f8c6a8720c094ee12d52e7c08359860310df96b218e334bdae0558727`  
		Last Modified: Sat, 11 Feb 2023 13:59:30 GMT  
		Size: 114.5 MB (114498303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ae80113afb2fdd70e4e74526ea293aab36abf3db344b6e88e5285ec7ce2ecd`  
		Last Modified: Sat, 11 Feb 2023 13:59:14 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm variant v6

```console
$ docker pull znc@sha256:72b91d57eaaac7019727c542ab556ef29433c67ae6f864ee9a5b8aa620a921fe
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144038791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae5136b99d5040832c77bc29a4170e6842ed073222a24fdfb8e2598206e3c76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 03:38:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 03:38:07 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 03:38:08 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 03:42:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 03:42:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 03:42:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 03:42:40 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 03:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 03:43:00 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 11 Feb 2023 03:43:01 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d99e5fbf0d5bbc554790b9b6f8139ad8a5c2d439cf8ada388c4dc07f3ef49`  
		Last Modified: Sat, 11 Feb 2023 03:43:35 GMT  
		Size: 44.8 MB (44791788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be077d44b9b301689f79ab3664eb481753d39da8082dfdf8c543c566a80c8fa9`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b389aac55b7e2893117b933180c7e49e5e8b6350871f05c581583d2266a57`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918549232d2460eb19a3c3ab854b119163e59423ea2ab9b896f889715039499`  
		Last Modified: Sat, 11 Feb 2023 03:44:07 GMT  
		Size: 96.1 MB (96134860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c791ed9239c7201a295fda8604cf8ec3d475f98e64d29d927b70cb5950e1856`  
		Last Modified: Sat, 11 Feb 2023 03:43:49 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:37cd94bb391753daf8119c220463ce73ffe921f292c1269c8ea5a56cb5031a55
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153313402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf1e209934bc1faa5d927e431d05dfdfb28529a4f23623bbced43cc5c1d9c3e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:34:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 06:34:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 06:34:11 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 06:34:11 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 06:37:26 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 06:37:27 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 06:37:27 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 06:37:27 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 06:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:37:39 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 11 Feb 2023 06:37:41 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b04ab7b5a12f57cb1cf8331a3288badf7a1a021775168e01400a895b2dd31b`  
		Last Modified: Sat, 11 Feb 2023 06:38:00 GMT  
		Size: 46.2 MB (46173500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e880eb099c01c2b6dfa9c3ef24d26f1130f5ce992eb4cf07a14499f3fa8d719`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6168449e9ccea607d3114ee348301a27d25dc49cb8d5368759d363cdb25366fe`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24212c2f471202286d4720f41278b1817ccd6c921a5f93729525ccd83a8ca66`  
		Last Modified: Sat, 11 Feb 2023 06:38:22 GMT  
		Size: 103.9 MB (103876661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729689fd2d06bce9d80b512d3d152e5378dc7ca4f2157e20049f7dd8222e172`  
		Last Modified: Sat, 11 Feb 2023 06:38:10 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:1.8.2-slim`

```console
$ docker pull znc@sha256:f77f37846b911c30b821c84471501fda38e96e839eea00ab052ad801dd4838e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:1.8.2-slim` - linux; amd64

```console
$ docker pull znc@sha256:04e14af599760c8852b86ecacf424f50cf9b3fe4735818537ffda39f108ad3f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49963497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2aa8a1a6b97954b23688b5f3e11ef1959263dae4a84dc86b9799539095b6b2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:54:45 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 13:54:45 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 13:54:45 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 13:54:45 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 13:58:31 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 13:58:32 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 13:58:32 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 13:58:32 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 13:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c1fb32d5b69cfb6ca8a4740b181b388598feea6d60c1b53f115e63b65fef0`  
		Last Modified: Sat, 11 Feb 2023 13:59:04 GMT  
		Size: 46.6 MB (46588099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd00d73a66e8304f42e67390ace34a478b4eb0aab6741066c52b5638a4e099`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb2152cbcae7ef77e4fa6a065607e8b2d32716cb3b24bdf18f9fa4a8677f73`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:6af40c9e744dc2cdd371b2058409d618844e8fea832ed62502ab476a24163568
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47903598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16c272fad6f85350300c57df766f0637565d94f07fef111882b8b715365e5ed`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 03:38:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 03:38:07 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 03:38:08 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 03:42:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 03:42:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 03:42:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 03:42:40 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 03:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d99e5fbf0d5bbc554790b9b6f8139ad8a5c2d439cf8ada388c4dc07f3ef49`  
		Last Modified: Sat, 11 Feb 2023 03:43:35 GMT  
		Size: 44.8 MB (44791788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be077d44b9b301689f79ab3664eb481753d39da8082dfdf8c543c566a80c8fa9`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b389aac55b7e2893117b933180c7e49e5e8b6350871f05c581583d2266a57`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:1.8.2-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:4f06f80d62b360c9a24d53011b2323f80193703fc449e42fe99271afd3b52777
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49436410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb6eaa2eebfc1965a231aaf6219d630a1c53ed6c2d79adee94280d83b7a1c2f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:34:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 06:34:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 06:34:11 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 06:34:11 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 06:37:26 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 06:37:27 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 06:37:27 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 06:37:27 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 06:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b04ab7b5a12f57cb1cf8331a3288badf7a1a021775168e01400a895b2dd31b`  
		Last Modified: Sat, 11 Feb 2023 06:38:00 GMT  
		Size: 46.2 MB (46173500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e880eb099c01c2b6dfa9c3ef24d26f1130f5ce992eb4cf07a14499f3fa8d719`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6168449e9ccea607d3114ee348301a27d25dc49cb8d5368759d363cdb25366fe`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:latest`

```console
$ docker pull znc@sha256:b5f81268045fe0f9f6da3ecbd8ec0f13858be87063e40bd0416c116c940fc9a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:5294d3e7cf6ed092ae08fe10d035d3dd0588abd5253df9a0f20cdaeeea677cbf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164462131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e4bbe32133512dc21b0bafbb6a54f5ae62e499b11eaa02a5e0dea481fff537d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:54:45 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 13:54:45 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 13:54:45 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 13:54:45 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 13:58:31 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 13:58:32 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 13:58:32 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 13:58:32 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 13:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 13:58:44 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 11 Feb 2023 13:58:45 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c1fb32d5b69cfb6ca8a4740b181b388598feea6d60c1b53f115e63b65fef0`  
		Last Modified: Sat, 11 Feb 2023 13:59:04 GMT  
		Size: 46.6 MB (46588099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd00d73a66e8304f42e67390ace34a478b4eb0aab6741066c52b5638a4e099`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb2152cbcae7ef77e4fa6a065607e8b2d32716cb3b24bdf18f9fa4a8677f73`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360f862f8c6a8720c094ee12d52e7c08359860310df96b218e334bdae0558727`  
		Last Modified: Sat, 11 Feb 2023 13:59:30 GMT  
		Size: 114.5 MB (114498303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ae80113afb2fdd70e4e74526ea293aab36abf3db344b6e88e5285ec7ce2ecd`  
		Last Modified: Sat, 11 Feb 2023 13:59:14 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:72b91d57eaaac7019727c542ab556ef29433c67ae6f864ee9a5b8aa620a921fe
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (144038791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae5136b99d5040832c77bc29a4170e6842ed073222a24fdfb8e2598206e3c76`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 03:38:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 03:38:07 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 03:38:08 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 03:42:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 03:42:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 03:42:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 03:42:40 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 03:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 03:43:00 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 11 Feb 2023 03:43:01 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d99e5fbf0d5bbc554790b9b6f8139ad8a5c2d439cf8ada388c4dc07f3ef49`  
		Last Modified: Sat, 11 Feb 2023 03:43:35 GMT  
		Size: 44.8 MB (44791788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be077d44b9b301689f79ab3664eb481753d39da8082dfdf8c543c566a80c8fa9`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b389aac55b7e2893117b933180c7e49e5e8b6350871f05c581583d2266a57`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f918549232d2460eb19a3c3ab854b119163e59423ea2ab9b896f889715039499`  
		Last Modified: Sat, 11 Feb 2023 03:44:07 GMT  
		Size: 96.1 MB (96134860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c791ed9239c7201a295fda8604cf8ec3d475f98e64d29d927b70cb5950e1856`  
		Last Modified: Sat, 11 Feb 2023 03:43:49 GMT  
		Size: 333.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:37cd94bb391753daf8119c220463ce73ffe921f292c1269c8ea5a56cb5031a55
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.3 MB (153313402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdf1e209934bc1faa5d927e431d05dfdfb28529a4f23623bbced43cc5c1d9c3e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:34:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 06:34:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 06:34:11 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 06:34:11 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 06:37:26 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 06:37:27 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 06:37:27 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 06:37:27 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 06:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 11 Feb 2023 06:37:39 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Sat, 11 Feb 2023 06:37:41 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b04ab7b5a12f57cb1cf8331a3288badf7a1a021775168e01400a895b2dd31b`  
		Last Modified: Sat, 11 Feb 2023 06:38:00 GMT  
		Size: 46.2 MB (46173500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e880eb099c01c2b6dfa9c3ef24d26f1130f5ce992eb4cf07a14499f3fa8d719`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6168449e9ccea607d3114ee348301a27d25dc49cb8d5368759d363cdb25366fe`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24212c2f471202286d4720f41278b1817ccd6c921a5f93729525ccd83a8ca66`  
		Last Modified: Sat, 11 Feb 2023 06:38:22 GMT  
		Size: 103.9 MB (103876661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0729689fd2d06bce9d80b512d3d152e5378dc7ca4f2157e20049f7dd8222e172`  
		Last Modified: Sat, 11 Feb 2023 06:38:10 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `znc:slim`

```console
$ docker pull znc@sha256:f77f37846b911c30b821c84471501fda38e96e839eea00ab052ad801dd4838e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:slim` - linux; amd64

```console
$ docker pull znc@sha256:04e14af599760c8852b86ecacf424f50cf9b3fe4735818537ffda39f108ad3f3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49963497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2aa8a1a6b97954b23688b5f3e11ef1959263dae4a84dc86b9799539095b6b2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 13:54:45 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 13:54:45 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 13:54:45 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 13:54:45 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 13:58:31 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 13:58:32 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 13:58:32 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 13:58:32 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 13:58:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:593c1fb32d5b69cfb6ca8a4740b181b388598feea6d60c1b53f115e63b65fef0`  
		Last Modified: Sat, 11 Feb 2023 13:59:04 GMT  
		Size: 46.6 MB (46588099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6dd00d73a66e8304f42e67390ace34a478b4eb0aab6741066c52b5638a4e099`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bb2152cbcae7ef77e4fa6a065607e8b2d32716cb3b24bdf18f9fa4a8677f73`  
		Last Modified: Sat, 11 Feb 2023 13:58:57 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:6af40c9e744dc2cdd371b2058409d618844e8fea832ed62502ab476a24163568
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47903598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16c272fad6f85350300c57df766f0637565d94f07fef111882b8b715365e5ed`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:28 GMT
ADD file:d825d9aef59df0df23c0140a490998407ee0a62a051699b5c050aef7cb03f042 in / 
# Fri, 10 Feb 2023 20:49:28 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 03:38:07 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 03:38:07 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 03:38:07 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 03:38:08 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 03:42:39 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 03:42:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 03:42:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 03:42:40 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 03:42:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:6a6e4ab63e54442e16400f69d37f662d60cbd67565631eff6bf59b4176e482c3`  
		Last Modified: Fri, 10 Feb 2023 20:50:22 GMT  
		Size: 3.1 MB (3110885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0d99e5fbf0d5bbc554790b9b6f8139ad8a5c2d439cf8ada388c4dc07f3ef49`  
		Last Modified: Sat, 11 Feb 2023 03:43:35 GMT  
		Size: 44.8 MB (44791788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be077d44b9b301689f79ab3664eb481753d39da8082dfdf8c543c566a80c8fa9`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de6b389aac55b7e2893117b933180c7e49e5e8b6350871f05c581583d2266a57`  
		Last Modified: Sat, 11 Feb 2023 03:43:26 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:4f06f80d62b360c9a24d53011b2323f80193703fc449e42fe99271afd3b52777
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49436410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cb6eaa2eebfc1965a231aaf6219d630a1c53ed6c2d79adee94280d83b7a1c2f`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:08 GMT
ADD file:9bd9ea42a9f3bdc769e80c6b8a4b117d65f73ae68e155a6172a1184e7ac8bcc1 in / 
# Fri, 10 Feb 2023 21:24:08 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:34:11 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Sat, 11 Feb 2023 06:34:11 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Sat, 11 Feb 2023 06:34:11 GMT
ARG MAKEFLAGS=
# Sat, 11 Feb 2023 06:34:11 GMT
ENV ZNC_VERSION=1.8.2
# Sat, 11 Feb 2023 06:37:26 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Sat, 11 Feb 2023 06:37:27 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Sat, 11 Feb 2023 06:37:27 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Sat, 11 Feb 2023 06:37:27 GMT
VOLUME [/znc-data]
# Sat, 11 Feb 2023 06:37:27 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:af6eaf76a39c2d3e7e0b8a0420486e3df33c4027d696c076a99a3d0ac09026af`  
		Last Modified: Fri, 10 Feb 2023 21:24:39 GMT  
		Size: 3.3 MB (3261959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b04ab7b5a12f57cb1cf8331a3288badf7a1a021775168e01400a895b2dd31b`  
		Last Modified: Sat, 11 Feb 2023 06:38:00 GMT  
		Size: 46.2 MB (46173500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e880eb099c01c2b6dfa9c3ef24d26f1130f5ce992eb4cf07a14499f3fa8d719`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6168449e9ccea607d3114ee348301a27d25dc49cb8d5368759d363cdb25366fe`  
		Last Modified: Sat, 11 Feb 2023 06:37:54 GMT  
		Size: 780.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
