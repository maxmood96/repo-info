## `node:hydrogen-bookworm`

```console
$ docker pull node@sha256:3d9819be1e6ce053673b64c69640ae4ba84c0fe4c77dd66eeec38249c39b6dc8
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

### `node:hydrogen-bookworm` - linux; amd64

```console
$ docker pull node@sha256:7635543bd50cf043f1c0af615126f09478ed0fa99ce41705f0618906751db81c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.2 MB (396153784 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e348d98bd63f4c939caf825a5153a6e10c8fb6e579d3fbbc26ce90d96f0d2a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fb06272621d93901f1618d85fc9f355fc58f07835606e94e28225a1f17c2140`  
		Last Modified: Fri, 27 Sep 2024 06:02:47 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7208174e5c55cca12cdb7cdf1c1907e98c957e13623151dc65486eb93ac4a91b`  
		Last Modified: Fri, 27 Sep 2024 06:02:47 GMT  
		Size: 45.6 MB (45636925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96cb38999f9f4a1c5a84569dd0b33527218eabb84b51f2d3e82c9f41e4c4a300`  
		Last Modified: Fri, 27 Sep 2024 06:02:47 GMT  
		Size: 1.2 MB (1247028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919dc9e6461a7236b25b34cfcc920b17869f4d7c22eb70205e0daff23e50afa1`  
		Last Modified: Fri, 27 Sep 2024 06:02:48 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:hydrogen-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:0f2dc19669fe9ac6f830a4210a741f2932f1bc8f3a24b7eead49bf8867db537b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15748991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac853b195100b3613aa464d3843060bdbcbaca96ba1194c310befe6223b37a96`

```dockerfile
```

-	Layers:
	-	`sha256:576c6350e22a00a47af562863c1d930258b71de031f7a47433a2bbd9173b0fce`  
		Last Modified: Fri, 27 Sep 2024 06:02:47 GMT  
		Size: 15.7 MB (15725058 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad7cdb259ef0a82bc44f7e5eb66d38311fa9642b1a8d1f510a2e960cef73dbfe`  
		Last Modified: Fri, 27 Sep 2024 06:02:46 GMT  
		Size: 23.9 KB (23933 bytes)  
		MIME: application/vnd.in-toto+json

### `node:hydrogen-bookworm` - linux; arm variant v7

```console
$ docker pull node@sha256:fa39fbb80d676450ac25d7114e8f36513d91dd622362a3ca94e1fa034c4d2e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345101310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2b26f7ee34e6f879bb30eb1eb7d47b203154016005ddac4cfb13353c4b60ba3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:ce9ce875a73b1b4b1e1c1d3a25f43061406d0cc45595b603c5aaf2eb033490e1 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:40a80c95f31d4a590ac5cfb88f8380e036f60bcffc5a805946b43ba82dc5f6d7`  
		Last Modified: Wed, 04 Sep 2024 22:01:19 GMT  
		Size: 45.1 MB (45148448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:000d3087a8c99ea87e011af172ffa23a565515328456f8ab3a8d3bbf65066c0c`  
		Last Modified: Wed, 04 Sep 2024 22:35:58 GMT  
		Size: 22.0 MB (21957240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74af1f53669444d39cb60af3d8b27682f29cd813798990f2763c4a3e13530631`  
		Last Modified: Wed, 04 Sep 2024 22:36:19 GMT  
		Size: 59.2 MB (59228610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaf1b5402e12f0e97f96b3da218271b7caf2abf4a321ce82a42bedc2d72eb82`  
		Last Modified: Wed, 04 Sep 2024 22:36:55 GMT  
		Size: 175.2 MB (175209450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05ad49e444f05f7167e6681bf0ed846ec4ea2af044643b9445373ae0f73531a8`  
		Last Modified: Thu, 05 Sep 2024 23:34:13 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb1d1780fb814f367f4ce0865b3342f586de18a54e21273128a4d70ce0e81e54`  
		Last Modified: Thu, 05 Sep 2024 23:40:13 GMT  
		Size: 42.3 MB (42306761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdfa929896939902feddea7a7a7831d8379fc5153ee3e3fd04ae191474e2d3f`  
		Last Modified: Thu, 05 Sep 2024 23:40:12 GMT  
		Size: 1.2 MB (1247030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c72f94048ed59819d5b56398a745011527b58aab9cc92b2e80dbf38d2c6e5d`  
		Last Modified: Thu, 05 Sep 2024 23:40:11 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:hydrogen-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:23351b8cefdc179ec65af45531e0af18bcb0df0e607e01359b8ffbd476a43217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15546403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:790811d68610d184298f1d94dadbaff777009beb2b7193fe9f8b6413df354b16`

```dockerfile
```

-	Layers:
	-	`sha256:b8656e5417a7514bd1707fcc301d3145f3504a26e31d19848b741a514a46f694`  
		Last Modified: Thu, 05 Sep 2024 23:40:12 GMT  
		Size: 15.5 MB (15522342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:016d63f33b51786612b287c3550ab8dc7b612cd66576e6e2af2f477ecc46cd96`  
		Last Modified: Thu, 05 Sep 2024 23:40:11 GMT  
		Size: 24.1 KB (24061 bytes)  
		MIME: application/vnd.in-toto+json

### `node:hydrogen-bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:83e94f4de054be8f9c7c06fa79ad954fac4aeef9bf7408af722a6953619ee563
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.1 MB (387118505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b569348fe08684858cf7d4b05e856062879c7b12acc21b463e8aecd28a0e9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d629be7509338cb54b2000d6e955e61cd65e815f47eff1ba13040c71fa12b0bb`  
		Last Modified: Fri, 27 Sep 2024 15:34:14 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75246d17c3d7de7afa8e6569173fc368a8d0024b971d100d1530083b301d222c`  
		Last Modified: Fri, 27 Sep 2024 15:42:54 GMT  
		Size: 45.7 MB (45687364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c66f94f7580e1a2caa656dbd66ffc250a9c809126ab31301dd870b39fb8766da`  
		Last Modified: Fri, 27 Sep 2024 15:42:52 GMT  
		Size: 1.2 MB (1247033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c82b75ebbf898f13a26843d94b952b4ac8389b964f72a7356352cee8b4755b2`  
		Last Modified: Fri, 27 Sep 2024 15:42:52 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:hydrogen-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:d32592eafc3f6d2a7f49c86274d4e9a0685a19784ac36fa1068dafdbc2fca03f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15777955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32aa36e3060e5481a9a35983ca21c54decebb9b9f8eb2e5d14c2723a19f41050`

```dockerfile
```

-	Layers:
	-	`sha256:74abc0619b3bbab7dc8e53ec9892389149c0b3c30c5d1a6fc93e55fcaa99bf1c`  
		Last Modified: Fri, 27 Sep 2024 15:42:53 GMT  
		Size: 15.8 MB (15753662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32cef9d209bc14a3a745b4b4c930bca0e6efc4d6ca80ac4cfe7266fe46bf5799`  
		Last Modified: Fri, 27 Sep 2024 15:42:52 GMT  
		Size: 24.3 KB (24293 bytes)  
		MIME: application/vnd.in-toto+json

### `node:hydrogen-bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:d35122f622c31da2ac9403c44bd4217932e1b66b9e533f40adbddf5a4b315ccb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.4 MB (412357509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85afb90064ecf68774a6c9f5a90ed0680b7d33197267adbefd8dab3f3fd1a225`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351d0d69381e1919eb17187e435e3cb9f1c054b5343e54442d8b706f81303688`  
		Last Modified: Fri, 27 Sep 2024 20:23:08 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014529627dfc3ec3b6ff95225d946bd876a1bb13f382767d191269732f312168`  
		Last Modified: Fri, 27 Sep 2024 20:30:12 GMT  
		Size: 47.7 MB (47726138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec8cde3b8f3503a7307f7dbd45d5626162c74c94142e385e9277d178229cbcf`  
		Last Modified: Fri, 27 Sep 2024 20:30:10 GMT  
		Size: 1.2 MB (1247031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:663acdd41ccbf8f75329b78e31dd90feec2721335eca65f017ed5bbe8ffa6949`  
		Last Modified: Fri, 27 Sep 2024 20:30:10 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:hydrogen-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:a70bce164795af8674b13047f1daea355c8f62f2f7fd187a453bd1d9a5f122aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15725602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74b2e1157a6c488def7532a844f50111fa05da7330c1f686f648c98ee6e28af`

```dockerfile
```

-	Layers:
	-	`sha256:7d3db53353c38be63b719985fed8b19d6387ebcff6fd8bb9717464d2be3d742c`  
		Last Modified: Fri, 27 Sep 2024 20:30:11 GMT  
		Size: 15.7 MB (15701603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5cfac228c26642d70e3370263e293fc655d6761fb5002294a7908d92654b1b81`  
		Last Modified: Fri, 27 Sep 2024 20:30:10 GMT  
		Size: 24.0 KB (23999 bytes)  
		MIME: application/vnd.in-toto+json

### `node:hydrogen-bookworm` - linux; s390x

```console
$ docker pull node@sha256:7f3ea1782c9d67e4e8ee1c9150ab6e0ea2fefd8fc37f62c7d56163bffb33786e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365454745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:237dda1b15b044f663985864ef8b76cb972486eacbc63cccfad919827d98cdce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 09 Jul 2024 05:33:43 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["bash"]
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Jul 2024 05:33:43 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV NODE_VERSION=18.20.4
# Tue, 09 Jul 2024 05:33:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENV YARN_VERSION=1.22.19
# Tue, 09 Jul 2024 05:33:43 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 09 Jul 2024 05:33:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 09 Jul 2024 05:33:43 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e4b95140c620254b323e9495b4b32b79c0b602e246a349abb84514daf1062f`  
		Last Modified: Fri, 27 Sep 2024 13:19:26 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd0fe5ef880d9d16e1c7aaee37f446b3bc9e5c94967f3bd1b5525bd069cf1a75`  
		Last Modified: Fri, 27 Sep 2024 13:24:13 GMT  
		Size: 45.4 MB (45430402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c61d741305e5c242c35dbd7e3cd2c174796ba70ea5851d47a380fda9ffd1331`  
		Last Modified: Fri, 27 Sep 2024 13:24:12 GMT  
		Size: 1.2 MB (1247029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8903d3809518b6567cda397670ac579c24ef07cd3b412a48387e49ad951a7a96`  
		Last Modified: Fri, 27 Sep 2024 13:24:12 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:hydrogen-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:ff96275b2580f24e9ad93313b305a24281be0129388b94a3d61f476ae69d05e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15562386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d52e023de1b8fbba792335eea1c4fb92211c95d89ef06ab25437c09e5524e2d6`

```dockerfile
```

-	Layers:
	-	`sha256:25a0ff5140daf12bca2f750032f226f4efbaeb4c9991562c7e1fb051bf332d71`  
		Last Modified: Fri, 27 Sep 2024 13:24:13 GMT  
		Size: 15.5 MB (15538453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71d07f277a1de7d1fcb3c77cd4cebe931614d2f83a0ebf126d4c542154fe3ae4`  
		Last Modified: Fri, 27 Sep 2024 13:24:12 GMT  
		Size: 23.9 KB (23933 bytes)  
		MIME: application/vnd.in-toto+json
