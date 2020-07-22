## `buildpack-deps:oldstable`

```console
$ docker pull buildpack-deps@sha256:fddd0881546405f75428a50ad1e95c359dd8a08cbc1fb8314c1d9f4f37fa0c89
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

### `buildpack-deps:oldstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:816fe62fe22331a241d60ca6e30df1e1ac247905cbc53ed217c771eb26c32c1b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325490958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d486287f16054cf35b163a84bd249b1afe9f9480723b3961c0c5c06958c6ed`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:06:48 GMT
ADD file:f98fe3d719ea765cb59da025d506d0bbd6db7a842b6b63c58c8d4d65b51bdb1f in / 
# Wed, 22 Jul 2020 02:06:48 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:11:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:12:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:13:26 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7e6d8ed603557d9bf077a9ace4ee506501970a4938b9a704f040ad15f22bd4e8`  
		Last Modified: Wed, 22 Jul 2020 02:12:13 GMT  
		Size: 45.4 MB (45369674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43421f771d04c7019cae6594c2b95ad92d692750fc57d201b5108c1bef2d095e`  
		Last Modified: Wed, 22 Jul 2020 03:19:27 GMT  
		Size: 10.8 MB (10750266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c36327c39ae4245e3dcfa5b77a55cff18b6d81f2b4ca1b0e107da95ecd6b225f`  
		Last Modified: Wed, 22 Jul 2020 03:19:26 GMT  
		Size: 4.3 MB (4339838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b0be3e8a6128bdb3b29195c2e0dba2ba95ef6bb3dbeb796b29f84df426f417`  
		Last Modified: Wed, 22 Jul 2020 03:19:44 GMT  
		Size: 50.1 MB (50082369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b168feb1bb04518793ccd98ad075fc6a0f6f610dcb7fa379f12410b6ab4e2e8`  
		Last Modified: Wed, 22 Jul 2020 03:20:30 GMT  
		Size: 214.9 MB (214948811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:49d5f05c3814e85dbc492be386d49b44d05f953cc1777703577ec86b2c2125a9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.5 MB (309477340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76782997dfc14eafc55fb6231aa234e4a3619bc116772f77a2dc2fa7e4d9585f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:54:50 GMT
ADD file:20254f5b25d60e6c982d1c79c039231162bbcd4f257bb6abffd80fcc90989150 in / 
# Wed, 22 Jul 2020 00:54:52 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:54:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:54:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:56:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 02:00:16 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:fd4c1ca2ea2c633172981c07bc3fa277bf52eb9dbb1010857e651754055dd468`  
		Last Modified: Wed, 22 Jul 2020 01:03:05 GMT  
		Size: 44.1 MB (44078283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde86d8f1cee1b2d3b4c76e0358f514d68286ce9a4772a5d16ad51a80213d213`  
		Last Modified: Wed, 22 Jul 2020 02:08:05 GMT  
		Size: 9.8 MB (9824381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a7a43ea3fbd0d9462b4838c62dcd94742d99a8782aed47312babbdfffabbc01`  
		Last Modified: Wed, 22 Jul 2020 02:08:05 GMT  
		Size: 4.2 MB (4158943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a96bddc4a6a2b813426656d27bed8b04a349ea8f1d8723718ea1b995e4cfdcba`  
		Last Modified: Wed, 22 Jul 2020 02:08:29 GMT  
		Size: 48.3 MB (48294302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00052b39633508c001f49bfbf98702c979483a015c2f5546f2e3fd01bbc66213`  
		Last Modified: Wed, 22 Jul 2020 02:09:30 GMT  
		Size: 203.1 MB (203121431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d5ef307a436e6db3dc20e4ea0db16b44ff5223fc38db34246f5cc5b662fd6136
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.5 MB (297484963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83f5999ebc9c391130476d07e012587322ef1a85db38272f90fb6afdec2609f0`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:32:02 GMT
ADD file:762e52a5e1d8ff2daa22c3bec2cfdfe4cbcf224deb1e73d7db3af0cbf5658785 in / 
# Wed, 22 Jul 2020 01:32:11 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:50:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:50:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 05:52:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:55:13 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:05dc12a0df610a09562914533797508b791bbd115ae17b6a1b75666ec90263da`  
		Last Modified: Wed, 22 Jul 2020 01:44:04 GMT  
		Size: 42.1 MB (42107480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b998b2d4ee2005b0f51e94b6fc7467091e54a910491e7873b9e0d6f59aabd98`  
		Last Modified: Wed, 22 Jul 2020 06:06:37 GMT  
		Size: 9.4 MB (9444083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15230f55c10a543d54564a792784b1d2e133d4edeadd58978682d9bf02d1425a`  
		Last Modified: Wed, 22 Jul 2020 06:06:34 GMT  
		Size: 3.9 MB (3918506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3910902ef268e18c5fe039b40cb36bf07e9728fc8e7aab969d5d236390d59e`  
		Last Modified: Wed, 22 Jul 2020 06:07:01 GMT  
		Size: 46.4 MB (46415355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6de4566253dac35da4372325587004bce8799ecd75b69affbcaaaa2445ce715c`  
		Last Modified: Wed, 22 Jul 2020 06:08:00 GMT  
		Size: 195.6 MB (195599539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:78185af8e76fc846d9e673d7a25090fce41be55c8cad30b6c1a20b28f6d9a3a5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.3 MB (307317950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfe650bfb21ec32f787854b8932468a2a4d9ff9dc4759a063afc60494c1214f2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:43:42 GMT
ADD file:9c5c9df9952cb51291333837bdb462bbdf9f157e91e616f1e3fb8d2fcb1a1983 in / 
# Wed, 22 Jul 2020 00:43:45 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:26:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:27:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:28:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:31:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ad4de4f68e9c2c0f5e5e62d379d936bb88ce467505ed002fb1e10c434fefe90c`  
		Last Modified: Wed, 22 Jul 2020 00:49:52 GMT  
		Size: 43.2 MB (43169407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05aedd313900c1f55a004cb5b8a8b93ee320b25c73286390f0669f387fd96c47`  
		Last Modified: Wed, 22 Jul 2020 01:38:43 GMT  
		Size: 9.7 MB (9700532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a2bc27f6e0cc82b950064aa77aa261962e402cb805c2c36bef0ece1371fa405`  
		Last Modified: Wed, 22 Jul 2020 01:38:43 GMT  
		Size: 4.1 MB (4094121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b45ec4f3e5ad5ce96ca9f1854568a75c1896d465e78ec5c2850220d1a85220`  
		Last Modified: Wed, 22 Jul 2020 01:39:07 GMT  
		Size: 48.0 MB (48034890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2338948e6aa2ca6194d6a03949a78485c19b28a44a68773921ddc7aca6bff6`  
		Last Modified: Wed, 22 Jul 2020 01:40:02 GMT  
		Size: 202.3 MB (202319000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:d836b617ebcdc886bcdeff145c2e712edc68f679cf9f2e43d658e2cdefad6e97
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.0 MB (333046509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425340540d43af8366c2216f677c6d8bdcc1c6693a9570d1c3efd561f6c1ee40`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:12:18 GMT
ADD file:d3f4f838251f30bbb4c033600c18e4c1065e310959dc105d22c6df709decb369 in / 
# Wed, 22 Jul 2020 02:12:19 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:34:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:34:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:35:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:36:41 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48006630f132977bf4db68efe0ddd39191244134bb38b95a1c28b7cc6ce01157`  
		Last Modified: Wed, 22 Jul 2020 02:19:12 GMT  
		Size: 46.1 MB (46092998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b55841d4427f3f7db211f0ce8bd00aec32e728961c97fd5c1bfd5c3f9ed73630`  
		Last Modified: Wed, 22 Jul 2020 03:45:32 GMT  
		Size: 10.8 MB (10774080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3f8c22b21a978b42daa813da3020469db274995a267599d278e2c6a196eb6d`  
		Last Modified: Wed, 22 Jul 2020 03:45:29 GMT  
		Size: 4.6 MB (4561195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79d8d12c056736dd08742a1865d13bc07d864c5eeb6084b16217b8bc2d835e5`  
		Last Modified: Wed, 22 Jul 2020 03:46:03 GMT  
		Size: 51.6 MB (51617221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4373c527db532e2636bd2aa069e423762228a948fed93ca2b0e91a3a411c70e`  
		Last Modified: Wed, 22 Jul 2020 03:47:11 GMT  
		Size: 220.0 MB (220001015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:1bf9f7a144ab9691ef3acb16a8bb8e112ee987d80ea523f3939c694d3a7c93ce
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318815865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739719a006ad9234b87db3b81f124a183a429852a674f9b4d29c69a44fe006f4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:12:47 GMT
ADD file:de9470ab1a8469c3a824a48056d16d354ec41a887b8b0e6f7b13cedc73a3f316 in / 
# Tue, 09 Jun 2020 01:12:48 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:00:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:01:02 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:02:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:06:10 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5fdce7db54786a0dce8a238fc9218fa25a9ccc5d0ac32920fd67f03f5571b347`  
		Last Modified: Tue, 09 Jun 2020 01:22:55 GMT  
		Size: 45.0 MB (45049756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffa9955e6182b5a1d2e59bd120f03d4bbf4c0e4c86773a33e7f98fea4f73a0d`  
		Last Modified: Tue, 09 Jun 2020 02:18:06 GMT  
		Size: 9.8 MB (9789501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2d1a085f35901bc4dc96d415aa9abf95233373a94aa4e89e20c50cd9fc6cb1`  
		Last Modified: Tue, 09 Jun 2020 02:18:02 GMT  
		Size: 4.4 MB (4394502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:968e741ea7d876279f8195bfcd9ef6e5eab8463b6e69fb92b9cb61225e843228`  
		Last Modified: Tue, 09 Jun 2020 02:18:56 GMT  
		Size: 49.5 MB (49475249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240b35a809489927e64f8c8276fd287dc6051053e7d4539a963f0c156904aba4`  
		Last Modified: Tue, 09 Jun 2020 02:21:40 GMT  
		Size: 210.1 MB (210106857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:40d936b00c0d238b14182477019d99b0a02e38f19fd4c4916465a525f2626e67
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.5 MB (320508370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a4633343e1f33f913faf39cc24ff7ab343ba5b201899c1c5dd3527c7c22f506`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:25:13 GMT
ADD file:878d3c5ae80057152412c4f5b685480e31771287ece3cf1d19fe21a16d80fb8b in / 
# Tue, 09 Jun 2020 01:25:18 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 03:29:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:30:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 03:31:43 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 03:39:03 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:68fc3b7ea52ef2eff565ff8598b519926d3888698d89f1144612b1a795fad33e`  
		Last Modified: Tue, 09 Jun 2020 01:36:44 GMT  
		Size: 45.6 MB (45644478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f566612be54210d3f13769bf477296dc458787a15c254838e477d0a263e4f5`  
		Last Modified: Tue, 09 Jun 2020 03:49:43 GMT  
		Size: 10.0 MB (9955962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6980ff97a81d5f3cd6e8db208e1a1f7784457373b97ed4a1480c7d4d1a861eb9`  
		Last Modified: Tue, 09 Jun 2020 03:49:35 GMT  
		Size: 4.3 MB (4296286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67146a7d847b7abdf00468db4fc2e38c9ca5b80c342c4fc189e319d0492cc6db`  
		Last Modified: Tue, 09 Jun 2020 03:50:30 GMT  
		Size: 50.1 MB (50081488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6f1610494e3291171ab6fe2b900bbbec5f187c7c6c22e44ead787c176acfac`  
		Last Modified: Tue, 09 Jun 2020 03:52:02 GMT  
		Size: 210.5 MB (210530156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:oldstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:166050211e2b14232f44b9326c18da1631efd9baafe405e6a1df2c8c36a7ceaf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317324665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a423fbc94a1ada04d0de1e579b1a6ffa709de2bbf411445d2a7dd1265cd159e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 09 Jun 2020 01:44:05 GMT
ADD file:ce4b8c76522cbe8599502985424901aee9d30d37296761d47dbcb9b0770f7aa2 in / 
# Tue, 09 Jun 2020 01:44:08 GMT
CMD ["bash"]
# Tue, 09 Jun 2020 02:13:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:13:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 09 Jun 2020 02:13:54 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 09 Jun 2020 02:15:38 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cc8faf537ff83acc994f80bcea99d8e073aa05b5eb0dab5ce495510af0b6d1f6`  
		Last Modified: Tue, 09 Jun 2020 01:47:50 GMT  
		Size: 45.2 MB (45232505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9816eeae17f469b3b58481bdbae04cc1b7b69f8d8a6ef15f6972d91ba2f29ee8`  
		Last Modified: Tue, 09 Jun 2020 02:19:43 GMT  
		Size: 10.3 MB (10280522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a7344ca59dab92a8238f2df0ea3779840ec21afc295e24f39259558c3bfc05`  
		Last Modified: Tue, 09 Jun 2020 02:19:48 GMT  
		Size: 4.4 MB (4372414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a9332093631759dcfd58267f270de204b0c9388802581c972141e78700c0bb`  
		Last Modified: Tue, 09 Jun 2020 02:20:00 GMT  
		Size: 50.5 MB (50510977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6abb293160bb369db1a3815bce0f615b6d0d75a3a6f4152e6d68933bfa3653ee`  
		Last Modified: Tue, 09 Jun 2020 02:20:29 GMT  
		Size: 206.9 MB (206928247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
