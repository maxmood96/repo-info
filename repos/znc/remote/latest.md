## `znc:latest`

```console
$ docker pull znc@sha256:67db8bda379e3fd705d5dad313884fea1431426d99bced02e934d003667a3f81
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
$ docker pull znc@sha256:68aad9ef612f73bab8cabe9a3ced77fcd6713d21c99b17afe0633338b68620e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157984531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314970a43e753fd52e0341d32d53980e44a6a46116e6832c851a80cfdb9acb53`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
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
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:406a3dfa159b9d23e152531d167a332825b5a59978e6db3a913dfb65bbbd8d8c`  
		Last Modified: Fri, 06 Sep 2024 23:29:45 GMT  
		Size: 46.7 MB (46667717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad7792ca89d5552cd77d8082473c124b5509d0c102a5f267669080a74f5bb8a`  
		Last Modified: Fri, 06 Sep 2024 23:29:43 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:853651eab9ad80f1df0af0932b2364669f12a8d69c34eda4f9e94275f8f4e6f2`  
		Last Modified: Fri, 06 Sep 2024 23:29:43 GMT  
		Size: 748.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfae7ca9d97f8beef3ba493847799d8a98f6c13e3834b3b97a8d72531a2a7103`  
		Last Modified: Sat, 07 Sep 2024 00:08:47 GMT  
		Size: 107.9 MB (107895856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f61cb710d10cba4fcd7c13c2c4e1471f560a7d6a2c662908093c2db950907b7`  
		Last Modified: Sat, 07 Sep 2024 00:08:45 GMT  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:6dceaff17af9602e021c7874bed50257cf81cddace217ebd6035090170d02a5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6764057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7b231be72a86512eb99af685a0bd093e7f5a15b9c1c04e8464481c37c41bdb5`

```dockerfile
```

-	Layers:
	-	`sha256:85e5a866f6958378584f09b5cd8a9f78a117a778330bf409bf9d12be454b1eb1`  
		Last Modified: Sat, 07 Sep 2024 00:08:46 GMT  
		Size: 6.8 MB (6754493 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55a327caf1a518c6c1129fedc38d15d5c946b603eeaefc4baf419e704eb974f8`  
		Last Modified: Sat, 07 Sep 2024 00:08:45 GMT  
		Size: 9.6 KB (9564 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:0ab206f35f31f3d659987c2df14a4179627ca1ccdb051dd8b58c30e7b2e8881a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140377641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78f4e7d6358bb4613b9137d5e301e0075754032504c63eb1b248cb157be45a5d`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:f7bd0000dae58eecf5aaf17e8bc517f5e29ad6a7692506fbceef89d3b61327c5 in / 
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
	-	`sha256:25b28a78657effc87fccb3820a41450134ddcdbea210294d5b989ee0f09c0563`  
		Last Modified: Mon, 22 Jul 2024 21:49:53 GMT  
		Size: 3.2 MB (3175673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58be51da89d582faefd6d54cac29d2f550693ded976faef3ed5210a3eeedd4a0`  
		Last Modified: Tue, 23 Jul 2024 11:54:20 GMT  
		Size: 45.3 MB (45303745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abf7940323f47cfa0307538de116a541971b7d95ed5864b3485ff6189d6326e6`  
		Last Modified: Tue, 23 Jul 2024 11:54:19 GMT  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c0c0bda3b084640e24d92d58998128eb779b61b1c0cd8a326beeda066fee94e`  
		Last Modified: Tue, 23 Jul 2024 11:54:19 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f66f510d2e00bd6f61a6398b391f5b88048abd15e488f76baa3c363b8d5a20d`  
		Last Modified: Tue, 23 Jul 2024 13:11:19 GMT  
		Size: 91.9 MB (91896972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2313a8d1f78fd9380b0a9d632056b7cf2820ae5cf1a292a97f8f29a6afa9b77f`  
		Last Modified: Tue, 23 Jul 2024 13:11:16 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:0cb1c25e7141105b0940b374be1e8f6e7920a52f7f6fc1b9e59ca49e3826cec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d65925fdb814317a328fa51ba5b03eff6bd6eaa1d50572db0cdf31209c77ee`

```dockerfile
```

-	Layers:
	-	`sha256:94506bfe5e3a84a36edef163e301f4141680142a12b4f5c09512272f13524b71`  
		Last Modified: Tue, 23 Jul 2024 13:11:16 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:507d4e9b67a74be8ca7f78a9afe17383d6ef7b4aefecb7c6ec8a6a505522cda8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.5 MB (152453085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e347382799033c0eda49c68045bd9bf066c1288d643272b438e8586d9088ce03`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
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
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1142838b39076da4a6601a88b29fc0b352f7c09f13baf27a9c7678035f9decd`  
		Last Modified: Wed, 24 Jul 2024 10:34:28 GMT  
		Size: 46.7 MB (46717398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae713b2fd15233f72f5e7a6369993fa200593fbb3805c48da5299a4c1db6a0b8`  
		Last Modified: Wed, 24 Jul 2024 10:34:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08e3a8014f971dff04c43b1c7551aaf1fe7f3640f1dc240907d22b27d290b257`  
		Last Modified: Wed, 24 Jul 2024 10:34:26 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f3a25f586f08dd4dfa0ad25c62b196b9168927da682ee77f4210c27471d29f`  
		Last Modified: Wed, 24 Jul 2024 14:23:05 GMT  
		Size: 102.4 MB (102375976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb9e531466d9ebaaf5203265fc5b7cf373620d5c29e0133691175122b96f0e4`  
		Last Modified: Wed, 24 Jul 2024 14:23:02 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:d496a2d9280146294352a80d4509bf9fa049d018924cb7b3d5d9d5be8c75843a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6800319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39e833f64229c4cdc17b3a0262a808ace0c0e21a82bb1c12c290657e55ba3a6a`

```dockerfile
```

-	Layers:
	-	`sha256:df14c23e18e2cb72583be8a0ebd9f486d55186b03d5fa9d8172e191d1768b8ba`  
		Last Modified: Wed, 24 Jul 2024 14:23:02 GMT  
		Size: 6.8 MB (6790364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0456aebf842ca1f5e3778e16d2cfd96379e2b913fc0e684b3039f327a8f6dc9`  
		Last Modified: Wed, 24 Jul 2024 14:23:02 GMT  
		Size: 10.0 KB (9955 bytes)  
		MIME: application/vnd.in-toto+json
