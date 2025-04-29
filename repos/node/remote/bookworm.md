## `node:bookworm`

```console
$ docker pull node@sha256:01465bb3bd39aa65fe0be5ee6156b004bff67aac602f3ca422817f54bef8a4e5
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
$ docker pull node@sha256:de2d8c00f6b1938eefdf575b5c1efa314a48dd8842a5983ec275cb11e8e6685c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.0 MB (407021119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f76a24af9b8f715c882baf0293e931b3c9245a74eff5831c3b033bb58d6808`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:cf05a52c02353f0b2b6f9be0549ac916c3fb1dc8d4bacd405eac7f28562ec9f2`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 48.5 MB (48491199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63964a8518f54dc31f8df89d7f06714c7a793aa1aa08a64ae3d7f4f4f30b4ac8`  
		Last Modified: Mon, 28 Apr 2025 21:55:02 GMT  
		Size: 24.0 MB (24011181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca513cad200b13ead2c745498459eed58a6db3480e3ba6117f854da097262526`  
		Last Modified: Mon, 28 Apr 2025 22:15:10 GMT  
		Size: 64.4 MB (64394427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c187b51b626e1d60ab369727b81f440adea9d45e97a45e137fc318be0bb7f09f`  
		Last Modified: Mon, 28 Apr 2025 23:12:20 GMT  
		Size: 211.4 MB (211356050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca4aac67e85659abbe224961bb55400130494418a3a5a6cd8607f2af090b90a`  
		Last Modified: Tue, 29 Apr 2025 00:11:48 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2528187cde48152fcbb44693a6d1bdd71f6f92f8b1c6d4efb2e8abeb35f0a871`  
		Last Modified: Tue, 29 Apr 2025 00:11:50 GMT  
		Size: 57.5 MB (57513762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07075481b4591121b72022d6b67c81839da8da680d6deeb5f6faba023cbad4b0`  
		Last Modified: Tue, 29 Apr 2025 00:11:48 GMT  
		Size: 1.3 MB (1250731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1488e2b0ebda59af91129389da18e3979af993eb0da43d83c39bd897fcbca628`  
		Last Modified: Tue, 29 Apr 2025 00:11:48 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:e972fc884df14bd8d3073e35da91dc857c67c97ed22beed858ee046e838e5308
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15799905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8ab952f10af3ab2c0ec332860c23be8caf0fb609e56d01a14eca15f146ca728`

```dockerfile
```

-	Layers:
	-	`sha256:e3247c797c3bc9d44e8971a7b30c25e6ab3b4ba062df31e49a8508776d00914d`  
		Last Modified: Tue, 29 Apr 2025 00:11:49 GMT  
		Size: 15.8 MB (15775875 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a572c691e06365ffc030953e174bb5f8c638320baeab370630fcb45d6266a32c`  
		Last Modified: Tue, 29 Apr 2025 00:11:48 GMT  
		Size: 24.0 KB (24030 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; arm variant v7

```console
$ docker pull node@sha256:948e3f37c1a104acf46292a816676249c72194eabc6be2924839c030cd193aeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.4 MB (354437540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aed9f68b8867078bbce48771dd1259e4611e0422637302d9bb8cdb9efe61280f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:e40f48a2e6d38c2746e98a645887fe65e2b335f766dc7c61af172a1356726d5d`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 44.2 MB (44196771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d083faafd756a71980d33b1aeb908b0db85cdc7a159e3d49107170305f1bf41c`  
		Last Modified: Tue, 08 Apr 2025 07:37:54 GMT  
		Size: 21.9 MB (21918243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5414268749270f000845caf5689fb7740534b9fe922712301ba571a6afca96`  
		Last Modified: Tue, 08 Apr 2025 17:29:39 GMT  
		Size: 59.6 MB (59639425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85bd5426bd57bea2caac0e0e87b98c0988fb39decb07637e76311bc28b01e6b7`  
		Last Modified: Tue, 08 Apr 2025 20:34:20 GMT  
		Size: 175.3 MB (175297229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ae22a1b4d10aec9ffa2edd78f24ca94cc3478a44f46f3b93ef3d1dd5332c3c0`  
		Last Modified: Wed, 09 Apr 2025 00:57:44 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591d1c1535992c39916f2539fa4e71e11c8133d419516bd813de4f401a19b5e4`  
		Last Modified: Wed, 09 Apr 2025 00:57:46 GMT  
		Size: 52.1 MB (52131361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca2dbf2c159a80a11a1cc2bcbbcf94974b9ecefdc0a58538de886ff1c9fcd8f4`  
		Last Modified: Wed, 09 Apr 2025 00:57:44 GMT  
		Size: 1.3 MB (1250739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f8d1cbf7425223990d7bf9dfb2f4b1c540096be8f0e456a543564ab3f1d5d05`  
		Last Modified: Wed, 09 Apr 2025 00:57:44 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:708d962a0a75ecb39308eb4e834df322869805f174c596fe6df8100ef78788d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15604503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4deaca808787ebde2ede5730c5fe7f6147f9e9cb4ce350b00564388bb754196c`

```dockerfile
```

-	Layers:
	-	`sha256:87c93b7b0984e1d37b17f8d0f7951efb4a2684cfc70ca7a9f4fa328f7e5b8f88`  
		Last Modified: Wed, 09 Apr 2025 00:57:44 GMT  
		Size: 15.6 MB (15580323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:102666ee6ac79860294d6e076181586573df533dd28b1472c58de841f8e09c71`  
		Last Modified: Wed, 09 Apr 2025 00:57:43 GMT  
		Size: 24.2 KB (24180 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:8716fbb53b6e151684ca51923cefa7eaa1bc8a808ad861c451740c0ed38a1065
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.2 MB (397204967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21f6d560cfe1e07627a137b4673d6de11d51c2fc608e902bcffdabf6f5bbc99`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:71daa2c787b0984bbf3b93b60686fc9fe305d28e833914019b2745ab9f36730e`  
		Last Modified: Tue, 08 Apr 2025 00:22:46 GMT  
		Size: 48.3 MB (48327469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d81c64672754c46e5d99e385c8f3283bec2060a79ad7dacdb2f5ce904caa401`  
		Last Modified: Tue, 08 Apr 2025 06:03:14 GMT  
		Size: 23.5 MB (23544339 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf144460616b42eb1462fd80a5e1909e578b1e1f7285b185e468ba2b01308b9`  
		Last Modified: Tue, 08 Apr 2025 12:18:06 GMT  
		Size: 64.4 MB (64355780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:002e18bd5659ca9d155e99922678788bec836a3ac4964d8a9567ce59e2154de9`  
		Last Modified: Tue, 08 Apr 2025 15:52:42 GMT  
		Size: 202.7 MB (202735307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3cee1fc214f8bfbdeb8e88f9154354b2419758c1c408d829aca79b3c85b043`  
		Last Modified: Tue, 08 Apr 2025 17:31:45 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d544747957ac2ae95d25fa8e3bbbd67f15bb785ff0e878054438c7fc8e7af589`  
		Last Modified: Tue, 08 Apr 2025 17:31:46 GMT  
		Size: 57.0 MB (56987562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97d08f9d68c03a893258d385196226adb5afdac32c7c9b4fad6c4815c2f57d0c`  
		Last Modified: Tue, 08 Apr 2025 17:31:45 GMT  
		Size: 1.3 MB (1250737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93e0c808df8a0221371857f30c54569968ead8bcb0e6ff2ee4c4712d42da3962`  
		Last Modified: Tue, 08 Apr 2025 17:31:45 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:c474326a11eaacf816910ea1259e97363bc8174ca3c83f3f72ea7fb1bab98505
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15828708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:990d0e3c1679b238e36e2caca0658fd3ec4320c787c3343a92ba455033f1b68e`

```dockerfile
```

-	Layers:
	-	`sha256:eb4feec82b1b1d853f41934add543e3264b57e0ace6eeea88a53781518eec296`  
		Last Modified: Tue, 08 Apr 2025 17:31:45 GMT  
		Size: 15.8 MB (15804472 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6100bdd3d56cb31d7ed1d91bd26becc9aa4ec3f3efc44166d697743b95cfd51`  
		Last Modified: Tue, 08 Apr 2025 17:31:45 GMT  
		Size: 24.2 KB (24236 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:628bac0312770b5684aa6052137474c551d33f20c5ac9c445dd1be53eb880e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.5 MB (423450492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af751c341f0eecf06b31cf5c49b033df847eeaeb61aeb2d343971a962a77f2d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:96130533c16d0aeecdcc4c64baab4a3adfb31877715c21a61125a04fe062f893`  
		Last Modified: Tue, 08 Apr 2025 00:23:16 GMT  
		Size: 52.3 MB (52331646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b54c9911bf701a3c84db58a7959c7ebb5f1e34a45bad705a2799f182bc4e0bf`  
		Last Modified: Tue, 08 Apr 2025 04:30:15 GMT  
		Size: 25.7 MB (25650176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d02bafec621c70d63b6b8b80ca09a779f1c6500fb5feaa4c53d57a46c6a6ff7`  
		Last Modified: Tue, 08 Apr 2025 08:37:54 GMT  
		Size: 69.8 MB (69843923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a675af5e5720aa9e9d4f74b056a7b58aa0a84a5b3cc2c23272c361e473b9c5b8`  
		Last Modified: Tue, 08 Apr 2025 15:34:04 GMT  
		Size: 214.4 MB (214387209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cd8a86c2c8f8e15a6bb16ab78e3429bd3f4c66eb631d8fee1a04fdb7235e6a3`  
		Last Modified: Tue, 08 Apr 2025 16:47:56 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e9217860c7d2aa5c6b35135ea5c4bdf494e81c961d527cda2ab3e56475b1d19`  
		Last Modified: Tue, 08 Apr 2025 16:47:59 GMT  
		Size: 60.0 MB (59983030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d06491421148a8509e08727129a3a32c086c8fe0e9189eb159e11bc1f843513`  
		Last Modified: Tue, 08 Apr 2025 16:47:57 GMT  
		Size: 1.3 MB (1250738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4c671943454f6bb892022a29440397cd3ac88d0d89f3112bd5bc5776c5b0e3`  
		Last Modified: Tue, 08 Apr 2025 16:47:56 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:ba1cca2682fe2e8861351297127b6cb85187d7e1189442418d78f8d1c2e96263
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15776404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e856519518cba58e24bb1ee6d964f157abcce4b6de1449bc87305021e625995`

```dockerfile
```

-	Layers:
	-	`sha256:fdafd01b1b1ba92036dd482e2c3ae720fa71468250667f8f3ab99a1f2aae6541`  
		Last Modified: Tue, 08 Apr 2025 16:47:57 GMT  
		Size: 15.8 MB (15752290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83b7e9e8d00f9cb15a9a41ca181748f76ad8c350be48f2aca7ffc282777bfd91`  
		Last Modified: Tue, 08 Apr 2025 16:47:56 GMT  
		Size: 24.1 KB (24114 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; s390x

```console
$ docker pull node@sha256:38ff015c6a059579b8622cb5997c6a5ecca2c649463dd39b2d8ae8d07f92cdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.9 MB (375925027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9edcc89223a293e5e3ada3c1dff1c703314a564535bc9ca83cd7c9d9999ab7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV NODE_VERSION=23.11.0
# Tue, 01 Apr 2025 16:05:11 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENV YARN_VERSION=1.22.22
# Tue, 01 Apr 2025 16:05:11 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 01 Apr 2025 16:05:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Apr 2025 16:05:11 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:02fcba40f83e05adf85891b5c708b183d1028fd36fd80528f148e95bf593ab77`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 47.2 MB (47150996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39a93e29489c173c9f7bae02e4e3f728f3e5b721748076de87502e6e9fd9108c`  
		Last Modified: Tue, 08 Apr 2025 03:44:19 GMT  
		Size: 24.0 MB (24008336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4fde99ce0eec506f038695c59ba0ff56bd0df358636c0b067f55c60d7d566c`  
		Last Modified: Tue, 08 Apr 2025 06:52:25 GMT  
		Size: 63.5 MB (63498375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766d2c4791b14ffb813f2bd4d87d95e9030a5939b65f31722bc2c223f845ecf8`  
		Last Modified: Tue, 08 Apr 2025 10:02:09 GMT  
		Size: 183.4 MB (183388438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7742459d60875a0ddf9ec76191753f31c6746abb748c43747b03d8db49ab3f3c`  
		Last Modified: Tue, 08 Apr 2025 15:02:37 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:608575ff104279dfabf121de64c29d00122bdbd0ffa4cbd9186d332546453ee4`  
		Last Modified: Tue, 08 Apr 2025 15:02:39 GMT  
		Size: 56.6 MB (56624367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e0998ea840077ddbfa73aef3a1795a56eedbcd93edd1c4fb4a1d4c5eca937d0`  
		Last Modified: Tue, 08 Apr 2025 15:02:37 GMT  
		Size: 1.3 MB (1250740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155e9fba46bf542f151533efe1e4ae7bb49dc7d3119712e4f756674e26b77fa4`  
		Last Modified: Tue, 08 Apr 2025 15:02:37 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:001d50e8afb064269d7de4a71af1ac011fc085237696e4615c8b5e47458d7fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15612593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfe91e78c3c43519f28ed79464b78930aec496f6c067a80f524a2183f5efe63`

```dockerfile
```

-	Layers:
	-	`sha256:5d35ce39ca0eb31c1ecd0f3af4944a2f12ba91dd99fe600ca7b79b8300fa1e9f`  
		Last Modified: Tue, 08 Apr 2025 15:02:37 GMT  
		Size: 15.6 MB (15588565 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a08e2926dbaea9e821e987cce702354b28cee82c7f0decea4b3f38713d56609`  
		Last Modified: Tue, 08 Apr 2025 15:02:37 GMT  
		Size: 24.0 KB (24028 bytes)  
		MIME: application/vnd.in-toto+json
