## `node:20-bullseye`

```console
$ docker pull node@sha256:5f87dcf0a5998c602cd82d2893b8dadade47111505c2fdc4a989bef9a7301808
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
$ docker pull node@sha256:afe2650a1f9207f9338eb0c1abc0527e88a02940edb94314ace99fb3c823cb68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.7 MB (371748485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7177327e85924fe98e7f3741c4860b0e91659d3d6ac204c1fde93a385e05a6b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 13 Jun 2024 01:21:05 GMT
ADD file:d2a2ac890c4f902560feaadaac9f36a9b844131c97453ecb90241cf525185196 in / 
# Thu, 13 Jun 2024 01:21:06 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 03:41:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 03:42:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 24 Jun 2024 14:33:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:29f873e2e3f8f1b35ae4bee023807e71b6e16e714dbd1cbd19b3124c62e7634c`  
		Last Modified: Thu, 13 Jun 2024 01:25:49 GMT  
		Size: 55.1 MB (55099190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e1ed81430e2556f97ec363517655fd54e04e4f6b0eaa55faa9aa88490e96d9`  
		Last Modified: Thu, 13 Jun 2024 03:50:28 GMT  
		Size: 15.8 MB (15764834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:065842589d7a62a96a08c1acc0bf9e7c0b5442f2770276be18328b755d1ffb99`  
		Last Modified: Thu, 13 Jun 2024 03:50:44 GMT  
		Size: 54.6 MB (54589356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dbd10f967df496e6665aeab3e08f15f3d577c1489dbddc64908dc6bc9a22972`  
		Last Modified: Thu, 13 Jun 2024 03:51:15 GMT  
		Size: 197.0 MB (197017260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8a7ed43efb8157f1fc27275bb11e6d1e65f276a0d21c0276ea380e8d5e5eae9`  
		Last Modified: Mon, 24 Jun 2024 21:55:01 GMT  
		Size: 4.1 KB (4091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c7d3e436ceb29b6089fab8347d832e89eca947e3b7c5e3f06c945e90656503`  
		Last Modified: Mon, 24 Jun 2024 21:55:02 GMT  
		Size: 48.0 MB (48022629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aed0e38cf0b94c5fb777f504857e3f6e688a64e83609cb20a068d218a229c916`  
		Last Modified: Mon, 24 Jun 2024 21:55:01 GMT  
		Size: 1.3 MB (1250673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2511100aaeb442ad6c7da3a7f0c0c223d2c268e416564369008b540ad744a4f2`  
		Last Modified: Mon, 24 Jun 2024 21:55:01 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:9dfd3acc6e5df5b8cafb63a2930019afaab0fea3f06dc6b3bee24b093b3f5b29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15242440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54d2b6076a5ed41e5a1eb8b1ac2a83d9eee22b12b32288a9bb6b44d52473a600`

```dockerfile
```

-	Layers:
	-	`sha256:4d5498d274c66588e6e755379326ea66d8cec76c631eeef0503bb14bc3616ec8`  
		Last Modified: Mon, 24 Jun 2024 21:55:01 GMT  
		Size: 15.2 MB (15219381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be047cfd27f98e65f181c70cc9e973e43ba29ba401ef0e10e01cc876cee6eeae`  
		Last Modified: Mon, 24 Jun 2024 21:55:01 GMT  
		Size: 23.1 KB (23059 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:84f5113f23cb1e2043b0322e3a8e17ba19d32e8c418c6a3e0d22d091c979faa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328379760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd34d6a94fa70bc6590be233a73c479f3890ffac878bffbaa1cff2dc7c299fa2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 28 May 2024 18:47:58 GMT
ADD file:4993add96e8cc180b89e1b978fddc0b0876a303bce87dc08120edbe9513432bd in / 
# Tue, 28 May 2024 18:47:58 GMT
CMD ["bash"]
# Tue, 28 May 2024 18:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 May 2024 18:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 May 2024 18:47:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 May 2024 18:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENV NODE_VERSION=20.14.0
# Tue, 28 May 2024 18:47:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENV YARN_VERSION=1.22.22
# Tue, 28 May 2024 18:47:58 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 28 May 2024 18:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 May 2024 18:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:45c5e98886f73bd45565e271bba1de66ffee1cfe17345d38a8e7179841133d4f`  
		Last Modified: Thu, 13 Jun 2024 01:01:59 GMT  
		Size: 50.3 MB (50256430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d823c90ec6db52ee3c5a3a116b21e47442be8c0e35cc53f6f7f4db398ba08fe`  
		Last Modified: Thu, 13 Jun 2024 01:34:16 GMT  
		Size: 14.9 MB (14880170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:738fc6141957592e4d069a8fcb0615b3f6dd757c25ee58dd7023fb923a7a4ecc`  
		Last Modified: Thu, 13 Jun 2024 01:34:36 GMT  
		Size: 50.4 MB (50359459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d33379b30e1ceb9b87b34482bff5906df43a22892099a6815c383a940044f8`  
		Last Modified: Thu, 13 Jun 2024 01:35:16 GMT  
		Size: 167.5 MB (167479604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34bebd29e34b13ef1c4bf5a68fa9fb8c62a036ecbf58ff4d8bc05b18fe731e63`  
		Last Modified: Fri, 21 Jun 2024 08:17:12 GMT  
		Size: 4.1 KB (4084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d139975b0fe436ae8e7095fcf443b91797e8751840346be1b242fc7850d7dde9`  
		Last Modified: Fri, 21 Jun 2024 10:07:06 GMT  
		Size: 44.1 MB (44148879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe82ac33f4c987c2bf4e30d756b916bb2ccef29a2fddc0d9e257c70e0ab66b4`  
		Last Modified: Fri, 21 Jun 2024 10:07:05 GMT  
		Size: 1.3 MB (1250683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:401fba6506af1eaa3c7536a88c42717a13335d0b03f24ac0132418343cc2eec9`  
		Last Modified: Fri, 21 Jun 2024 10:07:04 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:c59a8814ea85b05b2f2a35274c97f4f1ebc3fb894a85e038fd964a10b96ff35d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.0 MB (15044436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a54fc5958a45b4fd758f6ed4a9f6a22e97cb51ee04048b7714ea9b2269cf526`

```dockerfile
```

-	Layers:
	-	`sha256:983b0b924ef948ac0bbc2c00fa58a93ef8129ce0e7ec0f0b860032457147aa01`  
		Last Modified: Fri, 21 Jun 2024 10:07:05 GMT  
		Size: 15.0 MB (15021274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04a48a00dd7fd30221bc3a745232fbbe00ce819cbdd2c93489d3c419ebc3b420`  
		Last Modified: Fri, 21 Jun 2024 10:07:04 GMT  
		Size: 23.2 KB (23162 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:af9d367d28ab23ffa40a07a90b15ee4721539dfb4702309d9b6bf8ee6a000332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.4 MB (363366949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3769f515625fc004b76cf85c8195ee6dc45956b1bef9114064b36c58b80d95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:57 GMT
ADD file:cd3edc79f93d09aa5daffba99cc698c3fe0e02348e8dc284ef466b7e6596e68c in / 
# Thu, 13 Jun 2024 00:39:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:22:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:23:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 24 Jun 2024 14:33:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:f975e52008de385eb513258b4912477b214cddf1c8e87877f85028d940bfcdae`  
		Last Modified: Thu, 13 Jun 2024 00:43:32 GMT  
		Size: 53.7 MB (53739581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:859b5bb8f5d471015f3add7e778bc507fc4a6f1fce8561c2b0a336734a55a365`  
		Last Modified: Thu, 13 Jun 2024 01:31:15 GMT  
		Size: 15.8 MB (15750467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a7ca076c1ea04622ddf9f43ff2f138f6c50a40118747a45d2618cc64591d6b`  
		Last Modified: Thu, 13 Jun 2024 01:31:29 GMT  
		Size: 54.7 MB (54696375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:315e6e292ef6ca0113f94dbf806ecbea714420b97b385d4138e3cb84616995e3`  
		Last Modified: Thu, 13 Jun 2024 01:31:54 GMT  
		Size: 189.9 MB (189935383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7da1b7f41571162b9914fcc897bcf335b01421ffbc5cc9773c4d39c1bfb4eec4`  
		Last Modified: Fri, 21 Jun 2024 08:43:27 GMT  
		Size: 4.1 KB (4098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a7c16cfd0cdfd44e90662b92fa0ea882989c35c95b83f24427fafaff2028a1f`  
		Last Modified: Mon, 24 Jun 2024 22:48:49 GMT  
		Size: 48.0 MB (47989919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552c933c205cf8d1a65602c88c675e472c86f62ecd24462ea481b22b3ddfbbfb`  
		Last Modified: Mon, 24 Jun 2024 22:48:48 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c5075625ed0606b71863118aa26feace3bd15f260c1be52c7478042057cc709`  
		Last Modified: Mon, 24 Jun 2024 22:48:48 GMT  
		Size: 451.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:c84427baffcd6016979094dbcf9868314b2d8bea49cf0ca4986ca94ae8a12bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15245285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e2cf83324aac4fe072a3aa504d54161778964e4b053acb9c9ccf1989b1d8556`

```dockerfile
```

-	Layers:
	-	`sha256:e42d23867c35750c6c2a3d7df063528220d74041b00f6b95f989ad8741735f71`  
		Last Modified: Mon, 24 Jun 2024 22:48:48 GMT  
		Size: 15.2 MB (15221902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6f17207bc5f87840e67e75ce83ad5ced1f5fd86045659d603ea39ca4ebcb38`  
		Last Modified: Mon, 24 Jun 2024 22:48:47 GMT  
		Size: 23.4 KB (23383 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye` - linux; ppc64le

```console
$ docker pull node@sha256:7d46e5f593f6a7829730c0604a67d547347edcf6f86d9f87d71b086736ed35bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.7 MB (382728112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e9b5b09d8a672d7339b942d7b3f25eaf86710681bc087262c30529b826d494e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:16 GMT
ADD file:32733696002797fb377d3d8094c21c0f41f25da6f371eb4a8ecb6fa5c3ef1048 in / 
# Thu, 13 Jun 2024 01:17:19 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:49:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:49:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 13 Jun 2024 01:52:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 24 Jun 2024 14:33:35 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV NODE_VERSION=20.15.0
# Mon, 24 Jun 2024 14:33:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENV YARN_VERSION=1.22.22
# Mon, 24 Jun 2024 14:33:35 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 24 Jun 2024 14:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 24 Jun 2024 14:33:35 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:7afd12f588c414c122b8d3022d60effda2738a394347f5b3cbdebfe1420a8bf8`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 59.0 MB (58968957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918a353cdc3445173a18fe2f058dd7abb46fe3acfde05a65233cd1b979bd3d09`  
		Last Modified: Thu, 13 Jun 2024 02:01:07 GMT  
		Size: 16.8 MB (16766853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44a70314a2227a3d4a36c3baefe93d6e718bb4dd984f85adc8cb091a68f88b3`  
		Last Modified: Thu, 13 Jun 2024 02:01:25 GMT  
		Size: 58.9 MB (58874053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719a9ab0cabd6aa0929d32efa72a27e1b7732e1c13c57af740a74747a17626bb`  
		Last Modified: Thu, 13 Jun 2024 02:02:00 GMT  
		Size: 196.4 MB (196370976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a6474cbf463fe8a89e1cd4b79f1f3998fcf3ee2310bedacdae080ea91ee6216`  
		Last Modified: Fri, 21 Jun 2024 03:43:55 GMT  
		Size: 4.1 KB (4087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09136b66893ffcb5925252c21f8d12c04d53e61067b0e9dcef7e0cb0081f8f67`  
		Last Modified: Mon, 24 Jun 2024 22:32:23 GMT  
		Size: 50.5 MB (50492061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ef18bb8e05928d154fa038cc49006e113b0f61cf3811c56827cb767473784b`  
		Last Modified: Mon, 24 Jun 2024 22:32:22 GMT  
		Size: 1.3 MB (1250673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544f20349399dfa9164351617eebc993b3c86195b9f8afb84bd5b923b3a10f22`  
		Last Modified: Mon, 24 Jun 2024 22:32:21 GMT  
		Size: 452.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:349d825b7cc596536e138a135b94139d14244122e305bb9a5ffa0592658b90a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15211797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d89647cd0e0e187d04ad05556914d6b9fa6829ffe1ea9c76430bd83cd1f5520e`

```dockerfile
```

-	Layers:
	-	`sha256:68b10386b782a4a8aab9cac79dab02bcb9ecb6b7d7b1a390f668b3be7f75fac2`  
		Last Modified: Mon, 24 Jun 2024 22:32:22 GMT  
		Size: 15.2 MB (15188690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08c3852857de974962e98f075d94308065bef179822cfa4dfd90334bbd7112b4`  
		Last Modified: Mon, 24 Jun 2024 22:32:21 GMT  
		Size: 23.1 KB (23107 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-bullseye` - linux; s390x

```console
$ docker pull node@sha256:776080f4b527060c3d3a508d0396acaf58fdf15f2d7ed62b9628e373455e7c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345155441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd4e5e996c68b32be3abcc3f8ffa194c46ce463328bfe56c6b303f0423266134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 28 May 2024 18:47:58 GMT
ADD file:1f0333c084fe60bf682ad64dd7db93b2ca069c7e1d09bf26e7e65dedbd65b0f3 in / 
# Tue, 28 May 2024 18:47:58 GMT
CMD ["bash"]
# Tue, 28 May 2024 18:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 May 2024 18:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 May 2024 18:47:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 28 May 2024 18:47:58 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENV NODE_VERSION=20.14.0
# Tue, 28 May 2024 18:47:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENV YARN_VERSION=1.22.22
# Tue, 28 May 2024 18:47:58 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 28 May 2024 18:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 28 May 2024 18:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 28 May 2024 18:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:db300ed0c60856815a390ef84dc7c5441283ec11483c9da25ac0daf34bac6e83`  
		Last Modified: Thu, 13 Jun 2024 00:47:59 GMT  
		Size: 53.3 MB (53337540 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b507bf58c92373ad020c252404bcc63be7764e5ba99e1b46dbe95f2fb0d32531`  
		Last Modified: Thu, 13 Jun 2024 05:31:46 GMT  
		Size: 15.6 MB (15642492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be3e3e4d728c88a0a3906e1d03b1ffe00d8ceb7ae7abbf81186d2f281bcbf540`  
		Last Modified: Thu, 13 Jun 2024 05:32:00 GMT  
		Size: 54.1 MB (54076476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9d03b6fb081b49e222c939fdd441c740c52b7fc26d78ce4474d6b441e12a1c3`  
		Last Modified: Thu, 13 Jun 2024 05:32:25 GMT  
		Size: 173.0 MB (173028392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc720af38716cc3e2dfb7650da2e43335738a93fa5d0efa35778a2beb8a3b5ec`  
		Last Modified: Fri, 21 Jun 2024 09:39:43 GMT  
		Size: 4.1 KB (4105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5790e1667621d5a0dcccdf64375266dd921ff1a16ec6abdd4f0589d100b8f21`  
		Last Modified: Fri, 21 Jun 2024 11:12:40 GMT  
		Size: 47.8 MB (47815302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0a771b514bd2f5bcd7bcdfdaef9e35dc1d6658661c7840fec9495e4f5d2f886`  
		Last Modified: Fri, 21 Jun 2024 11:12:38 GMT  
		Size: 1.3 MB (1250680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef0af96abe6bd351880962a5f51d129e7ad2ead037730bf4f5c99fb08caeb54`  
		Last Modified: Fri, 21 Jun 2024 11:12:37 GMT  
		Size: 454.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:a2a447df1406a923a862d10128f3fa8ed626d4f8d08d7047b9dff6c3856c76e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15064111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a7a0b1899b58b06eab1bd80992f3cf96183a357053bf6d472dd98cc0ffbb2e0`

```dockerfile
```

-	Layers:
	-	`sha256:fa28b4676dff3c0be0ea06ee9c1e328563804791fdb245579a6b1bfe18d533ca`  
		Last Modified: Fri, 21 Jun 2024 11:12:38 GMT  
		Size: 15.0 MB (15041053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0408ca75a7f4de3ac346cb58b0119b20c1c1e225a44118ded1120dcac46d1c92`  
		Last Modified: Fri, 21 Jun 2024 11:12:37 GMT  
		Size: 23.1 KB (23058 bytes)  
		MIME: application/vnd.in-toto+json
