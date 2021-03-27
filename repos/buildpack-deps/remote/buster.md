## `buildpack-deps:buster`

```console
$ docker pull buildpack-deps@sha256:ff6c309ddf5b2021da0f1bbdde5020be3840113058c50863fc05ba840c4db4b3
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

### `buildpack-deps:buster` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:aeef6d8d20edb0dc1445e2a6a4ef58f4213db8c7eaba7ac13f66afc7310c26dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.4 MB (312413139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ee03c4ccbd4ea22b42e07c5bbf733115bd9791035b13c5fb73646b9ea26166`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:20:41 GMT
ADD file:89234bb2f86c7eb890235a48904d1c9898a8d287a525c4fe5698d4a04cdd8f12 in / 
# Fri, 26 Mar 2021 15:20:42 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 05:53:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:53:35 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 05:53:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 05:54:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8bf9c589d5f9475f1fcc050e02308d6b4eeb86eab7752ef948a13693e81a6aaa`  
		Last Modified: Fri, 26 Mar 2021 15:27:11 GMT  
		Size: 50.4 MB (50400278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c70e46d8b5f0e1d77797b7a0565b7a316bd8c7c024f5cca82592128af142dac`  
		Last Modified: Sat, 27 Mar 2021 06:03:41 GMT  
		Size: 7.8 MB (7832558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea848ad42f0d1676b3a0ce709208ba3fa154cd53370c50e7cf8e580c63d96ae0`  
		Last Modified: Sat, 27 Mar 2021 06:03:41 GMT  
		Size: 10.0 MB (9997159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe137f8d2641315dd2f93c46dfdb671ce7399edc1f44f10cc68984f2809d8e`  
		Last Modified: Sat, 27 Mar 2021 06:04:05 GMT  
		Size: 51.8 MB (51839972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b13f6ed9b0cab6a0e5a875bd6ecb04c0b0bc1cd98a1600fbaf5b2f49a4c7190`  
		Last Modified: Sat, 27 Mar 2021 06:05:00 GMT  
		Size: 192.3 MB (192343172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:09466d4352cf33a36e4646eedef162e0446f3686dc33f6f769d256098998d02f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.0 MB (286039867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ce310506f15274ba76fa9cbfb90cb4bc247185140157753c3e7874ccdffe8`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 07:51:21 GMT
ADD file:8451124009ea487b77e0efd08279d813677a58a69c3e008efffe72456f5b4cd4 in / 
# Fri, 26 Mar 2021 07:51:25 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 09:10:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:10:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 09:11:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 09:14:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d38b01f6f9cb629c11a3283c08ac8942a1dabc09a0fd1cf882e144886c4d4c2d`  
		Last Modified: Fri, 26 Mar 2021 07:59:52 GMT  
		Size: 48.1 MB (48111655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5b79e4c1a18c62ae0b58fc10bc99ce795232cbcd2cd5aacdda45457357bf228`  
		Last Modified: Fri, 26 Mar 2021 09:27:37 GMT  
		Size: 7.4 MB (7376462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4722e17bbecf50bf547d60af44536f7fe5f2e819630c31abb41dd678e56c40b0`  
		Last Modified: Fri, 26 Mar 2021 09:27:38 GMT  
		Size: 9.7 MB (9687518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02aedf3b95b92593cff7caa2a868b2adc310bc9b40c76820162cfb61f4467959`  
		Last Modified: Fri, 26 Mar 2021 09:28:02 GMT  
		Size: 49.6 MB (49573869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3952d5d93c54c5c1b47b9f0baaa648e341fe8da32b3fc962b059bf140aa1ed0c`  
		Last Modified: Fri, 26 Mar 2021 09:29:00 GMT  
		Size: 171.3 MB (171290363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:97af7621ed24f0c2e1a84eab59226cfe794741c509e05a95eed075a70fcef4a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 MB (278240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09803e44e9353631027de1ea702e5049dc0b813510962cda9c47d3dacc62d0d9`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 11:17:10 GMT
ADD file:b3e1f7b8ae0587f7850210420c8dd6da7fb60fa87c5863e6fe5a8bab1bdc7abc in / 
# Fri, 26 Mar 2021 11:17:11 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 13:22:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:22:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 13:23:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 13:25:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2703ee001e01b49055599d26cac8b1a472b75d8643e8a00ab281b97e3fe6aefd`  
		Last Modified: Fri, 26 Mar 2021 11:26:53 GMT  
		Size: 45.9 MB (45868006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f00d516e34bfa5a11e13fd33e0649e2bfcfa443418341f1cda5463ed8ee8046`  
		Last Modified: Fri, 26 Mar 2021 13:51:18 GMT  
		Size: 7.1 MB (7123912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac789cd7e7d8f8003e7ac6b6bbf96d3859a2318c4569114ccb686ffd779ce119`  
		Last Modified: Fri, 26 Mar 2021 13:51:16 GMT  
		Size: 9.3 MB (9343659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e16bfec3cd4c49403ed5b98e6216074d4f3c68c5dc09e6e12252c09aa8952cc`  
		Last Modified: Fri, 26 Mar 2021 13:52:03 GMT  
		Size: 47.4 MB (47356546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd8364950cc87a0ab5051809b3c724b0484c8ed4b04704e823d1683dc82a32d`  
		Last Modified: Fri, 26 Mar 2021 13:53:22 GMT  
		Size: 168.5 MB (168548826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:2d9edd50be686b3d9828c917c474fd355ccc1dd42397b527516e37151441c3aa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302926539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a6a2a800ef2fbba8ebca110fd9b024bef192105c7ef205ae46b50996fad9431`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:41:27 GMT
ADD file:536306ac674764a6a921b71adcbb4440797b916a0583b9270cd1565d62642e4d in / 
# Fri, 26 Mar 2021 15:41:30 GMT
CMD ["bash"]
# Sat, 27 Mar 2021 04:14:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:14:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 27 Mar 2021 04:15:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 27 Mar 2021 04:17:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:383261dafcc4f63ecae5f2d661d1ef8d0a5e1c9f4b1f12285115baca7d101d5a`  
		Last Modified: Fri, 26 Mar 2021 15:48:21 GMT  
		Size: 49.2 MB (49196215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a8073d5d993eeeb13d2b5798a56220bed01add2f8e543d1a68cf5bdeb13b3a`  
		Last Modified: Sat, 27 Mar 2021 04:28:03 GMT  
		Size: 7.7 MB (7694449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e04ac5d1463667a0a3b2db65c9975df4dda175b8d5442808d4b141537d5531`  
		Last Modified: Sat, 27 Mar 2021 04:28:03 GMT  
		Size: 10.0 MB (9984376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be813e6ab58661299ea055f3b4c3080523e549d0874073a5c2699c5a33082d44`  
		Last Modified: Sat, 27 Mar 2021 04:28:24 GMT  
		Size: 52.2 MB (52164238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4593b8a7f7922609406fb610deec926888503254a2de7d6ce4cd8699f1c5299f`  
		Last Modified: Sat, 27 Mar 2021 04:29:11 GMT  
		Size: 183.9 MB (183887261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; 386

```console
$ docker pull buildpack-deps@sha256:a035a0f9fa66778516cd12c7ed9940c06833a8996b9bfc687e703dac5dcb11c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.8 MB (321821743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1465ae430be90035d98953208432488523be1d8f8cab49f49830cb6efdef8aa6`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 13:52:53 GMT
ADD file:631a0d940844da5859827f6532f16d070023eb5af86b98b26e8225892a728141 in / 
# Fri, 26 Mar 2021 13:52:53 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 22:43:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:43:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 22:43:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 22:45:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:94f8ae80c7bd585581d232dff8e781c1feaab54ea8d41718d95f0c1059908488`  
		Last Modified: Fri, 26 Mar 2021 14:00:56 GMT  
		Size: 51.2 MB (51160351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f4518622de265d7d3f5069177f5b74a159365d671532dd8008b136906f5bc2`  
		Last Modified: Fri, 26 Mar 2021 22:56:04 GMT  
		Size: 8.0 MB (7997773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a088421a3906a0c48a07e35676054ae4ed2982936d931624723f6d6c6c1e53e`  
		Last Modified: Fri, 26 Mar 2021 22:56:05 GMT  
		Size: 10.3 MB (10340027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46f38ff13dccaac573470e0e14ff2b88a265abe995ffaa863e5690821b2ee7a`  
		Last Modified: Fri, 26 Mar 2021 22:56:41 GMT  
		Size: 53.4 MB (53437511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c9835606549334ddcb60c816a40c05e319d77fb747ce09981f18c4b1f84ae1`  
		Last Modified: Fri, 26 Mar 2021 22:57:57 GMT  
		Size: 198.9 MB (198886081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:dc5c54890eddccf3eeaf8ab0c6b7ac4c05da40fecfdb7078ac3544d25e544ac1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.0 MB (296977313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e85db0e5cb67965f182f9e17ad8a6c34699a54bcc704524eb40a72a04e7484`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 08:09:33 GMT
ADD file:24fb0f672b9623c5b9e2dc416fe7b91a485519962826a3def620d449c72052f6 in / 
# Fri, 26 Mar 2021 08:09:34 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 18:19:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 18:19:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 18:20:10 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 18:22:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:45e930b5a161529bdb19c7b813062fdeb224d004c1a5a716c817094752214853`  
		Last Modified: Fri, 26 Mar 2021 08:15:45 GMT  
		Size: 49.0 MB (49029292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ad80a148224544b054bd02d9e38d4e3faab1fd0f5fc036b1fef76b47e3fdee`  
		Last Modified: Fri, 26 Mar 2021 18:30:40 GMT  
		Size: 7.3 MB (7251155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f469c4240f70d8f2677ee4262b580b494bdb76348d54127726bc52308ef1504d`  
		Last Modified: Fri, 26 Mar 2021 18:30:37 GMT  
		Size: 10.0 MB (10016333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:834b70d7b92eec946956f610ecfb902f11596ce8501cb6ec617e44f7d3608ca5`  
		Last Modified: Fri, 26 Mar 2021 18:31:32 GMT  
		Size: 50.8 MB (50843088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb73d00aacee035255d5c019f5d0c868ad7ff4ad8914d8b907fed18ed0d8861e`  
		Last Modified: Fri, 26 Mar 2021 18:33:44 GMT  
		Size: 179.8 MB (179837445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cb1fd1c4561bd2139246286408045d3f826614fd4ef132f46b58fd299cee5944
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.8 MB (333773461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23af64f87612a0d961d18d082ecbc44b60f6bc2fb5b7abf87072e6d3a1438985`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 15:13:48 GMT
ADD file:2e3cbe75ac7fb7b716e5b7411062bb9ce510f3317d00ddbfd608a5057931cc9a in / 
# Fri, 26 Mar 2021 15:13:55 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 17:37:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:38:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 17:40:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 17:55:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2280757cb36e3eef6465890eb70453bb9f66e271e373f08ae5e9d7a3307c5fe4`  
		Last Modified: Fri, 26 Mar 2021 15:21:30 GMT  
		Size: 54.1 MB (54136619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de5b549e9718d8f1d72fed2093ec025063ce0d94eb6fe18e4f59d6233dc1231`  
		Last Modified: Fri, 26 Mar 2021 19:40:42 GMT  
		Size: 8.3 MB (8271707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8700bf4e1832c58cc634f3cc177e25538b86637e529844e6f8e340f5b4acd876`  
		Last Modified: Fri, 26 Mar 2021 19:40:32 GMT  
		Size: 10.7 MB (10727704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3650b3afac8fc5a8b47e5ce2681df05154740219a9355d33d04418e90f4b78`  
		Last Modified: Fri, 26 Mar 2021 19:43:11 GMT  
		Size: 57.5 MB (57456809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2201bcb3f7630cea267e25821259e17467f146339142332ea0b0f14ab8d92be9`  
		Last Modified: Fri, 26 Mar 2021 19:47:30 GMT  
		Size: 203.2 MB (203180622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:buster` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0cbfbc9ba80b22244ebcb6dd0b1cd77c9cdf4fab570874b4280d72dff14afd27
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294479936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ef3583c988bb37a9819fbf488bd8164f0be595d8433d4bed39db4f0f9a1287`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 26 Mar 2021 10:53:31 GMT
ADD file:a8707fa1aa1620bd4a2cfb08af992575ed92583d76d9bc5cdf7512c966ef97ec in / 
# Fri, 26 Mar 2021 10:53:35 GMT
CMD ["bash"]
# Fri, 26 Mar 2021 15:44:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:44:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Fri, 26 Mar 2021 15:45:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 26 Mar 2021 15:47:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1b0086a5cca01c7491d8c2f15dbad8cb1c1829a7d6d1edd7f8c3dd02be85f2b`  
		Last Modified: Fri, 26 Mar 2021 10:57:27 GMT  
		Size: 49.0 MB (48968913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b853ff3a647fb66a2e5b7307061cdfcb221462bf3a73b0a84e58f90ac3b881a`  
		Last Modified: Fri, 26 Mar 2021 15:55:02 GMT  
		Size: 7.4 MB (7399988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286674edc11eb23904d49908925aff4fe5babc031d3c022fff443a078dd87e21`  
		Last Modified: Fri, 26 Mar 2021 15:55:02 GMT  
		Size: 9.9 MB (9883250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e62476e7ae0d7567aa0af0346254446c4959eb64b48882d260b31cdd605477fa`  
		Last Modified: Fri, 26 Mar 2021 15:55:21 GMT  
		Size: 51.4 MB (51380222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198ee48346222bfcd069741f6da6532c1279cf5e837291f69ca43429e9e5784f`  
		Last Modified: Fri, 26 Mar 2021 15:55:53 GMT  
		Size: 176.8 MB (176847563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
