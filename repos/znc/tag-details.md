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
$ docker pull znc@sha256:e70b49ac03c413b56275e5072f1004546e38459e1532efc7ec507c18452d670c
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
		Last Modified: Tue, 12 Nov 2024 03:14:23 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9` - linux; arm variant v6

```console
$ docker pull znc@sha256:2d55f24c42a5f0fb2d239def641d050444ffdeec6db12ae20d832a8bf53f4d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140382097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc480be48524ec2c0f1c9602290dabebf0ab6a4e5fcac67d9ce9f338cfe0b5cb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dc53074094bd3ca27945edb8c21f7b9f48b247125cd0e1ca7e7db9dc29319d`  
		Last Modified: Sat, 07 Sep 2024 12:50:23 GMT  
		Size: 45.3 MB (45307730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b231f4639957be0ebee0a0d19b7bf8999a4ad75791df039313e97dd933d57dbb`  
		Last Modified: Sat, 07 Sep 2024 12:50:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809bf0f514073a8305260957ef69ddd676bafb0ca87987a29c9f03b4fc8125af`  
		Last Modified: Sat, 07 Sep 2024 12:50:21 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe2f1090c300c2d46a3a69ac07b9b5e1054202f1229c65e7211ac8d7089e867`  
		Last Modified: Sat, 07 Sep 2024 13:46:57 GMT  
		Size: 91.9 MB (91896722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763da966c4ea32ca06d416319d9b726f308917a3cdfa790e36103a373b4686b6`  
		Last Modified: Sat, 07 Sep 2024 13:46:54 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9` - unknown; unknown

```console
$ docker pull znc@sha256:cde72cd2dc29fc9016ac613865b3c168e50beaa69d13b292ac135b51ff5abeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20524ba55b7eba54fa7d5f7c6e496fdb560baf212b8bf31cbd40b270a967461d`

```dockerfile
```

-	Layers:
	-	`sha256:6c2eefad57b42a0c83c5efb6f228bce0f82f826713ac932c45b973ce2bf78307`  
		Last Modified: Sat, 07 Sep 2024 13:46:54 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:c4b58d259bb54bafb0e5132e9256f6ae2bfe807fa9fcc11a155ca2f5bfc73d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152457206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd60b5af8aa60eee2a7f9e3c83957db4f6d5391a4ee1d21e47e8ac281353da3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70145fd964e6774c2cb8af189ff945951dea59984de44aa529687f5c5f6a829f`  
		Last Modified: Sat, 07 Sep 2024 12:04:30 GMT  
		Size: 46.7 MB (46720511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a0f358b120fc9322ceee96373a6a3e5a4825f26fbcb49c9dea2e7f24c1948`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02787a2b677e7769a5585a18edfac82cd3a571176d9452a0d4f67363a4e85967`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cae74b6e116e7b2c68197896c90403057d8f9566c62462421591395658ccfe`  
		Last Modified: Sat, 07 Sep 2024 14:34:45 GMT  
		Size: 102.4 MB (102376340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5f00494fc42063a63f74bfbb18dc51ca0af94cd1c10ce25df64c9d4d608c98`  
		Last Modified: Sat, 07 Sep 2024 14:34:43 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9` - unknown; unknown

```console
$ docker pull znc@sha256:b985a8e2c9ed1ca33d724077baf615613bdec9133d277b014225f7d1038dd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed04fad3a9d32ec622c9daad3b926f24d050ec960e3b9ee35bbc22c289b7248`

```dockerfile
```

-	Layers:
	-	`sha256:505c2940f75a77b8e0e498d3d73ec04105ebac1887aff6ae98e1205cc6a6c22a`  
		Last Modified: Sat, 07 Sep 2024 14:34:43 GMT  
		Size: 6.8 MB (6790364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5e36c1bdcbffe10cf877969eb895850fffc02a681070b44a08ba4888e38d75`  
		Last Modified: Sat, 07 Sep 2024 14:34:42 GMT  
		Size: 10.0 KB (9955 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.9-slim`

```console
$ docker pull znc@sha256:f66270fb98b5bc498314f859ce3e36559841efe8678cd97ce4b20ed0e0b2a826
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
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
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
$ docker pull znc@sha256:dd63bfb838653cff7cea10439d63bb6210ac5c32a3f5073cbebae3cf45c1b41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50080535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e77264654e51a1da24aa3798ecc249fa0a53a6bc314c8de5ef88da6e3e80d82`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70145fd964e6774c2cb8af189ff945951dea59984de44aa529687f5c5f6a829f`  
		Last Modified: Sat, 07 Sep 2024 12:04:30 GMT  
		Size: 46.7 MB (46720511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a0f358b120fc9322ceee96373a6a3e5a4825f26fbcb49c9dea2e7f24c1948`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02787a2b677e7769a5585a18edfac82cd3a571176d9452a0d4f67363a4e85967`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9-slim` - unknown; unknown

```console
$ docker pull znc@sha256:c8a0718343e4da7417490f4d2494e4a6eb590d5b5564499703a83cb10e95b76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcad76fd4c6ad6cb0f8fb037258a6200beb9e4ffc8de637c977172f0dad59b31`

```dockerfile
```

-	Layers:
	-	`sha256:bdf90c3b7176200907824a585f7a641ed160e6e6b5acff036635659137614735`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 2.1 MB (2138546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7730aa24445bf24954e63873575c1b37fb40fba9a7c0cf0c343556b5dedeef`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 14.1 KB (14081 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.9.1`

```console
$ docker pull znc@sha256:e70b49ac03c413b56275e5072f1004546e38459e1532efc7ec507c18452d670c
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
		Last Modified: Tue, 12 Nov 2024 03:14:23 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1` - linux; arm variant v6

```console
$ docker pull znc@sha256:2d55f24c42a5f0fb2d239def641d050444ffdeec6db12ae20d832a8bf53f4d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140382097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc480be48524ec2c0f1c9602290dabebf0ab6a4e5fcac67d9ce9f338cfe0b5cb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dc53074094bd3ca27945edb8c21f7b9f48b247125cd0e1ca7e7db9dc29319d`  
		Last Modified: Sat, 07 Sep 2024 12:50:23 GMT  
		Size: 45.3 MB (45307730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b231f4639957be0ebee0a0d19b7bf8999a4ad75791df039313e97dd933d57dbb`  
		Last Modified: Sat, 07 Sep 2024 12:50:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809bf0f514073a8305260957ef69ddd676bafb0ca87987a29c9f03b4fc8125af`  
		Last Modified: Sat, 07 Sep 2024 12:50:21 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe2f1090c300c2d46a3a69ac07b9b5e1054202f1229c65e7211ac8d7089e867`  
		Last Modified: Sat, 07 Sep 2024 13:46:57 GMT  
		Size: 91.9 MB (91896722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763da966c4ea32ca06d416319d9b726f308917a3cdfa790e36103a373b4686b6`  
		Last Modified: Sat, 07 Sep 2024 13:46:54 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1` - unknown; unknown

```console
$ docker pull znc@sha256:cde72cd2dc29fc9016ac613865b3c168e50beaa69d13b292ac135b51ff5abeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20524ba55b7eba54fa7d5f7c6e496fdb560baf212b8bf31cbd40b270a967461d`

```dockerfile
```

-	Layers:
	-	`sha256:6c2eefad57b42a0c83c5efb6f228bce0f82f826713ac932c45b973ce2bf78307`  
		Last Modified: Sat, 07 Sep 2024 13:46:54 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:c4b58d259bb54bafb0e5132e9256f6ae2bfe807fa9fcc11a155ca2f5bfc73d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152457206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd60b5af8aa60eee2a7f9e3c83957db4f6d5391a4ee1d21e47e8ac281353da3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70145fd964e6774c2cb8af189ff945951dea59984de44aa529687f5c5f6a829f`  
		Last Modified: Sat, 07 Sep 2024 12:04:30 GMT  
		Size: 46.7 MB (46720511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a0f358b120fc9322ceee96373a6a3e5a4825f26fbcb49c9dea2e7f24c1948`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02787a2b677e7769a5585a18edfac82cd3a571176d9452a0d4f67363a4e85967`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cae74b6e116e7b2c68197896c90403057d8f9566c62462421591395658ccfe`  
		Last Modified: Sat, 07 Sep 2024 14:34:45 GMT  
		Size: 102.4 MB (102376340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5f00494fc42063a63f74bfbb18dc51ca0af94cd1c10ce25df64c9d4d608c98`  
		Last Modified: Sat, 07 Sep 2024 14:34:43 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1` - unknown; unknown

```console
$ docker pull znc@sha256:b985a8e2c9ed1ca33d724077baf615613bdec9133d277b014225f7d1038dd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed04fad3a9d32ec622c9daad3b926f24d050ec960e3b9ee35bbc22c289b7248`

```dockerfile
```

-	Layers:
	-	`sha256:505c2940f75a77b8e0e498d3d73ec04105ebac1887aff6ae98e1205cc6a6c22a`  
		Last Modified: Sat, 07 Sep 2024 14:34:43 GMT  
		Size: 6.8 MB (6790364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5e36c1bdcbffe10cf877969eb895850fffc02a681070b44a08ba4888e38d75`  
		Last Modified: Sat, 07 Sep 2024 14:34:42 GMT  
		Size: 10.0 KB (9955 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.9.1-slim`

```console
$ docker pull znc@sha256:f66270fb98b5bc498314f859ce3e36559841efe8678cd97ce4b20ed0e0b2a826
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
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
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
$ docker pull znc@sha256:dd63bfb838653cff7cea10439d63bb6210ac5c32a3f5073cbebae3cf45c1b41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50080535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e77264654e51a1da24aa3798ecc249fa0a53a6bc314c8de5ef88da6e3e80d82`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70145fd964e6774c2cb8af189ff945951dea59984de44aa529687f5c5f6a829f`  
		Last Modified: Sat, 07 Sep 2024 12:04:30 GMT  
		Size: 46.7 MB (46720511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a0f358b120fc9322ceee96373a6a3e5a4825f26fbcb49c9dea2e7f24c1948`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02787a2b677e7769a5585a18edfac82cd3a571176d9452a0d4f67363a4e85967`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.9.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:c8a0718343e4da7417490f4d2494e4a6eb590d5b5564499703a83cb10e95b76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcad76fd4c6ad6cb0f8fb037258a6200beb9e4ffc8de637c977172f0dad59b31`

```dockerfile
```

-	Layers:
	-	`sha256:bdf90c3b7176200907824a585f7a641ed160e6e6b5acff036635659137614735`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 2.1 MB (2138546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7730aa24445bf24954e63873575c1b37fb40fba9a7c0cf0c343556b5dedeef`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 14.1 KB (14081 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:latest`

```console
$ docker pull znc@sha256:e70b49ac03c413b56275e5072f1004546e38459e1532efc7ec507c18452d670c
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
		Last Modified: Tue, 12 Nov 2024 03:14:23 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:2d55f24c42a5f0fb2d239def641d050444ffdeec6db12ae20d832a8bf53f4d0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140382097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc480be48524ec2c0f1c9602290dabebf0ab6a4e5fcac67d9ce9f338cfe0b5cb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
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
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65dc53074094bd3ca27945edb8c21f7b9f48b247125cd0e1ca7e7db9dc29319d`  
		Last Modified: Sat, 07 Sep 2024 12:50:23 GMT  
		Size: 45.3 MB (45307730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b231f4639957be0ebee0a0d19b7bf8999a4ad75791df039313e97dd933d57dbb`  
		Last Modified: Sat, 07 Sep 2024 12:50:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809bf0f514073a8305260957ef69ddd676bafb0ca87987a29c9f03b4fc8125af`  
		Last Modified: Sat, 07 Sep 2024 12:50:21 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afe2f1090c300c2d46a3a69ac07b9b5e1054202f1229c65e7211ac8d7089e867`  
		Last Modified: Sat, 07 Sep 2024 13:46:57 GMT  
		Size: 91.9 MB (91896722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763da966c4ea32ca06d416319d9b726f308917a3cdfa790e36103a373b4686b6`  
		Last Modified: Sat, 07 Sep 2024 13:46:54 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:cde72cd2dc29fc9016ac613865b3c168e50beaa69d13b292ac135b51ff5abeed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20524ba55b7eba54fa7d5f7c6e496fdb560baf212b8bf31cbd40b270a967461d`

```dockerfile
```

-	Layers:
	-	`sha256:6c2eefad57b42a0c83c5efb6f228bce0f82f826713ac932c45b973ce2bf78307`  
		Last Modified: Sat, 07 Sep 2024 13:46:54 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:c4b58d259bb54bafb0e5132e9256f6ae2bfe807fa9fcc11a155ca2f5bfc73d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152457206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afd60b5af8aa60eee2a7f9e3c83957db4f6d5391a4ee1d21e47e8ac281353da3`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70145fd964e6774c2cb8af189ff945951dea59984de44aa529687f5c5f6a829f`  
		Last Modified: Sat, 07 Sep 2024 12:04:30 GMT  
		Size: 46.7 MB (46720511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a0f358b120fc9322ceee96373a6a3e5a4825f26fbcb49c9dea2e7f24c1948`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02787a2b677e7769a5585a18edfac82cd3a571176d9452a0d4f67363a4e85967`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2cae74b6e116e7b2c68197896c90403057d8f9566c62462421591395658ccfe`  
		Last Modified: Sat, 07 Sep 2024 14:34:45 GMT  
		Size: 102.4 MB (102376340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5f00494fc42063a63f74bfbb18dc51ca0af94cd1c10ce25df64c9d4d608c98`  
		Last Modified: Sat, 07 Sep 2024 14:34:43 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:b985a8e2c9ed1ca33d724077baf615613bdec9133d277b014225f7d1038dd558
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed04fad3a9d32ec622c9daad3b926f24d050ec960e3b9ee35bbc22c289b7248`

```dockerfile
```

-	Layers:
	-	`sha256:505c2940f75a77b8e0e498d3d73ec04105ebac1887aff6ae98e1205cc6a6c22a`  
		Last Modified: Sat, 07 Sep 2024 14:34:43 GMT  
		Size: 6.8 MB (6790364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f5e36c1bdcbffe10cf877969eb895850fffc02a681070b44a08ba4888e38d75`  
		Last Modified: Sat, 07 Sep 2024 14:34:42 GMT  
		Size: 10.0 KB (9955 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:slim`

```console
$ docker pull znc@sha256:f66270fb98b5bc498314f859ce3e36559841efe8678cd97ce4b20ed0e0b2a826
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
		Last Modified: Tue, 12 Nov 2024 02:15:35 GMT  
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
$ docker pull znc@sha256:dd63bfb838653cff7cea10439d63bb6210ac5c32a3f5073cbebae3cf45c1b41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50080535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e77264654e51a1da24aa3798ecc249fa0a53a6bc314c8de5ef88da6e3e80d82`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
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
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70145fd964e6774c2cb8af189ff945951dea59984de44aa529687f5c5f6a829f`  
		Last Modified: Sat, 07 Sep 2024 12:04:30 GMT  
		Size: 46.7 MB (46720511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a0f358b120fc9322ceee96373a6a3e5a4825f26fbcb49c9dea2e7f24c1948`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02787a2b677e7769a5585a18edfac82cd3a571176d9452a0d4f67363a4e85967`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:c8a0718343e4da7417490f4d2494e4a6eb590d5b5564499703a83cb10e95b76b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcad76fd4c6ad6cb0f8fb037258a6200beb9e4ffc8de637c977172f0dad59b31`

```dockerfile
```

-	Layers:
	-	`sha256:bdf90c3b7176200907824a585f7a641ed160e6e6b5acff036635659137614735`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 2.1 MB (2138546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c7730aa24445bf24954e63873575c1b37fb40fba9a7c0cf0c343556b5dedeef`  
		Last Modified: Sat, 07 Sep 2024 12:04:28 GMT  
		Size: 14.1 KB (14081 bytes)  
		MIME: application/vnd.in-toto+json
