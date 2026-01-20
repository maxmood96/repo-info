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
$ docker pull znc@sha256:721e444f9adc064119a6ec044afeb7d734613e8f7c604c2362b2e13664abae7a
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
$ docker pull znc@sha256:93b9b50d78bb617b6a8b1e829b8355647ecb813d9361af65a9d834ca68228cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169358313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6264ea21095b9f70d25dd704a6e8ebf31e4feee090dab5d91b58c6cc0e5d5f12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3506abfd78a36c30c23fe01f0c3ab62436212438294a0da94c8a15913326e030`  
		Last Modified: Wed, 08 Oct 2025 23:01:34 GMT  
		Size: 46.0 MB (46020467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651980d24865ee4f19fa471fbeed8f6ba65e8b7cf4b242999fc0c0b130abdee`  
		Last Modified: Mon, 08 Dec 2025 01:27:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7bbf12514d955bf730d0d365597fa448546c362e4120066bc07f0c079d2bbf`  
		Last Modified: Wed, 08 Oct 2025 23:01:32 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bf880348701f083008954ed278be282273a8e45fc68f720a1ed33e0177d60e`  
		Last Modified: Wed, 08 Oct 2025 23:37:19 GMT  
		Size: 119.5 MB (119534142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca864bafd665ba0480dd125ec1173a1207a65881bd252e8ef1f65fc135d8ec55`  
		Last Modified: Mon, 08 Dec 2025 01:27:27 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:c0cc87c7e7445142436ce99ec0c7f0aef44150775985a579afe163bdf5972e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6870705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06630f48b4cf4448e8d27d292c76a34dc8334b4652a0323a06b366cd75e71e73`

```dockerfile
```

-	Layers:
	-	`sha256:1124971e4e1662715a341504bc5cbb9a255299e1835fd9d1ddfbcd5b7ca57896`  
		Last Modified: Mon, 08 Dec 2025 11:54:03 GMT  
		Size: 6.9 MB (6861102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2605cf507fae06d7a63af0aca531bdba2ed51da86d6d2fee2b58ee343cdde1`  
		Last Modified: Wed, 08 Oct 2025 23:37:16 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm variant v6

```console
$ docker pull znc@sha256:405b85f6079b068d42e043105a049660fc1a7c8acac5baf3fdafb2f2c8b013b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148651441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae6033037fc5e121b9aa07180a3d87cbe57d3a0bc1c0d3f5ad99ea1a6c1a644`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840fec67135c40d32802946fc5362557e770be7653ca7360ea7070ab00fc998`  
		Last Modified: Wed, 08 Oct 2025 22:14:21 GMT  
		Size: 44.6 MB (44605106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c3022b2b83a72e01be3a371b41b75f14cc4ca6477a7acb11833eed902ae83`  
		Last Modified: Tue, 16 Dec 2025 14:28:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f63e8f4811c752e213827a9a95c65b0becdc1370ff48a07652a48776cdc5a`  
		Last Modified: Tue, 16 Dec 2025 14:28:33 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf49085a15491c788cf41a870e124304a09d125d3f0839052a153c2bd16a32c`  
		Last Modified: Wed, 08 Oct 2025 23:34:30 GMT  
		Size: 100.5 MB (100541003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccde0cf2e46c778ef26b4761fe3a54e1c1571395c28b9805f58725a36510abd`  
		Last Modified: Tue, 16 Dec 2025 14:28:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:1f7550ab101b3755e96e9eaf1956fa30a2f29f57b69aca77a983dfed071ea24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69397ea70fd15259dfa76a75308cb78deefcece9b8751d9ba145e4302939e894`

```dockerfile
```

-	Layers:
	-	`sha256:8aedb537f312316ca919e4d1e8087436f057cd8b0fb340c9699472182a3dd95f`  
		Last Modified: Wed, 08 Oct 2025 23:34:28 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:fcd8a04d2b8010a2c634b3b12454f83307bd4c815e857a9dd68591beee213a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163116328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee44987d8c8772780c28b7d14120451bee646b77eaddb79f9ce126a058af64d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec5fdc4fb497bea03514de3252130b7697ae2993a729ad8de1c9d778513bc24`  
		Last Modified: Wed, 08 Oct 2025 21:49:32 GMT  
		Size: 45.8 MB (45813795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa523922045723fa3792824ea44631401bb773284938e53b5b27dda2041376b3`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c90f7c9f8a7f5db7344e75bb64578f0b7b30439d01bdbc5c15e62833526056`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46deafa01e803acc346d7c558f432a758a4b7f99be4488fee34016ada71aa24`  
		Last Modified: Thu, 11 Dec 2025 18:06:18 GMT  
		Size: 113.2 MB (113163213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a60b66bd1d2b3a7c602cecc458a50bd3573492a27ea09e09fdd72ea434edb6`  
		Last Modified: Wed, 08 Oct 2025 22:56:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10` - unknown; unknown

```console
$ docker pull znc@sha256:b0d8e9b11d859e9cc8d4d23000574a77b0f2c0b892e92cd5daed2c02051408d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12533375389cd0ff941eec25254d6991119aa8600f1fb19be618de3c41ce93e0`

```dockerfile
```

-	Layers:
	-	`sha256:13cd7afefce47e2035fe8bbd34e1770dc422f824d930ce7d3fb988ebcdd013de`  
		Last Modified: Tue, 16 Dec 2025 11:31:26 GMT  
		Size: 6.9 MB (6940526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31770e469053bbce11b9337d3196c31a04fb515ee4413415df1358e4c87bb68`  
		Last Modified: Tue, 16 Dec 2025 11:31:24 GMT  
		Size: 9.7 KB (9695 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10-slim`

```console
$ docker pull znc@sha256:124c37d7fe8dffd345fc1e1258b5a589734e37eebbcb7698d53597863d2180de
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
$ docker pull znc@sha256:fae5167c8a61d5fbd49062bc8dec1c91dfa785bde38c7bd097c7de5b739e0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49823841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05117b24a815bf428045299e145a8d1d9a6134d6354c413d0e649b85246a1e23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3506abfd78a36c30c23fe01f0c3ab62436212438294a0da94c8a15913326e030`  
		Last Modified: Wed, 08 Oct 2025 23:01:34 GMT  
		Size: 46.0 MB (46020467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651980d24865ee4f19fa471fbeed8f6ba65e8b7cf4b242999fc0c0b130abdee`  
		Last Modified: Mon, 08 Dec 2025 01:27:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7bbf12514d955bf730d0d365597fa448546c362e4120066bc07f0c079d2bbf`  
		Last Modified: Wed, 08 Oct 2025 23:01:32 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:75d996fa50ca858ca2021215b43c083759ff2e81688ab94d54285e2dcdd3d6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28eeb49cc3fa631f14727ec0292593ee7c0a943987ec9993f2f9dbeddd0e17c9`

```dockerfile
```

-	Layers:
	-	`sha256:621f94726525728c0999a31ebf4c4ec1d00c759f8a5c86d9c87e2761c1634637`  
		Last Modified: Tue, 09 Dec 2025 08:36:40 GMT  
		Size: 1.8 MB (1752770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d37d5e7d20698fe7532c6e3dbfdc07892d94429b4f25c837f87ed0a101918f`  
		Last Modified: Tue, 09 Dec 2025 08:36:39 GMT  
		Size: 14.0 KB (14031 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:2fe48e75462242a7ede2a1c0c348310571f7ee23542931efeec97b8e3c0100ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48110107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee93bff90c32e17f3a74c25ea264399ec27ac3de7397a010a7cfa58c571a44e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840fec67135c40d32802946fc5362557e770be7653ca7360ea7070ab00fc998`  
		Last Modified: Wed, 08 Oct 2025 22:14:21 GMT  
		Size: 44.6 MB (44605106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c3022b2b83a72e01be3a371b41b75f14cc4ca6477a7acb11833eed902ae83`  
		Last Modified: Tue, 16 Dec 2025 14:28:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f63e8f4811c752e213827a9a95c65b0becdc1370ff48a07652a48776cdc5a`  
		Last Modified: Tue, 16 Dec 2025 14:28:33 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:9a11b18474f484361d568e3b1b4c215ac13ecb24171b20aabeb73ec222f8b35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f54bec2703401d236b520cbfcf642a219416fc6c2a15932d03610cb33d56e7`

```dockerfile
```

-	Layers:
	-	`sha256:143fbc029c2a24a9c8fd8ca6c25863b6892d267ba445da0456dd0765836aaca7`  
		Last Modified: Wed, 08 Oct 2025 22:14:20 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:14a1ba6341c42a9df7403e471dc85fa6c34bb7c06fae1f18cfee2552e8c1b55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49952785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f78b8c7f9677ac9a7921bf9124121f0f3b0d9a4be01d1a46585dc605c99eb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec5fdc4fb497bea03514de3252130b7697ae2993a729ad8de1c9d778513bc24`  
		Last Modified: Wed, 08 Oct 2025 21:49:32 GMT  
		Size: 45.8 MB (45813795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa523922045723fa3792824ea44631401bb773284938e53b5b27dda2041376b3`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c90f7c9f8a7f5db7344e75bb64578f0b7b30439d01bdbc5c15e62833526056`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10-slim` - unknown; unknown

```console
$ docker pull znc@sha256:4a900b3cbf481a15ff4c53094629589ad021553aefef1004ebd3b697390f6079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1767022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7058b82b91838ebfacf5853086642932ba146f2ad05fcc8ab274a6a991eb12`

```dockerfile
```

-	Layers:
	-	`sha256:5876732d2e3a5d3f9c22b939b59b950404a086aa77605eb56873e874bc934a47`  
		Last Modified: Wed, 08 Oct 2025 21:49:31 GMT  
		Size: 1.8 MB (1752900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e302684a02e42366864e17b224123f7d91874878390a786b63b04aa66cdd40`  
		Last Modified: Wed, 10 Dec 2025 23:05:19 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.1`

```console
$ docker pull znc@sha256:721e444f9adc064119a6ec044afeb7d734613e8f7c604c2362b2e13664abae7a
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
$ docker pull znc@sha256:93b9b50d78bb617b6a8b1e829b8355647ecb813d9361af65a9d834ca68228cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169358313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6264ea21095b9f70d25dd704a6e8ebf31e4feee090dab5d91b58c6cc0e5d5f12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3506abfd78a36c30c23fe01f0c3ab62436212438294a0da94c8a15913326e030`  
		Last Modified: Wed, 08 Oct 2025 23:01:34 GMT  
		Size: 46.0 MB (46020467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651980d24865ee4f19fa471fbeed8f6ba65e8b7cf4b242999fc0c0b130abdee`  
		Last Modified: Mon, 08 Dec 2025 01:27:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7bbf12514d955bf730d0d365597fa448546c362e4120066bc07f0c079d2bbf`  
		Last Modified: Wed, 08 Oct 2025 23:01:32 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bf880348701f083008954ed278be282273a8e45fc68f720a1ed33e0177d60e`  
		Last Modified: Wed, 08 Oct 2025 23:37:19 GMT  
		Size: 119.5 MB (119534142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca864bafd665ba0480dd125ec1173a1207a65881bd252e8ef1f65fc135d8ec55`  
		Last Modified: Mon, 08 Dec 2025 01:27:27 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1` - unknown; unknown

```console
$ docker pull znc@sha256:c0cc87c7e7445142436ce99ec0c7f0aef44150775985a579afe163bdf5972e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6870705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06630f48b4cf4448e8d27d292c76a34dc8334b4652a0323a06b366cd75e71e73`

```dockerfile
```

-	Layers:
	-	`sha256:1124971e4e1662715a341504bc5cbb9a255299e1835fd9d1ddfbcd5b7ca57896`  
		Last Modified: Mon, 08 Dec 2025 11:54:03 GMT  
		Size: 6.9 MB (6861102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2605cf507fae06d7a63af0aca531bdba2ed51da86d6d2fee2b58ee343cdde1`  
		Last Modified: Wed, 08 Oct 2025 23:37:16 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1` - linux; arm variant v6

```console
$ docker pull znc@sha256:405b85f6079b068d42e043105a049660fc1a7c8acac5baf3fdafb2f2c8b013b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148651441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae6033037fc5e121b9aa07180a3d87cbe57d3a0bc1c0d3f5ad99ea1a6c1a644`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840fec67135c40d32802946fc5362557e770be7653ca7360ea7070ab00fc998`  
		Last Modified: Wed, 08 Oct 2025 22:14:21 GMT  
		Size: 44.6 MB (44605106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c3022b2b83a72e01be3a371b41b75f14cc4ca6477a7acb11833eed902ae83`  
		Last Modified: Tue, 16 Dec 2025 14:28:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f63e8f4811c752e213827a9a95c65b0becdc1370ff48a07652a48776cdc5a`  
		Last Modified: Tue, 16 Dec 2025 14:28:33 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf49085a15491c788cf41a870e124304a09d125d3f0839052a153c2bd16a32c`  
		Last Modified: Wed, 08 Oct 2025 23:34:30 GMT  
		Size: 100.5 MB (100541003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccde0cf2e46c778ef26b4761fe3a54e1c1571395c28b9805f58725a36510abd`  
		Last Modified: Tue, 16 Dec 2025 14:28:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1` - unknown; unknown

```console
$ docker pull znc@sha256:1f7550ab101b3755e96e9eaf1956fa30a2f29f57b69aca77a983dfed071ea24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69397ea70fd15259dfa76a75308cb78deefcece9b8751d9ba145e4302939e894`

```dockerfile
```

-	Layers:
	-	`sha256:8aedb537f312316ca919e4d1e8087436f057cd8b0fb340c9699472182a3dd95f`  
		Last Modified: Wed, 08 Oct 2025 23:34:28 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:fcd8a04d2b8010a2c634b3b12454f83307bd4c815e857a9dd68591beee213a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163116328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee44987d8c8772780c28b7d14120451bee646b77eaddb79f9ce126a058af64d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec5fdc4fb497bea03514de3252130b7697ae2993a729ad8de1c9d778513bc24`  
		Last Modified: Wed, 08 Oct 2025 21:49:32 GMT  
		Size: 45.8 MB (45813795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa523922045723fa3792824ea44631401bb773284938e53b5b27dda2041376b3`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c90f7c9f8a7f5db7344e75bb64578f0b7b30439d01bdbc5c15e62833526056`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46deafa01e803acc346d7c558f432a758a4b7f99be4488fee34016ada71aa24`  
		Last Modified: Thu, 11 Dec 2025 18:06:18 GMT  
		Size: 113.2 MB (113163213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a60b66bd1d2b3a7c602cecc458a50bd3573492a27ea09e09fdd72ea434edb6`  
		Last Modified: Wed, 08 Oct 2025 22:56:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1` - unknown; unknown

```console
$ docker pull znc@sha256:b0d8e9b11d859e9cc8d4d23000574a77b0f2c0b892e92cd5daed2c02051408d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12533375389cd0ff941eec25254d6991119aa8600f1fb19be618de3c41ce93e0`

```dockerfile
```

-	Layers:
	-	`sha256:13cd7afefce47e2035fe8bbd34e1770dc422f824d930ce7d3fb988ebcdd013de`  
		Last Modified: Tue, 16 Dec 2025 11:31:26 GMT  
		Size: 6.9 MB (6940526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31770e469053bbce11b9337d3196c31a04fb515ee4413415df1358e4c87bb68`  
		Last Modified: Tue, 16 Dec 2025 11:31:24 GMT  
		Size: 9.7 KB (9695 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:1.10.1-slim`

```console
$ docker pull znc@sha256:124c37d7fe8dffd345fc1e1258b5a589734e37eebbcb7698d53597863d2180de
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
$ docker pull znc@sha256:fae5167c8a61d5fbd49062bc8dec1c91dfa785bde38c7bd097c7de5b739e0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49823841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05117b24a815bf428045299e145a8d1d9a6134d6354c413d0e649b85246a1e23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3506abfd78a36c30c23fe01f0c3ab62436212438294a0da94c8a15913326e030`  
		Last Modified: Wed, 08 Oct 2025 23:01:34 GMT  
		Size: 46.0 MB (46020467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651980d24865ee4f19fa471fbeed8f6ba65e8b7cf4b242999fc0c0b130abdee`  
		Last Modified: Mon, 08 Dec 2025 01:27:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7bbf12514d955bf730d0d365597fa448546c362e4120066bc07f0c079d2bbf`  
		Last Modified: Wed, 08 Oct 2025 23:01:32 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:75d996fa50ca858ca2021215b43c083759ff2e81688ab94d54285e2dcdd3d6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28eeb49cc3fa631f14727ec0292593ee7c0a943987ec9993f2f9dbeddd0e17c9`

```dockerfile
```

-	Layers:
	-	`sha256:621f94726525728c0999a31ebf4c4ec1d00c759f8a5c86d9c87e2761c1634637`  
		Last Modified: Tue, 09 Dec 2025 08:36:40 GMT  
		Size: 1.8 MB (1752770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d37d5e7d20698fe7532c6e3dbfdc07892d94429b4f25c837f87ed0a101918f`  
		Last Modified: Tue, 09 Dec 2025 08:36:39 GMT  
		Size: 14.0 KB (14031 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:2fe48e75462242a7ede2a1c0c348310571f7ee23542931efeec97b8e3c0100ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48110107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee93bff90c32e17f3a74c25ea264399ec27ac3de7397a010a7cfa58c571a44e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840fec67135c40d32802946fc5362557e770be7653ca7360ea7070ab00fc998`  
		Last Modified: Wed, 08 Oct 2025 22:14:21 GMT  
		Size: 44.6 MB (44605106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c3022b2b83a72e01be3a371b41b75f14cc4ca6477a7acb11833eed902ae83`  
		Last Modified: Tue, 16 Dec 2025 14:28:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f63e8f4811c752e213827a9a95c65b0becdc1370ff48a07652a48776cdc5a`  
		Last Modified: Tue, 16 Dec 2025 14:28:33 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:9a11b18474f484361d568e3b1b4c215ac13ecb24171b20aabeb73ec222f8b35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f54bec2703401d236b520cbfcf642a219416fc6c2a15932d03610cb33d56e7`

```dockerfile
```

-	Layers:
	-	`sha256:143fbc029c2a24a9c8fd8ca6c25863b6892d267ba445da0456dd0765836aaca7`  
		Last Modified: Wed, 08 Oct 2025 22:14:20 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.10.1-slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:14a1ba6341c42a9df7403e471dc85fa6c34bb7c06fae1f18cfee2552e8c1b55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49952785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f78b8c7f9677ac9a7921bf9124121f0f3b0d9a4be01d1a46585dc605c99eb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec5fdc4fb497bea03514de3252130b7697ae2993a729ad8de1c9d778513bc24`  
		Last Modified: Wed, 08 Oct 2025 21:49:32 GMT  
		Size: 45.8 MB (45813795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa523922045723fa3792824ea44631401bb773284938e53b5b27dda2041376b3`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c90f7c9f8a7f5db7344e75bb64578f0b7b30439d01bdbc5c15e62833526056`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:1.10.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:4a900b3cbf481a15ff4c53094629589ad021553aefef1004ebd3b697390f6079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1767022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7058b82b91838ebfacf5853086642932ba146f2ad05fcc8ab274a6a991eb12`

```dockerfile
```

-	Layers:
	-	`sha256:5876732d2e3a5d3f9c22b939b59b950404a086aa77605eb56873e874bc934a47`  
		Last Modified: Wed, 08 Oct 2025 21:49:31 GMT  
		Size: 1.8 MB (1752900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e302684a02e42366864e17b224123f7d91874878390a786b63b04aa66cdd40`  
		Last Modified: Wed, 10 Dec 2025 23:05:19 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:latest`

```console
$ docker pull znc@sha256:721e444f9adc064119a6ec044afeb7d734613e8f7c604c2362b2e13664abae7a
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
$ docker pull znc@sha256:93b9b50d78bb617b6a8b1e829b8355647ecb813d9361af65a9d834ca68228cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **169.4 MB (169358313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6264ea21095b9f70d25dd704a6e8ebf31e4feee090dab5d91b58c6cc0e5d5f12`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3506abfd78a36c30c23fe01f0c3ab62436212438294a0da94c8a15913326e030`  
		Last Modified: Wed, 08 Oct 2025 23:01:34 GMT  
		Size: 46.0 MB (46020467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651980d24865ee4f19fa471fbeed8f6ba65e8b7cf4b242999fc0c0b130abdee`  
		Last Modified: Mon, 08 Dec 2025 01:27:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7bbf12514d955bf730d0d365597fa448546c362e4120066bc07f0c079d2bbf`  
		Last Modified: Wed, 08 Oct 2025 23:01:32 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3bf880348701f083008954ed278be282273a8e45fc68f720a1ed33e0177d60e`  
		Last Modified: Wed, 08 Oct 2025 23:37:19 GMT  
		Size: 119.5 MB (119534142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca864bafd665ba0480dd125ec1173a1207a65881bd252e8ef1f65fc135d8ec55`  
		Last Modified: Mon, 08 Dec 2025 01:27:27 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:c0cc87c7e7445142436ce99ec0c7f0aef44150775985a579afe163bdf5972e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6870705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06630f48b4cf4448e8d27d292c76a34dc8334b4652a0323a06b366cd75e71e73`

```dockerfile
```

-	Layers:
	-	`sha256:1124971e4e1662715a341504bc5cbb9a255299e1835fd9d1ddfbcd5b7ca57896`  
		Last Modified: Mon, 08 Dec 2025 11:54:03 GMT  
		Size: 6.9 MB (6861102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2605cf507fae06d7a63af0aca531bdba2ed51da86d6d2fee2b58ee343cdde1`  
		Last Modified: Wed, 08 Oct 2025 23:37:16 GMT  
		Size: 9.6 KB (9603 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:405b85f6079b068d42e043105a049660fc1a7c8acac5baf3fdafb2f2c8b013b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.7 MB (148651441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae6033037fc5e121b9aa07180a3d87cbe57d3a0bc1c0d3f5ad99ea1a6c1a644`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840fec67135c40d32802946fc5362557e770be7653ca7360ea7070ab00fc998`  
		Last Modified: Wed, 08 Oct 2025 22:14:21 GMT  
		Size: 44.6 MB (44605106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c3022b2b83a72e01be3a371b41b75f14cc4ca6477a7acb11833eed902ae83`  
		Last Modified: Tue, 16 Dec 2025 14:28:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f63e8f4811c752e213827a9a95c65b0becdc1370ff48a07652a48776cdc5a`  
		Last Modified: Tue, 16 Dec 2025 14:28:33 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf49085a15491c788cf41a870e124304a09d125d3f0839052a153c2bd16a32c`  
		Last Modified: Wed, 08 Oct 2025 23:34:30 GMT  
		Size: 100.5 MB (100541003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ccde0cf2e46c778ef26b4761fe3a54e1c1571395c28b9805f58725a36510abd`  
		Last Modified: Tue, 16 Dec 2025 14:28:34 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:1f7550ab101b3755e96e9eaf1956fa30a2f29f57b69aca77a983dfed071ea24f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.5 KB (9460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69397ea70fd15259dfa76a75308cb78deefcece9b8751d9ba145e4302939e894`

```dockerfile
```

-	Layers:
	-	`sha256:8aedb537f312316ca919e4d1e8087436f057cd8b0fb340c9699472182a3dd95f`  
		Last Modified: Wed, 08 Oct 2025 23:34:28 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:fcd8a04d2b8010a2c634b3b12454f83307bd4c815e857a9dd68591beee213a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163116328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee44987d8c8772780c28b7d14120451bee646b77eaddb79f9ce126a058af64d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec5fdc4fb497bea03514de3252130b7697ae2993a729ad8de1c9d778513bc24`  
		Last Modified: Wed, 08 Oct 2025 21:49:32 GMT  
		Size: 45.8 MB (45813795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa523922045723fa3792824ea44631401bb773284938e53b5b27dda2041376b3`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c90f7c9f8a7f5db7344e75bb64578f0b7b30439d01bdbc5c15e62833526056`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e46deafa01e803acc346d7c558f432a758a4b7f99be4488fee34016ada71aa24`  
		Last Modified: Thu, 11 Dec 2025 18:06:18 GMT  
		Size: 113.2 MB (113163213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a60b66bd1d2b3a7c602cecc458a50bd3573492a27ea09e09fdd72ea434edb6`  
		Last Modified: Wed, 08 Oct 2025 22:56:36 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:b0d8e9b11d859e9cc8d4d23000574a77b0f2c0b892e92cd5daed2c02051408d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6950221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12533375389cd0ff941eec25254d6991119aa8600f1fb19be618de3c41ce93e0`

```dockerfile
```

-	Layers:
	-	`sha256:13cd7afefce47e2035fe8bbd34e1770dc422f824d930ce7d3fb988ebcdd013de`  
		Last Modified: Tue, 16 Dec 2025 11:31:26 GMT  
		Size: 6.9 MB (6940526 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b31770e469053bbce11b9337d3196c31a04fb515ee4413415df1358e4c87bb68`  
		Last Modified: Tue, 16 Dec 2025 11:31:24 GMT  
		Size: 9.7 KB (9695 bytes)  
		MIME: application/vnd.in-toto+json

## `znc:slim`

```console
$ docker pull znc@sha256:124c37d7fe8dffd345fc1e1258b5a589734e37eebbcb7698d53597863d2180de
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
$ docker pull znc@sha256:fae5167c8a61d5fbd49062bc8dec1c91dfa785bde38c7bd097c7de5b739e0166
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49823841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05117b24a815bf428045299e145a8d1d9a6134d6354c413d0e649b85246a1e23`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3506abfd78a36c30c23fe01f0c3ab62436212438294a0da94c8a15913326e030`  
		Last Modified: Wed, 08 Oct 2025 23:01:34 GMT  
		Size: 46.0 MB (46020467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e651980d24865ee4f19fa471fbeed8f6ba65e8b7cf4b242999fc0c0b130abdee`  
		Last Modified: Mon, 08 Dec 2025 01:27:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c7bbf12514d955bf730d0d365597fa448546c362e4120066bc07f0c079d2bbf`  
		Last Modified: Wed, 08 Oct 2025 23:01:32 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:75d996fa50ca858ca2021215b43c083759ff2e81688ab94d54285e2dcdd3d6cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1766801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28eeb49cc3fa631f14727ec0292593ee7c0a943987ec9993f2f9dbeddd0e17c9`

```dockerfile
```

-	Layers:
	-	`sha256:621f94726525728c0999a31ebf4c4ec1d00c759f8a5c86d9c87e2761c1634637`  
		Last Modified: Tue, 09 Dec 2025 08:36:40 GMT  
		Size: 1.8 MB (1752770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81d37d5e7d20698fe7532c6e3dbfdc07892d94429b4f25c837f87ed0a101918f`  
		Last Modified: Tue, 09 Dec 2025 08:36:39 GMT  
		Size: 14.0 KB (14031 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:2fe48e75462242a7ede2a1c0c348310571f7ee23542931efeec97b8e3c0100ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48110107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee93bff90c32e17f3a74c25ea264399ec27ac3de7397a010a7cfa58c571a44e`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-armhf.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:bb1da3d879939be7df9f182950d2fb201d4fc2e1043677da2037cd6afb084ce0`  
		Last Modified: Sun, 07 Dec 2025 22:05:32 GMT  
		Size: 3.5 MB (3504080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6840fec67135c40d32802946fc5362557e770be7653ca7360ea7070ab00fc998`  
		Last Modified: Wed, 08 Oct 2025 22:14:21 GMT  
		Size: 44.6 MB (44605106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405c3022b2b83a72e01be3a371b41b75f14cc4ca6477a7acb11833eed902ae83`  
		Last Modified: Tue, 16 Dec 2025 14:28:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f8f63e8f4811c752e213827a9a95c65b0becdc1370ff48a07652a48776cdc5a`  
		Last Modified: Tue, 16 Dec 2025 14:28:33 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:9a11b18474f484361d568e3b1b4c215ac13ecb24171b20aabeb73ec222f8b35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 KB (13888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f54bec2703401d236b520cbfcf642a219416fc6c2a15932d03610cb33d56e7`

```dockerfile
```

-	Layers:
	-	`sha256:143fbc029c2a24a9c8fd8ca6c25863b6892d267ba445da0456dd0765836aaca7`  
		Last Modified: Wed, 08 Oct 2025 22:14:20 GMT  
		Size: 13.9 KB (13888 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:14a1ba6341c42a9df7403e471dc85fa6c34bb7c06fae1f18cfee2552e8c1b55b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49952785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7f78b8c7f9677ac9a7921bf9124121f0f3b0d9a4be01d1a46585dc605c99eb`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Tue, 01 Jul 2025 21:26:43 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Tue, 01 Jul 2025 21:26:43 GMT
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec5fdc4fb497bea03514de3252130b7697ae2993a729ad8de1c9d778513bc24`  
		Last Modified: Wed, 08 Oct 2025 21:49:32 GMT  
		Size: 45.8 MB (45813795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa523922045723fa3792824ea44631401bb773284938e53b5b27dda2041376b3`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c90f7c9f8a7f5db7344e75bb64578f0b7b30439d01bdbc5c15e62833526056`  
		Last Modified: Tue, 09 Dec 2025 18:38:35 GMT  
		Size: 749.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:4a900b3cbf481a15ff4c53094629589ad021553aefef1004ebd3b697390f6079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 MB (1767022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7058b82b91838ebfacf5853086642932ba146f2ad05fcc8ab274a6a991eb12`

```dockerfile
```

-	Layers:
	-	`sha256:5876732d2e3a5d3f9c22b939b59b950404a086aa77605eb56873e874bc934a47`  
		Last Modified: Wed, 08 Oct 2025 21:49:31 GMT  
		Size: 1.8 MB (1752900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e302684a02e42366864e17b224123f7d91874878390a786b63b04aa66cdd40`  
		Last Modified: Wed, 10 Dec 2025 23:05:19 GMT  
		Size: 14.1 KB (14122 bytes)  
		MIME: application/vnd.in-toto+json
