## `znc:latest`

```console
$ docker pull znc@sha256:741f032ec510205eb16754f8eae8ce4d70d98b09f3681dd190f39467d0d3808a
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
