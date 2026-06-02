## `node:trixie`

```console
$ docker pull node@sha256:e3ffe0cbaeebdcddbfe1ee7bca9b564a92863a8386d5b99a3d72677b3667b61d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `node:trixie` - linux; amd64

```console
$ docker pull node@sha256:e902ef409edeb22827bac179d5e6ffabe6b21360fe02eeeef85b6857d7217c3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.0 MB (442048280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3944d959a8c66ea55985ea45bc4efb2d4838f31050d7b3977dae279c7630b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:23:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:26:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 01 Jun 2026 22:47:17 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:47:27 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:47:27 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:47:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:47:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:47:27 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:f32f49ce655a9cf7c1fd4ca1417ddb39a54cedf4b7ff35de20f8009c18dd7a96`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 49.3 MB (49310623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a7504cd2818ce40ac76c17886a03dff25ef0aa06ff6125bf0f0c7302cdc6471`  
		Last Modified: Tue, 19 May 2026 23:23:34 GMT  
		Size: 25.6 MB (25633915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53089dca50590292ecc77bf803152a5799650e734717e4b706cb812a02073ba`  
		Last Modified: Wed, 20 May 2026 00:26:48 GMT  
		Size: 67.8 MB (67777732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d6d44b254dab2063c4226fc8a0849d5527402d24d3bea80d644a1e4ac3a47e5`  
		Last Modified: Wed, 20 May 2026 01:16:36 GMT  
		Size: 236.2 MB (236176097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddfbc78780d696c1792bb7621307866d98a9775b5ab6669b0e56bcec0b286627`  
		Last Modified: Mon, 01 Jun 2026 22:47:56 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:919b1f297f1dabb7d9436b529f96bc9bbfc8d175af8bc24328ed94a56793112e`  
		Last Modified: Mon, 01 Jun 2026 22:47:58 GMT  
		Size: 63.1 MB (63146140 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743d264d8aaf570c0323fd602d03c5b81ae3db06aa10fa2e8c07bb0db203b05f`  
		Last Modified: Mon, 01 Jun 2026 22:47:56 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:trixie` - unknown; unknown

```console
$ docker pull node@sha256:f30453d45cbfa764075c99fd13324a145ae74cd678c0eb505c7fbba6f722d718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17432216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ab9de64cdd91dd650306636f8034286dd431dd8f003beca55b496553875c1ad`

```dockerfile
```

-	Layers:
	-	`sha256:2ad9d9f1dad0bbbfded245e55ff45e65d39faa618b197c3ddc4b4e73fe3bffef`  
		Last Modified: Mon, 01 Jun 2026 22:47:57 GMT  
		Size: 17.4 MB (17413253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ba51d7354ab883523ee6f82662a2e936a45c46c745a6ff905418fda24e7786f`  
		Last Modified: Mon, 01 Jun 2026 22:47:56 GMT  
		Size: 19.0 KB (18963 bytes)  
		MIME: application/vnd.in-toto+json

### `node:trixie` - linux; arm64 variant v8

```console
$ docker pull node@sha256:c59b5800f7cc97f6e15ba67c40410297c97df7ed67bfe2ec35f265f38f6d6f61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.0 MB (431955116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:014615ecd695adf99a229edb53d4b64b2cdc4f13e426bfa4d3e27f21ffcd15a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:27:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:27:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:15:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 01 Jun 2026 22:47:49 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:47:58 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:47:58 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:47:58 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:47:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:47:58 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:635135721e54f918d2d81497bc66b71f98aee3b440dd6498218827c56d7d277f`  
		Last Modified: Tue, 19 May 2026 22:37:01 GMT  
		Size: 49.7 MB (49672220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28313c8eaf165ac06f26bda4877768677cf5e44e5c61ec169a81b436b2e985b`  
		Last Modified: Tue, 19 May 2026 23:27:16 GMT  
		Size: 25.0 MB (25025606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39feea71264a587b284d92fded7754becc4682529629dd95c8bc3dd25a948a27`  
		Last Modified: Wed, 20 May 2026 00:27:52 GMT  
		Size: 67.6 MB (67592849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2882152811f66f9d033b8e9ebaa0473ab189d50d1a24186fe1ee418225e96521`  
		Last Modified: Wed, 20 May 2026 01:16:38 GMT  
		Size: 226.3 MB (226326757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd264eb324d00a0b9a0fa88ebc903688a51cbe10d104bfbf460186306ee06581`  
		Last Modified: Mon, 01 Jun 2026 22:48:29 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:203fdd9313dd348d6470e8763df60da41d759ee6f7516026ab0a61955db14b4f`  
		Last Modified: Mon, 01 Jun 2026 22:48:31 GMT  
		Size: 63.3 MB (63333909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f1a73884c0b5862b6f458447096a13225fd25a8bf6019dd0c73b39572dea0c`  
		Last Modified: Mon, 01 Jun 2026 22:48:28 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:trixie` - unknown; unknown

```console
$ docker pull node@sha256:c08d3a2cc79331d5263ae696fdf6bfb5e889b54f97a62a65ff4f2c4c6b68d802
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17516148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4336828ccdd64b0957680941d77855b6c609144c7f5344522e2c34c6580caa14`

```dockerfile
```

-	Layers:
	-	`sha256:abcd61933c8e5253148578e42f2e9e678b38de08147544c83e039bdd28947ef2`  
		Last Modified: Mon, 01 Jun 2026 22:48:29 GMT  
		Size: 17.5 MB (17496994 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e10e68dfc7d68cb73335bdf4f33286799875931caf91cbf4d6433f523afdb738`  
		Last Modified: Mon, 01 Jun 2026 22:48:28 GMT  
		Size: 19.2 KB (19154 bytes)  
		MIME: application/vnd.in-toto+json

### `node:trixie` - linux; ppc64le

```console
$ docker pull node@sha256:4b9d0c1c82fd1ff7f97266bbbf2b514c26dd92c2bd8da9671a15344e840eb3d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.9 MB (449947462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e794d8dbbe82eafcf19aa773d308aa4cd78f4b58c13da9ff4b6503b92f34501b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:14:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 06:52:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 09:10:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 01 Jun 2026 22:47:37 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:47:50 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:47:50 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:47:51 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:47:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:47:51 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:55497c62a793e62a2e78a3fd85fcedf060da73e331ad107733199ea991106b96`  
		Last Modified: Tue, 19 May 2026 22:37:59 GMT  
		Size: 53.1 MB (53132182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:743dcca676e80d0b7074d4f03820f8068053078d4942f2a921fdf172c62897ae`  
		Last Modified: Wed, 20 May 2026 01:14:53 GMT  
		Size: 27.0 MB (27021149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7396fcf223bd659e5dda1b961ab403e3df6f9d118708751addc02badc2015799`  
		Last Modified: Wed, 20 May 2026 06:53:00 GMT  
		Size: 73.0 MB (73042459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06bf5baaa69eb61df93cfa5666d94d0c8ad399bda9d0ffc7582002bfe76ba1b4`  
		Last Modified: Wed, 20 May 2026 09:11:54 GMT  
		Size: 231.3 MB (231309802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e805d369b364b36b4b1174cd6b51abf9d6effdd368cbb6e8f9d834aabca582f`  
		Last Modified: Mon, 01 Jun 2026 22:49:06 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e517a19252b033b4939769050c4a622769b2b340fbda31be1b04e8e8260c355e`  
		Last Modified: Mon, 01 Jun 2026 22:49:08 GMT  
		Size: 65.4 MB (65438098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec35e4d018e4e407aa3b86c4f45acc9e7cd79e3923dfc09c8cf63efa5150b42`  
		Last Modified: Mon, 01 Jun 2026 22:49:06 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:trixie` - unknown; unknown

```console
$ docker pull node@sha256:e19143419d192e1ee7e5ffc10e8100b5648fce84cc85b62bb8057d11649738ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17417877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5354793ff43c4b978580d80c8affa52d8399fe912b5bd5d6956ccc86f8b680b`

```dockerfile
```

-	Layers:
	-	`sha256:e89dc2353235c5cac7809eec67c68f07796ee6b885d94f40573a0e5ff79601fa`  
		Last Modified: Mon, 01 Jun 2026 22:49:07 GMT  
		Size: 17.4 MB (17398832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2ee81f6d3abfc43c2245a4baa060e1186137f28077619fecccaf07040f375be`  
		Last Modified: Mon, 01 Jun 2026 22:49:06 GMT  
		Size: 19.0 KB (19045 bytes)  
		MIME: application/vnd.in-toto+json

### `node:trixie` - linux; s390x

```console
$ docker pull node@sha256:bc53a950161abef4943caf51330107f2894f14a0e830124946b6600c259302f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.2 MB (416160057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d5e7249f13997b2ee9d42895cf0efded5d33077e2dc035128a4a8def6d518b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:18:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:44:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Mon, 01 Jun 2026 22:45:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:07 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:07 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:1540dbb0587ae9097c9d04c50809503aa74d42814940d640c6659645acc0bc6c`  
		Last Modified: Tue, 19 May 2026 22:37:00 GMT  
		Size: 49.4 MB (49379780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a95ac44f164c9c275ab328d3f5219a9cee0e2be081ed2ce1bb7cb8135bd49f`  
		Last Modified: Wed, 20 May 2026 00:19:10 GMT  
		Size: 26.8 MB (26804813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab366c3de62691a29444d50ed3d26e9d7524b8314a9b46521cbec555e978032`  
		Last Modified: Wed, 20 May 2026 02:06:37 GMT  
		Size: 68.6 MB (68638051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:670b9b1c4f415c6933bd1559c9c20d59c3dc10986a265d1744b77a8f0cff5bf8`  
		Last Modified: Wed, 20 May 2026 02:45:35 GMT  
		Size: 206.7 MB (206680668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa86ad99d5adb17b8d5ebbaa994baa77081c7ecfe60df7679b08195d9b8128e`  
		Last Modified: Mon, 01 Jun 2026 22:47:02 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e20cfd00756791125db3aca6d6c40341f30e0768fbaadaaef6de01c83d0b2f`  
		Last Modified: Mon, 01 Jun 2026 22:47:03 GMT  
		Size: 64.7 MB (64652980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe03c3a0d78d5c80dacd17049f592376131841ef67f9fc9fb435da75ad6a2fd`  
		Last Modified: Mon, 01 Jun 2026 22:47:02 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:trixie` - unknown; unknown

```console
$ docker pull node@sha256:fec8520ab8f26123947dfc35d032f85198337cea653dda333783dd483e951302
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.2 MB (17209449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc73e1c20f7c652d199c2e1a57605a43c0f78c5daa115e7b36270409c310c7e`

```dockerfile
```

-	Layers:
	-	`sha256:e921151f6db10124a462a3d337594d07b6fdabde2d37724b437b2946a2efcb5e`  
		Last Modified: Mon, 01 Jun 2026 22:47:02 GMT  
		Size: 17.2 MB (17190486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e39b100c90b8cfbb65912ee08e865142ee65e2bb9c56f58bd9f4332c12053f6`  
		Last Modified: Mon, 01 Jun 2026 22:47:02 GMT  
		Size: 19.0 KB (18963 bytes)  
		MIME: application/vnd.in-toto+json
