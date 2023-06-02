## `buildpack-deps:mantic`

```console
$ docker pull buildpack-deps@sha256:89f6d6fe2ead16342b3fbe4278e4d56d268f3e62843c5ef1ed0f466c4a57b21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:mantic` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:598222098057efe73046bf6e2d956e81ec2d59da9e1ddd347ab2e0a3a7a8ba2a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.4 MB (270427006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76f2d79e5c5bac1c52a59d889e6debf6e5837feeb3c26b585d01f6aeea42132b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:41 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:41 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:43 GMT
ADD file:6bd9b5983097734c3050b464660da9015c0e2f93416920b8404ff7d28d8bccd8 in / 
# Sat, 20 May 2023 16:58:43 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:46:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:46:34 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:48:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f4522178b7858636c4ea7b5a5ea742eba69b4a5a1b2a1486003997120464124a`  
		Last Modified: Fri, 02 Jun 2023 00:51:41 GMT  
		Size: 27.7 MB (27659622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eacb572e31dc476c7b24479be4daeff80cd8c18b7d9b325b670825bb972e1db`  
		Last Modified: Fri, 02 Jun 2023 00:51:38 GMT  
		Size: 13.8 MB (13757827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28e128bfac9c2cf18019357be40650171050807c31d6f2f562ec1844e210db1`  
		Last Modified: Fri, 02 Jun 2023 00:51:55 GMT  
		Size: 44.4 MB (44367852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21eec27b8fb41ecd8a4d942be53e84f6f392a044c8b894bd67e95eaa6afe697e`  
		Last Modified: Fri, 02 Jun 2023 00:52:27 GMT  
		Size: 184.6 MB (184641705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:9d19820e589347044a245bab4852dca05abcf6907308e46109c5b409f52f43ac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.7 MB (234728780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ca466e15863cd3ab5a186daa120ebbffcd895d22cd0cd43fff794a018d9ceb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:22 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:22 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:22 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:25 GMT
ADD file:c7522b8ff46586b3057c8eae94d6cfc77299a4f2ccc3762e6263780ccc7c82c0 in / 
# Sat, 20 May 2023 16:58:25 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:51:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:51:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:53:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:562137b754651e3134bc25cd5345aa8ee488e4018a6b98dca99da8c6a698516c`  
		Last Modified: Thu, 01 Jun 2023 23:57:12 GMT  
		Size: 25.4 MB (25360044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e14e8697677cc5b120d6102abcd07fc40bbe1f33ce15bf65b69c87877e6721`  
		Last Modified: Thu, 01 Jun 2023 23:57:10 GMT  
		Size: 12.7 MB (12675035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a38306dc25634af4f237ffb8f2dbbab5c0aeb30a2801455a0289a5f7a16b35d1`  
		Last Modified: Thu, 01 Jun 2023 23:57:28 GMT  
		Size: 48.7 MB (48697792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99b7f19af3d48bfc6e27c3789b7482ab8cdb77cce124e3590b998628faea086`  
		Last Modified: Thu, 01 Jun 2023 23:57:55 GMT  
		Size: 148.0 MB (147995909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:da7c21bbbcd3127d6c97083d2f2daf34d83c2e98d898aec84f1b9db5e79f5b4e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 MB (259969893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c31d4006ad5ebe1b5c5d3663a95305e5c7c1319babc98a2654a8bca75bcef97e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:34 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:35 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:35 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:36 GMT
ADD file:39dff3364ce4bb79539ed5e58493be16a66d424e605cb774559830ba8452bc4d in / 
# Sat, 20 May 2023 16:59:37 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:01:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:01:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:03:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:59e1b7a20de65cc40ff963f40b4d97f1bea4a466e8941c9538a13270a948c2a7`  
		Last Modified: Fri, 02 Jun 2023 00:06:42 GMT  
		Size: 27.0 MB (27042242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2739609605be7ce435def151c1c15562a7fbd66a303de8403e883c503df71c5c`  
		Last Modified: Fri, 02 Jun 2023 00:06:40 GMT  
		Size: 13.3 MB (13348666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ebe7a7f701ec267f2de61e65f122b1d0a90d288f30c4f4ab023ea558d7e042b`  
		Last Modified: Fri, 02 Jun 2023 00:06:55 GMT  
		Size: 44.2 MB (44204286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a463dd153418a10946eaaf3afedf560b36d06c88194c00b1f2b71cf0887c4f9`  
		Last Modified: Fri, 02 Jun 2023 00:07:32 GMT  
		Size: 175.4 MB (175374699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:7c7400898f994205d29845aa75c6da27a9ff2a6321308216fb303fd75b3da847
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.1 MB (295115560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba8e2f3f0a7841dcbd492b6e71460ff783601a983150eab2307940180e23d0a8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:58:51 GMT
ARG RELEASE
# Sat, 20 May 2023 16:58:51 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:58:51 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:58:54 GMT
ADD file:83fb0f5b40d9233c6017f5c5a9e51e184b8f56b03c54fafa207e9ca28aa2df52 in / 
# Sat, 20 May 2023 16:58:54 GMT
CMD ["/bin/bash"]
# Fri, 02 Jun 2023 00:15:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:16:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Fri, 02 Jun 2023 00:20:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4be5c776967dd754e54ca2493882fdb223dfd4f76d65c4fe5b6d0dd055c5329e`  
		Last Modified: Fri, 02 Jun 2023 00:26:34 GMT  
		Size: 31.9 MB (31902988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7e0dc3412a7fb87bd1fb770ec1ec58a973b8cc3c422c029592ed974c7bcbfb`  
		Last Modified: Fri, 02 Jun 2023 00:26:30 GMT  
		Size: 15.9 MB (15854436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cff6200508ca9e53c9f73931adb9b3c0dce83d1efa07ef4eaab23cb15fb897f`  
		Last Modified: Fri, 02 Jun 2023 00:26:58 GMT  
		Size: 49.1 MB (49068561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe33af081ad3ce830c0956a477e90b5ed8afd8d753b5a58671728e825e8d72c`  
		Last Modified: Fri, 02 Jun 2023 00:27:57 GMT  
		Size: 198.3 MB (198289575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:mantic` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:e808273a49cd04aea0361ee5f0557eedd4b20a8def9b1cd6ce25893be1d825f8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **241.9 MB (241903336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7c5d6a3a64c6a90649933face3a07b2a0a46c4d5c19e403ad0570dcf14b5cff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 20 May 2023 16:59:20 GMT
ARG RELEASE
# Sat, 20 May 2023 16:59:20 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 20 May 2023 16:59:20 GMT
LABEL org.opencontainers.image.version=23.10
# Sat, 20 May 2023 16:59:22 GMT
ADD file:fb602b3f6c251d8267de1cf0525d0b38aab5966c848182d037bb2890557f0a6e in / 
# Sat, 20 May 2023 16:59:22 GMT
CMD ["/bin/bash"]
# Thu, 01 Jun 2023 23:15:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:15:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 01 Jun 2023 23:17:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e6197ead7faf6fa2f836b159dd66c603a28c581c4e273f6b664c86588a78ec95`  
		Last Modified: Thu, 01 Jun 2023 23:20:39 GMT  
		Size: 26.2 MB (26231487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98abbd746ec759f3d8e8b447407b1e0248bc8e38e037360bdcebb69899e8cd07`  
		Last Modified: Thu, 01 Jun 2023 23:20:38 GMT  
		Size: 14.0 MB (14018998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc44de0957139a61045543f4801b3145fa3f06e69b887ac90673e1c3da52f0f`  
		Last Modified: Thu, 01 Jun 2023 23:20:51 GMT  
		Size: 44.3 MB (44252551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a181bc5faaeffba7958cf6a6c7522c36f39e831f6af3377bca7f48a3ffd18b40`  
		Last Modified: Thu, 01 Jun 2023 23:21:16 GMT  
		Size: 157.4 MB (157400300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
