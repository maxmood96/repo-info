## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:61fac766b35e83caaf7c0f72aa62815117d5dc68c094f2bd872781f1580e69d9
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
$ docker pull buildpack-deps@sha256:2fadd5965ddbb1b6fc947ba006047f357bc384ed5b845f892e6d8b6c7a14eebe
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368348507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4456cedeeb93eebe0f1e11b3f5a634ec02686089e3e9b021df7417230c7c0ce4`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:21:22 GMT
ADD file:2f0bf52b237d2aeea91dec200a2de7c5ae6b34efe77c934bb57f9d3d19f5eb15 in / 
# Thu, 17 Oct 2024 00:21:23 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:06:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:06:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:07:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c1a6eb9e541d6622604a2883c2b680cc3ec0ffdb4d333bf3622b65f135cb1fb4`  
		Last Modified: Thu, 17 Oct 2024 00:25:23 GMT  
		Size: 53.3 MB (53271874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd12486823035917e2bdfef20e61a67c184360d98ed6ebd28bb57588bf93a8a`  
		Last Modified: Thu, 17 Oct 2024 01:11:46 GMT  
		Size: 20.6 MB (20559740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea70d03627f3e5c406d1ee5dff15665aec2cced533a490d601ee7442319226e`  
		Last Modified: Thu, 17 Oct 2024 01:12:02 GMT  
		Size: 66.5 MB (66532116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81370ea3b478778c7acb7a9670c0d68b53757bc2055fe23cfe9e25806cae1c2d`  
		Last Modified: Thu, 17 Oct 2024 01:12:37 GMT  
		Size: 228.0 MB (227984777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7e95232f4447716af74bd2907bedc9ab047b94e7bdb4cfc15cb1cf4492f4afb5
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.7 MB (336701350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e528f9913cf5ebdc3bfd2c5f1ae6fdca4debe882d4913b75fe13dd04460aedca`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:54:41 GMT
ADD file:60f06c5e1590158022d322cc41b07cc01fa17e02a84be35114e99f05ec411c78 in / 
# Thu, 17 Oct 2024 00:54:42 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:27:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:28:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:31:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:cdb5fb3064b38bc0e5b5aae72dad6be74503e4faee528b87f7073a8a6ce9adfd`  
		Last Modified: Thu, 17 Oct 2024 00:57:47 GMT  
		Size: 50.1 MB (50147588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b51e9513f401d905da66d3e959803693c1c78e3059a3fd54de6ad45f59179fa`  
		Last Modified: Thu, 17 Oct 2024 01:36:39 GMT  
		Size: 19.6 MB (19568932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52911f6537dc2fd850c0c63bf4aa3806ec9b40b64d351e34d00f5df0a1434fb6`  
		Last Modified: Thu, 17 Oct 2024 01:37:00 GMT  
		Size: 64.0 MB (63988084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acb87602ce298bd118421d8a0f5456cad47ee48016fbe2aa008e1d427dbefcb0`  
		Last Modified: Thu, 17 Oct 2024 01:37:45 GMT  
		Size: 203.0 MB (202996746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

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

### `buildpack-deps:sid` - linux; arm64 variant v8

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

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b966178eda76dea66f452cb06f87f9906349dba82bbbd055da0e28ad91f15d7c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.0 MB (372969487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e980a127b4431a37149ed014ffa7e1d65e7e99b294288eb6fc7712cfa0b26b98`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 00:39:51 GMT
ADD file:a39a4e1fa9f977ce95bba21eda9e8c494e6af74b67bf3637c4ed4dfbcb6815b6 in / 
# Thu, 17 Oct 2024 00:39:52 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:06:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:06:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:07:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5e40dc1768587ca69bb610632a26014594f4d90017fbbf395667e0c4e317e3b7`  
		Last Modified: Thu, 17 Oct 2024 00:44:11 GMT  
		Size: 54.1 MB (54117977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15aaf6c71ee896572e8510fe4d438d0dbd76161c333521b2012d9264e2e14151`  
		Last Modified: Thu, 17 Oct 2024 01:12:12 GMT  
		Size: 21.7 MB (21665512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3baf36563cbaa64d32ebee9da5e6774f7c3ec5c4ccdfca4ab2bd2c321a22c66f`  
		Last Modified: Thu, 17 Oct 2024 01:12:33 GMT  
		Size: 68.4 MB (68352915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df250d2cf965e468007bccba284faeb8934d129f28b03bafd99c4b14fad6c3e4`  
		Last Modified: Thu, 17 Oct 2024 01:13:23 GMT  
		Size: 228.8 MB (228833083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:8e354256e268e95b4eb29793cf5442a60a571ebb0a9ea5333fa57af8d9e49758
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.0 MB (346019892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da56f0d01a64e286c3b8aed43478ed2441a3e37cdbe1e57f345af5e734ae1c96`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:10:11 GMT
ADD file:8ffd9575546e69884562db46178b841df2ba1ed04549599485b7c502f81ac4cc in / 
# Thu, 17 Oct 2024 01:10:17 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:50:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:52:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:59:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e3c6aca2e6ea9e1b19b3c46a60581e28de71137e5bd8fe9c8ea62365a8e75d74`  
		Last Modified: Thu, 17 Oct 2024 01:18:46 GMT  
		Size: 52.2 MB (52157899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8caa54e7215b92f68792f1b978dc23df0d8344fea83727a4b5758d7a94f9713e`  
		Last Modified: Thu, 17 Oct 2024 02:11:58 GMT  
		Size: 20.9 MB (20886491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378bf47a6c5edfd4ad9a37322329896d2917b0b410c7f41449f823883f86102a`  
		Last Modified: Thu, 17 Oct 2024 02:12:49 GMT  
		Size: 65.3 MB (65299790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36eee4379add186dfd518c292eb7926586afcdbd80524fb9da0627e98bee8333`  
		Last Modified: Thu, 17 Oct 2024 02:15:04 GMT  
		Size: 207.7 MB (207675712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:95f8dc6b9d534fb73f94dc2716623bf57a1930dd890d0db13e2ca8ca122dfd2c
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **377.8 MB (377765962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed9bc7b533f4e3ec7e3a3429cf0c5995b27faf10b7fdb016559a4c7432dad9f`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:19:05 GMT
ADD file:3f30d2b91e08061eb3185f2f9c67756024dc8f3e6cda74d75d6ae54a603cdd2b in / 
# Thu, 17 Oct 2024 01:19:08 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:45:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:45:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:47:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df36361b5ac72face21de9a14adcec98ba3abb2261a8339bf516725d8753f43e`  
		Last Modified: Thu, 17 Oct 2024 01:22:16 GMT  
		Size: 57.2 MB (57176824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d6fbbdfd760d192f962f091ac6ac50b83943b30afeeef05cb2189597ca0d4c`  
		Last Modified: Thu, 17 Oct 2024 01:52:34 GMT  
		Size: 21.9 MB (21945036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c8d006d9437ccf6825ce93da875340581aaede61b1bb556c25053444f5d60f2`  
		Last Modified: Thu, 17 Oct 2024 01:52:53 GMT  
		Size: 71.9 MB (71897145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f60d866924718e5a834ee211294703f7ccaff0c50b423716b8bcbdbadf15ee`  
		Last Modified: Thu, 17 Oct 2024 01:53:31 GMT  
		Size: 226.7 MB (226746957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4219b43dc777d41d6f85d0c160677d87619eb13b75f3158cd5218abb7610f899
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **449.6 MB (449638935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40cda9e1a8b19f0634dc0500a3dfb906412d655f75153f0909ff3ddaa1b30871`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Oct 2024 01:09:12 GMT
ADD file:9748961f840a27ae3342039309a28acc84e3a482f5ca3ece5bdaf9f92e7ebe33 in / 
# Thu, 17 Oct 2024 01:09:14 GMT
CMD ["bash"]
# Thu, 17 Oct 2024 01:41:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:44:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Thu, 17 Oct 2024 01:50:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:29cf887cb660615390407db841ad4c44be2414b9bf999ba668d93a8305675c7e`  
		Last Modified: Thu, 17 Oct 2024 01:14:47 GMT  
		Size: 51.6 MB (51562685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cffe06738a4c488c5af7baf511864fe81ba7e38149f28d93443e35a8d7d414`  
		Last Modified: Thu, 17 Oct 2024 01:54:09 GMT  
		Size: 20.0 MB (20025281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cae9f617aba80ede947d89c8c1533181fbf6bbf33b4f52cd58a464daf4cadf`  
		Last Modified: Thu, 17 Oct 2024 01:55:15 GMT  
		Size: 65.8 MB (65759438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4626b5f0a1b5e29bea40bdb350f939636cf2ba36351f5395f5d5c70852c7323`  
		Last Modified: Thu, 17 Oct 2024 02:00:59 GMT  
		Size: 312.3 MB (312291531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

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
