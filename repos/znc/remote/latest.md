## `znc:latest`

```console
$ docker pull znc@sha256:7fe76dbbafadb45fb00f7fdf7d206046858b4536aadf110ccf03a1164c14c220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `znc:latest` - linux; amd64

```console
$ docker pull znc@sha256:6a723d657e60398a1840e3694c33205cd8e1bf5a37f94e2f5751d13227b95630
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.5 MB (164485303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33388d7899aecc1b60689771121a917f101280ac1acd35abd1fd155532059045`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 04:24:56 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Thu, 15 Jun 2023 04:24:56 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Thu, 15 Jun 2023 04:24:56 GMT
ARG MAKEFLAGS=
# Thu, 15 Jun 2023 04:24:56 GMT
ENV ZNC_VERSION=1.8.2
# Thu, 15 Jun 2023 04:28:48 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Thu, 15 Jun 2023 04:28:48 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Thu, 15 Jun 2023 04:28:48 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Thu, 15 Jun 2023 04:28:48 GMT
VOLUME [/znc-data]
# Thu, 15 Jun 2023 04:28:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 15 Jun 2023 04:29:11 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Thu, 15 Jun 2023 04:29:12 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99530fd3b1a00a34431f8e1df9a0cc0f427c2bcfea3fe3fab0102367a0dbcd25`  
		Last Modified: Thu, 15 Jun 2023 04:29:28 GMT  
		Size: 46.6 MB (46591522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88eeab4f653f6c75d96e558096580534631f755704dff753edccc6006c53a7b`  
		Last Modified: Thu, 15 Jun 2023 04:29:21 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a9e34d6f01845b0e262c15ca0bc00529ab7a7d855485a02be61cb16febb6909`  
		Last Modified: Thu, 15 Jun 2023 04:29:21 GMT  
		Size: 776.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dec095213d05bffad6dc8a245dc9a9ebe68cf80fd47f771c09b3196e945db62`  
		Last Modified: Thu, 15 Jun 2023 04:29:54 GMT  
		Size: 114.5 MB (114517790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd9b646f143940d48ddcc4fb9337279937457d7b190abfe6ddc88697c9c03433`  
		Last Modified: Thu, 15 Jun 2023 04:29:38 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm variant v6

```console
$ docker pull znc@sha256:07d5c7e072255c6717aa361d3c3819b6a21acec27a29077237642227ddeb4737
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.1 MB (144064646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f8c5d262311959a6046b24fc7fb644d8e6abd3959319adac0d766e785fb7bb6`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 18:49:25 GMT
ADD file:07e668ef139dce7f076143a30b89ff57885c8539d8b5764ac1bd5277d9936702 in / 
# Wed, 14 Jun 2023 18:49:25 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 20:13:55 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 14 Jun 2023 20:13:55 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 14 Jun 2023 20:13:56 GMT
ARG MAKEFLAGS=
# Wed, 14 Jun 2023 20:13:56 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 14 Jun 2023 20:18:04 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 14 Jun 2023 20:18:04 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 14 Jun 2023 20:18:04 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 14 Jun 2023 20:18:05 GMT
VOLUME [/znc-data]
# Wed, 14 Jun 2023 20:18:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jun 2023 20:18:30 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 14 Jun 2023 20:18:33 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:33ec62e98ceea71d24212ee03e239c2d5538dbe7c98f41c42e8b2693fedf58fb`  
		Last Modified: Wed, 14 Jun 2023 18:50:00 GMT  
		Size: 3.1 MB (3110916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33307be6b66090bf65bdab1d1a56dfa125ac4a3a18db9adc8156e2b6e8a185ac`  
		Last Modified: Wed, 14 Jun 2023 20:18:52 GMT  
		Size: 44.8 MB (44792156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2186893ac1c9522ac10185266cda9406e7a492404936d0811f1150d749ca1ab2`  
		Last Modified: Wed, 14 Jun 2023 20:18:43 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6302be92bb802d0679620711eecf7d91604f2c4556cfc77e5f6b01b8bf44d4bc`  
		Last Modified: Wed, 14 Jun 2023 20:18:43 GMT  
		Size: 782.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89c890c8235198d9c0a89d5a6438cbdaa69a411243d2876b34d61fa5a37ebe7`  
		Last Modified: Wed, 14 Jun 2023 20:19:20 GMT  
		Size: 96.2 MB (96160290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ac9f384cae3b6e9433b9ac16f6a9d0849b35bdf733c340f5657a2d3d890d79`  
		Last Modified: Wed, 14 Jun 2023 20:19:01 GMT  
		Size: 331.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `znc:latest` - linux; arm64 variant v8

```console
$ docker pull znc@sha256:d84c3f4fb78d6ce56ec712f6584277560cf66a3bbe6eeffef71ac3f72910754e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.4 MB (153351216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68453737876ef4dbc504f0b08fff3d71e9c90305a13903b7a3f2a2a9388daa77`
-	Entrypoint: `["\/entrypoint.sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 23:17:52 GMT
ENV GPG_KEY=D5823CACB477191CAC0075555AE420CC0209989E
# Wed, 14 Jun 2023 23:17:52 GMT
ARG CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES
# Wed, 14 Jun 2023 23:17:52 GMT
ARG MAKEFLAGS=
# Wed, 14 Jun 2023 23:17:52 GMT
ENV ZNC_VERSION=1.8.2
# Wed, 14 Jun 2023 23:21:11 GMT
# ARGS: CMAKEFLAGS=-DCMAKE_INSTALL_PREFIX=/opt/znc -DWANT_CYRUS=YES -DWANT_PERL=YES -DWANT_PYTHON=YES MAKEFLAGS=
RUN set -x     && adduser -S znc     && addgroup -S znc     && apk add --no-cache --virtual runtime-dependencies         boost         ca-certificates         cyrus-sasl         icu         icu-data-full         openssl         su-exec         tini         tzdata     && apk add --no-cache --virtual build-dependencies         boost-dev         build-base         cmake         curl         cyrus-sasl-dev         gettext         gnupg         icu-dev         openssl-dev         perl-dev         python3-dev     && mkdir /znc-src && cd /znc-src     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz" -o znc.tgz     && curl -fsSL "https://znc.in/releases/archive/znc-${ZNC_VERSION}.tar.gz.sig" -o znc.tgz.sig     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "${GPG_KEY}"     && gpg --batch --verify znc.tgz.sig znc.tgz     && rm -rf "$GNUPGHOME"     && tar -zxf znc.tgz --strip-components=1     && mkdir build && cd build     && cmake .. ${CMAKEFLAGS}     && make $MAKEFLAGS     && make install     && apk del build-dependencies     && cd / && rm -rf /znc-src
# Wed, 14 Jun 2023 23:21:11 GMT
COPY file:15e47c9cc6835e0818d6896aa6537a8adda40ff814c287685183c73fa9df4713 in / 
# Wed, 14 Jun 2023 23:21:11 GMT
COPY dir:4684da7bbf1d77862fa1a1b074543f975eb608cc0b6b1951ff5c5b58959d0faa in /startup-sequence/ 
# Wed, 14 Jun 2023 23:21:11 GMT
VOLUME [/znc-data]
# Wed, 14 Jun 2023 23:21:12 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 14 Jun 2023 23:21:21 GMT
RUN set -x     && apk add --no-cache         build-base         cmake         icu-dev         openssl-dev         perl         python3
# Wed, 14 Jun 2023 23:21:22 GMT
COPY file:765473e154cb7674cba99ed8ee42b51feda01581be870e3d1e7e4930b82a0f37 in /startup-sequence/ 
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea2d5dae4844b5e0888bf91da15915273f907c297e917dcdcca8dad25945e53`  
		Last Modified: Wed, 14 Jun 2023 23:21:37 GMT  
		Size: 46.2 MB (46189731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a15b36520b6aab8222d6b5143826eee590bb0f74bbfd7478315b0fcc822126`  
		Last Modified: Wed, 14 Jun 2023 23:21:31 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:307a032731516a64d1b6860da8a0b1f7df436d013d655d58096a3d8fb320a7c0`  
		Last Modified: Wed, 14 Jun 2023 23:21:32 GMT  
		Size: 779.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13743297593f220c5d8cdd463b456d362bc2ae50b7babca64d5e6081897fabdd`  
		Last Modified: Wed, 14 Jun 2023 23:21:58 GMT  
		Size: 103.9 MB (103899063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49f473c2df4eaad7b91c91e1de5b1a03ddbbb61b154d0646eb0359bc003a641e`  
		Last Modified: Wed, 14 Jun 2023 23:21:47 GMT  
		Size: 332.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
