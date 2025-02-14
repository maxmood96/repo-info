## `node:23-bookworm`

```console
$ docker pull node@sha256:7411c6b1f0816389ecd4e69bad86e0222818ec10bf91fb2a5076f461104cd013
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

### `node:23-bookworm` - linux; amd64

```console
$ docker pull node@sha256:e27f5342fa34aa9a34dbc4d47b66953010cc3a8e1c76d1708ca06d163741e56b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407241799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8b766f73aa0a7076042bf2610b0a0fa0bd055884539b1d207db00fda1f01210`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
ENV NODE_VERSION=23.8.0
# Thu, 13 Feb 2025 19:20:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 13 Feb 2025 19:20:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:20:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a492eee5e55976c7d3feecce4c564aaf6f14fb07fdc5019d06f4154eddc93fde`  
		Last Modified: Tue, 04 Feb 2025 04:24:49 GMT  
		Size: 48.5 MB (48479687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b550be6cb62359a0f3a96bc0dc289f8b45d097eaad275887f163c6780b4108`  
		Last Modified: Tue, 04 Feb 2025 07:11:25 GMT  
		Size: 24.1 MB (24058355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35af2a7690f2b43e7237d1fae8e3f2350dfb25f3249e9cf65121866f9c56c772`  
		Last Modified: Tue, 04 Feb 2025 08:41:29 GMT  
		Size: 64.4 MB (64394292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7576b00d9bb10cc967bb5bdeeb3d5fa078ac8800e112aa03ed15ec199662d4f7`  
		Last Modified: Tue, 04 Feb 2025 08:23:04 GMT  
		Size: 211.3 MB (211328049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffda812dab268748c8d133d786313957a5b0d5f376fddb93e3e55a740f87e71`  
		Last Modified: Fri, 14 Feb 2025 00:19:58 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f618bded8e133e17af6bbe282eb1d5d534759d641d25b61f880bb25847032144`  
		Last Modified: Fri, 14 Feb 2025 00:20:02 GMT  
		Size: 57.7 MB (57726915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7789767e4aeb8f4a286d36243e21c3d300e213474600f90932811b1b4fd9edb`  
		Last Modified: Fri, 14 Feb 2025 00:19:59 GMT  
		Size: 1.3 MB (1250736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:391d39c2ae69aba3508fd5b486e3f9322fb8e4e5a3f80823855bcc21e83d1534`  
		Last Modified: Thu, 13 Feb 2025 22:28:05 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:23-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:4037aac400b3c94a0a791b7dc309ad0c33f2f46a304408d3028a61d2b9dfc245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15802753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ede5793a8d1eb220e0dac6c16754e34402c1752241d62f8d15a39cb352a8de58`

```dockerfile
```

-	Layers:
	-	`sha256:f056720d2b03170be4c70407d365151b5463161fc828e1bfe37429fa1608ac99`  
		Last Modified: Fri, 14 Feb 2025 01:39:38 GMT  
		Size: 15.8 MB (15778733 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d4e253fe7e3923c47e2c3209ea41ca50cd53392fc6a0c897f648fb684b1cb2e`  
		Last Modified: Fri, 14 Feb 2025 01:39:38 GMT  
		Size: 24.0 KB (24020 bytes)  
		MIME: application/vnd.in-toto+json

### `node:23-bookworm` - linux; arm variant v7

```console
$ docker pull node@sha256:710b8ec6050e26164ef800f810e075550dba73b56e696efd1127d4e2342e5e05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.2 MB (354213000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:342f2d2222fcf063d99230c7c0f91a8d2a1a80dced7dfd3682b2af8dc187442b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV NODE_VERSION=23.7.0
# Fri, 31 Jan 2025 17:21:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV YARN_VERSION=1.22.22
# Fri, 31 Jan 2025 17:21:26 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Jan 2025 17:21:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:bf65c309bba1c843ac26792f2d942bca2d7bfcc7024ba331cdfbb762d7573e8a`  
		Last Modified: Tue, 04 Feb 2025 05:02:17 GMT  
		Size: 44.2 MB (44184052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97dba4073c18c1d2882f0eb9a2b0d9bf057770ac1b8829e3e149a095273df800`  
		Last Modified: Tue, 04 Feb 2025 23:37:50 GMT  
		Size: 22.0 MB (21960085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66806698bb37ab9f15c9072a66ade0dcacacec8794e48afd7fdc2e801ccb928a`  
		Last Modified: Wed, 05 Feb 2025 04:00:39 GMT  
		Size: 59.6 MB (59639147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb08f2dfbcde333a583952948ebc4e632dcbb5e80617adcb1cf802d99c434d0`  
		Last Modified: Wed, 05 Feb 2025 08:37:36 GMT  
		Size: 175.3 MB (175281303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9cc8ea202fed9c017a286fdcf78796e780f83ea16a0220c1c977adeb48ea1e`  
		Last Modified: Wed, 05 Feb 2025 10:42:19 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d85153b543243d17d04011ed450094f807db4824d965f2cfcc5b933987b2208`  
		Last Modified: Wed, 05 Feb 2025 11:01:40 GMT  
		Size: 51.9 MB (51893914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3aa5b49d5ded9c5648c7761811a7df05ac4f7bb83c5e52dec8c2e836f19f38`  
		Last Modified: Wed, 05 Feb 2025 11:57:49 GMT  
		Size: 1.3 MB (1250732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904da7cada11c1a0e69592373a059b693afca42de09cbec7a599a8431aeead31`  
		Last Modified: Wed, 05 Feb 2025 10:53:26 GMT  
		Size: 443.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:23-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:8ad8c186addc22f6653f7f247723ef0645a276a6d674b63f94d5f89efeafc510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15607350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:654ab43158b1bac8b383974cd916af6dc613237e83ebabeae1cf68c26747e6ac`

```dockerfile
```

-	Layers:
	-	`sha256:40e81bf477aab1aad43097d8c8ba324a7b012a2a876d457e186ba8cb09f264ee`  
		Last Modified: Wed, 05 Feb 2025 13:02:24 GMT  
		Size: 15.6 MB (15583181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a6deda5f3275af45db252f5499dec16c13130b653fc001ad372d66e9c24ad5c4`  
		Last Modified: Wed, 05 Feb 2025 13:16:43 GMT  
		Size: 24.2 KB (24169 bytes)  
		MIME: application/vnd.in-toto+json

### `node:23-bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:3c2ddf521763d0e7785003bb9c01b5c089b82b9eaaa9d3875d7411e700acc37d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 MB (397420332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc264c3dbb1c0707f50db3e9e3c6ebb0349edff83f99f4c714a32fef8ea82c3b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
ENV NODE_VERSION=23.8.0
# Thu, 13 Feb 2025 19:20:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 13 Feb 2025 19:20:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:20:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:106abeaee908db66722312b3379ae398e2bcc5b2fdad0cc248509efa14a819ff`  
		Last Modified: Tue, 04 Feb 2025 04:37:12 GMT  
		Size: 48.3 MB (48306553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:193c44006e77abbadfdd7be72b4ab6d7a5c08640ef575970f722b798ee7800ac`  
		Last Modified: Wed, 05 Feb 2025 00:14:09 GMT  
		Size: 23.6 MB (23598428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d3572a68af0b860060b7ea84adfa8406fa20cfd1337c947dfb661aa965eee7`  
		Last Modified: Wed, 05 Feb 2025 02:21:14 GMT  
		Size: 64.4 MB (64357505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9611c2b713640ce0f9156445b244c4da5e621183b56c0901d97a8b6d54ce10d7`  
		Last Modified: Wed, 05 Feb 2025 02:24:38 GMT  
		Size: 202.7 MB (202718404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c21298d709bbe636f8e0117479908714e3c57fc25c29912ba1a879d9fe3b6be7`  
		Last Modified: Wed, 05 Feb 2025 10:08:16 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a817b2a8a44c3fae5240180c8b3420259fc5cdebc3d1bede570aa55b008545ea`  
		Last Modified: Fri, 14 Feb 2025 01:30:04 GMT  
		Size: 57.2 MB (57184939 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf743ecf4cc3c11c5f7baaa85eb084487bd5f637e8b500a58e461b0e2587a060`  
		Last Modified: Fri, 14 Feb 2025 01:30:03 GMT  
		Size: 1.3 MB (1250734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0737ac794cfc42aae44bda82df9f3865cd671ceb20ce8989ea8f50aad7b211`  
		Last Modified: Fri, 14 Feb 2025 01:30:03 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:23-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:3db33aa804865e7a8df1d1c5fd9586a1ab302cc18ae6ed58ecdb1c45a4c0851a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15831556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3676841870855a7a6ed2d936c8167e05dc538bb58628c4544c0388fd13c7883`

```dockerfile
```

-	Layers:
	-	`sha256:291829601a8298bda6a00fb4e0521a31a681835ee9f4492dfcca56222112f2a7`  
		Last Modified: Fri, 14 Feb 2025 01:39:55 GMT  
		Size: 15.8 MB (15807330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:721ba3a8d2098223b523dd674caef2f52ff442eea468f0f43fad36792757572b`  
		Last Modified: Fri, 14 Feb 2025 01:39:56 GMT  
		Size: 24.2 KB (24226 bytes)  
		MIME: application/vnd.in-toto+json

### `node:23-bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:dd6890f838a74b7bc1b67fcb6eaabf2c83be5971e320cc0a6d422ecaa9bf33b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.7 MB (423734748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df82ff54ae0b45a0f7da37f36ef851ca7c2ef28db4ec0d165052802e71b1cd62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
ENV NODE_VERSION=23.8.0
# Thu, 13 Feb 2025 19:20:00 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
ENV YARN_VERSION=1.22.22
# Thu, 13 Feb 2025 19:20:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 13 Feb 2025 19:20:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 13 Feb 2025 19:20:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:d32dc8295067a6f744a1fca9cfffe021a324e651f2834ad7b587e0380c3f2981`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 52.3 MB (52312857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27f161b1ac6fcd1e84495441a30458604c921f0c00816d0cd0926964e56d9717`  
		Last Modified: Wed, 05 Feb 2025 00:47:58 GMT  
		Size: 25.7 MB (25717668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7451c2aa1d936ee2bec4ea4db323da11f1dc2694095c250c16b70763100f29cf`  
		Last Modified: Tue, 04 Feb 2025 18:00:23 GMT  
		Size: 69.8 MB (69842739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:556dba2526850ef13f84af87d0289a40f2451777be07098d04c55f33c7f76b83`  
		Last Modified: Wed, 05 Feb 2025 02:08:13 GMT  
		Size: 214.4 MB (214366038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2ed15c7e85551f3c906024c76727582d5c97a774554d7449df61d68aec3e22`  
		Last Modified: Wed, 05 Feb 2025 08:01:03 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d987f9fcee1b09ec99de13e95db0e318e43d9f02bb7629edfd1a947314485890`  
		Last Modified: Fri, 14 Feb 2025 01:46:56 GMT  
		Size: 60.2 MB (60240940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ba5f103c047366402598dd0a9d33181e8b5dd1513e0dcd6b193d60ef022be6d`  
		Last Modified: Fri, 14 Feb 2025 01:46:44 GMT  
		Size: 1.3 MB (1250736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6516851e6b7f6a4ea5e77f36d0c0ac5b29eb6f39ddc8eb0b84e11268565c0e4e`  
		Last Modified: Fri, 14 Feb 2025 01:46:42 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:23-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:ff06d4511642a039cb11425a8910a468c1c71b4d867f372565d45950f96d5ece
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15779257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a64996e8bf8894cf4c35e8a458de2516741a0249922f46a543c366a18d64936`

```dockerfile
```

-	Layers:
	-	`sha256:197963114413e709f6853224060fd37bdbc26f7797e6417f13e0e02e766f37de`  
		Last Modified: Fri, 14 Feb 2025 01:40:05 GMT  
		Size: 15.8 MB (15755154 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb21da9b6045783cdb8c39a327be28a256ace6da98c315817b7ecdf5f2e4d742`  
		Last Modified: Fri, 14 Feb 2025 01:40:05 GMT  
		Size: 24.1 KB (24103 bytes)  
		MIME: application/vnd.in-toto+json

### `node:23-bookworm` - linux; s390x

```console
$ docker pull node@sha256:bbbcfc831a67ceb60a8a04202e1ef8699d3a10f7f2f8f3297cdba504c6050521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **375.7 MB (375677231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade05f6ba2fdb0eb54619064042b77db09320e5839193a3d0bdb12fca9b5572d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1738540800'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV NODE_VERSION=23.7.0
# Fri, 31 Jan 2025 17:21:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENV YARN_VERSION=1.22.22
# Fri, 31 Jan 2025 17:21:26 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 31 Jan 2025 17:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Jan 2025 17:21:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:92bc3bb38690fde96c4bb788f15f365b04d4cb8ab9368675dc9294bc24a9c7b6`  
		Last Modified: Tue, 04 Feb 2025 05:09:29 GMT  
		Size: 47.1 MB (47131492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe7257ceffda4bd6219bda9d63efd9f5fc932de95d2f5db69f3d95df88e73b0`  
		Last Modified: Wed, 05 Feb 2025 01:13:32 GMT  
		Size: 24.1 MB (24057578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:800fd1d6411dfa44ccdbe5db47bb7e970909c1a08d63328dfd165607beb67e7c`  
		Last Modified: Wed, 05 Feb 2025 00:15:03 GMT  
		Size: 63.5 MB (63499455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959543dffffce198d7241bd6958a549b695b11519fad12fc54ebe4df4b49bea4`  
		Last Modified: Wed, 05 Feb 2025 01:13:38 GMT  
		Size: 183.4 MB (183365325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13389cc06c4fc2807e255b85a4f6043f49163356acd6b9252d4162421c813a0c`  
		Last Modified: Wed, 05 Feb 2025 04:54:09 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff0bd5473d46d7749823e969a50ee373fca104c97e52d7d8230b21438d5db61`  
		Last Modified: Wed, 05 Feb 2025 06:23:53 GMT  
		Size: 56.4 MB (56368873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3a0fdd6584a69677c8e486ca4505db2c6a82e2b50ae66ae2b645377accd3ad`  
		Last Modified: Wed, 05 Feb 2025 05:01:02 GMT  
		Size: 1.3 MB (1250740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44740cf030a2447951861c3b8877799a6fa83e5abcf3192203eaf79a97aaec8b`  
		Last Modified: Wed, 05 Feb 2025 06:04:10 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:23-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:f61d146d88aac4e87e68be02dc6393969b02ca9ffbc279be0f60263d26ac242b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15615442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ff6704f3414ede1cd890ba32fcf2109c514ffb6e5eb01411fc8ace408eb35a`

```dockerfile
```

-	Layers:
	-	`sha256:2fd7537b579a092055a24c322bd1750f063795ef21ae9044f9f16a176753a186`  
		Last Modified: Wed, 05 Feb 2025 06:03:57 GMT  
		Size: 15.6 MB (15591423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8dca35b8d1e6f52544e92d804f04309c61cc9d943e103e5d75244e654198a96`  
		Last Modified: Wed, 05 Feb 2025 05:01:00 GMT  
		Size: 24.0 KB (24019 bytes)  
		MIME: application/vnd.in-toto+json
