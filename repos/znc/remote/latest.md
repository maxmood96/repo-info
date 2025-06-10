## `znc:latest`

```console
$ docker pull znc@sha256:8678ec544aae22d8fd5773319a141e3d921e2522b6b77413b9b422a2eea136c2
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
$ docker pull znc@sha256:1a21f01ec6d840a7d4667a444c5980adfea20616f764522244eb5f1d95e4bf34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.3 MB (169327033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0b38f1139c032fa67acbe51de4dfbdf32c3816017e8525fcbdd2d7c9702205a`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
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
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e1821654371e9782c93b6f44ac62caa41ebb3a4b580f1f4c0f5dfe1eb53abf9`  
		Last Modified: Mon, 09 Jun 2025 22:13:34 GMT  
		Size: 46.0 MB (45998369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29bdc0575955154fe20b2d1394240a1b66db06f0e06ef42e9e268091d5001d9e`  
		Last Modified: Mon, 09 Jun 2025 22:13:31 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d04261b36ac1b724af051791d3751d15494367540e899a9f0b8cccb1082a1f3`  
		Last Modified: Mon, 09 Jun 2025 22:13:32 GMT  
		Size: 748.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2addc86f68fa53c37b0e45329c651000fb6c5080a0720fabc6cca1277a31934`  
		Last Modified: Mon, 09 Jun 2025 23:07:23 GMT  
		Size: 119.5 MB (119530566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9d01ad1818e7e7bc71227f5ece6f468349137191ec391918f7cdfa883b94b7`  
		Last Modified: Mon, 09 Jun 2025 23:07:13 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:3292f55e1dac7c976bfc9650b5b86bb096f5ece0529b5a058a8d75998182c369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6872634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f391504be5e175b953f43ff8f9138d035ab293391a2229dae2d6fd903acdd7`

```dockerfile
```

-	Layers:
	-	`sha256:d46beaa4beb9acf79510a13c67c08e5ac676543de8445ad832bdb174ba521cc1`  
		Last Modified: Tue, 10 Jun 2025 00:35:26 GMT  
		Size: 6.9 MB (6863031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9cfdefeab9583ad3822906ac847fc86671599e4f3a3c252734873aa0c9f81335`  
		Last Modified: Tue, 10 Jun 2025 00:35:26 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:705ceccf932616d2656a58c9b07cb88338ee2d4c84717a438b278bd753d90ba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.6 MB (148642916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7044c17b00c4bde107a5ee0ead9e6ad92f44ba519f1490d9d4fe5f465814fc42`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
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
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3953687ee90083b0e6263a30825f0badb3a8e2f051fac68023e4f5cfc2039f93`  
		Last Modified: Mon, 09 Jun 2025 22:16:57 GMT  
		Size: 44.6 MB (44600790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a35d9bf1c3d48cd2936887d41d7b999e9e1006d7ce335f02959e74213d53de49`  
		Last Modified: Mon, 09 Jun 2025 22:16:53 GMT  
		Size: 170.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be492dcc4119f18213ef5d4e0dc4292cd4c08f5a8e1d1de452f33498dcd5d549`  
		Last Modified: Mon, 09 Jun 2025 22:16:54 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ace0491baf0ba8a98699be3ab88992fd76cdb6296092e6c0d4a20b2638851f`  
		Last Modified: Mon, 09 Jun 2025 23:06:41 GMT  
		Size: 100.5 MB (100539947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ffa02c95013161eeaab866c3eec26d2c48495c6ab0a955c05312a48dbafce2a`  
		Last Modified: Mon, 09 Jun 2025 23:06:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:a7d1481e107686a6ff5222b44fd96955f5c105e9fb033c40b638258c7043d174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:097087e27f42661f7636a669a44700a275d289c835fc0ce97ecbd3c7e867e753`

```dockerfile
```

-	Layers:
	-	`sha256:637e35aa5c9ef5eaf6be3b139a89a098ccf75a95822bdcec506a90f444ee55ca`  
		Last Modified: Tue, 10 Jun 2025 00:35:32 GMT  
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
