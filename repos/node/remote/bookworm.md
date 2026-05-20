## `node:bookworm`

```console
$ docker pull node@sha256:9dcb7951669ae6ad3830880d65e6cc60eb8b4e139e739816d57251e1b8b35976
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

### `node:bookworm` - linux; amd64

```console
$ docker pull node@sha256:2c327346abcd763a2683ab1d16d9a5650e5ad21b750478600cf9063000d09448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.4 MB (411415464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:041b8e52132bf3c5beec9549d1b30b11f94148847b43510dcb082c8782594230`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:20:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 May 2026 02:20:34 GMT
ENV NODE_VERSION=26.1.0
# Wed, 20 May 2026 02:20:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 20 May 2026 02:20:34 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 02:20:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 02:20:34 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce041001b8968f31ff00bb8f9dbd68f72d4bdc378a1309e38eb3dfe97cc1498`  
		Last Modified: Wed, 20 May 2026 01:15:50 GMT  
		Size: 211.6 MB (211586305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f4a2bb9afd24e3cf10003f29172ec10458de76265213d38f8904a1ccdc57a3`  
		Last Modified: Wed, 20 May 2026 02:21:00 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f898065af23a4d0d884a4c2eefc1edb63b6a7668adb0bca50bdfcc321300040`  
		Last Modified: Wed, 20 May 2026 02:21:02 GMT  
		Size: 62.9 MB (62882132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6f2e47288edc2abe9efedaaf6e76ad816e8e9c6c11563c6ac7815cad4f826d`  
		Last Modified: Wed, 20 May 2026 02:21:00 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:63e17615b3a423c38b61ad4ce4d2c7a0e8961985abf3767300a3b5aba2494968
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16092501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:976554beb2fd05c39321fafccea5d054e9eddbef1735c2ad6d46f12950cfef54`

```dockerfile
```

-	Layers:
	-	`sha256:feca121396bcd1de21da9a9753a4a596fac60b885b213d839f9799a13b05ce2e`  
		Last Modified: Wed, 20 May 2026 02:21:01 GMT  
		Size: 16.1 MB (16074871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99ed561e7b822c8a8b29559bf6055b55a8d0eb2d1da2baf0907dba0f2900a50d`  
		Last Modified: Wed, 20 May 2026 02:21:00 GMT  
		Size: 17.6 KB (17630 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:3eb89278b1b57220cde7f55dbee518e42599519b0e25c6543b164b55866dc837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.7 MB (402707092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b778b7b09951c71bfd13ff0ab99f43f6598d7f5f8ea2fe74c9874edc450c46b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:19:41 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 May 2026 02:19:51 GMT
ENV NODE_VERSION=26.1.0
# Wed, 20 May 2026 02:19:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 20 May 2026 02:19:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 02:19:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 02:19:51 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03874872dc6df1c0caacf1eaa4544f492fcb08bd68a885b9b784f5e9be1d6e6`  
		Last Modified: Wed, 20 May 2026 01:15:57 GMT  
		Size: 203.1 MB (203108347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e522ce25083be7c7e5f7fa58a145f5911193ffcc7afff686afe5062cb94ddbdd`  
		Last Modified: Wed, 20 May 2026 02:20:20 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d432cf6ee0e2d8ae74b8e0e4441f5d19b986fa5c8ac93080a02b99bda9214c5c`  
		Last Modified: Wed, 20 May 2026 02:20:23 GMT  
		Size: 63.1 MB (63114491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de29347d87196ce2180744f9c250f338a56d582bbe76e86186a391bc1197fd7a`  
		Last Modified: Wed, 20 May 2026 02:20:20 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:b52f820cb5258b89f65b0aa26718232e819c78e388b276cc5135d2311f422572
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16121170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2cc61f2e0e6ad18314399aca22b01e3bf66935655a63f8567b5e5dd5c441a49`

```dockerfile
```

-	Layers:
	-	`sha256:5ee0187985cc97a6db6fc1d77504a55d0aa4e38f94f92c32707f9339a21d8389`  
		Last Modified: Wed, 20 May 2026 02:20:21 GMT  
		Size: 16.1 MB (16103409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e01e74a9f7a38e62dbf07ba6df70d42e329d5cf6dd1500b7cab24324da664dd5`  
		Last Modified: Wed, 20 May 2026 02:20:20 GMT  
		Size: 17.8 KB (17761 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:a2b7c0e490802e992f130a5af592a8a63f7e7bdc5c306cb06f168cfd196a3d7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **427.5 MB (427458827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1661ee23fd593ec43ecc1ae866fb93e60b98b2807359151f21e9e666a86da1b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1777939200'
# Fri, 08 May 2026 22:30:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 03:26:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 06:06:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Sat, 09 May 2026 10:28:30 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Sat, 09 May 2026 10:28:46 GMT
ENV NODE_VERSION=26.1.0
# Sat, 09 May 2026 10:28:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Sat, 09 May 2026 10:28:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Sat, 09 May 2026 10:28:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 09 May 2026 10:28:46 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:30ef9f53c997c6c1f1ab8f4cc559b32d9206d169c54ad5a0f0363076708fffef`  
		Last Modified: Fri, 08 May 2026 19:44:07 GMT  
		Size: 52.3 MB (52336787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d76bedc371abd17d2a145cc444214f9d4db5b827f6b018dfa08217a285aa62a4`  
		Last Modified: Fri, 08 May 2026 22:30:50 GMT  
		Size: 25.7 MB (25679486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d12437260b341898b5eafdacd454cf094e6357253f008361a2200d2d98887726`  
		Last Modified: Sat, 09 May 2026 03:27:08 GMT  
		Size: 69.8 MB (69846587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8dc558cd48bcfa9874859861c70682b58786391c889d141c260d56d50b41d9d`  
		Last Modified: Sat, 09 May 2026 06:07:54 GMT  
		Size: 214.6 MB (214639458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200c55385620e367b7c4d10b53b30de0d06f8e743c3871c485a1aa5b5b9cf9cf`  
		Last Modified: Sat, 09 May 2026 10:29:38 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f18b82a39632f598818644e294d5cd9b6bc07c96b177ca0e9f11b436943274d`  
		Last Modified: Sat, 09 May 2026 10:29:40 GMT  
		Size: 65.0 MB (64952739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3406998c6c24f508d79274bff73c652c9b7ead45e07cb55b80fd09f0f2b9564`  
		Last Modified: Sat, 09 May 2026 10:29:38 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:f0f92329ccab0bb5e2396153a61fd539a4ce834e29b01cea85950e80290b0c9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16070572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c188272b86e7cff367b28fdbbe55ada6822deb5898a1a7023c23cae30dae45cc`

```dockerfile
```

-	Layers:
	-	`sha256:7c4b50b14bf0af8d9ec71e32ccd459842c4b87accde54a87de442cf55773c674`  
		Last Modified: Sat, 09 May 2026 10:29:38 GMT  
		Size: 16.1 MB (16052890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68f56d26e769a260c7417aa9c40dd78bd55fdca409089fc9ec7e3bcdeab1beba`  
		Last Modified: Sat, 09 May 2026 10:29:38 GMT  
		Size: 17.7 KB (17682 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; s390x

```console
$ docker pull node@sha256:4bc48adac30548767cfe5fc7314e7701d43886c05305876c174313166f71e370
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.1 MB (387137748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d485dd9064e60ceb7b858eba174f47fe9616f120ef7235415fb9c5a3463b466`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 05:14:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 20 May 2026 05:14:28 GMT
ENV NODE_VERSION=26.1.0
# Wed, 20 May 2026 05:14:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 20 May 2026 05:14:28 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 20 May 2026 05:14:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 20 May 2026 05:14:28 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ade0407a6db3c4a6853a735563e5fb22577aaaa32942a9458cc0c09942583`  
		Last Modified: Wed, 20 May 2026 02:05:37 GMT  
		Size: 63.5 MB (63498321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaa6dc17afbecf60ca3315d2c4ad18f3028bcf8091ccde763daf04c218092a7`  
		Last Modified: Wed, 20 May 2026 02:45:53 GMT  
		Size: 183.6 MB (183603631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba85ce6eb06ccf052ceefbfed48a6b2ff9f2213a5ea6d0934c75ffd7f4001700`  
		Last Modified: Wed, 20 May 2026 05:15:18 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:730457af333076a359e75ee26163b199b3786e0bb39ff3c0480502863e26c69e`  
		Last Modified: Wed, 20 May 2026 05:15:20 GMT  
		Size: 68.8 MB (68837240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c7b652c626ddf61857d9462810d84145d2dc87693a00c71b3e6cd40307a1f7`  
		Last Modified: Wed, 20 May 2026 05:15:18 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:cb274e4477382d9549e605d730e2a11b4e1c376f977714ec6bd11b79e969ccc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15900099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54221fec4edeb9f5a90be6462335f2ce2c364d1b609e820381c1b0c5fe5a3b3`

```dockerfile
```

-	Layers:
	-	`sha256:f9b866da02dfa7fa28c03a360f92e9ae15e42f3204264c2fa1a4fea4b4582d02`  
		Last Modified: Wed, 20 May 2026 05:15:18 GMT  
		Size: 15.9 MB (15882469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1865c0df0171c71e7205759d432e6fdd8e6f562985eb87366866ea3cf1eef4cb`  
		Last Modified: Wed, 20 May 2026 05:15:18 GMT  
		Size: 17.6 KB (17630 bytes)  
		MIME: application/vnd.in-toto+json
