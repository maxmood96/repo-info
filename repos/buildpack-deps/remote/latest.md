## `buildpack-deps:latest`

```console
$ docker pull buildpack-deps@sha256:746c53cc6e164dcd9af1516b9f77720f4e3cd34c01effc2367c244e2445dd7db
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

### `buildpack-deps:latest` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:42c43e33fe8c1a6bf904f2fbf28d55478ae44ec31011f7d3fe9ddc1f758be5da
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.9 MB (348885468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a46ede60b8536ce2cf5f75c2029332ed9c89be8f592d6e338881c511c607362`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:50:34 GMT
ADD file:ca6d1f0f80dd6c91b8ba1d1adf77d7af6d0e5f2f493a2858e384c11874314395 in / 
# Wed, 10 Apr 2024 01:50:35 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 05:24:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:25:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 05:26:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:609c73876867487da051ad470002217da69bb052e2538710ade0730d893ff51f`  
		Last Modified: Wed, 10 Apr 2024 01:55:11 GMT  
		Size: 49.6 MB (49560360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7247ea8d81e671d079d67f3a9909315ef4641b45db90d62a1b18e3430c1937d4`  
		Last Modified: Wed, 10 Apr 2024 05:34:49 GMT  
		Size: 24.0 MB (24046793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be374d06f38273b62ddd7aa5bc3ce3f9c781fd49a1f5a5dd94a46d2986920d7a`  
		Last Modified: Wed, 10 Apr 2024 05:35:08 GMT  
		Size: 64.1 MB (64140565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4580645a8e50b87a19330da289a9b1540022379f2c99d3f0112e3c5c4a8d051`  
		Last Modified: Wed, 10 Apr 2024 05:35:44 GMT  
		Size: 211.1 MB (211137750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c80efdb16aef6cefa72ad9215e5b6cf55b58e693338b5d23838f696c6904dc91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (316013788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4782661ccbbb2a70fe0f5604ff195eabbe8082d1169d406598d70d2562c3a304`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:48:43 GMT
ADD file:b0965dc0b90d6c10055f9e01eee401939303a005eff01dfc0ac17671ac10c89e in / 
# Wed, 10 Apr 2024 00:48:43 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:43:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:43:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:44:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:db9b031fc6f21cd210f5feeda489a6e10c26355e778fbdaeca7ec9da4a730942`  
		Last Modified: Wed, 10 Apr 2024 00:54:05 GMT  
		Size: 47.3 MB (47316142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ffbd9696eb657ee7a1f58c3ba55b7068e9217f964a268f6c9f74a7dd54e30c`  
		Last Modified: Wed, 10 Apr 2024 04:55:15 GMT  
		Size: 22.7 MB (22725022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a129a04f2d6b83a7f3a316a17496ec1b1a884022ea93fc33decc4cb7520e38`  
		Last Modified: Wed, 10 Apr 2024 04:55:38 GMT  
		Size: 61.5 MB (61515822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf0e0e8befd59b55c6a9b9cab341b48b4727d523d5b2d09b7e6f1948f4682ca`  
		Last Modified: Wed, 10 Apr 2024 04:56:17 GMT  
		Size: 184.5 MB (184456802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d2b275b164eceaad9b8902c98a635344263344ffeb4161b17aeef7c225c72a13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301425851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63ae65ed27d7a44f334c28ff5bca4b8605e85c622053ede90d59edd243b8a96`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:57:54 GMT
ADD file:30e85746fe77290a5de7286ebb7e2484b39554122eadc92de3df4ef4d95de9ff in / 
# Wed, 10 Apr 2024 00:57:55 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:42:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:43:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:44:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:debd7c42d7ee74277f743dba14187c21ed8be6cf4f57abbaeb7b88c779282f09`  
		Last Modified: Wed, 10 Apr 2024 01:03:59 GMT  
		Size: 45.2 MB (45158610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1564e42498f84ce1d5bb6808049f9c674335b23f95ba63cf15c09549e3990e59`  
		Last Modified: Wed, 10 Apr 2024 06:59:53 GMT  
		Size: 22.0 MB (21950348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea816b946832e576a6e2cfe5a7a28caeea429092724dc7daabb1e183ddd4817a`  
		Last Modified: Wed, 10 Apr 2024 07:00:21 GMT  
		Size: 59.2 MB (59213244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f06ca0e9dd61a104b8a520d84acce1978bf9c5574bb1c0d9b8cabc3205ce8ec`  
		Last Modified: Wed, 10 Apr 2024 07:01:07 GMT  
		Size: 175.1 MB (175103649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:bc7fa82b3515bd322ab2b4b8e0d5090e2450a0361254a9c53f62e7f6df7fd325
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.7 MB (339708505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a923360338a28b3914a7e7fb735c969f83c70f2a9348dcdb83d9ed82737944d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:40:12 GMT
ADD file:d795219dc83a41b5bb4106e62eebd31ceef0aae1b81541156eae5fe98e89337c in / 
# Wed, 10 Apr 2024 00:40:13 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 04:22:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:22:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 04:23:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1e92f3a395ff98a929e797a3c392bb6d0f05531068d34b81d3cd41ed6ce82ca4`  
		Last Modified: Wed, 10 Apr 2024 00:43:42 GMT  
		Size: 49.6 MB (49596265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374850c6db1702573c7004d630027931be318b2d71cb28e890e2fcd0f0730712`  
		Last Modified: Wed, 10 Apr 2024 04:31:58 GMT  
		Size: 23.6 MB (23582868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:421c44fab18bc9f4c62ca481e074d50b3a036e7c95c7607b6d036c34d67c5264`  
		Last Modified: Wed, 10 Apr 2024 04:32:17 GMT  
		Size: 64.0 MB (63990996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9717a38adec9939307bba3151627c24c2bbac069b221c2fcb0500a40f2736ec`  
		Last Modified: Wed, 10 Apr 2024 04:32:48 GMT  
		Size: 202.5 MB (202538376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; 386

```console
$ docker pull buildpack-deps@sha256:75bad1b160d42e671df362a792f70245750dc59fd182c983c142e2638432d39d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.5 MB (351517819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d32e6161d729cab74e65e5db8596538c11f741312bc2f2a868ce6efd2077b4b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 00:56:58 GMT
ADD file:790f7a239f36cc7d8fd7fba66cd64aaff5f743c1c06e080820f865bae8f4a8c1 in / 
# Wed, 10 Apr 2024 00:56:59 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 07:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:53:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 07:54:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:417ba0ba1bcbb46434cbd64273ffc8edbe2c1921e58094e580e87c3b8e518701`  
		Last Modified: Wed, 10 Apr 2024 01:01:38 GMT  
		Size: 50.6 MB (50587234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3845b288d815c745f12b9d8f5713e916e9d585644e3574c14b698e39da51082a`  
		Last Modified: Wed, 10 Apr 2024 08:05:45 GMT  
		Size: 24.9 MB (24884730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e5c516778392288fdc27cfc451916d0d1153e04fbb6687af2b9622dea744f5`  
		Last Modified: Wed, 10 Apr 2024 08:06:09 GMT  
		Size: 66.0 MB (65987074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0cf485acf1709a8d4f069eabc7f5100b17a3a2c8e434831de60567f6d520c2`  
		Last Modified: Wed, 10 Apr 2024 08:06:59 GMT  
		Size: 210.1 MB (210058781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3e131fedd6c0a053f4d92db50d59e106405e5047e2b38db2db93bd1cbf4dc08a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.9 MB (325858634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9827aaea1a13889e5939e08ab8f7c05be47b277bcb8f5da059cec0ab3b14c450`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:05:38 GMT
ADD file:4d32a17a925fe03541568abf911d846953d3660b326987a74427b0262134b3c6 in / 
# Tue, 12 Mar 2024 01:05:41 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:05:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:06:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Mar 2024 02:11:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1888556fef8803d385bcda912bec552fdbf67dbab0adac6cadf266d746cca55`  
		Last Modified: Tue, 12 Mar 2024 01:16:25 GMT  
		Size: 49.6 MB (49563114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f64944212b4456db3039905773dd6dea4c4590560c38ae7716d5dfa12559e8`  
		Last Modified: Tue, 12 Mar 2024 02:41:43 GMT  
		Size: 23.6 MB (23630647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638fdd2230a0e3b195fa0e78e24eb4739e6c5ad8a94c3bb93aedbaf4fad008ca`  
		Last Modified: Tue, 12 Mar 2024 02:42:36 GMT  
		Size: 63.0 MB (62965889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02977c85a258d317066e5a1e6febc79a4caa2a830ee66f596c866db50d3361d7`  
		Last Modified: Tue, 12 Mar 2024 02:44:46 GMT  
		Size: 189.7 MB (189698984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d8161a1838713d0b2a91ac15806b463e220259a9677936bd4bdbf84a9a13e4ac
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.0 MB (363012582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bfbdb9c609baada517a8f317d17824bfba02a57cde1b7a6e696403697080d0c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:26:15 GMT
ADD file:12519205a7ecc1a9b92b9b26c967bf9f7204f2e0b9c81cb9a147b10a29b0715c in / 
# Wed, 10 Apr 2024 01:26:17 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:28:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:29:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:33:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6dcf23c0df5604eb9aa3050ab9c36d44dec4ab1448d2c229f4beaaf0f7fa503`  
		Last Modified: Wed, 10 Apr 2024 01:30:37 GMT  
		Size: 53.6 MB (53562477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9a49dc2918c681cd1306002e0306d198b0ab9f74366235b251cb85c930eaaa`  
		Last Modified: Wed, 10 Apr 2024 07:16:20 GMT  
		Size: 25.7 MB (25696598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7558a95a0d29869e7f316194c1d23abcbbe4d8c3340f4d3103f670b9d4af3eef`  
		Last Modified: Wed, 10 Apr 2024 07:16:43 GMT  
		Size: 69.6 MB (69581154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab0dede385435598179e3ab86d7c4094cf59880d986b82c837b42b0649d5afa`  
		Last Modified: Wed, 10 Apr 2024 07:17:27 GMT  
		Size: 214.2 MB (214172353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:latest` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1f8aac9ec337221531d1b6cfb31e56b0421e3c433053080f65a495a303c7f8a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.3 MB (318259093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f3be8826d6f4e57d92074c4fb014c78be2fa8b842f3812670cc264631c1631e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 10 Apr 2024 01:11:40 GMT
ADD file:4b6b256d3328c1d19403b3eb0f375b5d33724b65f790edd27be4adca49c66e4b in / 
# Wed, 10 Apr 2024 01:11:45 GMT
CMD ["bash"]
# Wed, 10 Apr 2024 06:50:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:51:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 10 Apr 2024 06:53:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:17f5c0a7be3d447b0aca6569b534fabcb69c578072a0cdb81f078fd4872eba70`  
		Last Modified: Wed, 10 Apr 2024 01:48:11 GMT  
		Size: 47.9 MB (47922706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a94fdcea32a650c77c01028838d670a5840f3ead5a1cf5526e922967f0df66`  
		Last Modified: Wed, 10 Apr 2024 07:30:52 GMT  
		Size: 24.0 MB (24043531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdaec0019454e24574ad418259f50f0d68508dcf92f31f05ca5d5ad33dcf43bb`  
		Last Modified: Wed, 10 Apr 2024 07:31:10 GMT  
		Size: 63.1 MB (63126889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfce7e73c441e81b6b2408dea6732c47c87f4c633b91c6d77faf8891b50ab262`  
		Last Modified: Wed, 10 Apr 2024 07:31:45 GMT  
		Size: 183.2 MB (183165967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
