## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:ea34e08f3a66586eb937bbd443580165ea4a97f8882cde06b6bc93d869183738
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

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:0a833426bb3868692824094a9d5b47959d8736a4ccc12bc6561255ed08e18b7e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329043071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e37a106f5724dafdc951b677730a2b110d7032ff7951974ccac1bba01f27583`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:37:11 GMT
ADD file:96a5f24c28b0ba6960064c54e4643bc56eb6890db2c214c7d54bff6a00f9f049 in / 
# Tue, 13 Oct 2020 01:37:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:12:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:12:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:13:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:14:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:831751213a615bc3a20e0080e123bd3a2f1f1eef137b680b3101f3127cdff08e`  
		Last Modified: Tue, 13 Oct 2020 01:47:33 GMT  
		Size: 52.6 MB (52579873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0865ee0fc4d919fc9d8f50091271f48b9d93d23451b3b03fac42f42c4e96fa1f`  
		Last Modified: Tue, 13 Oct 2020 02:27:31 GMT  
		Size: 7.9 MB (7870921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99bd8b5719c34db0bfc0bc2bf3ed420adc1b98d9bd7b52a7210a5b240141fcfa`  
		Last Modified: Tue, 13 Oct 2020 02:27:31 GMT  
		Size: 10.6 MB (10627128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795dd20b363a5e86e17eef25246cf865107b7b53efddf0728732147795d47037`  
		Last Modified: Tue, 13 Oct 2020 02:27:48 GMT  
		Size: 59.0 MB (59046858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b495827a5788e90939ce7f236257dc18e7956840e3ce1a0a77a161de0c6c8838`  
		Last Modified: Tue, 13 Oct 2020 02:28:29 GMT  
		Size: 198.9 MB (198918291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bb54936596055d78534cd8dc24b129d01f35b794440205901c5d7abc442a6765
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306241219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:162b784ecf7d21c13940886b6202894fc810e84673fc8c9bfe85880502ba1874`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:50:20 GMT
ADD file:1aac38d903afb61492480cd4bdcc33919b418ac4dc88e3fb01b1d0a1589769db in / 
# Tue, 13 Oct 2020 01:50:23 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 03:36:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:37:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 03:38:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:42:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:17a424b21d91218fba0e197ed7ceea9ae2ea4b949acb3e096cdb220f324853f9`  
		Last Modified: Tue, 13 Oct 2020 02:00:22 GMT  
		Size: 50.5 MB (50502115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acbc82abbf9107f3acf2d4b2788cd9581852a883fe44f4875b8f32d23b2b04c7`  
		Last Modified: Tue, 13 Oct 2020 04:05:43 GMT  
		Size: 7.4 MB (7444491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:185e98d64e9c93a1facb94fa0c79188ed1d0c02d5280e1db1841f8df929613c3`  
		Last Modified: Tue, 13 Oct 2020 04:05:44 GMT  
		Size: 10.3 MB (10315464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21a9ff5754c6d1ea4ba2619fea44db11263cf5996571e57b4e70c83924137a6`  
		Last Modified: Tue, 13 Oct 2020 04:06:12 GMT  
		Size: 56.4 MB (56413402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5422cb72010bda4ac81f67f9ba8ed7856ea70b7c13ad26fa4e8b116142f619ae`  
		Last Modified: Tue, 13 Oct 2020 04:07:15 GMT  
		Size: 181.6 MB (181565747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:cf3ad7413a6d8b98f8664469c15b63ea69237b6a89245187490ab077d856310d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292373405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3e8236c96affcf7a8b1fefd455acf920d8d413e0451f796dbbc450b07be346`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 00:58:08 GMT
ADD file:fb1050c1c18a08781bda11a75976f0483098ae971141de440f987df6c3da5eb3 in / 
# Tue, 13 Oct 2020 00:58:11 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:30:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:30:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 01:31:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:33:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a1cc4a9f93bac620cf7887911c999122564026a7a9c2ca50766b3df4909c806f`  
		Last Modified: Tue, 13 Oct 2020 01:07:26 GMT  
		Size: 48.2 MB (48236859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517c91bf44a59eaea16877bae5d96e8e3739abbb8f93ededbe1a6edd9132e278`  
		Last Modified: Tue, 13 Oct 2020 01:54:44 GMT  
		Size: 7.2 MB (7184130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df823445c24dabde93145f0baf428b813928d6b636054a35a13293faaf42511`  
		Last Modified: Tue, 13 Oct 2020 01:54:45 GMT  
		Size: 10.0 MB (9958643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb060b2a6181fd285876f2f88e84e4bedbabc6cdcada618897d7e19b8202827`  
		Last Modified: Tue, 13 Oct 2020 01:55:13 GMT  
		Size: 53.9 MB (53945346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06174b6508d43e1bbc01deb7a0f32ef34f8efe6a17dcb592c795199825794d86`  
		Last Modified: Tue, 13 Oct 2020 01:56:06 GMT  
		Size: 173.0 MB (173048427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:84aacc2f78866f7d0a09f029aa4c76a20f424239b4c4d16d13d3d814d2a4e79a
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.6 MB (319635875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0e85e1a24547d1a1b58f2d1e71989e6ef8aa296ca876e3a3e5b8a3250d1f1b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:49 GMT
ADD file:78d9e0b86c707d2f2153d35cccb88e56434830b20463e2114857178cd2c28ed1 in / 
# Tue, 13 Oct 2020 01:39:52 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:29:24 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:29:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:30:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:32:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c45ba759b265011063551ebfd452fd79c0d477ff10d2fc0261e7edc8e46a5d3d`  
		Last Modified: Tue, 13 Oct 2020 01:47:12 GMT  
		Size: 51.5 MB (51484292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96906616e2d4ce424db1417d034acc953ef44b819f5866e2e98cde19ec79e22e`  
		Last Modified: Tue, 13 Oct 2020 02:46:01 GMT  
		Size: 7.7 MB (7742559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7abfcbcfc78d61faca659b2499d9df1584faa1fbc6589b71e7faa4bf3b8f6e9c`  
		Last Modified: Tue, 13 Oct 2020 02:46:01 GMT  
		Size: 10.6 MB (10636219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07f8a88f2319e4196ea3383a53797f7b79f7da093c44c6f0d17d2ab0c9c93299`  
		Last Modified: Tue, 13 Oct 2020 02:46:26 GMT  
		Size: 59.3 MB (59290998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380b28f7b37bee96a271a463852f4035929dbdee378ed1c80ebd3558edd53d32`  
		Last Modified: Tue, 13 Oct 2020 02:47:21 GMT  
		Size: 190.5 MB (190481807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:c9e955f92d4973f0d2580e8011db4029dddd255ace65c8e52bd34112fb339b12
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.4 MB (338351241 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe421d0cae1109570466b2b5e37aed6f598b2bd688b54b7f5a254d9600fbab95`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:42 GMT
ADD file:ddac7d3208f9bb85ea4273acbe09812b15d0635131191fc86bbb4bc2b6872873 in / 
# Tue, 13 Oct 2020 01:39:42 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:17:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:17:47 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:18:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:19:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a47de09075d002c62b36280b2b99d0486d6cd50266e6d6601b5c88535d032924`  
		Last Modified: Tue, 13 Oct 2020 01:48:03 GMT  
		Size: 53.6 MB (53627737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb79e160247595d474a4be5625892d5f99dae5a6432f72dfe50f479d8f1bd29`  
		Last Modified: Tue, 13 Oct 2020 02:36:48 GMT  
		Size: 8.0 MB (8046137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a31e3ced4c61ebf0b93021ede8fd74be48dc6b994fb61e0e99f0031dfa6bf3d`  
		Last Modified: Tue, 13 Oct 2020 02:36:49 GMT  
		Size: 11.0 MB (11015021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd42e0300ac0fec8fb6393766d3e7f40cc0ccaeb0188c68ace8079c1db610d26`  
		Last Modified: Tue, 13 Oct 2020 02:37:11 GMT  
		Size: 61.0 MB (60977331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364b7a80f13ec86449f125f6434ba7047f4b85fe0eba8962d9ac8e5488f349f7`  
		Last Modified: Tue, 13 Oct 2020 02:38:06 GMT  
		Size: 204.7 MB (204685015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:46c4cf6ef5abd0265db483b579416f1faf9c42bac18c24f3928f2dad54b2205c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.4 MB (316410124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20b4bb7da9b454b2b69d857b5aca23be63753b9b860c5c5949af3924df75555f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:08:29 GMT
ADD file:ca35129fd2f6a5420278e6a1790ba92b4afcb01f474e67f950b277b7d75db37e in / 
# Tue, 13 Oct 2020 01:08:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:06:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:06:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:07:33 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:11:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:abe3595453fb68f277799325ac06eb70b1ca68c849710051325993f2f22b051f`  
		Last Modified: Tue, 13 Oct 2020 01:14:37 GMT  
		Size: 51.3 MB (51279779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6290cae23b8ebfb371a811642ffb256d3e23ca0ff6150be76966ec0283d83125`  
		Last Modified: Tue, 13 Oct 2020 02:19:43 GMT  
		Size: 7.4 MB (7396581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeef5dab7e9de3f6b935b8bb68d316252a7ad220b1cabcd3f4a3a27344fecdfb`  
		Last Modified: Tue, 13 Oct 2020 02:19:44 GMT  
		Size: 10.6 MB (10639069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a13a51d0114bb5c79dec589b9cd66342d75d46442b19d37ecb4d4aea0903864`  
		Last Modified: Tue, 13 Oct 2020 02:20:38 GMT  
		Size: 57.9 MB (57903164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2bcc455ec4e252cd28e6969ff5c515126db1e3cae2686a0bac5476b467f0d37`  
		Last Modified: Tue, 13 Oct 2020 02:22:57 GMT  
		Size: 189.2 MB (189191531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1f24cd44d68a838789aef49f98dd8cf02062060c73a9f3652bb6302a15303c59
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.4 MB (344377550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5405673ae4e53462f89b9aa5e300afde40daef3c18e508ffac50fe203e0f6b0f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:36:17 GMT
ADD file:29c9502df00306ab143f7a4895ecbd5188710e18fa501d1931dfffe0d2281c6f in / 
# Tue, 13 Oct 2020 01:36:23 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 08:44:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 08:45:29 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 08:47:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 08:57:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e449e1f1ecdd90acbe5e4ea9a9f941aa8dcee06a83eb2eff72fe4dd55cc20576`  
		Last Modified: Tue, 13 Oct 2020 01:47:12 GMT  
		Size: 56.5 MB (56486527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b868bd306c5ff6ba6bbe52fb1cc3deaa47fed5a1362d135d89cfca87a684e4a4`  
		Last Modified: Tue, 13 Oct 2020 09:29:49 GMT  
		Size: 8.3 MB (8307201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca5bd324b7e56f3121bd85c3a06132da98d95654678c2a01b4439cab8adc5b5`  
		Last Modified: Tue, 13 Oct 2020 09:29:49 GMT  
		Size: 11.4 MB (11392086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26769c811da7971c25f9fab265e60dd509f2c8522ff89eea05deda913a34b33`  
		Last Modified: Tue, 13 Oct 2020 09:31:06 GMT  
		Size: 64.7 MB (64729192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77d111d1f21d3276ec3457e2a87edf499ebfa7d68721fabc9d29cc21105ffadb`  
		Last Modified: Tue, 13 Oct 2020 09:33:50 GMT  
		Size: 203.5 MB (203462544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:4ca60e0cb1c6de7656949811461c3c2746525b7f86c2531a3f2a6eabc3e6ee40
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.0 MB (307018262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb413057ae184fb8c1ca8ebab616b4d66f5fd67423a04c9fffb13ed33e68f22e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:41:35 GMT
ADD file:1952263a13d56f052b56241e876c31bad8764b58e4a2c516a99d4f39950caf39 in / 
# Tue, 13 Oct 2020 01:41:37 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:03:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:03:37 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:04:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:05:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cf0128f5938d0a765169c542feff60f3c439d59fb9c4be101b86202a01e6f72d`  
		Last Modified: Tue, 13 Oct 2020 01:45:00 GMT  
		Size: 51.1 MB (51118723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b959444d9f887602c790b9d941e7fb570dcef590dc48846b621da06e4ceba2e2`  
		Last Modified: Tue, 13 Oct 2020 02:10:25 GMT  
		Size: 7.5 MB (7541005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d524b8fa445700c4082be482549c0d7902ce50a93b37e1f7fc5d14c927285c3c`  
		Last Modified: Tue, 13 Oct 2020 02:10:25 GMT  
		Size: 10.5 MB (10505088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc7cb425e964f6a35cefee9f35323651b0036432a1ca4440bbc4126036b16886`  
		Last Modified: Tue, 13 Oct 2020 02:10:40 GMT  
		Size: 58.2 MB (58216067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ed4af2c71964ed4606363b55e28d07c977a0e1dd12ce3d3cc8f9669e378e43`  
		Last Modified: Tue, 13 Oct 2020 02:11:16 GMT  
		Size: 179.6 MB (179637379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
