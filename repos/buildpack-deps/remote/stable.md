## `buildpack-deps:stable`

```console
$ docker pull buildpack-deps@sha256:70ee864e343c63f87cf415c241bf6df93405fea0b0941d51518deb4c393e2ad1
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

### `buildpack-deps:stable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:53c55d6ae5633e090c738317558db84afe5e71f1939d0cce407d5a6ebd3a4fec
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.2 MB (312249282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b17fe82fbbe09bbc0907e370da10ccfdd78adeda152232d3f2a11879a0d2d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:03:16 GMT
ADD file:89dfd7d3ed77fd5e05f20a0ab631142207ae462f5bbd877f8745d3930c751d87 in / 
# Wed, 22 Jul 2020 02:03:16 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:00:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:00:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:01:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:02:23 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:31dd5ebca5efc5e96a425402fa85e492b02c8fe757dfd3edfdea2a7c67322909`  
		Last Modified: Wed, 22 Jul 2020 02:09:37 GMT  
		Size: 50.4 MB (50390325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed641c4ae9821ca3c399071ea82ae667237acbcaad1e367c3e1e87fc967834c`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 7.8 MB (7811702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd57146431eae70720cf24877e818256ae1a30b9c1c9e7d0ad093c945ca0af2`  
		Last Modified: Wed, 22 Jul 2020 03:16:28 GMT  
		Size: 10.0 MB (9996319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac34a4d7c330794ec24a76e7e58b50d4c8f6a2fc77ca958d83092c8962e7d6d7`  
		Last Modified: Wed, 22 Jul 2020 03:16:44 GMT  
		Size: 51.8 MB (51829832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0a7e6f20fbc38a7f19b3d07aa64262789970e984f390815f867ec783e4952d`  
		Last Modified: Wed, 22 Jul 2020 03:17:22 GMT  
		Size: 192.2 MB (192221104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:07eb390d00947811e3d97b6412858b7d60b0155cb9939967c46a1823618d7876
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.9 MB (285899441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:893038cca12883cb2b75c5dd3632b131323c2389582ebb52bf08776d750d8058`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:50:16 GMT
ADD file:0431730a3850ee2a710a03ba04d05224938cf2f5318e1f73ed74677c70d09b78 in / 
# Wed, 22 Jul 2020 00:50:20 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:31:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:32:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:33:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:36:46 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:71cf5632cfeb30dc5a7a7ccd4742a02af636cd970ef3a45bebc17d3f20b3662d`  
		Last Modified: Wed, 22 Jul 2020 00:58:30 GMT  
		Size: 48.1 MB (48107278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87dffc06540f2eca873274114a3d8d49684b38428e946f67b0b62aa848ae49c`  
		Last Modified: Wed, 22 Jul 2020 02:02:59 GMT  
		Size: 7.4 MB (7360981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad12a2dc68e08e793efc12362e49a16257506721c8074ee8361c242244763bc4`  
		Last Modified: Wed, 22 Jul 2020 02:03:00 GMT  
		Size: 9.7 MB (9686988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94df5576e4481b3422d3ba55ceb470a19b7245355de69b1ee3efb03aec34668b`  
		Last Modified: Wed, 22 Jul 2020 02:03:38 GMT  
		Size: 49.6 MB (49572370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:334d8faad6c3bf412589dea023c2eaf93157b9a20686a4154dedd09caf13a03a`  
		Last Modified: Wed, 22 Jul 2020 02:04:50 GMT  
		Size: 171.2 MB (171171824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:183d002e7e0e9b4ddfc97dbd07e860633fb82642832b60b804ff9aff1cf851f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.1 MB (278099110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9ebbbdc3308412ddcd9ea40997c7d4f5880ba6a66752765563ecb8344e958c7`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:18:19 GMT
ADD file:38965defa0df84392a8ff562c2fa6393fe8d42f65f85591c07a581d694eebc30 in / 
# Wed, 22 Jul 2020 01:18:24 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:27:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:27:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 05:29:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:31:51 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f890282b0ef00faf11d62374bcdfc54ca574d085127c66977d9a08ab80978a98`  
		Last Modified: Wed, 22 Jul 2020 01:40:13 GMT  
		Size: 45.9 MB (45868714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fda9a2c24b0e12476aa415979e2be070c1cb51f060e0af97ed46ee44de7a3be`  
		Last Modified: Wed, 22 Jul 2020 06:01:56 GMT  
		Size: 7.1 MB (7097816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792d650db03400aa008d695ec7474d63c2c2d0463789209a45254c5499c8e301`  
		Last Modified: Wed, 22 Jul 2020 06:01:54 GMT  
		Size: 9.3 MB (9343320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ae3a6960f6b0b04b913ea19c225553266ea5f28803bcc808df81983619d838`  
		Last Modified: Wed, 22 Jul 2020 06:02:25 GMT  
		Size: 47.4 MB (47355216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:931a7d84774277fb839e28a16e54fcbf96d6ac52abf929953fa96191d34d2feb`  
		Last Modified: Wed, 22 Jul 2020 06:03:25 GMT  
		Size: 168.4 MB (168434044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:d6e3deda50a3f86bbdf7336348378fb4ab7a6e27c26e38f51c90ef5a974beb82
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.7 MB (302746397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e8958dc531db292c40a454b996739e514cf55f8a1d4f1084e9e48a4405b125a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:40:37 GMT
ADD file:14b8dca0bc0e6dae2f0bdb018a3a4e6d8d041abd03d118ae27cf7a72668f4970 in / 
# Wed, 22 Jul 2020 00:40:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:16:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:17:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:17:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:20:30 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e2b2cb832ad58353bcc4edbdd16023beb64ec7856b469d202975f8de836c6906`  
		Last Modified: Wed, 22 Jul 2020 00:47:20 GMT  
		Size: 49.2 MB (49168473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d6493ea016bd1aa68fa88d01d53cd305f67bae5fa500592c76c466808bf221`  
		Last Modified: Wed, 22 Jul 2020 01:35:25 GMT  
		Size: 7.7 MB (7681419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33779eed82f6ae65801a87fd1278e902bbab0f609f0c6a0232d8ef0b37112127`  
		Last Modified: Wed, 22 Jul 2020 01:35:25 GMT  
		Size: 10.0 MB (9983891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59beb1d7f774f0b2aa38b8043218a6d924bda1eef4f4692efeae226cded00a94`  
		Last Modified: Wed, 22 Jul 2020 01:35:52 GMT  
		Size: 52.2 MB (52156162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7211efa60e4409a04ec82c35f2f1536347fd0e0a85e23e3d952c51f329da5ec6`  
		Last Modified: Wed, 22 Jul 2020 01:36:48 GMT  
		Size: 183.8 MB (183756452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:394569056241ef5479837c7ffb7d66c85e655983f7ae25f64f4fa65f37a4789b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321669684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d005fd9650709a57c2fd272047d10efc283975c884f91d4487b76b3986b55db`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:08:55 GMT
ADD file:2f4b8d9ab41b6e158f5926883b6bffdab1757086d903f3f0244f75bafc2e4876 in / 
# Wed, 22 Jul 2020 02:08:56 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:20:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:20:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:20:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:21:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:88151d2519867746e4945a0a06b45430b9ddc2ae4be7e7f927cc00e3f640290d`  
		Last Modified: Wed, 22 Jul 2020 02:15:24 GMT  
		Size: 51.2 MB (51157197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63faf17c1329ba4be1004b79b9d5981fdb34d19dafc018cddec9e666c9c34b01`  
		Last Modified: Wed, 22 Jul 2020 03:40:04 GMT  
		Size: 8.0 MB (7981104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01afb186eafcffc2d1ca254ef5ee318f8bcb96ad9f552c6d73ecb3d5330e09fb`  
		Last Modified: Wed, 22 Jul 2020 03:40:04 GMT  
		Size: 10.3 MB (10338463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33759e7774776f76867212a642bee66d5f4b1b73ce09b1af6b9504cbc769ee61`  
		Last Modified: Wed, 22 Jul 2020 03:40:35 GMT  
		Size: 53.4 MB (53429429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021b645cbc6ec8759a3790b819961389d37eda083f5bd71c637d4e6f9de61104`  
		Last Modified: Wed, 22 Jul 2020 03:41:43 GMT  
		Size: 198.8 MB (198763491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1b71c9b856c029a42745a890c92c311660724511cfc729692eb32ee4a7ff85c7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **296.9 MB (296854744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da85f5f3becd2382d5fa3e4adccbac59f955c3d95cc4f4adf73b35e18b6a2b6`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:09:26 GMT
ADD file:977c467052f70f2e12137d029c9b03878551b1d47fabd10269bb0eefa21dfcf8 in / 
# Wed, 22 Jul 2020 01:09:27 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 10:34:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:34:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 10:35:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:38:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7c04e94f82f3062ec5b60ae7bab01bf211a4a344fd83f7a014cfce0dea431fe8`  
		Last Modified: Wed, 22 Jul 2020 01:16:02 GMT  
		Size: 49.0 MB (49019482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052a483e51a26250616636fb64798fc3d2dae1d604bc2d2600938715ebcae62d`  
		Last Modified: Wed, 22 Jul 2020 10:47:02 GMT  
		Size: 7.2 MB (7231450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b65fc0bfc54a9bae7903f08c85b8a726be9b67a28d1b595ebda596154742797`  
		Last Modified: Wed, 22 Jul 2020 10:47:03 GMT  
		Size: 10.0 MB (10015795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a021a129008c5cd9aca6c98d0298edbbf4a92493ac5235e8db1796637485a18`  
		Last Modified: Wed, 22 Jul 2020 10:47:57 GMT  
		Size: 50.8 MB (50838886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e52f7c51b6f907bdf1a964c56d1daddf494800e6ec1fb5b554970dddbdc48f`  
		Last Modified: Wed, 22 Jul 2020 10:50:17 GMT  
		Size: 179.7 MB (179749131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:2723d8c73b9254556f09626f8a0f6de53a1e1e60d55a0f063fae4fc2320d615f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.6 MB (333621050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87daddba8adbea130d28eb4d413a053098cdbbf51864a3c6543c08a72515f1fa`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:15:14 GMT
ADD file:3e8bf6319c2535d9da6756a6f316eac0a488312c1297fdd54c9e064959e50da8 in / 
# Wed, 22 Jul 2020 02:15:27 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:16:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:16:46 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 05:19:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:34:48 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1c8685784756ef2cf52bfd7aa4cf826bd407c500b8402bd2b5b799a2e734e133`  
		Last Modified: Wed, 22 Jul 2020 02:24:38 GMT  
		Size: 54.1 MB (54143905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30caebadb02bf7491859d6fa88f91de1d93497d4cdb5f70e4143bad62b8b0fa`  
		Last Modified: Wed, 22 Jul 2020 05:56:52 GMT  
		Size: 8.3 MB (8254952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db29f67586358d5c325f4d311f8faa65e7151c18a12be33189e36384c7ce941`  
		Last Modified: Wed, 22 Jul 2020 05:56:52 GMT  
		Size: 10.7 MB (10727204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4207fc4c9343fb556aa40918bacc75880fb56765efc58b5a010c51a6a0aa78`  
		Last Modified: Wed, 22 Jul 2020 05:57:23 GMT  
		Size: 57.5 MB (57459984 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4672b8daff187f0e69c4778cfc485d12ff54707318d30169f001223e43d03df2`  
		Last Modified: Wed, 22 Jul 2020 05:58:12 GMT  
		Size: 203.0 MB (203035005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:stable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:0a52760945a4eb99236ecd6cdb8f39f6d5ed929dcd803922e89f32ac87e42a35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.4 MB (294413982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04812e58cd2fdd03216b8e7bbf8bb002b66159fb35d1e1d33cb1c9f5eb164817`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:02 GMT
ADD file:07519836baf21317676c799c0905c76bf767fe8caa1fa718c0dfe0a152577ee8 in / 
# Tue, 04 Aug 2020 01:17:04 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 02:22:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:22:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 02:22:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:23:58 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f2b199a6d9adcfa5f879ec8042306ab2f919623f8018d0d7a6f4e9dade5e1a71`  
		Last Modified: Tue, 04 Aug 2020 01:19:47 GMT  
		Size: 49.0 MB (48966275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5615f13ce6c82698ac5df02b39113e3a8949db1a7a7f7f5d07c9265ee15b79d0`  
		Last Modified: Tue, 04 Aug 2020 02:28:11 GMT  
		Size: 7.4 MB (7385167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ffecb808bd421be3db88ff08f67b19f28c1ffe0d4c157be3fcff3360f527bc`  
		Last Modified: Tue, 04 Aug 2020 02:28:11 GMT  
		Size: 9.9 MB (9882139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e2ce491a55134d5e4118405670fcc19b140898dc8ac62156e47a49f52e9f2d`  
		Last Modified: Tue, 04 Aug 2020 02:28:29 GMT  
		Size: 51.4 MB (51379924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52f0e863b61c88c558f6301fa0a803efd4f01fcf47081fd26f2dfd7a09b41ee7`  
		Last Modified: Tue, 04 Aug 2020 02:28:56 GMT  
		Size: 176.8 MB (176800477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
