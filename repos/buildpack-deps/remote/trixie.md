## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:48514be6350439a880254065836e69f7081c0014651ddf4589de5f672eb59e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 8
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:aa176341f4c3d6c4fb5456a5c4a823c82c22816f1f377315c22d1057df75ea38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.9 MB (370893021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9757632b447fc4059155fe799515b85035b2f13c175db9136cf9a33cc09848be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:58:17 GMT
ADD file:cd33732baf7a8215a9cb532ae6f2fe0be64d030adb1f3e0085e461cf4f22ec4d in / 
# Wed, 20 Sep 2023 04:58:18 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:27:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:27:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:28:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3954180d94025620e480192adbba35d582d59582f662e17f992f954d83539feb`  
		Last Modified: Wed, 20 Sep 2023 05:04:48 GMT  
		Size: 49.5 MB (49467670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e565cc2b6bbf1308bd8312f40ad760a99d8567113763dec2537af6652bb673`  
		Last Modified: Wed, 20 Sep 2023 09:34:11 GMT  
		Size: 20.3 MB (20269130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd10974eceaa5affd1244428fad92105303c6661b8d09326a7a85b3f11de3125`  
		Last Modified: Wed, 20 Sep 2023 09:34:28 GMT  
		Size: 64.7 MB (64669125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4505d43bc4385e169467514465a55c52a3f1e653b207da717c4fc7baef34cc87`  
		Last Modified: Wed, 20 Sep 2023 09:35:05 GMT  
		Size: 236.5 MB (236487096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:b6b4d49af1a135a0b9700d1b31cbfe1fda5885fc88085318d20c6f5677f4c267
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.7 MB (341744224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94edfebf8754105d0b1e2b17ab0f403de0d9b5e649ba4c9796e5ddb66e339895`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:39:06 GMT
ADD file:a7de42b73a4591d75c2ea2f44cdd15d34ce24fa78ca8e57ac62e4fd3ffe2019d in / 
# Wed, 11 Oct 2023 17:39:07 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:12:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:12:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:13:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a100e11229dc40f9cdcd25e779cd1f10bb500c44c5b9ae24abec0b01f4b26b1`  
		Last Modified: Wed, 11 Oct 2023 17:44:09 GMT  
		Size: 47.2 MB (47166046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f41504078ef3db4155843c88e3eb49d76721ce77692685bb502799200ff810`  
		Last Modified: Wed, 11 Oct 2023 18:18:08 GMT  
		Size: 19.4 MB (19369976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262dceb7106ef55dcd198f1f5e689fd8eb7e9ed58de15831f3c0c75dfd041123`  
		Last Modified: Wed, 11 Oct 2023 18:18:28 GMT  
		Size: 62.8 MB (62838690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d46f6f51ff369aa4d880bd7e8a20e601a1c90225ae57a890f12a2a25e5f49ec`  
		Last Modified: Wed, 11 Oct 2023 18:19:07 GMT  
		Size: 212.4 MB (212369512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4c045dc4f0a40ef7ea8aa643d85295c297dae4a7e62109ad9f9646ca46b7e814
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.9 MB (321887047 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:334991229eb00270da6c788fd956080cef3f7293ac3606209e71a1bd04874714`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 04:59:32 GMT
ADD file:48b3882ac99c385930d3ac71ac20fda8a1b071b08088814bf1a41054078ecd14 in / 
# Wed, 20 Sep 2023 04:59:32 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 15:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:33:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 15:34:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:219658aab374640dcbab3bd1cbe574955f68e4305522bfc19564d1ce15fed88d`  
		Last Modified: Wed, 20 Sep 2023 05:05:38 GMT  
		Size: 45.0 MB (44955127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e0f2039e0f302927a38df2eb35fc70587db403fbc14273b4fe098c21cb0969`  
		Last Modified: Wed, 20 Sep 2023 15:39:33 GMT  
		Size: 18.6 MB (18617697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba45c0e5519ac44055eac6898a4c8abe790e1be149095e9a8db5eaf719de3e2`  
		Last Modified: Wed, 20 Sep 2023 15:39:51 GMT  
		Size: 59.9 MB (59891965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b18f2abd66df756bc6a06d8b163ff75670f87a21b572f5fde1dca495dc25c9`  
		Last Modified: Wed, 20 Sep 2023 15:40:30 GMT  
		Size: 198.4 MB (198422258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:080672a6e364a27dc74f4ec29e73403740d0faa2676e8c119a74d82d8156d9a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.5 MB (363518845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7225dc2374bb409fec886a4babdb54f6e8707be41fd604029d5b36036471ecda`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 18:26:37 GMT
ADD file:ae967b7faba93d8a00f97f28b4d720835a90a27fe53b2f278072893f4cdaa8e7 in / 
# Wed, 11 Oct 2023 18:26:38 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:51:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:51:50 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 19:52:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddf19dd473b427de200cf2b123540cd1dce2dcb51aeeb4a1359b7f954dc951ba`  
		Last Modified: Wed, 11 Oct 2023 18:32:45 GMT  
		Size: 49.5 MB (49505530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3234e169293a5a7c5d4630e4d414fffc649556678901730a692ba3b43cd5e618`  
		Last Modified: Wed, 11 Oct 2023 19:57:45 GMT  
		Size: 20.1 MB (20110046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b71bac299e7b4e42a2756046d77fc625e1dc632615808cd1ec6bbcc2d48bf4f5`  
		Last Modified: Wed, 11 Oct 2023 19:58:01 GMT  
		Size: 65.4 MB (65405981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd31d1b7c77e861f5a1738daaf94715bed1e46ce9d29312378210f37d36a0041`  
		Last Modified: Wed, 11 Oct 2023 19:58:31 GMT  
		Size: 228.5 MB (228497288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:994ef7ea0528ecf13af562253a56f73215611d917ab27a646754b376219684c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.6 MB (377583489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8687b806f3edf6acdd139dc20b84f6944f4c0dd93ccea4d071e0dfd78397f5b5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:43:20 GMT
ADD file:ad97acda5f74778001aece2a9e280f0e58d2953cf8fdbd4740a049c4a595a225 in / 
# Wed, 11 Oct 2023 17:43:20 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:19:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:19:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:21:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ce8ed34eaeffdeb7ac49225c6093f421b0005558aedb2b9c429731032d156621`  
		Last Modified: Wed, 11 Oct 2023 17:50:59 GMT  
		Size: 50.5 MB (50485846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f94c813421107d5ab710ec3329c2cd90f1b42da6b64e3d4ea8428fc7802b293`  
		Last Modified: Wed, 11 Oct 2023 18:27:57 GMT  
		Size: 20.9 MB (20886277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f264142306efbcccd3638b5a3b7788249da917c198eab1e97f89a7fb7178050`  
		Last Modified: Wed, 11 Oct 2023 18:28:21 GMT  
		Size: 67.1 MB (67089139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27cdd865dd18cf6d9d37c1cf2104e99f5152965c92be6435b3e986f215cf6dc6`  
		Last Modified: Wed, 11 Oct 2023 18:29:15 GMT  
		Size: 239.1 MB (239122227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dca0a86138fbc50e65519ae1cb8864e2c188c758bcf38f11e36636b7656d341d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347936742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54fde2b02e81071bbe4ec5cae65d324e798d69935ed9fad301e0b1ace2d656be`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 03:16:43 GMT
ADD file:feafc03e82af46c6c55a0a73cf1d1107968b6694a898de04dbd04b90bd98508d in / 
# Wed, 20 Sep 2023 03:16:48 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 22:12:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 22:13:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 22:19:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0c3624a744ac0024156b087e27ec700730d5abd850c903edaefd0cd35bb20d02`  
		Last Modified: Wed, 20 Sep 2023 03:28:01 GMT  
		Size: 49.3 MB (49302317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee833587bbee7c28ebb44ce27cbd72e6bb33739d9203cf1e4464b7ae564d8c1`  
		Last Modified: Wed, 20 Sep 2023 22:30:41 GMT  
		Size: 19.6 MB (19560312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8fb39bb7824bc4241044104821fb808dc3b6465ce10625a02aee85775a106d`  
		Last Modified: Wed, 20 Sep 2023 22:31:30 GMT  
		Size: 63.6 MB (63606238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5964edc07d833070936e9b5e5c05b3f5b96bb59c525d17412a61cdb6a1f393`  
		Last Modified: Wed, 20 Sep 2023 22:33:49 GMT  
		Size: 215.5 MB (215467875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:309bfd6b1b1b3855702980edcb586bc26ba049db4463943b23153879f9c6eeec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.4 MB (384351616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:751aaaeb8b4738691d1aaf012e3cb97d29e306dac0ff37ad139457c8d1c8c919`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 11 Oct 2023 17:47:23 GMT
ADD file:24d4df221ce118a8059e0559a8bb2d715512fa6f5b15cd1397dbc177ceaa1bfd in / 
# Wed, 11 Oct 2023 17:47:26 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:30:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:31:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 11 Oct 2023 18:34:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:93b578febbe769059c90eaa91e9dc027d172e6088856c2c52dc3e26dfdf01d4c`  
		Last Modified: Wed, 11 Oct 2023 17:54:24 GMT  
		Size: 53.4 MB (53418134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:576f9c6569231cdc2bf492ed27ab8c980261301252c26c4d6fcf8dec4fa4de9b`  
		Last Modified: Wed, 11 Oct 2023 18:41:22 GMT  
		Size: 21.6 MB (21644083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86429c6121c1cef63b4087b6359567a0aa3be523db5603dc673793266a48e8c4`  
		Last Modified: Wed, 11 Oct 2023 18:41:50 GMT  
		Size: 70.8 MB (70768983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61d96d5ef85833f9afe41198588301802855414f4a727cccf6ccd0e7de39ad1`  
		Last Modified: Wed, 11 Oct 2023 18:42:56 GMT  
		Size: 238.5 MB (238520416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:53378fe23f1ede320d9ad15981dea6500e2dd4eabdb227ad0c9416881c8a0940
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342405728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ede672e2c43305b3e0274dd97b8401f9473ae542c2449c50b036a9255beab1c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 20 Sep 2023 02:57:24 GMT
ADD file:77b51e0abb2ed786e762b44ab5463930ac60fc37a4a4404ee62cf4653a99e1fa in / 
# Wed, 20 Sep 2023 02:57:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:54:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:55:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 09:56:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:dcfbcf60cde4d1764ae5735832195c5a57365459959cebb93c0e57bd40fd54a4`  
		Last Modified: Wed, 20 Sep 2023 03:02:19 GMT  
		Size: 48.8 MB (48760791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b239420005ab6c651870ef013ed3c379e88028e2ae4355642040198cb4a863c6`  
		Last Modified: Wed, 20 Sep 2023 10:01:14 GMT  
		Size: 20.0 MB (20005597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724dc0240d930e9ebf4eb3a0070c3eb553d06a44798e05283cc1cd48b73a5b82`  
		Last Modified: Wed, 20 Sep 2023 10:01:29 GMT  
		Size: 64.3 MB (64286239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93256ebbfd1df8e4641400040bcfb8607350dbe3e66591092348a73248ad4c32`  
		Last Modified: Wed, 20 Sep 2023 10:02:00 GMT  
		Size: 209.4 MB (209353101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
