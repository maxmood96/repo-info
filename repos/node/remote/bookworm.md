## `node:bookworm`

```console
$ docker pull node@sha256:c69f4e0640e5b065f2694579793e4309f1e0e49868b0f2fea29c44d9c0dc2caf
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

### `node:bookworm` - linux; amd64

```console
$ docker pull node@sha256:0c07e208ee94a97ffc2c452223b8577401ae1343efeafffcd6181351644d8d59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.5 MB (407489608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c42ab2c9553027da22a77a84c84395c756d286ec0296271c42233e8d670c984`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 05:00:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:12:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 06:12:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 07:16:25 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 22 Apr 2026 07:16:35 GMT
ENV NODE_VERSION=25.9.0
# Wed, 22 Apr 2026 07:16:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 07:16:35 GMT
ENV YARN_VERSION=1.22.22
# Wed, 22 Apr 2026 07:16:38 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 07:16:38 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 07:16:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 07:16:38 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:db53381ee51f9e43304e236099ba097ae1b33ae41a8007e0b6319992eb55fd00`  
		Last Modified: Wed, 22 Apr 2026 00:15:45 GMT  
		Size: 48.5 MB (48488628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5203b2bfeff92b72e816dc6cbb1f16856f0cd592e521e3c0cfa195a78fe180e`  
		Last Modified: Wed, 22 Apr 2026 05:01:15 GMT  
		Size: 24.0 MB (24042234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcda2b4d7993820b00c5488d173051e76d01ba6b85620617ba77001b0f9e2fa`  
		Last Modified: Wed, 22 Apr 2026 05:12:28 GMT  
		Size: 64.4 MB (64396988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2933ecab0f11302fd71f29aa83ad2904683246f7a8320ad0dc3a60b23f05fee9`  
		Last Modified: Wed, 22 Apr 2026 06:13:02 GMT  
		Size: 211.5 MB (211545979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35e2f0c813f89570d372c7d24a687cc7077640075ac7d98ec539cac4fa70327`  
		Last Modified: Wed, 22 Apr 2026 07:17:04 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9cba84649822e0db9bfe24ed54d0daea76ed81772cf1e58c4974d40efd2fd9c`  
		Last Modified: Wed, 22 Apr 2026 07:17:06 GMT  
		Size: 57.8 MB (57761344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b546b5153551e7fbc693e25cbaeba6aede1f260fc78cb6bcd38c7d1fc65173f8`  
		Last Modified: Wed, 22 Apr 2026 07:17:04 GMT  
		Size: 1.3 MB (1250667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e801f5f17a5446c897a2cc921d2308364abf89258501979ac14b2e24e52e63c`  
		Last Modified: Wed, 22 Apr 2026 07:17:04 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:bcac20bf4b6faf9881ea382bfb23c7efe40768eb29e4d516125a3b278331b073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16103812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbfaab306660b3f1d1f00dd6f4304370a69d38d227f68dd6ad74a04e5cf1f54`

```dockerfile
```

-	Layers:
	-	`sha256:24d79c4afb63dd1843fc4e373c2cb63ea29c8543f61257603c94b00a761494b1`  
		Last Modified: Wed, 22 Apr 2026 07:17:05 GMT  
		Size: 16.1 MB (16079306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:450a8e39d54d4f8eb143308cb8956d84039726e99d08a75dd43362db227551f3`  
		Last Modified: Wed, 22 Apr 2026 07:17:04 GMT  
		Size: 24.5 KB (24506 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:3712a33f5ca4f987d4ffc600f5a26e44aeae40381a754db0d90fd454b7358084
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 MB (398839136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:120c92b70f56e94a4196aab219427a218da0884b3636cd356fe81f16912bf940`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 01:42:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 02:32:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 03:16:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:19:41 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 22 Apr 2026 04:19:51 GMT
ENV NODE_VERSION=25.9.0
# Wed, 22 Apr 2026 04:19:51 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 04:19:51 GMT
ENV YARN_VERSION=1.22.22
# Wed, 22 Apr 2026 04:19:54 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 04:19:54 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 04:19:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 04:19:54 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:30de66f8fdafab67e88d876087f571a693a1a6c4cf0abc29efbf88ea878e0d29`  
		Last Modified: Wed, 22 Apr 2026 00:15:43 GMT  
		Size: 48.4 MB (48373071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb7bd28fbdfe678a7f45878b7b1c07dbbc0fa7753b0312aa8fd049667a9e137`  
		Last Modified: Wed, 22 Apr 2026 01:43:06 GMT  
		Size: 23.6 MB (23609423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599d07e8492bcee46202f5eae3e3010a470acc5139840e6d14556aefa3fc355f`  
		Last Modified: Wed, 22 Apr 2026 02:32:24 GMT  
		Size: 64.5 MB (64479606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f77b2a79d553481e7f962631ac14425d8c654928f18cdc3d1f265ceb460486e`  
		Last Modified: Wed, 22 Apr 2026 03:17:17 GMT  
		Size: 203.1 MB (203064331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcaa21912f6415854d6771d633aa205e413bd6d1f102c5f67274df5f2eed170`  
		Last Modified: Wed, 22 Apr 2026 04:20:21 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52d2437844155c861a64f6b77148739ec5e9ab2614b3beca9a9467e2471d5baa`  
		Last Modified: Wed, 22 Apr 2026 04:20:23 GMT  
		Size: 58.1 MB (58058265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b99db72b90d90716755d39bf29c944c9f85f59ad0db775c89e54d4d75fa355c`  
		Last Modified: Wed, 22 Apr 2026 04:20:22 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:150ed351d8307f93560ff2c7e8e525328b9b4ac07959df23ca19fdda6c626135`  
		Last Modified: Wed, 22 Apr 2026 04:20:21 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:b4aa7da4bf8c10a42d6ec2d04a4a9c108fd172f597de0f4af421215a0fe3c3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16132615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca72dfd1a42c1ff580baed13fc46aca7e12c95d876ad2880b390e97ad0e9f51`

```dockerfile
```

-	Layers:
	-	`sha256:9682b84bee9071b375de6d6e3abca2459029790625253cad926d4428d514a8ca`  
		Last Modified: Wed, 22 Apr 2026 04:20:22 GMT  
		Size: 16.1 MB (16107904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf67cb274d74663070f01acd18b880f4ece90cff8698c4bf75c0d9d5387a6e6c`  
		Last Modified: Wed, 22 Apr 2026 04:20:21 GMT  
		Size: 24.7 KB (24711 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:56d92e090a5610957562ea846052e51dc8d9093171140bc28d281e306acb4cb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.5 MB (423526572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81c5488bee88f4476c6fd07961dee4e6ce2cc144481efb9dac7bfd5b9afe9759`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 03:38:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 09:36:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 12:12:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 16:21:50 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 22 Apr 2026 16:22:10 GMT
ENV NODE_VERSION=25.9.0
# Wed, 22 Apr 2026 16:22:10 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 16:22:10 GMT
ENV YARN_VERSION=1.22.22
# Wed, 22 Apr 2026 16:22:18 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 16:22:18 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 16:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 16:22:18 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:0b84f035435acf0ec33df4748d96fad1243fd6b0ea9917f29eaa507d4c458365`  
		Last Modified: Wed, 22 Apr 2026 00:15:04 GMT  
		Size: 52.3 MB (52336735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c150273f4a5b502fcc97d9a922e79c7bc7d5035fb9eb1142f5adfbcea709a1`  
		Last Modified: Wed, 22 Apr 2026 03:39:23 GMT  
		Size: 25.7 MB (25679369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5543a629afcc86e06f307e20d98c8cdd9f2490908cdef00122fb2daf671594`  
		Last Modified: Wed, 22 Apr 2026 09:37:35 GMT  
		Size: 69.8 MB (69846406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77407553cbcc2d4c713e5cabfdcef2048c44ae73e83fb9a96fe610844a4ae05f`  
		Last Modified: Wed, 22 Apr 2026 12:14:13 GMT  
		Size: 214.6 MB (214607471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de360c10e96997f22ca2526c5a5afe3d196c901a2f2a4745f211ba02406a3923`  
		Last Modified: Wed, 22 Apr 2026 16:23:17 GMT  
		Size: 3.3 KB (3318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edc4b38863a83d103d0ad8c5d2a520099b5ada78ddc7a4499491dfe95181f55`  
		Last Modified: Wed, 22 Apr 2026 16:23:20 GMT  
		Size: 59.8 MB (59802153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf000fd24a3e47a1ce84c2ed406bcd3fde07ed93c16fb011e2ea7941e273d33`  
		Last Modified: Wed, 22 Apr 2026 16:23:17 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd04fbe6ec56a98cc9e1a817922e16079ef924dc16e28e936e0c3550e86b1b0b`  
		Last Modified: Wed, 22 Apr 2026 16:23:17 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:5ddf4a8fa3bf337fb6652ab7e6dbfd7ae5e9ef3ebac5c2188e8f16130e22059c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16080451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:073ae0759a7ca88e4296f8dfae97ffdcae2e32ab8aeeed4641009158470eee89`

```dockerfile
```

-	Layers:
	-	`sha256:95d189118c62ef9653d9f6eebf15e5baec297d5112c42209da2b939e62d5f4c5`  
		Last Modified: Wed, 22 Apr 2026 16:23:18 GMT  
		Size: 16.1 MB (16055861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4c28cef895dc908732b0e9efb5ac44cb172772e3d2fee551eb71d1a1ed7beab6`  
		Last Modified: Wed, 22 Apr 2026 16:23:17 GMT  
		Size: 24.6 KB (24590 bytes)  
		MIME: application/vnd.in-toto+json

### `node:bookworm` - linux; s390x

```console
$ docker pull node@sha256:2aa48bf3bdb9153d165754c8274dabf06ed80fa17bb5ea6db5351c812c25c2b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.9 MB (381909384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c8d4a3f7075a43ac1bf1ad758a073e86f2f047d35bacc88fbd5ab23afd8a82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1776729600'
# Wed, 22 Apr 2026 02:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 04:20:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 05:13:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Apr 2026 08:08:31 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 22 Apr 2026 08:08:42 GMT
ENV NODE_VERSION=25.9.0
# Wed, 22 Apr 2026 08:08:42 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     5BE8A3F6C8A5C01D106C0AD820B1A390B168D356     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||       { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 08:08:42 GMT
ENV YARN_VERSION=1.22.22
# Wed, 22 Apr 2026 08:08:46 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     { gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ||     { gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" && gpg --batch --fingerprint "$key"; } ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 22 Apr 2026 08:08:46 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 22 Apr 2026 08:08:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Apr 2026 08:08:46 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:65a8acd2327b0f3316fe8707ebd5c99b15e79306d4eca71f3e635588795ae2bb`  
		Last Modified: Wed, 22 Apr 2026 00:15:31 GMT  
		Size: 47.1 MB (47147970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac385f32c2d6e9209dd9f8ada378863aba00921ac3815f399e84f802ea5ce36e`  
		Last Modified: Wed, 22 Apr 2026 02:32:03 GMT  
		Size: 24.0 MB (24036363 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8df5494ce4223646f47cc2e95923748571f15dc98fdcd0c46696a358fa2128f`  
		Last Modified: Wed, 22 Apr 2026 04:20:41 GMT  
		Size: 63.5 MB (63500148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f897cf0b1d07756a3ff6dc04beacb6e6510a8778c56dc69d1a9dd01701400550`  
		Last Modified: Wed, 22 Apr 2026 05:14:17 GMT  
		Size: 183.6 MB (183571818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1095398ce8b544ce22a7e55a7677d32d8a6b5bf55e6ede7779b697d28e82d0af`  
		Last Modified: Wed, 22 Apr 2026 08:09:39 GMT  
		Size: 3.3 KB (3319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d0e874d87a9150641e2c271333b669145a73f37d01ec1c6f18fbcdf7df48d6`  
		Last Modified: Wed, 22 Apr 2026 08:09:41 GMT  
		Size: 62.4 MB (62398646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6fd2a1f2485f5cf267a1e92796d6251105bd5d873f0dccd46f4de9d03c8572a`  
		Last Modified: Wed, 22 Apr 2026 08:09:39 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13eef87cbbdd9b0ee6540607eedea13be433ab0c39d74ca8bd185097918533e1`  
		Last Modified: Wed, 22 Apr 2026 08:09:39 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:bookworm` - unknown; unknown

```console
$ docker pull node@sha256:26d4fbe75a6b5ee218b75a45e3df9a47b7e1ff4c9c14fa40723646abfcd07a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15911410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9357c26de3fe54893f9054230e3a42b0ca162fc8cc7ebd8127cc65f53368a1c1`

```dockerfile
```

-	Layers:
	-	`sha256:19c0832b8e3f292f4d4dfdc7927839f8dcbf4de1dd9bc236933c5e67aa1b3cec`  
		Last Modified: Wed, 22 Apr 2026 08:09:40 GMT  
		Size: 15.9 MB (15886904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4376a625296b7f1d4b22790e2f865b21bc8b4f5902a3b0ce2b4a5d3456ceeb4`  
		Last Modified: Wed, 22 Apr 2026 08:09:39 GMT  
		Size: 24.5 KB (24506 bytes)  
		MIME: application/vnd.in-toto+json
