## `node:iron-bullseye`

```console
$ docker pull node@sha256:fba4714ef5a7acbbddc490bd2cbe17dc87a6fb6beaf2dc6ce89384694ff6f36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `node:iron-bullseye` - linux; amd64

```console
$ docker pull node@sha256:90dde169ad58317837c7d65b9befc51f9dcf1221578ffe9668b64cebcddcf868
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.3 MB (372346083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc71000442dcdaf87cb062d28b4cdfa40e2dc0044b592bd535ce01eecb582d0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:20:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:21:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:22:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 09:32:03 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 25 Oct 2023 18:27:54 GMT
ENV NODE_VERSION=20.9.0
# Wed, 25 Oct 2023 18:28:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 25 Oct 2023 18:28:13 GMT
ENV YARN_VERSION=1.22.19
# Wed, 25 Oct 2023 18:28:16 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 25 Oct 2023 18:28:16 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 25 Oct 2023 18:28:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 18:28:16 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dedceb9c21c46986231d9dfb896b37cfc470d67799e7e919a641ac54dcc9eed`  
		Last Modified: Thu, 12 Oct 2023 03:29:53 GMT  
		Size: 15.8 MB (15764226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98dfe1ecd6ba8d7f42ee14ec8a64da6ba633ed96ac9c58f6c5a0028ce6908916`  
		Last Modified: Thu, 12 Oct 2023 03:30:09 GMT  
		Size: 54.6 MB (54595813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d198e46b4004b646fce783c4378d6841632c0fb7fb2360927673d788abfda172`  
		Last Modified: Thu, 12 Oct 2023 03:30:42 GMT  
		Size: 196.9 MB (196879362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0dd09141b2c5c048930243ee5eb476cfb6fd0ce17247e3a101987b9b962087`  
		Last Modified: Thu, 12 Oct 2023 09:35:52 GMT  
		Size: 4.2 KB (4203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac1b93861da6f3c800c9cb1eeaa354ce3d88db4ac3cf0a0fb53d8e15744c963`  
		Last Modified: Wed, 25 Oct 2023 18:37:42 GMT  
		Size: 47.8 MB (47836895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ebfb0882c5e131c224334620d8dd14079eb34eb61ca99b28a49b3c632ebeae`  
		Last Modified: Wed, 25 Oct 2023 18:37:35 GMT  
		Size: 2.2 MB (2207106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:221678f6950c70d5e855b4112c2d226953456425acfd9c04c7a703b332337be0`  
		Last Modified: Wed, 25 Oct 2023 18:37:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:iron-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:83a7cf66987002402a43742a561321f2f236b0b623a44a0869c173c0637290c2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329457054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba704bfd2ea4aa2a71f37d3d08f02a444fa713018c41e31ef26f40b832c651e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:19 GMT
ADD file:684f3634c6b747a4caad8f9f820cc02b53a2122591fe215935c5497ec234c3ad in / 
# Wed, 11 Oct 2023 17:42:20 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:47:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:47:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:48:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 09:30:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 25 Oct 2023 22:07:09 GMT
ENV NODE_VERSION=20.9.0
# Wed, 25 Oct 2023 22:07:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 25 Oct 2023 22:07:29 GMT
ENV YARN_VERSION=1.22.19
# Wed, 25 Oct 2023 22:07:32 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 25 Oct 2023 22:07:32 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 25 Oct 2023 22:07:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 22:07:33 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:33d0c7672db93e653471872c639cd6129ec25c168942e15a008c4920cafe62d7`  
		Last Modified: Wed, 11 Oct 2023 17:46:42 GMT  
		Size: 50.2 MB (50215704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe33e05af9470f2356c8047560fded363dda4990bb2d70e9194f0dca496bb82`  
		Last Modified: Thu, 12 Oct 2023 03:57:11 GMT  
		Size: 14.9 MB (14879720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0953bb94dc6fcb1dee741e8bfc886a0671f4516a04fbf1a92527c2bb1598e1dd`  
		Last Modified: Thu, 12 Oct 2023 03:57:33 GMT  
		Size: 50.4 MB (50353136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:783a8cf6b572fdf6838ef5ecf60b5713b7139f7f8e554b1ccd61d56a597e3cf7`  
		Last Modified: Thu, 12 Oct 2023 03:58:11 GMT  
		Size: 167.4 MB (167351841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d55f473b5894fd7606926038abb22f14cdcba4df0a74ef70310ded726b99490`  
		Last Modified: Thu, 12 Oct 2023 09:35:33 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523de34238b3cbe9d4e699121312962e75b955e29df474e13211d970972b40a4`  
		Last Modified: Wed, 25 Oct 2023 22:17:56 GMT  
		Size: 44.5 MB (44453113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef9eda13c62188291d214973d529ddbdd9db0cb5f2f609b7d8bff320781a2a6`  
		Last Modified: Wed, 25 Oct 2023 22:17:48 GMT  
		Size: 2.2 MB (2198899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba8ece29fb762c5871ee1afa58523654ea3ae214d6077268ecefdd5f1bbd6a5`  
		Last Modified: Wed, 25 Oct 2023 22:17:48 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:iron-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:953947302ebac39b7d521a667787472b8bd8733e6f15c87b8b2b3dbcec6a1b8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.0 MB (364000564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec1459d456901438acd25b4b6e5f5fdfe5a0ee12cdc596846b319a337c1d74f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:46:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:47:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 02:40:05 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 25 Oct 2023 20:45:07 GMT
ENV NODE_VERSION=20.9.0
# Wed, 25 Oct 2023 20:45:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 25 Oct 2023 20:45:24 GMT
ENV YARN_VERSION=1.22.19
# Wed, 25 Oct 2023 20:45:27 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 25 Oct 2023 20:45:28 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 25 Oct 2023 20:45:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 20:45:28 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7a630df11a812111dd2b7f5b819a692f2350ad055fab0cd3e60b322c2eead5`  
		Last Modified: Wed, 11 Oct 2023 19:54:57 GMT  
		Size: 15.7 MB (15749899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c8e3bce435b9fb78d2fd6a8f0ce18ddecff51902c10074a9da4287cb35963b`  
		Last Modified: Wed, 11 Oct 2023 19:55:14 GMT  
		Size: 54.7 MB (54700074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda70d4f1c4310da8eb56a83b481a5bda9d57efa32a6ef6d7915a7cf487c8ba6`  
		Last Modified: Wed, 11 Oct 2023 19:55:43 GMT  
		Size: 189.8 MB (189801508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ef1d5def490da11ece91c6d62ffb54a8048064f3daf96f1b247e3f974fcfc6a`  
		Last Modified: Thu, 12 Oct 2023 03:31:54 GMT  
		Size: 4.2 KB (4209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b59623c37df4e32d2808532bf555f4c6b4a4d7c6147e876915d841f1a77cf6`  
		Last Modified: Wed, 25 Oct 2023 20:53:57 GMT  
		Size: 47.8 MB (47829513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b432e21827fd2d4d3805c5b914fa32bcd255adc3f9483bc53ce19ac5daff7df`  
		Last Modified: Wed, 25 Oct 2023 20:53:51 GMT  
		Size: 2.2 MB (2207098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8770c09edccfa353b10701ffb3e8358b4b72199eb5bcdb690381ad522bce71a0`  
		Last Modified: Wed, 25 Oct 2023 20:53:51 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:iron-bullseye` - linux; ppc64le

```console
$ docker pull node@sha256:081db2fcb93c14549003222d9d1495e368b4ec6109aa7c1e09779e4342057a7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.3 MB (383332378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:068e2787081f42f880db5feb329a95ca34d8a7bb302661dd7aa54593b4dc1f17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 11 Oct 2023 17:44:35 GMT
ADD file:d59326770edede2ba1d2005697bf41540a3d76a4bae883b91fede9b68018630c in / 
# Wed, 11 Oct 2023 17:44:38 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:20:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:24:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 21:20:18 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 25 Oct 2023 20:14:45 GMT
ENV NODE_VERSION=20.9.0
# Wed, 25 Oct 2023 20:15:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 25 Oct 2023 20:15:11 GMT
ENV YARN_VERSION=1.22.19
# Wed, 25 Oct 2023 20:15:15 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 25 Oct 2023 20:15:15 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 25 Oct 2023 20:15:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 20:15:16 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6613fa9f09034273d2b35a47386f8d53c77953a73e561b9f189ffa43ea17bd54`  
		Last Modified: Wed, 11 Oct 2023 17:50:25 GMT  
		Size: 58.9 MB (58929717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565fd5d2ec4119e0cef3217e4496512c36e4adc4e98567f565f105e684e80c4e`  
		Last Modified: Wed, 11 Oct 2023 18:38:00 GMT  
		Size: 16.8 MB (16765485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac6ae11620e817afc07c304ae67f21276148cc99a42e4ac56d481faceb27146`  
		Last Modified: Wed, 11 Oct 2023 18:38:24 GMT  
		Size: 58.9 MB (58866926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e868ed372aa88cb7b1880038e68bff4def65e8692014745f7a779d67797a8527`  
		Last Modified: Wed, 11 Oct 2023 18:39:18 GMT  
		Size: 196.2 MB (196248657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448e4a7713ba8890614bfd441815d3d011797bddc8e9f20cfc9e3d9ebb022dc6`  
		Last Modified: Wed, 11 Oct 2023 22:18:34 GMT  
		Size: 4.2 KB (4204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e437af7d01243cc028e036f544e4cb6d22b90f04d836d1ccb1ba3f824165331`  
		Last Modified: Wed, 25 Oct 2023 20:24:16 GMT  
		Size: 50.3 MB (50309801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f56f3355ac5f5220a2e673de99427a5c1e7cf6d68c2266fb4afbb22da5c7cd0`  
		Last Modified: Wed, 25 Oct 2023 20:24:07 GMT  
		Size: 2.2 MB (2207135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65502d26f3b4631438b0935b640e7fabc422c32c92a2380900223be3183bc9dc`  
		Last Modified: Wed, 25 Oct 2023 20:24:06 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:iron-bullseye` - linux; s390x

```console
$ docker pull node@sha256:4f8437ceec91bfe32c892c7449f054dabd71e7ed39a7d73298112a11d4d1468c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345789268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1164700fed2cf0de64092295733e37dbdefc18e3030794989d029720197a4d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 11 Oct 2023 17:50:40 GMT
ADD file:bb3ee20a7ddf364b23163c517132146872491e85ef2f1465bf7fd2ed33f94827 in / 
# Wed, 11 Oct 2023 17:50:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 23:58:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 23:59:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 00:03:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 02:05:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 25 Oct 2023 22:05:13 GMT
ENV NODE_VERSION=20.9.0
# Wed, 25 Oct 2023 22:05:30 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 25 Oct 2023 22:05:37 GMT
ENV YARN_VERSION=1.22.19
# Wed, 25 Oct 2023 22:05:40 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 25 Oct 2023 22:05:40 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 25 Oct 2023 22:05:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 25 Oct 2023 22:05:40 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:e651436ffb848f56da62cd2c80f206a288b94da8113c4c23a7e5502fb597ce23`  
		Last Modified: Wed, 11 Oct 2023 17:56:38 GMT  
		Size: 53.3 MB (53296378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a52fe3127c9c85c0c5e50b52a035e6bcee230e0c38db795abfee4b60522f157`  
		Last Modified: Thu, 12 Oct 2023 00:35:16 GMT  
		Size: 15.6 MB (15640232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e9fa5eede43b49ed76d5e09e5c978ac8b2296773dad3161eae081bba447e45`  
		Last Modified: Thu, 12 Oct 2023 00:35:44 GMT  
		Size: 54.1 MB (54066239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d404a1f00add5fb24f6224adfac012cf688caba0fb9eb52c82c499b84498b414`  
		Last Modified: Thu, 12 Oct 2023 00:36:17 GMT  
		Size: 172.9 MB (172891128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88c2737160d002e423816a60738a47fe403be088b1c8b19d75f0a38b22398c4`  
		Last Modified: Thu, 12 Oct 2023 04:27:13 GMT  
		Size: 4.2 KB (4209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37ddb42c1ba6e9e2f5aa2f0d88f6c1a62de1d30d17ba1a729eb72745c5054e37`  
		Last Modified: Wed, 25 Oct 2023 22:13:10 GMT  
		Size: 47.7 MB (47681632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcbef925a860a322b4d40af13d0404fe0df44ee982f4316a2f7aefbf96bbd02`  
		Last Modified: Wed, 25 Oct 2023 22:13:03 GMT  
		Size: 2.2 MB (2208998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdf6fe319d90c13b774c392afd78e6d269f6742863033d1c65ad09b8904ca69`  
		Last Modified: Wed, 25 Oct 2023 22:13:03 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
