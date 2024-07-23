## `node:current-bullseye`

```console
$ docker pull node@sha256:5f924e3345c88fadc1b49e46e8a5369552a5f9570cfec42582d844e89fd1d59c
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

### `node:current-bullseye` - linux; amd64

```console
$ docker pull node@sha256:8d2d57d5ebbdbfcc9c732156e82015462a5423e8898f114aaad3da15dcf45836
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.8 MB (376846583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3fb72ad4dbf4a34eec8cdf03105328c62a5622282f7c055dfd4e16a04f20ca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 19 Jul 2024 15:48:06 GMT
ADD file:61c91b2a02e0d3deb2364da03241d137acf78345623ae188082e574b043032a0 in / 
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["bash"]
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV NODE_VERSION=22.5.1
# Fri, 19 Jul 2024 15:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV YARN_VERSION=1.22.22
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:73226dab8db5240a2ddbdbe2fb1f0949a911563a62a3d5de3c8669ae708e88de`  
		Last Modified: Tue, 23 Jul 2024 05:28:11 GMT  
		Size: 55.1 MB (55084578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53dfa00a586795de9dc9f5bc8ad4717b02a8c349b4bbc1f4600a926c5384f40`  
		Last Modified: Tue, 23 Jul 2024 06:14:18 GMT  
		Size: 15.8 MB (15764285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf8ed7043ae24342affc9e27ba2f362a3d02c164d6f2cc7b837f33b475f4ef54`  
		Last Modified: Tue, 23 Jul 2024 06:14:32 GMT  
		Size: 54.6 MB (54588538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25c6efb0908b76d25c6355b6afc739337771c5a9f3a556c262cb1d0c767b6604`  
		Last Modified: Tue, 23 Jul 2024 06:15:02 GMT  
		Size: 197.0 MB (197039174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29d704214847cafdbb3cc54d212f1932898aa47a958f4ac8e402cb3154dc7cfa`  
		Last Modified: Tue, 23 Jul 2024 07:15:44 GMT  
		Size: 4.1 KB (4085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc6d2035c4212e1adc0c51710b3677a1b297afaf77d24018d5f54fc24643e358`  
		Last Modified: Tue, 23 Jul 2024 07:15:46 GMT  
		Size: 53.1 MB (53114805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13210b20516806d3a287bbe496ff77d3ad2c4f7cd3ec9436d85748b522d62d3`  
		Last Modified: Tue, 23 Jul 2024 07:15:45 GMT  
		Size: 1.3 MB (1250673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c864e4e8890c41327aa02a1dfa7aef04768b5d69ecc5fb7998bba3dff01aea5`  
		Last Modified: Tue, 23 Jul 2024 07:15:44 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:cb2fb8f096e96358a8d7c2ec90b2e4c6714f3786f6d75ec2455327a3302ac895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0dfdff3cec3c1edddb812681952e9881451b9bc95770c50166bfabcf7b99119`

```dockerfile
```

-	Layers:
	-	`sha256:4bcf90f9363547caa65e7ba15298e690992a49a0c904d0a7b5a8c2e297c63d70`  
		Last Modified: Tue, 23 Jul 2024 07:15:45 GMT  
		Size: 15.3 MB (15317769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9a592a84ffb8f50154897ab6d786bf31af275563feceb299551f5742a59046a`  
		Last Modified: Tue, 23 Jul 2024 07:15:44 GMT  
		Size: 23.1 KB (23051 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:1c4f443a250dd24660210f610d0c65711da83cd5bf2f670d50d1590321c0cd56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332882913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4405e7953e9653cea94c9ef07c1d0de3a9ad8635820c555d89cccede2ca717e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:11 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Tue, 02 Jul 2024 01:00:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:27:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV NODE_VERSION=22.5.1
# Fri, 19 Jul 2024 15:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV YARN_VERSION=1.22.22
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jul 2024 15:48:06 GMT
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
	-	`sha256:8ed19a1394b43c07d29172d70a52103db93bea790137e7be9b79c8b324c1cc3d`  
		Last Modified: Thu, 18 Jul 2024 16:58:07 GMT  
		Size: 4.1 KB (4079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a34497bc7e57e71bf3f7758685614eefbd9de31227e3434848981a83e5f1a78c`  
		Last Modified: Sat, 20 Jul 2024 00:57:46 GMT  
		Size: 48.7 MB (48672324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f32e12955998eb98bf8512db340fd7262f2e1b410c2bb734045a73a5d2daf9d`  
		Last Modified: Sat, 20 Jul 2024 00:57:44 GMT  
		Size: 1.3 MB (1250673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25a7f1dfeb97384de0056acebe44a430636c1478cd672c439dc5be4b26536a55`  
		Last Modified: Sat, 20 Jul 2024 00:57:44 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:b906232c634e3bc80126feeec3cf50f3b8099e6af0a439eaff53e2a71c8ae826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15142744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:950ab6089ca494dee665757d018f8b627f9f55f70c4482730884fc631c3d71a1`

```dockerfile
```

-	Layers:
	-	`sha256:59ff481cfe54172f87abb32ff54021f4db20203e305563b21ae4dab305fdcc40`  
		Last Modified: Sat, 20 Jul 2024 00:57:44 GMT  
		Size: 15.1 MB (15119589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f956bb456822887f486af5ddcad50002741ee5a3d2e4773bf40a198703bfb77`  
		Last Modified: Sat, 20 Jul 2024 00:57:44 GMT  
		Size: 23.2 KB (23155 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:ab93fe087c2b8c440cd266286731804559994c893400b3f320957107e0a8ac2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368390911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468b0e8d5fbb7afb37bb1fe756c517815f98f4d3fee568405690dddc173f5b75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 19 Jul 2024 15:48:06 GMT
ADD file:bbd5c67ed8e7916601bc20e4ce4973720e715d9dcd892ccbd64c1d5de711a38d in / 
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["bash"]
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV NODE_VERSION=22.5.1
# Fri, 19 Jul 2024 15:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV YARN_VERSION=1.22.22
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:2c9750102c61ce3f4a11c8776dfc892d41a6d4a662d2882e471664dbad58487e`  
		Last Modified: Tue, 23 Jul 2024 04:20:44 GMT  
		Size: 53.7 MB (53729987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c27a83c76abd51a72277b6a74eb7f88e560054e0d04383f64e2886877a20dd5`  
		Last Modified: Tue, 23 Jul 2024 08:11:04 GMT  
		Size: 15.7 MB (15749501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac540a55631c4cba93c7e4e4bf634300076d45e71db5f34f3c0d770eb826303`  
		Last Modified: Tue, 23 Jul 2024 08:11:17 GMT  
		Size: 54.7 MB (54694822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df233b2a5328fe9ae508771678b5a4faaefca18e64196b4ac65584baa5c8aa9f`  
		Last Modified: Tue, 23 Jul 2024 08:11:41 GMT  
		Size: 190.0 MB (189965935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a55e5f3035df81057de661d91ec7c86fb73acb1084370d8f4c7f851563e9f5b2`  
		Last Modified: Tue, 23 Jul 2024 20:13:35 GMT  
		Size: 4.1 KB (4095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b5248de2a1afd7690fe2b86908051fc8e05b85bba60f610ac74edb486532a`  
		Last Modified: Tue, 23 Jul 2024 20:13:37 GMT  
		Size: 53.0 MB (52995455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c02781e3f165ff5723b92799c886e63f5658879ee3a06cbaddaa12b86fc439`  
		Last Modified: Tue, 23 Jul 2024 20:13:36 GMT  
		Size: 1.3 MB (1250669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd6917636381f4d7b1e3492b36678652f42e66e7771c0dc8588dffeec60f04a4`  
		Last Modified: Tue, 23 Jul 2024 20:13:35 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:45d425b815dc44d801de44032915c42551c4c1959934edb7ff9f320b36e78d03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15343522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32c29bd9135e501bfdb98fd2c4ddb742f6e7a7f53cbe635eae9a4056c4225dd6`

```dockerfile
```

-	Layers:
	-	`sha256:dd83cbe34eaa77d1b2eecf9b22d3d87650c87d84076739968d8e22d499c4d1da`  
		Last Modified: Tue, 23 Jul 2024 20:13:36 GMT  
		Size: 15.3 MB (15320147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:540420b2a2974db9928f68a35f5c38045e81aa1d5a4e0806dd02c17491586c09`  
		Last Modified: Tue, 23 Jul 2024 20:13:35 GMT  
		Size: 23.4 KB (23375 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bullseye` - linux; ppc64le

```console
$ docker pull node@sha256:3faf83341ec3b57d2985ae57e0adbdc087bda9cf8668483858352bf7d7dc15f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.0 MB (387959114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244e9082dfa04ecf2a2f5ce8b6be1a5444444ff6c44de6b77c1340e83d0ff273`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 19 Jul 2024 15:48:06 GMT
ADD file:538282e20405c23ce510f30f714f80393534997f12fd1cc25a8d7752dc6f1360 in / 
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["bash"]
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV NODE_VERSION=22.5.1
# Fri, 19 Jul 2024 15:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV YARN_VERSION=1.22.22
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:fb0b8650d20e29c53f770b72d16b7381f876f2a0053fff3e542a0cc3f0b944b9`  
		Last Modified: Tue, 23 Jul 2024 01:31:32 GMT  
		Size: 59.0 MB (58954687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89f3ec0749e802be2768d4d8d990f300a55cd418831db42ee374e4bb81ab0a3`  
		Last Modified: Tue, 23 Jul 2024 02:43:09 GMT  
		Size: 16.8 MB (16765814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3543cad9c41f9c9127d1adde535bc13ac5b446330727c5083aafa4b8d005c62`  
		Last Modified: Tue, 23 Jul 2024 02:43:26 GMT  
		Size: 58.9 MB (58872667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb8d0e14af4e3c68b0eae63b664f02cecf25bea995af2d28db767811530400f5`  
		Last Modified: Tue, 23 Jul 2024 02:44:02 GMT  
		Size: 196.4 MB (196396379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60451007ecaa24796dd82da2d24a0b0514f0a673111251a9b110fb0fd11b60d5`  
		Last Modified: Tue, 23 Jul 2024 18:15:25 GMT  
		Size: 4.1 KB (4086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6485ff7c1e779d1b345ec0b2cac7c1dc8ce0e09a1a229951a55b72d608289aef`  
		Last Modified: Tue, 23 Jul 2024 18:15:27 GMT  
		Size: 55.7 MB (55714358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abacadffb95e5547d233ad113bcb225dd3a00e7a6c536a8b02dd53ef03c5751`  
		Last Modified: Tue, 23 Jul 2024 18:15:26 GMT  
		Size: 1.3 MB (1250677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b99e2d728da925eb2a315940f7a0c60b7dec53a8dfa2a331fd01346a8342b8f3`  
		Last Modified: Tue, 23 Jul 2024 18:15:25 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:2e5a023e399c54aa4d3e661f2464242009f8350fad52cb3d0405f2be65fd5c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15310177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e59b3676763729ed2c5e70ed373e2896d74333341798b2735bd18dd13197d1`

```dockerfile
```

-	Layers:
	-	`sha256:cb221e7ad73eb2fe3580d04662bca08ce87ce95d62d47a435fbe9be637134cd0`  
		Last Modified: Tue, 23 Jul 2024 18:15:26 GMT  
		Size: 15.3 MB (15287078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a86fec987ab6dc30be546f3e321121cc399e97bd7c3b9c1d141234da7b8398c`  
		Last Modified: Tue, 23 Jul 2024 18:15:25 GMT  
		Size: 23.1 KB (23099 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bullseye` - linux; s390x

```console
$ docker pull node@sha256:63d6cf5a338778a21b6bff6f4de390f3041b032e0ed79ab920cce2e3e1bdef6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.1 MB (350051041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e185b932b78ad5fca7dd489f0f55a0df5f8fb865c0c86bbde066380b296a74ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 19 Jul 2024 15:48:06 GMT
ADD file:67d4db619a1cada17f248642d89d5b55ab04b5dd6885587148dedeb665795154 in / 
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["bash"]
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV NODE_VERSION=22.5.1
# Fri, 19 Jul 2024 15:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV YARN_VERSION=1.22.22
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0d03391dea2fdd66bd2c594e41ac7575c5879176469a4d1e7301b8498f5e5351`  
		Last Modified: Tue, 23 Jul 2024 02:32:57 GMT  
		Size: 53.3 MB (53324092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9e924418f310f18ad368886d6df84cac76659f51225b0784a1e53ff07318533`  
		Last Modified: Tue, 23 Jul 2024 03:15:16 GMT  
		Size: 15.6 MB (15641720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8af67dae0133d3a5f116411c20eed624558ce4a187db4fd8eb9a8d622a827e5f`  
		Last Modified: Tue, 23 Jul 2024 03:15:29 GMT  
		Size: 54.1 MB (54075295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d2fba31676a932e41fb57a433c1ba42080bc1e363d7a190b9c73795d53b569`  
		Last Modified: Tue, 23 Jul 2024 03:15:55 GMT  
		Size: 173.1 MB (173058357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f89a5fede5cddc4fd623f06453d6d118eac1fdfd1a998254f039f5c5e14395c1`  
		Last Modified: Tue, 23 Jul 2024 19:32:36 GMT  
		Size: 4.1 KB (4096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fea08547e0c22bedb1d201c45f1251736bbb141a98b01b678ca14e264dd3a3ac`  
		Last Modified: Tue, 23 Jul 2024 19:32:38 GMT  
		Size: 52.7 MB (52696355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:428f33564b637910814653e255c77535fc907f9642111a51849aac6a9a63e233`  
		Last Modified: Tue, 23 Jul 2024 19:32:36 GMT  
		Size: 1.3 MB (1250677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11baa328476bad9e0750d5cc2f1da823bc1fa94cd398a7493d55a74f95cab8e6`  
		Last Modified: Tue, 23 Jul 2024 19:32:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:b9e2d77b9d66f9542728c3744e0e30ceafc57268247e6fbced1c1d3416de58d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15161776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fb0f594227652bd6dd701423b3cc2b246acbb2856a36f4bf4cda6526268bb33`

```dockerfile
```

-	Layers:
	-	`sha256:fd89a034ebadfd357300eeddd51b1f0a9ad1a7670ac3296c52522a224601d2bd`  
		Last Modified: Tue, 23 Jul 2024 19:32:36 GMT  
		Size: 15.1 MB (15138726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029437807090db131d7137e4784fa50b535cbc76452fb0dee3689d490bbdf791`  
		Last Modified: Tue, 23 Jul 2024 19:32:36 GMT  
		Size: 23.1 KB (23050 bytes)  
		MIME: application/vnd.in-toto+json
