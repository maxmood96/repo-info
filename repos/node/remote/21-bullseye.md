## `node:21-bullseye`

```console
$ docker pull node@sha256:56185dc2982133b96f3fda7ac1666b80853203e54c83dd91d749933fab98eb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `node:21-bullseye` - linux; amd64

```console
$ docker pull node@sha256:31eab03caa3469172f9f96a254e8b5f0abc1f61e4ddfb6af6e57e9b359533133
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.4 MB (373436619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d974060b570bdf91542c54c2d69126718cbdb6fb1ee22438b17d40b45a32480`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 14 May 2024 01:28:14 GMT
ADD file:fc7856fc1fcc8bba68d0c729e34f64f4f113195167d677167a52eaa2c9760a19 in / 
# Tue, 14 May 2024 01:28:14 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:56:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:56:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 02:57:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 06:03:36 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 14 May 2024 06:06:12 GMT
ENV NODE_VERSION=21.7.3
# Tue, 14 May 2024 06:06:28 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Tue, 14 May 2024 06:06:29 GMT
ENV YARN_VERSION=1.22.19
# Tue, 14 May 2024 06:06:32 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/*
# Tue, 14 May 2024 06:06:32 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 14 May 2024 06:06:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 06:06:33 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:3d53ef4019fc129ba03f90790f8f7f28fd279b9357cf3a71423665323b8807d3`  
		Last Modified: Tue, 14 May 2024 01:32:47 GMT  
		Size: 55.1 MB (55099399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f0bf643eb6745d5c7e9bada33de1786ab2350240206a1956fa506a1b47b129`  
		Last Modified: Tue, 14 May 2024 03:05:14 GMT  
		Size: 15.8 MB (15764867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b037c2b46ab4e54a261a0ca65b12b93e00ca052e72765c9cc4caf1262a2b86c`  
		Last Modified: Tue, 14 May 2024 03:05:30 GMT  
		Size: 54.6 MB (54589605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6043113e1c69109f845390049c3534bbf0249241ce681aafd8e6d4bc4306dcb2`  
		Last Modified: Tue, 14 May 2024 03:06:01 GMT  
		Size: 197.0 MB (197014118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3124fb5fe8cc7612884412dbbc1630d16f9aedf27c6052241b1751b7ad7fa14f`  
		Last Modified: Tue, 14 May 2024 06:17:05 GMT  
		Size: 4.2 KB (4197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf0c111ae42ed820a353a8840a2998c117cce6f7dbd52346f19093c0e1b38847`  
		Last Modified: Tue, 14 May 2024 06:18:44 GMT  
		Size: 49.7 MB (49716886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2abac14e0ec30cca36e43dd2c5b0e2924e0993c6f813f52a959651d79bc8600`  
		Last Modified: Tue, 14 May 2024 06:18:36 GMT  
		Size: 1.2 MB (1247096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169d84d2ff1d25974e179d91c9fbef4a312e9e8597f593a32b053c4f9a5d6367`  
		Last Modified: Tue, 14 May 2024 06:18:36 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:21-bullseye` - linux; arm variant v7

```console
$ docker pull node@sha256:9b231af6215c46a992fe85583840251704b4a4deec0e8724612dba05508778c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.9 MB (329862698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1936bd1a8dfbbfaa2f7b13a4fa378a56d8024405dd5ef7421edea6b2f9274585`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Tue, 14 May 2024 01:08:54 GMT
ADD file:e0e66bc918a84b9ec6caaae1380270276be179a5864b6234a18c001b3e94f855 in / 
# Tue, 14 May 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:37:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:37:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:38:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 14 May 2024 01:54:09 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Tue, 14 May 2024 01:56:44 GMT
ENV NODE_VERSION=21.7.3
# Tue, 14 May 2024 01:57:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Tue, 14 May 2024 01:57:07 GMT
ENV YARN_VERSION=1.22.19
# Tue, 14 May 2024 01:57:10 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/*
# Tue, 14 May 2024 01:57:10 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Tue, 14 May 2024 01:57:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 May 2024 01:57:10 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:ebc97a184476667a6a83dfc0759e34e05bc66d258ece39a010b6273982b4dc57`  
		Last Modified: Tue, 14 May 2024 01:13:05 GMT  
		Size: 50.3 MB (50256445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f46483bc34de5be97fb9e8af88e9cf41c36db4eecccc529cc7904ee92a32f72`  
		Last Modified: Tue, 14 May 2024 01:48:02 GMT  
		Size: 14.9 MB (14880295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d6f4b9983a8ee98e2432d49e727c6278cadb8efecf5ab79268999b8d08c984`  
		Last Modified: Tue, 14 May 2024 01:48:20 GMT  
		Size: 50.4 MB (50359447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b75020cd82336d3062778f825587beaa94285a03f3e7cdf28704af4743b57a`  
		Last Modified: Tue, 14 May 2024 01:48:55 GMT  
		Size: 167.5 MB (167476287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:658f8c86317069ff89a24496062edcc690c425f8852d91908180589d78cf5e85`  
		Last Modified: Tue, 14 May 2024 02:07:42 GMT  
		Size: 4.2 KB (4185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dfb61be11f2c878141189e78768ea5a2169ba379bad7aba2118696b8f61785`  
		Last Modified: Tue, 14 May 2024 02:09:30 GMT  
		Size: 45.6 MB (45638494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d706052d0a4243ca3c455af4b701511301099b931b26be636b5601d5d12d3e96`  
		Last Modified: Tue, 14 May 2024 02:09:21 GMT  
		Size: 1.2 MB (1247095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a76bba0c83d45f59875cedfdfd95aded7f09e027b84c678fafe168dfea982cfb`  
		Last Modified: Tue, 14 May 2024 02:09:21 GMT  
		Size: 450.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:21-bullseye` - linux; arm64 variant v8

```console
$ docker pull node@sha256:3974ee5d5ac93508e87c38cf5c27ce056cd4ab65d30c1ae662bab272dde1833b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.9 MB (364923498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f625ef4eeda887a0649bfae7b8911e83eae60d55421d8f363e29016b205a723`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 24 Apr 2024 04:10:46 GMT
ADD file:3ebbb50438ec23ebe0c880a5421d505922771b7bd4202b5c8f839702dd726036 in / 
# Wed, 24 Apr 2024 04:10:46 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:33:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:33:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 08:34:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 15:32:45 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 24 Apr 2024 15:32:45 GMT
ENV NODE_VERSION=21.7.3
# Wed, 24 Apr 2024 15:33:01 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 24 Apr 2024 15:33:01 GMT
ENV YARN_VERSION=1.22.19
# Wed, 24 Apr 2024 15:33:04 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/*
# Wed, 24 Apr 2024 15:33:04 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 24 Apr 2024 15:33:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 15:33:05 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:64d502aff46d2ed56e6228994304818b354d02b13d6122492c5d3e0886c92897`  
		Last Modified: Wed, 24 Apr 2024 04:14:26 GMT  
		Size: 53.7 MB (53739959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33008ff0928e624ce22cedd5d004edd66b80372bfd1223e8900206330213ee34`  
		Last Modified: Wed, 24 Apr 2024 08:42:31 GMT  
		Size: 15.8 MB (15750623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36972983386f768dbeff5de37af34ed4e2f59541b2e3c43575f29758c3591923`  
		Last Modified: Wed, 24 Apr 2024 08:42:45 GMT  
		Size: 54.7 MB (54696233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3224178d7041e10ec03b66358ce4ba6bb5aeaf26b593f3e8672ca38f7b70769e`  
		Last Modified: Wed, 24 Apr 2024 08:43:09 GMT  
		Size: 189.9 MB (189912094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf881851f912a12efe98cb45a879f7bef20bdc3c4b09c61e53aef85e30f986c`  
		Last Modified: Wed, 24 Apr 2024 15:38:43 GMT  
		Size: 4.2 KB (4212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a774c14e78cd2249c35fd0b229be441bc1f4602832c1104c18504630c16b9c4`  
		Last Modified: Wed, 24 Apr 2024 15:38:50 GMT  
		Size: 49.6 MB (49572834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d924d7bd0c36480a6bff729dddaa522ed05f2c2af7c5103800304a50eb145b2a`  
		Last Modified: Wed, 24 Apr 2024 15:38:43 GMT  
		Size: 1.2 MB (1247092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70af08ecf172d6a9846b88d84060e1ca6767128b7a8837b7f750c558abfa734`  
		Last Modified: Wed, 24 Apr 2024 15:38:43 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:21-bullseye` - linux; ppc64le

```console
$ docker pull node@sha256:d6ea5843ff7276b2e283749ce2c6ad90bbd6a183d13c660899ca99efef538d32
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384439159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdeaf4dd3e8a7e2b089166e50bc6647cabe675bc7bdaecfb328d4c30520c15e4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:25 GMT
ADD file:f5283c61db1fea68c9d742ae60d7572775bfb46d2e8a92659edbd0c98e083a93 in / 
# Wed, 24 Apr 2024 03:21:30 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 03:57:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 03:58:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:04:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 06:01:54 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 24 Apr 2024 06:01:55 GMT
ENV NODE_VERSION=21.7.3
# Wed, 24 Apr 2024 06:02:15 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 24 Apr 2024 06:02:19 GMT
ENV YARN_VERSION=1.22.19
# Wed, 24 Apr 2024 06:02:24 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/*
# Wed, 24 Apr 2024 06:02:25 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 24 Apr 2024 06:02:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 06:02:26 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:aac3759e46343ae5d9b035355707bd07abf04ff80e3d29e689ea89cc78633190`  
		Last Modified: Wed, 24 Apr 2024 03:27:06 GMT  
		Size: 59.0 MB (58968197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc915aadd544630a28ea807628347805a6b8bc6f250feae34a46f66ac5228d3`  
		Last Modified: Wed, 24 Apr 2024 04:24:14 GMT  
		Size: 16.8 MB (16767223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87809a577847ee55cd1298464ee16a72985d1700dcf4e546db6fca794086d7c7`  
		Last Modified: Wed, 24 Apr 2024 04:24:32 GMT  
		Size: 58.9 MB (58873993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b19380d6722f8bacf55a08edef5ab2bef7d748909aa0109770daf96177909f5`  
		Last Modified: Wed, 24 Apr 2024 04:25:08 GMT  
		Size: 196.3 MB (196343705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a94009ba3d1d6237f951e4e40328458755353bc5271758ec386b0ecf55d7731f`  
		Last Modified: Wed, 24 Apr 2024 06:16:27 GMT  
		Size: 4.2 KB (4201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef5b0aec6dcadecb5cb9f5420759af2894f0cc0ba3df47b6a30b3a504ef937c`  
		Last Modified: Wed, 24 Apr 2024 06:16:36 GMT  
		Size: 52.2 MB (52234287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79d3b48f94f44ebebb6e849365e71f32a8e40a870b3997ca18ca270ba1004771`  
		Last Modified: Wed, 24 Apr 2024 06:16:27 GMT  
		Size: 1.2 MB (1247102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44ecfd9d80e8cb5b62040d1fe6d89c2b5fc770fbb41ebc348a24bb9f578e251b`  
		Last Modified: Wed, 24 Apr 2024 06:16:27 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:21-bullseye` - linux; s390x

```console
$ docker pull node@sha256:230e4eb9240e60306e920d7b34dfb4407ce9569fa1f355a2681272e1860bf11b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.8 MB (346828148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a16b49b7ac4d0daa74c032bebc45427602bdd2e09a0e9fa4bf88e0a02281e86e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 24 Apr 2024 03:43:33 GMT
ADD file:e0a1fc1de1477cea6fe41bdd15378013c680928cad3988dd16926cc1562c775e in / 
# Wed, 24 Apr 2024 03:43:38 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:12:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:13:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 07:03:44 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 24 Apr 2024 07:03:44 GMT
ENV NODE_VERSION=21.7.3
# Wed, 24 Apr 2024 07:04:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0     CC68F5A3106FF448322E48ED27F5E38D5B0A215F   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 24 Apr 2024 07:04:09 GMT
ENV YARN_VERSION=1.22.19
# Wed, 24 Apr 2024 07:04:13 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version   && rm -rf /tmp/*
# Wed, 24 Apr 2024 07:04:13 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 24 Apr 2024 07:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Apr 2024 07:04:14 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:b57a10abb081ff40e5bb34246c3875a71b8d258f767c4f8384d7054b1bc42725`  
		Last Modified: Wed, 24 Apr 2024 03:49:31 GMT  
		Size: 53.3 MB (53337419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:293ed92794c4710c20ea615a0e07fe947837768482be7bcd9d1fccb335072a92`  
		Last Modified: Wed, 24 Apr 2024 04:24:03 GMT  
		Size: 15.6 MB (15642846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede0318d2197701d71929fa882d8d64bdc0c65ee6bc9abd4bd4063694d92acb7`  
		Last Modified: Wed, 24 Apr 2024 04:24:17 GMT  
		Size: 54.1 MB (54076626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c3f9b4c72abaa52996d64ffc8754f8500b075a8a677c0fe59c310548e9af5c`  
		Last Modified: Wed, 24 Apr 2024 04:24:43 GMT  
		Size: 173.0 MB (172994116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5714d678a42ce1d7e25a9e90d90c54b8492ce16268969ca2f149c6b4de88e93`  
		Last Modified: Wed, 24 Apr 2024 07:15:39 GMT  
		Size: 4.2 KB (4212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b593f80eb1c6618232f481c91fe9ad6f0a676c4bc73e6db981b16c0c703941`  
		Last Modified: Wed, 24 Apr 2024 07:15:47 GMT  
		Size: 49.5 MB (49525378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccadc1ca721bfe45db035476ef68c249a065eacb5f49b8a8677db2ecdcaad6e5`  
		Last Modified: Wed, 24 Apr 2024 07:15:40 GMT  
		Size: 1.2 MB (1247099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c9b19f1758cdf1a6144a57e14886bad308280a8b0ba91774571e2843939b68`  
		Last Modified: Wed, 24 Apr 2024 07:15:40 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
