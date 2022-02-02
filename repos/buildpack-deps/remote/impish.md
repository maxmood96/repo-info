## `buildpack-deps:impish`

```console
$ docker pull buildpack-deps@sha256:dda2b1fe24acf9fdc391ee6aae8cf8d4bad719a479dc87c10104ed2386124385
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; riscv64
	-	linux; s390x

### `buildpack-deps:impish` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:37796c147908137c32720be9a867881045cb6f5dcacb0863899332faffa551cb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **406.7 MB (406694943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bb0c7549bbd6c4ddd57f13065f6e6c73b64e626ba60df935fd4dd9113465b9c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:15:05 GMT
ADD file:16b7fd02fce3322a13d01700f99fe66e6ed2e1973db3361b56f68beb1adccf19 in / 
# Wed, 02 Feb 2022 02:15:06 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 09:18:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 09:18:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 09:20:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 09:26:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:24496884391b0c292a71ad3f46bb689ff34f0dee4454901252ba7d52a977bbb0`  
		Last Modified: Tue, 01 Feb 2022 19:45:43 GMT  
		Size: 30.4 MB (30377763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c778222c5cf79311601885ba5ac2c44f0ef9dfcd186ef28e0563e6281c2191c4`  
		Last Modified: Wed, 02 Feb 2022 09:38:52 GMT  
		Size: 3.7 MB (3693950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f963dbeca763645c7dbb4b04280642452cc1ea615d22f35dbe1027666dfc08e`  
		Last Modified: Wed, 02 Feb 2022 09:38:52 GMT  
		Size: 3.6 MB (3552009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1778ab720dcf49f40ee01624db09f001f37d7267bd2825ca8a48d67547e0c1a4`  
		Last Modified: Wed, 02 Feb 2022 09:39:08 GMT  
		Size: 38.1 MB (38080407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a1832bb54dbcc4042ea968e2982545f87959604388f7676e143010056f6d10`  
		Last Modified: Wed, 02 Feb 2022 09:39:59 GMT  
		Size: 331.0 MB (330990814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3ecb825b4ba4182c2b50bb8b98bdc2df60232b22875c24a3a910eec7d6b3058b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.1 MB (371086262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24d38ad60acd7ec85e386c1f32b14b024669929fd1e0c865ee5e7eb7bab339ef`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:26:01 GMT
ADD file:32cc6b42d18aae85f2e55c58db7c21d70958ea4042c5a3b3d02fa68db5507935 in / 
# Wed, 02 Feb 2022 02:26:02 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:15:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:15:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 04:17:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:22:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:4a304b5b67cb0f88e02dba858b3d63b14bf2910fe10c7ca354d66076202e5a43`  
		Last Modified: Wed, 02 Feb 2022 02:30:44 GMT  
		Size: 26.9 MB (26918632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9de4838f1f90e55ad9c88ab8510ca88acc10d1fda129ced40c0308ef868b78`  
		Last Modified: Wed, 02 Feb 2022 04:48:40 GMT  
		Size: 3.4 MB (3443309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19780ca1848b91057df1dfb6c124559c11d3ca6da5cd58de559a02530a6435ef`  
		Last Modified: Wed, 02 Feb 2022 04:48:39 GMT  
		Size: 3.7 MB (3742850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be245cc30c2ccce63f465f04bdf365bea00f0feb8003968073fc6ffa6ee6d040`  
		Last Modified: Wed, 02 Feb 2022 04:49:20 GMT  
		Size: 40.3 MB (40284568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b132e9dae92e41c2da17c573f14f645bf806caa482247760469b6925c47de2e5`  
		Last Modified: Wed, 02 Feb 2022 04:52:21 GMT  
		Size: 296.7 MB (296696903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:45ae2d23516b4187cdfb306f6f701c53fe1da34c93bed8381cd72ee2b9db4460
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 MB (399347203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef7a65951069411f294813571709b0846e58fa1adeb2445cbd6f2d02c37f996`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:19:46 GMT
ADD file:af631b8d963a33e19a891426c5b4c15e0e884e9b3e5bebf20c2602a8640aa648 in / 
# Wed, 02 Feb 2022 03:19:47 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 04:18:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:18:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 04:19:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 04:22:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e5a81f6ca6c5971db4a3ff353799dac9a04be755a281494e34ce88fe67356149`  
		Last Modified: Wed, 02 Feb 2022 03:22:01 GMT  
		Size: 29.0 MB (29026521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ffbb61d29bef8270c292995b3dd80e5144e5a4d4b1338a0b2ee8aac62fa20cd`  
		Last Modified: Wed, 02 Feb 2022 04:36:55 GMT  
		Size: 3.7 MB (3678893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c6dbaef6d25df56d41df9e6b63a20f4af551c84f05741fa0ea2033e63e2da15`  
		Last Modified: Wed, 02 Feb 2022 04:36:55 GMT  
		Size: 3.3 MB (3327331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b6e4d6610b3c26e23acac9359af5ae84a00d1a630d0f2ae3ce8bd1d86a18e3`  
		Last Modified: Wed, 02 Feb 2022 04:37:12 GMT  
		Size: 38.0 MB (38032711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:591ff7e89cbfb705cd9fa2dbb0738b5d8e0b863ec269df7c48206b9cc7e7a737`  
		Last Modified: Wed, 02 Feb 2022 04:38:10 GMT  
		Size: 325.3 MB (325281747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4df551e142968245546b4d6ea5843acf0621063902be27c53a572ac507276ffe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.3 MB (414288913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64da9ec100d92380ed52dce16697e2ebcb95f06d049b596e837be7115ab08ce5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 03:51:07 GMT
ADD file:8e3408b07fced25894765792c2a819017c972ca15f54b605b365a78a78b719b9 in / 
# Wed, 02 Feb 2022 03:51:11 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 05:11:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:11:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 05:12:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 05:18:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:37685bfcfd86f994607875169656611b3d61a44ef3aff5a27a2ee9b2a9589d83`  
		Last Modified: Wed, 02 Feb 2022 03:53:55 GMT  
		Size: 36.2 MB (36174678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d645f1ef19c3c9982cb00d595afdd4a9918c56afe1ecdbeb41dc7fe949d2c034`  
		Last Modified: Wed, 02 Feb 2022 05:28:17 GMT  
		Size: 4.1 MB (4146831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aaebd659f835776e063ffc0860763d6764b0239ea97ab508dee0f7c2fbc75b`  
		Last Modified: Wed, 02 Feb 2022 05:28:17 GMT  
		Size: 4.2 MB (4242047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ac0e78337a0af9b9933ee48761cf18627bd32ebae2ce1b4773901bdc1ec3cc`  
		Last Modified: Wed, 02 Feb 2022 05:28:39 GMT  
		Size: 42.7 MB (42707765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bec44d7f3baa2871f635fb8dacf65f4541c3647295f82d9a27a766713bb848`  
		Last Modified: Wed, 02 Feb 2022 05:29:47 GMT  
		Size: 327.0 MB (327017592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:9d79c0b029bb5e59344ef9a337e7901ccb4422f51c3b972d543cf54a8e0caa13
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.4 MB (266357983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6f746a4f35e73ba6c2ed3e5971ebd8d55f42d16e853d38718493718545fccd9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 02:18:51 GMT
ADD file:aed98a49144458e8d813bb2fe41d35844f33ec0cd407efbbda660d7c4d563ef5 in / 
# Wed, 02 Feb 2022 02:18:52 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 03:29:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:32:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 03:36:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 03:44:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5ea871c1447312a914987af6fbf45d36b0530a692d2305da1d511d9e26964c1`  
		Last Modified: Wed, 02 Feb 2022 02:38:00 GMT  
		Size: 27.2 MB (27207633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a23d96fb726f08537ef498ee619dd3f58c6aadfc2e5be2db6b4de0582fc6a9`  
		Last Modified: Wed, 02 Feb 2022 04:28:06 GMT  
		Size: 3.5 MB (3490772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2938e8ee71b5edd912aad743966cca2640dbf9ecdaa556f981cf3f29855917ca`  
		Last Modified: Wed, 02 Feb 2022 04:28:05 GMT  
		Size: 3.8 MB (3804228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3411e8baf94412f94bfefca54e3dc444d33f2f70146a2df37d9a8e7a82749d24`  
		Last Modified: Wed, 02 Feb 2022 04:30:03 GMT  
		Size: 40.8 MB (40764085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8499384ab1aa3efa706ed66ff5ad18478928c8d0ea447b3e0e2221092ec8a29c`  
		Last Modified: Wed, 02 Feb 2022 04:35:51 GMT  
		Size: 191.1 MB (191091265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:impish` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:8c64f6f79fb7c0f4bc3f14a1c4f95db4fc8555b1caa1911cc4b2a0ab64f95b36
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367832823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ecb77d4a2112c0a00b2a1c91fc195793c24fea2f57083e0360dd22113644cbf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 02 Feb 2022 01:42:37 GMT
ADD file:3fe7050ee185df1177ad9379cb909109b7378a099eb79d22193a6156557aadbd in / 
# Wed, 02 Feb 2022 01:42:39 GMT
CMD ["bash"]
# Wed, 02 Feb 2022 02:12:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:12:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 02 Feb 2022 02:12:35 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 02 Feb 2022 02:13:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b7789252cadc365c0ef668a46558911d5a49589641581cf378f93ebf7f628cfe`  
		Last Modified: Wed, 02 Feb 2022 01:44:32 GMT  
		Size: 30.5 MB (30526428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7a0349055065a75c3dd86726ee33a39c10307e55f46198783b70736f5d71e9`  
		Last Modified: Wed, 02 Feb 2022 02:20:52 GMT  
		Size: 3.8 MB (3767831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244df8725100b92ceac2f708b84760d1b5ed6d40cfaa3e8c53902b76b2dc4dba`  
		Last Modified: Wed, 02 Feb 2022 02:20:52 GMT  
		Size: 4.0 MB (3963367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd28b2bdc4096507bcb4728309994780041c2e09763d6a3f19814a02fe2d20e0`  
		Last Modified: Wed, 02 Feb 2022 02:21:05 GMT  
		Size: 38.3 MB (38325419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3206b3a79f00d7019c686fb7923810b97699cb7d6b23100c4f7cf7610d85056f`  
		Last Modified: Wed, 02 Feb 2022 02:21:45 GMT  
		Size: 291.2 MB (291249778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
