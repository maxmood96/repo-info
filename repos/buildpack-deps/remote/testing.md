## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:44063815a06927077d4643d02836c864691429f07d69c35b72cc930e3a629549
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:4decdcb28b05d0b32a838ea93643c0dc94decbb34ba19f356c9d52dd15192a8f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.0 MB (340958155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee91c5c44d484c517172746ed616693628dd9317b66c6c4b11e94fb9fb72a337`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:20:17 GMT
ADD file:bc800ccc3502eee52ab13da7e930beeea45bff7ec8e6f625f2958550a0e0c4a0 in / 
# Tue, 06 Dec 2022 01:20:17 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 02:11:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:11:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 02:11:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 02:13:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3d5213c1b98149df5de6014f7a0822d3f7c1239b55b191918b5019861d2385bf`  
		Last Modified: Tue, 06 Dec 2022 01:24:15 GMT  
		Size: 50.3 MB (50260519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adf3c7a7c116d44387858d478529693ecefc787b2f5ab45aebdfe6884125ff8`  
		Last Modified: Tue, 06 Dec 2022 02:20:43 GMT  
		Size: 9.0 MB (9019439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a4bc2fe30909b334399b20974788d0da585394e55d471a14a5f3e60134f81d`  
		Last Modified: Tue, 06 Dec 2022 02:20:43 GMT  
		Size: 11.4 MB (11368978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4c76cf5170ac15770cc8edd5f98ed33f766d4a9d72d3200443bb50df873eb`  
		Last Modified: Tue, 06 Dec 2022 02:20:59 GMT  
		Size: 57.2 MB (57189320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e287bf877d695df88d90165b0e2ee0de3edf261155d56e87350b9ba84219bc2`  
		Last Modified: Tue, 06 Dec 2022 02:21:35 GMT  
		Size: 213.1 MB (213119899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:c3469a85411de0aad11927787bfd39a7ba6c284902903348a20210eba7d8af15
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.2 MB (309212479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a15e9443c2b34d8ddb22efb2ff19ddf32bf216d99355a0e3cb3b0800b300da`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:48:28 GMT
ADD file:1a47719ac251c6eab2626d584c016fd54fb5ad1212453da6f254e2977d844ec9 in / 
# Wed, 21 Dec 2022 01:48:29 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:16:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:16:24 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:16:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:19:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5a2ba72506fbd85b58dc5575f5616efa7992eac16768aa35e10922a41b5bc83a`  
		Last Modified: Wed, 21 Dec 2022 01:52:47 GMT  
		Size: 49.3 MB (49285345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c480e4f144d3171b1600a48c85c8893cb2e7068df99ac2a593073fc603175c6`  
		Last Modified: Wed, 21 Dec 2022 02:25:19 GMT  
		Size: 8.5 MB (8471399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bbe5572b5bd2366b9b993844292cd896c430947a32be55f045cd4a552447b46`  
		Last Modified: Wed, 21 Dec 2022 02:25:19 GMT  
		Size: 11.0 MB (11014351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d675c15b2b0af988362a3ff26bc1a95628fe1475e278f83cfe3c315ffa3df3e7`  
		Last Modified: Wed, 21 Dec 2022 02:25:41 GMT  
		Size: 54.9 MB (54929700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1280172fe4e65be2c38f4d16ee8585a3df2b7fbe2b1dd2d2d2c4edd28081f2fe`  
		Last Modified: Wed, 21 Dec 2022 02:26:23 GMT  
		Size: 185.5 MB (185511684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:dd790e4ab96cafb9c74c9191b9ec0b423a2c18900ec68a4bd52df99e7389187b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.0 MB (295039671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf29462b326dbfb45c27b4d6b360edfab18c3f9fb81ace95c294fe06a4cd2ab2`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:57:40 GMT
ADD file:3a39343b0809f063616f72499663466e4a509b48e03fab9262c152a211f015f7 in / 
# Wed, 21 Dec 2022 01:57:41 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:25:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:25:41 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:26:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:27:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5d2b0b92caaf35a430a2b891b3ae1c59a6cf60477263bd8e7a30cda427435d63`  
		Last Modified: Wed, 21 Dec 2022 02:03:55 GMT  
		Size: 47.1 MB (47101260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a36589bec34c9187227f581132ae596646abfc864ef9c4f049dcc7cb80d9e3`  
		Last Modified: Wed, 21 Dec 2022 02:36:46 GMT  
		Size: 8.1 MB (8119430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aa4da363e919b9e1ffa0593e59ab1b23caa6d60c84b20ebfea4db0863532e5c`  
		Last Modified: Wed, 21 Dec 2022 02:36:47 GMT  
		Size: 10.6 MB (10646191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca23736de3322232278a50330b166e2dc3a96e13bc603c0a868f7c6ed03aed8`  
		Last Modified: Wed, 21 Dec 2022 02:37:07 GMT  
		Size: 52.9 MB (52925737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5490550e73309c3d20201befafe5f69a532b1149118c1519a15d78e1849532e`  
		Last Modified: Wed, 21 Dec 2022 02:37:48 GMT  
		Size: 176.2 MB (176247053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:443f22d1117086034aa16e171494417a2ccde57c70928ed9b683e9cad4bc6496
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.9 MB (330854528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9626341e921dc9919810a16eb80f8a2d5483729e6f5238414b3762268dcb545`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:25 GMT
ADD file:b83d427ad5bc07aecb363a59c19809d66f1425c1d8df7a4d66eb56624cf5fcf3 in / 
# Wed, 21 Dec 2022 01:39:26 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 02:03:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:03:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 02:04:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 02:05:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:be520eae96ff7c486efeba591ba872089e3b618ce226d23bf2b72f07277fb6fc`  
		Last Modified: Wed, 21 Dec 2022 01:42:15 GMT  
		Size: 50.4 MB (50372842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fd22e8d17dba55cc72a876a3a9244c7b617edbf94a17fdaad2f9d803c02d5f`  
		Last Modified: Wed, 21 Dec 2022 02:11:45 GMT  
		Size: 8.8 MB (8849270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7950c3893d7d3fd9cc5fb052ba3abdcdc532147811125fdba6efec5d9b4efee5`  
		Last Modified: Wed, 21 Dec 2022 02:11:45 GMT  
		Size: 11.3 MB (11325894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53d0bb157e7432bcc4ced269bd85ce3c558f9fcefaac7844b601556fd5cffe72`  
		Last Modified: Wed, 21 Dec 2022 02:12:00 GMT  
		Size: 57.1 MB (57094158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b1db73f34c700043ec7eb90a1aae08d85c52d7526ec8e4bd4a3c0f7ce7a0a1`  
		Last Modified: Wed, 21 Dec 2022 02:12:30 GMT  
		Size: 203.2 MB (203212364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:91fb02366e9717f97dadcda313895f1b414a6c4fe91f68989f36ee9b120f7807
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343770539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa575e271aff10438b80f395a7e0eb478bbe62f22319325d669a4edae920457`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:38:43 GMT
ADD file:f11f9a6e73a1ba42c97eb037cc53f119df6d6b050eaeb10df2ae716f4eabd8bf in / 
# Wed, 21 Dec 2022 01:38:44 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 09:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:50:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 09:51:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 09:52:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bce8ae6c08a69b30b85b1e939b782fc4dee31791e21ed3abbf56d1ec1dde0381`  
		Last Modified: Wed, 21 Dec 2022 01:43:40 GMT  
		Size: 51.4 MB (51363529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d633e3250ed10016905229f6d67f3386ceb15eb9d1bc3deb88c518444ced27`  
		Last Modified: Wed, 21 Dec 2022 09:59:17 GMT  
		Size: 9.2 MB (9194506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e65f66728bfc6f4d6de6d54692bc94e1c8972c2fb1d47052d38b89b8d33481a2`  
		Last Modified: Wed, 21 Dec 2022 09:59:17 GMT  
		Size: 11.6 MB (11561149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:883b0fff1e223e986f26eda6c09aecaf9bf292dbb243e2d42df8aa52d520818a`  
		Last Modified: Wed, 21 Dec 2022 09:59:35 GMT  
		Size: 58.6 MB (58640479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dfbc944a3662672fc817188a98c16bd2795868ff0c1200fd91c031af024b30d`  
		Last Modified: Wed, 21 Dec 2022 10:00:10 GMT  
		Size: 213.0 MB (213010876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:689636aafbd71ce1ef6d68e4af01fbd46d08111f53fceacf493d49953c779738
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.0 MB (315974673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35cccb1886d576396c00b1c79ce169521cecc130a04d9795e46ccebd6fc35a72`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 06 Dec 2022 01:53:35 GMT
ADD file:5f771b53cd80db61f6fcf0df30ca6b99cd2c768f57ab1ffdf53d1f646b7db7c2 in / 
# Tue, 06 Dec 2022 01:53:41 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 17:06:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:06:58 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 06 Dec 2022 17:08:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 17:15:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9cc4004cb6d73c258a4d864dabb35e2beb3272eaf0de591430b0bb1af15141c`  
		Last Modified: Tue, 06 Dec 2022 02:01:46 GMT  
		Size: 50.3 MB (50259491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0bb8986f763b3dee4c5b32d9c82a018159c1bc6452e370fe08635660e89d7fe`  
		Last Modified: Tue, 06 Dec 2022 17:32:55 GMT  
		Size: 8.4 MB (8384079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a60f3afb7af77661e81375d03b106172646d324a7f36dcc156ffe006dd22158`  
		Last Modified: Tue, 06 Dec 2022 17:32:55 GMT  
		Size: 11.1 MB (11118473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc29876f092a179802df5708c39f6d2379d6f42f3ee77ce5ecf099fc21378b58`  
		Last Modified: Tue, 06 Dec 2022 17:33:46 GMT  
		Size: 56.1 MB (56055838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f8c6676910feaee2d13e3b6cc29272f9fe416066d86478c00ce5600eb29b5f`  
		Last Modified: Tue, 06 Dec 2022 17:36:00 GMT  
		Size: 190.2 MB (190156792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:5d2efa53d257d4f0ad9a6316e720c892de2b71ebb7cfafefd537994a7cbcbe94
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.8 MB (352836079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1fb3ca1a2847a3dcc1162b9da355a576afa8efb643648e708461a73bb75109`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:16:40 GMT
ADD file:ddf53eeecd4e99f9ac6dd446b84eed33212dae1b2a9476907b99dc988c316e5e in / 
# Wed, 21 Dec 2022 01:16:44 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 04:49:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 04:49:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 04:50:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 04:53:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9a50dadcc8beda7926088df1652aba274c8cf1817cd6956a9342f3b25db470e6`  
		Last Modified: Wed, 21 Dec 2022 01:21:57 GMT  
		Size: 54.4 MB (54373822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9716abced382581cab26adfab0007029a5bb1dda4112dbb4ba74c5cfc7f06ad`  
		Last Modified: Wed, 21 Dec 2022 05:04:22 GMT  
		Size: 9.6 MB (9596165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81dbde01939e5586504281eded1dd73c49a0b03f58c2cd890cc840b8267967f3`  
		Last Modified: Wed, 21 Dec 2022 05:04:22 GMT  
		Size: 12.1 MB (12128890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eadf6b46d5863b425edea1179a79cfa53aa4e33b4f2e8df8cfb2127727d75f3`  
		Last Modified: Wed, 21 Dec 2022 05:04:50 GMT  
		Size: 62.0 MB (62002362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b0adaac3511b77b3f22097236e252891819da52fcf18eac0b12d3bc48b2a18`  
		Last Modified: Wed, 21 Dec 2022 05:05:53 GMT  
		Size: 214.7 MB (214734840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f83b73067c5657f0ce93483cb3f6f4578ca182235d520f0dacf4a48b30fe279d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.9 MB (308865635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396957d2233c8d523a35370edd7c639124dacdc978376897ebe45a75dd138ecb`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 21 Dec 2022 01:41:58 GMT
ADD file:607007f7678c66cb1975d361bd26444fe0903e3a9dd7050476438a65264973e4 in / 
# Wed, 21 Dec 2022 01:42:08 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 05:23:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:23:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 21 Dec 2022 05:24:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 05:27:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9ac168fec9b2e04c14130a8666b154d956cef535df9b833dd775de5aa941079f`  
		Last Modified: Wed, 21 Dec 2022 01:48:22 GMT  
		Size: 48.7 MB (48719460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964a6f1008242d57a186240d9da881689edc71f02db9231b5dc700031a6a45f1`  
		Last Modified: Wed, 21 Dec 2022 05:40:19 GMT  
		Size: 8.7 MB (8650698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96489ea94aa4ff46b604abf252f7c3d707a5044a21c4015e6eeec8ad511daba6`  
		Last Modified: Wed, 21 Dec 2022 05:40:19 GMT  
		Size: 11.2 MB (11227271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35888d8608b914d92fb61d6d7e8a43bcf7933bf84d76141fc25d412ff47e6291`  
		Last Modified: Wed, 21 Dec 2022 05:40:34 GMT  
		Size: 56.3 MB (56332405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4aec40f6de35336999a503acc90b006bea7152456f79b4364f126aa5280d3f7`  
		Last Modified: Wed, 21 Dec 2022 05:41:02 GMT  
		Size: 183.9 MB (183935801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
