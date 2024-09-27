## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:7bef2d647f85a5c033d016e5534ae04085033c9b799b16e03bd6512b8a98f36d
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
$ docker pull buildpack-deps@sha256:ee76f9c492d0f4072868e40d1250a1ce243aac136384fefc31fe01e9aeea11e3
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.4 MB (367357446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b457d4ee4cfc4ebb25157e51045e62481112e0746dfe3d9f2508e00b1f64c0e1`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:30:28 GMT
ADD file:cf7f6034921acc5129d114b0d008fe8ab426ef9a8efc9b4514f253804c22cad9 in / 
# Fri, 27 Sep 2024 04:30:28 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:10:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:11:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:12:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d22ccc6b10e3548ee74d1cbbf8e7aeaa81ab8f9be02c19e64adafccd0de28e5d`  
		Last Modified: Fri, 27 Sep 2024 04:34:37 GMT  
		Size: 53.3 MB (53250042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dae9d245be83a876418da4287aadc60061be7b905df337290be90c8e2bd942b`  
		Last Modified: Fri, 27 Sep 2024 05:16:24 GMT  
		Size: 20.4 MB (20404612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d824605d3973d8333c12588307d4b7865a9d16a172cf713a69bed064281a179`  
		Last Modified: Fri, 27 Sep 2024 05:16:40 GMT  
		Size: 66.3 MB (66298648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8e9cccb32adeb73089e38bb77d73d59c2177bbb495bbbc4bac305a228188d9`  
		Last Modified: Fri, 27 Sep 2024 05:17:14 GMT  
		Size: 227.4 MB (227404144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c37c2fe099ca8c852db765ea796c72a5565fce2c9957748d192a6d2330d45ce7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.8 MB (335802621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959ed346fcd14aab877dc44925c39b738c268a59db692c7ca7224cecb1a1c14a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 03:19:29 GMT
ADD file:4e733f6ab5ca47e96afa5484ac2356542259685b0f38d5370aaf3ff6efd60b52 in / 
# Fri, 27 Sep 2024 03:19:29 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 04:00:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2dab2d41b4d3c1013596d851ef68dd96a59ea71db4c50a8e9daec6977beb1e9a`  
		Last Modified: Fri, 27 Sep 2024 03:22:02 GMT  
		Size: 50.1 MB (50141188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45409b0518e0782369823c9bfaead974fdd198f9b729525b7784d928cf3f7973`  
		Last Modified: Fri, 27 Sep 2024 04:04:32 GMT  
		Size: 19.4 MB (19423742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03463b6c07bccc1364fec128e533c62c4e2533ee53250fc1153a70167b6f44b`  
		Last Modified: Fri, 27 Sep 2024 04:04:50 GMT  
		Size: 63.8 MB (63754764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03773ce488248829376500af9b84cf97fcd39ed3242f9e2187079b56c71ea969`  
		Last Modified: Fri, 27 Sep 2024 04:05:25 GMT  
		Size: 202.5 MB (202482927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:7dce74814ac71c3c1a030db777e581f1ccd7233b7ba27541b483b18f3662dbe4
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317241853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e048cf3ab5d5edb6ad2b4ddbaaeaf5b699f98ca7db295e0a9416b4eacc47e2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:14:39 GMT
ADD file:7c02e68cb0d4c1b545df6c3c1548fdfbb0b8728190927f1aa0a481628eb80842 in / 
# Fri, 27 Sep 2024 05:14:39 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 07:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:33:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 07:35:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:55055767cac3db3f353667eecf5967bd4d61aaf6f68b845d1c472311762c6497`  
		Last Modified: Fri, 27 Sep 2024 05:18:38 GMT  
		Size: 47.7 MB (47656889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe7ba8ffc1ff9cdaa583c4b78a356d900036e41391f4ad532ea17ef7226ff6`  
		Last Modified: Fri, 27 Sep 2024 07:40:59 GMT  
		Size: 18.8 MB (18770645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39cad0c26ab0027c184690fde3603662a1fe5a37591c336a98696770ac66936e`  
		Last Modified: Fri, 27 Sep 2024 07:41:21 GMT  
		Size: 61.2 MB (61234643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e907df1326f4d0916b686b69508feaf27c5bfc2aa38710924f377f75b7fdbe09`  
		Last Modified: Fri, 27 Sep 2024 07:42:01 GMT  
		Size: 189.6 MB (189579676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2dcc03ae0e069e97bd427e3523013055888d7649c17b947c1770b684987e7b37
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.0 MB (361024922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34275d796bc4304378c9c4f5a93c485125d7f567b96e662711a64b21fef728bd`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:54 GMT
ADD file:0530740e6d33fef9d1d8ba1df1cda3d2bbd45ee34654975f96a8cd318b315f82 in / 
# Fri, 27 Sep 2024 04:38:55 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:21:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:21:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:22:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:99a192f51b57a678feb659bcbaa8cde28d31be7455d5517ca87c1d8fba2866f1`  
		Last Modified: Fri, 27 Sep 2024 04:42:11 GMT  
		Size: 53.6 MB (53594265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88fc848450eda758c5f4c056230d289d3bacb82835760763661a9b5aebb3758a`  
		Last Modified: Fri, 27 Sep 2024 05:26:37 GMT  
		Size: 20.1 MB (20139073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd393ac9d5f3e6f4ef01c240e4ee33361f9163326dc4fe0c98ca544756cddc12`  
		Last Modified: Fri, 27 Sep 2024 05:26:51 GMT  
		Size: 66.3 MB (66302891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac170a650f31dab130f92fb8708276d55343d8d7ee851c19b5b9f257acdd6f4`  
		Last Modified: Fri, 27 Sep 2024 05:27:19 GMT  
		Size: 221.0 MB (220988693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:1ded01fb58e652afea4c8e7094453b5af95454a57d274207a2bb3eb8d67ba93a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.9 MB (371902498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feb6475fc00c3a209abc95fa65afc37a1ed13142d0bb884b32069569704b4147`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:59 GMT
ADD file:b0f2319c396534f2fd08b2706fb1f0fd78e74e08c267d5e06e0eb0f82fe07ff0 in / 
# Fri, 27 Sep 2024 07:23:59 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 08:02:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:02:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 08:04:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:977268bcf0b2cba57760ad7ace3863e248276a9851a6938bfeda275ed37ec343`  
		Last Modified: Fri, 27 Sep 2024 07:28:47 GMT  
		Size: 54.1 MB (54077811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7fbbad98fe4fa8d720a3430a25da5207444dbe7555c066831aea5fea6901da`  
		Last Modified: Fri, 27 Sep 2024 08:09:26 GMT  
		Size: 21.5 MB (21485772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c71b0341053ee8776ca7ecfc201a051da349ec1f8e5c73b5d4a043fd3154532`  
		Last Modified: Fri, 27 Sep 2024 08:09:48 GMT  
		Size: 68.1 MB (68105180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f792864bd7cba3961b251eec2e1ee9f352895552addc1e17511d0c39b02e56ab`  
		Last Modified: Fri, 27 Sep 2024 08:10:36 GMT  
		Size: 228.2 MB (228233735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:2cfdb4463136f7a7fd6a964fc3abeffe5f208f66260fd0eaf0c70642e5386419
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344950889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d66d337adcb0f1ef97b6662438438bd5c5fdf7cf39e624d1a8af498fbb4b2d2e`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 09:03:44 GMT
ADD file:7373f4e4970ea9ada45c8717ca5498ffa4ffd9d16a9261475e1291ae954742c7 in / 
# Fri, 27 Sep 2024 09:03:49 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 10:42:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:44:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 10:51:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b63745dc97c5bfb473a84b3b12d099f6a8a1ca3adb2bdb16407181689c5a9724`  
		Last Modified: Fri, 27 Sep 2024 09:12:19 GMT  
		Size: 52.1 MB (52125578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ffc0b3c363e12b941d7e80d3bb54718d788594c92b04828cf954025257521c`  
		Last Modified: Fri, 27 Sep 2024 11:04:48 GMT  
		Size: 20.7 MB (20727164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3d0102a70641af727b17e4dda29d3e752776fe5f927c48dc6ba42534da6baf`  
		Last Modified: Fri, 27 Sep 2024 11:05:38 GMT  
		Size: 65.1 MB (65067190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3393aec747705ef0a675939b6f883a7ca72a36da98e766e42ca2a7286e7af3dc`  
		Last Modified: Fri, 27 Sep 2024 11:07:51 GMT  
		Size: 207.0 MB (207030957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:33011240df37cdf38b23d38f03d17a12051d05e4b3d94c36635ddd57eafd1713
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.9 MB (377881836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51344e88f1f121524c87aeabda4282378ca7a7659586aa483fb44b98340e72a2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:18 GMT
ADD file:61be8fbc8c48a038743e523ea5539b007c504e38025630b54f774464a5b21963 in / 
# Fri, 27 Sep 2024 05:33:21 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 05:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 05:58:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 06:00:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:7d9882c6fe69b65aaa672267378b325d49eb761a1518c6646ba15eafea787b1f`  
		Last Modified: Fri, 27 Sep 2024 05:36:38 GMT  
		Size: 57.1 MB (57123161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa5a7efb15e28989001836168c26f86cfa942d47c522ef07c07c02abbf8fb2a3`  
		Last Modified: Fri, 27 Sep 2024 06:05:40 GMT  
		Size: 23.0 MB (23025627 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83256233144f0df0689578c0a89c181e74e6ea6cc435661a805b2a60809bd43d`  
		Last Modified: Fri, 27 Sep 2024 06:05:59 GMT  
		Size: 71.6 MB (71626121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751e854e69a77c78cd9663a65ff9e955dcc052e392333a04a5bf6bd4c25ebb97`  
		Last Modified: Fri, 27 Sep 2024 06:06:39 GMT  
		Size: 226.1 MB (226106927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:17af248bfbe1e8ab33b0e561eb6c0ef3686f0cedd557e35c4853def42575cd35
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **442.9 MB (442888142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c77ba538f9adf10fd862946d1177b5d2576c85e90415beb3ccfb0210ae5248c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 04 Sep 2024 22:25:42 GMT
ADD file:f7660b52d63bdf7c045c4722f75fe4e353e88b57bffc834348ad141ea0d12995 in / 
# Wed, 04 Sep 2024 22:25:44 GMT
CMD ["bash"]
# Wed, 04 Sep 2024 22:55:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 22:58:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 04 Sep 2024 23:04:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:f9fbdbff518ec38d5367f0b03978c04c3107f39b06d2bb498f646b4903fd13db`  
		Last Modified: Wed, 04 Sep 2024 22:31:12 GMT  
		Size: 51.5 MB (51473852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea5ef465799bf40fb820e96c6cdb0b3ca4823cc42d2ef644d6b9684cb164fde`  
		Last Modified: Wed, 04 Sep 2024 23:07:16 GMT  
		Size: 20.0 MB (20026801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d55a7954253b1f3af858d514d5a50598aad4e02214e66bf45ff119714d2d5fd0`  
		Last Modified: Wed, 04 Sep 2024 23:08:21 GMT  
		Size: 65.4 MB (65415937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b8269d3170ea5e0ed9b1314bea3a8b5949e212597ca4322a5cda142d67f33c`  
		Last Modified: Wed, 04 Sep 2024 23:14:00 GMT  
		Size: 306.0 MB (305971552 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:02d80f6064f4d0e45507e4fb2c58bcaea875e315d0609b0be609a084766835cc
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342486230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3180d78e39311bbb86438bcfae83a1c25a9665ba35a16eda55358e509b4479f`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:46 GMT
ADD file:5c5ad29b01b72e50aceb20af8172a88e23803553ed45c73a28a9a138856ba70d in / 
# Fri, 27 Sep 2024 02:43:51 GMT
CMD ["bash"]
# Fri, 27 Sep 2024 03:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Fri, 27 Sep 2024 03:16:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:17aa999733edd287bf5bd51ab2a58ef17211e311db82e8024e72304b5186e2aa`  
		Last Modified: Fri, 27 Sep 2024 02:47:37 GMT  
		Size: 52.8 MB (52808143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8d052710c80bb8f1ba5c4daebfc8ac149ed5b56a5185e5d6bd1a75f49bba31`  
		Last Modified: Fri, 27 Sep 2024 03:21:13 GMT  
		Size: 21.4 MB (21426030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cedf4fdb3f455010b1f7eeb3d9f24a25a7fd469356a31a9f5f4de26d8238f1b`  
		Last Modified: Fri, 27 Sep 2024 03:21:27 GMT  
		Size: 67.3 MB (67330712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a95e4129bf276881f4c92fb92d3cf0bad3b55875c49bb65e8462f3ef6fecfb5`  
		Last Modified: Fri, 27 Sep 2024 03:21:55 GMT  
		Size: 200.9 MB (200921345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
