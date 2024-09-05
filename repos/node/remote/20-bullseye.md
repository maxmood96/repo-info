## `node:20-bullseye`

```console
$ docker pull node@sha256:440548809ee8022a902a9774d3c61b947cde94f6052298e5e26d4e8ec0d5d791
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 10
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:20-bullseye` - linux; amd64

```console
$ docker pull node@sha256:b607ac95dad2868eb73f0163b759323fda57d58c79044847b13e2259fde247e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.0 MB (372046522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9333ea04182e449b8058150d768007dd407f7defcc1b47f2c752ebc3caba67ac`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 21 Aug 2024 19:04:33 GMT
ADD file:e1bdcceaa316a43ad58ce8cf054a8e89ecf5a0dbae8125eb85e9b26fdb2fca2b in / 
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV NODE_VERSION=20.17.0
# Wed, 21 Aug 2024 19:04:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV YARN_VERSION=1.22.22
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:ba83bbfca9443648a883d1404b33faa0f5e096a99a2b683e3bbaee8912bca845`  
		Last Modified: Wed, 04 Sep 2024 22:34:34 GMT  
		Size: 55.1 MB (55081329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48e779000ed269823143d5ce9acd3ef6f6ff7465222482f7b02c10ba21f448cc`  
		Last Modified: Wed, 04 Sep 2024 23:02:18 GMT  
		Size: 15.8 MB (15764398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d691dff6d17d00b0cbbc4772eb805d97e02504d89ea3e5857cb97c943b74462`  
		Last Modified: Wed, 04 Sep 2024 23:02:33 GMT  
		Size: 54.7 MB (54726023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54cfd30604666dfdd92bea930c06ee58dc927e0da651b862491af1648a4aca73`  
		Last Modified: Wed, 04 Sep 2024 23:03:03 GMT  
		Size: 197.1 MB (197067753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e636b1d2ef21d4eb1cad42b74c737dd5856d40f409654a8e9fe7e525c0d61ef`  
		Last Modified: Thu, 05 Sep 2024 00:16:42 GMT  
		Size: 4.1 KB (4083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3863845dc08084ec6b9a84ef79fdc89b2f723c294cb6d6d49369ff53cd27ee1e`  
		Last Modified: Thu, 05 Sep 2024 00:16:43 GMT  
		Size: 48.2 MB (48151816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58ecaf6542ec672f97fbb6a6d8dd4be9dd5453b6a8fb5d111058bab463f9f54e`  
		Last Modified: Thu, 05 Sep 2024 00:16:42 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343f563c5c1c305eda6320cbdd0f5de2f5194376d087ae386ec156328927ae7`  
		Last Modified: Thu, 05 Sep 2024 00:16:42 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:4bdcf599a29091a283b04d34e6a5be834f9d2454ee19e947fdeca1947726d2c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249941e19361d1ba7cff85343fbeabc33e630998899a573e1d366b2ce23b18c9`

```dockerfile
```

-	Layers:
	-	`sha256:800d54e92dcc5718d5841610877891edf95cca98e4fc74c71c3205e039fb1f7d`  
		Last Modified: Thu, 05 Sep 2024 00:16:42 GMT  
		Size: 15.3 MB (15317777 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b028358ce5009141f74e0b553f0a434bf8f6b9d01f51236d3be69edfe182cf10`  
		Last Modified: Thu, 05 Sep 2024 00:16:42 GMT  
		Size: 23.1 KB (23058 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:10ba8082f511eb18541fd821a4663b0eda6a017927dde9ff61047ed9b31347cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328492569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e3dc242e76caf8984e220c56f287244834d63489e46d32aaab48e67c912722`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 13 Aug 2024 00:57:45 GMT
ADD file:7674761630f1c6dfdf95da576bd19dbfe7bc4d942d11d31eff2012ec8b2c7ff1 in / 
# Tue, 13 Aug 2024 00:57:45 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:26:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:27:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV NODE_VERSION=20.17.0
# Wed, 21 Aug 2024 19:04:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV YARN_VERSION=1.22.22
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a986643b6b9d356e3c44ee35fdd352a1064e1fb2a1524c0627e84ba34207b8e2`  
		Last Modified: Tue, 13 Aug 2024 01:01:15 GMT  
		Size: 50.2 MB (50242333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8868560f8e978ee832f67027b7330376be350ffacd30a199b730c72d9550757`  
		Last Modified: Tue, 13 Aug 2024 01:33:28 GMT  
		Size: 14.9 MB (14879497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7deb3ed53b620f0871f5051050fe0d850fd52da94803425820e75bb7b8d4e2e`  
		Last Modified: Tue, 13 Aug 2024 01:33:45 GMT  
		Size: 50.4 MB (50357748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78e6955cecd9dc8a3cc8022dd624334d4f3abc81e5801bb1a1d3ddcedd0ef645`  
		Last Modified: Tue, 13 Aug 2024 01:34:17 GMT  
		Size: 167.5 MB (167504270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7048b85418b6540ef0cbd9d56d573232d87253382988e3d7eddf65abdc4b5433`  
		Last Modified: Tue, 13 Aug 2024 12:12:59 GMT  
		Size: 4.1 KB (4076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0e4f506707b8c2f0d13f415ef5a5d7fc1996fc1a70647fe162230546b97a3d`  
		Last Modified: Wed, 21 Aug 2024 22:52:19 GMT  
		Size: 44.3 MB (44253520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdfeb02d5c21955d02449f4855a17aa13c935c44439d65f32a4a6e4274818aa8`  
		Last Modified: Wed, 21 Aug 2024 22:52:18 GMT  
		Size: 1.3 MB (1250677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbba235c3996dfece76cf0ce261c99d8f3e68d94f563e66060ab6451c3d8c694`  
		Last Modified: Wed, 21 Aug 2024 22:52:18 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:c5d3f616ad046b2755f9fdf595971ba49e202d62e3d5fde6eafc882e015242ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15141975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd1e13a371a4a0e8a2e822a64ec392cb49f7c7fdadc9f61cdda46cb17a96a64`

```dockerfile
```

-	Layers:
	-	`sha256:f9d1737d6416faaba59e1d134e3cc3cfcfee0a529948f05af1112e09b8d96aac`  
		Last Modified: Wed, 21 Aug 2024 22:52:18 GMT  
		Size: 15.1 MB (15118812 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6df48c2be6aec29238c4603f10c70aa3d925cd86bdf42c6bd3f3a710d946dd7`  
		Last Modified: Wed, 21 Aug 2024 22:52:17 GMT  
		Size: 23.2 KB (23163 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:c8c52eeb74b18e9cc74ec168840b9e5ed55ff9802891d02968e23d241a0e26bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.5 MB (363515370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5fafc9e18c93421e73be059c178539fb6e934aec3adc267775ed5d731e9c059`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 13 Aug 2024 00:39:58 GMT
ADD file:4a2aa1b23402547c558d14f98384342f2e98460b659cd211609373f5408e83bc in / 
# Tue, 13 Aug 2024 00:39:58 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:03:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:04:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:05:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV NODE_VERSION=20.17.0
# Wed, 21 Aug 2024 19:04:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV YARN_VERSION=1.22.22
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:5d8903d6126c38fefcb1196b9998da0798f56cbdf18a91c00d822144c232af6b`  
		Last Modified: Tue, 13 Aug 2024 00:43:03 GMT  
		Size: 53.7 MB (53729921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3db3ee6245513b1422983db21d89f4f743f300e726af9eff6c9f7e2dddcb67`  
		Last Modified: Tue, 13 Aug 2024 01:10:18 GMT  
		Size: 15.7 MB (15749505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5265d6983e8ed11fd8dc48e17209d3479015214ac92f89f4ac51b2e65060840`  
		Last Modified: Tue, 13 Aug 2024 01:10:33 GMT  
		Size: 54.7 MB (54694302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6073a281eb20b3b43e3cc472efa9f868c8f75fc13cae51a5b10fbe8054bc0ba0`  
		Last Modified: Tue, 13 Aug 2024 01:11:01 GMT  
		Size: 190.0 MB (189971927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32414f60f94c26bffdc07f0c72e7a29b344cdb10bd865eb30a435f624bc562cc`  
		Last Modified: Wed, 21 Aug 2024 21:59:58 GMT  
		Size: 4.1 KB (4102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:697583516166db41f1b7f52d7194c0ee40975c99889dea27ad2fe784bba76e20`  
		Last Modified: Wed, 21 Aug 2024 22:00:00 GMT  
		Size: 48.1 MB (48114497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73694675c2b615c96cb5cdb9e6b9f151b42599a1d83d1e6bbf43d823b56331d8`  
		Last Modified: Wed, 21 Aug 2024 21:59:59 GMT  
		Size: 1.3 MB (1250671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:190944566e38c54516a2ddc4e822c0613877ce31b1014e74ad4840a8538385c0`  
		Last Modified: Wed, 21 Aug 2024 21:59:58 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:1e72ba49d6e737638b0f81c3c16b1619717acb75b6cda84a58c0fc1f0d7013bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15343538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a9d07391410888ba11b86b54b24755de1f371141e22e96fda170929f16b976e`

```dockerfile
```

-	Layers:
	-	`sha256:51c4ee36bfa6fb51e9ec42bac967c73489257d9e309b216cf2c757439862204f`  
		Last Modified: Wed, 21 Aug 2024 21:59:59 GMT  
		Size: 15.3 MB (15320155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cf1a661d8232ed3d3706baf6909897ad385cec50fc2293cd0518f94ada2651e`  
		Last Modified: Wed, 21 Aug 2024 21:59:58 GMT  
		Size: 23.4 KB (23383 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye` - linux; ppc64le

```console
$ docker pull node@sha256:44f215477a17e3e5e81dcc6e42032fcd536eca33d503594d4b27c5a5b009fcad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.9 MB (382865477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8bbace37406a69d9abfda64311e9e3c09b353b0981b88ee3144d84d368467d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:14 GMT
ADD file:25dc93c8090a0afba4b41321f81883857bfdd6b30ea9f278833c5a5d9d16ad52 in / 
# Tue, 13 Aug 2024 00:22:18 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:23:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:26:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV NODE_VERSION=20.17.0
# Wed, 21 Aug 2024 19:04:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV YARN_VERSION=1.22.22
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:dad1c3eca3bf4b2a67cef1dbad507d7a913df7bbe1e3f88044230dd291ada39d`  
		Last Modified: Tue, 13 Aug 2024 00:26:46 GMT  
		Size: 59.0 MB (58954654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b50eef4accfc66462c4cf81c03bb57857b5f3ac891da5b87bfdf1ba826c9677`  
		Last Modified: Tue, 13 Aug 2024 01:36:03 GMT  
		Size: 16.8 MB (16765928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3df0e65d951ce5d0b07cbb65477bbb01cfa607241b5c5855f4fb361bedfd1247`  
		Last Modified: Tue, 13 Aug 2024 01:36:21 GMT  
		Size: 58.9 MB (58872586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9438dc035d6f851416f6745a25baa330ca04b6013564731b2c42ddce3979a2ff`  
		Last Modified: Tue, 13 Aug 2024 01:36:57 GMT  
		Size: 196.4 MB (196398494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:278616ef9292b6b023baa36dd34db6b6c6c65393135d8306374b8c4ffd469156`  
		Last Modified: Wed, 21 Aug 2024 22:03:08 GMT  
		Size: 4.1 KB (4095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61ff8e2de12297543315ae9ed0f7e9454b1b0a5831c498e0922bf448176f4c79`  
		Last Modified: Wed, 21 Aug 2024 22:03:10 GMT  
		Size: 50.6 MB (50618593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:942932859d189452045e894b6052ef70e2aed4cbc911ce0322014c32cc43e261`  
		Last Modified: Wed, 21 Aug 2024 22:03:09 GMT  
		Size: 1.3 MB (1250679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc0b15585d2f66fb90c0275e82b547aca0ad6b28151338ab2797af9a179b36d8`  
		Last Modified: Wed, 21 Aug 2024 22:03:08 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:ed1aa37db7e4f0ad4fc80725d64258bc4dbffbd8aca99e18df6e2b26fa79ce78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15310193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7f629583cb6e43285bfb028c14e213825260aa4ab8fccf1f86ee6d5544f06f`

```dockerfile
```

-	Layers:
	-	`sha256:57ab0ec8a12b0a4cb456b0fc4a3749bf3c528f8ccc4ad7e3621af8832b0592f3`  
		Last Modified: Wed, 21 Aug 2024 22:03:09 GMT  
		Size: 15.3 MB (15287086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ad7887d266d3d65d28c0821245133aa3fdc517c0803e548a81361063747024a`  
		Last Modified: Wed, 21 Aug 2024 22:03:08 GMT  
		Size: 23.1 KB (23107 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye` - linux; s390x

```console
$ docker pull node@sha256:6a9dafa94899131df2ebe79bd4063b446847c307f22f141bbadd88702c4d0ba5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.3 MB (345309024 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456d50eade2b769d2d60a4b53535e6fbddf62d3e43c38ec2d803cebe9d1a5c4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 13 Aug 2024 00:42:51 GMT
ADD file:993091e64467ec0ea9bcecdd744da64284d459b933863322bd011dd2111f47c1 in / 
# Tue, 13 Aug 2024 00:42:53 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:17:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:18:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Aug 2024 01:19:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV NODE_VERSION=20.17.0
# Wed, 21 Aug 2024 19:04:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV YARN_VERSION=1.22.22
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:9c1a2da0ad07de8657187bee6e4fad1ff817bafdbac14fb77a3953cd7f50038c`  
		Last Modified: Tue, 13 Aug 2024 00:47:43 GMT  
		Size: 53.3 MB (53324089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c695efccb58000e04eb154deca02ce22ea52fd05ee4246281c66bb7a42d20a96`  
		Last Modified: Tue, 13 Aug 2024 01:25:32 GMT  
		Size: 15.6 MB (15641934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63f3f87ffa253b4cb357637ad56494facf5bf533f6fd3bdf78f1066c6fb0fb23`  
		Last Modified: Tue, 13 Aug 2024 01:25:44 GMT  
		Size: 54.1 MB (54075217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8b49e88f43277ce63fe01761080f821f3b3be9f581e45ed6dbb50b5168642a1`  
		Last Modified: Tue, 13 Aug 2024 01:26:08 GMT  
		Size: 173.1 MB (173060876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44161e488f30fda9099b0be17e2d052b44c94e8505f4c4e6f7391b4f2df3df14`  
		Last Modified: Wed, 21 Aug 2024 22:36:52 GMT  
		Size: 4.1 KB (4095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9589f33598aa543b9f1b4498356ab8c80b112a66153b0dec949cae4304c35456`  
		Last Modified: Wed, 21 Aug 2024 22:36:53 GMT  
		Size: 48.0 MB (47951694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150d8443f1d23b23ee6867785880aaa0c2b5fd8bdba9107a294f191d5d677cca`  
		Last Modified: Wed, 21 Aug 2024 22:36:52 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4969b7e55fbbe1a9a543a3ea52e737aaaef0e4565e46797a1b37abed1f782b6`  
		Last Modified: Wed, 21 Aug 2024 22:36:51 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:36f6640ca526bd3c916727e9912eca688bcd986f437ee30d016377985c44faf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15161793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f14f440a68df8d7f33333b73e34d4ce11818dd6ee02de46b656fdba982f889b`

```dockerfile
```

-	Layers:
	-	`sha256:e2564b8249a59162e331f29774d7d1a77bf2a26f40f10c9c2fff7e8de5decfa3`  
		Last Modified: Wed, 21 Aug 2024 22:36:52 GMT  
		Size: 15.1 MB (15138734 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7523f9ecbc48f3eff62904a331a3cb4ee0a6b2aeebd8ba8d65562f2d34b3bf64`  
		Last Modified: Wed, 21 Aug 2024 22:36:51 GMT  
		Size: 23.1 KB (23059 bytes)  
		MIME: application/vnd.in-toto+json
