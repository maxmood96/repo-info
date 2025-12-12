## `node:lts-bullseye`

```console
$ docker pull node@sha256:59e748fef2c6fa80641cd0e0b1a4e1c626ad49567e0290c3888b0dab3e6a50da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:lts-bullseye` - linux; amd64

```console
$ docker pull node@sha256:fa53c9365ba28bd0af6a278098828c72aa8b5690eaacbf3e0e5a9fefbf0781cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.7 MB (380674438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be659863fe28ffd6fdded7f4542fb36ad16059f99ddcece7273118e0f47847c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:07:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:05:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:43:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 19:36:08 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 11 Dec 2025 19:36:18 GMT
ENV NODE_VERSION=24.12.0
# Thu, 11 Dec 2025 19:36:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:36:18 GMT
ENV YARN_VERSION=1.22.22
# Thu, 11 Dec 2025 19:36:20 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:36:20 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 19:36:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 19:36:20 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:437b5b60e3a4b64e2c621589a67483eeef6d4b3fc4926655006ef41bd44f71dd`  
		Last Modified: Mon, 08 Dec 2025 22:16:49 GMT  
		Size: 53.8 MB (53756413 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:291bf09cec80aaf3d13eefc3fba3a6cb13a44cdce91da75e0e2c3d8b72348e79`  
		Last Modified: Mon, 08 Dec 2025 23:07:20 GMT  
		Size: 15.8 MB (15764219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17ff9cfdab33e1021de93428c7968b682c4bb6322df919b3c6622b8ac14ec0b`  
		Last Modified: Tue, 09 Dec 2025 00:06:29 GMT  
		Size: 54.8 MB (54755559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853b40334c538bcc5e2df110b0fecfb8423a3bbe5081982d24d096846277413`  
		Last Modified: Tue, 09 Dec 2025 01:40:24 GMT  
		Size: 197.2 MB (197205872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1111b2fc98c45147d1ad514986a60eadc8c049b4301b891d70daf6c4c7948a`  
		Last Modified: Thu, 11 Dec 2025 19:36:53 GMT  
		Size: 4.1 KB (4083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c45d7ca23bf03cf4d6523f058304912e33f789f2c5cf52f61bf466917e803c`  
		Last Modified: Thu, 11 Dec 2025 19:36:59 GMT  
		Size: 57.9 MB (57937174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44a76e3e1dfb17c32ee1d17370f8893964b61bac56809c3df4d6e77abb39174f`  
		Last Modified: Thu, 11 Dec 2025 19:36:53 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a20fdc85667ff13245d68cf93048e4cc07c707c36d187319dae7f6df0fcb2402`  
		Last Modified: Thu, 11 Dec 2025 19:36:53 GMT  
		Size: 444.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:b94ba3b89ed3c81475b879b30ffafdc472e38b25c63d37d65cc2372bb18c3a49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15773830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d33555e8c431c13ef81f48ae7aeb910c4694e6f449935df65adeb988ede0c229`

```dockerfile
```

-	Layers:
	-	`sha256:eb38df6dc7d35cbc8afb87b895a15259735f3c35467e5957243a2b73b24ee8b7`  
		Last Modified: Thu, 11 Dec 2025 22:40:17 GMT  
		Size: 15.8 MB (15750770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af1602cc07c9de2927aefe83cac3ad406943e7445a8668de38d858d824d17d0e`  
		Last Modified: Thu, 11 Dec 2025 22:40:18 GMT  
		Size: 23.1 KB (23060 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:a78e2ce975c7e9d2f118e073e991a881eb28291a85c845ebaaa8dff7116590ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.2 MB (372187843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55143e93d3b26d9d07d2bea95646ffaf090058bdd6327ec00a361b8d716e5cbf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Mon, 08 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1765152000'
# Mon, 08 Dec 2025 23:10:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 00:11:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Dec 2025 01:14:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Dec 2025 19:33:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 11 Dec 2025 19:33:29 GMT
ENV NODE_VERSION=24.12.0
# Thu, 11 Dec 2025 19:33:29 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:33:29 GMT
ENV YARN_VERSION=1.22.22
# Thu, 11 Dec 2025 19:33:31 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 11 Dec 2025 19:33:31 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 11 Dec 2025 19:33:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Dec 2025 19:33:31 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:24bca79f74a34f86894c8fcdc6ce8d7dc3c11dd0c76b7e9fa80c7c64df65d166`  
		Last Modified: Mon, 08 Dec 2025 22:16:57 GMT  
		Size: 52.3 MB (52257713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82b879966726dc963ee08cbddddb10287e93034fcf9e3ddf7a290b1b7e42538c`  
		Last Modified: Mon, 08 Dec 2025 23:10:44 GMT  
		Size: 15.7 MB (15749537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9cd25be3019ce9576369c1d01896d355c209a13773e0054363e0e12e57b0e1`  
		Last Modified: Tue, 09 Dec 2025 00:11:43 GMT  
		Size: 54.9 MB (54866122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8012df9f3f9ffe1b4b7749d91d60381788bf2363eb4b53d656bc467a3673fef5`  
		Last Modified: Tue, 09 Dec 2025 01:15:34 GMT  
		Size: 190.1 MB (190104139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2911ca838cf25728e3c53dffd1ff8854de6739ecf320872e81e85ed9133523`  
		Last Modified: Thu, 11 Dec 2025 19:34:07 GMT  
		Size: 4.1 KB (4089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c49b5271ef240dc8271d708595f4581a6a75c22e01939774023a48aec2c7566`  
		Last Modified: Thu, 11 Dec 2025 19:34:15 GMT  
		Size: 58.0 MB (57955124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92c7d0870c923e31385b6ffd0dae46840677506088892a0e4845bb1f0459eb1`  
		Last Modified: Thu, 11 Dec 2025 19:34:07 GMT  
		Size: 1.3 MB (1250672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81133bcc713d535279b061d89c52d6aed7066d62561c6aeeeda72a6924dcf6cd`  
		Last Modified: Thu, 11 Dec 2025 19:34:07 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:98673dd226dd473c2f806b03f5d147276800dbb0d8358f5763c304ff2d9db4d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15775957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3aa268bbbda2eb060271367c2552309f1d10445f83abde7c20824272ed9c4f`

```dockerfile
```

-	Layers:
	-	`sha256:4992a37a30ef25b72c2f5a3d6aa14968f5df8af64032b4bae382afaa6af16e0b`  
		Last Modified: Thu, 11 Dec 2025 22:40:33 GMT  
		Size: 15.8 MB (15752751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71609611819a016c04e9a55e540cf3f4a969fe704cf4b651a68a0197d702b869`  
		Last Modified: Thu, 11 Dec 2025 22:40:34 GMT  
		Size: 23.2 KB (23206 bytes)  
		MIME: application/vnd.in-toto+json
