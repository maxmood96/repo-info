## `node:lts-bullseye`

```console
$ docker pull node@sha256:8ed4363da3ee6f4d6c95465d0837e92201ada020e706d00d4a4826bcd1074e0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `node:lts-bullseye` - linux; amd64

```console
$ docker pull node@sha256:a0074524b2d2d84f85f8b6262c3a6ad01876be80828e4097375adff467db446a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.1 MB (372116094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c049e15d6c413315e7fc9bb38dd3db4f72d899e582db1ea5a52d2943882768a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 27 Sep 2024 04:29:42 GMT
ADD file:52a4b3d3a7281812594cb25cd6c6e83649d63a981e9f92f7c189ebe080249490 in / 
# Fri, 27 Sep 2024 04:29:43 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:09:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:10:31 GMT
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
	-	`sha256:014ac6453c34f79cc163f6567c184e5eb0b48cdc07ecbfb1388d90e95ac90b02`  
		Last Modified: Fri, 27 Sep 2024 04:33:28 GMT  
		Size: 55.1 MB (55081391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21912b76607d1849ada521d53cc1be42bcc38d6583bd385a1bbd91babc6745f8`  
		Last Modified: Fri, 27 Sep 2024 05:15:27 GMT  
		Size: 15.8 MB (15764314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee27f1f94c19451b787e3a7d81f5eefbd7aed799349b4208bb04c1ce8880ccb2`  
		Last Modified: Fri, 27 Sep 2024 05:15:42 GMT  
		Size: 54.7 MB (54723654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7a7fe5b36fbd67e153a5a6e8ec36c41c1fb931871662835b9abdd59e785fdb`  
		Last Modified: Fri, 27 Sep 2024 05:16:13 GMT  
		Size: 197.1 MB (197069002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ecfc9458f40978838b0689372f78e73ee19cb6d41e95b689c26de5bf9cc6836`  
		Last Modified: Fri, 04 Oct 2024 18:57:22 GMT  
		Size: 4.1 KB (4090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba0e74124c6f14ec13ac4cc3c8d0a45095bdb303c15654a1fc61267c09ac39e`  
		Last Modified: Fri, 04 Oct 2024 18:57:23 GMT  
		Size: 48.2 MB (48222518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea7b4c56b1493d9104702bff08278ebbd8ae429ad39a54eb4c87c0a25e7775a8`  
		Last Modified: Fri, 04 Oct 2024 18:57:22 GMT  
		Size: 1.3 MB (1250676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b198f1bc4ec1f4e1ca304a6fef4e6736ec78cc4cdf844a8cbf7130437bd99481`  
		Last Modified: Fri, 04 Oct 2024 18:57:22 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:4e1bc313503dacac40d5639e45e781d20d2bc7d28163f0c367df4e6029ef5ceb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15340560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3873ac2a71b6e0ccb2d5de3c3b45cb0ce1e3cbdeac843914226573e608bfc9b8`

```dockerfile
```

-	Layers:
	-	`sha256:5dbf5d5346987a7a454cd2bc692b675139c05362d307ef88062fbbb97957fdff`  
		Last Modified: Fri, 04 Oct 2024 18:57:22 GMT  
		Size: 15.3 MB (15317790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78585b95a9e2bdbb31bc76b1a4b9de0758c1e50543d71ec41d20cbd1a36530fc`  
		Last Modified: Fri, 04 Oct 2024 18:57:22 GMT  
		Size: 22.8 KB (22770 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:fd9071227987d05c2b2d10ff3c768be9c0d4f42d61376e119b2e5499d892fdc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328806314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37aa656ca15433f6d417da70d133d4fa8ae4da95b3516b2eb98d556f6b11d60a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 27 Sep 2024 05:13:55 GMT
ADD file:9ce266c398209e90f7206a05ac5b3ad0e1b36639b555d8c794491312b40e94cc in / 
# Fri, 27 Sep 2024 05:13:56 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:31:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 07:33:07 GMT
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
	-	`sha256:5b73fe599d8a11adf217817ed59555cdbc95d93efb1d72ea85683e0e5ea179d6`  
		Last Modified: Fri, 27 Sep 2024 05:17:30 GMT  
		Size: 50.2 MB (50240380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fec523352a6e63a855ebebdbc8288b9cccf719fe4121211d5e0cae3f11e4f6b2`  
		Last Modified: Fri, 27 Sep 2024 07:39:46 GMT  
		Size: 14.9 MB (14879678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bfb8add2d4bda22b21df2a3eff38a6f4f66c2ef9fe110e7714a93f720a4f47`  
		Last Modified: Fri, 27 Sep 2024 07:40:06 GMT  
		Size: 50.6 MB (50618560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07f69bcefdc97cf5fabaf3b01d416ce54278fa217058c4433beb68d39a6e1bc1`  
		Last Modified: Fri, 27 Sep 2024 07:40:47 GMT  
		Size: 167.5 MB (167508654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95784ccf34df4aceb6457feeeb4515a04e3413e9b1b54babfa739cf467d0a778`  
		Last Modified: Fri, 27 Sep 2024 23:47:53 GMT  
		Size: 4.1 KB (4074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca8f3c6ca3f236c97c5f1ef486fde17eb28047665a9822a221d1ff1534470f19`  
		Last Modified: Fri, 04 Oct 2024 21:00:07 GMT  
		Size: 44.3 MB (44303843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d728c52aea87d3f34153e4016439669a5b9ff1060661087edefb711df7776b2`  
		Last Modified: Fri, 04 Oct 2024 21:00:06 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc14c0bc7e8478a3efe6f69f80d9e87fe72c9e88f1b2c7d31fd0b94c4176948`  
		Last Modified: Fri, 04 Oct 2024 21:00:05 GMT  
		Size: 450.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:1e526f226279262358f77a775ebfa550a544043d734bef79181777f331c0a940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15141699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a082ad6e7b46a6af03a1648201f33a922ac5686029449786626e576c65cc616`

```dockerfile
```

-	Layers:
	-	`sha256:269caf45de67f8668eb012c6815d7b1a180c1143643965eb563f8d75f9db4a7b`  
		Last Modified: Fri, 04 Oct 2024 21:00:06 GMT  
		Size: 15.1 MB (15118825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07aec52e3a020713710fb43e4e730a1a93e4e9fee1d11fcf08708019b5a250aa`  
		Last Modified: Fri, 04 Oct 2024 21:00:05 GMT  
		Size: 22.9 KB (22874 bytes)  
		MIME: application/vnd.in-toto+json

### `node:lts-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:d406d325e834909db344c9c309ada54e4f8018f77520988f9f0efd9d23518ff5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363722698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31df17e7edfcf5c9f47d2ed0cf6e4737a7acd2065a2add3715dac1019fc0aefd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:24 GMT
ADD file:20638e93d5a3e884b24b90ba3bef17ad5a4c795085c457bd5729f2f5caaf6a73 in / 
# Fri, 27 Sep 2024 04:38:25 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:20:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 27 Sep 2024 05:20:53 GMT
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
	-	`sha256:374a548aba539daa8d37f8b0fe7326b582daa60fe22cc343a838af2e82a4ca1c`  
		Last Modified: Fri, 27 Sep 2024 04:41:08 GMT  
		Size: 53.7 MB (53733864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb4bba36b8add5e5ec5da6aa2c18637b64bce2d5f3f7d83723817e2139a11bcc`  
		Last Modified: Fri, 27 Sep 2024 05:25:50 GMT  
		Size: 15.7 MB (15749698 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f212bcfdd3a473cde2991df3e1cf5373d8f097a630557a35fa77d891acce93d6`  
		Last Modified: Fri, 27 Sep 2024 05:26:04 GMT  
		Size: 54.8 MB (54834694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09310330a122777457e6d6b3094e1d1391aa246ba1b028adeb03cd353d0d29`  
		Last Modified: Fri, 27 Sep 2024 05:26:28 GMT  
		Size: 190.0 MB (189964252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b4a0aae549957d497367fc72504f7823b6f4c22b3799ae9cd3db9900d440152`  
		Last Modified: Fri, 04 Oct 2024 19:51:57 GMT  
		Size: 4.1 KB (4099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637bfe05c5dc62d7064fbda17f065ca954f556275349baafb510914956686f1a`  
		Last Modified: Fri, 04 Oct 2024 19:51:58 GMT  
		Size: 48.2 MB (48184974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d234f7d299e80bab4917cc495b7099c600c308ee5cb7391155d77335a93d4d6b`  
		Last Modified: Fri, 04 Oct 2024 19:51:57 GMT  
		Size: 1.3 MB (1250669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcb4266586f5d8ff05b986cdac9d324b3fb56a4cce66585ea47495c8e206a10d`  
		Last Modified: Fri, 04 Oct 2024 19:51:57 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:lts-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:88099f49f623ba98e3db3da0b41e7ced74c835d8070bdd88e2c518093652e1f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15343078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fc0f9ffd88bbd4bd32ebf5e49592f84ae8b63e8240ec869663c53bbaece7fa5`

```dockerfile
```

-	Layers:
	-	`sha256:337aa8972f29727c0b09e258d4b767e248ff0c44828ae6e863cf5af63d1ca8fa`  
		Last Modified: Fri, 04 Oct 2024 19:51:57 GMT  
		Size: 15.3 MB (15320168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0997ddb48dbd6ae58e1904b8aa4538bbf4775eb7b6f1a35888f2ec14e441fb6c`  
		Last Modified: Fri, 04 Oct 2024 19:51:56 GMT  
		Size: 22.9 KB (22910 bytes)  
		MIME: application/vnd.in-toto+json
