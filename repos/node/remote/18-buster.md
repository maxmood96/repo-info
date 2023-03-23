## `node:18-buster`

```console
$ docker pull node@sha256:bac7af3648f362ecbc3855de0fb6ff1abc92c0e2e767deee0f36c8437f325f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `node:18-buster` - linux; amd64

```console
$ docker pull node@sha256:64182c2ed72616115b76416546223ea450e6e734fa6045b038070cd2e41c3d47
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359893901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96228cef9efee33a504e872129a655e557cd52f09ade18a9fcabef6f6ed15c88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:38 GMT
ADD file:f5e6e6cbfbb36f50f49f06fbac953a130383acb67a1c5e9979441f1915b1077d in / 
# Thu, 23 Mar 2023 01:30:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:02:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:03:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 06:03:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:04:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 15:41:13 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 23 Mar 2023 15:43:24 GMT
ENV NODE_VERSION=18.15.0
# Thu, 23 Mar 2023 15:43:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Thu, 23 Mar 2023 15:43:39 GMT
ENV YARN_VERSION=1.22.19
# Thu, 23 Mar 2023 15:43:41 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Thu, 23 Mar 2023 15:43:42 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 23 Mar 2023 15:43:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Mar 2023 15:43:42 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:4e2befb7f5d18aa27b3619ddf1b93607e62ca82d0c627557537c149893346d86`  
		Last Modified: Thu, 23 Mar 2023 01:34:40 GMT  
		Size: 50.4 MB (50448639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792af667f62688dbef1f3ffeeca2daa6d448a62b6cacd604f1c4fc043d6cc2a6`  
		Last Modified: Thu, 23 Mar 2023 06:09:02 GMT  
		Size: 7.9 MB (7863352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e37868ebf669334a2dbdb206ac7b84d8f8d184a40dfb8c9bc501b29cda12548`  
		Last Modified: Thu, 23 Mar 2023 06:09:02 GMT  
		Size: 10.0 MB (10001388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591fe17e35ddac86d63495a7708b07af369e0d67d8742880f1e73cf1a205e028`  
		Last Modified: Thu, 23 Mar 2023 06:09:16 GMT  
		Size: 51.9 MB (51874529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9cba6e3073a1f2eac2d50c107bba6dbb76de0325854a3a0e7c6f52ae8fc5521`  
		Last Modified: Thu, 23 Mar 2023 06:09:46 GMT  
		Size: 191.8 MB (191848818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d54aff43b9d5a82025cbae68c26151d48ce3e061018e8547a567ee0de7ca4a3`  
		Last Modified: Thu, 23 Mar 2023 15:50:35 GMT  
		Size: 4.2 KB (4197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94704c6ed815823f622e39a8bc00ef72a7e1a713fe12cd3d5cdbf7fb9b6d6f6b`  
		Last Modified: Thu, 23 Mar 2023 15:52:30 GMT  
		Size: 45.6 MB (45576271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a29537f8b685f7b99bd5d915573a832f2d456dc95f3c057f59ae636361b81cc`  
		Last Modified: Thu, 23 Mar 2023 15:52:23 GMT  
		Size: 2.3 MB (2276258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33653a0104b5dba8c845d9ad5328567754777cfeabc6b3a60078d9f4c9a285ca`  
		Last Modified: Thu, 23 Mar 2023 15:52:23 GMT  
		Size: 449.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:18-buster` - linux; arm variant v7

```console
$ docker pull node@sha256:c8ea4608ffa37fa5b6c4007903a30b0f32477b4421bf11545d32ffcb08f6b57e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322380211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a7e0333304ef93ca448f708e2e1e115df578ac817051d80758d850dc62490a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 01 Mar 2023 01:58:03 GMT
ADD file:28e7414281fcd12661d43cccdf7062bf4aa15641f986cae3aa3260fcb8e16bb5 in / 
# Wed, 01 Mar 2023 01:58:03 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:34:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:34:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:34:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:36:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 18:29:52 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 08 Mar 2023 21:35:57 GMT
ENV NODE_VERSION=18.15.0
# Wed, 08 Mar 2023 21:36:17 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 08 Mar 2023 21:36:18 GMT
ENV YARN_VERSION=1.22.19
# Wed, 08 Mar 2023 21:36:33 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 08 Mar 2023 21:36:33 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 08 Mar 2023 21:36:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Mar 2023 21:36:34 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:4ba30d485dd0583b3079a70184a97c458599a0629e661b1382394653cb802242`  
		Last Modified: Wed, 01 Mar 2023 02:03:25 GMT  
		Size: 45.9 MB (45916077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f5b3ed640e906ad20c2a86568f52c60a48e1d82e4654d3378280f572737f7c1`  
		Last Modified: Wed, 01 Mar 2023 03:10:25 GMT  
		Size: 7.2 MB (7152340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:028b21e39d17f6632c7b82f0c900d32b50233b13940a7a60009782a6abc32cdd`  
		Last Modified: Wed, 01 Mar 2023 03:10:25 GMT  
		Size: 9.3 MB (9349019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35297b6d570293c7581e727c51353a6eb15d3b2f7bdaf391595c28c2a8d4fc6`  
		Last Modified: Wed, 01 Mar 2023 03:10:43 GMT  
		Size: 47.4 MB (47396639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db985543ef8399c92c217abd234865cfb8fc38d73e04bede21a4921385745eae`  
		Last Modified: Wed, 01 Mar 2023 03:11:15 GMT  
		Size: 168.1 MB (168095959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c9e8f2ae456c5d15ef6a4aab25af48c01e22cbc96f4273809e42a34540c490`  
		Last Modified: Wed, 01 Mar 2023 20:49:16 GMT  
		Size: 4.2 KB (4190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b068c8e40bb7bf64c5d98845807d80619b0e480410d51a654275979104d49f61`  
		Last Modified: Wed, 08 Mar 2023 21:49:06 GMT  
		Size: 42.2 MB (42198267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5d4ec00e7a23c5086484d73cd4f87b969fd5e619c08a13d8fa4f6d00704faf8`  
		Last Modified: Wed, 08 Mar 2023 21:48:57 GMT  
		Size: 2.3 MB (2267266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c63c8298bb5fb5beb8f0eb639fc33d36fd1258a2e4f711826ea9d562fb2d7e`  
		Last Modified: Wed, 08 Mar 2023 21:48:56 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:18-buster` - linux; arm64 variant v8

```console
$ docker pull node@sha256:26f3aa710f695016f94bda8abbf612ac178ac28899f55857d61f9abbc976e028
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.5 MB (350541648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c70c1891b7d8e6544a2b2a8ec442f6ac661a49a22a525da688b038d1deea098`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:16 GMT
ADD file:35dd833b036748f887e8224e9c5f09846aa5d1d6e1798d12a6355c28e0a087d3 in / 
# Thu, 23 Mar 2023 00:45:16 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:12:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:12:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 07:12:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:14:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 16:02:19 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 23 Mar 2023 16:03:05 GMT
ENV NODE_VERSION=18.15.0
# Thu, 23 Mar 2023 16:03:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Thu, 23 Mar 2023 16:03:19 GMT
ENV YARN_VERSION=1.22.19
# Thu, 23 Mar 2023 16:03:22 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Thu, 23 Mar 2023 16:03:22 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 23 Mar 2023 16:03:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Mar 2023 16:03:22 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6a9fffb8d1cb480140dc56a24c58a5d1a284109cd8a640a3719bcda5963d1298`  
		Last Modified: Thu, 23 Mar 2023 00:48:25 GMT  
		Size: 49.2 MB (49239721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f926b3d11ccb48534d760b7e8ccd49db3841835d1c101a700f3683415d6c24de`  
		Last Modified: Thu, 23 Mar 2023 07:18:02 GMT  
		Size: 7.7 MB (7732152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05517ad1eaae60c6b12d7f5c80a935abed6019e2ecc42b288c0861b582f9a739`  
		Last Modified: Thu, 23 Mar 2023 07:18:02 GMT  
		Size: 10.0 MB (10003634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77a3f42d13a5b883782685b1672575097e42f7318f89d26005d124c632de87f`  
		Last Modified: Thu, 23 Mar 2023 07:18:16 GMT  
		Size: 52.2 MB (52191970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbe3c7a3e88e7e5e9c98326e73439e845f5e2476de052c9cbf24ad2865dad263`  
		Last Modified: Thu, 23 Mar 2023 07:18:41 GMT  
		Size: 183.4 MB (183435104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a601d6810166a5de5755e4f4223558d34ad288562196773044a4d69cdb199b79`  
		Last Modified: Thu, 23 Mar 2023 16:06:24 GMT  
		Size: 4.2 KB (4210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:850ba51b07022750d4a5321b43a9ad72c3a18252648a8708913d89da87f9b7d1`  
		Last Modified: Thu, 23 Mar 2023 16:07:30 GMT  
		Size: 45.7 MB (45658122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:522795394f17d50ece777bca33d0e7cba73bb298ae88868dd20c3bfb7e4519f4`  
		Last Modified: Thu, 23 Mar 2023 16:07:24 GMT  
		Size: 2.3 MB (2276284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bbb2bb90969610fce2208a0020969c0d647684c22b9c81f06007b2d5c5cc831`  
		Last Modified: Thu, 23 Mar 2023 16:07:24 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
