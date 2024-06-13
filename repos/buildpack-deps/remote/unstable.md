## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:afd24bad5dc4806be63fad3d4ac3724c6fe301ecdf83f6f9a043707f55a04a78
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
$ docker pull buildpack-deps@sha256:23742a24d183ff420647512e78ce459cb89eb479cea30d180cdec0175fc077b1
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.9 MB (345912159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37c42b3df689e76f103c1d1bb86546c10817577f7bb4471423d09c057e1f925b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:49:12 GMT
ADD file:53c5bacab4479c2281acdc8e18c636052e6d20212a45337d8a17b19319ec5ca7 in / 
# Thu, 13 Jun 2024 00:49:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:18:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:18:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:21:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a884fb5df6a69e4609683ee45a6be09afed09564ce4f6b3902caeb9298054718`  
		Last Modified: Thu, 13 Jun 2024 00:53:18 GMT  
		Size: 49.5 MB (49497721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23a34ed06c08a0ade11823d7031f7d8e27822e2579c680e8f6960a126d5c3c1a`  
		Last Modified: Thu, 13 Jun 2024 01:26:23 GMT  
		Size: 18.0 MB (17974516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e56a60eda8fe51134230ba91fc34d75d688a8e8668d0bc0836c49f14c886c82`  
		Last Modified: Thu, 13 Jun 2024 01:26:43 GMT  
		Size: 64.4 MB (64414283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae581ede8f2c1d7302c93ac10d87cd470c5a5641bdbc563bc1606c09aa60177`  
		Last Modified: Thu, 13 Jun 2024 01:27:28 GMT  
		Size: 214.0 MB (214025639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:477914b6fbdfc2a5308d84f4d0557e828580fc5fb583a97d294638388eaba72d
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.7 MB (326696137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:794beec7cc73358bed5b7ff44b555cf6e4c8f21b8bc10dcce4f2f234d5cc7644`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:58:58 GMT
ADD file:447d578cf14b4a73088105e96e789b86c902fce17f3abdbe2d9af6404943e16d in / 
# Thu, 13 Jun 2024 00:58:58 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:28:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:28:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:30:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5ce389400ad34c3c307d0ed4f17eb1ab2ebf0cace811962fd7529ddeb931a8cb`  
		Last Modified: Thu, 13 Jun 2024 01:04:22 GMT  
		Size: 47.0 MB (47006979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235b6587c5780c1c7e65c98dff1392373e5f0b3294f927a258767325ac74de69`  
		Last Modified: Thu, 13 Jun 2024 01:36:27 GMT  
		Size: 17.4 MB (17370774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd3f6ffc5c655060a11e9801093c4f6da417ab1bd25c0ed1d7f810badd59a1e`  
		Last Modified: Thu, 13 Jun 2024 01:36:46 GMT  
		Size: 61.8 MB (61768778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e59e48a8a26ae4b39d549817d9f6485a412bea366150e0b4cf93a1dc2ff4c20c`  
		Last Modified: Thu, 13 Jun 2024 01:37:23 GMT  
		Size: 200.5 MB (200549606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:daa240adc3a26e2cfccc8f82dd71f77925f6e95bc18d608dd874c8899a15943f
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.9 MB (369902961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9399dafa2937341b2f8e58f15cff1becc501382148d41cfe86b2f9edcbdb6e9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:53 GMT
ADD file:0df3518c1c665e2879ed3c7b7c5961b53fc28709cc135a245b209411a275c037 in / 
# Thu, 13 Jun 2024 00:40:54 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:25:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:26:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:27:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:844667f4b2125bd419ff2157667c09ca5b8d442b399e2db99e62277881555d82`  
		Last Modified: Thu, 13 Jun 2024 00:45:41 GMT  
		Size: 52.7 MB (52683111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de631d800a2d5597fbeefa6256f2a1b9ec1248adc1daeb69a836e05978fa6d5c`  
		Last Modified: Thu, 13 Jun 2024 01:32:52 GMT  
		Size: 18.8 MB (18771377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d43c1cffc0bde8580055dfb72c20e5ff7b0e65c7530d279c7ccb77fada1a6f`  
		Last Modified: Thu, 13 Jun 2024 01:33:07 GMT  
		Size: 67.0 MB (66991284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b2611f13f4ded7c5c4db9cec62d32aa647f19b894c8d49a71181242d891cdaa`  
		Last Modified: Thu, 13 Jun 2024 01:33:37 GMT  
		Size: 231.5 MB (231457189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:333e240091ae3ba55acd6c3de0b1975631a7acd0458fb0a447556bc4617a26b0
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.0 MB (382952788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590aeac83bac56baf8646254d28495861d39e591245e6bcc85a9fc2cf80e0079`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 00:40:29 GMT
ADD file:8452dc45806912ac27c72fbde099f24d3385b2fe336f125781076ac8fada56f2 in / 
# Thu, 13 Jun 2024 00:40:30 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:14:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:16:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:892c6905b91a2725baf7261577bc387b671ddd2ecf5bba2922a38096ad8e5eae`  
		Last Modified: Thu, 13 Jun 2024 00:46:12 GMT  
		Size: 53.3 MB (53304297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d90251148762e9b64a325035fd3aefcf26ce939ab1b44ed3e8097e28585f2b`  
		Last Modified: Thu, 13 Jun 2024 01:22:39 GMT  
		Size: 20.0 MB (20037479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97408847bd4bc01a7750cb15d364c1b778603f2d0c10e350ab59c571a518c4f`  
		Last Modified: Thu, 13 Jun 2024 01:23:01 GMT  
		Size: 68.6 MB (68587764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a44d02da26a64e916b188437fc3eb829bf06dc211923352addff42906c24621`  
		Last Modified: Thu, 13 Jun 2024 01:23:52 GMT  
		Size: 241.0 MB (241023248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:40c3656face54fea61efa09f88d14275309eaf2f728af49bf188790b67253f49
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.3 MB (353271641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6988d0814284ba42eaf3dbd77589908052c2766caa764b6924d0cbff4d5b133`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:13:44 GMT
ADD file:bc1c5f4f7dc974780be655fc08cd2e36c5d04921a942dd0065534fe0f2520661 in / 
# Thu, 13 Jun 2024 01:13:50 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:17:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:19:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:26:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:371a3512d511da5522a67af4d5945c86f5bf5015bc3be3dfc08ea50797400367`  
		Last Modified: Thu, 13 Jun 2024 01:25:20 GMT  
		Size: 51.3 MB (51279195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e19ab65511529aa4e809a989c916e7d1eea56540a36758da55666b6d063b69`  
		Last Modified: Thu, 13 Jun 2024 02:42:33 GMT  
		Size: 19.5 MB (19513685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a59683027da59c0bb0526447861a6a715f53ce57d4a231feeedcc859064169e`  
		Last Modified: Thu, 13 Jun 2024 02:43:27 GMT  
		Size: 65.8 MB (65791634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c1a82d886848eaaf9a129b694b52bc6d423bcd3a15d74fbbe168f5b1822eadf`  
		Last Modified: Thu, 13 Jun 2024 02:45:53 GMT  
		Size: 216.7 MB (216687127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:ea30753f1224f1f5cb5e34422188b975101357fe4d0ddb484978f73f59e08aa8
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.7 MB (390706449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc9dc035b1adea9f2d0d5c51b5f3dd943c5f235300052030e3157a364df7eb4b`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:18:10 GMT
ADD file:17f3c29affbf057347abf006bc2aa243347ef42e5dcd37286af3c79f3fe983a4 in / 
# Thu, 13 Jun 2024 01:18:13 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 01:52:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:53:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 01:55:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:edab80a24633b63ae0ba8926dd3e7105717650d226694cdbfeaa41301a651162`  
		Last Modified: Thu, 13 Jun 2024 01:23:25 GMT  
		Size: 56.3 MB (56296967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0cda58a29e7eca0ea797c77896694dad5c8ba0063d2386e0f1bcf721031263`  
		Last Modified: Thu, 13 Jun 2024 02:02:11 GMT  
		Size: 21.0 MB (20999280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01598ab5f3c9225be75c4028dc80f4a7779148be59896c9ea495823c6197e0e0`  
		Last Modified: Thu, 13 Jun 2024 02:02:30 GMT  
		Size: 72.4 MB (72443431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7aa75ae95c16172e4465e5205c61a34bfd2016d89c74bccd72151275ba50738`  
		Last Modified: Thu, 13 Jun 2024 02:03:13 GMT  
		Size: 241.0 MB (240966771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:fb402c32a0d7a46239e4bac3ae4e9e2b837d472557bf87726ea5b90311c856a3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.0 MB (416991573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e097f8a7c9e4cbba83e8a7b30a72328b9a87eb9536f56670761a9a4c282bf1ca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 13 Jun 2024 01:31:50 GMT
ADD file:5f145818f2852834c826623d73119954ead96eb9bce2d43c78acb87643e22613 in / 
# Thu, 13 Jun 2024 01:31:53 GMT
CMD ["bash"]
# Thu, 13 Jun 2024 02:02:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:05:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 13 Jun 2024 02:13:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6ac783982847dc2f82c444819c90a10bdd382db79de84981f527e1462e567adf`  
		Last Modified: Thu, 13 Jun 2024 01:36:23 GMT  
		Size: 50.7 MB (50715744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1659c611213bc35c1eb01ea12d4ad271643ffd53f1e2e2bc4b26608a2487a2b`  
		Last Modified: Thu, 13 Jun 2024 02:14:02 GMT  
		Size: 18.7 MB (18705876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fc926fbb86329f17c9d7a8101110c3dcd41d78ea4ae3f1d9f5edba14dde6dd`  
		Last Modified: Thu, 13 Jun 2024 02:15:27 GMT  
		Size: 66.3 MB (66255342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf57fed0a12235ec4e26b0c6ef510c211f6a00747da09d3b16578daa501a8e5`  
		Last Modified: Thu, 13 Jun 2024 02:22:49 GMT  
		Size: 281.3 MB (281314611 bytes)  
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
