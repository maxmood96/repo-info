## `node:bullseye`

```console
$ docker pull node@sha256:50e1c8326c7e8ae441bd0cdeab9d3cda4f1fa9fb0038951ad04668f3d4c563d9
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

### `node:bullseye` - linux; amd64

```console
$ docker pull node@sha256:12a4db7251f19b006ec1949e7a004f4ad5821dae352d27c70ab0d9e8b1af8478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.7 MB (376742429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c7291d4bcbdfd304dbc89b96c84094caed869b1bb3b43b46a7af1bb14a19df`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:51:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 10:48:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 02 Jul 2024 10:48:00 GMT
ENV NODE_VERSION=22.4.0
# Tue, 02 Jul 2024 10:48:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 02 Jul 2024 10:48:00 GMT
ENV YARN_VERSION=1.22.22
# Tue, 02 Jul 2024 10:48:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 02 Jul 2024 10:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 10:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 10:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da238dd9d1f579bf4f3cd6589e3ab75747f8ea35be2bf50403f8f3fafa942eea`  
		Last Modified: Tue, 02 Jul 2024 02:01:35 GMT  
		Size: 54.6 MB (54588637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414da18c1936c380bc310a14aa9627a150fd6e6393e752068962869f27d2907c`  
		Last Modified: Tue, 02 Jul 2024 02:02:06 GMT  
		Size: 197.0 MB (197018307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5442e915d8e4810f519c4bd096d2c231eff8214f610c81d84fac38dd84bf5cdf`  
		Last Modified: Tue, 02 Jul 2024 20:05:48 GMT  
		Size: 4.1 KB (4087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c11655aa38ba12d7360c7fd1ac7baa36e485a1ad79c6c28047ac1a614f3803`  
		Last Modified: Tue, 02 Jul 2024 20:05:49 GMT  
		Size: 53.0 MB (53034742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47883bb0e54bfe1aac69b07b83582864eb13913d1a4db67e17d086ba9245aa92`  
		Last Modified: Tue, 02 Jul 2024 20:05:48 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d013a979202df8a50a1bc316b99599cdd22929035f4eb235084df5a487693a`  
		Last Modified: Tue, 02 Jul 2024 20:05:48 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bullseye` - unknown; unknown

```console
$ docker pull node@sha256:47423fb6d08f827162d5008b1a861687c75288825d74f02658a74ca04d348aa8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15240247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b31f85aa51760427e3e7868230654f361187d791524cfa6ec45cf513ce4a9b8d`

```dockerfile
```

-	Layers:
	-	`sha256:59006852b494d70ab629257446133c17d517f7236160c32eeeb310dba79495dd`  
		Last Modified: Tue, 02 Jul 2024 20:05:48 GMT  
		Size: 15.2 MB (15217196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:012653115770be8d2cd3a484ce16d671d5a547f10a3d728872e5535e4ae3636c`  
		Last Modified: Tue, 02 Jul 2024 20:05:48 GMT  
		Size: 23.1 KB (23051 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:77e6523648c5c663389710e51ea21e9a85d7f694d670141e959c17c37ae5b545
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.1 MB (332144054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8aa2528765daf7eeeba387462f07cf138fad8ad24649fb9828634d173c2c13e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 11 Jun 2024 20:48:04 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 20:48:04 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
ENV NODE_VERSION=22.3.0
# Tue, 11 Jun 2024 20:48:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
ENV YARN_VERSION=1.22.22
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c595e4d8c2d2c7ad66ab723b54c73c6a0aa876b01511358ec8af1aed8c8b94`  
		Last Modified: Tue, 02 Jul 2024 01:40:13 GMT  
		Size: 14.9 MB (14879331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577c5fe1f5243a6910c54b7b4a338cc9cbae0cfeba74a350b011d2a467e49daf`  
		Last Modified: Tue, 02 Jul 2024 01:40:31 GMT  
		Size: 50.4 MB (50358262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53a04feb4a55b8a4920c0ad42332dddf76ad9bb3bd19eac2f580036953cf88`  
		Last Modified: Tue, 02 Jul 2024 01:41:09 GMT  
		Size: 167.5 MB (167478798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38c806680ec6674be7288e96d6bb0fe6ddc1256a7fa167b788624bdb3a11dd7a`  
		Last Modified: Tue, 02 Jul 2024 13:36:58 GMT  
		Size: 4.1 KB (4077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0689feb53b715b540d19f559defdeca95604013684524cf61824dae158cc8525`  
		Last Modified: Tue, 02 Jul 2024 13:37:00 GMT  
		Size: 47.9 MB (47933470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d094c9247fbc1291bffbb3174130c2cfd992cc5619f1dc71ed94437461e78de`  
		Last Modified: Tue, 02 Jul 2024 13:36:58 GMT  
		Size: 1.3 MB (1250671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bd6494f53b2b33bfe40a13feb7fab596b38e0b71ec4cf9ac2fe8ae2e1d54fc4`  
		Last Modified: Tue, 02 Jul 2024 13:36:58 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bullseye` - unknown; unknown

```console
$ docker pull node@sha256:56b46f2dcda356476bce01bd2438f10d1e8d49d2861484c76ed3644f6d4af525
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15042243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a8599dc57b5f1799ee056adde825a49ee465eb8344350894a707ef81cbef2a5`

```dockerfile
```

-	Layers:
	-	`sha256:3015ed73543cc01c7f0c1410500e2487393ad149caf535aeaa10105f381c1c9e`  
		Last Modified: Tue, 02 Jul 2024 13:36:59 GMT  
		Size: 15.0 MB (15019089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f2b6abbb52801759fe24eea8b2945fe4eb7d41aaa8a7366f7e3550fb286b0d`  
		Last Modified: Tue, 02 Jul 2024 13:36:58 GMT  
		Size: 23.2 KB (23154 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:a919b63c62b40dfb986a3ed412ec5b20c9d4cc9285b2cb9fb37cb4659936c7da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.5 MB (367535251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3cbccc5b30c982a891a5f24da6d11cdc7aa969bc25a803fc9fb6dbeb17e8c47`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 11 Jun 2024 20:48:04 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 20:48:04 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
ENV NODE_VERSION=22.3.0
# Tue, 11 Jun 2024 20:48:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
ENV YARN_VERSION=1.22.22
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75f0ece8974d005f2532701f9fffb099d09a9bd1a53465b796982e4c2f594c`  
		Last Modified: Tue, 02 Jul 2024 04:03:16 GMT  
		Size: 189.9 MB (189935947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e44ee33f0f7a9d593ab93a30d7f8f0fbc2a99042aa5ca8135cf56c5befd7082`  
		Last Modified: Tue, 02 Jul 2024 16:09:43 GMT  
		Size: 4.1 KB (4091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61334221ad702007decf8e697dff599cb5918315f4cafe75aafb48444ddcb6c9`  
		Last Modified: Tue, 02 Jul 2024 16:09:45 GMT  
		Size: 52.2 MB (52177817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848bdb2452c27967c28b5f4395e5b314c63aeca0dc16c921caf75de99657334f`  
		Last Modified: Tue, 02 Jul 2024 16:09:44 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1830de28fa81b7ad073169bc3bddbdaf33024cb4b670bc1a36d50aafa07ac990`  
		Last Modified: Tue, 02 Jul 2024 16:09:43 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bullseye` - unknown; unknown

```console
$ docker pull node@sha256:0d0697f86d4c8e142bd84618eeb00ad22dbd78ed79ae7780a7834c5cc452f458
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15243092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86d90ad451ba47be118ddbb9b7598c222f898b43f2917c8ed84ca05db447808`

```dockerfile
```

-	Layers:
	-	`sha256:63096e51bd8f527dcf1c078f7c3696767bb924ea09da552a11b67631a5097f4d`  
		Last Modified: Tue, 02 Jul 2024 16:09:44 GMT  
		Size: 15.2 MB (15219717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8137f11e5b19597085b43643133cca93bd0238b395fdef6dcb3ca396444e23e`  
		Last Modified: Tue, 02 Jul 2024 16:09:43 GMT  
		Size: 23.4 KB (23375 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bullseye` - linux; ppc64le

```console
$ docker pull node@sha256:dfac6297ab4fd95d40cdd8f9b315260fdf3ed0dbd5870a1b2ab887de96a90b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.8 MB (387849761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b001aa2dc8e1560aa875206256592d684386ca7bed320cda0c5698f7acdb93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:47 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
# Tue, 02 Jul 2024 01:17:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:47:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:50:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 10:48:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 02 Jul 2024 10:48:00 GMT
ENV NODE_VERSION=22.4.0
# Tue, 02 Jul 2024 10:48:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 02 Jul 2024 10:48:00 GMT
ENV YARN_VERSION=1.22.22
# Tue, 02 Jul 2024 10:48:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 02 Jul 2024 10:48:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 02 Jul 2024 10:48:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Jul 2024 10:48:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:202e493da11eac96a36d754afa396feec67f46e0492e70c0cc4d61dfb06d6a75`  
		Last Modified: Tue, 02 Jul 2024 01:22:20 GMT  
		Size: 59.0 MB (58950397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661ff02529d6818e558d6049a746391403c023c68ac6d75816221bd99e3244c`  
		Last Modified: Tue, 02 Jul 2024 02:05:47 GMT  
		Size: 16.8 MB (16765868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93f0edb37745f21593aefba0898d81dbc780a39dfe73cf03491e10c88480878`  
		Last Modified: Tue, 02 Jul 2024 02:06:04 GMT  
		Size: 58.9 MB (58872635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ef5fcf94d321c187fa4f90d7b4b53743171e2926b6152cebcc4b0206128a8f`  
		Last Modified: Tue, 02 Jul 2024 02:06:39 GMT  
		Size: 196.4 MB (196369493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d40b5d2a1983f5ad4441258c519f2daec9bd32cf53cae819313018453acdd0`  
		Last Modified: Tue, 02 Jul 2024 11:21:08 GMT  
		Size: 4.1 KB (4086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14c13cf7cfa4c912cf8af2034bed20d8cce2e65e304a8b39778d280dbb34df6`  
		Last Modified: Wed, 03 Jul 2024 02:13:53 GMT  
		Size: 55.6 MB (55636160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f729254db5700c6f80512eba04a5251a4541b9b8a9dfbeacd267b41da524097`  
		Last Modified: Wed, 03 Jul 2024 02:13:51 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734b5a8895810d7baa9f7c87576f6a170026f0ba82640c24eb5ca62364dd967b`  
		Last Modified: Wed, 03 Jul 2024 02:13:51 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bullseye` - unknown; unknown

```console
$ docker pull node@sha256:d391181997d9559ec27729524ee44cfea26b66aaf0b05c8d7a0993c14649d02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15209603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba11ccaad8cc9252e16c9987c8130fb65e8a5a0c02a49af4077a250db0a277f7`

```dockerfile
```

-	Layers:
	-	`sha256:4e3aed7299a2b32e3888f2c39e2aae0f13c9dfca0add115d9165dbfb8821bd39`  
		Last Modified: Wed, 03 Jul 2024 02:13:52 GMT  
		Size: 15.2 MB (15186505 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6a67628f26c23c21b6e8de208ded1b56a0908b3bf4fc3c37562532c858cbf89`  
		Last Modified: Wed, 03 Jul 2024 02:13:51 GMT  
		Size: 23.1 KB (23098 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bullseye` - linux; s390x

```console
$ docker pull node@sha256:afceb0ab915b30d3df52b52c4b0158b136c4968f86dcdf44ee09e79408af8131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.2 MB (349180101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe726c03030374f264a53288b0981e66226d7c0128f3d4ed97ac68e712e03632`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 11 Jun 2024 20:48:04 GMT
ADD file:5752d26037cbb262eeafd1819ecd77ecf8a8cd0019683c05fb92c50c6a458861 in / 
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 11 Jun 2024 20:48:04 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
ENV NODE_VERSION=22.3.0
# Tue, 11 Jun 2024 20:48:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
ENV YARN_VERSION=1.22.22
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 11 Jun 2024 20:48:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:aa9549a3d8effd17bc1f93fd40d83261d2505d37791c5aa837c9f7c0fff5c9e3`  
		Last Modified: Tue, 02 Jul 2024 00:48:47 GMT  
		Size: 53.3 MB (53319825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7860b53e214213e98b388ade5c0d289331e291bb4e43197e4a14a4e8a111583e`  
		Last Modified: Tue, 02 Jul 2024 03:45:25 GMT  
		Size: 15.6 MB (15641817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b8db73130bc88255a98f66627e7258a074a0223eef8b550e6c1084068d24d0`  
		Last Modified: Tue, 02 Jul 2024 03:45:38 GMT  
		Size: 54.1 MB (54075315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afac5d5564136a413fbebb4f4ab7b85f2fa277f71f996d27bc1d7e24b307c5d4`  
		Last Modified: Tue, 02 Jul 2024 03:46:03 GMT  
		Size: 173.0 MB (173024898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0dabc618c2d78e495b9d55b717a30e0ee7b5b8ce161a92e50f8b8b9ee40580d0`  
		Last Modified: Tue, 02 Jul 2024 16:04:56 GMT  
		Size: 4.1 KB (4093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1112c508ecb95b58d902d0ffaacfd998249104949139112ac07486ed491ca7`  
		Last Modified: Tue, 02 Jul 2024 16:04:58 GMT  
		Size: 51.9 MB (51863033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26202beadf19e9ceb89e9fe5f22673781eae53874905b77d90e9e57077ed9f9d`  
		Last Modified: Tue, 02 Jul 2024 16:04:57 GMT  
		Size: 1.3 MB (1250671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67775240db2aa634b243739c1457ff33dccb3532f7cba5730094bedcc16602a0`  
		Last Modified: Tue, 02 Jul 2024 16:04:56 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bullseye` - unknown; unknown

```console
$ docker pull node@sha256:7bbac1c6599b47bdb301c2e6b3e3540e5fa81919bef44aa3eb8aa279bccc78fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15061919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a919cf39b64bf64b45622a345630be3d0efc44231c6197708260a3a2fad301b5`

```dockerfile
```

-	Layers:
	-	`sha256:a394dcf03c6d8bd285fbcd443dc5f6ee7ea6af709d8d7bfbd33c88fb9154bef6`  
		Last Modified: Tue, 02 Jul 2024 16:04:57 GMT  
		Size: 15.0 MB (15038868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28518d46eed2d46860dac48c2d330f4445846d2d2bde0280bb3476ea5570ab61`  
		Last Modified: Tue, 02 Jul 2024 16:04:56 GMT  
		Size: 23.1 KB (23051 bytes)  
		MIME: application/vnd.in-toto+json
