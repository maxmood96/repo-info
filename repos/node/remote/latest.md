## `node:latest`

```console
$ docker pull node@sha256:1745a99b66da41b5ccd6f7be3810f74ddab16eb4579de10de378adb50d2e6e6f
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

### `node:latest` - linux; amd64

```console
$ docker pull node@sha256:8b2b79dcd4164985acb914c82222c2a1e8277399a2b02c681109a04327baaf5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.5 MB (406475153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b536d17a0f8a33c85b1ad262f50d3ffd82446c46c2240ba7657b9e66f3817d8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0a96bdb8280554b560ffee0f2e5f9843dc7b625f28192021ee103ecbcc2d629b`  
		Last Modified: Tue, 24 Dec 2024 21:32:13 GMT  
		Size: 48.5 MB (48497066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54c7be425079efba0003054ee884bf72f1ffebca733bedd6f077d2809ee9aa6f`  
		Last Modified: Tue, 24 Dec 2024 22:15:27 GMT  
		Size: 23.9 MB (23865817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aa8176e6d893aff4b57b2c22574ec2afadff4673b8e0954e275244bfd3d7bc1`  
		Last Modified: Tue, 24 Dec 2024 23:16:06 GMT  
		Size: 64.4 MB (64391074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1523f4b3f5602bf41caf8d8e649536ac0b3e56984c81a9f518fb20c6516ca075`  
		Last Modified: Wed, 25 Dec 2024 00:14:20 GMT  
		Size: 211.3 MB (211306201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4750555286bf39334e46fe234e32dd75330a37d165b081c33f8e732164744c`  
		Last Modified: Wed, 25 Dec 2024 01:16:01 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6e53e173f1a1a5e0d1e103944f56e65085c9a77b50cf1fae147edaea0e7ba9`  
		Last Modified: Wed, 25 Dec 2024 01:16:02 GMT  
		Size: 57.2 MB (57160494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d51d3fd8ab39481c52cd9474ac6314f91cd67494112cc293cef62beb07e25c2f`  
		Last Modified: Wed, 25 Dec 2024 01:16:01 GMT  
		Size: 1.3 MB (1250735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b99c0c66ceafcca5439fcbad64a95db5d77613864175aa9d56233c67901da16`  
		Last Modified: Wed, 25 Dec 2024 01:16:01 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:latest` - unknown; unknown

```console
$ docker pull node@sha256:4725594cae7f479b4e4b4179d5cba36d5769c0bb9866187909119adfdd294448
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15802680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed061e5a10e90724e11da2697954ff65d4fedcf04c9140aa4d8f5f1d42dafdc4`

```dockerfile
```

-	Layers:
	-	`sha256:e62cd55430d8e875cf8dfcbd18e16d9737972a6cf14cccb4dcccf864091a1c31`  
		Size: 15.8 MB (15778661 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4563bd103b5506865936730b789842fdcf2b06de66c756e2076e1bf1df07eeb`  
		Last Modified: Wed, 25 Dec 2024 01:16:01 GMT  
		Size: 24.0 KB (24019 bytes)  
		MIME: application/vnd.in-toto+json

### `node:latest` - linux; arm variant v7

```console
$ docker pull node@sha256:ba0b3fe45c3713b9cfcbfe845f923526789ab2787e329feceae247eac6ff8976
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.9 MB (353946304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dea8f0a89cde14dce092f2be54de8d73be6d5b638308231fb44a77962feeb514`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:e5492f1033203c78872d1ddcc5f604ba35c18b30ac50e9f89180b9d7dfa33fb9`  
		Last Modified: Tue, 24 Dec 2024 21:33:33 GMT  
		Size: 44.2 MB (44199967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd0b2553b5f713f3599802646253e049500cbf687966d319c07d85faa64679`  
		Size: 21.8 MB (21767217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcaf98fafca7f2bb5e42aa0418e5ad79c885f1afd75a0c044855cb3f9f482cb6`  
		Size: 59.6 MB (59638987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e83d023041aaecc65d16b7b91769e4928cb4f4f650899a539fa07e3615ad9d8`  
		Last Modified: Wed, 25 Dec 2024 15:45:54 GMT  
		Size: 175.2 MB (175243028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea8a4fe41fa8e188cfaf6d831939831458c331463feaa16cc5fe131baa38b93`  
		Last Modified: Wed, 25 Dec 2024 19:59:10 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b164661280e3fb005fea1265e558c51b5a177d052ae29c0201fb94e5662d733e`  
		Last Modified: Wed, 25 Dec 2024 19:59:13 GMT  
		Size: 51.8 MB (51842603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cdbdd15bdeb3076a69b935e5a3d14698171e35d9f1235e5041130a08cfd9770`  
		Size: 1.3 MB (1250734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb8951c573df5fdb9b065bebaeb168ff513903f0798a47271b9d6edc071b369`  
		Last Modified: Wed, 25 Dec 2024 19:59:10 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:latest` - unknown; unknown

```console
$ docker pull node@sha256:adbae168a51e410ab68e910f5dfae64c51aefd418eceea5ddc3ea6fb9adc491a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15607278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ae825f2549b86587d494cc88f6bd2b58cd1e16075d76561d733d2dc477f9e5`

```dockerfile
```

-	Layers:
	-	`sha256:ae792690ef350e5618708d72fb6a80e6d4c99f4bcd22f0b8f7d1c422ad78d092`  
		Last Modified: Wed, 25 Dec 2024 19:59:11 GMT  
		Size: 15.6 MB (15583109 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20239772fc7d9055940c19d74e3c3b5d7bef5e30bff5b40f92d0a0eecbb1117a`  
		Last Modified: Wed, 25 Dec 2024 19:59:10 GMT  
		Size: 24.2 KB (24169 bytes)  
		MIME: application/vnd.in-toto+json

### `node:latest` - linux; arm64 variant v8

```console
$ docker pull node@sha256:7410ae2698c596f95ec4de5de1ef036032b5cbf694d4df02e21421fbf15dbb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 MB (396680523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3f34bb865fd38bea9085f71aa6cd1d5f5c280bc4cf5c20af27a8fee88694a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:ba1dd0e85e0bf7e5cb632a24bbc3ec0060700bc5be9273b05d7e059950225037`  
		Last Modified: Tue, 24 Dec 2024 21:34:06 GMT  
		Size: 48.3 MB (48325484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b12b0dccf212c795e61e16dcc85f0caa01c231281e3287400bd334ffedb5ff`  
		Last Modified: Wed, 25 Dec 2024 01:49:19 GMT  
		Size: 23.4 MB (23405768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd63102cac360c09802a29bab13f15de711e8bd1a730d419c66110513700983c`  
		Last Modified: Wed, 25 Dec 2024 08:11:51 GMT  
		Size: 64.3 MB (64347452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e5e0e9e68b5c9172e85869f2decfc76c39919ba6ae80d8e2b597d25e854f0d3`  
		Last Modified: Wed, 25 Dec 2024 11:19:12 GMT  
		Size: 202.7 MB (202686398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9c5a973b5c3a1cc15fc8223320b63e02fa53025ed9bd75f5543031380e1deac`  
		Last Modified: Wed, 25 Dec 2024 15:10:10 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff38b4fb1289a9fc04dcb8a9c0e3e5947f0c76b7b11ea16d9fb60dbe2707d345`  
		Last Modified: Wed, 25 Dec 2024 15:10:12 GMT  
		Size: 56.7 MB (56660924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cfb6ada390bffe1ec5deee321bde26ddf37d83f087db4959e6d54938413ca13`  
		Last Modified: Wed, 25 Dec 2024 15:10:10 GMT  
		Size: 1.3 MB (1250730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdf2d9986e4feb5c7f7a599ca5797fe5b7d42889cac9e22211f7eee7634b126`  
		Last Modified: Wed, 25 Dec 2024 15:10:10 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:latest` - unknown; unknown

```console
$ docker pull node@sha256:33c283744c0d32746fc09e74961865ae5b77aa9a2309c49352739505e4c82881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15831484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9bba74bb89b4e92015e7523994a38d2b9b5c543e69b1bbadc72bc4b1c96123`

```dockerfile
```

-	Layers:
	-	`sha256:bf12289f20ad83e57bb8572ee3f26978820af70ca3886b6ffd80f05e4ea1d814`  
		Last Modified: Wed, 25 Dec 2024 15:10:11 GMT  
		Size: 15.8 MB (15807258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e7b51cf82661b26ce8a062f462b0dd497014df98744231acdfbc605ad5dec62`  
		Last Modified: Wed, 25 Dec 2024 15:10:10 GMT  
		Size: 24.2 KB (24226 bytes)  
		MIME: application/vnd.in-toto+json

### `node:latest` - linux; ppc64le

```console
$ docker pull node@sha256:eed705b70f54cc89a6e80c159e7108418f893dec3dd65d5ba4941f9370fbcd46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **422.9 MB (422875459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a92af79762c9121d18600833fd31db709ac51b610a4104886cdf2f2729222d5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:308f39459045dc7bdf1e0f0796ba6cc67e14899ab5c36afc6c0692da37a1f331`  
		Last Modified: Wed, 25 Dec 2024 09:07:26 GMT  
		Size: 52.3 MB (52328075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5a609591090f1b2fe90289666414a8be62bd40b89ccbd53d2567ba14f37f52a`  
		Last Modified: Wed, 25 Dec 2024 12:51:22 GMT  
		Size: 25.5 MB (25523681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44eb81eb15a16dd3be1309db287e3a3b8589c16f49f4938705cd78c20f9035c`  
		Last Modified: Wed, 25 Dec 2024 13:15:17 GMT  
		Size: 69.8 MB (69812237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc88116b337337204514f1443b661b30d7821092e93cc32e73d38803d573dc8e`  
		Last Modified: Wed, 25 Dec 2024 14:10:42 GMT  
		Size: 214.3 MB (214339172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa934234cbdd4c5408f18cf0925006a1ade13c7c6742caa028886ded18f54c49`  
		Last Modified: Wed, 25 Dec 2024 17:55:10 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:503e6d5b3ed3a1f3381f5c766c81993dfbafc0442a6d49cd5edc437d096db6e0`  
		Last Modified: Wed, 25 Dec 2024 17:55:12 GMT  
		Size: 59.6 MB (59617787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c41207c2857e4c35ea66b91be1345da3e3b8666cb5bfd5482a525a8ce168e010`  
		Last Modified: Wed, 25 Dec 2024 17:55:10 GMT  
		Size: 1.3 MB (1250736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9646b5b665a381481c87d7fe44047cd77c9a22ec63b72019753819d53c3176a`  
		Last Modified: Wed, 25 Dec 2024 17:55:10 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:latest` - unknown; unknown

```console
$ docker pull node@sha256:be0ec4db7406c3625e9b36387b429b0025b6b7c598a7e977cf85c3f91ed6d726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15779186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9da1cde1778258652c492cce6c8f9733cf77c61b19b22284e1ccd99a3d16ab7`

```dockerfile
```

-	Layers:
	-	`sha256:e174452936d52a9ec952b1ece135e83568dd7871f4818b69a4329f8d4adb0d6b`  
		Last Modified: Wed, 25 Dec 2024 17:55:11 GMT  
		Size: 15.8 MB (15755082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74b295e503b908a592211f1f3619f985b4c0671be798af37dc3e552853c4f4ae`  
		Last Modified: Wed, 25 Dec 2024 17:55:10 GMT  
		Size: 24.1 KB (24104 bytes)  
		MIME: application/vnd.in-toto+json

### `node:latest` - linux; s390x

```console
$ docker pull node@sha256:a353eba47c3a706ff08a0a8eb08524dfd660a4899a7d37921b35fa5626c6a4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.4 MB (375352188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66fa06c0016f95f203248a573e4f1352102428dd604012651c4eda0c2bf404f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV NODE_VERSION=23.5.0
# Thu, 19 Dec 2024 20:48:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 19 Dec 2024 20:48:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 19 Dec 2024 20:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 19 Dec 2024 20:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:29bd91c5aff546f191fe0c6a3ff3058c52bb3850131ee98a2d3fe9b96198878c`  
		Last Modified: Tue, 24 Dec 2024 21:33:12 GMT  
		Size: 47.1 MB (47149625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65c625039a5998156fd2a92e83b33c35e10b4f91017063d54d2a949d78884a65`  
		Last Modified: Wed, 25 Dec 2024 00:16:25 GMT  
		Size: 23.9 MB (23864731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2c4d6ca294087595fc1adf8f3d033945c38a166a01db670c00b336716a18a6`  
		Last Modified: Wed, 25 Dec 2024 03:29:07 GMT  
		Size: 63.5 MB (63473996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e88c95c11e135edcc3e50ddc764dd43154a7deb840aeab95b0811be73511f52`  
		Last Modified: Wed, 25 Dec 2024 05:10:29 GMT  
		Size: 183.3 MB (183324742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb317e25eafd8cd432521a7e303c3ea63d8e582c703a3719a49b53585f253dd8`  
		Last Modified: Wed, 25 Dec 2024 08:42:58 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f7fb64958076562511a13849c587e61af20ce3e5f275dafc08da086b15abefe`  
		Last Modified: Wed, 25 Dec 2024 08:42:59 GMT  
		Size: 56.3 MB (56284601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871550bed584ea258b58ede67143dca1889976c07a0ac172d4aff6462cc4d329`  
		Size: 1.3 MB (1250731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b697497591d935d3813be43825dc9b45e3e1098f8a35f57015b002067f14eb`  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:latest` - unknown; unknown

```console
$ docker pull node@sha256:25d40cc6047b2c685754ae3adf032021d6c4ef01dbd49507d0ce7a5175ac14a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15615369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbb9c01987f097b51c0ff5364b1f1abae74b8faf726bf2d279ae7d75f8dfd8b`

```dockerfile
```

-	Layers:
	-	`sha256:2302970e0d50ed60ad5607d85aefc4dbe23b3ef0862c147a97c8c3165a8bec38`  
		Last Modified: Wed, 25 Dec 2024 08:42:58 GMT  
		Size: 15.6 MB (15591351 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d64d6678ade46fc93bd1193541ce7b6b22d65468ef8561684dead3a10dd54596`  
		Last Modified: Wed, 25 Dec 2024 08:42:58 GMT  
		Size: 24.0 KB (24018 bytes)  
		MIME: application/vnd.in-toto+json
