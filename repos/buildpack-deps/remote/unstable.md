## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:d8d83cac7e7a209d999b8026dffdd3b8f076897704e93b05a0829f19c0cb423c
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:510629bf7ce9533a231f49951f789b23afdf54922c1505c96da14394e0222d5b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 MB (390247272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f61a281502e7231809486544e2dfc46a5b2be4dd982295d8a5670aa527f4445`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:29:36 GMT
ADD file:b10a84e4e404c6ca6a1a6782f9040f24bb7bfbb95055e8cd39600ef22a4a9284 in / 
# Tue, 14 May 2024 01:29:36 GMT
CMD ["bash"]
# Tue, 14 May 2024 02:59:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 02:59:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 03:01:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a79fdf356ad40501c2429368bf029e9f2414f18b03d6fa40ddac5cebf750f95c`  
		Last Modified: Tue, 14 May 2024 01:35:04 GMT  
		Size: 52.6 MB (52642897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc1cdf2f53eab47078fb369ea2ed0807107650f4e0c9a7ff1cae9e9467eba2d`  
		Last Modified: Tue, 14 May 2024 03:07:13 GMT  
		Size: 24.8 MB (24816707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af1c456d7bfe2b9bf229bd339b2bf174e56648e3dfbc34de48bd637651d2f40`  
		Last Modified: Tue, 14 May 2024 03:07:31 GMT  
		Size: 66.2 MB (66150169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac544ac355064026ba785eadccce3f97f0eaf50205a8f46a879294788785684b`  
		Last Modified: Tue, 14 May 2024 03:08:10 GMT  
		Size: 246.6 MB (246637499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:a9e4e0528b1b873d53534caf5d0e2f3dfc4027361ba082170acfb160809622ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351570386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2926ac41042263b96f3e9164ceceb09e9e73aba9aee61822d8b3454373be0128`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:49:14 GMT
ADD file:48ad2cec46f0edaca758532e477d58141198d71874a7a659465c7778bc242f0e in / 
# Tue, 14 May 2024 00:49:15 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:16:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:17:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:19:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96c71f057932ff03c2e4c9ce93dc6ca864ede3a6ed0a0a4316465b6b244a70e6`  
		Last Modified: Tue, 14 May 2024 00:53:10 GMT  
		Size: 49.7 MB (49745150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa3dc2b7166580d8b48f65e06b51724e39b263522cf4d0680077e2d9bb25bf55`  
		Last Modified: Tue, 14 May 2024 01:24:03 GMT  
		Size: 23.2 MB (23220295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e412a60626a8f13aee74eae854661ed61935d3db74192666e599dd771a4bca`  
		Last Modified: Tue, 14 May 2024 01:24:22 GMT  
		Size: 63.9 MB (63863672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1307d05e957f8d06ce8b77a0b98f69c472fe5d7cfa35527318c35710406753f4`  
		Last Modified: Tue, 14 May 2024 01:25:02 GMT  
		Size: 214.7 MB (214741269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a2bdccce366857ebfd98636c6c28c6a3bb76e4118e54f9dcad69ba1046ba264e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334624150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1779dbb2aec9ce327d768f39ae5d9a2fbf1e8652fb20e9eb30a0ed69153f81c4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:10:01 GMT
ADD file:02154de0dc9450545487c68904a4e760ff1ce6b2170e0658abc5f63881b61f8e in / 
# Tue, 14 May 2024 01:10:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:41:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:42:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:44:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bdb66c06bd7989a8ebc0daa12fd841f7fcee2541fcb911169e2813963f822a18`  
		Last Modified: Tue, 14 May 2024 01:15:24 GMT  
		Size: 47.3 MB (47253384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:189169cb3c2ae8c9630343a69b9fbd4a22a6c652a99ce0018ad4752718803357`  
		Last Modified: Tue, 14 May 2024 01:50:06 GMT  
		Size: 22.5 MB (22524428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d33a5e1a677114ef4ca34a82b42bc5871256a2551a4a2c2641d80ee4cfbd4b6`  
		Last Modified: Tue, 14 May 2024 01:50:24 GMT  
		Size: 61.3 MB (61275812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb2c4c8da248b55d4e49f98f86b76677c97b30e0619da86d56bfc5b76df1675`  
		Last Modified: Tue, 14 May 2024 01:50:58 GMT  
		Size: 203.6 MB (203570526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:17e12d296d1812ecc9218685fb0b31738151fd3170fd1b8b0b8dec20346e5662
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **381.3 MB (381314516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bbe544e6895d59702bad3e10b6ce925536b9d2a5cbef44df7bafeadce963059`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:40:41 GMT
ADD file:65d77d3f6289af1318c696652b600f022ddbc3a1daaf105602e348ad91d2c41c in / 
# Tue, 14 May 2024 00:40:42 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:48:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:49:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:50:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:66334a1d5d0f0597e9440b0db265b333533e2fce7f5bb2d1fba09c85ef6cd21d`  
		Last Modified: Tue, 14 May 2024 00:45:15 GMT  
		Size: 52.9 MB (52930287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699aafb7efe9505bddcc73d0e5a54c28cf53e16271eae78e8e83cbc483d6a6bf`  
		Last Modified: Tue, 14 May 2024 01:55:32 GMT  
		Size: 24.1 MB (24095148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876041f742dfb5017e9256c238c132f97b01823ec0190fc0451b731193e6b523`  
		Last Modified: Tue, 14 May 2024 01:55:48 GMT  
		Size: 66.4 MB (66361236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bee6c9f71412d6a769be694597041bb4c5ba482c0614bf2b7839c74ef39283bd`  
		Last Modified: Tue, 14 May 2024 01:56:19 GMT  
		Size: 237.9 MB (237927845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:028c3c56f8b8c48f3dbf59a11c8c8980b0e0aebd39e5b72f721d34b3746f521f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 MB (390255864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb21431704d21d79e4de0a6684e51d922f1fd104b1c2a637bbd70165cf684f06`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:48:47 GMT
ADD file:e7eb6b079b0eae2716a306dfd153c88de0766961cbb0cbc2499648abc3b7bb7d in / 
# Tue, 14 May 2024 00:48:48 GMT
CMD ["bash"]
# Tue, 14 May 2024 09:07:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 09:08:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 09:10:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:241b052c0f57772eb9a56c460c88c133545f781291832042a8e20e0fd5b01591`  
		Last Modified: Tue, 14 May 2024 00:54:59 GMT  
		Size: 53.5 MB (53539918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137fcf033ffeba23f126575a61f0568479824add57544692806db0ea178f1a88`  
		Last Modified: Tue, 14 May 2024 09:17:13 GMT  
		Size: 25.9 MB (25943205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4edfcb76742431a37187c6870b54c6960f5c0328ee2ade86a3c00ae88b7d5e`  
		Last Modified: Tue, 14 May 2024 09:17:35 GMT  
		Size: 67.9 MB (67902262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682a94d1379218ce20847bbf1bb1de64fb90112d1d9d9b4252bb57d682574c28`  
		Last Modified: Tue, 14 May 2024 09:18:32 GMT  
		Size: 242.9 MB (242870479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:84e1d4e2b5b3643c67a7dec4bb189b32e2cff2f9c9500de31a98e0bf3c42f3df
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359708966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:867490fd8a8761f0b11b7e2ead79189e24a94657b0d08b60eecee6681c4a1d8b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:14:15 GMT
ADD file:33e0af2de2241c9212af2152c10bf302aa0352fa38eaae9fab1cb558d6a457a2 in / 
# Tue, 14 May 2024 01:14:21 GMT
CMD ["bash"]
# Tue, 14 May 2024 11:17:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:19:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 11:27:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:69f45a8662462c65462de8a317ebc50b0eeacc442e8038f6212a37458ce29095`  
		Last Modified: Tue, 14 May 2024 01:25:45 GMT  
		Size: 51.5 MB (51536337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986a4a732401bdf41df13978606b8c78e41c50362f2dab701093c923a5deb3aa`  
		Last Modified: Tue, 14 May 2024 11:43:29 GMT  
		Size: 25.3 MB (25307082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be2989fc28155b5fa118ba37bab607b8e502b0c3d87d6857cadfcbb97fff7b9`  
		Last Modified: Tue, 14 May 2024 11:44:22 GMT  
		Size: 65.2 MB (65196404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd0b2c691a41774071c0d9dd21f2ac31d580543d1b70cd9eb6e4ca27aae33b3`  
		Last Modified: Tue, 14 May 2024 11:46:47 GMT  
		Size: 217.7 MB (217669143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:44994ebe239276f8c148f94904212fe0e082dd7a6a06509a0b841baba3204e9b
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.1 MB (404129957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c27e94800d6d03b5ef7856567848c95031b762ed4d0284cf0eff3b0c9d93ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:21:02 GMT
ADD file:48cc1541210c6108c0251f6f008cd7e9eb30330f4f7a0e4ca8f13863de6afe2f in / 
# Tue, 14 May 2024 01:21:05 GMT
CMD ["bash"]
# Tue, 14 May 2024 07:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:02:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 07:05:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:bae7d269c4dd7d40de29faa635851f1c684cc32fdc792af4ff32efd2461c744f`  
		Last Modified: Tue, 14 May 2024 01:25:52 GMT  
		Size: 56.5 MB (56538197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cba953fb3ef8f77266c250f5f1e3517eaee2b356a1467463a6aa091c29b3d81e`  
		Last Modified: Tue, 14 May 2024 07:12:49 GMT  
		Size: 27.0 MB (26983263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3beb418175c6418b6d04d65091d4af4454b996b35118eb49bfd7288fa5a5eeaf`  
		Last Modified: Tue, 14 May 2024 07:13:09 GMT  
		Size: 71.7 MB (71704756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:666e37da3df3c94824cb116466c272922f2a7c733cad8460357b2504dc816849`  
		Last Modified: Tue, 14 May 2024 07:13:53 GMT  
		Size: 248.9 MB (248903741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:a8a6cba424fbb8acb65e7459c95265712378982cd5dfbbc849ab2fc0d182f18f
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **425.2 MB (425163913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895c9e1fbf05033a4f4607b05de62de26b589467a64610c4aa368e44ed99ad6a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 01:08:59 GMT
ADD file:18cb19ec2784efee4339c923ec316987819836eb7aad9280180eeca7729ae78c in / 
# Tue, 14 May 2024 01:09:01 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:30:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:32:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:38:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e438edd6428d670b6cea990c6caad079c8929366cc17e63aaad3fad6d8aaa661`  
		Last Modified: Tue, 14 May 2024 01:11:42 GMT  
		Size: 51.0 MB (50961424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e0d23029d29d3802db61889c19c99463249e5cb15c8c9edcf99017419bbf7b`  
		Last Modified: Tue, 14 May 2024 01:39:45 GMT  
		Size: 24.0 MB (24031978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ee6c77bd5ae96b2a3d9ab1089946c965a1a40231cecbf5bd726f0d397837b2`  
		Last Modified: Tue, 14 May 2024 01:40:53 GMT  
		Size: 65.6 MB (65646012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe41b9eb8f07e9c6e67c4cf4ae6b4fe894f733f429286173f646100119905c`  
		Last Modified: Tue, 14 May 2024 01:45:57 GMT  
		Size: 284.5 MB (284524499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:5bc0f1580f7da7dd52f12f0fb6a45bc148ad7a5b1f37094d065634e86715364d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.6 MB (371563717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f14b04d8b3d5f404a739ef30d225977273df38f670b35a7cdb00df85d22db2f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 14 May 2024 00:43:54 GMT
ADD file:34bf2264b5be5e585bc909c05f313cebb02329e956459b02e719a727804b5ef1 in / 
# Tue, 14 May 2024 00:43:57 GMT
CMD ["bash"]
# Tue, 14 May 2024 01:23:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:24:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 14 May 2024 01:25:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d8beb42479d9c358247f3312313f4b01304d06a9f4350f46669bc0340b164395`  
		Last Modified: Tue, 14 May 2024 00:48:47 GMT  
		Size: 52.3 MB (52293312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe716d1139dcfb0e4a0ac4867ff5d98684c037b80d0741511a7238159f33b964`  
		Last Modified: Tue, 14 May 2024 01:31:04 GMT  
		Size: 25.5 MB (25547590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1304310af4bca11dbfe21a9c4024e96521d8ac5f79eeb909c372706c5604a8`  
		Last Modified: Tue, 14 May 2024 01:31:19 GMT  
		Size: 67.5 MB (67453873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c512ee7e60445e2908d19d2738b076dfc41b764ba56a3e9509b8e8a8319a68`  
		Last Modified: Tue, 14 May 2024 01:31:53 GMT  
		Size: 226.3 MB (226268942 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
