## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:293e07b4bf1416dd4f661c0c27688e51da05a3ddb26baa07c8821ce58b88cf1a
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
$ docker pull buildpack-deps@sha256:7dc4e920c8dd7c76cfa100138f52fa0f562fb3964c77e26c5cbe6ed6e6535213
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.0 MB (344982884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b8cd9b59abb7fdd67a7c9956c737bb3d1b65c562a5ca8e079ec879cb486e32a`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:31:25 GMT
ADD file:8efef3fd1e16c5994e0b27af5c19056cc369818d299aaf62b89b89ad82426fe3 in / 
# Thu, 23 Mar 2023 01:31:25 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:04:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:05:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 06:05:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:06:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ddb08f6d450933d22f98a93a56726ec0491dcd496caf4455cfe7066900409348`  
		Last Modified: Thu, 23 Mar 2023 01:35:52 GMT  
		Size: 49.3 MB (49291637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b67c216879c602a3357a3e051406068e953242d0d7b402dd7e6671d414199c7`  
		Last Modified: Thu, 23 Mar 2023 06:09:55 GMT  
		Size: 9.1 MB (9081298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:184c8a28afd4da0484a1f9c3cc7e52748726daac5cac85bc0fc702f666f1939e`  
		Last Modified: Thu, 23 Mar 2023 06:09:56 GMT  
		Size: 11.4 MB (11422514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65c6e206a59e86efff44db2d95c81b3eb92e784a910507906ef0fabd1c750fc`  
		Last Modified: Thu, 23 Mar 2023 06:10:12 GMT  
		Size: 64.3 MB (64258354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d78cf9510e3c5f639d777d6a4a7aabbdcc9b82ed86af114ac95b061ee4a6e6`  
		Last Modified: Thu, 23 Mar 2023 06:10:46 GMT  
		Size: 210.9 MB (210929081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cfab3ca8a8f26671e80ccdb59dd4ba9f96d324240fab5eca7fda5b7282e680d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313512864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98658392247eaba632e8d135986bbf3cb581ed4c064c7c09cc42508038e13052`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 01 Mar 2023 01:49:01 GMT
ADD file:4fadb88d3ead8d91349c79d7e903bbb8f6130b292bda6cb8099131210a815bc1 in / 
# Wed, 01 Mar 2023 01:49:02 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:21:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:21:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:21:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:22:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a03e1abdb2ebe924d64faf35eb6563891039999ec54a62f65419caf539ba6a88`  
		Last Modified: Wed, 01 Mar 2023 01:53:21 GMT  
		Size: 48.1 MB (48107781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d446d9cfc1201a906803d21a6e36423e22e9bebf24cf64bd16a4a3a73af61a2`  
		Last Modified: Wed, 01 Mar 2023 02:26:11 GMT  
		Size: 8.5 MB (8514426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14dc22595c5f06cd6d232ff8a3594b9aadef31095cb355dffad2b48a861717bf`  
		Last Modified: Wed, 01 Mar 2023 02:26:11 GMT  
		Size: 11.1 MB (11051502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0760e34b5fee30fa55ba71775caf6a3b2e755775ea03be4db0c03e5d83ff0a3`  
		Last Modified: Wed, 01 Mar 2023 02:26:32 GMT  
		Size: 61.6 MB (61563988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0bee41572d3fd2c79c2cec17ba9f302c4197090c7cd926637454ea269c1fcf`  
		Last Modified: Wed, 01 Mar 2023 02:27:08 GMT  
		Size: 184.3 MB (184275167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:13bc1f7227e4eb190e2425e9ae9baaa9afa595247f7c48578dae477f5206c282
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **299.1 MB (299089852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82add4ff4f01d1f31c7d61d6b83e243c99fc38f0cb8fbe94fc118eaf5a75103`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:28:43 GMT
ADD file:628ac1300ca273dba23c7d617164bc6e664cdebb4106910020d7b3dcb39429c8 in / 
# Thu, 23 Mar 2023 01:28:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 12:42:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:42:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 12:42:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 12:43:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:53d7f1f008e91cd29c47c933b404c16fc1d4cf64b8699ad1269e882f53ca6e2d`  
		Last Modified: Thu, 23 Mar 2023 01:34:10 GMT  
		Size: 45.9 MB (45911196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61016f9e9c2f44cda61da9f54267fbafe7fef3695caec3c87c6d5ae9eb452ae4`  
		Last Modified: Thu, 23 Mar 2023 12:46:05 GMT  
		Size: 8.2 MB (8168245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e4226b16c6b7093dc765001b6e5615e8150c8d19be6c96ea1171e1ad13654f5`  
		Last Modified: Thu, 23 Mar 2023 12:46:04 GMT  
		Size: 10.7 MB (10704470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889e5e2259a7026a6a42309e4673ccd18c4288dce5b85e2039cb7238e36ce3fe`  
		Last Modified: Thu, 23 Mar 2023 12:46:22 GMT  
		Size: 59.4 MB (59373909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd2df18bf0523ee48067a579083ad967febe18f6eda98aa82f65c4fbb8ff974`  
		Last Modified: Thu, 23 Mar 2023 12:46:53 GMT  
		Size: 174.9 MB (174932032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:a63ffd11342ac558338f8535c43a0d34241c92fcd52ae7cabbbcebd61fc4a879
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.1 MB (336111072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1624a01c9fe5d53011e9dbb23654960b9e19d0745249fae6121416a2b697c630`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:42 GMT
ADD file:56248f74ca6cf497dee2c80a5824447bf5ee5e730a9c092f440d9c666ec1c076 in / 
# Thu, 23 Mar 2023 00:45:43 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:14:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:14:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 07:14:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:15:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3a84baeeebe4b5ede833105ba5c2fe8b6102a8c47c386cc79b5833fea9489c99`  
		Last Modified: Thu, 23 Mar 2023 00:49:34 GMT  
		Size: 49.3 MB (49318983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0d42af9a92d82ccbe90040ec3d71455dfd1d92426d7f302766baf42eb07f8b`  
		Last Modified: Thu, 23 Mar 2023 07:18:50 GMT  
		Size: 8.9 MB (8914256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb28b2a98fb7b8844969dec5b68c7cfa2df0d77f1ab1a55bbfac387493184004`  
		Last Modified: Thu, 23 Mar 2023 07:18:50 GMT  
		Size: 11.4 MB (11388593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97069ba18337ebbd2738aac40ed449af0931f84e6a095665ef234602c5b1fefd`  
		Last Modified: Thu, 23 Mar 2023 07:19:05 GMT  
		Size: 64.2 MB (64152722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e13bc19413b672c07ccfd454323aa392448d3b83829fe08cef6b8f4c7a81c1a`  
		Last Modified: Thu, 23 Mar 2023 07:19:32 GMT  
		Size: 202.3 MB (202336518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:be61cbf0ebc0ae626f32c0bdc915e750c12c6cad08b614750092f78292d422bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347380976 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9589df05cc927e1f68533a64c3b822582214454492bc25806fae74c58cfcccde`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:40:10 GMT
ADD file:b6719d98d83dc3affc1d45dd9bc533456f19b9fbedf5369cde4c632f24f6146c in / 
# Thu, 23 Mar 2023 00:40:11 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:49:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:50:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 13:50:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:51:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1dab6ed4b4dcc22cec1b58fa38e2c22941443603bb1cb3a1f4025cca4556556b`  
		Last Modified: Thu, 23 Mar 2023 00:44:54 GMT  
		Size: 50.3 MB (50314549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693b9d83c0fac98a0803452b66e1b3479deb5c3bf2327160262a3795816c2626`  
		Last Modified: Thu, 23 Mar 2023 13:55:40 GMT  
		Size: 9.3 MB (9261739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be1b6a0d96c4a9175530cdacdc798d12c89c8a0fcb3e61704e44e229b4d6db16`  
		Last Modified: Thu, 23 Mar 2023 13:55:42 GMT  
		Size: 11.8 MB (11825786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bafec5f6a00fab51a420f21430812475289c684fb2d9caa7f7351e8c3a73eb3a`  
		Last Modified: Thu, 23 Mar 2023 13:56:04 GMT  
		Size: 66.1 MB (66125227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b994652f306cc47edfbded978b15b69760d07391e3d4d7bfbc806e28e5a55de`  
		Last Modified: Thu, 23 Mar 2023 13:56:49 GMT  
		Size: 209.9 MB (209853675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:3862aaeea79e1c28e659f99f4d362b54d636ab87938c521b7e6c32cd660f4359
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321528438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01d166a77be6f0012f9af9d61d3c7ad01ee0b80e1584627a75c08c07fee6b7e9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 05:18:32 GMT
ADD file:2d913f7b6c2e804834958b3d144bd7b5150a438e2aaa73cdf2f1be1c64d10100 in / 
# Thu, 23 Mar 2023 05:18:38 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:22:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:23:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 07:24:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:30:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:83c1a140184ad386a37a5446dba474a2a8498dff7ae8d2ccd2957aaf8dc1682e`  
		Last Modified: Thu, 23 Mar 2023 05:26:35 GMT  
		Size: 49.3 MB (49291603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaeb19ea7953e3c0a2cce0d76910d46a1fc5e289c90379ecb81b3e5ba2a0c16`  
		Last Modified: Thu, 23 Mar 2023 07:37:04 GMT  
		Size: 8.4 MB (8439874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecc4eca24f781c1e786d1fc88cb24202f1248f85adc06cf1b375f5607ec2d93`  
		Last Modified: Thu, 23 Mar 2023 07:37:04 GMT  
		Size: 11.2 MB (11170914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3768b306fba92d6a836552b3ee3a1bb755cd0f7d6618ca028d0643fde06553`  
		Last Modified: Thu, 23 Mar 2023 07:37:53 GMT  
		Size: 63.1 MB (63099163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cde7245b1c56e104d5370eab7caa185d690ab7a9d05dd04502c112995eedf9c`  
		Last Modified: Thu, 23 Mar 2023 07:39:55 GMT  
		Size: 189.5 MB (189526884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1cd92695e70eee806ffc668ffc3613c1ae37e09e9905ff84a9ad42e7353a4a07
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358843576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dff6cf39c1a7a6027c3f5251567633ab1cfbf3af110fb104f2f31ece459b538e`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:20:05 GMT
ADD file:3534cf3f10dae5b70c64865fd70cf5b9aa6ace6be9caa2d69518d6d59c4943fa in / 
# Thu, 23 Mar 2023 01:20:08 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 13:18:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:19:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 13:19:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 13:21:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8de2c12bac6cdfac096a845424e637222b157d221d8080dfc0e3cd14581716d5`  
		Last Modified: Thu, 23 Mar 2023 01:24:47 GMT  
		Size: 53.3 MB (53290173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ffcd14b130bc950e2e794bcf2e09ddffa8e18668803aa384fc8de743e9d8d2`  
		Last Modified: Thu, 23 Mar 2023 13:26:33 GMT  
		Size: 9.7 MB (9661589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecca2a654e1b66be833e49110ac475ae4995f36d83ba12ad0396e8f4cf953872`  
		Last Modified: Thu, 23 Mar 2023 13:26:33 GMT  
		Size: 12.2 MB (12185219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5053cb00528479013fa5db3eb35bb36ff11628a7f8c9c6ae0310021f09a7005`  
		Last Modified: Thu, 23 Mar 2023 13:26:59 GMT  
		Size: 69.7 MB (69740333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb6e33785c280f1561e4dcdae27bfcb7e802b5b52d2ebf732730e9c11c4c717`  
		Last Modified: Thu, 23 Mar 2023 13:27:58 GMT  
		Size: 214.0 MB (213966262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:1cad6f0e1cac8cfc4282f6769f2f43aa3f41c390dc8bcdb583305d9fd977c252
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.6 MB (356577785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8d3d7093b4225d61e4ec3a12847d552084ef5b41733bb97d0ddaa0c20a377f9`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 01:09:07 GMT
ADD file:0ead2f17f27ee13f553b88d07f59f56840fc40a7d668942a261c1a8714543b00 in / 
# Thu, 23 Mar 2023 01:09:09 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 01:31:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 01:32:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 01:35:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 01:43:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:94da1857a4ca1e8976329ef725087fbbe73af98bd925fbca65400b32537f3178`  
		Last Modified: Thu, 23 Mar 2023 01:12:27 GMT  
		Size: 45.5 MB (45471889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c96232283bbd760cb6134bc51d0a8713ce646f72c2f26103aecffb6f0744dc`  
		Last Modified: Thu, 23 Mar 2023 01:44:11 GMT  
		Size: 8.1 MB (8115301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e58559086b64d3108c9d17e9f17b13d71448a05197854524491ba5f1c5889ab5`  
		Last Modified: Thu, 23 Mar 2023 01:44:11 GMT  
		Size: 10.8 MB (10788034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5854e28797388adf451df519f9fc31237b24ea2ad1aa16b56d8cc738795ffc24`  
		Last Modified: Thu, 23 Mar 2023 01:45:30 GMT  
		Size: 59.7 MB (59733797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ef088b09b73a9f845196e354c219b3a0873ed0b06d799ba98428f8997d86ae`  
		Last Modified: Thu, 23 Mar 2023 01:50:54 GMT  
		Size: 232.5 MB (232468764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:ef6937355520911e322bf37cf4eacdbe10ccf42e6a938e3885be4925fe90e73a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.9 MB (313890251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9464dfffeacf05f845eee8d0edbb95a413003c5b4950df4176cec848d7e0b4d`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 23 Mar 2023 00:44:17 GMT
ADD file:f722c963bb9fb9eed0d7ba7fa5de1fdaf0fac91107cd71702d55f0cc074cd6ee in / 
# Thu, 23 Mar 2023 00:44:20 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 07:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:17:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 23 Mar 2023 07:17:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 07:18:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:866ca1f7e7197a336b8f05cbbb9eb6e6a32a17ade3068f3bd62dd93f926293d6`  
		Last Modified: Thu, 23 Mar 2023 00:47:32 GMT  
		Size: 47.6 MB (47648043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a6b4cd67d490a2c70edebe1070c48db7a7451d2f3907f036960fa85459f9f4`  
		Last Modified: Thu, 23 Mar 2023 07:22:03 GMT  
		Size: 8.7 MB (8713413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76ea7fdd8644a777c3ecd69ea57c24497971eabba7d4f9f5d7a151239348da4c`  
		Last Modified: Thu, 23 Mar 2023 07:22:03 GMT  
		Size: 11.3 MB (11285989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae83324033fd40f1d83bc12ac4be12dea69bc5afe1fb1e3fb18bcf2e5108bff`  
		Last Modified: Thu, 23 Mar 2023 07:22:16 GMT  
		Size: 63.3 MB (63255018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6c95a3a10333b031518bdfb4b42e8822a28a4b5275df3241264cad07e2db62`  
		Last Modified: Thu, 23 Mar 2023 07:22:47 GMT  
		Size: 183.0 MB (182987788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
