## `buildpack-deps:impish`

```console
$ docker pull buildpack-deps@sha256:710ffcabeddc3a9df48ec061a961f9871ed0c579a015cc7571638b062f2a4dc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:impish` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:74e04bcb4ce77c2f7f498ceedef4bcd22dd482d3bd751c9860c2ae0b5940eaac
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406701540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f4f2dc8d354435cd0cd1ca02df54d39a82b73e7316f0378acb7c272ffa7ff7a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 05:30:54 GMT
ADD file:dc66b6b0841e395b5cf9d65976a75c3a46a19eb2c0fda4556ac6b4c5b0fe4dea in / 
# Fri, 18 Mar 2022 05:30:55 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 06:49:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:49:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 06:50:53 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 06:55:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:49dc71d53e6dff9c7147b85fbe167470cff447114548e6df43606b75526c1451`  
		Last Modified: Fri, 18 Mar 2022 05:32:45 GMT  
		Size: 30.4 MB (30385910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee29a8440a917a1f49c8a66657a5f8a8c2effd9e25b3bb9367ee85276d079b4`  
		Last Modified: Fri, 18 Mar 2022 07:11:01 GMT  
		Size: 3.7 MB (3694257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30247b645fd7fa468adece5509844320b82b4af192c0633c03785f1304e95c7e`  
		Last Modified: Fri, 18 Mar 2022 07:11:01 GMT  
		Size: 3.6 MB (3552145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b435325fdd0055e7dbb9c2e27ca4c08b8206afc1663c4c8d7cbedd1830a4f6b`  
		Last Modified: Fri, 18 Mar 2022 07:11:20 GMT  
		Size: 38.1 MB (38085451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa059c5ef6b1dd2e695c85aef87bbaa2149230373de2bb7f0c6741cd00489d0`  
		Last Modified: Fri, 18 Mar 2022 07:12:29 GMT  
		Size: 331.0 MB (330983777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:4c1c95fe68bbaaec28ce49b6f0d940a6ea9fae708b95c1ed0a363ca1aca0a0f8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371090640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91e02b51a1d1e13cd3e3dd4774008dc0aa81b48382ef98222fa5a16ad1ba8d1c`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 21:21:55 GMT
ADD file:2147b6b5f5a6085917d41d8d2c1cace254f6f07b78f75973d696c4aadc615c7e in / 
# Thu, 03 Mar 2022 21:21:55 GMT
CMD ["bash"]
# Fri, 04 Mar 2022 03:22:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:22:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 04 Mar 2022 03:23:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 04 Mar 2022 03:25:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0e5117981c2b00f6b01a0a1aca7c0fc638269b9372a736c2f4e60f0ee26f1c88`  
		Last Modified: Thu, 03 Mar 2022 21:25:44 GMT  
		Size: 26.9 MB (26921937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063f27cd7b6a3b3adf03f7c99abb087586c307ea8a6822f834cab8840e832a48`  
		Last Modified: Fri, 04 Mar 2022 03:40:09 GMT  
		Size: 3.4 MB (3443736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166ccda40e86aecd84ebc63263f1e0fbf366905e989217e8e90ab8e42845d855`  
		Last Modified: Fri, 04 Mar 2022 03:40:09 GMT  
		Size: 3.7 MB (3743304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfff3c988beff6e832fa04ae3e0a0996a0ff6557dfce6c77513659eed983f9d`  
		Last Modified: Fri, 04 Mar 2022 03:40:49 GMT  
		Size: 40.3 MB (40286786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eeb44863ddbe2befa731838649ba0c130966fd873bc107aeb9889e2a340e56f`  
		Last Modified: Fri, 04 Mar 2022 03:43:50 GMT  
		Size: 296.7 MB (296694877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8bc197a5da2152c2a78d1cb86feb1cfbfbedeaeb1787ae1286c2ad731ccc111a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.4 MB (399362498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f729819c49b43ab327170b838ae049227e8d3c13476b13c3d39af58c18eb4b3`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:41:11 GMT
ADD file:0e8c3ab0e6e7f15d32d0e43c17409e1ad9e4c77cb87b27edcb23fd8bbd941784 in / 
# Thu, 03 Mar 2022 19:41:12 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:10:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:10:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:10:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:11:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:070b8fff765c544371e1499a46e470f8c2eeb6f493d1e9949af6b068f1208ad8`  
		Last Modified: Thu, 03 Mar 2022 19:42:58 GMT  
		Size: 29.0 MB (29031972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66bb6800b180c2bbd9c0d917ea78669aa5e7110362527fc96692bdb2cd314ffa`  
		Last Modified: Thu, 03 Mar 2022 20:18:18 GMT  
		Size: 3.7 MB (3679015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1bd2a7b702ea3cee495ba3e01196c92f87bcd77f372d995d2ad1c555947e9da`  
		Last Modified: Thu, 03 Mar 2022 20:18:17 GMT  
		Size: 3.3 MB (3327773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4528b4c4ba1eea7093dab1e9cdb512996043c77118167e5e0cc564e63e7d18fe`  
		Last Modified: Thu, 03 Mar 2022 20:18:34 GMT  
		Size: 38.0 MB (38033546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79c48c53c3c42b32dcae316931674bcda55a10489feba01b420ab26a960be94`  
		Last Modified: Thu, 03 Mar 2022 20:19:29 GMT  
		Size: 325.3 MB (325290192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:74b3cc98cfb9ee1e2684f15602afb2eb17ad2e8c26fbbc1c3dfbc5c2a47d8f37
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.3 MB (414322514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd447d66114f00a0129131d347411ccdf99adc885dfa81c31576699b18839268`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 20:28:54 GMT
ADD file:c9dbe94a6e712a5b1a894d57c1396be96b5bd702e90b77b82817ce85618dadcb in / 
# Thu, 03 Mar 2022 20:29:04 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 21:36:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:37:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 21:39:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 21:52:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0c4c4e967fa8621c96984594294f639a4d7ec13235867cbd56a506b4ef96bf1`  
		Last Modified: Thu, 03 Mar 2022 20:35:37 GMT  
		Size: 36.2 MB (36175818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab8dd918329f318acaa93d44e882d2d310d61f08741b32bf697e381e348af61b`  
		Last Modified: Thu, 03 Mar 2022 22:02:28 GMT  
		Size: 4.1 MB (4147822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95f180d1cc1b110578ee29533ee2466d939fc44bb802f1c74ea0241c95d3e02`  
		Last Modified: Thu, 03 Mar 2022 22:02:28 GMT  
		Size: 4.2 MB (4242315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb4c4d37a778e320b4ae12d134942515574fe1fd2706b3073ddaca573f7715b`  
		Last Modified: Thu, 03 Mar 2022 22:02:50 GMT  
		Size: 42.7 MB (42728193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd9a48bfb4e4c07baf9a3a9b9619fb83b7ca66028760513100f3133990d9eb3`  
		Last Modified: Thu, 03 Mar 2022 22:03:57 GMT  
		Size: 327.0 MB (327028366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:deffede3e6fdec826b872957b218bab93b2fe96730805df900f4a0decb8660fb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266377994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11bc3d20896023a17f6c2ecffec4ba41be76d71f39f48441553e260a77d39b8a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 18 Mar 2022 00:40:33 GMT
ADD file:52433e15e49d335dfc7bbc78550a32b9e0fa14eb31fae0ee2600087827048035 in / 
# Fri, 18 Mar 2022 00:40:34 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 02:58:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 02:58:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 18 Mar 2022 03:02:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 03:08:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b8d4dcb4c786a507e8054e237dcda4d54fecb228f526b4716da0b3748e4e9c9d`  
		Last Modified: Fri, 18 Mar 2022 00:58:59 GMT  
		Size: 27.2 MB (27214441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d018cc194635cf808f308a016bf556df0c929bbaeca2419ddd072f327e7eef22`  
		Last Modified: Fri, 18 Mar 2022 03:39:27 GMT  
		Size: 3.5 MB (3490494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0316dd6f0f2b9e02907cd326ff95e0950fc92c02a622066c5d1f6cfe1cba12da`  
		Last Modified: Fri, 18 Mar 2022 03:39:25 GMT  
		Size: 3.8 MB (3803952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902635f9f6391d0ff49d9a5ec92a582053c43b14a45c73d99c5d11695f8a1a4a`  
		Last Modified: Fri, 18 Mar 2022 03:41:37 GMT  
		Size: 40.8 MB (40769200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebb6e159f66cc0955e900209ae54fabc0879193f42e007caa197592a19e487ed`  
		Last Modified: Fri, 18 Mar 2022 03:47:40 GMT  
		Size: 191.1 MB (191099907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a304c4698aa995c284986049af9aa0afa2daa10fa1e54abfddb3bedfc0c1f0f9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367825754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11609ad1461b7b2d5fe426a83d5c9c7d5fe1fe5cac08f994b9370a8d91acd160`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 03 Mar 2022 19:42:01 GMT
ADD file:e150af68d3db546783a6fafa964d1b9264cb1b35930b07255ce083fa0c40e532 in / 
# Thu, 03 Mar 2022 19:42:03 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 20:36:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:36:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 03 Mar 2022 20:36:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 20:37:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e0cf59e92c5acec5ae595918f7a30d60c44156b11926f39465f58e2132619a47`  
		Last Modified: Thu, 03 Mar 2022 19:43:36 GMT  
		Size: 30.5 MB (30524528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7871093b66fa67764e2403a711a69a008b0941e41ea3b9edb6b89473ad18a0`  
		Last Modified: Thu, 03 Mar 2022 20:43:52 GMT  
		Size: 3.8 MB (3763377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3fc096c211db0aeef7379615bb3126fc4a81163cc8fc1c0b54d1ada0869b3e`  
		Last Modified: Thu, 03 Mar 2022 20:43:52 GMT  
		Size: 4.0 MB (3963395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e75021dcdcb9dcae8b7132547ff083a6cdfddda8976a3e188ac791c9884d2d`  
		Last Modified: Thu, 03 Mar 2022 20:44:06 GMT  
		Size: 38.3 MB (38327374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09409f7c801465e5b9b1a0b593d01585712f0af485a63bbb52d2fea25d333c3`  
		Last Modified: Thu, 03 Mar 2022 20:44:46 GMT  
		Size: 291.2 MB (291247080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
