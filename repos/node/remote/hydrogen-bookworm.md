## `node:hydrogen-bookworm`

```console
$ docker pull node@sha256:56ed84097b42a0aa7c218bb7970add8efa4407750a576d8a8e4a5726002ca3b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `node:hydrogen-bookworm` - linux; amd64

```console
$ docker pull node@sha256:3414e5030433c00ee2431b136cec19bb10f6d938d5531c0674609584e649fbb2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 MB (397136188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acc6f84723fca4dff3fdbdc224ebc04d8bae0964af556c176e373687664d076a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 22:35:05 GMT
ADD file:6d9e71f0d3afb0b288cf2c06425795d528a142872692072ab1cd1ad275b67d1f in / 
# Wed, 31 Jan 2024 22:35:06 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:22:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:22:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:23:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 01:27:48 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 01 Feb 2024 01:33:41 GMT
ENV NODE_VERSION=18.19.0
# Thu, 01 Feb 2024 01:33:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Thu, 01 Feb 2024 01:33:56 GMT
ENV YARN_VERSION=1.22.19
# Thu, 01 Feb 2024 01:34:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Thu, 01 Feb 2024 01:34:00 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:34:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 01:34:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:6a299ae9cfd996c1149a699d36cdaa76fa332c8e9d66d6678fa9a231d9ead04c`  
		Last Modified: Wed, 31 Jan 2024 22:39:27 GMT  
		Size: 49.6 MB (49583754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e08e8703b2fb5e50153f792f3192087d26970d262806b397049d61b9a14b3af5`  
		Last Modified: Wed, 31 Jan 2024 23:32:17 GMT  
		Size: 24.1 MB (24050083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68e92d11b04ec0fe48e60d59964704aca234084f87af5d1a068c49456b37fe3d`  
		Last Modified: Wed, 31 Jan 2024 23:32:37 GMT  
		Size: 64.1 MB (64142328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9fe7fef9befda786bc8e1dd1ae42ffd8b9c37a4cce3c433e65ebb890cb1672`  
		Last Modified: Wed, 31 Jan 2024 23:33:14 GMT  
		Size: 211.1 MB (211111518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278d467c182fb935287ed6f4be3d44f8ac2714264bcb58b883d0cd25754f75d6`  
		Last Modified: Thu, 01 Feb 2024 01:38:09 GMT  
		Size: 3.4 KB (3371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc545d3635f75d17dc6806aa9003687dcf7d15010c26d7ea8dc75a33cae110a3`  
		Last Modified: Thu, 01 Feb 2024 01:42:49 GMT  
		Size: 46.0 MB (46036064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e162bf5ca48d3403b5ae00884fdc0136b3d433c80d2f32bd1f6c7f1c24ee07`  
		Last Modified: Thu, 01 Feb 2024 01:42:42 GMT  
		Size: 2.2 MB (2208616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd653604fd2633f6c5a52d254971956363556775f6489bda1fba9793999f9981`  
		Last Modified: Thu, 01 Feb 2024 01:42:42 GMT  
		Size: 454.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:hydrogen-bookworm` - linux; arm variant v7

```console
$ docker pull node@sha256:34fb9433d0a97fa06a3f01e2857c49eb37bb506fa44a9e7578f89939c436b6cd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.4 MB (346418587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c5670f8b58e654b91536f32b70915743d2a6e37a5de2e4ab93d13ecb86d02a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:09 GMT
ADD file:24186d75daba80fe802230517bbb6b4e9d6c695398d1db98108b4487d27ebb43 in / 
# Wed, 31 Jan 2024 22:44:09 GMT
CMD ["bash"]
# Thu, 01 Feb 2024 02:47:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:47:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 02:48:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 06:36:36 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 01 Feb 2024 06:43:53 GMT
ENV NODE_VERSION=18.19.0
# Thu, 01 Feb 2024 06:44:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Thu, 01 Feb 2024 06:44:14 GMT
ENV YARN_VERSION=1.22.19
# Thu, 01 Feb 2024 06:44:20 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Thu, 01 Feb 2024 06:44:20 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 01 Feb 2024 06:44:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 06:44:21 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:af02191d26cb0ab470ac42e81c677a72e87ee39e67a36576e102fffc8b1de4a7`  
		Last Modified: Wed, 31 Jan 2024 22:48:27 GMT  
		Size: 45.2 MB (45177992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5dbfdb18fe3f9c4fd9d347eb380df7b3080c079f6bffef53d6d588fa3b49bf`  
		Last Modified: Thu, 01 Feb 2024 02:58:27 GMT  
		Size: 22.0 MB (21953682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2114ad3bcb8a20c51922836cabcbf31c1cc36bf285577a204f4dac5b756e1cc`  
		Last Modified: Thu, 01 Feb 2024 02:58:49 GMT  
		Size: 59.2 MB (59216669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d88bc19189eb4f1105881142f65d20f20c62599e816c26cb5fab6c266f89b80`  
		Last Modified: Thu, 01 Feb 2024 02:59:25 GMT  
		Size: 175.1 MB (175081910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dc5adb323c5ead4e03729bcdb0c1a9715ed5e506c4cb063e24133e3f4f315d`  
		Last Modified: Thu, 01 Feb 2024 06:46:36 GMT  
		Size: 3.4 KB (3371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36481df1cb4734cd29dbe8936f1e881c86aa1c5ab5ca697aa0a465e13750a3fe`  
		Last Modified: Thu, 01 Feb 2024 06:48:59 GMT  
		Size: 42.8 MB (42783542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287a3f7ae4de25e1885ac78f3a849f8db0a1e6926ede7e203342ca3ff70a38fa`  
		Last Modified: Thu, 01 Feb 2024 06:48:50 GMT  
		Size: 2.2 MB (2200969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6971c5ca340af5adea1e4e50a71dd648a6840063b0e8dcbeee47727a5b08b7b0`  
		Last Modified: Thu, 01 Feb 2024 06:48:50 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:hydrogen-bookworm` - linux; arm64 variant v8

```console
$ docker pull node@sha256:7acb1244ae2e48325160574afc4069e1c88f96ab66ac27ffc752f2e5b9dcbd00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.0 MB (388030482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ee7ef8ce2802bf66a8850fe799d4223bb6c72edb1a72d28f7c2af4b37eaaba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 22:44:15 GMT
ADD file:8bc7f537dd3dc4b92ec9006080fd563cc79205ee1ec3f456d03e869125a5bc21 in / 
# Wed, 31 Jan 2024 22:44:15 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:42:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:43:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:44:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 07:28:47 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 01 Feb 2024 07:34:20 GMT
ENV NODE_VERSION=18.19.0
# Thu, 01 Feb 2024 07:34:35 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Thu, 01 Feb 2024 07:34:35 GMT
ENV YARN_VERSION=1.22.19
# Thu, 01 Feb 2024 07:34:39 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Thu, 01 Feb 2024 07:34:39 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 01 Feb 2024 07:34:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 07:34:39 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:66932e2b787d33a94ee3eb8b489be6e6838b29f5c1d732262da306da9b1f2eed`  
		Last Modified: Wed, 31 Jan 2024 22:47:40 GMT  
		Size: 49.6 MB (49615296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afa7e263db1a3a05a9f31906dee83c0ef41151669759a3362e724b2765fd66f`  
		Last Modified: Wed, 31 Jan 2024 23:52:05 GMT  
		Size: 23.6 MB (23586448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c812910e5e62436c8483e793d1956d1c70bcf42d20d5f0885ddafbe0ba124459`  
		Last Modified: Wed, 31 Jan 2024 23:52:23 GMT  
		Size: 64.0 MB (63994808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e4299bb649220caaf79678771b6f57f97122a0a5b638fff83400a663d282b3`  
		Last Modified: Wed, 31 Jan 2024 23:52:55 GMT  
		Size: 202.5 MB (202505949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb7a03a532775c938026778d5433751da3b3c9c49c6e4e91224f9b4697de1f05`  
		Last Modified: Thu, 01 Feb 2024 07:41:34 GMT  
		Size: 3.4 KB (3375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980aaf67aefdc51e369eadb09c307871b4c99bc05e461be178c1137eae5543e2`  
		Last Modified: Thu, 01 Feb 2024 07:45:52 GMT  
		Size: 46.1 MB (46115351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5edb64497008395d085fc639e21dc3411ba039bda2531e6033908fa6b71ae460`  
		Last Modified: Thu, 01 Feb 2024 07:45:47 GMT  
		Size: 2.2 MB (2208804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:578557c910ff6738d7d41d0f04dc2f05eca43117af53d5907afc5c37e2d9f5ee`  
		Last Modified: Thu, 01 Feb 2024 07:45:47 GMT  
		Size: 451.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:hydrogen-bookworm` - linux; ppc64le

```console
$ docker pull node@sha256:380658c92ef42d5120c5ed39c3e18f92c1e75f3de478df8590157ef1acf87238
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.4 MB (413371726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ebf3f637d483605f5ab506be7d243790d2c2751c501812bf7a946f9199264d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Wed, 31 Jan 2024 22:29:20 GMT
ADD file:e856dcd026d65beec0f1b0cf2e26a377ae06e730603870e5f78290fc8c78c3fd in / 
# Wed, 31 Jan 2024 22:29:23 GMT
CMD ["bash"]
# Wed, 31 Jan 2024 23:26:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:27:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 31 Jan 2024 23:30:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Feb 2024 00:48:28 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Thu, 01 Feb 2024 01:00:34 GMT
ENV NODE_VERSION=18.19.0
# Thu, 01 Feb 2024 01:00:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Thu, 01 Feb 2024 01:00:57 GMT
ENV YARN_VERSION=1.22.19
# Thu, 01 Feb 2024 01:01:02 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Thu, 01 Feb 2024 01:01:03 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Thu, 01 Feb 2024 01:01:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 01 Feb 2024 01:01:03 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:7579f5ed16e0992350eed26d915c99451987a3b2cfb96fee25d4b65b8d8c2aac`  
		Last Modified: Wed, 31 Jan 2024 22:33:56 GMT  
		Size: 53.6 MB (53578470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ec8e5c0fa7f8ec08ca2f938f40e14f359ca71996729690f50368e0ff622ad3`  
		Last Modified: Wed, 31 Jan 2024 23:47:36 GMT  
		Size: 25.7 MB (25699520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa97c27b10146b73ca93631d629172e2bb41f6535ff6306e0fb5b0c9b4a71263`  
		Last Modified: Wed, 31 Jan 2024 23:48:00 GMT  
		Size: 69.6 MB (69584038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbd5edc8501c8ac210226c299c64633308c37f4d32ef7d6bcea2583f769270f0`  
		Last Modified: Wed, 31 Jan 2024 23:48:41 GMT  
		Size: 214.1 MB (214143709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8b6d4c52cde1903b0b353c8bcdc53dc33360f784eddabde2ef991fad1855fd`  
		Last Modified: Thu, 01 Feb 2024 01:06:17 GMT  
		Size: 3.4 KB (3369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af619792e1cd0459e189cd7a71dae83885a871614ac4f56c00391865a29cf64`  
		Last Modified: Thu, 01 Feb 2024 01:10:47 GMT  
		Size: 48.2 MB (48153367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9348a91b503771b8c85a5bdf8ea0926956bfdd202dda203b62f63c7c51fa5dd0`  
		Last Modified: Thu, 01 Feb 2024 01:10:39 GMT  
		Size: 2.2 MB (2208801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b44d2a7c0edbb7a38a8c81634ee6abd3f6fc0d3116f77429f4a8fe611613846`  
		Last Modified: Thu, 01 Feb 2024 01:10:39 GMT  
		Size: 452.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:hydrogen-bookworm` - linux; s390x

```console
$ docker pull node@sha256:2c8a057e32e1786fec9deb3f3a4db06e7441ff5eaead8b0920ff1606984dd929
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **366.3 MB (366334710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eab2b14ed5403a9a6a3ffa7177e6ca04b8c3d646ca5b9c30e0167c24e2196e3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Thu, 11 Jan 2024 01:44:46 GMT
ADD file:b52927273f91d79b0b493ff5507714cde656c5d76433c6c5b3dafd358f4ed7cd in / 
# Thu, 11 Jan 2024 01:44:50 GMT
CMD ["bash"]
# Thu, 11 Jan 2024 02:09:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:11:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 03:14:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Jan 2024 06:20:23 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 17 Jan 2024 06:37:41 GMT
ENV NODE_VERSION=18.19.0
# Wed, 17 Jan 2024 06:37:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && export GNUPGHOME="$(mktemp -d)"   && set -ex   && for key in     4ED778F539E3634C779C87C6D7062848A1AB005C     141F07595B7B3FFE74309A937405533BE57C7D57     74F12602B6F1C4E913FAA37AD3A89613643B6201     DD792F5973C6DE52C432CBDAC77ABFA00DDBF2B7     61FC681DFB92A079F1685E77973F295594EC4689     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     890C08DB8579162FEE0DF9DB8BEAB4DFCF555EF4     C82FA3AE1CBEDC6BE46B9360C43CEC45C17AB93C     108F52B48DB57BB0CC439B2997B01419BD92F80A     A363A499291CBBC940DD62E41F10027AF002F8B0   ; do       gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||       gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs   && node --version   && npm --version
# Wed, 17 Jan 2024 06:37:57 GMT
ENV YARN_VERSION=1.22.19
# Wed, 17 Jan 2024 06:38:00 GMT
RUN set -ex   && export GNUPGHOME="$(mktemp -d)"   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$key" ||     gpg --batch --keyserver keyserver.ubuntu.com --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && gpgconf --kill all   && rm -rf "$GNUPGHOME"   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && yarn --version
# Wed, 17 Jan 2024 06:38:00 GMT
COPY file:4d192565a7220e135cab6c77fbc1c73211b69f3d9fb37e62857b2c6eb9363d51 in /usr/local/bin/ 
# Wed, 17 Jan 2024 06:38:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 17 Jan 2024 06:38:00 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:d28727deb22d156e281ef621e3fd48900f453abc05f099f88bfed20e0f5861b3`  
		Last Modified: Thu, 11 Jan 2024 01:50:35 GMT  
		Size: 47.9 MB (47917872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdcda5a31401318d38b94cd36426844d1953c0561252561b5205f9b95c442bac`  
		Last Modified: Thu, 11 Jan 2024 02:21:00 GMT  
		Size: 24.0 MB (24043257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ed6bc65286743fe499d9acd1b031ec55623990da97c0b8c5a36e90e5efb4f45`  
		Last Modified: Wed, 17 Jan 2024 04:03:37 GMT  
		Size: 63.1 MB (63126558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574246225f84293d825d33ddedfe60c69bf6ec125be2de566f07c54ea8e0e2f2`  
		Last Modified: Wed, 17 Jan 2024 04:04:05 GMT  
		Size: 183.1 MB (183143910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ed4171a51d1470c3077e8b528d817bf6430a57a23d31523fbca2f4fcc536c7`  
		Last Modified: Wed, 17 Jan 2024 06:44:18 GMT  
		Size: 3.4 KB (3369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f46c8c08952f0dbf271325c6c791d4df097fc59889a881ab9db236db906c77`  
		Last Modified: Wed, 17 Jan 2024 06:46:09 GMT  
		Size: 45.9 MB (45888858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35777e61eacddf68d9512f094f2f5082a36896b9ec03170c7ffe60f053af9b9`  
		Last Modified: Wed, 17 Jan 2024 06:46:03 GMT  
		Size: 2.2 MB (2210433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad6212b4384fbe9012c832b27fb61f1cbfdbe456ade87b71d371faf05b927a93`  
		Last Modified: Wed, 17 Jan 2024 06:46:02 GMT  
		Size: 453.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
