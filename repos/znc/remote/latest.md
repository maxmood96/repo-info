## `znc:latest`

```console
$ docker pull znc@sha256:36353daf0ba6dad4b872c49bc28aad4d6094ec1c85473bc61bbd7391bfc73314
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
$ docker pull znc@sha256:df40c938c0a9f4812d0083a2c0fcd062128e2bf415a551f846b258da2a1e858f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.0 MB (157952292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593cc9c61f0411c5a0bc847d6621454001cf6bb2c60a6548220a71b1ca01e852`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
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
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbee9c933a5086145c18bb76d6cd13ace916c9e9b0aac1ac6626b017c8877ea4`  
		Last Modified: Tue, 07 Jan 2025 03:32:21 GMT  
		Size: 46.6 MB (46640219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1166cc9094add7747ffd8e4d9638f12b3e84f3dced588b6a0ba45927babd00`  
		Last Modified: Tue, 07 Jan 2025 03:32:20 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d068f85a3b3887a2e25ad06c4638173c474053a7ffa678dc683a24ea0ad9c35c`  
		Last Modified: Tue, 07 Jan 2025 03:32:19 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1b60ae4a373e2cd05b51a3b8e7c4033c9742d2b8bee3586f5fe660ea709729c`  
		Last Modified: Tue, 07 Jan 2025 04:18:38 GMT  
		Size: 107.9 MB (107897547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20be272abaa8b74c9d8e8456abc294ef8799fdca32344db27c2907431a71e87d`  
		Last Modified: Tue, 07 Jan 2025 04:18:35 GMT  
		Size: 333.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:6569ebde33bfc1a7c6e9d0f3d5a7d18109f3c5a05d94042807a4856b4d323c73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6749585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1752731c3746d3db3358b34c1698ffe37f95aa919dcc581f7a1ba595a6dc5992`

```dockerfile
```

-	Layers:
	-	`sha256:0987bd2e1e92b42fdc9947f6900419ece9fafa2ae5956d102b12c28b30f319f6`  
		Last Modified: Tue, 07 Jan 2025 04:18:36 GMT  
		Size: 6.7 MB (6739987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f35e4c088ba629d5ee0967ae442e557c27a912ae8ad441d9b70af71e8fd9990`  
		Last Modified: Tue, 07 Jan 2025 04:18:35 GMT  
		Size: 9.6 KB (9598 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:d50336f52e6fe166891f58edb5bd6ec2be59c4c1766b71c69cfddce1e4f111c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140341020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c030aaa76abc671841e651a739a5db43fd7a0287baaeddbecb3fee1ad7f10e2`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.5-armhf.tar.gz / # buildkit
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
	-	`sha256:7ebe2b3dea80a0cf44722451c51fa37efc40b0c599e291ba324046244780a76f`  
		Last Modified: Tue, 07 Jan 2025 02:30:01 GMT  
		Size: 3.2 MB (3169627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26b19fd69445f34b80c9394c2b8eed43142c98f21082e617414b6a576aad697d`  
		Last Modified: Tue, 07 Jan 2025 06:49:25 GMT  
		Size: 45.3 MB (45279130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4c6412cbb9a286f04871877b0c6a6cc4698b94dd5915f8049ddf8ea554882a`  
		Size: 171.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d05039a5cdcbaa65d4cedb361439d0e8668daf04ff705cc107ba34ce05866d`  
		Last Modified: Tue, 07 Jan 2025 06:49:24 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4491dbd2c287e79f8f89c23bff8498366e3f982aabcdb9d727a05dd44e8c6884`  
		Last Modified: Tue, 07 Jan 2025 18:30:44 GMT  
		Size: 91.9 MB (91891011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d43f839e492fc85de8124c337b91b2ed1459ef640a2cd2d44ca287d27a78eb29`  
		Size: 331.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:654b8cdb73551fda87f7e624cb188d288b2e70a983987dc306d9036a8ec0faef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.4 KB (9449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614bba1dc13d98d7212fccfb47cb14a3df56c497256f46e739fc83fb4cf7bd6e`

```dockerfile
```

-	Layers:
	-	`sha256:c5fd767b32eedb2a46280404657e8576c0e48f886904da7880453e637c436e49`  
		Last Modified: Tue, 07 Jan 2025 18:30:41 GMT  
		Size: 9.4 KB (9449 bytes)  
		MIME: application/vnd.in-toto+json

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:3a7a8995cebcc8b37115f181dc0d2773272a4d3152d882e593270c56a03d070d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152441978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8afadd731116a1f61dc811a32fc0f0321d04f77b669e14a857e0ef73ab0fd95c`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 03 Jul 2024 16:05:23 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Last Modified: Tue, 07 Jan 2025 03:03:15 GMT  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ba074f05a5f16d41754cae326ec8c7158928af8940f1b37f84c0b7566987b7`  
		Size: 46.7 MB (46701665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4395959983f224ebcbc26776aa9c45d18caa732a9325280d2874e2ac1e471550`  
		Last Modified: Tue, 07 Jan 2025 07:18:30 GMT  
		Size: 172.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:504cf82a539e7caf3d1ca36fad9bf6bdc4cf3a7ea9eb62fbfd7c6f8e9ae84c64`  
		Last Modified: Tue, 07 Jan 2025 07:18:30 GMT  
		Size: 750.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f84d5a49fac9cc4afebd70608897f2a8b57271bc5271cd96d1cb754ca96d2087`  
		Last Modified: Tue, 07 Jan 2025 16:06:34 GMT  
		Size: 102.4 MB (102387113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4617e8f881f1fb523192a56f28242f21b9483a7fe3b3a5405ebc6927adafd417`  
		Last Modified: Tue, 07 Jan 2025 16:06:31 GMT  
		Size: 330.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `znc:latest` - unknown; unknown

```console
$ docker pull znc@sha256:24bb3be0b64541c748f39c7d73fe6568fdfbdc541486da7eed947f36785fd963
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6785492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21cc743d69496cfe24fc0ac3a7adcd8f8becd9654378a9cbb081ba5b35be27d8`

```dockerfile
```

-	Layers:
	-	`sha256:bdc3d388ae169e7ff302658202e1c6bd415f5b1d755deab4bad28ac97fa9dd9b`  
		Last Modified: Tue, 07 Jan 2025 16:06:31 GMT  
		Size: 6.8 MB (6775803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f254fe83ba50ee570b102fbb58463c2fbf2dc89217e9d25796f7a21e4704a4d5`  
		Last Modified: Tue, 07 Jan 2025 16:06:30 GMT  
		Size: 9.7 KB (9689 bytes)  
		MIME: application/vnd.in-toto+json
