## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:69e7ea22a716ce8780425cdd695694845f3252a7122273968b48858f6304571d
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:88e881c4139542d0a34138a7b629292802af1f15a534467984e738e465b0b143
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **480.8 MB (480785408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9622f52f8d906cf82aa642547e80b461ab7e69cd5b0dcf93e36099d904c274`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:07:48 GMT
ADD file:51a85ad79ebd7e288cd0ea14cd2ae41990aab2d77352f801f09c3a4682cb83a9 in / 
# Fri, 11 Dec 2020 02:07:48 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 16:59:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 16:59:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 17:00:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 19:54:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ff8cddfd21234a3c42ee0af471b251a807aa29af4ca00392976a17d3257ed269`  
		Last Modified: Fri, 11 Dec 2020 02:14:23 GMT  
		Size: 53.4 MB (53352668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58120f59d80232cb93b7fff568312888d13cf4167158305ffe8adc4483af30e5`  
		Last Modified: Thu, 17 Dec 2020 17:27:16 GMT  
		Size: 7.9 MB (7909957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37776afef7b17d4680060a625bb43a68146d6e6d5ab006be07856897c2aed6dd`  
		Last Modified: Thu, 17 Dec 2020 17:27:16 GMT  
		Size: 10.6 MB (10648135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43542ad23e1682377f889e0fd8dd5dd662b4d9f1b8e85bf63145a64dcaed34a1`  
		Last Modified: Thu, 17 Dec 2020 17:27:37 GMT  
		Size: 56.2 MB (56206121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f736bbaaa1cd33da01e6d007510801e383def04412b4a322fc73ff48cc1d02`  
		Last Modified: Thu, 17 Dec 2020 19:58:27 GMT  
		Size: 352.7 MB (352668527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:48759e3b439680032c8eff6559e531600ad98f51a36ee2d78687860fcc6232e6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.7 MB (303665816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a224ba857929852f5721f0716304f4267899e20c85875c9b5ea15304405a1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:53:57 GMT
ADD file:7c196731dd997fe0c289ed02eba35ecfe200559ab33bcd6e863f39d8dd0ea362 in / 
# Tue, 12 Jan 2021 00:53:59 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:32:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:33:01 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:33:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:35:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8703e0802b99292f132d58e67ad879ab0ffa44370ae81a8ca7a93ee05c332d4d`  
		Last Modified: Tue, 12 Jan 2021 01:03:20 GMT  
		Size: 54.4 MB (54362040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2920a5dce5819aaefba9b42acf5eecc9bf6a9cece8f1115be0561cd7604d55`  
		Last Modified: Tue, 12 Jan 2021 01:45:30 GMT  
		Size: 5.1 MB (5061367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ad854c9d78348debd410e2b83d72c46ebbefeabc275c2a9fa7877161420d56`  
		Last Modified: Tue, 12 Jan 2021 01:45:32 GMT  
		Size: 10.3 MB (10336421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea051d0fa4b3585dc14e2b6b16e7bd6bab45c2363fd73fdb6f52016e7976558`  
		Last Modified: Tue, 12 Jan 2021 01:45:58 GMT  
		Size: 51.8 MB (51760561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52880a6fa5a3eafaa047afd4d619007f9c3c5801c9f0b8281830b8a031a42ac6`  
		Last Modified: Tue, 12 Jan 2021 01:47:04 GMT  
		Size: 182.1 MB (182145427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c1a5d1df20246e7d3d7b2f1e39a8fbb35b3e628fb1cc9f4cc024fd728926bd6b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.9 MB (290930553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aabd8a869fb2cfbef7b7f444c27355aecc88c101048648229136fc3d6b5a1fb4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:03:45 GMT
ADD file:a459be4601ccf608a415f6ce53ea885edd1a9a10ba1205f3e8493e277e6a7faf in / 
# Tue, 12 Jan 2021 00:03:51 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:17:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:18:12 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:18:48 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:20:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2fdfe7e087b5c823888d02320fcca90d4debb7a7d0ead6a978abb2de6acbbc00`  
		Last Modified: Tue, 12 Jan 2021 00:13:47 GMT  
		Size: 51.9 MB (51902171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0592e7529a748d8d0e52ef640addc32dcea717609f5c656e4399e87bdd4d9db`  
		Last Modified: Tue, 12 Jan 2021 01:31:29 GMT  
		Size: 4.9 MB (4921500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeb968aa1e6a404fcd0a89cbc65878f592c4c4067725853712ca4d00c1669ce`  
		Last Modified: Tue, 12 Jan 2021 01:31:31 GMT  
		Size: 10.0 MB (9976214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdb7dfd157d86a4ab3edd03ec9cf4d063137a8f583451d79dea1963f4ac7213`  
		Last Modified: Tue, 12 Jan 2021 01:31:56 GMT  
		Size: 49.8 MB (49773988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8404f1d47230fefca10223d740c1a5fa2e76c045332a3c60239565f12c1ae8`  
		Last Modified: Tue, 12 Jan 2021 01:33:48 GMT  
		Size: 174.4 MB (174356680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b5fab0439bef44567b7b4bc4ba18c58fbd5d200ead534c504fedd129f3b195c8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.3 MB (322307384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e00adcd4bdb71388ab9559a395864b64f207572a45cee957abef37c8166548e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 00:42:27 GMT
ADD file:ba9ce45e2c6743713798982615c806de6db6d8fd9a0d8734c8a69d80f3959eb6 in / 
# Tue, 12 Jan 2021 00:42:35 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:27:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:27:27 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:28:06 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:29:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:01dba80e9024f3ac734ae74a14f2997ea67918b4de57aef778ed839a508baab1`  
		Last Modified: Tue, 12 Jan 2021 00:53:15 GMT  
		Size: 55.5 MB (55537816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8417d785c975de855b94a5c17e92b69107a02149bbd61ac1b6d1355d80b32549`  
		Last Modified: Tue, 12 Jan 2021 01:40:11 GMT  
		Size: 5.1 MB (5140360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e34511ce04354db34bda0eb613bcb4990a4e262fe16307861b007423a0033c44`  
		Last Modified: Tue, 12 Jan 2021 01:40:13 GMT  
		Size: 10.7 MB (10655802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23256b8138d02e2f8552e7878b3d34195476c50b86ef0dcf9d758fb0bade2fc`  
		Last Modified: Tue, 12 Jan 2021 01:40:39 GMT  
		Size: 54.2 MB (54162075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edeb7157ff06148c1376bed60425e6b71419153c1fcc36329b193e9fe0eb5bc1`  
		Last Modified: Tue, 12 Jan 2021 01:41:36 GMT  
		Size: 196.8 MB (196811331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:15b1a3b51028ec66aee695e7f8b24caa563dd440808a07c3b231d32243ddb9c9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.0 MB (341981466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db06ab5204fa239ec889bc726025404f3d1a213c446b827dba533348d3780c2`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:43 GMT
ADD file:ac372b15438c9387718286ebd1a5b9512e674cdc90319668b3612fcb0cd99441 in / 
# Fri, 11 Dec 2020 02:04:43 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 08:10:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:10:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 08:11:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 08:12:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bbad886384348be399f916b804d2efe113827e77f3c2b05f9b19a4dd67bff32e`  
		Last Modified: Fri, 11 Dec 2020 02:11:56 GMT  
		Size: 54.4 MB (54407631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107edbf54231bab6e619380b341236d89d7c373021e0ca4ced89d4b094f74537`  
		Last Modified: Thu, 17 Dec 2020 08:27:04 GMT  
		Size: 8.1 MB (8083852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:770453472dffc640059e49933b5042237ef0d2a63e4ecbc572da6109134c440b`  
		Last Modified: Thu, 17 Dec 2020 08:27:04 GMT  
		Size: 11.0 MB (11031266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6aff5ce2d179cce5128375be4a9798643c0eece646c52f9f561fc0a83103843`  
		Last Modified: Thu, 17 Dec 2020 08:27:29 GMT  
		Size: 57.6 MB (57633904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b3410cfcd2872b64f65323d2fcedc2805ac7adf7a3ead0226e9e7aa5a54eebb`  
		Last Modified: Thu, 17 Dec 2020 08:28:56 GMT  
		Size: 210.8 MB (210824813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:22bec863142ed8e8496a1d3154ba4d703b31a6f6a0437298a09f8fe350169d80
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.6 MB (308561365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55105e9c29cc1388b1065a2707a7ed824600cf3fa1bc9895b0340360b4024699`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Jan 2021 01:16:48 GMT
ADD file:7bfb9d47fcd2b6a553e5be3b702d34f192cd8798dd3982fc6e6e77479f0affdc in / 
# Tue, 12 Jan 2021 01:16:49 GMT
CMD ["bash"]
# Tue, 12 Jan 2021 01:54:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:54:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 12 Jan 2021 01:55:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 12 Jan 2021 01:58:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24a4375dbae3deddd016bd6d4372d219ba5fe4102ce643c06dd57677bc882654`  
		Last Modified: Tue, 12 Jan 2021 01:24:08 GMT  
		Size: 55.0 MB (55046139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1447ce8a926cf7692ae55e3f2edb9925e5b11be684c7fd68fe2a385a5b812880`  
		Last Modified: Tue, 12 Jan 2021 02:05:46 GMT  
		Size: 5.1 MB (5114938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfd08658a76a7d3cedb6b4760f760c0ce830104bb77dbffd92228d4d0448730`  
		Last Modified: Tue, 12 Jan 2021 02:05:49 GMT  
		Size: 10.7 MB (10658281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:646e7a05de00a7a60c4b7f630af924f98065319eb7883ece0b8839a36675802f`  
		Last Modified: Tue, 12 Jan 2021 02:06:42 GMT  
		Size: 52.8 MB (52759060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54f2c5555956884b697e6a39cf2e689a400d851e4909aed099803a5ac13905d8`  
		Last Modified: Tue, 12 Jan 2021 02:08:55 GMT  
		Size: 185.0 MB (184982947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:fcf9cdc654fd307016395bb15f755f2ed6ca94c37425fbfa9f95063fd1887e3d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **479.4 MB (479425220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25f8b13e6d4e6cc71c73299400dd1eff92b27106d14287da20889f70b2a1dea`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 03:34:34 GMT
ADD file:d6769e024c4c1bf3ac50de798e3b70ddbae5e8dc6c4edc64cbf31ef39fba2896 in / 
# Fri, 11 Dec 2020 03:34:40 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 11:52:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:53:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 11:57:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 12:11:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:897184b44dea4f1c1b646278a369b1024dac0562097178b81b92da84665fd760`  
		Last Modified: Fri, 11 Dec 2020 03:42:05 GMT  
		Size: 57.3 MB (57314487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23bf9998295a2348e5ea5ebbb24a1bb17e57e20b1c41f8d55a26942cbf9ecd66`  
		Last Modified: Thu, 17 Dec 2020 13:42:13 GMT  
		Size: 8.4 MB (8363493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f68f738f0b4ea98f73eedce2726aaa0b017e60b3ee74625615e9fe42eb3d6b`  
		Last Modified: Thu, 17 Dec 2020 13:42:18 GMT  
		Size: 11.4 MB (11421158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a257d57292a484299d176728b9425b924212f272740dac171d871150b47e6abc`  
		Last Modified: Thu, 17 Dec 2020 13:43:37 GMT  
		Size: 60.6 MB (60633039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f91b6f404170d1dd6256e77a177d1f5614f0bbc0b4841b57b4911ba1180484c`  
		Last Modified: Thu, 17 Dec 2020 13:47:17 GMT  
		Size: 341.7 MB (341693043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3a8bd086704fd2960ced6c846db5f7ce581fc438eaab560416ef238195870a14
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **438.8 MB (438828841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502c21e7e22521de810a076aef04e1e427867219e972909b2cb35610137cf2d3`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:29 GMT
ADD file:81f25bd988cd2db6809416e7139b279a1a04ce8e2b864c71e35768d7211232db in / 
# Fri, 11 Dec 2020 02:12:36 GMT
CMD ["bash"]
# Thu, 17 Dec 2020 11:18:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:18:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 17 Dec 2020 11:19:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Dec 2020 11:22:54 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d882124dbf8a54501109f018ee08c93cb805beed092d3bf2e6979740fad5f861`  
		Last Modified: Fri, 11 Dec 2020 02:17:27 GMT  
		Size: 51.9 MB (51894888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03d19883059c6574b24a1136327bfb2a42e1709d68c54db24a7b443ea27ba6fb`  
		Last Modified: Thu, 17 Dec 2020 11:47:32 GMT  
		Size: 7.6 MB (7585305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3620af9fd07136686b0a9a787703282d968f4e2b3e04654c62094c925d7eefd`  
		Last Modified: Thu, 17 Dec 2020 11:47:31 GMT  
		Size: 10.5 MB (10525413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5636f80b0edab0a99700edbedaee1ac005f359c022f913368483c3495326e1fe`  
		Last Modified: Thu, 17 Dec 2020 11:47:49 GMT  
		Size: 55.7 MB (55690291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ddb2771012175d631173cf4331bbb5bb922666d37e4f6cf2cf25c75683ffa7d`  
		Last Modified: Thu, 17 Dec 2020 11:48:40 GMT  
		Size: 313.1 MB (313132944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
