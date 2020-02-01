## `buildpack-deps:jessie`

```console
$ docker pull buildpack-deps@sha256:cc3e427f4440a96192c41109fe0cfd78b21ce65c8eb0b3f28046ff75a33de9af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; 386

### `buildpack-deps:jessie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:f484eaf6d21e9020daa9eeeeab6b839a5089dd87e3ac7252f530d1d05bcddbb3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.1 MB (247147563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a3cd2a1e821ae88f05fa104995e36b9928bc7af01bd4d6a7f8e6a144a0ecc20`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:35 GMT
ADD file:6bea7fdf1d11cd3f2dfa923395205f70d42d388f597b21e289e7f516a2c687f1 in / 
# Sat, 28 Dec 2019 04:21:35 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:51:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:51:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:53:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:56:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4888a2f4fb02c1971555f590f5c9ef6369e7fa4599e586fb70cdfe80330370b`  
		Last Modified: Sat, 28 Dec 2019 04:26:07 GMT  
		Size: 54.4 MB (54389662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7fe6cef1db298eb80da7e99c0df1d8cf44011585831905df6373b5dbb32e0a8`  
		Last Modified: Sat, 28 Dec 2019 05:02:45 GMT  
		Size: 17.5 MB (17545463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d711a2398cd1349ffa38f874196cbe32d2cc4e6742bec566f58fd70eadd0138`  
		Last Modified: Sat, 28 Dec 2019 05:02:59 GMT  
		Size: 43.3 MB (43319288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a6d5cefeb40aa2db60a29905bac044f850d39ed32052a122721ed4bc0108ff`  
		Last Modified: Sat, 28 Dec 2019 05:03:24 GMT  
		Size: 131.9 MB (131893150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:4c65b682cf2847c168c9515e457947f20c7b5aa172fbda6c0c4d470d3156df3e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.1 MB (227122859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:805448899c6729f849a8495710bd985cf8e07eddb760e196dc631f0a2031dde2`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:50:07 GMT
ADD file:d4edce93ba93edcd37d608a9b631879fc39506074ab425c75b3c55c68ce0f349 in / 
# Sat, 28 Dec 2019 04:50:10 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:30:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:31:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:33:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:37:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5fdba72d0442ed279b2949203d28c37c7388a87145a31eff8a5dbd1ec4d3f8dd`  
		Last Modified: Sat, 28 Dec 2019 04:56:54 GMT  
		Size: 52.6 MB (52579512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185dfc772e20f53d92109142b40655cb4ad05fd0c5a9d98fbc8588dbd41be3cc`  
		Last Modified: Sat, 28 Dec 2019 05:52:05 GMT  
		Size: 17.0 MB (17036607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e547a5aca6d1873224ad1dd685e40fb404e262be8dab3b9babd9a06110880f`  
		Last Modified: Sat, 28 Dec 2019 05:52:26 GMT  
		Size: 41.2 MB (41160176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5facacdc4adeb619fe643381271c0ddcd1d073c4b9f8a7064aed745bb11fb91`  
		Last Modified: Sat, 28 Dec 2019 05:53:11 GMT  
		Size: 116.3 MB (116346564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:412fc265abcd12144f5d614a53b7644e37e4fb651d04ca31f5c16ddce2d8a121
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.4 MB (221402868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5be44fdcf0c77da615462ed079080534cb683fdcb4d9972b89aa6c72dbc3c840`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:59:26 GMT
ADD file:1e4262fa38cc66ad7a041517492cdebc1a6003d5abdf60247a62ac9b6e4f89a2 in / 
# Sat, 28 Dec 2019 04:59:29 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:49:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:49:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:51:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:55:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:aea5fd044669abb13c109c414677bbdfcff8ede5c7702238c4f2ac6516aed8d2`  
		Last Modified: Sat, 28 Dec 2019 05:07:53 GMT  
		Size: 50.3 MB (50303019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d184ad45cae18544214bc702ca0f30ac229146272a0beb9a2cadb33e292754`  
		Last Modified: Sat, 28 Dec 2019 07:08:31 GMT  
		Size: 16.7 MB (16722673 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419f61375e6a1502499e02be09f7c9c9ebd6d98cf596528d66dd2846bb8674c2`  
		Last Modified: Sat, 28 Dec 2019 07:09:03 GMT  
		Size: 39.8 MB (39772491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a52186bd012f39d89f345d293c4a4884d6e89f26cad07e9dc4478a662c069a`  
		Last Modified: Sat, 28 Dec 2019 07:09:36 GMT  
		Size: 114.6 MB (114604685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:jessie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e66a052efc8007ef643425dbc2f0cdd29d603c84f5f0a166272cf80b33aea866
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254314136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa24dc437f02a2b9e51bb81622d671ca0805d448537fccab9281b1f3c7991ba3`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:39:48 GMT
ADD file:23c9537c86963e84613c942db01132e5d06384a5fd0b9f92595ecd7aeff0935d in / 
# Sat, 01 Feb 2020 16:39:48 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:29:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:10 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:32:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:36:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:605158be38a8eaa27411bc385ed7dcdc4884e9ad8da221b2c160b4dc702fd008`  
		Last Modified: Sat, 01 Feb 2020 16:44:50 GMT  
		Size: 54.6 MB (54607256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ddb6eab72836c2f7baabe2d7cc8baedb1fd4b769a0b80c9bafac7bd2504cb0`  
		Last Modified: Sat, 01 Feb 2020 17:43:34 GMT  
		Size: 19.9 MB (19855762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:297985b73d122356ed17677fc8b290e4f7868384fae0b731bb529cb8791165f4`  
		Last Modified: Sat, 01 Feb 2020 17:43:49 GMT  
		Size: 44.0 MB (43976429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ddf50e81a8dc5cd91306855023c7830a9e32276134e92e5ab174ef972b7335`  
		Last Modified: Sat, 01 Feb 2020 17:44:23 GMT  
		Size: 135.9 MB (135874689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
