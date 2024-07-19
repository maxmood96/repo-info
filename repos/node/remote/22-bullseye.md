## `node:22-bullseye`

```console
$ docker pull node@sha256:fe4b70f53b78c793737d393b827480f37865944444a1d7137c17c47699d220f5
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

### `node:22-bullseye` - linux; amd64

```console
$ docker pull node@sha256:f3f4c4bb68edd0acaadf89273a6b2b0e996666959cc2f4d50008db0bcf1ecea1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **376.8 MB (376822487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0750423bad6956bcec3caa914945f7092c9b8030370e15763bd4922c272fe6c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 02 Jul 2024 01:25:11 GMT
ADD file:b8d066bbda2d783c3ca81ab100fc5e45550234b68fde96332f303f669256842e in / 
# Tue, 02 Jul 2024 01:25:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:50:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:51:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV NODE_VERSION=22.5.1
# Fri, 19 Jul 2024 15:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV YARN_VERSION=1.22.22
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:c1c1a7d83fb1e16686c4e98df3d6f88b37beb4d65daae1ddd715f95d7ac4db5c`  
		Last Modified: Tue, 02 Jul 2024 01:29:07 GMT  
		Size: 55.1 MB (55081360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a305f523084f0a28b5daf532a5216d9be05d863c6bd3f5bd2969965eb7e9a27`  
		Last Modified: Tue, 02 Jul 2024 02:01:21 GMT  
		Size: 15.8 MB (15764174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da238dd9d1f579bf4f3cd6589e3ab75747f8ea35be2bf50403f8f3fafa942eea`  
		Last Modified: Tue, 02 Jul 2024 02:01:35 GMT  
		Size: 54.6 MB (54588637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414da18c1936c380bc310a14aa9627a150fd6e6393e752068962869f27d2907c`  
		Last Modified: Tue, 02 Jul 2024 02:02:06 GMT  
		Size: 197.0 MB (197018307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5704f9c2db9386a05ca9b6a5b992cb64cc232e0a3799e1992fe9d1436a12e4b6`  
		Last Modified: Fri, 19 Jul 2024 17:59:09 GMT  
		Size: 4.1 KB (4092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e99fe4895318b05f8c59bf6693e85863b333617a0058daa3d0bb6cc257e42b2`  
		Last Modified: Fri, 19 Jul 2024 17:59:10 GMT  
		Size: 53.1 MB (53114791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868eccaf9070a87d98bf79fef375a412763be3f31728dc343a30f53be8998e34`  
		Last Modified: Fri, 19 Jul 2024 17:59:09 GMT  
		Size: 1.3 MB (1250678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcb9d41ff827a9913e6877bd9798e6b44833ad198a35d896e0a9228207d65ef`  
		Last Modified: Fri, 19 Jul 2024 17:59:09 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:cd72909051d9d598d0b7cb43de6c77edb0247fc29ea4d3082dc60ad87d838cea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15341604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6596965d14cd50587c58fea1a50995f7f52ab75036da645b189464742bbe285`

```dockerfile
```

-	Layers:
	-	`sha256:aa7f78ece265660d09fff076d8bf7b9df76f3b5f5fdaacd63dba3dc39b77636a`  
		Last Modified: Fri, 19 Jul 2024 17:59:09 GMT  
		Size: 15.3 MB (15318554 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e08adbed9b15a8e220a09caef7dee565359b7db8ce00fd1b9c9efa65804da3dc`  
		Last Modified: Fri, 19 Jul 2024 17:59:09 GMT  
		Size: 23.1 KB (23050 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:1aef7a5f20bc7d78dec41c3f334a4ab7c425866ca646fe524b3f13ffa096c9ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.9 MB (332884598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb3645640a9b8e698d233fdb46672b509ed68037740d7f82d610b51cb22290a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 02 Jul 2024 01:00:11 GMT
ADD file:6e828fd5dbd54f949f96129ea922c27ff88709484119faef51401e338e900e6e in / 
# Tue, 02 Jul 2024 01:00:12 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:27:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Jul 2024 03:35:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
ENV NODE_VERSION=22.5.0
# Thu, 18 Jul 2024 03:35:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jul 2024 03:35:26 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jul 2024 03:35:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a0610bbe9cb80952dba5ef5efb55f03668fd4f8ab63ade3ba30e22a4c03c42da`  
		Last Modified: Tue, 02 Jul 2024 01:03:38 GMT  
		Size: 50.2 MB (50238998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5c595e4d8c2d2c7ad66ab723b54c73c6a0aa876b01511358ec8af1aed8c8b94`  
		Last Modified: Tue, 02 Jul 2024 01:40:13 GMT  
		Size: 14.9 MB (14879331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:577c5fe1f5243a6910c54b7b4a338cc9cbae0cfeba74a350b011d2a467e49daf`  
		Last Modified: Tue, 02 Jul 2024 01:40:31 GMT  
		Size: 50.4 MB (50358262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e53a04feb4a55b8a4920c0ad42332dddf76ad9bb3bd19eac2f580036953cf88`  
		Last Modified: Tue, 02 Jul 2024 01:41:09 GMT  
		Size: 167.5 MB (167478798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ed19a1394b43c07d29172d70a52103db93bea790137e7be9b79c8b324c1cc3d`  
		Last Modified: Thu, 18 Jul 2024 16:58:07 GMT  
		Size: 4.1 KB (4079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc88c53024c9304b4181bbf1991cfb419589683eddc29e43171ab14589948144`  
		Last Modified: Thu, 18 Jul 2024 16:58:09 GMT  
		Size: 48.7 MB (48674007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977756d931fb4dbf477e14ac703b1f20797dde2123513ecee2d8dba2e7b997a5`  
		Last Modified: Thu, 18 Jul 2024 16:58:08 GMT  
		Size: 1.3 MB (1250675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:690f2fb55c2e84d6d306fa1a7c9d5660a262f04bb47d7bc42215f10cf4a0f4d1`  
		Last Modified: Thu, 18 Jul 2024 16:58:07 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:785fb1765a7c317ffa7ae9c9e8f4f343d3e9ddd7b83df741b3c47a665e4adcf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.1 MB (15142744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9310c53e538b3fcb8ddc45019566ce4b7dc7fa792a8640ec803b5d52c19b73`

```dockerfile
```

-	Layers:
	-	`sha256:e6ae001f740b8c46c88be84b16a0302242f97f575c99f269398f271c8db38958`  
		Last Modified: Thu, 18 Jul 2024 16:58:08 GMT  
		Size: 15.1 MB (15119589 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29c1b38e2ad971e9716d3b6f603ce17ba0efc82998f3c204dc23a2d6347b7793`  
		Last Modified: Thu, 18 Jul 2024 16:58:07 GMT  
		Size: 23.2 KB (23155 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:9c021e845148304b1ea1e5b9b9b60826efea6664f11251d07da692503c6f25e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368354172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1221a22a04be60fd6d089ad0f6a156c53cc94f40719167640de934265526ca41`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 02 Jul 2024 00:39:43 GMT
ADD file:4e98397394fc6db8fa55fb21c15dab09007b6ba883cb193f3a53f94480fee872 in / 
# Tue, 02 Jul 2024 00:39:44 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:52:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:53:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Jul 2024 03:35:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
ENV NODE_VERSION=22.5.0
# Thu, 18 Jul 2024 03:35:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jul 2024 03:35:26 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jul 2024 03:35:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:a4cd3ad66f7873241881d2ddd4efa6521034245e95e2b0b4a059817345151048`  
		Last Modified: Tue, 02 Jul 2024 00:42:43 GMT  
		Size: 53.7 MB (53721653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:699d9ac7785741df545f96a8744d3a9a5c29f75a171fb8de0a0bae196294ad50`  
		Last Modified: Tue, 02 Jul 2024 04:02:37 GMT  
		Size: 15.7 MB (15749565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eeecfcb7b2ee9a8806953208440dbffd4b9110e5d2950924c7395e7ea3c070`  
		Last Modified: Tue, 02 Jul 2024 04:02:51 GMT  
		Size: 54.7 MB (54695057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c75f0ece8974d005f2532701f9fffb099d09a9bd1a53465b796982e4c2f594c`  
		Last Modified: Tue, 02 Jul 2024 04:03:16 GMT  
		Size: 189.9 MB (189935947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03223f72dc4f3bcd3c2334a22864c251e0446f3678512b32640eaa50b39475ea`  
		Last Modified: Thu, 18 Jul 2024 15:37:06 GMT  
		Size: 4.1 KB (4098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170926425ba5034478f2dcce47e6fde9fa071c0f983c44c4a9bf6cec9b580167`  
		Last Modified: Thu, 18 Jul 2024 15:37:08 GMT  
		Size: 53.0 MB (52996728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:724ea329560495f54e8cdcd0b6ac7223558f3690f371de9dc1315a8dfc1e46fe`  
		Last Modified: Thu, 18 Jul 2024 15:37:07 GMT  
		Size: 1.3 MB (1250676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfaf4a038a3cecd8c7c90bbace3adb0c7a9a4ea3831ee79b321eb015d58847aa`  
		Last Modified: Thu, 18 Jul 2024 15:37:06 GMT  
		Size: 448.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:b78532e3771bd6ac1b43eaa3ef5906f88ffdbc8ef40755a84193f710f2ed78c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15344306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:883325fe975081fc9e6b740989bbb8d8cc7622eee10de05c7c9e0dda1e8a43dd`

```dockerfile
```

-	Layers:
	-	`sha256:37080ebffd4f140b426d9166dacab6e808187df800a360086570388b2fc41978`  
		Last Modified: Thu, 18 Jul 2024 15:37:07 GMT  
		Size: 15.3 MB (15320932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d33a4b86a32f3f8adcbd1a642fcf5924c89f14d9d703c03a8f5ea39a7de9d7`  
		Last Modified: Thu, 18 Jul 2024 15:37:06 GMT  
		Size: 23.4 KB (23374 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-bullseye` - linux; ppc64le

```console
$ docker pull node@sha256:191792bb5debaced7774bb426b804f4d8d80e7a371a704b0b7dd14c9b50d331a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.9 MB (387927989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63d40bf5ee63edb845749d4718a263834916feea823ee6f89e1a72de8bcef95`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 02 Jul 2024 01:17:47 GMT
ADD file:288859e020cf9178f55732ac2eaa62400e2c2d66b3ca500ac7df69c8025abba9 in / 
# Tue, 02 Jul 2024 01:17:50 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 01:47:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:48:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 01:50:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 19 Jul 2024 15:48:06 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV NODE_VERSION=22.5.1
# Fri, 19 Jul 2024 15:48:06 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENV YARN_VERSION=1.22.22
# Fri, 19 Jul 2024 15:48:06 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 19 Jul 2024 15:48:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 19 Jul 2024 15:48:06 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:202e493da11eac96a36d754afa396feec67f46e0492e70c0cc4d61dfb06d6a75`  
		Last Modified: Tue, 02 Jul 2024 01:22:20 GMT  
		Size: 59.0 MB (58950397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8661ff02529d6818e558d6049a746391403c023c68ac6d75816221bd99e3244c`  
		Last Modified: Tue, 02 Jul 2024 02:05:47 GMT  
		Size: 16.8 MB (16765868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93f0edb37745f21593aefba0898d81dbc780a39dfe73cf03491e10c88480878`  
		Last Modified: Tue, 02 Jul 2024 02:06:04 GMT  
		Size: 58.9 MB (58872635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71ef5fcf94d321c187fa4f90d7b4b53743171e2926b6152cebcc4b0206128a8f`  
		Last Modified: Tue, 02 Jul 2024 02:06:39 GMT  
		Size: 196.4 MB (196369493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eaf66171012d310d00bfb2861b7d312708992f0ca204c3958671e566dce7958`  
		Last Modified: Thu, 18 Jul 2024 14:14:08 GMT  
		Size: 4.1 KB (4091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e61fd5a55c19bd3a1a813c021a4be16598ce9e732266e0a638b809eecc28ca`  
		Last Modified: Fri, 19 Jul 2024 18:12:31 GMT  
		Size: 55.7 MB (55714384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b3f178bd27286283d7b01900c36046dcd32dfa4e4a256f39f081db75d50c6b`  
		Last Modified: Fri, 19 Jul 2024 18:12:29 GMT  
		Size: 1.3 MB (1250674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d8f141364d7b82a83fe0bfb4030117c051223c2a980d3f05847b603ebfd6518`  
		Last Modified: Fri, 19 Jul 2024 18:12:29 GMT  
		Size: 447.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:6c40748648df945bb11866596e7ef76ebe80199a04e1f233fd1b1b8e50bc9237
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.3 MB (15310962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037dba5b9ce778804a518d865f873865536ebf33a9ffb64e0e9cd49065fe4ae5`

```dockerfile
```

-	Layers:
	-	`sha256:39dee2040dc4e84cf9c90a3d1a954882c80dbdb07a7cce6bfacf3e456f032d15`  
		Last Modified: Fri, 19 Jul 2024 18:12:30 GMT  
		Size: 15.3 MB (15287863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20a88166152965d9191082ef5e39277eb6284d65d2636187c28b0237946ba787`  
		Last Modified: Fri, 19 Jul 2024 18:12:29 GMT  
		Size: 23.1 KB (23099 bytes)  
		MIME: application/vnd.in-toto+json

### `node:22-bullseye` - linux; s390x

```console
$ docker pull node@sha256:c943d736ae58e58742a807af4fcb5b623ca0f3376847eaeb8297810986a5e0b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.0 MB (350015747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79e2b4a169ec28e1ca08934681e81b53fb8a348c7a0fba8a3a481bc072e9e15e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 02 Jul 2024 00:43:57 GMT
ADD file:5752d26037cbb262eeafd1819ecd77ecf8a8cd0019683c05fb92c50c6a458861 in / 
# Tue, 02 Jul 2024 00:44:00 GMT
CMD ["bash"]
# Tue, 02 Jul 2024 03:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:35:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Jul 2024 03:36:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Jul 2024 03:35:26 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
ENV NODE_VERSION=22.5.0
# Thu, 18 Jul 2024 03:35:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
ENV YARN_VERSION=1.22.22
# Thu, 18 Jul 2024 03:35:26 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/* # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 18 Jul 2024 03:35:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 18 Jul 2024 03:35:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:aa9549a3d8effd17bc1f93fd40d83261d2505d37791c5aa837c9f7c0fff5c9e3`  
		Last Modified: Tue, 02 Jul 2024 00:48:47 GMT  
		Size: 53.3 MB (53319825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7860b53e214213e98b388ade5c0d289331e291bb4e43197e4a14a4e8a111583e`  
		Last Modified: Tue, 02 Jul 2024 03:45:25 GMT  
		Size: 15.6 MB (15641817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8b8db73130bc88255a98f66627e7258a074a0223eef8b550e6c1084068d24d0`  
		Last Modified: Tue, 02 Jul 2024 03:45:38 GMT  
		Size: 54.1 MB (54075315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afac5d5564136a413fbebb4f4ab7b85f2fa277f71f996d27bc1d7e24b307c5d4`  
		Last Modified: Tue, 02 Jul 2024 03:46:03 GMT  
		Size: 173.0 MB (173024898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2306cf7f638e8c7ae48a28389cec756009a0f88c2eef4144dbbfbec9cb4b8021`  
		Last Modified: Thu, 18 Jul 2024 17:05:59 GMT  
		Size: 4.1 KB (4100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0dae3a581ede38e2cb485c4d0d95e2a92894f6bce015f3bf9aa8990424e8dba`  
		Last Modified: Thu, 18 Jul 2024 17:06:00 GMT  
		Size: 52.7 MB (52698665 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32de2c595cf3f9e05f15ea9e9aef128d0e949cffdb61cc23e5c085d046d4bd3`  
		Last Modified: Thu, 18 Jul 2024 17:05:59 GMT  
		Size: 1.3 MB (1250678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9079c8defd2e76ddd5004492d28509c91c3d9dbf31697dba7a8f626f5f20360b`  
		Last Modified: Thu, 18 Jul 2024 17:05:59 GMT  
		Size: 449.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `node:22-bullseye` - unknown; unknown

```console
$ docker pull node@sha256:63a628301672ebc1f3eb7ad769b658244580385ef9293c25fce7d5c24d5dc7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.2 MB (15162562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0292dd2ac325100b90887949bfa22cffe4eb2d485c4a2c2b823e05a85d6593e0`

```dockerfile
```

-	Layers:
	-	`sha256:205f967eb460068de788a0e32161660f79a139126723cc3642027caa1e8c688c`  
		Last Modified: Thu, 18 Jul 2024 17:05:59 GMT  
		Size: 15.1 MB (15139511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc066ec06fe2015189e5de5f336528cd3e0b40b3c9e679869867b82ce4aa133b`  
		Last Modified: Thu, 18 Jul 2024 17:05:59 GMT  
		Size: 23.1 KB (23051 bytes)  
		MIME: application/vnd.in-toto+json
