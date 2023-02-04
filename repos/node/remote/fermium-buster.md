## `node:fermium-buster`

```console
$ docker pull node@sha256:488426aa1a2fb9fb935d907457d9c1d3a10996efbdabc17249a2305878fd5a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `node:fermium-buster` - linux; amd64

```console
$ docker pull node@sha256:cb1f00af82464c0b258f4140719f6bf63d2f78f83361d72275a6551ef8bb06ca
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350473178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc5014e36df3751c235fe122b87110d00c7ff70fae52d6254a17b4691c6b65e8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Sat, 04 Feb 2023 06:51:54 GMT
ADD file:2f52161f98fff6a77f865fbd61397b76f3ad3391fa6d694a50a08ad43fd5c8c9 in / 
# Sat, 04 Feb 2023 06:51:54 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 07:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:24:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 07:24:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 07:25:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 09:56:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 04 Feb 2023 10:02:59 GMT
ENV NODE_VERSION=14.21.2
# Sat, 04 Feb 2023 10:03:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Sat, 04 Feb 2023 10:03:12 GMT
ENV YARN_VERSION=1.22.19
# Sat, 04 Feb 2023 10:03:15 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Sat, 04 Feb 2023 10:03:15 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 04 Feb 2023 10:03:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 10:03:15 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:d42a0fb443d7323eac0a2073d5a229cf6871c4cbddd8e85bad4b0301b2dadedb`  
		Last Modified: Sat, 04 Feb 2023 06:56:36 GMT  
		Size: 50.4 MB (50449110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f390d41539fbbd93f1f47d53f91bd33882827be2b6c7bd1aee8e0e5a3357e375`  
		Last Modified: Sat, 04 Feb 2023 07:30:33 GMT  
		Size: 7.9 MB (7861207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103b21370b9f71057fb1b91dcef9da199c272320fda90e0f449887f779b625b4`  
		Last Modified: Sat, 04 Feb 2023 07:30:33 GMT  
		Size: 10.0 MB (10001436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab930f25aaae407656553520d66a66def23df0c747402157413d83ec3726f10`  
		Last Modified: Sat, 04 Feb 2023 07:30:49 GMT  
		Size: 51.9 MB (51867959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:955f339d2cf4512ae13cf7c3f00f454c99cfcc7c4b17f1f1fdaacc8e3c60289b`  
		Last Modified: Sat, 04 Feb 2023 07:31:22 GMT  
		Size: 191.9 MB (191922928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7782f8b93a297909aa523c114c99481c5e949b4c871078af1b26d5263856d61`  
		Last Modified: Sat, 04 Feb 2023 10:07:21 GMT  
		Size: 4.2 KB (4200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc6ec011cc4830215ac441fe4e2f756b1c7e8e815573a78dd4e97be195de2b5`  
		Last Modified: Sat, 04 Feb 2023 10:12:21 GMT  
		Size: 36.1 MB (36072567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8f90116fd28cb6a0bfa8e6aec4b11a043b2972fa7482a444122b3beff33879`  
		Last Modified: Sat, 04 Feb 2023 10:12:16 GMT  
		Size: 2.3 MB (2293322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35eecea036fa6fc02b15bbaa0b87b733b5e01a2a50d707fe8e143fa45c980aa1`  
		Last Modified: Sat, 04 Feb 2023 10:12:15 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:fermium-buster` - linux; arm variant v7

```console
$ docker pull node@sha256:59226518604864bd2746b725f38097c59d48d658581548c9f2d8a927e7498067
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.5 MB (314455279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c2ca48e8c68780d5dfa63b52f3fa5e4e50a6c2a109aa73c0baebc376fff6ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 11 Jan 2023 04:00:52 GMT
ADD file:7a8ada9998422200d8f422ba7967ecc0f2435715f4b69347f7c0eddf589b1dc5 in / 
# Wed, 11 Jan 2023 04:00:53 GMT
CMD ["bash"]
# Wed, 11 Jan 2023 04:34:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:34:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 11 Jan 2023 04:35:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 04:36:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Jan 2023 07:29:02 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 11 Jan 2023 07:37:07 GMT
ENV NODE_VERSION=14.21.2
# Wed, 11 Jan 2023 07:37:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 11 Jan 2023 07:37:21 GMT
ENV YARN_VERSION=1.22.19
# Wed, 11 Jan 2023 07:37:24 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 11 Jan 2023 07:37:24 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 11 Jan 2023 07:37:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 11 Jan 2023 07:37:24 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:1af2e9dc936b1285f4472a18af1e9b913352d31b1238f1c158995d9c15b6024a`  
		Last Modified: Wed, 11 Jan 2023 04:08:13 GMT  
		Size: 45.9 MB (45915604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba37bd2b08543867db0934e29dd6c1476f71509aa0b42f10786733820b6c2008`  
		Last Modified: Wed, 11 Jan 2023 04:45:15 GMT  
		Size: 7.1 MB (7147799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe84c7428034fbe63e62868f1c420279eda084b4d396cc79161f73a9aeba29c`  
		Last Modified: Wed, 11 Jan 2023 04:45:15 GMT  
		Size: 9.3 MB (9349030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8389ce7126cbebf5244cba3ec839cd0c0cf2ff817fcc3f23a3ea989766c31570`  
		Last Modified: Wed, 11 Jan 2023 04:45:34 GMT  
		Size: 47.4 MB (47397357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f0d249ce4dfe96287ec3df755c06b871b8a6e07e954116bbd66245083477963`  
		Last Modified: Wed, 11 Jan 2023 04:46:13 GMT  
		Size: 168.1 MB (168121331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31966c78aeaf1ffaec5b54ea95e9ba54f4cd03226134a8aaaa4555ac70bc2fa`  
		Last Modified: Wed, 11 Jan 2023 07:46:46 GMT  
		Size: 4.2 KB (4163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9531ab62f6281b9489f39fa27796d2ec427eac652038267df75463b7486cb4dc`  
		Last Modified: Wed, 11 Jan 2023 07:53:49 GMT  
		Size: 34.2 MB (34235658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e1350847168e346c8447d37750d80ab00de6f2a705b52d2aaa0cf08bbfa10f`  
		Last Modified: Wed, 11 Jan 2023 07:53:42 GMT  
		Size: 2.3 MB (2283889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f40d077f02f695d29ff15ceaf83806d16c971e6486973ee2482dd5724fa8289`  
		Last Modified: Wed, 11 Jan 2023 07:53:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:fermium-buster` - linux; arm64 variant v8

```console
$ docker pull node@sha256:771a7fd41b51c8d686ee1ad8c90b69f1c8ad0e5a5863017bfe36add707c6b916
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.1 MB (341128983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c99510488fb5876138ccc0f2d087b3e97c9d8b2f703e8c3eb43e5cbbfe1cfc50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Sat, 04 Feb 2023 06:17:45 GMT
ADD file:0241487c3fb43506be1511724644c00339c32361e6b4c21a224d7190e4e1063b in / 
# Sat, 04 Feb 2023 06:17:46 GMT
CMD ["bash"]
# Sat, 04 Feb 2023 06:47:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:47:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 04 Feb 2023 06:47:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 06:48:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 04 Feb 2023 08:55:49 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 04 Feb 2023 09:02:08 GMT
ENV NODE_VERSION=14.21.2
# Sat, 04 Feb 2023 09:02:20 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Sat, 04 Feb 2023 09:02:20 GMT
ENV YARN_VERSION=1.22.19
# Sat, 04 Feb 2023 09:02:23 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Sat, 04 Feb 2023 09:02:23 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Sat, 04 Feb 2023 09:02:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 04 Feb 2023 09:02:23 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:8e0a5a2afd38370f358c0a7154362a8d17faf709c206b40b1553a077f810c3b3`  
		Last Modified: Sat, 04 Feb 2023 06:21:43 GMT  
		Size: 49.2 MB (49239373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec9f4eeb3b61de38aae4678c79731cf85a809fe12a5e34b7c6043703f3ff600`  
		Last Modified: Sat, 04 Feb 2023 06:53:01 GMT  
		Size: 7.7 MB (7729353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3a72451e0eb2675bda2fe64354ac7eefce09a9d51825711cb59d895cea46d2`  
		Last Modified: Sat, 04 Feb 2023 06:53:01 GMT  
		Size: 10.0 MB (10003656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a612a40907fa6b93dcc878ffa9b0a5bf6307d5498b4685e2f5f3cd98993694`  
		Last Modified: Sat, 04 Feb 2023 06:53:16 GMT  
		Size: 52.2 MB (52191607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc004b544019f357e7b008aa75ec0946dbca7e17075f6d0ad477667bb60597e`  
		Last Modified: Sat, 04 Feb 2023 06:53:42 GMT  
		Size: 183.5 MB (183499920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de68cd3bffff4d43e679515550caff53b6371f18fe404426ca3e4f979429efa`  
		Last Modified: Sat, 04 Feb 2023 09:06:44 GMT  
		Size: 4.2 KB (4208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd63cf2504cd525346a407bcc1ca5e9e850ad78d882fc9883f1d37af2a8599b`  
		Last Modified: Sat, 04 Feb 2023 09:11:38 GMT  
		Size: 36.2 MB (36167154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8019811f3787d1e45b71a9438879bb9a4852eb73d1b91b804f864fca80384f1`  
		Last Modified: Sat, 04 Feb 2023 09:11:34 GMT  
		Size: 2.3 MB (2293262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43676221e1719a6b3218748320e336b046acae2a7262ac68256dcf5a20a8ad13`  
		Last Modified: Sat, 04 Feb 2023 09:11:34 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
