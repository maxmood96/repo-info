## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:aa0c978ba1f9dd047efd1f0813773fa1959b74e62f82122c61a5f45204d05ecf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4ff80bd769b65dd85501684cdc4e819a46ed39638ec413258a90c08e6b962247
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.9 MB (311905592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ea119635dd515e55aa2d8a34af1fa35d2a5d0c22998ae58ff28637215f9df67`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:21:33 GMT
ADD file:4c836bb72137197bf8963c1982aba28db2b125a4276307783f46668bb4189f34 in / 
# Tue, 12 Mar 2024 01:21:34 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:56:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 05:57:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9a7bf5145e4a86e137c0a7612407b53eb4b97f73f4d6f15a64c2d52c682b500`  
		Last Modified: Tue, 12 Mar 2024 01:26:38 GMT  
		Size: 50.5 MB (50500797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f92106516f03d231db59cbea79958083f6e93317b065086e0c3d7ea6c401a3`  
		Last Modified: Tue, 12 Mar 2024 06:04:28 GMT  
		Size: 17.6 MB (17584732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50c719b870d0be3d68698a8ab9d2604ba1d9b85d3206a13ce6f1e5c50928dcc`  
		Last Modified: Tue, 12 Mar 2024 06:04:43 GMT  
		Size: 51.9 MB (51877435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a275b8bae6bef10ec9dd71151b41617e72eac0780ecbfe93ee1dc86db2f5e9`  
		Last Modified: Tue, 12 Mar 2024 06:05:14 GMT  
		Size: 191.9 MB (191942628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b4761ce8f33fd0256c24ca66d9e214b4def4275f792ed17b05d5a0bd1f313539
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277728447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0b3aac61bbb0a61c4a7044b56686673dc640b296ffa8d92bbe4f9451beb1940`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:59:47 GMT
ADD file:5f3389726cf59e3b1d0650186a49490baa1e933702b9cf9df5fca7adacd54104 in / 
# Tue, 12 Mar 2024 00:59:47 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:13:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:13:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:15:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4218e49953a4d45c8fc0862a697fdc774311ff33abed887ac34cc7b5b03ef005`  
		Last Modified: Tue, 12 Mar 2024 01:04:44 GMT  
		Size: 46.0 MB (45967270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ef5888a68a0506ce77bb71273482bc253eb745caed538f2af7471c91fef2983`  
		Last Modified: Tue, 12 Mar 2024 02:22:23 GMT  
		Size: 16.2 MB (16216521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec28d557d3104596d3ba5ab227e1e527ff8f93195f04af289dd5da1316ba29d9`  
		Last Modified: Tue, 12 Mar 2024 02:22:40 GMT  
		Size: 47.4 MB (47410735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb141b0531169976182ab39baba3c902bed903a2c25a2e2045f8c6cee114563c`  
		Last Modified: Tue, 12 Mar 2024 02:23:15 GMT  
		Size: 168.1 MB (168133921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bb7e022e9bc1cfbad07b9efb81d22c724a86aab30c7769950ea7a0d6ceac7130
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.5 MB (302488134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5a5efe5c6052414a5d5ff289e9a2bddbc111ae796933875d6253560f57c555`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:57 GMT
ADD file:969a4e1bb3ace306012b0fdb34a936b1c5aff4ed7670a054b38ce31e3c70ddcb in / 
# Tue, 12 Mar 2024 00:45:58 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:27:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:27:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 01:28:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8f2867cba3550760f11e3707290af4ab014e08a6171620407549210c558e3429`  
		Last Modified: Tue, 12 Mar 2024 00:49:48 GMT  
		Size: 49.3 MB (49289836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f662d0fd286524f0287f1ab689d234c733c6bd6efb38a645b2231168bbe94949`  
		Last Modified: Tue, 12 Mar 2024 01:36:44 GMT  
		Size: 17.5 MB (17455473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8987ebef52bd1e6f6f20b38f5dd0fa9030c75a5089144eabf4a20c7b2aa2605a`  
		Last Modified: Tue, 12 Mar 2024 01:36:57 GMT  
		Size: 52.2 MB (52225028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe09b4296b95b0c32948c55d4f978937b58f5a899208693bb4c304804492322`  
		Last Modified: Tue, 12 Mar 2024 01:37:27 GMT  
		Size: 183.5 MB (183517797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c599298d79066b772b81128b1a1620592b7f32ad6e4750cd4c1ca6372f362d7f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.3 MB (321315894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374e59245d31877d21714838a3bcd92de3c784fc49d659c13da5667752558d16`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:30 GMT
ADD file:654c015ee394379d17dbff41ad51721cde33b46fa1db3b0e9a7d54473d92d291 in / 
# Tue, 13 Feb 2024 00:39:30 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:21:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:22:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Feb 2024 01:23:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:33a96960e66e0a13921d9c0fbd1ff84e40544f75b84b3cb7124dc858fc844dc3`  
		Last Modified: Tue, 13 Feb 2024 00:44:58 GMT  
		Size: 51.3 MB (51255359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78788b06b363de6c8e3b44276527f47f5277530dc33ff6a512c93b0b96fb288a`  
		Last Modified: Tue, 13 Feb 2024 01:32:13 GMT  
		Size: 18.1 MB (18099425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c395b259eaee16d252933b055fc10e238ccf180dd0e226f790cc4d6d05ee33a`  
		Last Modified: Tue, 13 Feb 2024 01:32:36 GMT  
		Size: 53.5 MB (53491004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5394ce220a4fdfe5a7557da33b1d28ce42579dd6401bfcece4be46f785212cb5`  
		Last Modified: Tue, 13 Feb 2024 01:33:21 GMT  
		Size: 198.5 MB (198470106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
