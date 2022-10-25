## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:ef275d36c79af8d25536e704a3c53d813d196ca9540a11985b98ca3da093c7d7
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
$ docker pull buildpack-deps@sha256:46fd0f039d6777f0284cd64b70c1040cab9f378ba6d85ee4b707b1a170de3ddf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342324380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0884915c27a5935af5e5b5d74ba464d8ab37de87155db970934c55ad64ebb3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:22 GMT
ADD file:3b158c11a921c91aa3cebf5651e59c21fe59da295d3edc56147fefaa760329ff in / 
# Tue, 25 Oct 2022 01:43:23 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:21:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:21:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:21:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:23:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3721e3e259583b8b78cfdeb51a553c189938925b902bceaa1f4f92e837fb9a23`  
		Last Modified: Tue, 25 Oct 2022 01:46:52 GMT  
		Size: 51.3 MB (51261783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71496268904f3a840d9bce0c685a75189d26a0bc17e7e433cb15e8591db71c94`  
		Last Modified: Tue, 25 Oct 2022 09:46:30 GMT  
		Size: 9.2 MB (9150622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6dabb627a933a05d9921efa339a1a23fb1601652ed637def09b8afb87cfde62`  
		Last Modified: Tue, 25 Oct 2022 09:46:31 GMT  
		Size: 11.9 MB (11876512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1e1b526d184c32611382431c10f26791b2bc6d4785b7447b03ea96bc5e4104`  
		Last Modified: Tue, 25 Oct 2022 09:46:48 GMT  
		Size: 57.1 MB (57122938 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc955867fb524b03c6c2d7f16f01603abb8e57aa6fc4fe0bb6fd6d097f2063a`  
		Last Modified: Tue, 25 Oct 2022 09:47:26 GMT  
		Size: 212.9 MB (212912525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d7f420e4177af2c9b91b120ebe9e979d0dcad3966763acb1ed21525041e635fe
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.9 MB (309899153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9046c47430ebdd5f5d55eed0c00fd443d2e16476c60f2500fb777b7b45a350e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:05:47 GMT
ADD file:226ff5e5e8066a03822e2865c6f72c554de94710c5664ee8bebd127d8aa32388 in / 
# Tue, 25 Oct 2022 03:05:48 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:08:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:08:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:09:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:11:36 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:cff7bd795d206b13b585de0da179a0c9616a5278eb7d74a97c97746085567403`  
		Last Modified: Tue, 25 Oct 2022 03:10:30 GMT  
		Size: 50.2 MB (50178371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40202823259eac4be0260092f1fb5f25fa9d866c32ec384dcadb0c7bb6bf8363`  
		Last Modified: Tue, 25 Oct 2022 06:17:42 GMT  
		Size: 8.6 MB (8599297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72794c6cd90917676f9d44ebd1f1f244c5564c41ea99e25ce09ad37df455551`  
		Last Modified: Tue, 25 Oct 2022 06:17:42 GMT  
		Size: 11.5 MB (11507226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0eb73f65f06d3ba6bd41e6c61146c374cf595cc07b9da8e8d08207cdff5b13c`  
		Last Modified: Tue, 25 Oct 2022 06:18:06 GMT  
		Size: 54.8 MB (54848363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ed4a8a2ecd9b8eaf5a1622f101fd89785ada6f5b963abb9d8a661f9a06bc76`  
		Last Modified: Tue, 25 Oct 2022 06:18:49 GMT  
		Size: 184.8 MB (184765896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:f8a1f3a13a8adaaea5da7e387c0c6867d981753b39f1e85cc607bb0e97fa47a7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298606196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:922e36dda65d9735b5f1feb9124dfafb756dd2899076bce2617b826416afae3c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Oct 2022 23:57:54 GMT
ADD file:9f3a74b8856c0affe36dd4e0700a8a2686a9d2275934fd9af95135f13731d10e in / 
# Tue, 04 Oct 2022 23:57:54 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:29:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:29:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 00:29:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 00:32:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b2ee1685df1bf13149eece9e0085c6befe355f21deeea69484a3ab1fab51e40c`  
		Last Modified: Wed, 05 Oct 2022 00:03:53 GMT  
		Size: 49.7 MB (49692608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237b865ef48770b9d41964e18461ec2d393677f4fc653a0953e9f0b9773d47ac`  
		Last Modified: Wed, 05 Oct 2022 00:52:01 GMT  
		Size: 8.4 MB (8396889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:902b8eea02f53006b302a3dbae787275ce520ccf78df670e0dcafbfd1c4e17cd`  
		Last Modified: Wed, 05 Oct 2022 00:52:01 GMT  
		Size: 10.7 MB (10661490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540119c620ce1fcebd013dc72077ca8f4751440b9eb633b56bd350f29e749420`  
		Last Modified: Wed, 05 Oct 2022 00:52:26 GMT  
		Size: 53.0 MB (53011353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a5488439a4130d35884d12b04702afc44c003d55109f1c35f807bec217827a`  
		Last Modified: Wed, 05 Oct 2022 00:53:14 GMT  
		Size: 176.8 MB (176843856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ee5b64f7e30f64d230a9ff27700194f9626fb19c2c73fe165d174212296040a2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.6 MB (331564773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84aff2caea9cce7230accd474a102aed797b4fe65257864e59b236a314318e71`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:44 GMT
ADD file:83253dd857c3f1ea456b2b77494a2d865a467a36c188ecaeaf493faa5afb4c1c in / 
# Tue, 25 Oct 2022 05:45:44 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 07:56:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:56:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 07:57:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 07:58:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:bec7a4c1eec818efa32bedb19eba072edfb65db7384f73efc2a6ee7b13a3ca49`  
		Last Modified: Tue, 25 Oct 2022 05:48:08 GMT  
		Size: 51.3 MB (51263048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c4dc154ad7b510114eae26976432c9de05c3e285368849cc3bf60481e326fa2`  
		Last Modified: Tue, 25 Oct 2022 08:29:25 GMT  
		Size: 9.0 MB (8982532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4415de5e6c24b057c96d4d8d3d21d5834d4e30729a87dda8eb4f92335d108f53`  
		Last Modified: Tue, 25 Oct 2022 08:29:25 GMT  
		Size: 11.8 MB (11833453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2f80dfabd19f4d09eacf6b535eddbd31119db80916887d34ccb44789d2c48d`  
		Last Modified: Tue, 25 Oct 2022 08:29:42 GMT  
		Size: 57.0 MB (57038097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d56771029d9a89dd111cdb7504b5beb3d00b15609edb9efb094397bcd1b35b`  
		Last Modified: Tue, 25 Oct 2022 08:30:12 GMT  
		Size: 202.4 MB (202447643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:cd231c46916a59c2c2bc5835368b83385c4b55bf48767e2a85292860022b37aa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344545856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a75efaa56b01dda2b7cfee3829312128b18b88f8201eb147e8e83c442bfb2e2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:21:54 GMT
ADD file:f47fc1d53965bb08e38b482e78bd79e3cbeecc53e586ffd88bff0e6fed0a1f3c in / 
# Tue, 25 Oct 2022 02:21:55 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:12:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:12:59 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 05:13:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:14:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:11f88873ba86e184f57ba78457d36c4f22e16eaffb9c293964adc7905e18bfe5`  
		Last Modified: Tue, 25 Oct 2022 02:27:09 GMT  
		Size: 52.2 MB (52224672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683bf09527f61248ec1a0fa70be7388069c28d961ae31bd3a05c43ae41192a7a`  
		Last Modified: Tue, 25 Oct 2022 05:26:29 GMT  
		Size: 9.3 MB (9330348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:823ddfa7a0daf2e9e0c4b6ce038b2e2cce83bde4ba9aef56fb6911d8241ca03d`  
		Last Modified: Tue, 25 Oct 2022 05:26:29 GMT  
		Size: 12.1 MB (12094186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f47813fb488b28b2af09c6f4d188832f52b886546c7885a3bb2d1b67b0d69be`  
		Last Modified: Tue, 25 Oct 2022 05:26:48 GMT  
		Size: 58.6 MB (58616294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7ff00f1ad533c8fdcd88e287626a678680009104d15d1e1eadf92ce8d913b96`  
		Last Modified: Tue, 25 Oct 2022 05:27:25 GMT  
		Size: 212.3 MB (212280356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:778a18de493e866010d895926647d9365f0371f5c271c8aa465b1455f8413308
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.3 MB (317259284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1d243a7e4baf1b08176c26cc13249fee00a8a029ff0a9cf0570ed183e08e3a6`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:37:41 GMT
ADD file:a1c9e78f0a426fb245eff7a26706bf5500c9afba4a267812a4b2ec71113c371c in / 
# Tue, 25 Oct 2022 04:37:46 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:20:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:21:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:23:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:29:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:132042cf7d4760fcfc85f263dd04337e03e7c8105a5e98f7b530ac7170f31a8e`  
		Last Modified: Tue, 25 Oct 2022 04:45:25 GMT  
		Size: 51.3 MB (51259641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d69a1dd49e6ce17928ad491f90ab6ce7d931f9c5e5a417a0d9fb3f1ce72b8b06`  
		Last Modified: Tue, 25 Oct 2022 09:48:41 GMT  
		Size: 8.5 MB (8513255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff5ed8c26291706609a5805858b3aef9cd315c13a4d16d8fb8a664ca1d3a86d`  
		Last Modified: Tue, 25 Oct 2022 09:48:41 GMT  
		Size: 11.6 MB (11632110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d9c909aca86b92807e96dc4b657562ad939143011fac9714484bea28dd5c02`  
		Last Modified: Tue, 25 Oct 2022 09:49:31 GMT  
		Size: 56.0 MB (55956122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80a540c329eb6a2509af5c67092906520069203b1f72125133cad98ae1e3426`  
		Last Modified: Tue, 25 Oct 2022 09:51:43 GMT  
		Size: 189.9 MB (189898156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:10b2439d4c94fc7a0ba39b4e84eaed23c271b8710fe08cfbd1ae8d6f6670d842
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.8 MB (353751941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c23610f60883dea822eec2be63953e6e838d90afc6601ab133f664b2867939f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:12:50 GMT
ADD file:1f55ca9aa64d69398e6bff99fdfd63dbf022ecefc46450a6fd32ae46e9718557 in / 
# Tue, 25 Oct 2022 03:12:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:09:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:09:39 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:10:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:13:34 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:264fa02db63011b604885c7feecaeb78fbee4ce4d8191fa5050f4fef88c74001`  
		Last Modified: Tue, 25 Oct 2022 03:18:00 GMT  
		Size: 55.3 MB (55338800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1baf225de572024a1c39187c5ece555fd8056d94bb80d56f889f4e825aa70b`  
		Last Modified: Tue, 25 Oct 2022 06:47:11 GMT  
		Size: 9.7 MB (9732694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55c6a98be02e0940d4fe69cf5b8ef19e3e86304cda7170f1dd085e4a01338a2`  
		Last Modified: Tue, 25 Oct 2022 06:47:11 GMT  
		Size: 12.7 MB (12677561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e65982f752eb81f7771ff52e7dc61db3a43a5e7b89882ff7934a391492daaae`  
		Last Modified: Tue, 25 Oct 2022 06:47:45 GMT  
		Size: 61.9 MB (61899359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3848d68d34827501ccc99d058522edfc766c2b8e572d9746ee9fe584768e46a6`  
		Last Modified: Tue, 25 Oct 2022 06:48:47 GMT  
		Size: 214.1 MB (214103527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3187110300a65451f0ac705920a497de95773130cd67d6e0c464fcd99b688388
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.8 MB (309800763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa4a44fa173102a4106d3d5e3dafaaa3a72e2769418c8076d5f4f047a14ef7c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:13:56 GMT
ADD file:92a462945d4b32c30f41478992b9ab30d452ac37b0ecef64e2325e4e99296ea8 in / 
# Tue, 25 Oct 2022 01:13:58 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:29:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:29:40 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 02:30:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:30:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:e544dc28605cf962b36f5ba4703f824c022460d64f8973e49764cd76163df5ff`  
		Last Modified: Tue, 25 Oct 2022 01:18:08 GMT  
		Size: 49.6 MB (49578501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50715b09b75ed5a3b59f5532be8529ac130746e899c823894a3ee91fc976a5ed`  
		Last Modified: Tue, 25 Oct 2022 02:48:44 GMT  
		Size: 8.8 MB (8785586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bb8ed5a6b2d134cb7b866721196b0adaa54ab94d27c13c65773f16fffc143d`  
		Last Modified: Tue, 25 Oct 2022 02:48:44 GMT  
		Size: 11.7 MB (11727044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b78b28a264fd0d8e36e29b1b3e4c349049eedd6af26957228a4bb291b7f90`  
		Last Modified: Tue, 25 Oct 2022 02:48:58 GMT  
		Size: 56.4 MB (56393185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7928bcdca7e0273482c1c8420378652a6c34aba7f44c83eef04a283ed7cb46da`  
		Last Modified: Tue, 25 Oct 2022 02:49:25 GMT  
		Size: 183.3 MB (183316447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
