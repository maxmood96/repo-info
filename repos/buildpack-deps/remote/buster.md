## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:593195f42b9f6fe30d1c5aca53130dbe74e8474ac4a2c7ab4f942afad171af18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:7b15bbfb6e6b0453dea52399a5bfb551f05939d4cb3870d29f690722a8248f5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311864064 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a892faa8327b253cf112e94c1480d311f8995792bc1e90d4a4d7b7ac61143c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:13 GMT
ADD file:5a868c8105f7b621ffe46e19453d846faef824601a70979f6ef2bb46076151b5 in / 
# Wed, 20 Sep 2023 04:56:13 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:23:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:24:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:25:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0dfc3f78750b97e03b66f316b37e155e3de173a8ac79942f0511888531fbe5ac`  
		Last Modified: Wed, 20 Sep 2023 05:01:23 GMT  
		Size: 50.5 MB (50498165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830b67cf52132f96464e9186a134b45378cef272f020722032b8d0ccff73e2ca`  
		Last Modified: Wed, 20 Sep 2023 09:32:05 GMT  
		Size: 17.6 MB (17580790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70dedca5333820ad46911bb546a9751d6641b13d86f87175818a188b41e0b7fa`  
		Last Modified: Wed, 20 Sep 2023 09:32:20 GMT  
		Size: 51.9 MB (51887578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc1616e79d7fc2b8c0d0c1c96469a7a4e3b1fb4542595374cd2c57e795cee3c5`  
		Last Modified: Wed, 20 Sep 2023 09:32:54 GMT  
		Size: 191.9 MB (191897531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:74862eb2a8e0da4e0ab20d6f15add73820d6c7ccb3352867c4417a57089c34f7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277697404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a24e8e731849eb75c2eb4827a1c1da6babe16c4a71bca6d3061051e56fc138b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:57:44 GMT
ADD file:61a164f3dead6329acddcce40680f06b7b0f27e5620a1afd975e186153e42077 in / 
# Wed, 20 Sep 2023 04:57:44 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:28:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:28:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:30:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6e2ab1511f035b8d0208496939ad6f66778c120d1c102125b629bdb138ce4a14`  
		Last Modified: Wed, 20 Sep 2023 05:02:14 GMT  
		Size: 46.0 MB (45966225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b42b2c67c3bd9bb3552fc4424f51e962669da3a9daf4294ea3a82867faa9ead`  
		Last Modified: Wed, 20 Sep 2023 15:37:25 GMT  
		Size: 16.2 MB (16213379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77af292e4101bab353aa314a3d1abfee18e65d9da12d6550c323dfc8367ebe01`  
		Last Modified: Wed, 20 Sep 2023 15:37:41 GMT  
		Size: 47.4 MB (47410368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cddd24ee8f30be81526dd5589e9b7903aedf0c02b621427623fd414b3a12179b`  
		Last Modified: Wed, 20 Sep 2023 15:38:15 GMT  
		Size: 168.1 MB (168107432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:f8e53ff95899f67abb3aa35ec671c43f119ca559ee8b0e519a0ece7cfe03c0fc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302434057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ab5f1e32878a2fe74760a4cb35219c1d3828050ae2f605403539b5a27473351`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:25:12 GMT
ADD file:d97d8c89883987c89b2150923abea982086030e71970f5473a534e95252b4972 in / 
# Wed, 11 Oct 2023 18:25:13 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:48:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:49:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a7acee270b8289bdc6bb8836f1a4899f794d60337a0cdc46b58a717bd27ba89`  
		Last Modified: Wed, 11 Oct 2023 18:29:25 GMT  
		Size: 49.3 MB (49291086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d43a8471c221305b41e4a48fe1a36d8d976208b182f048b98aa6dc81e6fec8`  
		Last Modified: Wed, 11 Oct 2023 19:55:54 GMT  
		Size: 17.5 MB (17451818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a82d27a09b100de4594fbc9e341ab946a39a8d635f12e633b1341a1c7aaa4b`  
		Last Modified: Wed, 11 Oct 2023 19:56:09 GMT  
		Size: 52.2 MB (52208642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb224d9b0fd6283df35335f4979c2c54bdc5609ca8473220d5d9924a91a0e11`  
		Last Modified: Wed, 11 Oct 2023 19:56:34 GMT  
		Size: 183.5 MB (183482511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:e2ca1129326f210b765c3fc489de34d0c965072bdb15a62cf1b72ab756fa27b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321272799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:138b172705b3f04788d90ae5fdf81f014877dfb0f9d4e808fba131bc14519f3d`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:14 GMT
ADD file:47cece2eff96bf7383dd2a9c5632f0ad7bb31b3a459677530f77a78e22658e98 in / 
# Wed, 11 Oct 2023 17:41:14 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:14:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:14:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:16:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:62bc68699d611f4c048328a0468ebc10de528260c7823c8938796da30db31a17`  
		Last Modified: Wed, 11 Oct 2023 17:46:45 GMT  
		Size: 51.3 MB (51256071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a664405fd519ae385ebac7659c355b2c380dd5c84037f38e6d3673b2bd9795c5`  
		Last Modified: Wed, 11 Oct 2023 18:25:03 GMT  
		Size: 18.1 MB (18097310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c138636d1c51e715c73bdb28e49fb18fc2d82cca0a21d5641a911f48cd3ff695`  
		Last Modified: Wed, 11 Oct 2023 18:25:25 GMT  
		Size: 53.5 MB (53487954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31fb7080416fbc4aee5e058de75799128cbeb8d55130f29854b8e5d7666fca0c`  
		Last Modified: Wed, 11 Oct 2023 18:26:09 GMT  
		Size: 198.4 MB (198431464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
