## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:e0af3b4e8e0aac38e04cbcb22ab860b12451b54f92738135489a8081d910bef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 9
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; mips64le
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:932d10004817582e5f12276f08ef80e227b8612b2cd7b5f8a82f4d66f5228ee2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.2 MB (331161903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc1051378fd1477164031d74f61888aa56f17074f0a80c1f5657035c8586e46`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:49:37 GMT
ADD file:aa0a8871e20fb4e68758bdebe7ee1e99e982c5e9d2e97b73575b8dcc2ab4adf8 in / 
# Thu, 02 Dec 2021 02:49:37 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:43:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:43:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:43:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:45:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:af46a953975205f2d7320842b5338767ad3d4aa084267279fc21cdc807374c52`  
		Last Modified: Thu, 02 Dec 2021 02:56:05 GMT  
		Size: 55.7 MB (55746868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923af8c82d6eb6585aa625d753ea67606bccd40758565b49eb6e0636c4281a9a`  
		Last Modified: Thu, 02 Dec 2021 03:51:55 GMT  
		Size: 5.3 MB (5276824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c97b84d4ef8d40d6b16c75023fa3aa650861e59f1151d2ab44e9643bfa121be`  
		Last Modified: Thu, 02 Dec 2021 03:51:55 GMT  
		Size: 10.9 MB (10904313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80321460c0114c02492753431792e6c46ac3fe9b80600356543e3068ed7a067`  
		Last Modified: Thu, 02 Dec 2021 03:52:14 GMT  
		Size: 56.7 MB (56722501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6166346ca25cffccddd770a09ba4d40da3e4ea06460e7d5c28f02459b76d0325`  
		Last Modified: Thu, 02 Dec 2021 03:52:54 GMT  
		Size: 202.5 MB (202511397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f86e2e49303e0f69fbdddedbc4977786956734c5a61f502a2b15e0dd0beb4fb2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302449524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf13b62a9828247b7ea9451b1bdcfbfd0df15ea312838c036c4abd213728944d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:54:44 GMT
ADD file:358278336204ee1e51bf00f8c88d281c73e7e5d5b537fca1ddea89c9e69da90e in / 
# Thu, 02 Dec 2021 02:54:45 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:47:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:47:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:48:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:52:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92d580f40fe8bf02becf360f6a4dc76454bfd66964c4acc0ddcd113fa0e9c2d1`  
		Last Modified: Thu, 02 Dec 2021 03:13:27 GMT  
		Size: 53.2 MB (53226256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638194516b96610900042221009a8c126b7644c26fe612397f2b2622bdfd03ac`  
		Last Modified: Thu, 02 Dec 2021 04:04:39 GMT  
		Size: 5.2 MB (5180320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23b2f3d24644f1e0eec33ec3662f820a19dc6b8cfa47e1f1551776f80f739780`  
		Last Modified: Thu, 02 Dec 2021 04:04:41 GMT  
		Size: 10.6 MB (10611050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced16911b039c1097a2b138cf1e729c67a19c941b575a03dee7c08a1c42d3e6f`  
		Last Modified: Thu, 02 Dec 2021 04:05:17 GMT  
		Size: 54.4 MB (54384666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d843a861ebdda9236e2509fd0e0edf6d32361323b1dce82cde777563e328269`  
		Last Modified: Thu, 02 Dec 2021 04:06:34 GMT  
		Size: 179.0 MB (179047232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:e5d398a3937f1df1597bc5898051b7a70e5a435478750fc89d2783128a58b280
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.4 MB (289417511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33265e1aba0c3258b55bc1ed291e152e0ba83ad1435d8ba1ae895f2878cad3c8`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 09:08:50 GMT
ADD file:9740c987db5f6d577c2e2575a0974eb1a867a5c79cca1eb79e7c19d112bea4d3 in / 
# Thu, 02 Dec 2021 09:08:51 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 11:45:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:46:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 11:46:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 11:49:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:366f7fef67fd1fee5779f5f26a7bf655fe3e0243c51566b5fc28b209c153a87e`  
		Last Modified: Thu, 02 Dec 2021 09:25:38 GMT  
		Size: 50.9 MB (50857401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63a2c21d88128fa3e4e629036fbd1d1d18eb72a94a41ffddfbc249ba7bfda70`  
		Last Modified: Thu, 02 Dec 2021 12:05:54 GMT  
		Size: 5.0 MB (5037501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3c060d5561088295a9205a8a15042f3a66b6758e385cae2e07d3f2f5f58e49`  
		Last Modified: Thu, 02 Dec 2021 12:05:56 GMT  
		Size: 10.3 MB (10253601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80273a3f397b2e47f3a65064b16f0b619eb3a2129a44b15d1f347c8ef553ea1f`  
		Last Modified: Thu, 02 Dec 2021 12:06:43 GMT  
		Size: 52.2 MB (52247072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c06123009a35898dfe9df2c4c476967107829127e58e51a2e0324e70f9557b`  
		Last Modified: Thu, 02 Dec 2021 12:08:29 GMT  
		Size: 171.0 MB (171021936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:3d901173d23ee38ee2d93376d320733987668586f800d8f24606fdc114815cf0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **323.8 MB (323840199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0670448471bfffcbfc60ca6410ddbeeba3b12f53d2eec3735bc7f0211a9f6e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 08:09:29 GMT
ADD file:55fe3fd1ac33de3f564d68a8c2ecffd0191c93450cb0d4cb1ad737305962c5f9 in / 
# Thu, 02 Dec 2021 08:09:30 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 09:55:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:56:04 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 09:56:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 09:57:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:670b98b9b0d3937727686672aa7a6a70d1575086655d0ec9a8862c567ab8b29e`  
		Last Modified: Thu, 02 Dec 2021 08:43:17 GMT  
		Size: 54.8 MB (54776380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:422c039fac9ed6d1af02d09d0682a0b85305423b6ebdae379fd5a6e6cc3f9157`  
		Last Modified: Thu, 02 Dec 2021 10:07:25 GMT  
		Size: 5.3 MB (5263651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a872e69f11058da0fafb7717fed9273710562e91c5a2614cc6733d685cdd4e`  
		Last Modified: Thu, 02 Dec 2021 10:04:43 GMT  
		Size: 10.7 MB (10680616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dc6e77d5f506109f0f5f6e4966ba727a7c3642b324c5949e1dfca891a40241f`  
		Last Modified: Thu, 02 Dec 2021 10:07:44 GMT  
		Size: 56.8 MB (56756677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a82dfe522bd5cab855027ca9bc55304897da12a45b9328c565c90b5f8285e3`  
		Last Modified: Thu, 02 Dec 2021 10:08:23 GMT  
		Size: 196.4 MB (196362875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:10b5d04f0946ff13f346e3c5a8e1cfc2edc9500f928f28e161d337c64019acf4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.3 MB (334271615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b584f58958a3ad972722a86f669c9e4f6105362f799e529c7881e61e30772d10`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 02:41:35 GMT
ADD file:166234c060754022c10737b949088caccb46aa6315aa91f9ff63dd1f60704729 in / 
# Thu, 02 Dec 2021 02:41:35 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:14:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:14:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 03:15:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:16:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:158718d3425b2eb9ceb4c5321a7633c30d7b948b7dfe2a98608b354788b1c2ab`  
		Last Modified: Thu, 02 Dec 2021 02:51:07 GMT  
		Size: 56.8 MB (56808054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fe1b108338e18a41ef0392f3153179fc4c7809ae0d46bd4c0ad04d928fa2ca`  
		Last Modified: Thu, 02 Dec 2021 03:23:43 GMT  
		Size: 5.4 MB (5408797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360266616da2d6b21d216fa2104faaa2528b4c353538e2fc67ab8b0942e7f3fc`  
		Last Modified: Thu, 02 Dec 2021 03:23:44 GMT  
		Size: 11.3 MB (11285984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99c83bcfec09f5a8285a2c904ff5ebadbe779a1888d98acbc22ff42f814c916`  
		Last Modified: Thu, 02 Dec 2021 03:24:10 GMT  
		Size: 58.1 MB (58139010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b39faab74dce51fb1e893a5612cb36b32738dc4dd28317a18a31ba5b1bac1e`  
		Last Modified: Thu, 02 Dec 2021 03:24:59 GMT  
		Size: 202.6 MB (202629770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:a6e5ea0f260707e39294ceb24197e58e708f11dc31a203f5d6da3ea2bd10f26d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.1 MB (312051713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:290c3b1465fec089196d5e62327cb5f13ea807ce07e0835bb9cd2c214dbf0f1d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 03:11:25 GMT
ADD file:756c847932d446a78e78b1785e3773acc2f468bed861faa53b3a777f03b1273d in / 
# Thu, 02 Dec 2021 03:11:26 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 04:19:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 04:20:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 04:21:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 04:24:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:851a637e7cfa078b1e4bcb2543d21b6bd9e139295986a256dac39682452e1a34`  
		Last Modified: Thu, 02 Dec 2021 03:48:41 GMT  
		Size: 54.5 MB (54455441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ed4124392ca3477be2c7aafcf44d0c7a1c0ac313b6aa4db5e42c0fd0d27038`  
		Last Modified: Thu, 02 Dec 2021 04:31:41 GMT  
		Size: 5.2 MB (5235788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90d46352d707f92ef2034e26342ca34e8d34141a50bef2663631e66049929929`  
		Last Modified: Thu, 02 Dec 2021 04:31:45 GMT  
		Size: 10.9 MB (10907304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11f0ae65985544fc4af9dfed32cf43717ac87519a70907b32399aa3b9bdc13c`  
		Last Modified: Thu, 02 Dec 2021 04:32:35 GMT  
		Size: 55.6 MB (55554324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c957056a816f9a0ea2f455042b6d5584bc431421435295a1bfdadaab7fd2b32`  
		Last Modified: Thu, 02 Dec 2021 04:34:46 GMT  
		Size: 185.9 MB (185898856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:25e515c5a55ba9629ec735c79bbbf6094f71f45e506b9c603c3f031dbb5f3fc4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340954054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bd81326f2f59060003916c421db6dd38a25bed5df657abf1c7b685ce417ada6`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 07:23:26 GMT
ADD file:0ba5425cea9bcdb1fac898f3ddd38f4505205a5b32c1288a9a4ecece03ec10a1 in / 
# Thu, 02 Dec 2021 07:23:34 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 12:38:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 12:39:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 12:42:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 12:51:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b9442172998188c0fffb75559bba82a9436fd970dbf2b25460afc71f86479c20`  
		Last Modified: Thu, 02 Dec 2021 07:33:54 GMT  
		Size: 60.0 MB (60041316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5b299250e1b93acaab942bfa0d27e9d3870773ddfc17e10df4fd3d31f96f82`  
		Last Modified: Thu, 02 Dec 2021 12:57:42 GMT  
		Size: 5.5 MB (5538234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3154daa6ac50e0863a376a29692bd68a0e9a4a87862f71434ccc121a401f7b8c`  
		Last Modified: Thu, 02 Dec 2021 12:57:42 GMT  
		Size: 11.7 MB (11659280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:990ba6858763a274b899da9a34d5f84598bd4e6dd076b319a268ef7fd61d7416`  
		Last Modified: Thu, 02 Dec 2021 12:58:06 GMT  
		Size: 61.4 MB (61393717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ddb22b9bff7486ed563236c142f1725ba2711051e87f5113ffd5f52b90be44c`  
		Last Modified: Thu, 02 Dec 2021 12:58:53 GMT  
		Size: 202.3 MB (202321507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:5331bfa443622d84c7295687469ca00996bc388c434e640676e36be6280ba2de
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342577661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:626ee5c259f26fc3a7190cd5846658a8187aca3f13d27ad1ce545143fae78699`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 03:16:27 GMT
ADD file:2408c0186c2415b201c5fb609f218da02da0aec9aff7f9467433a1bcbdeb0da9 in / 
# Thu, 02 Dec 2021 03:16:29 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 03:58:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 03:59:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 04:03:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 04:13:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:6a1cc4c4003753c168cfc12397594854587c6645c5f03e57779bd85f43632403`  
		Last Modified: Thu, 02 Dec 2021 03:32:36 GMT  
		Size: 51.5 MB (51509234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0400a63f68eccacb4581e73d2e13a149f13d2f96ede6f9a5041b48108f8267a`  
		Last Modified: Thu, 02 Dec 2021 04:37:08 GMT  
		Size: 5.1 MB (5089467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8536bb4db4e00844c1bdf6f562fd2fb2840423d4d90c98e791568915c641acf0`  
		Last Modified: Thu, 02 Dec 2021 04:37:11 GMT  
		Size: 10.3 MB (10318523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b46552026ea3fee87ea1959d63905f5dc028cccb4ee43e623210e771c78f3cf`  
		Last Modified: Thu, 02 Dec 2021 04:39:19 GMT  
		Size: 52.8 MB (52817111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7889a5504f245b5e769f4d6cdea23c50d597b0cf057df4d590ea4041f0c75143`  
		Last Modified: Thu, 02 Dec 2021 04:45:28 GMT  
		Size: 222.8 MB (222843326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8950dfb3348f6b26704168aa0d0ec68925e9eef22dc05aa3346238c663f7eaec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303706221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdef8d140fcb641231b9bbcf4c53f90d98096d450aff282913cad55a27ec20b4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 02 Dec 2021 07:20:26 GMT
ADD file:d7694f1f6512fdbbb5735764707de9bd26f8f25119496509ff4d721f4776e1ce in / 
# Thu, 02 Dec 2021 07:20:29 GMT
CMD ["bash"]
# Thu, 02 Dec 2021 08:23:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 08:23:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 02 Dec 2021 08:23:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 02 Dec 2021 08:24:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a71993c832edfb3256a0ce6f0d3fee82664f911373efacb0b2509901e613ab5`  
		Last Modified: Thu, 02 Dec 2021 07:26:28 GMT  
		Size: 54.1 MB (54051648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5059d18cc4add6886867dd20f08845df69f87db81dddd4aed5bbee167d1fcac3`  
		Last Modified: Thu, 02 Dec 2021 08:29:57 GMT  
		Size: 5.3 MB (5256958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049ab954cc89b359baaed86b422549b3e98ca5da0abe2643498c79abc91f1ab0`  
		Last Modified: Thu, 02 Dec 2021 08:29:58 GMT  
		Size: 10.8 MB (10797001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04b67e4108109ff26fc4cf7e8e573f64288ed5b8e504ea90e52e1f48c7ed4ef`  
		Last Modified: Thu, 02 Dec 2021 08:30:17 GMT  
		Size: 56.1 MB (56095661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:403e154ec928d2590364f499ba49afeba4c7a4dc84d1c54a184b19e68232cb6e`  
		Last Modified: Thu, 02 Dec 2021 08:30:43 GMT  
		Size: 177.5 MB (177504953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
