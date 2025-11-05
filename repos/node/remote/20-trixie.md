## `node:20-trixie`

```console
$ docker pull node@sha256:35a8e5af66bc628e5d7da6843dadc5bf44399d897547f7088bb60496cfed9930
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
$ docker pull node@sha256:bbfcee2543398d6548ca46044623470968844e4f1bc1b339ac919b1a88a738a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **436.4 MB (436389176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15d80bab9b6db54e72b3c884cecaaca05cd4b86c78dde0f7d731e2cc84c52141`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 06:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 16:02:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 20:53:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 05 Nov 2025 05:36:40 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 05 Nov 2025 05:42:04 GMT
ENV NODE_VERSION=20.19.5
# Wed, 05 Nov 2025 05:42:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 05 Nov 2025 05:42:04 GMT
ENV YARN_VERSION=1.22.22
# Wed, 05 Nov 2025 05:42:07 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 05 Nov 2025 05:42:07 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 05:42:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 05:42:07 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:3c335bb15935da0eae5ce30111cfa6a289c813162bada9fd389d8ae5510d5d66`  
		Last Modified: Tue, 04 Nov 2025 00:20:22 GMT  
		Size: 53.1 MB (53110127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c598502b2d4d7d278f56bfb7b6960ccd64d116b7bc7b02516bad5cdad4a631`  
		Last Modified: Tue, 04 Nov 2025 06:28:57 GMT  
		Size: 27.0 MB (26996633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fbe8662034d4013b7fae91328f939dfb669ce78f36e4a91a9a0c68675f61828`  
		Last Modified: Tue, 04 Nov 2025 16:03:22 GMT  
		Size: 73.0 MB (73035332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c20ef82941d48d9739dd464559bc277a122b8fd20002e75ffb6f6a2fb6ca09`  
		Last Modified: Wed, 05 Nov 2025 00:18:10 GMT  
		Size: 231.1 MB (231095465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab42c8de2f562b8f5a9d331fe80f9568fa4a22ec68b41ee9e7deb4fdb5dda457`  
		Last Modified: Wed, 05 Nov 2025 05:38:10 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:056e7388cfdbc9789a364ff852bdd7c860e6c65f4145f2dd21de0e41e15a9af0`  
		Last Modified: Wed, 05 Nov 2025 05:43:26 GMT  
		Size: 50.9 MB (50897179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3f268e080d0ba3f41501ca6f3b536c7949c5886b817117c27b66bfb498d79dc`  
		Last Modified: Wed, 05 Nov 2025 05:43:17 GMT  
		Size: 1.3 MB (1250669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451e77cb5899c14ac72110ae5c22ab502d73f150678008d1e81b165c05b2e744`  
		Last Modified: Wed, 05 Nov 2025 05:43:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-trixie` - unknown; unknown

```console
$ docker pull node@sha256:696363bea2a56f76c9863c7430451954e57af8fa55a2ea79f1b5d0326887dc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.5 MB (17503779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d3d552e86cac5cf386dd9e1c91e64ce01819aed07158af17960512b251e50cd`

```dockerfile
```

-	Layers:
	-	`sha256:3f372d48ac48c8beb35c4e5692f797cce15d9bfd2983412383be6dda16c7d03c`  
		Last Modified: Wed, 05 Nov 2025 07:38:59 GMT  
		Size: 17.5 MB (17481012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:745401173ef8e377c1c77b441a2ef274891afe32e2d6d8578c4850bd116019ae`  
		Last Modified: Wed, 05 Nov 2025 07:39:00 GMT  
		Size: 22.8 KB (22767 bytes)  
		MIME: application/vnd.in-toto+json

### `node:20-trixie` - linux; s390x

```console
$ docker pull node@sha256:210eabe8844667d73529aebdcd09fd80ebbae04d9ff8809633349bc0f535c22e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.7 MB (400697664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64dff7eff68d4db0ad77de22f93696292e4207a8c297ac2a5198ca6927b94448`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 10:03:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:52:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 17:30:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
# Wed, 05 Nov 2025 02:19:22 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 05 Nov 2025 02:28:53 GMT
ENV NODE_VERSION=20.19.5
# Wed, 05 Nov 2025 02:28:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 05 Nov 2025 02:28:53 GMT
ENV YARN_VERSION=1.22.22
# Wed, 05 Nov 2025 02:28:57 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 05 Nov 2025 02:28:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 05 Nov 2025 02:28:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 05 Nov 2025 02:28:57 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:48bd359f940d437208e8579c571291503fa327e04a66a6c8d918cfe93cae2e1e`  
		Last Modified: Tue, 04 Nov 2025 00:19:45 GMT  
		Size: 49.4 MB (49352299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205358f383faecf1c434c76ac887bd7a626ec58dd373ab479cce2de6c6d63849`  
		Last Modified: Tue, 04 Nov 2025 10:04:16 GMT  
		Size: 26.8 MB (26783618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207e263d619c54c23185f97b8200ca156bd013604c1f55c66784ca7069ae48ff`  
		Last Modified: Tue, 04 Nov 2025 14:53:19 GMT  
		Size: 68.6 MB (68638436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef0634d2aa9f89c6fe5db66904261bec1da301aa6c1cde54b9c465265b676459`  
		Last Modified: Tue, 04 Nov 2025 20:25:30 GMT  
		Size: 206.5 MB (206450371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd7181e254e934889faba17c43380817c407922e28b255d63f485d072b06226`  
		Last Modified: Wed, 05 Nov 2025 02:21:34 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53066fa35cd748839ebd7de86ff42e789ea3bf6e14b6ebf1f73e60d07c7d03f`  
		Last Modified: Wed, 05 Nov 2025 02:30:54 GMT  
		Size: 48.2 MB (48218480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e55adc69fd0111f25cfccdde5067d56ce300eed33ac5b48b699ec3e750e7dcdf`  
		Last Modified: Wed, 05 Nov 2025 02:30:44 GMT  
		Size: 1.3 MB (1250678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88fa1c3169895629c1d7675c419d5ac53f4a174ce63520d02c10df8feaecf715`  
		Last Modified: Wed, 05 Nov 2025 02:30:43 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:20-trixie` - unknown; unknown

```console
$ docker pull node@sha256:d6bfea82928c5ce376b9e0140c4b9638c57a2f406b014c325d56817c5cfd98d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17295410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31afbfe88791adc681fd77f92532a512d2b3f6e8009943c86eea855d0843a393`

```dockerfile
```

-	Layers:
	-	`sha256:f51c28a8b8df1730c20561f24a74dc2b9f9e2cd48353cd5d99c87614d01f5ea6`  
		Last Modified: Wed, 05 Nov 2025 04:39:04 GMT  
		Size: 17.3 MB (17272690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42467980e634e95a6bb91f1d010ff172485f01acda7d8b12d3c8a05280642c67`  
		Last Modified: Wed, 05 Nov 2025 04:39:05 GMT  
		Size: 22.7 KB (22720 bytes)  
		MIME: application/vnd.in-toto+json
