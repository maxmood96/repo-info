## `node:lts`

```console
$ docker pull node@sha256:b49eb3c4aa70ec0182b0462beafb953304940c0f8bd25422f49d608918d98259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `node:lts` - linux; amd64

```console
$ docker pull node@sha256:8d9ab6d838d3930dba80803340a4d18867f9a1898cb338ac94f71ffc7c9f2002
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.3 MB (350287242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a73e56f893cf6284a6ad2be795dfe627da1b354e95befc61e49011a84e3f846`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:33 GMT
ADD file:8f7dc710e276f54a3a73d34b6b8fa261950a781d68ceb7401fa18dabc601c5a5 in / 
# Sat, 28 Dec 2019 04:23:34 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:58:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:38 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:59:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:00:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 23:32:56 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Wed, 08 Jan 2020 22:22:18 GMT
ENV NODE_VERSION=12.14.1
# Wed, 08 Jan 2020 22:22:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     77984A986EBC2AA786BC0F66B01FBB92821C587A     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     4ED778F539E3634C779C87C6D7062848A1AB005C     A48C2BEE680E841632CD4E44F07496B3EB3C1762     B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Wed, 08 Jan 2020 22:22:26 GMT
ENV YARN_VERSION=1.21.1
# Wed, 08 Jan 2020 22:22:29 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Wed, 08 Jan 2020 22:22:29 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Wed, 08 Jan 2020 22:22:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 08 Jan 2020 22:22:30 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:146bd6a886182fde06fbf747470b1c89814bc8ab1c96fdf1aef6107171959fe6`  
		Last Modified: Sat, 28 Dec 2019 04:28:25 GMT  
		Size: 45.4 MB (45380744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9935d0c62ace92b388be202275e222007d6cac10b9c1f2c1ea63af38c09ea7ab`  
		Last Modified: Sat, 28 Dec 2019 05:04:30 GMT  
		Size: 10.8 MB (10797221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db0efb86e80601b5bbdbb7c406426982c4202d339687c14c3941b364527e2249`  
		Last Modified: Sat, 28 Dec 2019 05:04:28 GMT  
		Size: 4.3 MB (4340114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705a4c4fd310b96bfb3d7928428e65f0d3f5bad0cd0bda1434aee1d89418468`  
		Last Modified: Sat, 28 Dec 2019 05:04:45 GMT  
		Size: 50.1 MB (50072671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c877b722db6f4d4297c21f07162d21fa6ac6f51d03360f75e24cfa3bcaefe57d`  
		Last Modified: Sat, 28 Dec 2019 05:05:38 GMT  
		Size: 214.8 MB (214840548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:645c20ec82147f2bdc182280ac02b60687cfac33c4231059051bbdcf60e31035`  
		Last Modified: Sat, 28 Dec 2019 23:47:04 GMT  
		Size: 4.2 KB (4163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72851fd0a9e4d1a6abd2d49075934ad9747981aedcbd97989d6aed74a58a826b`  
		Last Modified: Wed, 08 Jan 2020 22:33:30 GMT  
		Size: 23.5 MB (23450181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97d6cf2691b176b9c1f6886a570e34aa48309992956730c1cb07555707d5328`  
		Last Modified: Wed, 08 Jan 2020 22:33:25 GMT  
		Size: 1.4 MB (1401307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df0baa2324d9b232111906c0c1975660cf656703844e63906553c7549d358c6`  
		Last Modified: Wed, 08 Jan 2020 22:33:25 GMT  
		Size: 293.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:lts` - linux; arm variant v7

```console
$ docker pull node@sha256:1375423c8521137710b73dc767f5e28a32a124191ad143976a3f807635a19a9c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.4 MB (320414560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e48c4e0603263df1d06f7fd3798c33a78ddc0da0484722512fa5e2fc4a11f93`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Sat, 01 Feb 2020 17:04:08 GMT
ADD file:b7fc54d004d962f2cfb469a1aaa9e689e46dfa2554e0cf44c33981d688adc31b in / 
# Sat, 01 Feb 2020 17:04:09 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:18:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:18:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:19:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:23:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 02:35:52 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sun, 02 Feb 2020 02:48:55 GMT
ENV NODE_VERSION=12.14.1
# Sun, 02 Feb 2020 02:49:07 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     77984A986EBC2AA786BC0F66B01FBB92821C587A     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     4ED778F539E3634C779C87C6D7062848A1AB005C     A48C2BEE680E841632CD4E44F07496B3EB3C1762     B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sun, 02 Feb 2020 02:49:11 GMT
ENV YARN_VERSION=1.21.1
# Sun, 02 Feb 2020 02:49:17 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sun, 02 Feb 2020 02:49:18 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sun, 02 Feb 2020 02:49:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2020 02:49:21 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:cc3b08e804cce7e88d9df954b76be506569775afe9cf36316f2fa6c5c9bf3d5c`  
		Last Modified: Sat, 01 Feb 2020 17:11:13 GMT  
		Size: 42.1 MB (42108370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa649f4f33c2131c2969e49352ff247ebe5a62a62b83498c3580f883aa35621e`  
		Last Modified: Sat, 01 Feb 2020 18:31:10 GMT  
		Size: 9.5 MB (9498229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901c0c16dce9409a6a020f4b874b40fb3f7d302fe0b4e7a80a87a7cfbab7da04`  
		Last Modified: Sat, 01 Feb 2020 18:31:10 GMT  
		Size: 3.9 MB (3918766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715a264d83dc76a4a25b4110827c1ac6cc620c406edb6b2089cd1117aec271ed`  
		Last Modified: Sat, 01 Feb 2020 18:31:32 GMT  
		Size: 46.4 MB (46400091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854dcba3350bdff3f923ff69f2dec445f47ef5726d3d15bde4242c2ff122aabc`  
		Last Modified: Sat, 01 Feb 2020 18:32:28 GMT  
		Size: 195.5 MB (195523495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:301cb43662ca8c451e43bd09943103516bf3c7329dc5212d34e343ba8cb66ce7`  
		Last Modified: Sun, 02 Feb 2020 03:03:05 GMT  
		Size: 4.2 KB (4176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7aa67871a2a2cdb52df56fe343cec92d79bd64e50ab6eafdb1d64b55857e18b`  
		Last Modified: Sun, 02 Feb 2020 03:05:00 GMT  
		Size: 21.6 MB (21559780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:490fd513fe7036e244f94b57e72442e0f67402e36a4b31aec02357561b5c5d02`  
		Last Modified: Sun, 02 Feb 2020 03:04:52 GMT  
		Size: 1.4 MB (1401361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca22c2ac6529fa09e00c90e6ca6354ce816b8af93a4549a782e2064c86680d1f`  
		Last Modified: Sun, 02 Feb 2020 03:04:51 GMT  
		Size: 292.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:lts` - linux; arm64 variant v8

```console
$ docker pull node@sha256:087d22026971eb0b9d165b1e633512071072cf4141cbc22b3f132e0e0dbbf3f2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.1 MB (332091713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d27b1eb6808dfd8829a33260ffddd2175a2ef719186e873b54f3afb9f19a617`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:01 GMT
ADD file:1618e6474dbe6462a610ce7eed99f0bfd087ea37ddfc287bbd69def5c24ede47 in / 
# Sat, 01 Feb 2020 16:43:02 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:30:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:32:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 01:36:20 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sun, 02 Feb 2020 01:40:35 GMT
ENV NODE_VERSION=12.14.1
# Sun, 02 Feb 2020 01:40:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     77984A986EBC2AA786BC0F66B01FBB92821C587A     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     4ED778F539E3634C779C87C6D7062848A1AB005C     A48C2BEE680E841632CD4E44F07496B3EB3C1762     B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sun, 02 Feb 2020 01:40:48 GMT
ENV YARN_VERSION=1.21.1
# Sun, 02 Feb 2020 01:40:53 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sun, 02 Feb 2020 01:40:54 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sun, 02 Feb 2020 01:40:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2020 01:40:55 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:df3de44c7096ba135556a1e7044f9e1feee3ef713ab96f0416f71fe78422cbf6`  
		Last Modified: Sat, 01 Feb 2020 16:48:40 GMT  
		Size: 43.2 MB (43166749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf173a01baf7d45b479bb380ece219cbf0ea52178e9b8cdc5b87891759d1122`  
		Last Modified: Sat, 01 Feb 2020 17:39:19 GMT  
		Size: 9.7 MB (9748586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3392eac7bc27f3bd5fcb024413ca55ec4115c22da3e229567d5fc03cd4ff4e4`  
		Last Modified: Sat, 01 Feb 2020 17:39:18 GMT  
		Size: 4.1 MB (4094322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a82fc9ca296b095585ba7f3f6d83566428dbefcbfd284e242039aba97840b2`  
		Last Modified: Sat, 01 Feb 2020 17:39:40 GMT  
		Size: 48.0 MB (48024205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd9a981e1269e4bf23132efb6a90365b5d82020f20a2ae5252c2d7c3b9ad7f48`  
		Last Modified: Sat, 01 Feb 2020 17:40:34 GMT  
		Size: 202.2 MB (202233524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8666c72fbca9f7a68fbd224fe100c9a474db03243deee1d0189f89fc94d30`  
		Last Modified: Sun, 02 Feb 2020 01:50:49 GMT  
		Size: 4.2 KB (4197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620505a6c430b22895faf962f239f6ff437c0c83fd6b3214270d9da2311ef0cc`  
		Last Modified: Sun, 02 Feb 2020 01:52:24 GMT  
		Size: 23.4 MB (23418471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b658724dfb8f7bab9ebf5ae017f2915e562fbc5ae990f8d7dd4e36bb8e9413b`  
		Last Modified: Sun, 02 Feb 2020 01:52:16 GMT  
		Size: 1.4 MB (1401365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69853e4bf017be96aeb4a9a2b0215a02a69f5cd017c601fd15ae906e0724e5b1`  
		Last Modified: Sun, 02 Feb 2020 01:52:16 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:lts` - linux; ppc64le

```console
$ docker pull node@sha256:040901e66de8d997397ced64057d7b36d52ddf15d6e6fbf7dc050303eaf91bd7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345230681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed265d6f9a0f45f62a3657ce774cc62ed177caa77a4fea2ab18410d815bb4ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Sat, 01 Feb 2020 17:20:12 GMT
ADD file:ebcf4b112436fa7be8efa5ef204cc174c0d1af648c6ab4af968a71aa2ab2cf4a in / 
# Sat, 01 Feb 2020 17:20:16 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 19:04:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 19:05:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 19:06:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 19:13:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 08:23:56 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sun, 02 Feb 2020 08:32:07 GMT
ENV NODE_VERSION=12.14.1
# Sun, 02 Feb 2020 08:32:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     77984A986EBC2AA786BC0F66B01FBB92821C587A     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     4ED778F539E3634C779C87C6D7062848A1AB005C     A48C2BEE680E841632CD4E44F07496B3EB3C1762     B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sun, 02 Feb 2020 08:32:29 GMT
ENV YARN_VERSION=1.21.1
# Sun, 02 Feb 2020 08:32:39 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sun, 02 Feb 2020 08:32:41 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sun, 02 Feb 2020 08:32:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 02 Feb 2020 08:32:49 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:072f803f12e35b1a40604b6081cb448d46529e3eb1d453ebbf56850c211f5bdb`  
		Last Modified: Sat, 01 Feb 2020 17:30:44 GMT  
		Size: 45.7 MB (45652299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1738f3141f5288b7d088c111ef5c0250cf1779363648e4abd0a2fa786691279a`  
		Last Modified: Sat, 01 Feb 2020 19:25:20 GMT  
		Size: 10.0 MB (10002083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3a959eee44d8ac35abe99ef74efe938d0f14c75e8ba029451e3bb2f3c594206`  
		Last Modified: Sat, 01 Feb 2020 19:25:18 GMT  
		Size: 4.3 MB (4296690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c05296e9b4c4e064ac637742557d903aff58a97639760bb778595e90492a8f`  
		Last Modified: Sat, 01 Feb 2020 19:26:08 GMT  
		Size: 50.1 MB (50086371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0053e8ab1908886809e0b53ed05d1644123e096ed152bef227af4bdd63d04506`  
		Last Modified: Sat, 01 Feb 2020 19:28:13 GMT  
		Size: 210.5 MB (210480034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88cdf8eae5df094c97d6a1c8d001161105bda9fe2400fc6e6e5f8aacb39ceca`  
		Last Modified: Sun, 02 Feb 2020 08:50:05 GMT  
		Size: 4.2 KB (4198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9273fa45f886e500bfd0e7a5050b5bcc70e080ea372be7232128dde1754d20`  
		Last Modified: Sun, 02 Feb 2020 08:52:01 GMT  
		Size: 23.3 MB (23307350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf2b9e446df99762dbb53d623198dfb7d3e6192a8241fdf636e136d3ef2cf82`  
		Last Modified: Sun, 02 Feb 2020 08:51:55 GMT  
		Size: 1.4 MB (1401362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aed669ab37a323870b09f301e796278e92b03899742eb29bab64bb70b2d0073`  
		Last Modified: Sun, 02 Feb 2020 08:51:55 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `node:lts` - linux; s390x

```console
$ docker pull node@sha256:9eefb96b4032399cfe90adf955268d41633f2ae87f844addc62d0fd44f6dbfcf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342259406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34212d80abef01abb639ef9d105e2782bf0d0e60ee74ed4c82c32c120fd99a7c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["node"]`

```dockerfile
# Sat, 01 Feb 2020 16:43:43 GMT
ADD file:17af4834ca99365d5ecf14eb938572689bd3c3ad5fd8a88da12c4c3474975771 in / 
# Sat, 01 Feb 2020 16:43:45 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 18:00:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:00:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 18:00:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 18:01:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 21:05:38 GMT
RUN groupadd --gid 1000 node   && useradd --uid 1000 --gid node --shell /bin/bash --create-home node
# Sat, 01 Feb 2020 21:08:07 GMT
ENV NODE_VERSION=12.14.1
# Sat, 01 Feb 2020 21:08:14 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)"   && case "${dpkgArch##*-}" in     amd64) ARCH='x64';;     ppc64el) ARCH='ppc64le';;     s390x) ARCH='s390x';;     arm64) ARCH='arm64';;     armhf) ARCH='armv7l';;     i386) ARCH='x86';;     *) echo "unsupported architecture"; exit 1 ;;   esac   && set -ex   && for key in     94AE36675C464D64BAFA68DD7434390BDBE9B9C5     FD3A5288F042B6850C66B31F09FE44734EB7990E     71DCFD284A79C3B38668286BC97EC7A07EDE3FC1     DD8F2338BAE7501E3DD5AC78C273792F7D83545D     C4F0DFFF4E8C1A8236409D08E73BC641CC11F4C8     B9AE9905FFD7803F25714661B63B535A4C206CA9     77984A986EBC2AA786BC0F66B01FBB92821C587A     8FCCA13FEF1D0C2E91008E09770F7A9A5AE15600     4ED778F539E3634C779C87C6D7062848A1AB005C     A48C2BEE680E841632CD4E44F07496B3EB3C1762     B9E2F5981AA6E0CD28160D9FF13993A75599653C   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-$ARCH.tar.xz"   && curl -fsSLO --compressed "https://nodejs.org/dist/v$NODE_VERSION/SHASUMS256.txt.asc"   && gpg --batch --decrypt --output SHASUMS256.txt SHASUMS256.txt.asc   && grep " node-v$NODE_VERSION-linux-$ARCH.tar.xz\$" SHASUMS256.txt | sha256sum -c -   && tar -xJf "node-v$NODE_VERSION-linux-$ARCH.tar.xz" -C /usr/local --strip-components=1 --no-same-owner   && rm "node-v$NODE_VERSION-linux-$ARCH.tar.xz" SHASUMS256.txt.asc SHASUMS256.txt   && ln -s /usr/local/bin/node /usr/local/bin/nodejs
# Sat, 01 Feb 2020 21:08:15 GMT
ENV YARN_VERSION=1.21.1
# Sat, 01 Feb 2020 21:08:19 GMT
RUN set -ex   && for key in     6A010C5166006599AA17F08146C2130DFD2497F5   ; do     gpg --batch --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys "$key" ||     gpg --batch --keyserver hkp://ipv4.pool.sks-keyservers.net --recv-keys "$key" ||     gpg --batch --keyserver hkp://pgp.mit.edu:80 --recv-keys "$key" ;   done   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz"   && curl -fsSLO --compressed "https://yarnpkg.com/downloads/$YARN_VERSION/yarn-v$YARN_VERSION.tar.gz.asc"   && gpg --batch --verify yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz   && mkdir -p /opt   && tar -xzf yarn-v$YARN_VERSION.tar.gz -C /opt/   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarn /usr/local/bin/yarn   && ln -s /opt/yarn-v$YARN_VERSION/bin/yarnpkg /usr/local/bin/yarnpkg   && rm yarn-v$YARN_VERSION.tar.gz.asc yarn-v$YARN_VERSION.tar.gz
# Sat, 01 Feb 2020 21:08:19 GMT
COPY file:238737301d47304174e4d24f4def935b29b3069c03c72ae8de97d94624382fce in /usr/local/bin/ 
# Sat, 01 Feb 2020 21:08:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 01 Feb 2020 21:08:19 GMT
CMD ["node"]
```

-	Layers:
	-	`sha256:fb54e9d54b34d992a5c6582a6fe3836692cce3589a408748090bbb916a4cc63d`  
		Last Modified: Sat, 01 Feb 2020 16:47:28 GMT  
		Size: 45.2 MB (45241584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d13d85604945e95d31c38d488a822d8e0b84e7548a10db0c89115cca1887aa`  
		Last Modified: Sat, 01 Feb 2020 18:06:29 GMT  
		Size: 10.3 MB (10325358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596b324848b1286794120fbcb3c696328dd955db597ec3e70840b5dc97d794db`  
		Last Modified: Sat, 01 Feb 2020 18:06:33 GMT  
		Size: 4.4 MB (4372596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38645e5b0e6402c091627176f5aed8b9d434ccf323ecc4ca2c66f934acc1a11a`  
		Last Modified: Sat, 01 Feb 2020 18:06:45 GMT  
		Size: 50.5 MB (50499891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6815a6a287c8fc9388e7131e2c39538e99952d5f119a9d0778399e162143aa71`  
		Last Modified: Sat, 01 Feb 2020 18:07:33 GMT  
		Size: 206.9 MB (206870838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6db3c643e53f9dcac9c809ec70218f067d567a7731100abcc871cceb3ea7527e`  
		Last Modified: Sat, 01 Feb 2020 21:13:05 GMT  
		Size: 4.2 KB (4198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f1e84b554390175bf62884f74ff90552ddd1f8dd884047da2a38481a744081`  
		Last Modified: Sat, 01 Feb 2020 21:14:30 GMT  
		Size: 23.5 MB (23543295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4f0f53ebefa7dbf297c99fe105085debee6fb81c4641c8fec38ff3cde91905`  
		Last Modified: Sat, 01 Feb 2020 21:14:32 GMT  
		Size: 1.4 MB (1401352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc0b21395c84b79f7d3530f21383b5957f219a7a09ca95a1f922750e8680198`  
		Last Modified: Sat, 01 Feb 2020 21:14:31 GMT  
		Size: 294.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
