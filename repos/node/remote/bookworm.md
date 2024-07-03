## `node:bookworm`

```console
$ docker pull node@sha256:56d771fe1c1be92693d1ec5a61d4ca29c35be9470228d0d953c6edda3071e314
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

### `node:bookworm` - linux; amd64

```console
$ docker pull node@sha256:4d7bcfe46effa474ca1be502a1d97878bf972ac6507eda2cf93d57c09a9400d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.3 MB (403261288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3146073457c8e12e3de3d59fe9e2d6eb06f8b1d7384b2cfe35ce78cc5940250`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 02 Jul 2024 01:24:49 GMT
ADD file:e8aac9b1598114ead96b4038c19d915b87f662ef342291d69c7e5255c5d731fc in / 
# Tue, 02 Jul 2024 01:24:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:48:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:50:03 GMT
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
	-	`sha256:e9aef93137af6e967e7242f3b3c8ecd8e6f571d1e6fdd9e72db0befeeae3cf13`  
		Last Modified: Tue, 02 Jul 2024 01:28:26 GMT  
		Size: 49.6 MB (49554064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b365fa3e8dc16e70d89fab0e91f5242feb38ae3cfeb6655e654209ea109333`  
		Last Modified: Tue, 02 Jul 2024 02:00:17 GMT  
		Size: 24.0 MB (24049794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbed71fc5444cf6889a21b002de3e7805e810aa88f91a9ca941b4e3880246d1`  
		Last Modified: Tue, 02 Jul 2024 02:00:35 GMT  
		Size: 64.1 MB (64142928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae70830af8b64968596022cd9041ce522f0c77eab5419b19e169b53582c69e3f`  
		Last Modified: Tue, 02 Jul 2024 02:01:09 GMT  
		Size: 211.2 MB (211225279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0078cb5df4578846ca6d1a44499337752057d68da49a7bd9da73d67782fe6b6`  
		Last Modified: Tue, 02 Jul 2024 20:05:41 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ee31c98c928249e90131c569fbeac09fae1ed4b5312d6a95ef33aaf0046fc0`  
		Last Modified: Tue, 02 Jul 2024 20:05:42 GMT  
		Size: 53.0 MB (53034777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b067ecbfab4fe7bba9616e90071d85967bb0d194f118145b4ffe28c5d0026ba9`  
		Last Modified: Tue, 02 Jul 2024 20:05:41 GMT  
		Size: 1.3 MB (1250677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65fcc43c3afb298ff7659802dc9db3e3ce36d8b609a69d531c7a3861e5b52a6e`  
		Last Modified: Tue, 02 Jul 2024 20:05:41 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:13781f738ca1d15d3dfe660b929bddcf95aa5a5af34ca95af3045922690c28af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15633875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375946847a4c99ec005b9269941a0afdd7bf6a8240ead0047701f52be63d4f79`

```dockerfile
```

-	Layers:
	-	`sha256:95e3b3f8b5ace431b275484fac3ccb580bc4e8be401da8eca79a515322fb797b`  
		Last Modified: Tue, 02 Jul 2024 20:05:41 GMT  
		Size: 15.6 MB (15609364 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a6d751e63d7fd3f8c05883f27cadc72581b114333c76c0bf4779070d2112703`  
		Last Modified: Tue, 02 Jul 2024 20:05:41 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; arm variant v7

```console
$ docker pull node@sha256:0caa91f5ab95221a3f8f1ae9d18ff75d2af9d2fd840a7e87003ac1df23b2f66e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.7 MB (350677206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ba4ff39211179afba0ccdd38940977e0431778e93581496584e92d95baa1d16`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 11 Jun 2024 20:48:04 GMT
ADD file:526dbb34ac449ae8f3c9025d71b3ffeb0e24fa5dc1a01da707f0a8b834eb4e33 in / 
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:335f2c484898b910fac13d5650ed3c78e5e673fe8dab1b06a071c71478a153d0`  
		Last Modified: Tue, 02 Jul 2024 01:02:57 GMT  
		Size: 45.1 MB (45148097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0aa30b2bcbde45c2fc67abf425197af3af3e67d55296f168143343ef1b0e2d3e`  
		Last Modified: Tue, 02 Jul 2024 01:39:04 GMT  
		Size: 22.0 MB (21954038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4650a14deed524a46f7f7b410ff5d81e5ff66e51c7345e2b05887b6e3f4030`  
		Last Modified: Tue, 02 Jul 2024 01:39:24 GMT  
		Size: 59.2 MB (59222408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11ceb3cc12c0338c85a0602b703f838a13aa2e232ffde0c008b8db42bec79a26`  
		Last Modified: Tue, 02 Jul 2024 01:40:01 GMT  
		Size: 175.2 MB (175164748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c589958cf4b2a398ee04185c6be3e3bc60b8983ba407c514faeb9a112807d6`  
		Last Modified: Tue, 02 Jul 2024 13:34:09 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38480de75a757afc0de8698a2c6adaab72376670fd8e150a1005df0373b5b39`  
		Last Modified: Tue, 02 Jul 2024 13:34:11 GMT  
		Size: 47.9 MB (47933469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62ba4dce681d5818aab815b50487d2e8a6766983faf9e82940d17348a26155df`  
		Last Modified: Tue, 02 Jul 2024 13:34:09 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49207ca7c8d112bbde20315dcc0a264be404bcf00f3944042294404645e98225`  
		Last Modified: Tue, 02 Jul 2024 13:34:09 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:c2688bb190556741584410df68be7bd68a9d3afcced9fb5770e96b6dad218747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15439903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ed7713b8c73406fb4c03ab39c0bda56304c7feb33a87c7447dbf30e765c3713`

```dockerfile
```

-	Layers:
	-	`sha256:7c75bf9b9501e0f833378b53c858bcc85cbe9403a77fd7da4a91345b5d51cd76`  
		Last Modified: Tue, 02 Jul 2024 13:34:09 GMT  
		Size: 15.4 MB (15415248 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c893da1dbb4e553a952518c7ec7e1197b93cc5f8c957923de7e8ba1e76fceac`  
		Last Modified: Tue, 02 Jul 2024 13:34:09 GMT  
		Size: 24.7 KB (24655 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:a782e51c7a9e45dd3875939a33dfc9b62f5cbd64e3737c2d742beb4d160a248d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.2 MB (393217303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5fdebd48e5a2f9affc6e6bc90aec4df9a7071b139326d3cfdacf42624bdb09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 11 Jun 2024 20:48:04 GMT
ADD file:696648070a57689a69a184fda234045f7be4a8a9f3b2fff9031ff0a2d9914113 in / 
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:0bd1f8180c504ba389021ce74895ed487ccd8c70e2d9af3707934bc801ba28d8`  
		Last Modified: Tue, 02 Jul 2024 00:42:03 GMT  
		Size: 49.6 MB (49588448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16610496e73ba3d120d519598b53fa8a2db4c80ccc097a5016ad44aedd0654b`  
		Last Modified: Tue, 02 Jul 2024 04:01:41 GMT  
		Size: 23.6 MB (23591145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64a6ab51b82df5ee608db374a16686eefb99bc53834af17064184653121729b3`  
		Last Modified: Tue, 02 Jul 2024 04:01:58 GMT  
		Size: 64.0 MB (63994637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f8241ab9fefcedcf3f5b57b6b8b870d07c8ac5d8e37b6c24189ae5b084f48`  
		Last Modified: Tue, 02 Jul 2024 04:02:26 GMT  
		Size: 202.6 MB (202610801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb112e1e1c7f470dcb11345b4c73ae5dc16dd87ffd2f2101a6b462cd730193a4`  
		Last Modified: Tue, 02 Jul 2024 16:07:30 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:880e3d658d0b7820009a42896b1111288c5ce1224002522b195601f55656d49d`  
		Last Modified: Tue, 02 Jul 2024 16:07:32 GMT  
		Size: 52.2 MB (52177823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f9f3439f23c8be17d720b79f6da4473b83b8faf5ec491777d34ee33456ea4e4`  
		Last Modified: Tue, 02 Jul 2024 16:07:31 GMT  
		Size: 1.3 MB (1250678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35f80ed3b1425dd2b77e74c3812d000ed6ae2041a756fbb500b78696bb0a3bbf`  
		Last Modified: Tue, 02 Jul 2024 16:07:30 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:2e7bbfd7b226d2322ceaf9f99e21e6dba1817586326884dd358fe003b05c875a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15662887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deaa5e37268a5e6b81676a6d6fef146edc9969f0dd4d2c06b25a5bd72f7e9aa8`

```dockerfile
```

-	Layers:
	-	`sha256:c6aeb3071c68ebe643d218fcfec6df250961b2c70a8d13e57301ea8d431a1b72`  
		Last Modified: Tue, 02 Jul 2024 16:07:31 GMT  
		Size: 15.6 MB (15637992 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c028b5ea129c2612f3dd1b45a4c076e2f733a1df3b902a40ba7b7089d663f9df`  
		Last Modified: Tue, 02 Jul 2024 16:07:30 GMT  
		Size: 24.9 KB (24895 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:e6e1722e94d2fdf30c84596a8851d5f6e742a517adfd119faf3b9d010d48566a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **419.1 MB (419103890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6571e49744be668e29b116d3e83c61e784a999f98dc608fafabeb33051b958dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 11 Jun 2024 20:48:04 GMT
ADD file:a02c311ba745dd8d5b3cc5585e2fe57a4aa9807b1ca2005815257da116010b54 in / 
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:2ebe64104880a6a83eee169b12fbd82da8a0ddeac711670e50f30e975bcb92bc`  
		Last Modified: Tue, 02 Jul 2024 01:21:30 GMT  
		Size: 53.6 MB (53557015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bf317c43d118e9cf38efabf9b1e93b406add8c26e307fde367e39a47a1c5821`  
		Last Modified: Tue, 02 Jul 2024 02:04:25 GMT  
		Size: 25.7 MB (25695092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91f1c93d43f65ddb5b49fa7540ab263862ed9868139cb0bfc51bd8dffe47f60`  
		Last Modified: Tue, 02 Jul 2024 02:04:48 GMT  
		Size: 69.6 MB (69582302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3851398057330b42908d94c58bef25257d4970fa040c693d176d2cf32992a715`  
		Last Modified: Tue, 02 Jul 2024 02:05:34 GMT  
		Size: 214.3 MB (214252411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c687418fc2a41a3f339d584db6c8d8ab48c55d08c93e49fcc8817062e48f338`  
		Last Modified: Tue, 02 Jul 2024 11:17:25 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858e0ddf2374d463d7b53d0f91891bacfc77118bc94da706b6d831624e434452`  
		Last Modified: Tue, 02 Jul 2024 11:17:27 GMT  
		Size: 54.8 MB (54762633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84b8d29af82ef72a97604d3bc96eab5e7a64314b8c34f49f8771f7b57c6b4382`  
		Last Modified: Tue, 02 Jul 2024 11:17:25 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f57e77d333fe8c5d85e1fcf51c3cb5622443dc4b140485933e39b702ef7075fa`  
		Last Modified: Tue, 02 Jul 2024 11:17:25 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:8d5dcd073a1146a6edb900abafed9fdd4d833d9c7c341a27a58bc2c752d8c59a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15610653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3256dd533e0a9907957eee81d1a2c887bc7248b0cb1c6e7b6ca2bfe0f360b05`

```dockerfile
```

-	Layers:
	-	`sha256:10a109161072aaa2a41f6d678243595156ff1de62a6fe9b9cc98fb35ae5985e1`  
		Last Modified: Tue, 02 Jul 2024 11:17:25 GMT  
		Size: 15.6 MB (15586064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f78c53a89788f44dcb1cc7c5b54f753f7a52edbbe186729d30d3756bd2d8f71`  
		Last Modified: Tue, 02 Jul 2024 11:17:25 GMT  
		Size: 24.6 KB (24589 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; s390x

```console
$ docker pull node@sha256:b906389376195dd02d7e4ff5b90732570c30a7ccc4e16836f2d44052e1628e4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.5 MB (371476726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f20d5ca99e73f4cc195d54c9f6e7ced05d589210a756766c029624a6b5668b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 11 Jun 2024 20:48:04 GMT
ADD file:397aa43721bc5ca67ab359263843a05c62e131f07114e92f39927f59790c9a5b in / 
# Tue, 11 Jun 2024 20:48:04 GMT
CMD ["bash"]
# Tue, 11 Jun 2024 20:48:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
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
	-	`sha256:1b8bfe08588d8939b4d39134c5c614351649e3890ceb7c234b7542f58d7bcc28`  
		Last Modified: Tue, 02 Jul 2024 00:48:16 GMT  
		Size: 47.9 MB (47931511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37bf3d98ae5de59851adab45daeaaca9d29f76110a2923bd8937c4ad2e8cd52`  
		Last Modified: Tue, 02 Jul 2024 03:44:34 GMT  
		Size: 24.0 MB (24048872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e6cb3bef78d7b20f095bd16b5a39e3ffec90c96f6d1307f8672edb9deef1c5f`  
		Last Modified: Tue, 02 Jul 2024 03:44:49 GMT  
		Size: 63.1 MB (63125178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e457fb781c30f5a251f0251b0cafc815abfed65652bdecac052b60618b497a23`  
		Last Modified: Tue, 02 Jul 2024 03:45:17 GMT  
		Size: 183.3 MB (183253702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73571bdbf33d37d53cae5ba3fe2f6778e2cce8f584b7c55533646b6a2c09bdc3`  
		Last Modified: Tue, 02 Jul 2024 16:03:50 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d633bf02448460b5344e4cf6f93a0170b0dcbc198a01b53a72ec256345618749`  
		Last Modified: Tue, 02 Jul 2024 16:03:51 GMT  
		Size: 51.9 MB (51863018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74cbb1dea7e54d31db6ef59292c59419a22806431c5712710f22098289f7efcd`  
		Last Modified: Tue, 02 Jul 2024 16:03:50 GMT  
		Size: 1.3 MB (1250673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e09aea1ebfe860a65490079d1f24af60c0f1a3817234f6c09808fea26f96fd`  
		Last Modified: Tue, 02 Jul 2024 16:03:50 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:853a2e1c2e9411d3b7351ade088fd43adb8975dce7bd0c60572698f0f0e4d5e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15448557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d43d5702c8d1c298d04701fa1da415018381b8739bb6846c9ed747c2710ccc`

```dockerfile
```

-	Layers:
	-	`sha256:d82f110c0f29deede9c552d40049f59d84f3fc7d91e92003b3e27c45610db353`  
		Last Modified: Tue, 02 Jul 2024 16:03:50 GMT  
		Size: 15.4 MB (15424046 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30de152904f11b8f17e137d2de0a6f58a84b6dbf2875a8fbcc036b14ab5f7bf`  
		Last Modified: Tue, 02 Jul 2024 16:03:50 GMT  
		Size: 24.5 KB (24511 bytes)  
		MIME: application/vnd.in-toto+json
