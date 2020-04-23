## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:4ed277104a491eeb9ca0086b3add16a0471c31c5bf931dc64873c910216ce670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:bullseye` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2a1a411f7b9a3dcdaed111e2d392776142cb64aee606ec845914c02f5d75e7ca
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.5 MB (323462119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be92327eb2bc5fe18c8b6cbbf3cbe31e7d2fc9262ff9481bf3654901b9072a56`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:19:50 GMT
ADD file:3785e6fc0adaed3cfee77ab7dd0756681492573e3553e88b5225fc14d56562d1 in / 
# Thu, 23 Apr 2020 00:19:50 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:48:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:48:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:48:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:49:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:91028a6d2ef79dd78d620852cfc6dcda63ffb7301b4a1e87108edd2e9e499625`  
		Last Modified: Thu, 23 Apr 2020 00:24:32 GMT  
		Size: 52.0 MB (51981200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:831d9a74fb2992a6446c6eea6a71db00f998b765785b1f37a56464bd43408d09`  
		Last Modified: Thu, 23 Apr 2020 01:01:52 GMT  
		Size: 7.9 MB (7933113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f1160e3e672fe333aee8b37fb0e11661c02ab6ee62a7e276efe6b6f42271d9`  
		Last Modified: Thu, 23 Apr 2020 01:01:53 GMT  
		Size: 10.3 MB (10297877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb1b44c07b5963deefc7eb6049f8d70bbf5144fb469244d7bbc84ab510d03c3`  
		Last Modified: Thu, 23 Apr 2020 01:02:08 GMT  
		Size: 55.6 MB (55644473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb451cc05cefb11d498037c65f2c1bab6f225366af23d485cd39a0bcff59fe`  
		Last Modified: Thu, 23 Apr 2020 01:02:43 GMT  
		Size: 197.6 MB (197605456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:15f82e02b048b0941b29a19e093ea27d8c6d1a38b56cadc42ab152733b0138a9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.8 MB (294846222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50d2f812464890db1a136a836cbb5fb69d5ee2940560daccc4c71e8586d56fcd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:51:06 GMT
ADD file:5be2178df3e21d9545818a91f7ad742ffb521f470db4ffb6f2b4b8e5381d0427 in / 
# Thu, 23 Apr 2020 00:51:09 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:21:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:21:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:22:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:24:59 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07d9742943d725059b0958dfff17760efe7b78df3e20635aab1c80cecf4d1375`  
		Last Modified: Thu, 23 Apr 2020 00:58:41 GMT  
		Size: 49.9 MB (49935576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6804de3a0793db8acc856e22cd4ad64c904053890cc2d87651cc6e49fe02b38`  
		Last Modified: Thu, 23 Apr 2020 01:47:02 GMT  
		Size: 7.5 MB (7514841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270a05b6f98e0c3895a7e4e4a0bc79d3ae0e9198c978423547432797212d3c83`  
		Last Modified: Thu, 23 Apr 2020 01:47:01 GMT  
		Size: 10.0 MB (10008598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f17e3b8b92d507a69bf5d98d8571bbf60bc2f3724064eb6f9dcc64adb3e9a6`  
		Last Modified: Thu, 23 Apr 2020 01:47:29 GMT  
		Size: 53.2 MB (53222383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931472ff9546287416c3f8eafadbe8d5608669f079e2718eab0da45ad20df9ee`  
		Last Modified: Thu, 23 Apr 2020 01:48:30 GMT  
		Size: 174.2 MB (174164824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:0bad2b3406187224a882b9a448e58fc6a418fee8e703ec80291110e7c8f50bde
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289312675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1dc95a7badef77ebe17701abbfc97a1d1a29a4048412b530bdf843db5ddc2f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 01:02:10 GMT
ADD file:85e3bb4657a3517a43e0275a958ad028f3f1684bc8a1a2ab4370553a106583be in / 
# Thu, 23 Apr 2020 01:02:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 04:03:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:03:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 04:04:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 04:07:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:584761cab5c57084a1bd0e36523834571e95168e0a6245926b908313dd826549`  
		Last Modified: Thu, 23 Apr 2020 01:10:09 GMT  
		Size: 47.7 MB (47659184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1e340b2750c5a3fef5b49207324ded3ab2bab0ec5b13355bc0b1479b14ed1fe`  
		Last Modified: Thu, 23 Apr 2020 04:28:03 GMT  
		Size: 7.3 MB (7255985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92a158eb7564ad64eba8f5106f2f533b09bdfce834baf124daae77ec75837670`  
		Last Modified: Thu, 23 Apr 2020 04:28:03 GMT  
		Size: 9.7 MB (9672905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c73dfc1241c0df6667cc7df3946c524d3e6c3ae8ddd128d21feb342d8fa7069`  
		Last Modified: Thu, 23 Apr 2020 04:28:46 GMT  
		Size: 51.1 MB (51064686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd29e0ffa9b4810768b418bb7e397e0a67b8fc7a2e32971f98f7dd2e3a85bffe`  
		Last Modified: Thu, 23 Apr 2020 04:29:36 GMT  
		Size: 173.7 MB (173659915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7864b8b6b9d400515079584931731c05d180b822765c50f5059fdc17b4ad30e1
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315398987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c09853ff2a6bc33e538e926430c37215ef00d1448527abe36c490d52b354ab6a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:53:05 GMT
ADD file:99275cc5b8d6761ab79ba23a20d3b0bbcf4de8d067f9bfcddaafa88e17896ab0 in / 
# Thu, 23 Apr 2020 00:53:13 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 03:33:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:33:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 03:34:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 03:37:32 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:66996f8a7f93aa23f91784fa408a35cbaf913d8046e2f6f13a7af916c500e308`  
		Last Modified: Thu, 23 Apr 2020 01:02:28 GMT  
		Size: 50.9 MB (50908186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdfb0684cc2e626db76b396f85933158cbc7dc2b612036dd90856e21e619baa`  
		Last Modified: Thu, 23 Apr 2020 03:50:08 GMT  
		Size: 7.8 MB (7808198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:361e10adf6a1fea868c509a1a730cb254017a3f8d82bc5545f885d03eb38e38b`  
		Last Modified: Thu, 23 Apr 2020 03:50:08 GMT  
		Size: 10.3 MB (10294359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1589210a19fdfcc709abcef8745e5944ec6f308c5ec7b7e442e828602914bc02`  
		Last Modified: Thu, 23 Apr 2020 03:50:36 GMT  
		Size: 55.8 MB (55795532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3198ec4cb8b0eca4e0889351540f41389f2a17fa87998f509d8f04a6dbf725b8`  
		Last Modified: Thu, 23 Apr 2020 03:51:28 GMT  
		Size: 190.6 MB (190592712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:470abb34eccc6bd549c7f2bc4b7c75d7a2c13a7ea46afbb2f565ff2cf4b35491
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.3 MB (333251255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0611e089dedcac15418475c933f9e6880e8779ca79c370a90b67b7c201a3794d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:38:53 GMT
ADD file:8842691c10d9cacf5f52fd9fdb3b0f3a9a5ed4212d9f2ab558d17e5efd9a758f in / 
# Thu, 23 Apr 2020 00:38:53 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:39:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:39:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:40:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:41:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0bf245c0cdf57ebbfbaf49d796259272bf11094420c0537965c4d322d66b4e55`  
		Last Modified: Thu, 23 Apr 2020 00:43:49 GMT  
		Size: 53.1 MB (53124775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3766da29a92d4e7819901f2cd3fd92af428a41fa1efecc94dadb17f8bd6e6d`  
		Last Modified: Thu, 23 Apr 2020 01:58:36 GMT  
		Size: 8.1 MB (8110585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6891810791eccf312b55bd366b84147115acf3dc533fd07cc22ed2ce3dd771b1`  
		Last Modified: Thu, 23 Apr 2020 01:58:36 GMT  
		Size: 10.7 MB (10657349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b2d4fc44bb2b15f9080c349ce508b8e7c2e640679fb59aaf2f9f78b4b2b456`  
		Last Modified: Thu, 23 Apr 2020 01:58:59 GMT  
		Size: 57.5 MB (57496351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6672e899d07c4422d9dbaced559f95bb0d5ee6140b5c6a476172131b2abef85`  
		Last Modified: Thu, 23 Apr 2020 01:59:54 GMT  
		Size: 203.9 MB (203862195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f4b48f3237081cae168cc74cd9bac7bd33a68996d22b6dc0800147c9a437db04
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.7 MB (305671815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:949290776e4984545f43457f8fd2ec9ff39808d1bbfe4dbac9fbe295841cf1d1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:08:38 GMT
ADD file:01a8dba65674c16c3bae58d6e4cf7693a0616ee5efc5495e513ba4454fdaa97b in / 
# Thu, 23 Apr 2020 00:08:39 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:46:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:47:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 00:48:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:50:57 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1ccb563ff5d3d7b0b42a931c0aef1761ab04927c47d729b21ae98a7788ef6af2`  
		Last Modified: Thu, 23 Apr 2020 00:15:41 GMT  
		Size: 50.7 MB (50694211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35cc1749bc72a1c4ea633b9f43ee46469e3c9b9fca82f799a577fbddf0a0295d`  
		Last Modified: Thu, 23 Apr 2020 01:06:10 GMT  
		Size: 7.5 MB (7460628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed375c9815816af90643e25af4799e3d5c112ac07bc80b13cc5976a394275f53`  
		Last Modified: Thu, 23 Apr 2020 01:06:11 GMT  
		Size: 10.3 MB (10324480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6b47876b2590563400c1a797f7f51c2152380cb414e543cb90b037dbd2cee06`  
		Last Modified: Thu, 23 Apr 2020 01:07:06 GMT  
		Size: 54.6 MB (54585872 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f39ba028ddcd6e173ca76dce16814d7bf73e4de689e3ff5705edcf7394b08c`  
		Last Modified: Thu, 23 Apr 2020 01:09:33 GMT  
		Size: 182.6 MB (182606624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d14043077a5b378ea7323d77e75815dd180c6bb176d7d435f08ae7bd8e148995
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.8 MB (342774999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562970dfd2104f374ad48968bae76c1f0b19ee0da1c6a863be8b3c81c01831fd`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:32:36 GMT
ADD file:93aa541f8747875de57b6848e6e2df3b2ae7cdc03dcee5489fcfc1bbf45c4920 in / 
# Thu, 23 Apr 2020 00:32:41 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:39:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:40:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:41:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:49:04 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:23044bc1c77de90086fe2791c49374dbad1ff9af6b3b4dde5f4d46fc92e6a936`  
		Last Modified: Thu, 23 Apr 2020 00:48:13 GMT  
		Size: 55.9 MB (55855771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b244e406f7e60e72181a1fc05e23631e55e349385a03256c692ed685e75d61`  
		Last Modified: Thu, 23 Apr 2020 02:21:35 GMT  
		Size: 8.4 MB (8356173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bb62044b675b46ae88158a62f5e93b36bed0459b07a8e50881cd48a7d4070e`  
		Last Modified: Thu, 23 Apr 2020 02:21:35 GMT  
		Size: 11.0 MB (10975739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3335db3829bab72102f9d1637bea7f1aeb652766860510ad63400bf5e283430`  
		Last Modified: Thu, 23 Apr 2020 02:22:09 GMT  
		Size: 61.0 MB (61002339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5bf98eaf1596ff1d477b54f67a9f7f4262c973db57b18c260ce706e5ce99052`  
		Last Modified: Thu, 23 Apr 2020 02:23:38 GMT  
		Size: 206.6 MB (206584977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:6e73e6173f28c2e620a5dbae978dcc303075c5f314a5418a27b6e99bfb883dbe
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.1 MB (304139646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84cde88ec6e1662645a43962d779858cc43a71f738cfd95b59faf2cc366141ba`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:50:53 GMT
ADD file:f056a549a046e95dc913639e6f66f03822a0253c29e80ca83bfec0ad17ce61a0 in / 
# Thu, 23 Apr 2020 00:50:56 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:52:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:52:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:53:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:54:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dea34220fb3629088500931b5a9b5f42e8310437035ae5d967501a1b59801c6b`  
		Last Modified: Thu, 23 Apr 2020 00:55:22 GMT  
		Size: 50.6 MB (50579994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a059087ed5236381609d7860683f56075adbd498ce096fd21827cb24329124a7`  
		Last Modified: Thu, 23 Apr 2020 02:06:32 GMT  
		Size: 7.6 MB (7600648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb9b52f51c99a0897c6de164eb2fea990a9c6433eb44a6d979eed78270fb2b7`  
		Last Modified: Thu, 23 Apr 2020 02:06:33 GMT  
		Size: 10.2 MB (10183991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65106f2e1ea5731a1e6189fa863014d5706b4d58b8b483e937c817dcd3186786`  
		Last Modified: Thu, 23 Apr 2020 02:06:48 GMT  
		Size: 54.9 MB (54879886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d536f4ec41465dcdaabc4cd8b849d80736b086afd03765e8b0a6d9ab23e4104`  
		Last Modified: Thu, 23 Apr 2020 02:07:22 GMT  
		Size: 180.9 MB (180895127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
