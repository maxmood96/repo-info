## `buildpack-deps:stretch`

```console
$ docker pull buildpack-deps@sha256:00c55b98cc95457df8fae3b5f81338938bab63996eb632201f921574eee0e2ab
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

### `buildpack-deps:stretch` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1092593f57a1a0ce7df5ce8d4be23eacf00e89496c00f35a3be6cc40db20f977
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325502455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b45c882f0d36f1719fe08f79f10398ed1ee767cce7c715c592eb93c3d5709137`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:22:48 GMT
ADD file:21bf6969c2166c361350c07b1089a1a4b34b7cd3e802a602385d83c49f44a7f6 in / 
# Thu, 23 Apr 2020 00:22:48 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 00:59:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 00:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:00:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:01:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:99760bc62448fbba69f6f0981d09bb4b7532e17362ecfb709141a7195d9b01d3`  
		Last Modified: Thu, 23 Apr 2020 00:27:35 GMT  
		Size: 45.4 MB (45375951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3fa264a7a881e244e7fd3420edda0d550ee3b26ed870f5c021d937497ffd602`  
		Last Modified: Thu, 23 Apr 2020 01:05:50 GMT  
		Size: 10.8 MB (10797279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a222a2af289fc1fe54c037f02e7651e0aead2f81f40cb2885786bfe57aed10a9`  
		Last Modified: Thu, 23 Apr 2020 01:05:48 GMT  
		Size: 4.3 MB (4340174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1f89293f045ce3c13f0d10aa189292713a213532b69efada74fe25d2d4db381`  
		Last Modified: Thu, 23 Apr 2020 01:06:08 GMT  
		Size: 50.1 MB (50082601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115b6fc5ace19f10a939b9462204914b46f25e6d90a0d2cbd05f015b23c1e5b9`  
		Last Modified: Thu, 23 Apr 2020 01:07:07 GMT  
		Size: 214.9 MB (214906450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:58040e8fab3d9283054ad7d0d347d163877344128f9b13c64ff14d052a20249c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309479406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb30aefcfb3a3067594263d605d17eb88213a9efab038c0cd11890f3d8a295fc`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:54:28 GMT
ADD file:c32e9d5ebedbf7d4d46c8547ec1385d73ff4bb1d974ef50c0f8b5eff16b5a6b8 in / 
# Thu, 16 Apr 2020 00:54:30 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 07:58:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 07:58:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 07:59:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Apr 2020 02:07:15 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f3041cb19a4c1ef6e07f5cd99b75e4a39e4467bbb70f15c5a0f391e26752e76`  
		Last Modified: Thu, 16 Apr 2020 01:02:13 GMT  
		Size: 44.1 MB (44068060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23d3830d6b9ee5a39d175e90acabdb00e95db1dde0ad55a7a6a2f613083ee9a2`  
		Last Modified: Thu, 16 Apr 2020 08:09:51 GMT  
		Size: 9.9 MB (9866674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcaa03069fade4274b1c026a1a89b48bbca5a2acc893cb7959369ea62f92fc0`  
		Last Modified: Thu, 16 Apr 2020 08:09:49 GMT  
		Size: 4.2 MB (4159196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48da1d0e1b77f63d74ef617b05d8c474ab6526a2d8e68a3e5b00e5405a4b5558`  
		Last Modified: Thu, 16 Apr 2020 08:10:13 GMT  
		Size: 48.3 MB (48302981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b42b683682633f14435369b2e52849698812abdcb47192f7ebadaf413004861`  
		Last Modified: Tue, 21 Apr 2020 02:12:20 GMT  
		Size: 203.1 MB (203082495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a1c0ec760d7ae85ae5b8146389f4e32bbf919df09a491955de7146638fc8e784
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297494911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734431be1b9d3124a9a966a86381dca6752e237fa53cbc47c11aa3d1b05e094a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:04:37 GMT
ADD file:b83ed4f9f7c8b10eba728f85030722a771b39336afd7ff9eef2eb6b94791533e in / 
# Thu, 16 Apr 2020 01:04:40 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 01:50:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 01:50:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 01:51:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Apr 2020 01:19:12 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:37d8a5aac9ec54f7757e1243cff051c8372be0cf907e086fba2607e08d2a4135`  
		Last Modified: Thu, 16 Apr 2020 01:12:16 GMT  
		Size: 42.1 MB (42101227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f4f4abba4245745ee86a35473696f5ecbe961a03af35bd6f07b2253c3bedba`  
		Last Modified: Thu, 16 Apr 2020 01:59:44 GMT  
		Size: 9.5 MB (9498336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3accf104e4ac412a36f3c1fc31fb94722661bf356ac878a4b502dc20086c8d2f`  
		Last Modified: Thu, 16 Apr 2020 01:59:42 GMT  
		Size: 3.9 MB (3918841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661b06bea35fef2d1bfd84e8d9bb0f243557b3d08139187ad1d0956db6fccc0`  
		Last Modified: Thu, 16 Apr 2020 02:00:05 GMT  
		Size: 46.4 MB (46410934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:186e211feda53a739862ad449add54162b3f3dc800f0adda1a99e91c489fdaf7`  
		Last Modified: Tue, 21 Apr 2020 01:27:42 GMT  
		Size: 195.6 MB (195565573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee19c1c78a1572cdfa994a92ac9ef81698ef2e5297428558e11e02fb5806f2d9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307312641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134774bfc009e525d2cb559d3129b27cb059cb946356e10580cfdbda454764e1`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 02:44:49 GMT
ADD file:6d09304a2db2752e78b9ce9610594102dc756aa4cd210f85bbfa21105c7dd88f in / 
# Thu, 16 Apr 2020 02:44:52 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 03:21:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 03:21:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 03:22:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Apr 2020 01:59:39 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:65d54b492d599e7c785a582a0f70195e1f09f0886e54cb7788f1021f383eb4ed`  
		Last Modified: Thu, 16 Apr 2020 02:51:10 GMT  
		Size: 43.2 MB (43159230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be35cdee43e0bbb89c0867d201ff274ba25b6ea9bfe7f8f0c1d1d6de36ab08a`  
		Last Modified: Thu, 16 Apr 2020 03:30:52 GMT  
		Size: 9.7 MB (9748442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b803ac2c0e69edab9b8db20bee0f9dfc0191a7975c94d4d2ea0088d5a1759be8`  
		Last Modified: Thu, 16 Apr 2020 03:30:51 GMT  
		Size: 4.1 MB (4094379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f56b7aa1f85cab0d60a62bc0cefa5ec56563f6681054c670ba97d559b4e7ba34`  
		Last Modified: Thu, 16 Apr 2020 03:31:12 GMT  
		Size: 48.0 MB (48027596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b89e9488b4b59192ce9868d217da40cc24690ddd35b2d6814d99af7cdaf74ae`  
		Last Modified: Tue, 21 Apr 2020 02:09:38 GMT  
		Size: 202.3 MB (202282994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; 386

```console
$ docker pull buildpack-deps@sha256:db0a8aff96c37c2e72c229aa255b069bf213d81f601c7bff3831668b47c380c2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333045363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a0a09273d6c4f0bcc0d1d17afe0a8eb5f541db359dd21fb18e5a27c6db97a72`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:06 GMT
ADD file:298a4dfec0058f9502705ebab6ca3787b1bcb5845d21ecfcd1771505b061b061 in / 
# Thu, 16 Apr 2020 01:43:06 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:33:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:33:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:33:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Apr 2020 01:53:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aedad1667b3098c616b8251fdfca8170596731152b6043a01601df826b79b4e0`  
		Last Modified: Thu, 16 Apr 2020 01:49:17 GMT  
		Size: 46.1 MB (46094897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a13ff1ee1a9968ed086324092c33ec123f94ecb99ccede500342483418d840`  
		Last Modified: Thu, 16 Apr 2020 02:40:58 GMT  
		Size: 10.8 MB (10818136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6cdc434eb33063a8439a59c1a179e4fa3c9d968ee9a3ad4e2ff12714e1b77b1`  
		Last Modified: Thu, 16 Apr 2020 02:40:57 GMT  
		Size: 4.6 MB (4561464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2fcb87ea1dc9422e771e3534fe181a7836d49701ee9061b31b09a1a00c9f44`  
		Last Modified: Thu, 16 Apr 2020 02:41:16 GMT  
		Size: 51.6 MB (51613902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3173724bf64dfbe2b62b74e000e77641d96a04a0cdd110beb7149fb56db5c628`  
		Last Modified: Tue, 21 Apr 2020 02:03:51 GMT  
		Size: 220.0 MB (219956964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:6fd4aa12ffcee90fc6493cfba838cbfe8e817c67d0761aa6c890a146e28742a3
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318847378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f8d4f114521dedd1be3729371711a5b44322d9b4345eb0a10055af55aab795`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Apr 2020 00:12:30 GMT
ADD file:076cd21ba96c7d91a0af4f716c8309a9b092cbbcd4c11f5ead2e2a91dae43736 in / 
# Thu, 23 Apr 2020 00:12:31 GMT
CMD ["bash"]
# Thu, 23 Apr 2020 01:00:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:00:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Apr 2020 01:02:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Apr 2020 01:05:31 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3535f2056d5540d877f08809fd21e68e9db2ecaa1af00cb85b4522a16c35e414`  
		Last Modified: Thu, 23 Apr 2020 00:22:41 GMT  
		Size: 45.0 MB (45048818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20e3b44e91d14a9d07b503cf60d0ed04ee5d11eebacef157dabfa2c6d4a62fed`  
		Last Modified: Thu, 23 Apr 2020 01:17:13 GMT  
		Size: 9.8 MB (9826234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecb2ad4ea35a7a01e57dfa74ff5af3cdcfad24105d385a7b475a3d0a9e9f4e1`  
		Last Modified: Thu, 23 Apr 2020 01:17:10 GMT  
		Size: 4.4 MB (4394838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b206fda6aa600e14c689d94764f50425c38308c250f177746840c0618364fe90`  
		Last Modified: Thu, 23 Apr 2020 01:18:05 GMT  
		Size: 49.5 MB (49475549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce792e4297f5b34adf49eddcf215c0d6b96f31d54fc62b863fd83f9b07843689`  
		Last Modified: Thu, 23 Apr 2020 01:20:49 GMT  
		Size: 210.1 MB (210101939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c49588c626f1bd48e6c7237a72492e22eae15a7ef6e5d7f8c131d6588caeccf4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.6 MB (320554564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2fa4c7bdbbe0e182ca696607eeb01b961745365b0b43d516385677b6ac5be2d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 01:43:04 GMT
ADD file:d4949f465ac0dbf2adcd2e1b8f1d0feafefbf5ca291cc71952eb3ad16ee14985 in / 
# Thu, 16 Apr 2020 01:43:11 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 06:02:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 06:03:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 06:04:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Apr 2020 02:33:55 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3071a1f69d49da5ef8731d119a68201faab21b496e239d4b67677cf66ba3d98e`  
		Last Modified: Thu, 16 Apr 2020 02:03:49 GMT  
		Size: 45.6 MB (45646020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c622e17c315eff3fdebc5db0e9b85f745434834b8f6f35fb284c0a6415e40a`  
		Last Modified: Thu, 16 Apr 2020 06:27:24 GMT  
		Size: 10.0 MB (10002451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be3d6b2c6b9995d22ea2928ba6dac51748f74b7c8ad0c833e2f3e31530bbad5e`  
		Last Modified: Thu, 16 Apr 2020 06:27:18 GMT  
		Size: 4.3 MB (4296592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3266d75c5a1cc86917df2a9268d25412e12d090e1ec1a857e707d0fdeab7247`  
		Last Modified: Thu, 16 Apr 2020 06:28:51 GMT  
		Size: 50.1 MB (50085109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e5754d72218630159979731577cebe38d6f97b8fe2d82e6c5a12da1d638ec18`  
		Last Modified: Tue, 21 Apr 2020 02:57:06 GMT  
		Size: 210.5 MB (210524392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stretch` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f96f97f324a2a9d321dea9e1219eeabb5a95a0735077656b0fe0c4587d3f4230
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.4 MB (317365622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2333c7d7428870da9349e7586ae132daf98f58b6d7498e6384f844f5961f527`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 16 Apr 2020 00:43:47 GMT
ADD file:bf54e49d85edbe8d61bd9e868d71faf0f26b4474f23eda7b692abfaf7aea50a4 in / 
# Thu, 16 Apr 2020 00:43:49 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 02:02:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 02:02:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 16 Apr 2020 02:03:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Apr 2020 01:50:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b4e6598a8ad88c3d661d89d6fda41ee33a54f3c6f16c4988cceaa6fd0afd04bb`  
		Last Modified: Thu, 16 Apr 2020 00:48:18 GMT  
		Size: 45.2 MB (45232626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cb98b0a4ec56e95b4ba3f3261ba975cd69e2a0240149eb53e4bbff9739e272`  
		Last Modified: Thu, 16 Apr 2020 02:08:04 GMT  
		Size: 10.3 MB (10325610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c82c0f221bc14891b71387b7587fd4f2a615d339ecf0afadce350f82b3e098`  
		Last Modified: Thu, 16 Apr 2020 02:08:03 GMT  
		Size: 4.4 MB (4372651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d17818ca9e172b803a01ef9860f9b1c67b359a6d75c51e65a63c0448b3816d`  
		Last Modified: Thu, 16 Apr 2020 02:08:18 GMT  
		Size: 50.5 MB (50513161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f48fe90066f878a657e838515e626ddc19be11a7e6a415e1f7e3d01a2007d1`  
		Last Modified: Tue, 21 Apr 2020 01:54:58 GMT  
		Size: 206.9 MB (206921574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
