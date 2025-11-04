## `node:20-trixie`

```console
$ docker pull node@sha256:c79f5ed9e6630723cbed4221db47a53d37844598e40800a236b2c664a4740638
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

### `node:20-trixie` - linux; amd64

```console
$ docker pull node@sha256:1b4e61cbee69bc826d36652e6256c36bc501c5fb488080368507975e83c450fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.3 MB (428277578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc92477c256c1e719a110135df5c32c6aebee31db83e7eda581511f2aef70b1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:14:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 10:58:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:27:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 14:27:35 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 14:27:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 14:27:35 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 14:27:37 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 14:27:37 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 14:27:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 14:27:37 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:13cc39f8244ac66bf1dd9149e1da421ab1bbc80d612dc14fe368753e7be17b33`  
		Last Modified: Tue, 04 Nov 2025 00:13:22 GMT  
		Size: 49.3 MB (49285628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3143549f2b8b3ad8d79efdc47824641c6771796b3770f3c637a38aabd2b3462`  
		Last Modified: Tue, 04 Nov 2025 04:14:53 GMT  
		Size: 25.6 MB (25615393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72e8e93b0d018b135d833207c6feaba205653ac52e0a80d214477ec0de239dee`  
		Last Modified: Tue, 04 Nov 2025 07:43:02 GMT  
		Size: 67.8 MB (67776858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d55a674b2e3641a37b7f2053f00af6fe4f2a89576ffb917d4b7b4deaf24591`  
		Last Modified: Tue, 04 Nov 2025 11:23:13 GMT  
		Size: 235.9 MB (235937246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62d2ed4afe189abad791f874faaff3837e2634614b412ddd8a21b57157a9daae`  
		Last Modified: Tue, 04 Nov 2025 14:28:13 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79360bda4b8ff43dbeb1d94018216344b90296e721053ecb3b06a791bbb85f35`  
		Last Modified: Tue, 04 Nov 2025 14:28:17 GMT  
		Size: 48.4 MB (48408002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f48b22afab0e38500222949ed2b5072fff49187a28b37f786ba86ce2473371e4`  
		Last Modified: Tue, 04 Nov 2025 14:28:13 GMT  
		Size: 1.3 MB (1250678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee1709de73e4509c620131e2ce0bcb8ab94a40671d75f35fdb7ce225d0b99454`  
		Last Modified: Tue, 04 Nov 2025 14:28:13 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-trixie` - unknown; unknown

```console
$ docker pull node@sha256:ef3947fa253a723f74b7c3ad3fa1e59f711909efd5af5186e95f66090e036003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17518177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ff1d15020ceeabc8c0f591a3e5d72f2c61d4c8b822d11b47ec280bc26f75727`

```dockerfile
```

-	Layers:
	-	`sha256:fbb40c90288922e0e920e10d60b8df8a34ebf6755045863489dc69c5fa75d11d`  
		Last Modified: Tue, 04 Nov 2025 16:38:34 GMT  
		Size: 17.5 MB (17495457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd3aa52fa2ac7d0d77208429014140356fdd3e06f63409b03625b1e7edec58c`  
		Last Modified: Tue, 04 Nov 2025 16:38:35 GMT  
		Size: 22.7 KB (22720 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-trixie` - linux; arm64 variant v8

```console
$ docker pull node@sha256:42b3060c2f7e8632437e96fc08c2c3ff02ce6b821f1119a0616fabce43361676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **418.0 MB (417954812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd875dc79a44b641c95f6d25d131b1489dbcaae4c7c65b6baa5f8dfce151365f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:29:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:15:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:16:03 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Tue, 04 Nov 2025 04:16:13 GMT
ENV NODE_VERSION=20.19.5
# Tue, 04 Nov 2025 04:16:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 04:16:13 GMT
ENV YARN_VERSION=1.22.22
# Tue, 04 Nov 2025 04:16:15 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Tue, 04 Nov 2025 04:16:15 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Tue, 04 Nov 2025 04:16:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 04 Nov 2025 04:16:15 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:04077a68e2b807cad70ec4dfc0a2e8e1ff1ea6d9523e4c8f042b9a1ae8a54409`  
		Last Modified: Tue, 04 Nov 2025 00:13:46 GMT  
		Size: 49.7 MB (49650430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f766ef2ec48737a0f300405019c312acd667d14467b50c402750d1454e3591`  
		Last Modified: Tue, 04 Nov 2025 01:30:11 GMT  
		Size: 25.0 MB (25017577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:186d0d0b2411f880d1a385216013fead1acb2dee0584aac75da87dfdeb1202db`  
		Last Modified: Tue, 04 Nov 2025 02:21:20 GMT  
		Size: 67.6 MB (67583874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91656fd58bb5f57cac88ac067f1fad07e73ca96589dd592517520d14bd020eb7`  
		Last Modified: Tue, 04 Nov 2025 04:13:49 GMT  
		Size: 226.1 MB (226079884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5645736a83e92728815badec74ba9904138e32589687894d4871001a6ca5a73`  
		Last Modified: Tue, 04 Nov 2025 04:16:51 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554abf610c02c53b1a3a5750be0aa25a308e92c7dcd555d910d50b9764de32e0`  
		Last Modified: Tue, 04 Nov 2025 04:16:53 GMT  
		Size: 48.4 MB (48368608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30d0a7765a2e81f8efdbac697eaaddaeb86d47735f5ac38c5987e106d842d1e`  
		Last Modified: Tue, 04 Nov 2025 04:16:51 GMT  
		Size: 1.3 MB (1250673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917f393b5cd114d76aed6a17f8dcf2edb838263eef97d41df7515e699fdb31f1`  
		Last Modified: Tue, 04 Nov 2025 04:16:51 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-trixie` - unknown; unknown

```console
$ docker pull node@sha256:25353387ee3f55dec9ef9125764347ba891a15f54780f99d1d22bcbfb5d62681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17602617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cc5b10ac2d4c9d4044bf5195d303fad874ee4f88214eca5fbb8460b82636281`

```dockerfile
```

-	Layers:
	-	`sha256:a48985a9f76f65c137440e8b01d85c7645de891ed15a6a7064d78d9cf90e0e09`  
		Last Modified: Tue, 04 Nov 2025 10:39:32 GMT  
		Size: 17.6 MB (17579763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2bfb92ec4018a2f1c2d0b1381151f2ff796ba3e6e532fdfe5bb7d80ee8e04b6`  
		Last Modified: Tue, 04 Nov 2025 10:39:33 GMT  
		Size: 22.9 KB (22854 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-trixie` - linux; ppc64le

```console
$ docker pull node@sha256:71b5cc6839b2e4729078d8ca46f6827a9625fba188a4252894a159c6bec2320c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.4 MB (436373474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75036675197617f9e48e91d44060f91addfdd2dd55062dd63bb63c974a01feb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:047d1b265d8a7d20ef8b3ccb9f133c3c5f1e4f9c92089889756590b7f20452b5`  
		Last Modified: Tue, 21 Oct 2025 00:26:24 GMT  
		Size: 53.1 MB (53109476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62dfb88672cf0a942c4fdfcadf1912c35c9d30a3a001b18a9dad505fb960ae8`  
		Last Modified: Tue, 21 Oct 2025 07:47:00 GMT  
		Size: 27.0 MB (26996207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06029381e2f1b3a0885caf1b758b0461bfaf9db7b9642ca0b79ab28ed1dd4ecc`  
		Last Modified: Tue, 21 Oct 2025 17:35:58 GMT  
		Size: 73.0 MB (73029685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac677cb325b211e7ad7714eb6d52abf13c0d7630be372cac77812dd27241a158`  
		Last Modified: Wed, 22 Oct 2025 01:27:43 GMT  
		Size: 231.1 MB (231086523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7057b20b5fb8d4dd2b526140fa8de0dfd93fc19ffd5b8c6619ae385bae7e5d9`  
		Last Modified: Wed, 22 Oct 2025 04:59:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c95e2b62f0eb43d0350faa8ff3921947748f11657f8111f259c0293fabcd72ea`  
		Last Modified: Wed, 22 Oct 2025 05:10:04 GMT  
		Size: 50.9 MB (50897136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ed7ccf30275d0da0fb4fbd709a649f0e00e2f4760a1040d3b70d26bdbd762b`  
		Last Modified: Wed, 22 Oct 2025 05:10:01 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:878206a894683169d2ee39d125a4d1daec325e081b01221094cd8e80f2a197c8`  
		Last Modified: Wed, 22 Oct 2025 05:10:01 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-trixie` - unknown; unknown

```console
$ docker pull node@sha256:3e2b2a2d50e55815870bce90aafb5e484557f637f72040fe6ceec4f7d1a4ea71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17503823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c40a2e64177bd7bcb24543b53d46ab8fa6ca3bd5f0c195cc3d6300d3309f5314`

```dockerfile
```

-	Layers:
	-	`sha256:952af4496776749b33ab943c110c87f1414dc297511b692bf692d6a42a0e8c66`  
		Last Modified: Wed, 22 Oct 2025 06:39:22 GMT  
		Size: 17.5 MB (17481012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9d72f28267c5b738c2b96d47569f85bc86af50eaf900c9aa11dea06c942d2ee`  
		Last Modified: Wed, 22 Oct 2025 06:39:23 GMT  
		Size: 22.8 KB (22811 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-trixie` - linux; s390x

```console
$ docker pull node@sha256:bb2e218a20db785b294e997db62d4a49ee0ff303ca4dbf03ff909ff3edf1e83e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400698734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25c3c6804d7e7534e686b382dcf2efe2ccf58e2794f05b6e5eae99f5959f1044`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV NODE_VERSION=20.19.5
# Thu, 16 Oct 2025 10:35:31 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENV YARN_VERSION=1.22.22
# Thu, 16 Oct 2025 10:35:31 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 16 Oct 2025 10:35:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 16 Oct 2025 10:35:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:be7c8533c3f8dfcf5ab5c0fd76b47a568dc971c853834a20808defd1e88a5ffe`  
		Last Modified: Tue, 21 Oct 2025 00:27:58 GMT  
		Size: 49.4 MB (49351699 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9f518343ed4506c34ae7900f538c56bac66f4fad9740034ee8b819bd8d15e`  
		Last Modified: Tue, 21 Oct 2025 12:43:19 GMT  
		Size: 26.8 MB (26783314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efdb7d34d2ff189fa2150ed8d82914c7669f312817531bbe187965e9d30825d3`  
		Last Modified: Tue, 21 Oct 2025 23:25:03 GMT  
		Size: 68.6 MB (68630635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4131ad2e1cf6d0e51274c6e30ebc34015c8e72c5b79a0146220944b33c750ff`  
		Last Modified: Wed, 22 Oct 2025 12:46:56 GMT  
		Size: 206.5 MB (206460184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90554c8c6f24ae814310c9f2456405e67d3716b1cc314de626ecce0a76ba5cc3`  
		Last Modified: Wed, 22 Oct 2025 10:33:45 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8658761fbe89f424040d8276f7968ea84497857fc28c63497622898e20d38cfb`  
		Last Modified: Wed, 22 Oct 2025 10:42:39 GMT  
		Size: 48.2 MB (48218452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6714972f20bd4934378b412c2fa5dc461ab6db357b0b73cb63019e52b4c5a86e`  
		Last Modified: Wed, 22 Oct 2025 10:42:33 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0ab15a20c2678e761d48368615e0de903456623262bb9613e5d1ae00e13c4f8`  
		Last Modified: Wed, 22 Oct 2025 10:42:33 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-trixie` - unknown; unknown

```console
$ docker pull node@sha256:7ef59f8a2af36c3693154548bf8acfd9c058b3bb59f72213d124b30d4592c7c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17295453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaf95ab38893f84a753160f43a2ba4892a397d7308368500ca862e7b8628cd4c`

```dockerfile
```

-	Layers:
	-	`sha256:2b4edc2e29ba5e1dd771c2e9bcc9a31a61f2a60ddbf235a6951891c2275fddd5`  
		Last Modified: Wed, 22 Oct 2025 12:39:16 GMT  
		Size: 17.3 MB (17272690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71f070a91a42a1e646f412c9910772f85ab92232eda95570e39480e1cd14f376`  
		Last Modified: Wed, 22 Oct 2025 12:39:17 GMT  
		Size: 22.8 KB (22763 bytes)  
		MIME: application/vnd.in-toto+json
