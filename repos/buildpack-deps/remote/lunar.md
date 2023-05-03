## `buildpack-deps:lunar`

```console
$ docker pull buildpack-deps@sha256:4ed5c241f18d2b103e13e83339129564f79c5f881dc48db9f5e586821e730cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:lunar` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:72ad873c98760942ca5d465edffae7211e80ccba27958674a87e2ed6811682fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.8 MB (263779689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109c993812239ed394fa44c10012d2997940875c6fd0b8150169b452a8c4d767`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:04 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:04 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:04 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:05 GMT
ADD file:0974d2aeef46c39070cbf74e10bf8644b9753060809b3c7100126a1bcb448f12 in / 
# Sat, 15 Apr 2023 04:51:06 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:34:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:34:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:37:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:43bb70e8bba148f5c5a4d50f8a5204951f795a069a2cd25b2e37ebafdd10afc7`  
		Last Modified: Tue, 18 Apr 2023 01:36:35 GMT  
		Size: 27.6 MB (27604045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72868f35a1e9600e9177cd873e711b17f41b81258e96f625749bf3cdc1ce699f`  
		Last Modified: Tue, 02 May 2023 23:45:22 GMT  
		Size: 9.8 MB (9781462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24353b37d60fc58c0d8aa5a4b347d986a0b3f1123f3fd2c3858acbd69af8b45a`  
		Last Modified: Tue, 02 May 2023 23:45:36 GMT  
		Size: 44.3 MB (44342458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8817520b7a2e0024c5e8a72456b1f818036e40e1db4691bd9c1f0797a75e12ab`  
		Last Modified: Tue, 02 May 2023 23:46:08 GMT  
		Size: 182.1 MB (182051724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a44ab7e595ea6a61300375b81e980b3227452de4f6139fd79d21d0bec3b38dad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228684948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e98502ceed6def07bcc4a3627f00428c38545188e529e0609030f3fbe14f9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:38:02 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:38:02 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:38:02 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:38:05 GMT
ADD file:9f0981aade24310bb7a4c492e6ec76e24f146f4efd6782ddba79ece3b8afe7b5 in / 
# Sat, 15 Apr 2023 04:38:05 GMT
CMD ["/bin/bash"]
# Tue, 02 May 2023 23:29:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:30:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 02 May 2023 23:33:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc0ec898907bfe3505695fd5ae23b4cf5d6d180fdb036e767c23cc35a2abc39b`  
		Last Modified: Tue, 18 Apr 2023 01:51:15 GMT  
		Size: 25.4 MB (25437825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e170addce9795b6038144ffe99cd922705650aa1f48bdd240773e32470086971`  
		Last Modified: Tue, 02 May 2023 23:43:57 GMT  
		Size: 9.1 MB (9103985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba500d7f7d20fcb8c648baf959b4a4bf8916b5f782b49731cb716c22013e8447`  
		Last Modified: Tue, 02 May 2023 23:44:17 GMT  
		Size: 48.7 MB (48687523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9140d292819a9c0d3b4f12351ac9d74687f4c2f8fe7654d52479dd864f241061`  
		Last Modified: Tue, 02 May 2023 23:44:54 GMT  
		Size: 145.5 MB (145455615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:7eb8a34ef8517f80859dc448e809c9c9078e6b8dacf23a6750cd0eae459b9487
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.3 MB (254284885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a583d5b43c43b667581b05b79463eba4d8cf6b9295ec519f94633ce5f61562a1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:41:09 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:41:09 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:41:10 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:41:17 GMT
ADD file:0a45cfb0f66cc6191e34ca0d42987f4ee1f86f70c5ee9a29ec3e353ceea7ce51 in / 
# Sat, 15 Apr 2023 04:41:18 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:29:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:30:09 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:30:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:33:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc6919ddce2a233f58cc3e7dbe578e059849f4571e49c4a84c7c981f17a89835`  
		Last Modified: Tue, 18 Apr 2023 01:36:11 GMT  
		Size: 27.0 MB (27018561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dfffa12a1f77a99f18745a89a98d7c560b403d259aaabb2ea7e8099aba267`  
		Last Modified: Tue, 18 Apr 2023 01:36:08 GMT  
		Size: 6.2 MB (6217841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b46934c541eaff8b64481ad9212943b45e46655b2e916d0a2a1edf56c835075`  
		Last Modified: Tue, 18 Apr 2023 01:36:09 GMT  
		Size: 3.7 MB (3653186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ff58527001798506a9dc32ce859a3d047cc557aa033359f185d2451be24cf5b`  
		Last Modified: Tue, 18 Apr 2023 01:36:24 GMT  
		Size: 44.1 MB (44077916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55eb81a3584d1feea46abd6869b71852c54408ee766a0895b86d4915752208de`  
		Last Modified: Tue, 18 Apr 2023 01:36:49 GMT  
		Size: 173.3 MB (173317381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5090fa89cb4d665c6b029976d4d929e424390503a1f35135e12612c86f8d073e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.5 MB (288502540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29bf47b159469fa22c03c0456e2d2221865676486fbf95b847453b413e41ca0a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:51:08 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:51:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:51:09 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:51:11 GMT
ADD file:57838c4589ddbfb3bfb239d9d6749a36f0d7201d8788fa4293dfe9ad93308e40 in / 
# Sat, 15 Apr 2023 04:51:12 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 00:54:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 00:54:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 00:55:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:00:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fcabd7528fca87cc5a63f487865487cc2f6832df71a8c871f40b369f4f0f945d`  
		Last Modified: Tue, 18 Apr 2023 01:04:41 GMT  
		Size: 32.0 MB (31996733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd02da4adaf96b5e8dea2c0a2846b3cda00cb99c8a2af6a5da9996399bdab78`  
		Last Modified: Tue, 18 Apr 2023 01:04:36 GMT  
		Size: 7.4 MB (7364592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6bd36dd881e6a900302ba6370fbb475b14bf1dd9e35dc4209f84fb8c5065fb`  
		Last Modified: Tue, 18 Apr 2023 01:04:35 GMT  
		Size: 4.4 MB (4413806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11b8a0da4d0a3c624fb719be6321b9020894b77b2028fb6352c38403a1a77e6`  
		Last Modified: Tue, 18 Apr 2023 01:05:04 GMT  
		Size: 48.9 MB (48945236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f1c1f4dc0b62d9d13e02a7d9066e7642d3a6440780c8ff95db3ba050af43976`  
		Last Modified: Tue, 18 Apr 2023 01:06:01 GMT  
		Size: 195.8 MB (195782173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:lunar` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:51c88a6dfccf081c6f31980cfce4183a66f188868648a9d6382e802317134227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235447894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3f0864f3aba4bc5def98d2e8129dfbc7c9b623b4f64aa2d42cee71bc56f8a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 15 Apr 2023 04:52:00 GMT
ARG RELEASE
# Sat, 15 Apr 2023 04:52:00 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Sat, 15 Apr 2023 04:52:00 GMT
LABEL org.opencontainers.image.version=23.04
# Sat, 15 Apr 2023 04:52:02 GMT
ADD file:fbea81511df0975bdcf894e5be93dc02670d76233449f6221b0a6752e6178646 in / 
# Sat, 15 Apr 2023 04:52:02 GMT
CMD ["/bin/bash"]
# Tue, 18 Apr 2023 01:09:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:09:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 18 Apr 2023 01:10:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 18 Apr 2023 01:12:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:92338e21c9dcc2f2402a20239390e6f35f1a8beaa9ebf17ca317ce011b1cef40`  
		Last Modified: Tue, 18 Apr 2023 01:14:57 GMT  
		Size: 26.2 MB (26236111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1665ec17c4182267692bd75dd16a85d9e658f0f52656651e35f3c6856edf38f`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 6.1 MB (6066022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435dc1ff769b0f8daba446a3386907dc4fe1be7df7f69e61b212baf2fb17ce18`  
		Last Modified: Tue, 18 Apr 2023 01:14:54 GMT  
		Size: 3.7 MB (3678419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af9b4b3cd888e49ca9b73654104bd6dafd3b084b47dbe8b9aa070a6fec27c58`  
		Last Modified: Tue, 18 Apr 2023 01:15:08 GMT  
		Size: 44.1 MB (44087604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b8dfd448b2176a355c388f14e3c38c9a20244ab8c4a8f63df88fbe70b2f6630`  
		Last Modified: Tue, 18 Apr 2023 01:15:33 GMT  
		Size: 155.4 MB (155379738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
