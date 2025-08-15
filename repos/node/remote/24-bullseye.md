## `node:24-bullseye`

```console
$ docker pull node@sha256:4c90ae2268a9f3662f47d3f65e3a4c8efe8d1ba95e51482893ecc60933221da1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:24-bullseye` - linux; amd64

```console
$ docker pull node@sha256:8169f7263802d708e500392a3f8d4f479be85b39e5a628203d69d73453992f99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.1 MB (383131211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:470f609f53012fc154e82ae86c2b8a9f9d8e25fe17ba9d5300570869d357caa4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 23:05:41 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 14 Aug 2025 23:05:41 GMT
ENV NODE_VERSION=24.6.0
# Thu, 14 Aug 2025 23:05:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 14 Aug 2025 23:05:41 GMT
ENV YARN_VERSION=1.22.22
# Thu, 14 Aug 2025 23:05:41 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 14 Aug 2025 23:05:41 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 14 Aug 2025 23:05:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 14 Aug 2025 23:05:41 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:078965fc7cf303b72cc4eef5479dc2dbf5bc84fb8e6052a89b9b5362e14b3651`  
		Last Modified: Tue, 12 Aug 2025 20:44:43 GMT  
		Size: 53.8 MB (53755344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8620e616831b3851d274036e48fee788599fe355ea621ba7b912b9c15925e81f`  
		Last Modified: Tue, 12 Aug 2025 21:21:48 GMT  
		Size: 15.8 MB (15765318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99bdf4e3059e088f15d90d719c388546de462f8152d07d724a4895907f69c1ce`  
		Last Modified: Tue, 12 Aug 2025 22:15:17 GMT  
		Size: 54.8 MB (54757082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6f7f2858f78fda61ee4b09ef4641600c64959581a56b582d6110d612850d83`  
		Last Modified: Tue, 12 Aug 2025 22:50:22 GMT  
		Size: 197.1 MB (197145445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb625281a55fd811ea2e90998bac042686a564ba05b7f7dac93b3da83b29bf28`  
		Last Modified: Fri, 15 Aug 2025 17:45:41 GMT  
		Size: 4.1 KB (4090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f1dfba61e8886a55547d0b4c0fba6cb36810f3a5dbe02c34474428a43d267c`  
		Last Modified: Fri, 15 Aug 2025 17:45:44 GMT  
		Size: 60.5 MB (60452817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f38923f31297f1fe721ccbc0be0187f74f6fad8ad58525f8df9ef02cc9fee0d`  
		Last Modified: Fri, 15 Aug 2025 17:45:43 GMT  
		Size: 1.3 MB (1250669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c7779c1999d9a3f1a6f60f7b9d613baaf03689151978897aaaa9e3554d618f`  
		Last Modified: Fri, 15 Aug 2025 17:45:43 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:24-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:709b8ff88e21fcaf580b5447f5e86904f25e95236b158807f11233a6b45981f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15782807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:532c78b9b1759a80cc43165e5998bd5de097628e0b7f2062963679864266ef6b`

```dockerfile
```

-	Layers:
	-	`sha256:73fe4b24a7b6ac08f670bf7396247456a06bcf713ac82e5512b67648082b052a`  
		Last Modified: Fri, 15 Aug 2025 18:39:52 GMT  
		Size: 15.8 MB (15759718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5efc5e37e340f2a301de84f087634d26beaf58d705947d2a781c0f77870fc0d5`  
		Last Modified: Fri, 15 Aug 2025 18:39:53 GMT  
		Size: 23.1 KB (23089 bytes)  
		MIME: application/vnd.in-toto+json

### `node:24-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:addd4368db407d199775d126e67561ae26cf01f381d592d88bc397eba0a4e2f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.5 MB (374521104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8c374ac97d171b3fc7a8308da3da80d1e8da7781444900a733d440a8cd2eb16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV NODE_VERSION=24.5.0
# Fri, 01 Aug 2025 10:06:16 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENV YARN_VERSION=1.22.22
# Fri, 01 Aug 2025 10:06:16 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 01 Aug 2025 10:06:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Aug 2025 10:06:16 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25635cbca821869ea9220087d35fa6b59e758fb2dca635f36530cb5e44b7c481`  
		Last Modified: Wed, 13 Aug 2025 07:20:06 GMT  
		Size: 15.8 MB (15750676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06836ab0250fb74efa819c381a3a62f540817c74a1d0468d4e03f53c6b03758a`  
		Last Modified: Wed, 13 Aug 2025 15:28:22 GMT  
		Size: 54.9 MB (54856134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d454c8e58c4069692ce41e243c84f24682d348d8667ce5764628f03111249d`  
		Last Modified: Thu, 14 Aug 2025 00:15:27 GMT  
		Size: 190.1 MB (190058369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb59ee0e15b514e0b9fe6b0e45a92aacf914fa0a3e8e72d12c86a9c4e419963b`  
		Last Modified: Thu, 14 Aug 2025 03:48:51 GMT  
		Size: 4.1 KB (4099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb03494abc58547071d2464b6e37e71448193c7e3d7a227c937dcae912dc94d`  
		Last Modified: Thu, 14 Aug 2025 03:48:53 GMT  
		Size: 60.4 MB (60352295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e688390a7f6bd43e69cdaca78478d92dc2fbfd5551de9d9605c36c3e79c1a856`  
		Last Modified: Thu, 14 Aug 2025 03:48:51 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e9bad680f7ef393a86f1a288fc00d60e12bc0d1d552b5256151576a957a0ab`  
		Last Modified: Thu, 14 Aug 2025 03:48:52 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:24-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:1c8540220db9086a96865c5f9a855c549c5ca19472fe98d86b7077318423b4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15784934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633d4cfdb71201023fc71f7ce00984e7d384488359af5bebd0bc59bbf8c4de54`

```dockerfile
```

-	Layers:
	-	`sha256:321981b623ae1a6ac9b6303bbc9d0e5f3fd07dfba80172777dcc6d681bda8d1c`  
		Last Modified: Thu, 14 Aug 2025 06:40:38 GMT  
		Size: 15.8 MB (15761699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cca10eb3d091958bf7fb7d05171bf6437444d07eb9899a45f7f8d1c2d4d790d6`  
		Last Modified: Thu, 14 Aug 2025 06:40:39 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json
