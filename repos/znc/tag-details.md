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
$ docker pull znc@sha256:e7913d0404a70209932125f4739b25b208eb816e982eb4da2cdb51f5bc2e7bea
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

### `znc:1.9` - unknown; unknown

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

### `znc:1.9` - unknown; unknown

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

## `znc:1.9-slim`

```console
$ docker pull znc@sha256:6759891cbf99ece47e46e35e8e3426bbfaa246f31e31f89d87d129fe02f88b4a
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
$ docker pull znc@sha256:8035eb0375ca369f2f6e720fe5a0bc46aca124f47c39e037173f96b9cfb7d996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50088344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280f4e0a0551b143d4bf474269db412048f9d9e6eadd46799567563207a41e98`
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

### `znc:1.9-slim` - unknown; unknown

```console
$ docker pull znc@sha256:4ec5190f986d1c5d648cb66d7fba5a4f3b45ac8dcbc3d2c2db5a8ac36cb4aa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1028dfc559f0b4aea0201312edc8f03693e3c73d869efef21e975d6b45905587`

```dockerfile
```

-	Layers:
	-	`sha256:0d12edda0b5a98501af0c9d049e53bd780bfd1e9bc6df45233cb55887efd14bb`  
		Last Modified: Fri, 06 Sep 2024 23:29:44 GMT  
		Size: 2.1 MB (2138417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448019100652206a0f988b822d988dbbf1f0eadcd98423f5e30f14af6a63beb`  
		Last Modified: Fri, 06 Sep 2024 23:29:43 GMT  
		Size: 13.8 KB (13793 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:5eca7090f217caf9c22c4271c4f330d042545ef7f5f8fbf0266a37572223fdc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48485045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b8e0a6e810c80d2ea6f49833a656b8895fc880e86ee7f230e58ada49eec001`
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

### `znc:1.9-slim` - unknown; unknown

```console
$ docker pull znc@sha256:a2afe055e9760f152bf26f4f222e77506d8d0387d5ac82639e23f23e339e50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8febbc9be4b623fdb9541735ed40297679114aab034f6ed3606491cac89953a3`

```dockerfile
```

-	Layers:
	-	`sha256:03b82f0798c4cba892877500cd4ff0d10d90b639fd562cd53ea60c3ae94bc136`  
		Last Modified: Sat, 07 Sep 2024 12:50:21 GMT  
		Size: 13.6 KB (13636 bytes)  
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
$ docker pull znc@sha256:e7913d0404a70209932125f4739b25b208eb816e982eb4da2cdb51f5bc2e7bea
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

### `znc:1.9.1` - unknown; unknown

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

### `znc:1.9.1` - unknown; unknown

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

## `znc:1.9.1-slim`

```console
$ docker pull znc@sha256:6759891cbf99ece47e46e35e8e3426bbfaa246f31e31f89d87d129fe02f88b4a
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
$ docker pull znc@sha256:8035eb0375ca369f2f6e720fe5a0bc46aca124f47c39e037173f96b9cfb7d996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50088344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280f4e0a0551b143d4bf474269db412048f9d9e6eadd46799567563207a41e98`
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

### `znc:1.9.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:4ec5190f986d1c5d648cb66d7fba5a4f3b45ac8dcbc3d2c2db5a8ac36cb4aa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1028dfc559f0b4aea0201312edc8f03693e3c73d869efef21e975d6b45905587`

```dockerfile
```

-	Layers:
	-	`sha256:0d12edda0b5a98501af0c9d049e53bd780bfd1e9bc6df45233cb55887efd14bb`  
		Last Modified: Fri, 06 Sep 2024 23:29:44 GMT  
		Size: 2.1 MB (2138417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448019100652206a0f988b822d988dbbf1f0eadcd98423f5e30f14af6a63beb`  
		Last Modified: Fri, 06 Sep 2024 23:29:43 GMT  
		Size: 13.8 KB (13793 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:1.9.1-slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:5eca7090f217caf9c22c4271c4f330d042545ef7f5f8fbf0266a37572223fdc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48485045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b8e0a6e810c80d2ea6f49833a656b8895fc880e86ee7f230e58ada49eec001`
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

### `znc:1.9.1-slim` - unknown; unknown

```console
$ docker pull znc@sha256:a2afe055e9760f152bf26f4f222e77506d8d0387d5ac82639e23f23e339e50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8febbc9be4b623fdb9541735ed40297679114aab034f6ed3606491cac89953a3`

```dockerfile
```

-	Layers:
	-	`sha256:03b82f0798c4cba892877500cd4ff0d10d90b639fd562cd53ea60c3ae94bc136`  
		Last Modified: Sat, 07 Sep 2024 12:50:21 GMT  
		Size: 13.6 KB (13636 bytes)  
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
$ docker pull znc@sha256:e7913d0404a70209932125f4739b25b208eb816e982eb4da2cdb51f5bc2e7bea
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

## `znc:slim`

```console
$ docker pull znc@sha256:6759891cbf99ece47e46e35e8e3426bbfaa246f31e31f89d87d129fe02f88b4a
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
$ docker pull znc@sha256:8035eb0375ca369f2f6e720fe5a0bc46aca124f47c39e037173f96b9cfb7d996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50088344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280f4e0a0551b143d4bf474269db412048f9d9e6eadd46799567563207a41e98`
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

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:4ec5190f986d1c5d648cb66d7fba5a4f3b45ac8dcbc3d2c2db5a8ac36cb4aa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2152210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1028dfc559f0b4aea0201312edc8f03693e3c73d869efef21e975d6b45905587`

```dockerfile
```

-	Layers:
	-	`sha256:0d12edda0b5a98501af0c9d049e53bd780bfd1e9bc6df45233cb55887efd14bb`  
		Last Modified: Fri, 06 Sep 2024 23:29:44 GMT  
		Size: 2.1 MB (2138417 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e448019100652206a0f988b822d988dbbf1f0eadcd98423f5e30f14af6a63beb`  
		Last Modified: Fri, 06 Sep 2024 23:29:43 GMT  
		Size: 13.8 KB (13793 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:slim` - linux; arm variant v6

```console
$ docker pull znc@sha256:5eca7090f217caf9c22c4271c4f330d042545ef7f5f8fbf0266a37572223fdc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48485045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3b8e0a6e810c80d2ea6f49833a656b8895fc880e86ee7f230e58ada49eec001`
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

### `znc:slim` - unknown; unknown

```console
$ docker pull znc@sha256:a2afe055e9760f152bf26f4f222e77506d8d0387d5ac82639e23f23e339e50de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.6 KB (13636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8febbc9be4b623fdb9541735ed40297679114aab034f6ed3606491cac89953a3`

```dockerfile
```

-	Layers:
	-	`sha256:03b82f0798c4cba892877500cd4ff0d10d90b639fd562cd53ea60c3ae94bc136`  
		Last Modified: Sat, 07 Sep 2024 12:50:21 GMT  
		Size: 13.6 KB (13636 bytes)  
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
