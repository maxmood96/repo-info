## `node:16-buster`

```console
$ docker pull node@sha256:83caf672d71f2f62b3afbc90450f50eee0c7f3409c6187ed273839a0aae4c19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `node:16-buster` - linux; amd64

```console
$ docker pull node@sha256:b5d0c4ac87defdb664254d48b50e75015ead413bf16365bde9110f4a5054a9b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349315221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a307306f720eac5dac3cd2ad1d45a43ab799991d5bf5b4504e01c66b32934e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:33 GMT
ADD file:dc52371b5f4608e5887e8c657ff951d1895e0047960f44b153c4a55ebf1726d5 in / 
# Thu, 09 Feb 2023 03:20:33 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:12:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:12:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 09:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:13:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 11 Feb 2023 01:49:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 17 Feb 2023 18:27:14 GMT
ENV NODE_VERSION=16.19.1
# Fri, 17 Feb 2023 18:27:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Fri, 17 Feb 2023 18:27:27 GMT
ENV YARN_VERSION=1.22.19
# Fri, 17 Feb 2023 18:27:30 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Fri, 17 Feb 2023 18:27:30 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 17 Feb 2023 18:27:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 18:27:30 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:b2404786f3febb4866f85b0c8f52b0b0b94dfdb6543e94cd65f961c68f325ff7`  
		Last Modified: Thu, 09 Feb 2023 03:25:32 GMT  
		Size: 50.4 MB (50449613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ef50ee5a8f962aeac812883159a9ffe3f00819fcb446f0b1fc87d7060e16e`  
		Last Modified: Thu, 09 Feb 2023 09:19:04 GMT  
		Size: 7.9 MB (7861254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb1477a1a0e7cfeb697ce3d2aae0e31f6af42409c4581a3c23e0df0b832da6f`  
		Last Modified: Thu, 09 Feb 2023 09:19:04 GMT  
		Size: 10.0 MB (10001378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838447eff6a7c0b7b49fd5248bd06fe00feedb8f836c346bf3a58c0516a9502d`  
		Last Modified: Thu, 09 Feb 2023 09:19:21 GMT  
		Size: 51.9 MB (51869925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f659024e304142fe11bb0455df68c5526e9bd397bffc0af9947e8d09078b28`  
		Last Modified: Thu, 09 Feb 2023 09:19:53 GMT  
		Size: 191.9 MB (191923525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6a3fa7db3be04d1c23c4bab6c756cfc83d12b84903547b94d340388d748bdd`  
		Last Modified: Sat, 11 Feb 2023 01:55:34 GMT  
		Size: 4.2 KB (4205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dc0836661e82f742e5b18fabdbb7c8d5a30ac149fe5a9bb12093e137fd83c1`  
		Last Modified: Fri, 17 Feb 2023 18:40:19 GMT  
		Size: 34.9 MB (34929218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fe983bf72718bc4683668f8a3ff7955364d5cf93f499addb338a092a72c14b`  
		Last Modified: Fri, 17 Feb 2023 18:40:15 GMT  
		Size: 2.3 MB (2275651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8857b94166a8d5f1cb67820067392c0c30467e27d5d6853f84d126bb1f2aa881`  
		Last Modified: Fri, 17 Feb 2023 18:40:14 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:16-buster` - linux; arm variant v7

```console
$ docker pull node@sha256:d72cb5214c2abdc42778dc1ad8ec58a312739a8512028e8e97e48e1ababcda92
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.3 MB (312312358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005a87d9c9820451f3d6628048d964f041817d29ed0e5c72a9cd5a26288ddc2b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 09 Feb 2023 06:12:25 GMT
ADD file:434e1b35b834ee1254f1ab5af684808d2738b7ce070f44565598588210f839a7 in / 
# Thu, 09 Feb 2023 06:12:26 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 17:38:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 17:38:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 17:39:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 17:40:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 10 Feb 2023 02:56:42 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Fri, 17 Feb 2023 23:05:07 GMT
ENV NODE_VERSION=16.19.1
# Fri, 17 Feb 2023 23:05:24 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Fri, 17 Feb 2023 23:05:25 GMT
ENV YARN_VERSION=1.22.19
# Fri, 17 Feb 2023 23:05:28 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Fri, 17 Feb 2023 23:05:28 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Fri, 17 Feb 2023 23:05:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Feb 2023 23:05:29 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a7cf8e1360b682d042f81c22ae6f7c6aa270e84e27f8ee36d91af13052431c38`  
		Last Modified: Thu, 09 Feb 2023 06:19:43 GMT  
		Size: 45.9 MB (45916628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71aa5f9f66c35e93fcb2f3f4fc4b73a17c2a877cd1b6f90918a21a4f8f5f265a`  
		Last Modified: Thu, 09 Feb 2023 17:48:25 GMT  
		Size: 7.1 MB (7148015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a1986226d79ecbd4a3c24fe5a49ab2935c273ad7f050f716d4b552d2557b63`  
		Last Modified: Thu, 09 Feb 2023 17:48:25 GMT  
		Size: 9.3 MB (9349010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093b7e80e1c5ee592d1711142c0899b7ea1138f7f9278a69d39250fbde51e1db`  
		Last Modified: Thu, 09 Feb 2023 17:48:44 GMT  
		Size: 47.4 MB (47397187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:530cc523cabce61c59977d71780b2378eab5d7bbfd3181276308a289af674783`  
		Last Modified: Thu, 09 Feb 2023 17:49:22 GMT  
		Size: 168.1 MB (168105696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc6338165a602563217c32ef078902322c9cba39c7dbe509f8c16cf25926cf`  
		Last Modified: Fri, 10 Feb 2023 03:08:50 GMT  
		Size: 4.2 KB (4166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e385aa1fe144fedf4b7b80490c9ada4bc115c53fd3cfe14062179d27bdecba31`  
		Last Modified: Sat, 18 Feb 2023 00:33:49 GMT  
		Size: 32.1 MB (32123870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59adac2eadb998220685c61495fa66748516bc67ea64fb76c0986c7e23e42d25`  
		Last Modified: Sat, 18 Feb 2023 00:33:40 GMT  
		Size: 2.3 MB (2267333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7793688c8bb9d21802ff5ef8a9c0d75fe11f4bb8e1947a4aa19b641b57065ddc`  
		Last Modified: Sat, 18 Feb 2023 00:33:39 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:16-buster` - linux; arm64 variant v8

```console
$ docker pull node@sha256:93d9a097ac15cad2230266625f0c87241a05be52b1e029ca5f74d1a66544858c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.1 MB (340094017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a54819887907fc08422ee7dd07fc9c4b064ef6002553833b4dc2cc61aa74f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:46 GMT
ADD file:bf5b2f8cbddd98de6093dde190b043c3e2b58a5063d1acec0aba091e7d203dbd in / 
# Wed, 01 Mar 2023 02:20:47 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:50:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:51:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:52:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 05:07:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 01 Mar 2023 05:11:44 GMT
ENV NODE_VERSION=16.19.1
# Wed, 01 Mar 2023 05:11:55 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 01 Mar 2023 05:11:55 GMT
ENV YARN_VERSION=1.22.19
# Wed, 01 Mar 2023 05:11:58 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 01 Mar 2023 05:11:58 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 01 Mar 2023 05:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Mar 2023 05:11:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:06cfbde07ccb39d53563bd87f3c2b50f04ddd0c8f6cd52be3c7089a3413688e1`  
		Last Modified: Wed, 01 Mar 2023 02:24:34 GMT  
		Size: 49.2 MB (49240002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a788623352140f16227efacfe9a8b497cf91ee63fa69554615640474975ca5`  
		Last Modified: Wed, 01 Mar 2023 02:57:17 GMT  
		Size: 7.7 MB (7731356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12086fb08985806514ae1e77eef44a12e303bd44b113e62dac28b16b778fc797`  
		Last Modified: Wed, 01 Mar 2023 02:57:17 GMT  
		Size: 10.0 MB (10003642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afc4bf76406adbdc8533ba0c416f2aac77ca7db02bb6d380eaeeb778f56c5d4`  
		Last Modified: Wed, 01 Mar 2023 02:57:32 GMT  
		Size: 52.2 MB (52192055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7fd78b041bf9263b5362da19c99f8256c7954621d32679777cd6fcd99d86a`  
		Last Modified: Wed, 01 Mar 2023 02:57:57 GMT  
		Size: 183.5 MB (183499167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a83710638944249b4a30c8f9a140d1bdbc61a14312593b93194396993693e9d`  
		Last Modified: Wed, 01 Mar 2023 05:18:08 GMT  
		Size: 4.2 KB (4208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc9fe7c84ef1f9d2d78b1bf7c374c4cc748955f62a806070f387dc052db587e7`  
		Last Modified: Wed, 01 Mar 2023 05:21:29 GMT  
		Size: 35.1 MB (35147548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d33dc365a2bea65a0d8cdc99afe164c76dfae17f1a3a10526c3f255db5ee48`  
		Last Modified: Wed, 01 Mar 2023 05:21:25 GMT  
		Size: 2.3 MB (2275589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff1bd53c8969afc20f1446bc017341b431028daa499a83ff46615b223fc15c06`  
		Last Modified: Wed, 01 Mar 2023 05:21:25 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
