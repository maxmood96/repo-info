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
$ docker pull znc@sha256:81008b6d7450be6d6f7b7f241b19c4cee19fb8f8fc778a22d6076adc53cbf79c
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
$ docker pull znc@sha256:8868ad64ab7e86759d13ea45a4674e82c550ee9faecc2750d81915ff529cf549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160057757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90665877ac61c7cd0625dceb499c8567c6810d237b3f08e07875ffd97a61673c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7255ba75f09422e92f5b03173d4ac2445ed0dc5d63bd5fc7e400f2d8ed14d6f0`  
		Last Modified: Tue, 12 Nov 2024 02:15:36 GMT  
		Size: 48.7 MB (48738616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c47e2e766d93b260dc09d164e658d80c3b49c332212869ed93b16a2b35fb99`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d374b785294f04add930f967130dee87e921997e90dfcaec93d997e438254`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743edbe5fb0489332c63e2a74d1ba362e46fa280399fe6c839520c5b0520edb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 107.9 MB (107898161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2655bbd710e271936146abde038817c9c80c018f35243848de745df0c6b5afa`  
		Last Modified: Tue, 12 Nov 2024 03:14:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9` - unknown; unknown

```console
$ docker pull znc@sha256:d788e8983658a9069f68a71722a4408bc72f01c0ed837b693b9a5b6b2c73fb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6764314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962e4ee36d892f194cf69d833b27c34cd9e1d57d77241e22cdfddba1c832392f`

```dockerfile
```

-	Layers:
	-	`sha256:16dc9e8b49c08a9ea045a229ea8710c95b199e51fca708ec738381b317334519`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 6.8 MB (6754716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:605e398d6a92c631bff1405e86b3dee0c2a9882c81f2106dafcc5d97aad467df`  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9` - linux; arm variant v6

```console
$ docker pull znc@sha256:b76fd7f8b01d4f02f032ddf6f06e4e94606d6f8624389260fd8cc89c3a03377d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142121256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56de870d344896a7aeb8d89d4dc771d60f0df363804fbcda007febbccb79e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27a3f96d29923ef46e08a34814b935b4d1f40bc3836ef2c04cd3a693aaa78ef`  
		Last Modified: Tue, 12 Nov 2024 06:36:14 GMT  
		Size: 47.1 MB (47057236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569fa38966c4810094c11b5f2106ea179b371bb82bc49708e9a5bb6a5858475`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fe78d2155beeb9cdb650cca986261f658b966381489425ff6386b9b62b1962`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cc894f3b365c421b1b71b65a18e5a024a729fbbe9289ca8874910d5d0a26d1`  
		Last Modified: Tue, 12 Nov 2024 16:08:56 GMT  
		Size: 91.9 MB (91886333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d8e039a904d65943c5650f43f5c85a65e4a124a9f51bba4432df8feb4df485`  
		Last Modified: Tue, 12 Nov 2024 16:08:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9` - unknown; unknown

```console
$ docker pull znc@sha256:9a40c5dc5724c7f9530db9d7b563f15d045b7702d62e0f9582abd7b32cd14d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06251646038f4e054cc9281f94a3868125eeee7b6d1f8326b01eafe0ce22cb00`

```dockerfile
```

-	Layers:
	-	`sha256:3273cdb77a81d2ed32ac34a717a943c46e33e10119b18fcc70d83b77a0708052`  
		Last Modified: Tue, 12 Nov 2024 16:08:53 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:735128aeb74225fe8f1d10bfad638b78d64620ebfdc42960fdf0f45608b6f199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154443707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de70f5828de3b30a926fdd89eb3cea98875e374f605eead6e1d37769530d2014`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2efe174d3548884a91aa29a27ea7fb2f28a9140b5f6790ff4fa017b38ea041`  
		Last Modified: Tue, 12 Nov 2024 11:01:19 GMT  
		Size: 48.7 MB (48692583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e294d2e4f62e4a5d05063ca34b3bd9a7ecb119f1d111dd4bc56be49ef689b198`  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e94c1dd8fdbe845a00e0fb1749d09bb9bd2370758ae02f265d1e7a35568c358`  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fe02be43e44e4f106593a660f4aad34a6ad8516ae5e9bb09675cb5286f8e26`  
		Last Modified: Wed, 13 Nov 2024 02:38:16 GMT  
		Size: 102.4 MB (102390625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17059de2064f7ceb4fb5900be50f931bdf7d4a942df9adc104a7f59e5efff504`  
		Last Modified: Wed, 13 Nov 2024 02:38:13 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9` - unknown; unknown

```console
$ docker pull znc@sha256:0d9bdc95d82944d0eda5e9f8b13e9952ea7d8c52dff2cebe71b1b594c83a9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b230fe72a07263dbdab835cec559cafba1b79cf8213f834dd0dedc41e8ef34`

```dockerfile
```

-	Layers:
	-	`sha256:5680fe1aa6243e352e37c64253542d3bb0ed2ddd386c78198699efd89ab0afc9`  
		Last Modified: Wed, 13 Nov 2024 02:38:13 GMT  
		Size: 6.8 MB (6790587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bb48e630b2407925ceb398b656847f1d2edd6f4d44d8da58f75657ff46b7bc4`  
		Last Modified: Wed, 13 Nov 2024 02:38:13 GMT  
		Size: 9.7 KB (9690 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.9-slim`

```console
$ docker pull znc@sha256:c3e05771be0800fd37b2cef41bb3ec85eaff40eb9deb0810325438e6512943e8
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
$ docker pull znc@sha256:84891b367c068f78558f135a12d6da1021bff9e7cf1f621755df85a555361bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52159265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8877daa348f4853d54fd573f431e62fc4af1b904f486525e5c9021a164386e58`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7255ba75f09422e92f5b03173d4ac2445ed0dc5d63bd5fc7e400f2d8ed14d6f0`  
		Last Modified: Tue, 12 Nov 2024 02:15:36 GMT  
		Size: 48.7 MB (48738616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c47e2e766d93b260dc09d164e658d80c3b49c332212869ed93b16a2b35fb99`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d374b785294f04add930f967130dee87e921997e90dfcaec93d997e438254`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9-slim` - unknown; unknown

```console
$ docker pull znc@sha256:6b59288fc7c23245f43bea0db325743d0d3786aaac32d930f89d701a346b4e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21aade788a7e0fbd4d75bd22c883af992181c917e874378c1dfe9a77bfdd362a`

```dockerfile
```

-	Layers:
	-	`sha256:06410eea70beaaa321ab71e30c8cfc5663b7a3ecf80f4b08277efd909e41e763`  
		Size: 2.1 MB (2138640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8e73106c34f624e828feaab045b9f220294ff45319a3370f95ffd2d100eb6f`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 14.0 KB (14026 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:aa1a2d5152b0019a6a47f611b3716313763d3827db519144fa4e55841f71400d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50234591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7877f41260f63e5183b9cbd450abaa747991f1b09501ce6586864e887e810b7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27a3f96d29923ef46e08a34814b935b4d1f40bc3836ef2c04cd3a693aaa78ef`  
		Last Modified: Tue, 12 Nov 2024 06:36:14 GMT  
		Size: 47.1 MB (47057236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569fa38966c4810094c11b5f2106ea179b371bb82bc49708e9a5bb6a5858475`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fe78d2155beeb9cdb650cca986261f658b966381489425ff6386b9b62b1962`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9-slim` - unknown; unknown

```console
$ docker pull znc@sha256:9c52d598192e7341d20061c4763281bb20729fbd43bd9d2e67ec9bbd3571b618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ffd0aafdb677bc279c5532ba4ca8fa39e8379500827b69c62286184a83d67e`

```dockerfile
```

-	Layers:
	-	`sha256:dd3f95e860da7037eb88c524cc5f9fe471158defbcc72a669e0bd06fa9f31885`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:79656c7acc30ed0f7ef05772f8f980c3a0e9586fa49b7ab482c61559962ffcb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52052752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f874e744fdba644af4dc056bbd00d68af8370fbcb45ab601a40bfee3c0668b5c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2efe174d3548884a91aa29a27ea7fb2f28a9140b5f6790ff4fa017b38ea041`  
		Last Modified: Tue, 12 Nov 2024 11:01:19 GMT  
		Size: 48.7 MB (48692583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e294d2e4f62e4a5d05063ca34b3bd9a7ecb119f1d111dd4bc56be49ef689b198`  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e94c1dd8fdbe845a00e0fb1749d09bb9bd2370758ae02f265d1e7a35568c358`  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9-slim` - unknown; unknown

```console
$ docker pull znc@sha256:17ee86d4911c5faf0491ff17a25a65dddeb7e8b2fbd9a10b5dedc1f788f06212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea749328092f4bbcb7680372f9d34e34a6e4bf2711f77e8e95e4d4d0d1ab8ed`

```dockerfile
```

-	Layers:
	-	`sha256:06c41fc48e2b37bc5f8c3476059dd96046eda68b9e108ae329709982a1cbeb86`  
		Last Modified: Tue, 12 Nov 2024 11:01:17 GMT  
		Size: 2.1 MB (2138769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca77749514918e3de88123ff5122ddb63b3ab564eec0def695f592bb1dd7f04`  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.9.1`

```console
$ docker pull znc@sha256:81008b6d7450be6d6f7b7f241b19c4cee19fb8f8fc778a22d6076adc53cbf79c
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
$ docker pull znc@sha256:8868ad64ab7e86759d13ea45a4674e82c550ee9faecc2750d81915ff529cf549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160057757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90665877ac61c7cd0625dceb499c8567c6810d237b3f08e07875ffd97a61673c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7255ba75f09422e92f5b03173d4ac2445ed0dc5d63bd5fc7e400f2d8ed14d6f0`  
		Last Modified: Tue, 12 Nov 2024 02:15:36 GMT  
		Size: 48.7 MB (48738616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c47e2e766d93b260dc09d164e658d80c3b49c332212869ed93b16a2b35fb99`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d374b785294f04add930f967130dee87e921997e90dfcaec93d997e438254`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743edbe5fb0489332c63e2a74d1ba362e46fa280399fe6c839520c5b0520edb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 107.9 MB (107898161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2655bbd710e271936146abde038817c9c80c018f35243848de745df0c6b5afa`  
		Last Modified: Tue, 12 Nov 2024 03:14:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1` - unknown; unknown

```console
$ docker pull znc@sha256:d788e8983658a9069f68a71722a4408bc72f01c0ed837b693b9a5b6b2c73fb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6764314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962e4ee36d892f194cf69d833b27c34cd9e1d57d77241e22cdfddba1c832392f`

```dockerfile
```

-	Layers:
	-	`sha256:16dc9e8b49c08a9ea045a229ea8710c95b199e51fca708ec738381b317334519`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 6.8 MB (6754716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:605e398d6a92c631bff1405e86b3dee0c2a9882c81f2106dafcc5d97aad467df`  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1` - linux; arm variant v6

```console
$ docker pull znc@sha256:b76fd7f8b01d4f02f032ddf6f06e4e94606d6f8624389260fd8cc89c3a03377d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142121256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56de870d344896a7aeb8d89d4dc771d60f0df363804fbcda007febbccb79e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27a3f96d29923ef46e08a34814b935b4d1f40bc3836ef2c04cd3a693aaa78ef`  
		Last Modified: Tue, 12 Nov 2024 06:36:14 GMT  
		Size: 47.1 MB (47057236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569fa38966c4810094c11b5f2106ea179b371bb82bc49708e9a5bb6a5858475`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fe78d2155beeb9cdb650cca986261f658b966381489425ff6386b9b62b1962`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cc894f3b365c421b1b71b65a18e5a024a729fbbe9289ca8874910d5d0a26d1`  
		Last Modified: Tue, 12 Nov 2024 16:08:56 GMT  
		Size: 91.9 MB (91886333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d8e039a904d65943c5650f43f5c85a65e4a124a9f51bba4432df8feb4df485`  
		Last Modified: Tue, 12 Nov 2024 16:08:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1` - unknown; unknown

```console
$ docker pull znc@sha256:9a40c5dc5724c7f9530db9d7b563f15d045b7702d62e0f9582abd7b32cd14d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06251646038f4e054cc9281f94a3868125eeee7b6d1f8326b01eafe0ce22cb00`

```dockerfile
```

-	Layers:
	-	`sha256:3273cdb77a81d2ed32ac34a717a943c46e33e10119b18fcc70d83b77a0708052`  
		Last Modified: Tue, 12 Nov 2024 16:08:53 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:735128aeb74225fe8f1d10bfad638b78d64620ebfdc42960fdf0f45608b6f199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154443707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de70f5828de3b30a926fdd89eb3cea98875e374f605eead6e1d37769530d2014`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2efe174d3548884a91aa29a27ea7fb2f28a9140b5f6790ff4fa017b38ea041`  
		Last Modified: Tue, 12 Nov 2024 11:01:19 GMT  
		Size: 48.7 MB (48692583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e294d2e4f62e4a5d05063ca34b3bd9a7ecb119f1d111dd4bc56be49ef689b198`  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e94c1dd8fdbe845a00e0fb1749d09bb9bd2370758ae02f265d1e7a35568c358`  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fe02be43e44e4f106593a660f4aad34a6ad8516ae5e9bb09675cb5286f8e26`  
		Last Modified: Wed, 13 Nov 2024 02:38:16 GMT  
		Size: 102.4 MB (102390625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17059de2064f7ceb4fb5900be50f931bdf7d4a942df9adc104a7f59e5efff504`  
		Last Modified: Wed, 13 Nov 2024 02:38:13 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1` - unknown; unknown

```console
$ docker pull znc@sha256:0d9bdc95d82944d0eda5e9f8b13e9952ea7d8c52dff2cebe71b1b594c83a9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b230fe72a07263dbdab835cec559cafba1b79cf8213f834dd0dedc41e8ef34`

```dockerfile
```

-	Layers:
	-	`sha256:5680fe1aa6243e352e37c64253542d3bb0ed2ddd386c78198699efd89ab0afc9`  
		Last Modified: Wed, 13 Nov 2024 02:38:13 GMT  
		Size: 6.8 MB (6790587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bb48e630b2407925ceb398b656847f1d2edd6f4d44d8da58f75657ff46b7bc4`  
		Last Modified: Wed, 13 Nov 2024 02:38:13 GMT  
		Size: 9.7 KB (9690 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.9.1-slim`

```console
$ docker pull znc@sha256:c3e05771be0800fd37b2cef41bb3ec85eaff40eb9deb0810325438e6512943e8
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
$ docker pull znc@sha256:84891b367c068f78558f135a12d6da1021bff9e7cf1f621755df85a555361bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52159265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8877daa348f4853d54fd573f431e62fc4af1b904f486525e5c9021a164386e58`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7255ba75f09422e92f5b03173d4ac2445ed0dc5d63bd5fc7e400f2d8ed14d6f0`  
		Last Modified: Tue, 12 Nov 2024 02:15:36 GMT  
		Size: 48.7 MB (48738616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c47e2e766d93b260dc09d164e658d80c3b49c332212869ed93b16a2b35fb99`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d374b785294f04add930f967130dee87e921997e90dfcaec93d997e438254`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:6b59288fc7c23245f43bea0db325743d0d3786aaac32d930f89d701a346b4e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21aade788a7e0fbd4d75bd22c883af992181c917e874378c1dfe9a77bfdd362a`

```dockerfile
```

-	Layers:
	-	`sha256:06410eea70beaaa321ab71e30c8cfc5663b7a3ecf80f4b08277efd909e41e763`  
		Size: 2.1 MB (2138640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8e73106c34f624e828feaab045b9f220294ff45319a3370f95ffd2d100eb6f`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 14.0 KB (14026 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:aa1a2d5152b0019a6a47f611b3716313763d3827db519144fa4e55841f71400d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50234591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7877f41260f63e5183b9cbd450abaa747991f1b09501ce6586864e887e810b7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27a3f96d29923ef46e08a34814b935b4d1f40bc3836ef2c04cd3a693aaa78ef`  
		Last Modified: Tue, 12 Nov 2024 06:36:14 GMT  
		Size: 47.1 MB (47057236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569fa38966c4810094c11b5f2106ea179b371bb82bc49708e9a5bb6a5858475`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fe78d2155beeb9cdb650cca986261f658b966381489425ff6386b9b62b1962`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:9c52d598192e7341d20061c4763281bb20729fbd43bd9d2e67ec9bbd3571b618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ffd0aafdb677bc279c5532ba4ca8fa39e8379500827b69c62286184a83d67e`

```dockerfile
```

-	Layers:
	-	`sha256:dd3f95e860da7037eb88c524cc5f9fe471158defbcc72a669e0bd06fa9f31885`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:79656c7acc30ed0f7ef05772f8f980c3a0e9586fa49b7ab482c61559962ffcb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52052752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f874e744fdba644af4dc056bbd00d68af8370fbcb45ab601a40bfee3c0668b5c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2efe174d3548884a91aa29a27ea7fb2f28a9140b5f6790ff4fa017b38ea041`  
		Last Modified: Tue, 12 Nov 2024 11:01:19 GMT  
		Size: 48.7 MB (48692583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e294d2e4f62e4a5d05063ca34b3bd9a7ecb119f1d111dd4bc56be49ef689b198`  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e94c1dd8fdbe845a00e0fb1749d09bb9bd2370758ae02f265d1e7a35568c358`  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:17ee86d4911c5faf0491ff17a25a65dddeb7e8b2fbd9a10b5dedc1f788f06212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea749328092f4bbcb7680372f9d34e34a6e4bf2711f77e8e95e4d4d0d1ab8ed`

```dockerfile
```

-	Layers:
	-	`sha256:06c41fc48e2b37bc5f8c3476059dd96046eda68b9e108ae329709982a1cbeb86`  
		Last Modified: Tue, 12 Nov 2024 11:01:17 GMT  
		Size: 2.1 MB (2138769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca77749514918e3de88123ff5122ddb63b3ab564eec0def695f592bb1dd7f04`  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:latest`

```console
$ docker pull znc@sha256:81008b6d7450be6d6f7b7f241b19c4cee19fb8f8fc778a22d6076adc53cbf79c
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
$ docker pull znc@sha256:8868ad64ab7e86759d13ea45a4674e82c550ee9faecc2750d81915ff529cf549
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.1 MB (160057757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90665877ac61c7cd0625dceb499c8567c6810d237b3f08e07875ffd97a61673c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7255ba75f09422e92f5b03173d4ac2445ed0dc5d63bd5fc7e400f2d8ed14d6f0`  
		Last Modified: Tue, 12 Nov 2024 02:15:36 GMT  
		Size: 48.7 MB (48738616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c47e2e766d93b260dc09d164e658d80c3b49c332212869ed93b16a2b35fb99`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d374b785294f04add930f967130dee87e921997e90dfcaec93d997e438254`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743edbe5fb0489332c63e2a74d1ba362e46fa280399fe6c839520c5b0520edb3`  
		Last Modified: Tue, 12 Nov 2024 03:14:26 GMT  
		Size: 107.9 MB (107898161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2655bbd710e271936146abde038817c9c80c018f35243848de745df0c6b5afa`  
		Last Modified: Tue, 12 Nov 2024 03:14:23 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:d788e8983658a9069f68a71722a4408bc72f01c0ed837b693b9a5b6b2c73fb60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6764314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:962e4ee36d892f194cf69d833b27c34cd9e1d57d77241e22cdfddba1c832392f`

```dockerfile
```

-	Layers:
	-	`sha256:16dc9e8b49c08a9ea045a229ea8710c95b199e51fca708ec738381b317334519`  
		Last Modified: Tue, 12 Nov 2024 03:14:24 GMT  
		Size: 6.8 MB (6754716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:605e398d6a92c631bff1405e86b3dee0c2a9882c81f2106dafcc5d97aad467df`  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:b76fd7f8b01d4f02f032ddf6f06e4e94606d6f8624389260fd8cc89c3a03377d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142121256 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c56de870d344896a7aeb8d89d4dc771d60f0df363804fbcda007febbccb79e12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27a3f96d29923ef46e08a34814b935b4d1f40bc3836ef2c04cd3a693aaa78ef`  
		Last Modified: Tue, 12 Nov 2024 06:36:14 GMT  
		Size: 47.1 MB (47057236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569fa38966c4810094c11b5f2106ea179b371bb82bc49708e9a5bb6a5858475`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fe78d2155beeb9cdb650cca986261f658b966381489425ff6386b9b62b1962`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03cc894f3b365c421b1b71b65a18e5a024a729fbbe9289ca8874910d5d0a26d1`  
		Last Modified: Tue, 12 Nov 2024 16:08:56 GMT  
		Size: 91.9 MB (91886333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4d8e039a904d65943c5650f43f5c85a65e4a124a9f51bba4432df8feb4df485`  
		Last Modified: Tue, 12 Nov 2024 16:08:54 GMT  
		Size: 332.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:9a40c5dc5724c7f9530db9d7b563f15d045b7702d62e0f9582abd7b32cd14d82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06251646038f4e054cc9281f94a3868125eeee7b6d1f8326b01eafe0ce22cb00`

```dockerfile
```

-	Layers:
	-	`sha256:3273cdb77a81d2ed32ac34a717a943c46e33e10119b18fcc70d83b77a0708052`  
		Last Modified: Tue, 12 Nov 2024 16:08:53 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:735128aeb74225fe8f1d10bfad638b78d64620ebfdc42960fdf0f45608b6f199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.4 MB (154443707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de70f5828de3b30a926fdd89eb3cea98875e374f605eead6e1d37769530d2014`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2efe174d3548884a91aa29a27ea7fb2f28a9140b5f6790ff4fa017b38ea041`  
		Last Modified: Tue, 12 Nov 2024 11:01:19 GMT  
		Size: 48.7 MB (48692583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e294d2e4f62e4a5d05063ca34b3bd9a7ecb119f1d111dd4bc56be49ef689b198`  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e94c1dd8fdbe845a00e0fb1749d09bb9bd2370758ae02f265d1e7a35568c358`  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62fe02be43e44e4f106593a660f4aad34a6ad8516ae5e9bb09675cb5286f8e26`  
		Last Modified: Wed, 13 Nov 2024 02:38:16 GMT  
		Size: 102.4 MB (102390625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17059de2064f7ceb4fb5900be50f931bdf7d4a942df9adc104a7f59e5efff504`  
		Last Modified: Wed, 13 Nov 2024 02:38:13 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:0d9bdc95d82944d0eda5e9f8b13e9952ea7d8c52dff2cebe71b1b594c83a9e03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81b230fe72a07263dbdab835cec559cafba1b79cf8213f834dd0dedc41e8ef34`

```dockerfile
```

-	Layers:
	-	`sha256:5680fe1aa6243e352e37c64253542d3bb0ed2ddd386c78198699efd89ab0afc9`  
		Last Modified: Wed, 13 Nov 2024 02:38:13 GMT  
		Size: 6.8 MB (6790587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bb48e630b2407925ceb398b656847f1d2edd6f4d44d8da58f75657ff46b7bc4`  
		Last Modified: Wed, 13 Nov 2024 02:38:13 GMT  
		Size: 9.7 KB (9690 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:slim`

```console
$ docker pull znc@sha256:c3e05771be0800fd37b2cef41bb3ec85eaff40eb9deb0810325438e6512943e8
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
$ docker pull znc@sha256:84891b367c068f78558f135a12d6da1021bff9e7cf1f621755df85a555361bfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52159265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8877daa348f4853d54fd573f431e62fc4af1b904f486525e5c9021a164386e58`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7255ba75f09422e92f5b03173d4ac2445ed0dc5d63bd5fc7e400f2d8ed14d6f0`  
		Last Modified: Tue, 12 Nov 2024 02:15:36 GMT  
		Size: 48.7 MB (48738616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c47e2e766d93b260dc09d164e658d80c3b49c332212869ed93b16a2b35fb99`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66d374b785294f04add930f967130dee87e921997e90dfcaec93d997e438254`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:6b59288fc7c23245f43bea0db325743d0d3786aaac32d930f89d701a346b4e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21aade788a7e0fbd4d75bd22c883af992181c917e874378c1dfe9a77bfdd362a`

```dockerfile
```

-	Layers:
	-	`sha256:06410eea70beaaa321ab71e30c8cfc5663b7a3ecf80f4b08277efd909e41e763`  
		Size: 2.1 MB (2138640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a8e73106c34f624e828feaab045b9f220294ff45319a3370f95ffd2d100eb6f`  
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
		Size: 14.0 KB (14026 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:aa1a2d5152b0019a6a47f611b3716313763d3827db519144fa4e55841f71400d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50234591 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7877f41260f63e5183b9cbd450abaa747991f1b09501ce6586864e887e810b7`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-armhf.tar.gz / # buildkit
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
	-	`sha256:1962dd3845094270fb16c55729f52e68e09c9fdecbe06ccfa89e981fa679172d`  
		Last Modified: Mon, 09 Sep 2024 07:03:19 GMT  
		Size: 3.2 MB (3176432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b27a3f96d29923ef46e08a34814b935b4d1f40bc3836ef2c04cd3a693aaa78ef`  
		Last Modified: Tue, 12 Nov 2024 06:36:14 GMT  
		Size: 47.1 MB (47057236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0569fa38966c4810094c11b5f2106ea179b371bb82bc49708e9a5bb6a5858475`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7fe78d2155beeb9cdb650cca986261f658b966381489425ff6386b9b62b1962`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:9c52d598192e7341d20061c4763281bb20729fbd43bd9d2e67ec9bbd3571b618
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ffd0aafdb677bc279c5532ba4ca8fa39e8379500827b69c62286184a83d67e`

```dockerfile
```

-	Layers:
	-	`sha256:dd3f95e860da7037eb88c524cc5f9fe471158defbcc72a669e0bd06fa9f31885`  
		Last Modified: Tue, 12 Nov 2024 06:36:12 GMT  
		Size: 13.9 KB (13878 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:79656c7acc30ed0f7ef05772f8f980c3a0e9586fa49b7ab482c61559962ffcb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52052752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f874e744fdba644af4dc056bbd00d68af8370fbcb45ab601a40bfee3c0668b5c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a2efe174d3548884a91aa29a27ea7fb2f28a9140b5f6790ff4fa017b38ea041`  
		Last Modified: Tue, 12 Nov 2024 11:01:19 GMT  
		Size: 48.7 MB (48692583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e294d2e4f62e4a5d05063ca34b3bd9a7ecb119f1d111dd4bc56be49ef689b198`  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e94c1dd8fdbe845a00e0fb1749d09bb9bd2370758ae02f265d1e7a35568c358`  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:17ee86d4911c5faf0491ff17a25a65dddeb7e8b2fbd9a10b5dedc1f788f06212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ea749328092f4bbcb7680372f9d34e34a6e4bf2711f77e8e95e4d4d0d1ab8ed`

```dockerfile
```

-	Layers:
	-	`sha256:06c41fc48e2b37bc5f8c3476059dd96046eda68b9e108ae329709982a1cbeb86`  
		Last Modified: Tue, 12 Nov 2024 11:01:17 GMT  
		Size: 2.1 MB (2138769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ca77749514918e3de88123ff5122ddb63b3ab564eec0def695f592bb1dd7f04`  
		Size: 14.1 KB (14118 bytes)  
		MIME: application/vnd.in-toto+json
