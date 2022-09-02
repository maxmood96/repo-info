## `buildpack-deps:focal`

```console
$ docker pull buildpack-deps@sha256:7e46c886cfb15a4bb8d6c337f664f56a107e337264a74f80d9a1d0835b83dd61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:focal` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:236275a19f23e22211c79a72f7606ead785500c53780cff18e7ebff5fffdada5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.7 MB (245735269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c377f7b08c01644a3b2aa6f083ce6d4f1812e8652efbc64a7b9b550dbfb08132`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:23:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:23:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 02:24:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:27:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aceaa9f66a60a3695a6348be449df629aed61f57a9cbd55a388bdcfa40cb27b7`  
		Last Modified: Fri, 02 Sep 2022 02:37:25 GMT  
		Size: 7.7 MB (7747479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d69e69900ca0c9eb8762e001879c1e84e29d94a2397e389440b1d8689445e5`  
		Last Modified: Fri, 02 Sep 2022 02:37:24 GMT  
		Size: 3.6 MB (3624451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035d79e04aad5acedcb6ebd870819e030f0f1cb534d55136ac5f6087b31b39f9`  
		Last Modified: Fri, 02 Sep 2022 02:37:44 GMT  
		Size: 60.7 MB (60738066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f65cb058b8e19392f740a77af749897af039a43730af19d5b986a7de8cc696`  
		Last Modified: Fri, 02 Sep 2022 02:38:15 GMT  
		Size: 145.1 MB (145052588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:6cc83b90351f8ac0223faa87e392c2a9f24157d4f422e588bb779baa01f1ce55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211783596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581bfa0c33a65661c95cc0c51eb8e5cebb681ebbee12360daadc798008c4d1ee`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 06:08:22 GMT
ADD file:685f4b5f8c1f11b6389e9f929909e1a667abf29814a7ccfb859aae287dacd7e1 in / 
# Fri, 02 Sep 2022 06:08:22 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 09:31:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 09:32:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 09:32:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 09:33:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:eff72fca8e1d166ddfda6ac6c409e888c95950da6c47d360a088219c0ad7ba05`  
		Last Modified: Fri, 02 Sep 2022 06:10:16 GMT  
		Size: 24.6 MB (24588743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0063ca7d240c073b50b399efe49028199e2fc1671c3d5e69e566b2b36dea9282`  
		Last Modified: Fri, 02 Sep 2022 09:41:04 GMT  
		Size: 6.7 MB (6741254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c93ac5277e93cfbfa1f89a828713b7c6314babc86f222357de3141883f92a010`  
		Last Modified: Fri, 02 Sep 2022 09:41:04 GMT  
		Size: 3.1 MB (3104403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ccea48caa3d4856a1e5a5278dfb92e187166e74c5f4226090de64a520ae1f91`  
		Last Modified: Fri, 02 Sep 2022 09:41:27 GMT  
		Size: 55.4 MB (55442260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715d9c57028ba4ae9a65a2fe21da32b16c0d47fed424958a335b6ff470ec3fad`  
		Last Modified: Fri, 02 Sep 2022 09:41:57 GMT  
		Size: 121.9 MB (121906936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:6e21811ff53feb197c55dbcb5913e6167d2f756d5225790d038f9b9b82b31c3e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.5 MB (235507390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8031960c5c0d2a8ef476a475b524c69ce8e35c58b47617ebd56fe13cdd990406`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 00:57:42 GMT
ADD file:78c56cf572dbf860290780b955a94dc4de09bd3b8d64b6a83aee51afb349129a in / 
# Fri, 02 Sep 2022 00:57:43 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 04:38:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:38:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 04:39:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 04:40:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a9f619ee5e9c87f19eed59abef41d53eb0694f492da010ee069ff26e7b4ff3f`  
		Last Modified: Fri, 02 Sep 2022 00:59:23 GMT  
		Size: 27.2 MB (27191817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6667cb55d48ba4971074c7d8aa09e7b2368fb83f8ab6336c1ae53675ef8a5fdc`  
		Last Modified: Fri, 02 Sep 2022 04:46:48 GMT  
		Size: 7.6 MB (7614784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f84ae37056f7e9d12b5c5d6fbf1924cc86999a56dd4adeff2f422552b9edf08`  
		Last Modified: Fri, 02 Sep 2022 04:46:48 GMT  
		Size: 3.4 MB (3387844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a8330d23b3e1d0fb7320e653a9dba9018129a28846b4d6cffdc5caa044ceee0`  
		Last Modified: Fri, 02 Sep 2022 04:47:09 GMT  
		Size: 60.8 MB (60803136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131f3a8b3e4894860eeb15da87fb3843ad69cebaa2ea4bb04c6b16240a96eef2`  
		Last Modified: Fri, 02 Sep 2022 04:47:40 GMT  
		Size: 136.5 MB (136509809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:b864ae13cc2a8ce0ee0d8dee4231935012a1f332f708f5e160d746b0e322b543
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.5 MB (269549986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3829078671a39b677798e7ff15db74a35aa34c521d9cdba344014e925803e15d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 01 Sep 2022 23:49:54 GMT
ADD file:eb82827919ea73f9595d7b0b70fe9aa5ff23e16ea6a87f7f9ef4e1905857b789 in / 
# Thu, 01 Sep 2022 23:49:56 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 03:34:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:35:00 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 03:36:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 03:39:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:891f6400ce611ee5975f04ad6d2c68305c76a8628b846df1b1f9ac7c45b1311c`  
		Last Modified: Thu, 01 Sep 2022 23:52:11 GMT  
		Size: 33.3 MB (33295624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c38e8344eceb4e722b9d2cc7cf0d2cdca38bb2870c652f545c8ea652efa4f6`  
		Last Modified: Fri, 02 Sep 2022 03:55:42 GMT  
		Size: 8.7 MB (8704791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059cb2841292be0e2908a7c8f78a0db3f136154b78b70a9881535c8c1080dc3f`  
		Last Modified: Fri, 02 Sep 2022 03:55:41 GMT  
		Size: 4.5 MB (4456160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93cd324c0fe479474378bdfc00b7027887775d4396a082938a08a2b3f8163431`  
		Last Modified: Fri, 02 Sep 2022 03:56:12 GMT  
		Size: 69.5 MB (69529571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845e0c714d38e7d101ce3585817a73b34d9f7e53c5810c5ad7ecc1f8469f0e7b`  
		Last Modified: Fri, 02 Sep 2022 03:57:03 GMT  
		Size: 153.6 MB (153563840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:focal` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0983feadc237a384bc35d020091ffbf6b9eb5b8b312f716e301223786fa27dd4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **226.4 MB (226432077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30c4f4a81fad6a7cffcc865b12be1766a3f2d65338bbd923218ff0906b2232f3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 02 Sep 2022 01:03:13 GMT
ADD file:75a78d9ec31ac5486bdde3e48ebfc534089c5f38f14850243c2ab2e632f0bbe5 in / 
# Fri, 02 Sep 2022 01:03:16 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 02:03:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:04:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 02 Sep 2022 02:04:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Sep 2022 02:06:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b87ab7b8bb5c2a1f34d9a2e9887fde669c33cea7428fdb048362dfa81eccaa75`  
		Last Modified: Fri, 02 Sep 2022 01:04:49 GMT  
		Size: 27.0 MB (27045282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f81ff7514526202dbe703eab1c9f1a8c08e2fdc2c2d56b949c8d1f90825e908`  
		Last Modified: Fri, 02 Sep 2022 02:15:30 GMT  
		Size: 7.4 MB (7397526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cf575bc155da8ebabf970fa2716a48bb3789c6a3967d83d0f7583991658942`  
		Last Modified: Fri, 02 Sep 2022 02:15:30 GMT  
		Size: 3.5 MB (3542655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423b3fa0fb4a3902e95b623da0004da02d690cf894720b6584469c6c7709e39a`  
		Last Modified: Fri, 02 Sep 2022 02:15:48 GMT  
		Size: 60.0 MB (60008998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4036fb36c2cf3563cffaf474016b239dfaed09f13efbeea14c7f35e3027aecfb`  
		Last Modified: Fri, 02 Sep 2022 02:16:12 GMT  
		Size: 128.4 MB (128437616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
