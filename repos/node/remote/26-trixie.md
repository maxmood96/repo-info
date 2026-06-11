## `node:26-trixie`

```console
$ docker pull node@sha256:f9a1756160a9e1c3dca456bc0b185bf8f2f112a6771c694df87288046f4306f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:26-trixie` - linux; amd64

```console
$ docker pull node@sha256:aa47e489ccc8af40cbfcbc6ed598f22638232ee525276152b29fffeec8fb57eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.1 MB (442082125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eb9fc940c5403413fee48498d4cb16514bad5e21416e09533ccd5f934cd0d96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:42:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:24:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:16:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 04:20:21 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 11 Jun 2026 04:20:34 GMT
ENV NODE_VERSION=26.3.0
# Thu, 11 Jun 2026 04:20:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Jun 2026 04:20:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:20:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:20:34 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:ef1b08ddd59d42b444e8f9c68a6cebbed70636aed0c242fdccb0bd61b61ba26b`  
		Last Modified: Wed, 10 Jun 2026 23:40:27 GMT  
		Size: 49.3 MB (49317121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b365b6ff7b7e310e1b9a88f996e65b89969c7fa450492b68249d1d1c38e0676`  
		Last Modified: Thu, 11 Jun 2026 00:42:51 GMT  
		Size: 25.6 MB (25635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ca884014342f240be01d391b498c3ec61b2f4af2c205e7e9a0b5ac2cb2f24c4`  
		Last Modified: Thu, 11 Jun 2026 02:25:01 GMT  
		Size: 67.8 MB (67784745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:442cca122a8b0987d6ea29e5fa7d0b8caf699cb127ec5fdbd8191faf86da521f`  
		Last Modified: Thu, 11 Jun 2026 03:17:25 GMT  
		Size: 236.2 MB (236195157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bfcbadb91e929f3bb1a4668f069ad6382158c13a784ae3750b8691df9c45a73`  
		Last Modified: Thu, 11 Jun 2026 04:21:02 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52be57c1f9889ad73eb5690c78eb07b53022d9a47a4317d0afe0c23f4848876b`  
		Last Modified: Thu, 11 Jun 2026 04:21:04 GMT  
		Size: 63.1 MB (63146162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd407e757cedc11aa734a2e776951cd63be10ab947c7672273b07c5a59a0980`  
		Last Modified: Thu, 11 Jun 2026 04:21:02 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-trixie` - unknown; unknown

```console
$ docker pull node@sha256:4165d05f5121832835f0e853534e93a7de5c354e22dad24cc87d171672841414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17432431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14ee29686c0e59a6561689b273d8e7c186d98c462144a212d1c027f12c1f1e93`

```dockerfile
```

-	Layers:
	-	`sha256:87b3afc863046ba18501df7ce6154cdd14abb6e28b8e611204e6e516ae5390c2`  
		Last Modified: Thu, 11 Jun 2026 04:21:03 GMT  
		Size: 17.4 MB (17413469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29aecd1451f2a9ab0280236539d3ffaf78669380acf126a309dbad3a3a547f54`  
		Last Modified: Thu, 11 Jun 2026 04:21:02 GMT  
		Size: 19.0 KB (18962 bytes)  
		MIME: application/vnd.in-toto+json

### `node:26-trixie` - linux; arm64 variant v8

```console
$ docker pull node@sha256:0c95f535259692cfee43892dd0fa454d855a3016ef343c5475b46d668c0a5d9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.0 MB (431987410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88000c501bd985d20fd62f118f05339fe32d604a294511e6a74ccaa911d337d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:44:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:22:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:16:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 04:20:09 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 11 Jun 2026 04:20:23 GMT
ENV NODE_VERSION=26.3.0
# Thu, 11 Jun 2026 04:20:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Jun 2026 04:20:23 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 04:20:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 04:20:23 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:ed660e1af0f5da9e93a4c43fb29e86cb46fe69c76bcf11a3de9c57c987acab82`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 49.7 MB (49678169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2ab02859108b91c1c26f2badd015b5215eb066b7ef4f3a22bd1536a8debe96`  
		Last Modified: Thu, 11 Jun 2026 00:44:32 GMT  
		Size: 25.0 MB (25026911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f2e427d8856f71d8d3667d1c4d9274b8aca2bd9d228387c51c211909e51263f`  
		Last Modified: Thu, 11 Jun 2026 02:22:21 GMT  
		Size: 67.6 MB (67599934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3bbd0b4297d07a9ba4bb3bfa1d7d9179e010ad584caad22d552ff94eb33b93`  
		Last Modified: Thu, 11 Jun 2026 03:17:28 GMT  
		Size: 226.3 MB (226344743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:884eca07656bc062543b38e2dcfecbf78862bed0b11c79b294f24212b589a406`  
		Last Modified: Thu, 11 Jun 2026 04:20:50 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34988e319840dd14138ba7d9355e45ddd49ce48b7a697d0591fb3e86aa93b15`  
		Last Modified: Thu, 11 Jun 2026 04:20:52 GMT  
		Size: 63.3 MB (63333884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f2bc5bc6c60e8a9bdb2590619bdc7e3b0cbca2f7184131d4e8d4ced842d9daf`  
		Last Modified: Thu, 11 Jun 2026 04:20:50 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-trixie` - unknown; unknown

```console
$ docker pull node@sha256:a246aaa202691b0ef4dfcc44c19a83489d90fb6934a4a2dec3dd4e990e38a492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17516364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afdefc157a102902cb4872896f30cf7032ac1d8a07fbfa93767a0d92e4b4588`

```dockerfile
```

-	Layers:
	-	`sha256:1ea96a348789d992f14f367fc80340f67374166293a5beada260db570c88c8b5`  
		Last Modified: Thu, 11 Jun 2026 04:20:51 GMT  
		Size: 17.5 MB (17497210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca5f64510f009272c8ec01b328c297d9e812a4438aec62ac494b9de2b4ec0cdb`  
		Last Modified: Thu, 11 Jun 2026 04:20:50 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.in-toto+json

### `node:26-trixie` - linux; ppc64le

```console
$ docker pull node@sha256:da799af13a900c25456b4dd9cd24f9be2832d9cf0cf90931743a7a1b67b5fd3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **450.0 MB (449968784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e709d8aec45d979674d119b6096962cff80ebf2cf3c6ae5de0394d905053554`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 04:45:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 10:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 12:49:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 16:39:15 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 11 Jun 2026 16:39:28 GMT
ENV NODE_VERSION=26.3.0
# Thu, 11 Jun 2026 16:39:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Jun 2026 16:39:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 16:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 16:39:28 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:fc2380819f7227178ecd607b245c244d8811737f42c6112caf011a01a3889a8e`  
		Last Modified: Thu, 11 Jun 2026 00:24:43 GMT  
		Size: 53.1 MB (53137939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc5ae5d968e23911f86d428bf6a67c0599a9449efc6170bd77e591b9eaf7c90d`  
		Last Modified: Thu, 11 Jun 2026 04:45:58 GMT  
		Size: 27.0 MB (27021977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82a68ee36453f6ba3cb200c7dbe5182e1d61ba54c525dacec15d40f163304257`  
		Last Modified: Thu, 11 Jun 2026 10:28:58 GMT  
		Size: 73.1 MB (73050891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1bbc6fa72ea93361e5c38810a0e56ae911b30362ab2aa094f6fd93a7b8b6d5`  
		Last Modified: Thu, 11 Jun 2026 12:50:34 GMT  
		Size: 231.3 MB (231316137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708343116b52c5fcef5a14c7309893bf7616a7c74830e9b461fd4dbac7c7b401`  
		Last Modified: Thu, 11 Jun 2026 16:40:24 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f0679f5601fcf55087d34b1745875f6ca332a783ab4908568cee1628feef4cc`  
		Last Modified: Thu, 11 Jun 2026 16:40:27 GMT  
		Size: 65.4 MB (65438066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e866a4ed74befcec47bc6180802f83b39cafd1cc93718dfbb84c500d93665f99`  
		Last Modified: Thu, 11 Jun 2026 16:40:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-trixie` - unknown; unknown

```console
$ docker pull node@sha256:8d7a3ffc18d99d98f71fc69d0798b853853c140543b2679f16f3cf96be5837b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17418093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9ebf26e047311b81da0ce9502509d71f20eb13c002bfcc8f986733184bb7ed6`

```dockerfile
```

-	Layers:
	-	`sha256:b9c722740a6650aaaf5129983f6a305648da742dd4eb777fc473a2753206b170`  
		Last Modified: Thu, 11 Jun 2026 16:40:25 GMT  
		Size: 17.4 MB (17399048 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b93ea343ba83fdbae92d59cf30fa005b35dfa1ee71d37d4daac8505d85374fee`  
		Last Modified: Thu, 11 Jun 2026 16:40:24 GMT  
		Size: 19.0 KB (19045 bytes)  
		MIME: application/vnd.in-toto+json

### `node:26-trixie` - linux; s390x

```console
$ docker pull node@sha256:a38cbebecaf8b1f3b7029400a715e18817456db455110deaf66530fc095b4b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416207792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46789d7a9f90c3e53d8323cd73229789a8bf1418ba3efd51f13579027b76e7bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:44:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 03:26:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 04:14:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 07:28:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 11 Jun 2026 07:28:14 GMT
ENV NODE_VERSION=26.3.0
# Thu, 11 Jun 2026 07:28:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Jun 2026 07:28:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Jun 2026 07:28:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Jun 2026 07:28:14 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0ebf827318debac5b829e4cd5c36e0122490cf2392f532aa02b2b0999d5c1b37`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 49.4 MB (49385897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b58925113278ed74d68122ff77b22976b064cb872b273063a3ab182209055ee`  
		Last Modified: Thu, 11 Jun 2026 01:44:45 GMT  
		Size: 26.8 MB (26803918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c67e4e83aa860c5b719a4e0cc01db908ae525049821b3c459f866ed434f070e`  
		Last Modified: Thu, 11 Jun 2026 03:27:03 GMT  
		Size: 68.7 MB (68653348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5ee4e18810194ccfb4c065c512c41bbd68891231f3d39485a8c21bfe151d5c2`  
		Last Modified: Thu, 11 Jun 2026 04:15:57 GMT  
		Size: 206.7 MB (206707893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8660df76628dde01727dea7404d0d4506390c23bb12c163e34a515b953fe0457`  
		Last Modified: Thu, 11 Jun 2026 07:29:00 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33ab1e9e35ebf7f3cf7500b99a9ec11839e96ea786cf2989502dd9f68bad09a`  
		Last Modified: Thu, 11 Jun 2026 07:29:03 GMT  
		Size: 64.7 MB (64652972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea71e825aa0e9d15647d0f141b11e25a1cea4caac7698dada93d4a2b9162233`  
		Last Modified: Thu, 11 Jun 2026 07:29:01 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:26-trixie` - unknown; unknown

```console
$ docker pull node@sha256:1d4d82828ceee4858473dbb08a9c7c2ef5f2d6b8dff0bb57ef775862e64bc678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17209665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf57fbbb7bc5e51fce6cf5c66bf7b749202801b157a9fc0e6ec9a018326e9d8`

```dockerfile
```

-	Layers:
	-	`sha256:8b3699dedb37c90131b772eb4ecfffcf5cba1ab9e6d4afbc1f07961df2a37fd2`  
		Last Modified: Thu, 11 Jun 2026 07:29:01 GMT  
		Size: 17.2 MB (17190702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff6bb3e1f3f208f3bdd3ed14ce36468b4c5e134f060d49676b12be3e71940e7`  
		Last Modified: Thu, 11 Jun 2026 07:29:01 GMT  
		Size: 19.0 KB (18963 bytes)  
		MIME: application/vnd.in-toto+json
