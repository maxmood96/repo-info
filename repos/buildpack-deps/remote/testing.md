## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:5382d9fd452d0f2bd6d24fc8c7081b1d8e2e75fa1f4977c24bfb5a4e19fedc38
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
$ docker pull buildpack-deps@sha256:576d8f654e14e25e7b8276fd0d16ba3b8ebb588b794de94ed51c4a48eb4f5876
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.5 MB (338475903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f764fd7c2dd3b3cb74bbe69c5a82dd830839389f11d54048d23290c051e168cf`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:02:39 GMT
ADD file:1fda4c82a4eaecf44b3fc4eb92bb0aac8d81c1c87822bd86f8b52b3620b70420 in / 
# Wed, 22 Jul 2020 02:02:40 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 02:58:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 02:58:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 02:59:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:00:22 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c07b17c5753ba5920876a4091c37318cc0787c8027550cb13d9c1bd7ebfab87f`  
		Last Modified: Wed, 22 Jul 2020 02:09:11 GMT  
		Size: 54.1 MB (54102477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d597760a8071b7dad395d547ed7915e05c7d4fba09ba2c81e36fcf54c4a712d2`  
		Last Modified: Wed, 22 Jul 2020 03:15:18 GMT  
		Size: 6.6 MB (6607399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e255324867b8c5356029c240f78c0cf753ace14e42bbc98bb34675857b8afaa5`  
		Last Modified: Wed, 22 Jul 2020 03:15:18 GMT  
		Size: 10.6 MB (10584304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c716c6c862a6ed53f272071f72c0799b3304e67fe7335a4527865c9f20e553bb`  
		Last Modified: Wed, 22 Jul 2020 03:15:34 GMT  
		Size: 57.0 MB (57021425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f1cd4eda51de14f1d5af1e82415f0f7a7d77cd49edb9aa613866c6ffbd93d6`  
		Last Modified: Wed, 22 Jul 2020 03:16:23 GMT  
		Size: 210.2 MB (210160298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bfc921667d054022cf5744fc0f183d2316f29975293cc81797b54ce309caa0cc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.7 MB (308666831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d8214becc1ecc78ad1ffc736b45eab8e371803e254c1d306e37efefd146d99c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:49:13 GMT
ADD file:057073afde8372e5586242898989764dc7739ad5fc93c170548a9831952368b5 in / 
# Wed, 22 Jul 2020 00:49:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:21:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:22:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:25:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:29:36 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a9cdb0a98bd26018b67bc273d7a9bbd7c5d47c8ed8ba0b72c2024f049430a2e1`  
		Last Modified: Wed, 22 Jul 2020 00:57:48 GMT  
		Size: 51.8 MB (51782291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f77dbfe5f595e23e67fa5c93bcef27e0855291352f61d2818001054fe906d1f1`  
		Last Modified: Wed, 22 Jul 2020 02:00:55 GMT  
		Size: 6.5 MB (6486760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2244202796f405d730ccf4e2e91cedd51e3cb380515ba202422d289179a182`  
		Last Modified: Wed, 22 Jul 2020 02:00:56 GMT  
		Size: 10.3 MB (10271646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40ece8618b3e24af2eef118d18af9a0d027ac6a700decd318bd6c2cf58612bb`  
		Last Modified: Wed, 22 Jul 2020 02:01:28 GMT  
		Size: 54.6 MB (54590249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbcb183844fe239461c45475f65cf565f7a0b5c2e6258e88abb9709472e37410`  
		Last Modified: Wed, 22 Jul 2020 02:02:49 GMT  
		Size: 185.5 MB (185535885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a33b266efc9fa8bccc7d1c3f471f5911024f96e16c68029368087ee15fc1f588
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.4 MB (302393089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3473290ff5a55636aa734e2768a33ea40b79133aed3bdf1d16d04714849a10`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:16:07 GMT
ADD file:b12e6ee23a8c36af2c020959d86c9277008b6b54ceff80954502340dee6e145e in / 
# Wed, 22 Jul 2020 01:16:12 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:21:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:21:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 05:22:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:25:59 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9142e33629754cf85d79355e893c9c07e344f32f4fbe710c344514aada5f1b92`  
		Last Modified: Wed, 22 Jul 2020 01:39:35 GMT  
		Size: 49.5 MB (49461754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab191c0042bdb971560c33a6e7bee561ff37ce4309087897cad70ea149a1c831`  
		Last Modified: Wed, 22 Jul 2020 06:00:20 GMT  
		Size: 6.3 MB (6296595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:588773c504d467808703f4e8fb464799ea4ce5a0db4e5d91e73995846917d34b`  
		Last Modified: Wed, 22 Jul 2020 06:00:22 GMT  
		Size: 9.9 MB (9919209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12803f25cfc88d50ce8e086428f15a6ea8545773d80a6b6326e1e467f109832a`  
		Last Modified: Wed, 22 Jul 2020 06:00:48 GMT  
		Size: 52.3 MB (52260735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a879d21f5d891553610e041eec537390e9169ffa9d1bbe1d617029a20498ee`  
		Last Modified: Wed, 22 Jul 2020 06:01:42 GMT  
		Size: 184.5 MB (184454796 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:30d92ad1321fc59bb381f5035799610fec5373067bbc3efd3f101ffd8f9b9161
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.5 MB (329537288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90cd90b60a941d141fcff77308cfe5b60a4b4e459f268e1358b3dcc30f59c01c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:39:52 GMT
ADD file:19b87dac8088f103e1a9992c229b17344439af0da8af45bc6d678f69471077d4 in / 
# Wed, 22 Jul 2020 00:39:54 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:08:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:09:55 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:12:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:16:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:508fd3fb95b7fcde22f3f927caabf293cc04dcbdb4c45b85a5130d5122e12a0c`  
		Last Modified: Wed, 22 Jul 2020 00:46:40 GMT  
		Size: 52.9 MB (52886369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5915a33a39d2dc36bde47815617bc03c29dc80e9539719e24091c59faeb64f73`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 6.6 MB (6634801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696ea5d467b9d2286b1dcd428b411982c7ca3d5a2471f013ef721842af48ec9b`  
		Last Modified: Wed, 22 Jul 2020 01:33:46 GMT  
		Size: 10.6 MB (10591622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ce2f62ac83f0fb7af53d2e4faa8b93e2b37157d2cfd0eb7725e95b633a33e1`  
		Last Modified: Wed, 22 Jul 2020 01:34:12 GMT  
		Size: 57.2 MB (57203269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40485f6c44a09a9e2f05943531673fd9c708341542a5319cedb5ac1627bbbb39`  
		Last Modified: Wed, 22 Jul 2020 01:35:14 GMT  
		Size: 202.2 MB (202221227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:314126cf071d0994c56db32b968dc02cd30b5cfc7a8c8a7c8126f1ec6b82df37
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.4 MB (345426730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f597152eec479649bed320e2fb55b6df8901ea8ee076225944f393a5f8101b2c`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:08:16 GMT
ADD file:ca0e279e6fd6eb980b9731b695496074a130913346e67625acec79226fc6c10b in / 
# Wed, 22 Jul 2020 02:08:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:17:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:18:07 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:18:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:19:53 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f7fe72ad45ca30a1e73e494824a081709c2e449cb1bac8b4deb1b1a29c62e6c`  
		Last Modified: Wed, 22 Jul 2020 02:14:35 GMT  
		Size: 55.2 MB (55225022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3647f8e1aff936bbcccf16d2eb142f694cf4736d8d8adfaf3114569bc553035`  
		Last Modified: Wed, 22 Jul 2020 03:38:03 GMT  
		Size: 6.8 MB (6808980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a520a2450f762082c65c471256beae8c5f1c15f69b32c692c574b4c4caa4a20d`  
		Last Modified: Wed, 22 Jul 2020 03:38:03 GMT  
		Size: 11.0 MB (10964527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b88bc4c73fa3892709b4f76b34086d1ddc06082c734c3e2fefdf5692a46913`  
		Last Modified: Wed, 22 Jul 2020 03:38:38 GMT  
		Size: 59.0 MB (59012743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3630d7e6a89531faf0872d967ba323939a1240ce7cd1bdedbb7d671a36684ac6`  
		Last Modified: Wed, 22 Jul 2020 03:39:55 GMT  
		Size: 213.4 MB (213415458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:9da20f824f11fa13477e33c07ab060623886ce1da5f758d209c638b56a7ee9b7
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.9 MB (319874539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c866a83bf93709cd9e37e9252aaf63586b126dbbf4aeb54314de72f57f3f1f5b`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:08:31 GMT
ADD file:7401625ebd06dafb2256bbcc5a70246e5e6282bcc356478f05fd7ddcaa55003c in / 
# Wed, 22 Jul 2020 01:08:32 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 10:28:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:28:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 10:30:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:33:56 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c240b05d7ff10891b36c505769b275684894e6a8ed8b5d40f20220a3da221e14`  
		Last Modified: Wed, 22 Jul 2020 01:14:40 GMT  
		Size: 52.4 MB (52358232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f2b31f704addd955e451fd2986f5159585f197625488725aac773df35e8478`  
		Last Modified: Wed, 22 Jul 2020 10:43:19 GMT  
		Size: 6.6 MB (6568575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30eb65f190ba6e9a301c9609ece037a9e82a8414a773e19a288860911d2d844`  
		Last Modified: Wed, 22 Jul 2020 10:43:21 GMT  
		Size: 10.6 MB (10602660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7563c2a484b0d69603f3e34a17264d58b347499d427207d3713673838df0295`  
		Last Modified: Wed, 22 Jul 2020 10:44:15 GMT  
		Size: 56.0 MB (55977036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edb7f55f0ac968ad0301c5d97a07ef6c0e6a8ef3c836eb70d9d21e9f090977e1`  
		Last Modified: Wed, 22 Jul 2020 10:46:45 GMT  
		Size: 194.4 MB (194368036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:1f2586de3559b19e6165fc9c6b1e0ccb0d23107eb5ef8c5fbcb8eb6101edfc8b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.5 MB (359473905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2413afcbf69259985657f8ce4d87743d2733661f9047fd5df537f6ebb76a172e`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:13:38 GMT
ADD file:92efdcf349a6f1580ab27a2612939d75fc0e449e05e20e6385f5f7e409cd6684 in / 
# Wed, 22 Jul 2020 02:13:52 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 04:52:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 04:53:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 04:56:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:14:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1eb910fa0fdd2afbde1007491a0fe3461e3029a0c5950e2a5ea3a69d15cab80c`  
		Last Modified: Wed, 22 Jul 2020 02:22:28 GMT  
		Size: 58.0 MB (57953394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e46d2506c2944fcb5f8a4602131b518bc797e95e34ec5068a32eea4f31d2db6`  
		Last Modified: Wed, 22 Jul 2020 05:52:43 GMT  
		Size: 7.0 MB (6990284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2b78285d9f403581b34af8b80dc4d9f5f258ba139298995ee9c8fc3bf6a899`  
		Last Modified: Wed, 22 Jul 2020 05:52:43 GMT  
		Size: 11.3 MB (11331208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5785ab810f904f56ab9454018dbab7c040384b76f7a8c3fdabb9055e335ce954`  
		Last Modified: Wed, 22 Jul 2020 05:53:55 GMT  
		Size: 62.7 MB (62687631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b31c0806a046af21bae6374bc50816fa178ba340ebd127da86f00f6068375d`  
		Last Modified: Wed, 22 Jul 2020 05:56:38 GMT  
		Size: 220.5 MB (220511388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:9cefcd09c095b5ea139296f3eb5b28999e6b4ed05cdd056c053396e291a920f2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.7 MB (307651092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76a823d941314e3416a3c6e0e2ac2c88ad9ed2a1016166dbf74ad6372790873e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:16:37 GMT
ADD file:be061a89b8959a241d8303ec83a6494b37d71fe20736b073046173371101421e in / 
# Tue, 04 Aug 2020 01:16:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 02:19:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:19:49 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 02:20:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:21:49 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:67f968df5fed9ab1993b2cba53f4810f984f47936fce947baf7ef2e7d8a5a20c`  
		Last Modified: Tue, 04 Aug 2020 01:19:19 GMT  
		Size: 50.4 MB (50416822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789709f3eb6ec781e7bd5d546a438d9f93b42d8201f34934bb917541d98545eb`  
		Last Modified: Tue, 04 Aug 2020 02:27:09 GMT  
		Size: 7.6 MB (7590147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b17405c3991955650e0612638adcfcaec522e3c07552eb6b1924bd354bc8e608`  
		Last Modified: Tue, 04 Aug 2020 02:27:09 GMT  
		Size: 10.5 MB (10456481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d68e926add9df5b913b9031846ca2cf9730906d323525f8cf01eaea4906b08b0`  
		Last Modified: Tue, 04 Aug 2020 02:27:23 GMT  
		Size: 56.2 MB (56210651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23a70deb767730ec1748917bacaa90dc3d04f86bb83ad901ad4898c1798086`  
		Last Modified: Tue, 04 Aug 2020 02:28:03 GMT  
		Size: 183.0 MB (182976991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
