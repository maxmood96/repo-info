## `node:18-bullseye`

```console
$ docker pull node@sha256:18771cbc2ddf2fa1b11ff793fcc12e583f7cc4599c2d5f9ab776e7e83e4aa42f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:18-bullseye` - linux; amd64

```console
$ docker pull node@sha256:8a9a7e0483bac3ede4c8219aa9e4fdc5ffb7ee22f1713ff3d40c641e33a7865a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368305697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36fa9401c30918acb171ffb425a9f5346a403124e2adc5f8ad1495e576cc33f1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENV NODE_VERSION=18.20.8
# Thu, 27 Mar 2025 14:23:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 27 Mar 2025 14:23:08 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 14:23:08 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Thu, 08 May 2025 17:04:45 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Thu, 08 May 2025 17:04:40 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Thu, 08 May 2025 17:04:55 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee2c8b84461fce714721ac74cb275f6aaa0de67c2aeaccb8193af9ea8b4d38`  
		Last Modified: Thu, 08 May 2025 17:04:52 GMT  
		Size: 197.1 MB (197107708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ab477d3a3bb033820eba7bf28c4fe4b4c75e9c4ef8a99a647207af30a8e341`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 4.1 KB (4088 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa1e1a8a5f6fd18da84aefec2022bc9855c5d0296eeee9aa72793caaeace845`  
		Last Modified: Thu, 08 May 2025 17:05:05 GMT  
		Size: 45.7 MB (45675494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1e2de4035f4a1ae17f3bf3235b0b80510983b80ee360c5987e248329900c3f`  
		Last Modified: Thu, 08 May 2025 17:04:56 GMT  
		Size: 1.3 MB (1250671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb8b81d76c87d36b08cd10211c680737582d7f7c48f070190ca2b183b07ead7`  
		Last Modified: Thu, 08 May 2025 17:04:57 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:18-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:32a7604ca1c38159dec315b635576cb18b361e2463bdaef7eec12b51b1a57cf1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15384594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dad62dbd75ab1adb80575255b268a0d785fbf00a7815df8ae0fb43a9ee549b4`

```dockerfile
```

-	Layers:
	-	`sha256:c038e2f388a23130d3bd066db1d104089fe9a7753e6f2bfe9c791c41f459f431`  
		Last Modified: Tue, 29 Apr 2025 00:11:35 GMT  
		Size: 15.4 MB (15362324 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd80e0fa8ee30865bb770f8ed64c9e6b908c5999034d162f5cb83db2a9e218c9`  
		Last Modified: Tue, 29 Apr 2025 00:11:34 GMT  
		Size: 22.3 KB (22270 bytes)  
		MIME: application/vnd.in-toto+json

### `node:18-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:7dca0a55e965e29ca532814185288396ac8df34d5d3edbc7c4e67eb60c9c28ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325688698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e3b2101592d913badbcfdd0a47d4f45b8014583e47fc18609937566402739e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENV NODE_VERSION=18.20.8
# Thu, 27 Mar 2025 14:23:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 27 Mar 2025 14:23:08 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 14:23:08 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:72fa46f1d669ee2de1ffbc36b654bfe8dd0aad49156f4143a5d9edd3a5c3d559`  
		Last Modified: Thu, 08 May 2025 17:18:11 GMT  
		Size: 49.0 MB (49040048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64850f276e76efd1e91be51cb4b2577218e49bf52707b1bf6de3be76028cd8`  
		Last Modified: Thu, 08 May 2025 20:08:04 GMT  
		Size: 14.9 MB (14879026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc4cecedb434598f97e33a3320b6af6e1676388e6c13b31f0aab4b7c9372012`  
		Last Modified: Thu, 08 May 2025 20:08:14 GMT  
		Size: 50.6 MB (50625161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce34362265f33a06975f249d19b3ebf3e131e052b1333868e863a53ee816bc45`  
		Last Modified: Thu, 08 May 2025 20:10:03 GMT  
		Size: 167.6 MB (167558886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a1fa7603036005ea1a357719d15ef3a839b85b2e27d743c09b2bb48ce67b7f4`  
		Last Modified: Thu, 08 May 2025 23:05:00 GMT  
		Size: 4.1 KB (4076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a48b9e745b90e735d5aaf4d49018e3afe57eaf0f30612b49bd96e03812bd0a`  
		Last Modified: Tue, 29 Apr 2025 20:44:50 GMT  
		Size: 42.3 MB (42330378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc4cdd5fbd58f45ef0d5bb168c5647ab5d5feceb7be84f961fca0bd5b7a2357f`  
		Last Modified: Tue, 29 Apr 2025 20:44:48 GMT  
		Size: 1.3 MB (1250676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f3cbac6de22c6621fc621d0c03779d34a74526bd7480f4ad7e53a34dae036c`  
		Last Modified: Tue, 29 Apr 2025 20:44:48 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:18-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:389132a8cc2f15ace7f4ffdad942efe59e1ae2f29ab99c68458d1bc53525312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15185477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec91b1e98f0020046107ae821c8a68d48cc3055e6f83a87cbb41ff0988989c96`

```dockerfile
```

-	Layers:
	-	`sha256:abe7880d0b31108b073c9318b76fa92341814da001310bcb758aef1065e0054e`  
		Last Modified: Tue, 29 Apr 2025 20:44:48 GMT  
		Size: 15.2 MB (15163105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b14b22093c69d4364ae37b693c67519a111034ae0eedcc0fb7b43edf17a4c1bc`  
		Last Modified: Tue, 29 Apr 2025 20:44:48 GMT  
		Size: 22.4 KB (22372 bytes)  
		MIME: application/vnd.in-toto+json

### `node:18-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:716b8e65be11e8a9e7c06d7a2fcff52a892558b403f8555c1be4e5cb2bd16eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359855486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30670fa223d46867f567d14d29bb2004e9848f6352cb3ead5aa42ff87d64db1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENV NODE_VERSION=18.20.8
# Thu, 27 Mar 2025 14:23:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENV YARN_VERSION=1.22.22
# Thu, 27 Mar 2025 14:23:08 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 27 Mar 2025 14:23:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 27 Mar 2025 14:23:08 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:9ce0153b823c3af508e9c8a003aa35daca140e8f4578ff2a451ac20469ea739a`  
		Last Modified: Thu, 08 May 2025 17:08:39 GMT  
		Size: 52.2 MB (52245979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d4b10bbe754ef0579f7ae8162881d71484a39910114f01fdcee0bc53987fec1`  
		Last Modified: Thu, 08 May 2025 17:09:23 GMT  
		Size: 15.7 MB (15749108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2b30b3b7ef57604d52a4f287f3a1202fa7094c2c34ba89e66f13f2ef75a47ae`  
		Last Modified: Thu, 08 May 2025 17:09:26 GMT  
		Size: 54.9 MB (54850001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356545a2ed16b26897f2a271b3f4a7d7e64a9bf9bc0c78fdf4f1386401e37428`  
		Last Modified: Thu, 08 May 2025 17:09:35 GMT  
		Size: 190.0 MB (190024328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503f70a0d4a3a723dc95c8e69a772d359515e8c5b1831496046f7cbe06b78597`  
		Last Modified: Thu, 08 May 2025 17:09:24 GMT  
		Size: 4.1 KB (4094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d556fcade26cdf182a9dc311d76bfa5ac652a55c7f9d562a412b053b967559e`  
		Last Modified: Thu, 08 May 2025 17:10:40 GMT  
		Size: 45.7 MB (45730858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4585269bceb17891fd01815ae03329a9e2d77073b206d736a02b98b07182c6ed`  
		Last Modified: Thu, 08 May 2025 17:10:36 GMT  
		Size: 1.3 MB (1250672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e39b93eadf02a9ca4b8d44313429277298c503fb8c6e9e816605b8115f1df21e`  
		Last Modified: Thu, 08 May 2025 17:10:35 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:18-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:4766ea1f1af5885b5da7b16d749e2cc33391ee3201836c079c295006a83ac0d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15386986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d36ccc04d9691d577680d2773f22c97f2f7b16e7b384b079c59c260b10a852e`

```dockerfile
```

-	Layers:
	-	`sha256:f70a48731932f59839c68b2065d0007fb8abdaab064a4e586936b8c8594c434c`  
		Last Modified: Wed, 30 Apr 2025 07:04:43 GMT  
		Size: 15.4 MB (15364582 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87c33d6ae18cf824c46462ee4716759ce8b2dbbd94963ef8540624184e53f897`  
		Last Modified: Wed, 30 Apr 2025 07:04:42 GMT  
		Size: 22.4 KB (22404 bytes)  
		MIME: application/vnd.in-toto+json
