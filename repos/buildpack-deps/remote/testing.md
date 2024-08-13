## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:fb7113eb99aad37f83be15b0759ce3f814dd1c9bd54df0ebc403578c652af5ec
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:6cb51ae8eae5ec3ce7f3ec350915ccae6b541b521adacb8456d16be0771c81b5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.4 MB (359383752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4407507b0be57273c84cc8e6f66d720821a7a39fed54b0187d2476663f7d09`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:22:11 GMT
ADD file:a2a54a01545a139e680d47b64716d1b9faa13cfedbe015124f93c561b7c8cf6e in / 
# Tue, 13 Aug 2024 00:22:11 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 00:47:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:47:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 00:48:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:805956af4eee3ab822c97611cafc9a57a586c1386772c91babe5075c77f79efe`  
		Last Modified: Tue, 13 Aug 2024 00:26:39 GMT  
		Size: 52.8 MB (52841189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8000d3eb244249a76a53e7b3f03c8e999bbac83be7058bc1aa1fe0eebb494baf`  
		Last Modified: Tue, 13 Aug 2024 00:52:48 GMT  
		Size: 20.4 MB (20428585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75784ed4e534b2a8c61e811f3ae902dd7265dcbdd4784c9d0a1e99630fb6e3c8`  
		Last Modified: Tue, 13 Aug 2024 00:53:05 GMT  
		Size: 65.4 MB (65370635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1247732ff7d24b76cc160cc1ef3080dffbe5cecadf4bee97be75bdd50da3d9`  
		Last Modified: Tue, 13 Aug 2024 00:53:38 GMT  
		Size: 220.7 MB (220743343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:f16dd90fed099bbdd38c9ba2b4043c2f6dd5fff753f8e83efcb01f53c54aee5f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340730804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e1602b1478c15c9a4d7e0895ad2894d4d31414497f18460bc450208deea5af`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 22 Jul 2024 23:59:14 GMT
ADD file:03b45e1df3fc6931a8ddcada5ff0a44361f55a5f77b85b332a37efac67af70c7 in / 
# Mon, 22 Jul 2024 23:59:15 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:48:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:49:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:51:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7c6b0161e34fdad02b8c4ce71aed07442e95f3916056ffa8fc8957d554429aa6`  
		Last Modified: Tue, 23 Jul 2024 00:04:42 GMT  
		Size: 49.8 MB (49807789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aadbc8644d3857b913228d91ab9cef7cad02ed0c4961160ca60a012db531734`  
		Last Modified: Tue, 23 Jul 2024 03:56:12 GMT  
		Size: 23.4 MB (23409933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3995f67f100684b8a4349bea104130c9a88c087b6156a290542809abaf92fee`  
		Last Modified: Tue, 23 Jul 2024 03:56:39 GMT  
		Size: 65.5 MB (65524112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6e5d20634a81bc4b6c92c003ee534fb6e97c79718d23d099b71e138a19b8e9e`  
		Last Modified: Tue, 23 Jul 2024 03:57:24 GMT  
		Size: 202.0 MB (201988970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:77e38d7aa99a2e0cb7e262cc703690c283c00862288360178c22022695df5b0e
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321697298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:032c751d25fd26bece446525e54e6934ccedf99662f558a6584db2e9ca8d68ca`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 03:05:07 GMT
ADD file:b71b90e852d24ff72e11c891781becf7dff5c6b7913fe6f75d4afaaf9dd0fb77 in / 
# Tue, 23 Jul 2024 03:05:09 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:43:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:44:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:45:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6a5c1f2df69e68e08287b3688c735ace9ad27b45503738288df9d10ef7066ce1`  
		Last Modified: Tue, 23 Jul 2024 03:10:02 GMT  
		Size: 47.3 MB (47313443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0cc17ffe2d1d252bf936d01f2e7c153c81aadb436d6f199344bf17351709fb6`  
		Last Modified: Tue, 23 Jul 2024 03:50:59 GMT  
		Size: 22.5 MB (22485255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b90386b6142530b1ede165d6dd3a0cd162bcd3ddd68e43f48c8f76f8ada03618`  
		Last Modified: Tue, 23 Jul 2024 03:51:24 GMT  
		Size: 62.9 MB (62860451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b2ab6b90f24721261dec59e268b9ba45d61a39ab16580eb2fc884cc1af4ac2`  
		Last Modified: Tue, 23 Jul 2024 03:52:04 GMT  
		Size: 189.0 MB (189038149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:9f10a8475810f2c2d592419b7c5719ef5d06a777dc62e46deec85f5780225a15
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.9 MB (352922735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f7b572589d05089575808b5690fe012e226c3eb471d242353689145e5c038d9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:41:11 GMT
ADD file:44df8bf38e0a6481ddb1093ad0c25ca4508a15c2b5d1c0733757db62627a7413 in / 
# Tue, 13 Aug 2024 00:41:12 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:07:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:07:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:08:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8858b14d914bd710ce161898770a04753f6d66b911364becd105945179fc07fa`  
		Last Modified: Tue, 13 Aug 2024 00:45:37 GMT  
		Size: 53.2 MB (53152442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cbc2390559926818fa461fbc23891f666f695df10963c68e66dbcd7d2a33119`  
		Last Modified: Tue, 13 Aug 2024 01:12:05 GMT  
		Size: 20.2 MB (20169643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f885d3fa750607fbd2f71e34070f91d1e6ad0cf13800756907e5eeb2a71a2eec`  
		Last Modified: Tue, 13 Aug 2024 01:12:19 GMT  
		Size: 65.4 MB (65414213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e489edad87279139fb9ce1fead44360dfb336ec312291d0b8ca9cdd02a51688`  
		Last Modified: Tue, 13 Aug 2024 01:12:47 GMT  
		Size: 214.2 MB (214186437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:eb8bff1d818def7a2f22ea0f49a8685fa94b9917603df0642628116b1a30c508
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363874327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70deb4dfacb021a563799df9a83678c946ed3a56efb8cb6244b5b2d6af11605e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Aug 2024 00:40:54 GMT
ADD file:9b748afacb31779094b92d19b7c5d9f886ed5db3b0944737e2a8ba99f7693903 in / 
# Tue, 13 Aug 2024 00:40:55 GMT
CMD ["bash"]
# Tue, 13 Aug 2024 01:11:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Aug 2024 01:13:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5c467332b7b5117922107a3e97e80e3a634fa6b47d841b15a9b5b2022ff8e9ab`  
		Last Modified: Tue, 13 Aug 2024 00:45:56 GMT  
		Size: 53.8 MB (53777497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d5e4079dd728cdba618039a6a9ad0704da86ad75fe54b71916daf9ed246990`  
		Last Modified: Tue, 13 Aug 2024 01:17:35 GMT  
		Size: 21.4 MB (21445114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c48d5537246281a2b042db46345f63c991852c265f95f1491f160d1b2439b318`  
		Last Modified: Tue, 13 Aug 2024 01:17:57 GMT  
		Size: 67.1 MB (67124784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee207a11e4a6de69d2bf4707298d7d6291e3b054d299d2964e51c9aef6ee01e`  
		Last Modified: Tue, 13 Aug 2024 01:18:43 GMT  
		Size: 221.5 MB (221526932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:086ee42fd7bfcbcf3a180d3a1fb8cd492372909dca9ac35acf6f30908f5d6b98
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.2 MB (336180671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c9924d6cd88082f4605e70e21cbb36a72f69d506bf2427203ffbb64b4af9841`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 00:44:48 GMT
ADD file:392fc10c04bd3df02b9ce57b447e54a4d1bcdfb0ec61a622808e7db6f2f1914f in / 
# Tue, 23 Jul 2024 00:44:54 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 01:50:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:52:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 01:57:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:4c50956a8a7195506ef530c7c5f445057322dc9fe660c45a79ea6c6084874804`  
		Last Modified: Tue, 23 Jul 2024 00:56:14 GMT  
		Size: 51.6 MB (51636151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff87574102eceba634bda143ff5b2bf4b17818f5418215956831655aa15d6f1`  
		Last Modified: Tue, 23 Jul 2024 02:08:39 GMT  
		Size: 19.8 MB (19771003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eee36f9299929b13c64e8d1dcbbecffbc23ec614ec5279d3468b3cc790fe0439`  
		Last Modified: Tue, 23 Jul 2024 02:09:30 GMT  
		Size: 64.2 MB (64222016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4466f890a1001c0f56f2d169603e31a1e4180b6e1c7a95244e03020c696c07fe`  
		Last Modified: Tue, 23 Jul 2024 02:11:46 GMT  
		Size: 200.6 MB (200551501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c0231f23e687071af6193d3f0efe7be3b212b3ea430c78ed6f8239d66a92b110
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370097457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90c1fa43090877b8dfc38d6d93cdb85f0bae92c5bfc0a34b06b25c9908342eb8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 01:29:19 GMT
ADD file:3a2bd17a40219dbb040555571523f8df1fea9b1d1a82249388c40cefedfa6de9 in / 
# Tue, 23 Jul 2024 01:29:22 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 02:38:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:38:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 02:40:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ef086634154fd58171058df19eb35df551381968a0480be4625baa26e8bd8a54`  
		Last Modified: Tue, 23 Jul 2024 01:34:29 GMT  
		Size: 56.7 MB (56722073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58910df9409127e8ce8b003f5bc4570e63366685c5b298d2bb94fc69d37fd17b`  
		Last Modified: Tue, 23 Jul 2024 02:45:21 GMT  
		Size: 21.3 MB (21295446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432aca4b63ee1a3a6c2c0c85f637c9ff06323c852e1a5363d3eaf9b36ec6bafd`  
		Last Modified: Tue, 23 Jul 2024 02:45:39 GMT  
		Size: 70.7 MB (70683207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0b716eafc6c8d8353c17c7c5d4fab52f3e2e2faa1180bb4d0761b66a184629`  
		Last Modified: Tue, 23 Jul 2024 02:46:18 GMT  
		Size: 221.4 MB (221396731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:b82e36ee67e0cb1b63575257de321a356d70d95f7859923b926ed40667d7d01a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.6 MB (334590501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34de17661113981e29208c56c9e5a0c3adc6da76e0f0dde5d6b1ea77592a668`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 Jul 2024 02:30:46 GMT
ADD file:5991487b53c92b85f56a9cb6ec51789428cf5b58777f5dee12014b0223fc1434 in / 
# Tue, 23 Jul 2024 02:30:48 GMT
CMD ["bash"]
# Tue, 23 Jul 2024 03:11:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:11:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 23 Jul 2024 03:12:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6deaf86d1b7bfd5bc637ea83983f978199741e71e1597a41b9ad7983be78ad34`  
		Last Modified: Tue, 23 Jul 2024 02:35:01 GMT  
		Size: 52.4 MB (52414237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24dd707523e73e3eba57ef16b7ac55b16771f34411fbf8a78ce790f60d615035`  
		Last Modified: Tue, 23 Jul 2024 03:16:57 GMT  
		Size: 20.5 MB (20479164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e13abee5c4577fc2e5e5ccd45eb4abcc067e815317edd4eb7fb89c6b9ff137b4`  
		Last Modified: Tue, 23 Jul 2024 03:17:12 GMT  
		Size: 66.5 MB (66483586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b246619b57093ef2ffbfca7ad46965ab0172ecaa73b81ecb7f975cf22e368de`  
		Last Modified: Tue, 23 Jul 2024 03:17:39 GMT  
		Size: 195.2 MB (195213514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
