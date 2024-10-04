## `node:lts-bookworm`

```console
$ docker pull node@sha256:d9204281f05b497330fe26b29761e0445707dd9b4e484db73d491e01d47702c3
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

### `node:lts-bookworm` - linux; amd64

```console
$ docker pull node@sha256:979b917260c5ac04146dd0f21f2a820ce14084ed54012498a87ebcaf4c128e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 MB (398743040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef970e331526a3ccb44f8915cc0f1cc0265e6b2b4418f380e369618faa117f75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:19 GMT
ADD file:087f68d5558e06c7160c9322582925635e7539a7702413828357c28c77f6f345 in / 
# Fri, 27 Sep 2024 04:29:20 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:08:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Oct 2024 15:27:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
ENV NODE_VERSION=20.18.0
# Fri, 04 Oct 2024 15:27:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
ENV YARN_VERSION=1.22.22
# Fri, 04 Oct 2024 15:27:57 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 15:27:57 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:cdd62bf39133c498a16f7a7b1b6555ba43d02b2511c508fa4c0a9b1975ffe20e`  
		Last Modified: Fri, 27 Sep 2024 04:32:50 GMT  
		Size: 49.6 MB (49555051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a47cff7f31e941e78bf63ca19f0811b675283e2c00ddea10c57f78d93b2bc343`  
		Last Modified: Fri, 27 Sep 2024 05:14:26 GMT  
		Size: 24.1 MB (24053049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a173f2aee8e962ea19db1e418ae84a0c9f71480b51f768a19332dfa83d7722a5`  
		Last Modified: Fri, 27 Sep 2024 05:14:43 GMT  
		Size: 64.4 MB (64392323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01272fe8adbacc44afd2b92994b31c40a151f4324ca392050d9e8d580927dd32`  
		Last Modified: Fri, 27 Sep 2024 05:15:17 GMT  
		Size: 211.3 MB (211265642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69752a170a9cd7718768d71ae627b34ce2b63e0b0f1b21ba345f0f665ed46e14`  
		Last Modified: Fri, 04 Oct 2024 18:57:30 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6986256fa1607627a696c196c33290f4f96f88a1b0a41275327a2f69612bbed5`  
		Last Modified: Fri, 04 Oct 2024 18:57:33 GMT  
		Size: 48.2 MB (48222526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:894ebdcee85de9bf6daf452b243b65a082986d7865d984ec080c81f01e7bff53`  
		Last Modified: Fri, 04 Oct 2024 18:57:31 GMT  
		Size: 1.3 MB (1250676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4163bcd94ffee8c075555d4a8d9531bce8f7fd572e00d4326a8ff15409ea7e04`  
		Last Modified: Fri, 04 Oct 2024 18:57:30 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:74174ab52572ea55ec27db2f0efcf7c64824e0522cefcb5a1e650b8f87569e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15743262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52a3bac911d4f704763e02526045d3152ad1fef765d2442d26da13a992f75f20`

```dockerfile
```

-	Layers:
	-	`sha256:57178bee663716f4ea47031234a4cb38cf153861c9dd96edd0a79dbec198d9ce`  
		Last Modified: Fri, 04 Oct 2024 18:57:31 GMT  
		Size: 15.7 MB (15718743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93f6797cec8fc993c0588fd411b6c722385ec2c8eb336fcc8dada8de55dfc2a9`  
		Last Modified: Fri, 04 Oct 2024 18:57:30 GMT  
		Size: 24.5 KB (24519 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-bookworm` - linux; arm variant v7

```console
$ docker pull node@sha256:bede236f02a7d1b9a772a821403dc5776a876461bc68b1c40c65b2de15c37770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.5 MB (347461046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3772acfd405521b586e251586f8d1cb4aea358f2ddc9d73b4502c5a61ca0da6f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 21 Aug 2024 19:04:33 GMT
ADD file:49c32fc494edae0bed40e890247b9ef7df519d1e54935d02413688f8bf40ff64 in / 
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV NODE_VERSION=20.17.0
# Wed, 21 Aug 2024 19:04:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV YARN_VERSION=1.22.22
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:1450ddb05e7bb5bf1d3f39b84ab0fd335cb7a83278261349391848d6d6ebe12e`  
		Last Modified: Fri, 27 Sep 2024 05:16:52 GMT  
		Size: 45.1 MB (45147913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f70a0f54506c0e5d7968526bbfe4c20cb47120ed77a04daff3faf5eb96171900`  
		Last Modified: Fri, 27 Sep 2024 07:38:31 GMT  
		Size: 22.0 MB (21957548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1d8069439bcb2f814251e906dcc07c3e02aa2c77623cc5603448c7e08e710ab`  
		Last Modified: Fri, 27 Sep 2024 07:38:54 GMT  
		Size: 59.6 MB (59639666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea668db82ddd31e7300e905d69bfbcc24fd0c70cd7c7212c915763a9e47f3e7`  
		Last Modified: Fri, 27 Sep 2024 07:39:33 GMT  
		Size: 175.2 MB (175207938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9138db288ce843aec86eb507f4a4041dffe5544ac46c7eb0c9cad128f4f1997d`  
		Last Modified: Fri, 27 Sep 2024 23:45:56 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14fa22fe658e0a133ac9f6b607898958289f8743fd59a1cccc824c1bbed1b6fe`  
		Last Modified: Fri, 27 Sep 2024 23:50:25 GMT  
		Size: 44.3 MB (44253541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351119324da501a746778d3d4e30374780b249efe44656b1fd771fd69ca956b8`  
		Last Modified: Fri, 27 Sep 2024 23:50:23 GMT  
		Size: 1.3 MB (1250673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2776bfd930c9c65aa31e5d198e9ec85c701a2fb5b0481f7c734a7a50b71402a`  
		Last Modified: Fri, 27 Sep 2024 23:50:23 GMT  
		Size: 445.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:f2a13bab7dcf6076121787e42a86bdcdfbc48b3387011dca9b79347570a18721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.5 MB (15548595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ead22b99acaeee8c3896fb902b35baaad8b365699cd9bc87f161941609f094`

```dockerfile
```

-	Layers:
	-	`sha256:a58aa687737231f5e469ec36c96a9e01951b560f16faef6a1b4f5abbbfcbe0af`  
		Last Modified: Fri, 27 Sep 2024 23:50:23 GMT  
		Size: 15.5 MB (15523634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50ae42bd32c975543de851b188aa24290dc6677d0711ac5dd470a0e477ec9dc7`  
		Last Modified: Fri, 27 Sep 2024 23:50:22 GMT  
		Size: 25.0 KB (24961 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:dcdf3abdb18f4ad87b7ea4508fb2e18224cc21c53dd30939d2b7ea5e90fc188d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 MB (389549276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ded92f6e58904cadd7fb6df8dcc8ca23cf034aba4c6640342c35f5ae8feffcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 21 Aug 2024 19:04:33 GMT
ADD file:e689b230a6f8e5eb3500dfa6f80afd8bda70b82deda3656ddeea10df15dd54c3 in / 
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["bash"]
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Aug 2024 19:04:33 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV NODE_VERSION=20.17.0
# Wed, 21 Aug 2024 19:04:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENV YARN_VERSION=1.22.22
# Wed, 21 Aug 2024 19:04:33 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 21 Aug 2024 19:04:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Aug 2024 19:04:33 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6d11c181ebb38ef30f2681a42f02030bc6fdcfbe9d5248270ee065eb7302b500`  
		Last Modified: Fri, 27 Sep 2024 04:40:33 GMT  
		Size: 49.6 MB (49584886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b238499ec52e0d6be479f948c76ba0bc3cc282f612d5a6a4b5ef52ff45f6b2c`  
		Last Modified: Fri, 27 Sep 2024 05:24:56 GMT  
		Size: 23.6 MB (23594043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b754d079e82fafdf15447cfc188868092eaf1cf4a3f96c9d90ab1b7db91230`  
		Last Modified: Fri, 27 Sep 2024 05:25:12 GMT  
		Size: 64.3 MB (64349696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71ace0e8bbdcfcf795b836e24a37a6ed0054100e14d6aa6e5a63f7e162ba729`  
		Last Modified: Fri, 27 Sep 2024 05:25:40 GMT  
		Size: 202.7 MB (202651718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d629be7509338cb54b2000d6e955e61cd65e815f47eff1ba13040c71fa12b0bb`  
		Last Modified: Fri, 27 Sep 2024 15:34:14 GMT  
		Size: 3.3 KB (3320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d972059172e715bdd49f6d6aa20a79539fd82b86b8987dfb3e0c11a879b31604`  
		Last Modified: Fri, 27 Sep 2024 15:38:45 GMT  
		Size: 48.1 MB (48114495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e1b4555ab69732872330804735e388eb036e378dd47999fbe2b0953e004426`  
		Last Modified: Fri, 27 Sep 2024 15:38:44 GMT  
		Size: 1.3 MB (1250672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8a2f37eac20eef957b233c18a8830bd24edace0459335b4fbbd272cb6483fb9`  
		Last Modified: Fri, 27 Sep 2024 15:38:44 GMT  
		Size: 446.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:e7c4076aaff2a1123d9113353c5df431696f34aaaee94c732359d39bad3502ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15772588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2464f3e6842cdd9395d9b5e2294e7c1c569ccc67f56a107261ecc7453e2d7d63`

```dockerfile
```

-	Layers:
	-	`sha256:19c0f92e403006df3c5d59e6f5403cd082d1854cc30308d432cddf10e4325c80`  
		Last Modified: Fri, 27 Sep 2024 15:38:45 GMT  
		Size: 15.7 MB (15747383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39706a23757b3ed52415d6522d4d41f40a591e392879fe5a2d3a78fb5fd51715`  
		Last Modified: Fri, 27 Sep 2024 15:38:44 GMT  
		Size: 25.2 KB (25205 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:9b4db251aa2c99525f4b7d7accb986269028ff143c203660593da0df66a578db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.3 MB (415325469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d9f7f2a3cbbf07be45039392d761eeda9187e597ae323d10e8a23212e28d6cf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 27 Sep 2024 05:32:50 GMT
ADD file:39bfb91ec68f023ba3e4a3c05d0dfdb989ff60ef5e4b837a0ecaa8942b2ad723 in / 
# Fri, 27 Sep 2024 05:32:53 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:55:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:56:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:57:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Oct 2024 15:27:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
ENV NODE_VERSION=20.18.0
# Fri, 04 Oct 2024 15:27:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
ENV YARN_VERSION=1.22.22
# Fri, 04 Oct 2024 15:27:57 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 15:27:57 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:2152610574debd8c97d08dc906619a0e0236b1babe381e6bb4344af83de79b32`  
		Last Modified: Fri, 27 Sep 2024 05:35:55 GMT  
		Size: 53.6 MB (53555157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f01e8a9703247996468adbac5e62ad953af89ee07fab102b87f0f239ba5b248`  
		Last Modified: Fri, 27 Sep 2024 06:04:25 GMT  
		Size: 25.7 MB (25710201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:969201721a962bfe7832a7e84f31d0ea32d3b9ab675bc1c2b0b546921a9233ed`  
		Last Modified: Fri, 27 Sep 2024 06:04:45 GMT  
		Size: 69.8 MB (69829501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e2f2830e2003232ca51768518e8eb9e372430ea0c0445d3ec3c8d96672cb8c`  
		Last Modified: Fri, 27 Sep 2024 06:05:25 GMT  
		Size: 214.3 MB (214285718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c48a0f70de91b4bb3b7e8b60597f3e4f16805626bf5353f3da1daf43361dc5ef`  
		Last Modified: Fri, 04 Oct 2024 19:31:49 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe7c6d3e03ebbde62d5f002b94de101bb1f5bbe87aaa17005bb83baae1591096`  
		Last Modified: Fri, 04 Oct 2024 19:31:51 GMT  
		Size: 50.7 MB (50690440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f189732af443e2563f522310943b122c1982d73dc76d98528c09ac21aee23e49`  
		Last Modified: Fri, 04 Oct 2024 19:31:50 GMT  
		Size: 1.3 MB (1250678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:180757f72b0ee2226b427b302e4905a84446ac8edaae8503a52cc2e6d46186bd`  
		Last Modified: Fri, 04 Oct 2024 19:31:49 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:09534f4be26325151ac6ef7c13d1ec9f6aae4c59329cb15be76a87abe3da396f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.7 MB (15719909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82dc7907f2e818bc03bfbbdd5c53b1d08c603f5a9e8151b3773a0abc829647fc`

```dockerfile
```

-	Layers:
	-	`sha256:68ac818e7769eeb14240dff20c8108047495b4c3a8fe5f43aac72053dad2098c`  
		Last Modified: Fri, 04 Oct 2024 19:31:50 GMT  
		Size: 15.7 MB (15695306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f22d576085a0155638cc1d477bad04550dbdb27dd9e9d2f135ff18237ac8d5c6`  
		Last Modified: Fri, 04 Oct 2024 19:31:49 GMT  
		Size: 24.6 KB (24603 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-bookworm` - linux; s390x

```console
$ docker pull node@sha256:20b1118cb2cc8038809b47518a8abbce560946b3a15b5a37a0032be9ebf5ae87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.0 MB (368049235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:427dfbe74e44ef58ba34a8bd11e5bd63d593a4186ba3156e45c5305d0a137a5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:05 GMT
ADD file:13791d2f4c8294a5a26418d80bbff45c57fab5ce92bdae0e320e66cb17100687 in / 
# Fri, 27 Sep 2024 02:43:07 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:12:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:13:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 03:14:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Oct 2024 15:27:57 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
ENV NODE_VERSION=20.18.0
# Fri, 04 Oct 2024 15:27:57 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     CC68F5A3106FF448322E48ED27F5E38D5B0A215F     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
ENV YARN_VERSION=1.22.22
# Fri, 04 Oct 2024 15:27:57 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 04 Oct 2024 15:27:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 04 Oct 2024 15:27:57 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6a5a49e215ac054c13cd0ff6e9a0c18a9c165966cef8ed4784be68b4de5e4efb`  
		Last Modified: Fri, 27 Sep 2024 02:47:05 GMT  
		Size: 47.9 MB (47938670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2004fe4a468d3282361e2ef876bdcc17abe5a1687258f6815b0da8184479ae63`  
		Last Modified: Fri, 27 Sep 2024 03:20:20 GMT  
		Size: 24.1 MB (24051974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78ee8056ef9e7b7b84c8a2dbc9be7594311846c7f56746c00b61aefdf68b74a5`  
		Last Modified: Fri, 27 Sep 2024 03:20:35 GMT  
		Size: 63.5 MB (63495242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1411196315040fbdc5fb36f5519fcdf47619046fa9476d4e7607333bcbd8131`  
		Last Modified: Fri, 27 Sep 2024 03:21:02 GMT  
		Size: 183.3 MB (183287662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2601f7aea30e54d3d5776ea0fc395fe2ebc608e382e8acab81940a16f32ba0cd`  
		Last Modified: Fri, 04 Oct 2024 20:18:01 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ba7de9e3d9bc2becb93abf9c31deb6b2dd46936923763f557e1c62578b37fb`  
		Last Modified: Fri, 04 Oct 2024 20:18:02 GMT  
		Size: 48.0 MB (48021233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a90814d8a4f3c81d1417c02ba235c69a23204d38b58e35ae5a3ae1c0a02f76`  
		Last Modified: Fri, 04 Oct 2024 20:18:02 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5c162bd57f234e3b356a9bbc8f0c3919d10bf1e54396f580f487b0d90c8b2ab`  
		Last Modified: Fri, 04 Oct 2024 20:18:01 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bookworm` - unknown; unknown

```console
$ docker pull node@sha256:ab180380b9ccb1b63a159fa0984c7c57fe866da97a43cca666497a63847f4a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.6 MB (15556658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eaf612f8540f6786883eba20b5e22fa7d713116978476c7e11501f0a056429a`

```dockerfile
```

-	Layers:
	-	`sha256:73ef4587754ce968fca23fe15bb7a9907edd7f16147fffa33b3df0e561639c29`  
		Last Modified: Fri, 04 Oct 2024 20:18:02 GMT  
		Size: 15.5 MB (15532138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b6c0e757331a7e023474b340772d8be183c6c5a0ac21118b646e492bc55b137`  
		Last Modified: Fri, 04 Oct 2024 20:18:01 GMT  
		Size: 24.5 KB (24520 bytes)  
		MIME: application/vnd.in-toto+json
