## `buildpack-deps:bullseye`

```console
$ docker pull buildpack-deps@sha256:065c3254dfcb343c14aaf46f2bbce740b3125a287234cb05173f9ff2b79ff393
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
$ docker pull buildpack-deps@sha256:d070ed6a77719da38d83207aea452cbd685ac6a947db79579ba33aefe41b8245
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.4 MB (341427652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5645f8c867e3a724d7d8886e0f58a8dfcddf21d3426263fd8d6d130aaf36d6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:00 GMT
ADD file:91c81aa3735ab11fcf7db3eb2dc51c94759276e7d3657f0fe81829c133f7c8dc in / 
# Tue, 04 Aug 2020 15:42:00 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 23:24:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 23:25:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 23:25:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 00:20:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a7bda3d6de74128f57cc726f2172127887e010c6a291320273a9c9eb8ad29209`  
		Last Modified: Tue, 04 Aug 2020 15:48:28 GMT  
		Size: 51.8 MB (51838182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8231f0c7125cafbd1f958df6356c90a0dc3947e50ede3c176820814176b1318`  
		Last Modified: Tue, 04 Aug 2020 23:38:27 GMT  
		Size: 7.9 MB (7921995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e4f23b97ad1b9a745be0f1e7dc1856f9a233a25a83f51b22fce0c16759de05`  
		Last Modified: Tue, 04 Aug 2020 23:38:27 GMT  
		Size: 10.6 MB (10580797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2bf24be332afd3092d09e178f69ceece27993e6347cf9f2b4fa4526dc9131f`  
		Last Modified: Tue, 04 Aug 2020 23:38:44 GMT  
		Size: 57.0 MB (57018253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df66a53f0d02ee96856546903ea1ca411418937f7b8a11cdc9860655ab673aa`  
		Last Modified: Tue, 01 Sep 2020 00:30:41 GMT  
		Size: 214.1 MB (214068425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:153aa2e4a98bf332116dbd9815eb1ec63e166aa8d65f570b041192940c4ad4fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.1 MB (318056918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411df297ff360f2d2cefe38083e151ec5256e283446bda659e11b3597609d7c9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:08:44 GMT
ADD file:2b581429c7fee51f5899cbb76a5d9c36cf7223edcbb473fbe2f8db3a53a82263 in / 
# Tue, 04 Aug 2020 03:08:52 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:07:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:07:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 06:08:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 00:08:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a2a8e3d684f3a7d5eba8b8ba267ffcbcf9d2089c1f803e105113f8b34f8991e`  
		Last Modified: Tue, 04 Aug 2020 03:32:48 GMT  
		Size: 49.8 MB (49784523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa91b4ecc0f372adaedd757806f1b23aee559777f06d525ee224f6f2911c31f`  
		Last Modified: Tue, 04 Aug 2020 06:35:19 GMT  
		Size: 7.5 MB (7501685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9150d7965ec842da0721c1a458d2f16e78d852da4190dd6c46b4d82e38e27476`  
		Last Modified: Tue, 04 Aug 2020 06:35:20 GMT  
		Size: 10.3 MB (10267288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c670d1433953e1f7e99c5959030cdd629bc54e680c8aafc16116a6288cbada`  
		Last Modified: Tue, 04 Aug 2020 06:35:44 GMT  
		Size: 54.6 MB (54587591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0edcdc0a145ba13a0820595a02b8ad2df3ad74e1e8ae3a8716f42f178614159`  
		Last Modified: Tue, 01 Sep 2020 00:37:52 GMT  
		Size: 195.9 MB (195915831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a4745c3c7476d351c81c52ea6cf01e571ce99e1a8cf44b7d62f5fb6fa7640e57
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.8 MB (303797404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a072df981b1ff2635099f367647cbd8377afdf9d4a0344d5c036a4552404feab`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:55:34 GMT
ADD file:8d817c9168a8bfbddda5007f76443d27203cb5bf02ec609cd277ddc327736b10 in / 
# Tue, 04 Aug 2020 04:55:36 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:45:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:45:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 07:47:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 00:02:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:984ab044320fbabd5c060737e15adfea7aa109893b7f68f41abc04f445d3440f`  
		Last Modified: Tue, 04 Aug 2020 05:04:18 GMT  
		Size: 47.6 MB (47570419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93473ce552fd633dff0ed8a7eba4610e368b271c6582de1c474472a31cc7340c`  
		Last Modified: Tue, 04 Aug 2020 08:24:12 GMT  
		Size: 7.2 MB (7243678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9559bb2ff9f55098d0aae9e6210eb73fdb47f91e0b6fff535ae21fcbbfa54dea`  
		Last Modified: Tue, 04 Aug 2020 08:24:13 GMT  
		Size: 9.9 MB (9915965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2ff07294173b72b0b22d817ab0dce8e848d6eee67c264eafd80f785b1c18e4`  
		Last Modified: Tue, 04 Aug 2020 08:24:40 GMT  
		Size: 52.3 MB (52257311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21d23aaca0f8c2903223d6b21639135345a7a01142f8b10667cd5ccf66d9b78d`  
		Last Modified: Tue, 01 Sep 2020 00:33:30 GMT  
		Size: 186.8 MB (186810031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ac256ff5d075a3afd686fd444624eb33145091d5d499cfcfe4b74ff0048ffac6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331745602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dcbc7bc194b56197c32b6263c5c71b4c7317e623d3331b57762d6e459dac4c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:56:13 GMT
ADD file:4fc4606909c4e142a9f6338c83f07b785ba5e327445dcc39b633d0ba1c6641aa in / 
# Tue, 04 Aug 2020 06:56:15 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 11:06:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 11:06:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 11:07:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 31 Aug 2020 23:42:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71e8526225e6316d22b8a5c3ff79ea6218380b2061da9bdc547cbde64ac697cb`  
		Last Modified: Tue, 04 Aug 2020 07:03:03 GMT  
		Size: 50.8 MB (50751888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e591597eed5c9bcdab48d2f92580ee39ad123cfb112c1bfb5595ad424cdc6a3a`  
		Last Modified: Tue, 04 Aug 2020 11:21:15 GMT  
		Size: 7.8 MB (7796393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3ab5699c96506c152cbf0948edcadd188d0926d97f92a4080681b075d4c3b5`  
		Last Modified: Tue, 04 Aug 2020 11:21:16 GMT  
		Size: 10.6 MB (10588126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c214453711c8c213df0ba7270cd91a97aac1b97877b5346f40325a5dce5556d1`  
		Last Modified: Tue, 04 Aug 2020 11:21:48 GMT  
		Size: 57.2 MB (57199506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fc5a0a5434c69dd22e88295df92059e8362f3f76757d3c1283d75341dc3b80e`  
		Last Modified: Mon, 31 Aug 2020 23:51:55 GMT  
		Size: 205.4 MB (205409689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; 386

```console
$ docker pull buildpack-deps@sha256:9494bc773f888a01589381a9d0cd9484b8e45c7d2911219537acdc84fd1f122d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350762165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc211a0c16f56ce6f4ddd418ec95f278981ac2d633950c658942df2bb3ee27`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 03:36:50 GMT
ADD file:e3f476fccb15ccc08c3c8c26ac23f1909e7c0f79bc060289f35fc37bb4483f80 in / 
# Tue, 04 Aug 2020 03:36:50 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 08:04:49 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 08:04:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 08:05:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 31 Aug 2020 23:39:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:308ce7c38ffec8ca43e219653810c298ee87abfaaa068ff112f1e8003b108546`  
		Last Modified: Tue, 04 Aug 2020 03:41:50 GMT  
		Size: 52.9 MB (52909727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429c636a1f75410c98b200faef3ff9f568a242579e0d885a7b7c70d771f96e9a`  
		Last Modified: Tue, 04 Aug 2020 08:24:23 GMT  
		Size: 8.1 MB (8099324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e845809b7e141a8bd0e85748582037ea1e08bcb9ca449097624dfc315d876d2e`  
		Last Modified: Tue, 04 Aug 2020 08:24:23 GMT  
		Size: 11.0 MB (10960569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a782bddafbc0654d5b0e92f99d7ee9edffa1960018fb14017095b3dae8bfc63`  
		Last Modified: Tue, 04 Aug 2020 08:24:45 GMT  
		Size: 59.0 MB (59009528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e136b7f1a8fbf916ad88a2b55b360f678691b87a4ec807c4f5f701d3e108de07`  
		Last Modified: Mon, 31 Aug 2020 23:49:25 GMT  
		Size: 219.8 MB (219783017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:232a65d9c6fd7d07101e6470c9f5d3ada8dee186cbca6a31deec7cd62cdc37b9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328329968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f040f641ccdddad298e18338ba80ff60c0d442cc7bc49ce07fee9fef24b5b8d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 06:41:13 GMT
ADD file:9e3d31545fae8b44e8aa3ad24629d2336276c01e23dfbdde9885d01e61a54298 in / 
# Tue, 04 Aug 2020 06:41:14 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 10:33:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 10:34:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 10:35:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 01 Sep 2020 00:10:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:249c58d6beef4ec2d380f0e2adf7ea99a80c295cddcf6f6bc3d6b463dfe44a05`  
		Last Modified: Tue, 04 Aug 2020 06:46:35 GMT  
		Size: 50.6 MB (50550783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:049f809de28cc8d8e169ab9ee5721613f58fafdc670bbe6d66a1058fe998ee06`  
		Last Modified: Tue, 04 Aug 2020 10:47:30 GMT  
		Size: 7.5 MB (7450522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d557e2093dc94091a8f931745b728c83f35ad977f14de65f1ec5db00bedf8580`  
		Last Modified: Tue, 04 Aug 2020 10:47:30 GMT  
		Size: 10.6 MB (10599039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:748d597a52166ec3c0e83e53c0b933c57f9230d87fbc629e0c1fb4c68970dec8`  
		Last Modified: Tue, 04 Aug 2020 10:48:22 GMT  
		Size: 56.0 MB (55973336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfc999e7d7fd4c3ced516367f51379b9dace7c2210c5fe087d53d0b39673608`  
		Last Modified: Tue, 01 Sep 2020 00:18:21 GMT  
		Size: 203.8 MB (203756288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:e057dde2bdde18735be922cee70c47a4e14ad70e0dd64bccc21cfc4b1a180a92
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.7 MB (347659835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8ca4337ca7784cf57570ce09524b7064d63622504affc56bcf616776caee72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 04:43:52 GMT
ADD file:a1065b5d1a75daf3153a753a23c630c5a77451644b83418dd23b2c1d046c970d in / 
# Tue, 04 Aug 2020 04:44:00 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 07:01:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:02:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 07:03:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 07:11:59 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:26d0cc426ef5200b8e12941b37f3b65f8de8a01be463ecfef94be00ae56f5596`  
		Last Modified: Tue, 04 Aug 2020 04:50:57 GMT  
		Size: 55.7 MB (55655910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1aadce00449a8701783ecb72b8dce872a06609d7a90a69b4dfa29a8727a1bc3`  
		Last Modified: Tue, 04 Aug 2020 07:42:12 GMT  
		Size: 8.3 MB (8347825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48f8213614f8c61ad803c5be08bb2ca48b08b0b8111551a50801c69e31afcf4b`  
		Last Modified: Tue, 04 Aug 2020 07:42:13 GMT  
		Size: 11.3 MB (11327020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a3017101817902f76986e15e141f0d4e7a84d78f35d8e4ddb6d03363fd29d6`  
		Last Modified: Tue, 04 Aug 2020 07:43:26 GMT  
		Size: 62.7 MB (62684011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93ec3bf77149f9b06e900628a54d7202ba55850a6a6cea7aaf5c8e7d61d7cee5`  
		Last Modified: Tue, 04 Aug 2020 07:44:50 GMT  
		Size: 209.6 MB (209645069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:bullseye` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3eb57dd568cc0c8aee259419372b4de9da3f71be07585bacdcad92fa02ab8f18
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (318984452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218b397d838565786b34d9d934058b8e53ed1badba818714a276c43e07a9e83b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:16:37 GMT
ADD file:be061a89b8959a241d8303ec83a6494b37d71fe20736b073046173371101421e in / 
# Tue, 04 Aug 2020 01:16:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 02:19:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:19:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 02:20:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 31 Aug 2020 23:44:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:67f968df5fed9ab1993b2cba53f4810f984f47936fce947baf7ef2e7d8a5a20c`  
		Last Modified: Tue, 04 Aug 2020 01:19:19 GMT  
		Size: 50.4 MB (50416822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789709f3eb6ec781e7bd5d546a438d9f93b42d8201f34934bb917541d98545eb`  
		Last Modified: Tue, 04 Aug 2020 02:27:09 GMT  
		Size: 7.6 MB (7590147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17405c3991955650e0612638adcfcaec522e3c07552eb6b1924bd354bc8e608`  
		Last Modified: Tue, 04 Aug 2020 02:27:09 GMT  
		Size: 10.5 MB (10456481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68e926add9df5b913b9031846ca2cf9730906d323525f8cf01eaea4906b08b0`  
		Last Modified: Tue, 04 Aug 2020 02:27:23 GMT  
		Size: 56.2 MB (56210651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5567868dbebc64b33e56840f199da4cf65f2f704f799cd3fa265a082795e17`  
		Last Modified: Mon, 31 Aug 2020 23:51:21 GMT  
		Size: 194.3 MB (194310351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
