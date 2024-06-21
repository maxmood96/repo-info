## `znc:latest`

```console
$ docker pull znc@sha256:26650910bbdb0a5caad5578684bf8bc563188c297433d59d3bc6246ddb636d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:4e5126e93c45b4dc08b4d822b2910b43d83de6a3017ec05b33866d9a2115a650
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157963740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c2ad5a36af7b7bf30356a370fbbb96b1eddab5b41080dc1601b6e8ba5b567a4`
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
# Fri, 21 Jun 2024 02:37:02 GMT
ENV ZNC_VERSION=1.9.0
# Fri, 21 Jun 2024 02:41:40 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 21 Jun 2024 02:41:40 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 21 Jun 2024 02:41:40 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 21 Jun 2024 02:41:40 GMT
VOLUME [/znc-data]
# Fri, 21 Jun 2024 02:41:40 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Jun 2024 02:42:02 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 21 Jun 2024 02:42:03 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80556cf328a77b2fda65f75bdedae34d1f2ba6201ebc3078a9f4d382d412c3f6`  
		Last Modified: Fri, 21 Jun 2024 02:42:19 GMT  
		Size: 46.6 MB (46649346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4ff56299cf7583aadd860a3ce7882e0f1e7a5a07117e6fa927ad555ea25c22`  
		Last Modified: Fri, 21 Jun 2024 02:42:12 GMT  
		Size: 170.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5d21cdc76372dc23c2e3230ad6115de9003ea03bbf6b1e126add7b15e111110`  
		Last Modified: Fri, 21 Jun 2024 02:42:12 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acfb14846948ac07948270921ae61f8e470c03ec370583b484a320c71442f4a6`  
		Last Modified: Fri, 21 Jun 2024 02:42:43 GMT  
		Size: 107.9 MB (107895807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:066b3812a1f0de3abefcedfa28f9217d326ab83447fa788ca236d05cf4b63521`  
		Last Modified: Fri, 21 Jun 2024 02:42:28 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:2b1f31c174319cbd78589492eeaa6afc2215568731d549cfb74478ac68769efd
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140363716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad2799544162940d63f8c7d4fc4d6097d5c7d1255b1ad0bc0daf73eba47d566`
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
# Fri, 21 Jun 2024 02:00:59 GMT
ENV ZNC_VERSION=1.9.0
# Fri, 21 Jun 2024 02:05:36 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 21 Jun 2024 02:05:36 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 21 Jun 2024 02:05:37 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 21 Jun 2024 02:05:37 GMT
VOLUME [/znc-data]
# Fri, 21 Jun 2024 02:05:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Jun 2024 02:06:00 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 21 Jun 2024 02:06:01 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:217d5fa2bafb793ad47d21c0abaeeca94f1d39763a4cd3d178069467c1c42712`  
		Last Modified: Thu, 20 Jun 2024 17:49:48 GMT  
		Size: 3.2 MB (3173908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a7a21afb2318296dee076c9de4808c44431c66ccab49f1f59f4e160f6dc73c0`  
		Last Modified: Fri, 21 Jun 2024 02:06:19 GMT  
		Size: 45.3 MB (45292643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237e8217466ea507ef425e7efcd2f74558b20cf8a4134e047b91ce845d63e7f7`  
		Last Modified: Fri, 21 Jun 2024 02:06:12 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5659c36664eb2f5ed5d11336c31d6d40f8a52156d014fc25064baf5dfa2bc529`  
		Last Modified: Fri, 21 Jun 2024 02:06:12 GMT  
		Size: 755.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:091812966b40b2b49224b9ec09efceb89eed3efd0c5961f0f81a1da9e17f5545`  
		Last Modified: Fri, 21 Jun 2024 02:06:43 GMT  
		Size: 91.9 MB (91895904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed306986dca785decd2c15d9195d3254dfc05abd89891ea15ce98b29c09dd084`  
		Last Modified: Fri, 21 Jun 2024 02:06:29 GMT  
		Size: 334.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:548f216f6424a62baf7ffb6435b567a7295947c1bfc466f7569f51d597ebc6a4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152452230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cfdbc7bcd9dad5b2aa6b326a05be5666abd49c6f4f69707de07d0c6c38e3e1b`
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
# Fri, 21 Jun 2024 01:14:40 GMT
ENV ZNC_VERSION=1.9.0
# Fri, 21 Jun 2024 01:18:34 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES -DWANT_ARGON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         argon2-libs         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         argon2-dev         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Fri, 21 Jun 2024 01:18:35 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Fri, 21 Jun 2024 01:18:35 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Fri, 21 Jun 2024 01:18:35 GMT
VOLUME [/znc-data]
# Fri, 21 Jun 2024 01:18:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Fri, 21 Jun 2024 01:18:54 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Fri, 21 Jun 2024 01:18:56 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b717069202c9df255188b3da2ceb8e0099934c053f6ad35d7b1d4a3c5a828105`  
		Last Modified: Fri, 21 Jun 2024 01:19:13 GMT  
		Size: 46.7 MB (46717606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c947365d3b2e0cfa6c01f35f407e956da7fb26c9799caf1b6ff4e033ad05703`  
		Last Modified: Fri, 21 Jun 2024 01:19:07 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16be3569b437bf90039fb1cd138bf463a75a3330f21f96c70fbe0e93e25cd39`  
		Last Modified: Fri, 21 Jun 2024 01:19:07 GMT  
		Size: 753.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:722d0fc7ba2dc4ac24819776b1ced05e004e975698dbddf60c268e7f0c6f69f8`  
		Last Modified: Fri, 21 Jun 2024 01:19:33 GMT  
		Size: 102.4 MB (102376167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc65fa1f3291d0b58bdf715c103c87197d7b74a4efed4a9f43a5a00829ccae3`  
		Last Modified: Fri, 21 Jun 2024 01:19:22 GMT  
		Size: 330.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
