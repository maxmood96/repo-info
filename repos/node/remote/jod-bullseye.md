## `node:jod-bullseye`

```console
$ docker pull node@sha256:bfa1b71d684deafe38f3d847e8a095ebbe18bd01445787a191c041f8cdad9ff1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:jod-bullseye` - linux; amd64

```console
$ docker pull node@sha256:df551a77877d6398c7feb20ce58f58faab402a903ebd356c8fef784bbb957557
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378471627 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8570af325fd0310a94257d4724c893c81bf6a1b29c373301166d2869757db136`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
ENV NODE_VERSION=22.15.0
# Wed, 23 Apr 2025 08:50:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 23 Apr 2025 08:50:54 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 08:50:54 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:19f1f54854d69811b3745bdd374e863f2fc2dc765fe37d1a30df3e590273322b`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 53.7 MB (53747740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ee1ef79bfdcd8777f441528bcffb7a16f7a3d0852661baef04456810160e792`  
		Last Modified: Mon, 28 Apr 2025 21:55:44 GMT  
		Size: 15.8 MB (15763544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68201ec6e5815a0906ce41187e7e52419a2d2c28d73d199e7612f268f81bbc35`  
		Last Modified: Mon, 28 Apr 2025 22:15:30 GMT  
		Size: 54.8 MB (54756006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3ee2c8b84461fce714721ac74cb275f6aaa0de67c2aeaccb8193af9ea8b4d38`  
		Last Modified: Mon, 28 Apr 2025 23:12:29 GMT  
		Size: 197.1 MB (197107708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4925eac7a2d86753c628e4c6762dfa6d97ab10eb1ae22a2aff14fa54b88fe90`  
		Last Modified: Tue, 29 Apr 2025 00:11:36 GMT  
		Size: 4.1 KB (4092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0dd53af777fe8b212a5594d91ef819603490237088a07be632b95ed9fa8604`  
		Last Modified: Tue, 29 Apr 2025 00:11:37 GMT  
		Size: 55.8 MB (55841414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19cf23b61bdfd7aef26ac8d8669edf6246ef49663ba1d683bd7f26c3a3007bc1`  
		Last Modified: Tue, 29 Apr 2025 00:11:36 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace91f5f20849daae1a498672f64fe1ac9cd56d7e415875f89e1f67614da645e`  
		Last Modified: Tue, 29 Apr 2025 00:11:36 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:jod-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:87104d75f8e54cdacabd7e7895d20a1bf687597c22156b423a2c5d9f0aa2573b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15402480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552de78b91ba0b10a4e9095a4799f38ba1beadee2b29bf7b7235518ac4c2d40f`

```dockerfile
```

-	Layers:
	-	`sha256:2183e8a2d73140ea97b2212c9ab9b9a64c21971ededace3b1f138d6b708b27fb`  
		Last Modified: Tue, 29 Apr 2025 00:11:36 GMT  
		Size: 15.4 MB (15379818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a9457d6c6a86644a14538f11263730d630e7b7b7073ecf10912c5aad06bbf2d`  
		Last Modified: Tue, 29 Apr 2025 00:11:36 GMT  
		Size: 22.7 KB (22662 bytes)  
		MIME: application/vnd.in-toto+json

### `node:jod-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:9bef3abcde9107da51a8d52bcfb335f52110049e433d9f84db1414335d3d59b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.2 MB (334172522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119b0f89126b672f749d7ecbb0d45bd9b89819b981753ff931fc8abe745467a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
ENV NODE_VERSION=22.15.0
# Wed, 23 Apr 2025 08:50:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 23 Apr 2025 08:50:54 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 08:50:54 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:8c2fc9e6d23f3debfa68416a2b96331b92d563b20272933315ecfbbada38e955`  
		Last Modified: Tue, 08 Apr 2025 00:23:35 GMT  
		Size: 49.0 MB (49031449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:525b68fed12d763a57f1b020aa1579673112de80a5b780b5ffaa045109c81f23`  
		Last Modified: Tue, 08 Apr 2025 07:38:26 GMT  
		Size: 14.9 MB (14878713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909681b45fdfcbd0bfebc28d96cd1bdab32fd85e3af6788b49d9cb80e8ff865a`  
		Last Modified: Tue, 08 Apr 2025 17:30:33 GMT  
		Size: 50.6 MB (50624452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ae4904ff46404ac5bb348da93b4e4f750b89ecaf468fd2f4b669038dc51cfb`  
		Last Modified: Tue, 08 Apr 2025 20:36:13 GMT  
		Size: 167.6 MB (167560460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d6e3269fce3278e34ec654aeb2ad7eb6f2bd134002d86e6877c3f2bda4d2e6e`  
		Last Modified: Wed, 09 Apr 2025 01:00:19 GMT  
		Size: 4.1 KB (4079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e36534cc868a4184aee1408e472199f14fe231f23160f2c5d14ae803b45bb3`  
		Last Modified: Wed, 23 Apr 2025 17:00:26 GMT  
		Size: 50.8 MB (50822245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3310754da2c289d835b1f4639da2f6e72cd114877b5a9a81bd0258b8cf0283d`  
		Last Modified: Wed, 23 Apr 2025 17:00:24 GMT  
		Size: 1.3 MB (1250676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93c84dc8e3a9988e511ca0228403f9f0aa8dd4951af4621a3e2d4a18ac2917c`  
		Last Modified: Wed, 23 Apr 2025 17:00:24 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:jod-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:7ddbcaed1a81d6cba4d5f00e6c09af0cfe9270617e6e36280cc169e3f3a21bcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15203326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:259e5e47575fcfef24cc9b5585657a4dc26b1a7a02ee58706c01240c8f508141`

```dockerfile
```

-	Layers:
	-	`sha256:e55b6c681693f5e8002a5f4498e95be0d4d6ebea9ca686294f67b1f32cd1e130`  
		Last Modified: Wed, 23 Apr 2025 17:00:24 GMT  
		Size: 15.2 MB (15180553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2350f16e99cd0e0df0f7e1ba00821f14a81ff0e07bdc534a712c9490ca0ff7d`  
		Last Modified: Wed, 23 Apr 2025 17:00:23 GMT  
		Size: 22.8 KB (22773 bytes)  
		MIME: application/vnd.in-toto+json

### `node:jod-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:0951d4b782231162d7b3b046eeb7ba1b28c5fe5306ed24563da82d20817c116e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.6 MB (369635032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:051c1c288d0637063a86e8d9d86a7fb97a9a0fc9b31eff1164ec0dd4da0fc440`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
ENV NODE_VERSION=22.15.0
# Wed, 23 Apr 2025 08:50:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     C0D6248439F1D5604AAFFB4021D900FFDB233756     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
ENV YARN_VERSION=1.22.22
# Wed, 23 Apr 2025 08:50:54 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 23 Apr 2025 08:50:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 23 Apr 2025 08:50:54 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848ef88a118038c35ad53e6bc0e94192e99b916044a11fb61a40b31c77edc820`  
		Last Modified: Tue, 08 Apr 2025 15:54:19 GMT  
		Size: 190.0 MB (190022174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:225a04138092b0531561514f97b70b0989b28bed64fd04ff1a2ab9e1c01ee806`  
		Last Modified: Tue, 22 Apr 2025 18:02:42 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59551900da23ff0d4b41c2146aab397588faad009ae144cd37b957a7a1fd5f12`  
		Last Modified: Wed, 23 Apr 2025 15:38:52 GMT  
		Size: 55.5 MB (55504316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066a686e8a57da205b496fcf3133ea4b3742946181c66558546d5020b891edbe`  
		Last Modified: Wed, 23 Apr 2025 15:38:50 GMT  
		Size: 1.3 MB (1250676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373b21b3406b3cb47d7ff42daeec5b55a5ea43e8a40724b3ba8d700fe4d6f915`  
		Last Modified: Wed, 23 Apr 2025 15:38:50 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:jod-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:b4abf4a419846655405f9e62031465ab5313cf4ae062bf70878a78a016192f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15404843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed43ddf5c840151da4d374e779ad3041dc0a6c7c817729d8a24adba7df5c0451`

```dockerfile
```

-	Layers:
	-	`sha256:0b5e317eaad10fe5b3170d0f0b1281f6f36097ef8359a3a6203e9588163b6250`  
		Last Modified: Wed, 23 Apr 2025 15:38:50 GMT  
		Size: 15.4 MB (15382034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e240210a9966a9a50f786dfeb58dce7652a7ab523cae6b2a14961ee744055d`  
		Last Modified: Wed, 23 Apr 2025 15:38:50 GMT  
		Size: 22.8 KB (22809 bytes)  
		MIME: application/vnd.in-toto+json
