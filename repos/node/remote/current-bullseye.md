## `node:current-bullseye`

```console
$ docker pull node@sha256:8927f17be39632ee340d798cc17a8a2257273a01b1865fd0f9970d029f2983d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:current-bullseye` - linux; amd64

```console
$ docker pull node@sha256:14671502e8e7b000cd644c1ad56934bab4a82077457af6461d084fd5d0e85c05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.2 MB (383191688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1530df750f188aa0f514c6e464d2a27177a1c0059511a3cf347e919ece3e0082`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1757289600'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV NODE_VERSION=24.7.0
# Wed, 27 Aug 2025 23:04:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 27 Aug 2025 23:04:59 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Aug 2025 23:04:59 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:035115815e46101f9c9956e02e706f2f3ec8748e2b415f0d232b51eb76a6a779`  
		Last Modified: Mon, 08 Sep 2025 21:12:56 GMT  
		Size: 53.8 MB (53755396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebbe40dd6978ce6b51e9d84d91a658eb2959635aec29cb2475587fda81e28d1`  
		Last Modified: Mon, 08 Sep 2025 21:54:22 GMT  
		Size: 15.8 MB (15765345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b969d43370836ef53860df2c53e721ccfdd06653f3db3f7100570314bf509d12`  
		Last Modified: Mon, 08 Sep 2025 22:13:40 GMT  
		Size: 54.8 MB (54757246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c6412c7204557d8c521d4b9da4c0a744f9cd8038936537301a90b9395815640`  
		Last Modified: Mon, 08 Sep 2025 22:39:07 GMT  
		Size: 197.1 MB (197146531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eee0f6015fc6750a83d21264d4ac3b41231ce0a8a40af8038a2aa631582fc59d`  
		Last Modified: Mon, 08 Sep 2025 23:21:28 GMT  
		Size: 4.1 KB (4081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8292bf50b845b1710fb5b715db4651176643c2976e6bcbc91b469d521813af3`  
		Last Modified: Tue, 09 Sep 2025 00:42:44 GMT  
		Size: 60.5 MB (60511967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9e2aa48c9d081c735ad2e96671c4a27419f98f0ca94a96d841a7ea7c76a743c`  
		Last Modified: Mon, 08 Sep 2025 23:21:33 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16bd69439e5d699175f57cf565eb39d70e00209850ead34003a64eb1c12ccc6b`  
		Last Modified: Mon, 08 Sep 2025 23:21:39 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:7c192361489c0c030671683f6cc8c80acbc104e8f52ddaac4304ee3acef7f4f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15782807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d6e34faec84bb378e0dd76ca46dd739f105dd6271b86732eaf0134f936812bf`

```dockerfile
```

-	Layers:
	-	`sha256:9f64495a738a9bcacd12d54669e99dd4259473d9041438c15e8f23a4f24b9c0f`  
		Last Modified: Tue, 09 Sep 2025 00:42:04 GMT  
		Size: 15.8 MB (15759718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43fb4514a85855537a005a501b4ec2e52d33aa686bb4e7aec6480fe33dc8f541`  
		Last Modified: Tue, 09 Sep 2025 00:42:05 GMT  
		Size: 23.1 KB (23089 bytes)  
		MIME: application/vnd.in-toto+json

### `node:current-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:dc3c26257966469dd62a76e93e1aa6016e050984f2facd6cd91663f9d49f482b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374613991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21fb6afc105ce03494f16955c24f8e3be998eaa77d67c59d38c2e29b1c449e94`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1754870400'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV NODE_VERSION=24.7.0
# Wed, 27 Aug 2025 23:04:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENV YARN_VERSION=1.22.22
# Wed, 27 Aug 2025 23:04:59 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 27 Aug 2025 23:04:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 27 Aug 2025 23:04:59 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:7b68ea47bc3cd8615e51fdbe0976cb4999ba56ce8764e755543a4521d69a32f6`  
		Last Modified: Tue, 12 Aug 2025 22:08:57 GMT  
		Size: 52.2 MB (52248409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25635cbca821869ea9220087d35fa6b59e758fb2dca635f36530cb5e44b7c481`  
		Last Modified: Wed, 13 Aug 2025 07:20:06 GMT  
		Size: 15.8 MB (15750676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06836ab0250fb74efa819c381a3a62f540817c74a1d0468d4e03f53c6b03758a`  
		Last Modified: Wed, 13 Aug 2025 15:28:22 GMT  
		Size: 54.9 MB (54856134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3d454c8e58c4069692ce41e243c84f24682d348d8667ce5764628f03111249d`  
		Last Modified: Thu, 14 Aug 2025 00:15:27 GMT  
		Size: 190.1 MB (190058369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de5dbb89028d4a2e9976f66d06c61b5bd180be744020263cbbeed0ddc541ea8`  
		Last Modified: Thu, 28 Aug 2025 15:33:59 GMT  
		Size: 4.1 KB (4097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b237ec56e362ff20a86eea8692cd704b30eae4a5db2f2f18c4e91d22662513f3`  
		Last Modified: Thu, 28 Aug 2025 15:50:30 GMT  
		Size: 60.4 MB (60445179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:965f4158c369143af0307820f9a193e2f2995cd0a168fb35388112514eb64658`  
		Last Modified: Thu, 28 Aug 2025 15:34:00 GMT  
		Size: 1.3 MB (1250679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200e9f8e3948792583b508d21891f6b1b439a0852b914f23b5ef48d5eb1fea7f`  
		Last Modified: Thu, 28 Aug 2025 15:33:59 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:current-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:a542805d08bce4a60ed6a4f30ce328da2d9390551c0f26c8445778892dfa9f11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15784934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3730e643fe0efa44a8eaf06425849f4c5dbe8e41d8729d8fa49ab00008accb`

```dockerfile
```

-	Layers:
	-	`sha256:1b8b427d125fb4304b31728e3264a262467f0f67723bf5592c6e4ed7d78eb086`  
		Last Modified: Thu, 28 Aug 2025 15:40:36 GMT  
		Size: 15.8 MB (15761699 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a248b24a2ae41aab8bb6f8dbc3fe3c3d632d263e7c3d7c3d06ca75adcab9a0c`  
		Last Modified: Thu, 28 Aug 2025 15:40:37 GMT  
		Size: 23.2 KB (23235 bytes)  
		MIME: application/vnd.in-toto+json
