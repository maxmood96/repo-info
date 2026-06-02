## `node:current-bookworm`

```console
$ docker pull node@sha256:076dd90a458a4baf8b8d2716f022a2c8db245dbe70c7de38bacad1708258eeab
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

### `node:current-bookworm` - linux; amd64

```console
$ docker pull node@sha256:178c8ecf89dcd8db1270bf57c03fe7ca70c061bb3929f2f091ef17d2ee1f69f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.7 MB (411679487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04c7b53faf65efe9fa1841396e1c2197a10d3275f11bdb767e8ec4af4fa0648`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:23:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jun 2026 22:46:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:18 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:18 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:4887723d153cfd7fd9e356c8730311c36a64e4f9329f9d3ae1929e05715f2e73`  
		Last Modified: Tue, 19 May 2026 22:36:12 GMT  
		Size: 48.5 MB (48495432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e51c50554dce9c9549d76c40bfea45780a8342aea81ba8b270ba1bf46a2aec5`  
		Last Modified: Tue, 19 May 2026 23:23:20 GMT  
		Size: 24.0 MB (24043374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a234579dfb0d2a4c7e869bc6c39c06f306aa019f90ec3e79f682671badaeb4f3`  
		Last Modified: Wed, 20 May 2026 00:26:20 GMT  
		Size: 64.4 MB (64404451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce041001b8968f31ff00bb8f9dbd68f72d4bdc378a1309e38eb3dfe97cc1498`  
		Last Modified: Wed, 20 May 2026 01:15:50 GMT  
		Size: 211.6 MB (211586305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:740ad48dac87fe2097b8c8ff5ca25eb576d7e8b1863f4a90021f6a965ec16e0a`  
		Last Modified: Mon, 01 Jun 2026 22:46:42 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96daae20653acccabe1aa8d1f52f3978890cc75acfd00d61a3129597368136ce`  
		Last Modified: Mon, 01 Jun 2026 22:46:45 GMT  
		Size: 63.1 MB (63146154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1bdaa40f17bb2cf77b179dd2035bc5c2cf6fba60efe82333a09aa0e7504c2b7`  
		Last Modified: Mon, 01 Jun 2026 22:46:42 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:88ea7a9e389ceaa5620e97d1d230cf1446c3a801a80bfe86a77d05d14205fb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16092402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c29b28da5a86c4f5d26d67e3b14daf599b85dce8fcc966e297e83c92e1a2c1e`

```dockerfile
```

-	Layers:
	-	`sha256:e6c5ed5103c3eee4a4e15771a121d23b24feae85385c4e5c5419119119905f6e`  
		Last Modified: Mon, 01 Jun 2026 22:46:43 GMT  
		Size: 16.1 MB (16074873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fbf41fee7d1eff97ce5c824732f8f1c19cb75d7270958cc5ddd5e8e1deddfeb`  
		Last Modified: Mon, 01 Jun 2026 22:46:42 GMT  
		Size: 17.5 KB (17529 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:979f77122c557c3dc525f16de7df5bddf5784a9fd41ffbbf39692c2bcc997a5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **402.9 MB (402926512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb0d3127b2a685d724b9af15c3c84cefbac4e87b2eb30f530a86d07926e93822`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:26:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 01:15:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jun 2026 22:46:53 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:47:03 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:47:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:47:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:47:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:47:03 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:1fbcdab7270278c1f989ae72190255d85d2117e990efb76cde6eb206b803672c`  
		Last Modified: Tue, 19 May 2026 22:36:02 GMT  
		Size: 48.4 MB (48379432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3daebbc198bd7b84bdd72840d7f4ded251896f03b9a9f880894e95e926bc543`  
		Last Modified: Tue, 19 May 2026 23:26:38 GMT  
		Size: 23.6 MB (23613394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35c669ec0346d48159cb837d6257098593cd53e61de677d9c0426474d36e1c5e`  
		Last Modified: Wed, 20 May 2026 00:27:16 GMT  
		Size: 64.5 MB (64487655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03874872dc6df1c0caacf1eaa4544f492fcb08bd68a885b9b784f5e9be1d6e6`  
		Last Modified: Wed, 20 May 2026 01:15:57 GMT  
		Size: 203.1 MB (203108347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ef36dd1f2e0550c46307eb6216a17dea8058de1a4d9576840892fc8396aae80`  
		Last Modified: Mon, 01 Jun 2026 22:47:32 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b441b632b218ed1c7c38976169b34f615755d1ece53be66cd4b80a363b9d514`  
		Last Modified: Mon, 01 Jun 2026 22:47:34 GMT  
		Size: 63.3 MB (63333911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be5e803aa19a1a8c60add4ba4fe385f6ef53d39dca88169bca3da57628a2f629`  
		Last Modified: Mon, 01 Jun 2026 22:47:32 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:e47aef77f8e6e8fdafd9f39bd117abee6687c04bffad1a60fe3dee3b04d3f49a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16121073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:722f66fc1ae7fa097773f213a38b58c8682b8d1de71231a0000a78d271db91d2`

```dockerfile
```

-	Layers:
	-	`sha256:51546af35ae323141684efd0e78cb811cf7dae3a8ef73ea5a054d7b19408d01b`  
		Last Modified: Mon, 01 Jun 2026 22:47:33 GMT  
		Size: 16.1 MB (16103411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd0e280cc4eb6f0e85bc69fba76ba7713551649ea21703ac4ac451f1de98e270`  
		Last Modified: Mon, 01 Jun 2026 22:47:32 GMT  
		Size: 17.7 KB (17662 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:ba49e25ad7e6951753f4a66d3786cf3ef4488f2516b720c4a5399a29ccae0ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.0 MB (427962832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21b4476b36bb537b737eb0dcaaf0eb44fb3698b8336b741b2d709f5577de3cc5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 01:13:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 06:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 09:06:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jun 2026 22:45:49 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:04 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:04 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:04 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:04 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:b3943e183051423c3dc79fa53ad6d50fff9621945bbfc636eec039b14ead2b66`  
		Last Modified: Tue, 19 May 2026 22:35:10 GMT  
		Size: 52.3 MB (52340199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f46c910cb3dd366a8b080c77b15459d7465da54412b3570454cddcaf0cdf40`  
		Last Modified: Wed, 20 May 2026 01:13:39 GMT  
		Size: 25.7 MB (25686466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67cb71cd5984ee53ab56bef57a29d3b0ef6e8939c352146b1efe66402d4c7ff`  
		Last Modified: Wed, 20 May 2026 06:51:27 GMT  
		Size: 69.9 MB (69853485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f372df3d76a6b5b287650eecc7c27316f949d95187b1436e85093ce3107c45`  
		Last Modified: Wed, 20 May 2026 09:07:42 GMT  
		Size: 214.6 MB (214640794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eae4ca0383a9e5d1caa42510fde787235a970b66bf21e81b3a5128b2a87fc03`  
		Last Modified: Mon, 01 Jun 2026 22:47:26 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:638878e4bf6ea66907bb663c937b4e9fd473f01c02b1a16399aefd1f5c92bed0`  
		Last Modified: Mon, 01 Jun 2026 22:47:28 GMT  
		Size: 65.4 MB (65438110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f324d402658cf06f6adb09190f4663dcc3839f5cc49b6ad72297da13fdfdfb45`  
		Last Modified: Mon, 01 Jun 2026 22:47:26 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:e6aec786253e6eea8255975ecdb43fef40c0e456bbc6198c2c8325debc21744e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16068977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb94a248454b105ace7583f0054f87e2ee46bc034a0b5ed7eba51220284ba0c0`

```dockerfile
```

-	Layers:
	-	`sha256:155e28afe8362d63583093fba0aa52eab9b96d2bb63e6775c9ad8fad02e2bac4`  
		Last Modified: Mon, 01 Jun 2026 22:47:27 GMT  
		Size: 16.1 MB (16051394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d8049b93e83d6076dac08f78a8be80bec471616dc80b28109ab457ec40ebeae`  
		Last Modified: Mon, 01 Jun 2026 22:47:26 GMT  
		Size: 17.6 KB (17583 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bookworm` - linux; s390x

```console
$ docker pull node@sha256:75a9f5d54701f7fb5294bbd3e53efd0da5e4f3c75213509ffdb7733582695847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.0 MB (382953486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed8db55ec1a98f3e8f0a435c0bcc9bf7cfed5018daa1c58d2fa17ce7f3f87eef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:17:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:05:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:44:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 01 Jun 2026 22:45:55 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Mon, 01 Jun 2026 22:46:03 GMT
ENV NODE_VERSION=26.3.0
# Mon, 01 Jun 2026 22:46:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Mon, 01 Jun 2026 22:46:03 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 01 Jun 2026 22:46:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Jun 2026 22:46:03 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:e0fc2c7a6bb12f7a9b333cc117b6ea5fa5cf251c5fa4dd298303beee01028f59`  
		Last Modified: Tue, 19 May 2026 22:35:39 GMT  
		Size: 47.2 MB (47155589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d79feab17202415ba0b431eca0e903b1c895e662e755c4c9f1b5678ad8eb605f`  
		Last Modified: Wed, 20 May 2026 00:18:12 GMT  
		Size: 24.0 MB (24039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:511ade0407a6db3c4a6853a735563e5fb22577aaaa32942a9458cc0c09942583`  
		Last Modified: Wed, 20 May 2026 02:05:37 GMT  
		Size: 63.5 MB (63498321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaa6dc17afbecf60ca3315d2c4ad18f3028bcf8091ccde763daf04c218092a7`  
		Last Modified: Wed, 20 May 2026 02:45:53 GMT  
		Size: 183.6 MB (183603631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1266fd2a9cd3f2f86002d5db17d18819bc63e84287df4f0aefbeeef7f55ef6d1`  
		Last Modified: Mon, 01 Jun 2026 22:46:46 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d446677a3b845f7a2eb38371f97255c5311d796f53e149f938ab1fa2f7b75e0`  
		Last Modified: Mon, 01 Jun 2026 22:46:47 GMT  
		Size: 64.7 MB (64652976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6926d27b5f597d82566fc8b23294a575ce7fdf008e451bbe72da36502a37388`  
		Last Modified: Mon, 01 Jun 2026 22:46:46 GMT  
		Size: 441.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:d7ae154d26ef7ea907a74542d15ae1b21f8926f34f908392ce880a1dd9fdd217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15900002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ca235f205e2b53bfd1c277fadd1caa037d0be8b2d1c8bb7ebe78b6e8a448dc4`

```dockerfile
```

-	Layers:
	-	`sha256:b35a2852855b1ae0d414dd7a26887d51faa201fce51c276e8142958d3fdd95ca`  
		Last Modified: Mon, 01 Jun 2026 22:46:46 GMT  
		Size: 15.9 MB (15882471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba004a7b798c6ec777da2ee2127a2cdf25e5489f87dc5cc0678cf82811d9695`  
		Last Modified: Mon, 01 Jun 2026 22:46:46 GMT  
		Size: 17.5 KB (17531 bytes)  
		MIME: application/vnd.in-toto+json
