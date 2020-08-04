## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:6eae610e26ecc512aedfcbdc29cc39eb8e2a42be03682cac7e2ef99790e148cc
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
$ docker pull buildpack-deps@sha256:ba4ca69b955aea1a99df15ca45a9b7b8e755f0659a620f66cb6cfd2454f735bb
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.2 MB (327169094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a26a192de0c331d49b9ebabb0f623f22c64d8af7523aa27c88b45179ea682f`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:05:41 GMT
ADD file:388f29164844b8493d30bf1feffd1158559ab161886928f977604c10f983a704 in / 
# Wed, 22 Jul 2020 02:05:41 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:09:21 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:09:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:10:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:11:11 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:babaea2ea26ef0e3e4a90ecc928d26bf25d699e1dcba843f16b8a2f0a153b3d7`  
		Last Modified: Wed, 22 Jul 2020 02:11:28 GMT  
		Size: 52.3 MB (52340330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a37a5f4c4c2303f8d9f818b910d8f9caefdb8cf414a4189c131fe87eac26c2d`  
		Last Modified: Wed, 22 Jul 2020 03:18:23 GMT  
		Size: 7.9 MB (7921724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a136692b9cb363269d4efa1edc43bf0b539b0495b6ab5f8229f02319829642`  
		Last Modified: Wed, 22 Jul 2020 03:18:24 GMT  
		Size: 10.6 MB (10580682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:044462b11abaf8b753d1589c7b6b7d8c20479da7e1c06538ea604786fbbbaa62`  
		Last Modified: Wed, 22 Jul 2020 03:18:41 GMT  
		Size: 58.7 MB (58733149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfb7456b55af4789d6610e90225f9d26a1a9f7353332ab848b40685125f99ec`  
		Last Modified: Wed, 22 Jul 2020 03:19:20 GMT  
		Size: 197.6 MB (197593209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e544c91b7be995fbb4b206628c10342c101fe046814339c1eebcf9ec81e7faf1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.0 MB (304957860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01896b6c49f87a2c564a6a490f28bf0590a84ea65b4c937ccc76c9c7e67a4d37`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:53:26 GMT
ADD file:72bf1dc350aa2201a007e97d34f6d8ae4edadbfae65004d87b70d8bde1ca66f6 in / 
# Wed, 22 Jul 2020 00:53:27 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:46:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:47:52 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:49:09 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:53:02 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3868d999f42cbdf70764edb51ce2454cdb2f061f76b646ca6b109e3294cd106a`  
		Last Modified: Wed, 22 Jul 2020 01:01:42 GMT  
		Size: 50.3 MB (50268734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f11ca48a92528806c80b7a1add7e641a3bc25a3283d24aebfe4773c1479ab72`  
		Last Modified: Wed, 22 Jul 2020 02:06:16 GMT  
		Size: 7.5 MB (7501174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b474db4689f860236c9af7f7821d8ec3e4df8bf30bfb7b4ae53cde9f435eb3`  
		Last Modified: Wed, 22 Jul 2020 02:06:16 GMT  
		Size: 10.3 MB (10266925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce30b915c952ab0005a807bbc2ae90c61bf483b7a5dce8c903239a7cceb790d0`  
		Last Modified: Wed, 22 Jul 2020 02:06:43 GMT  
		Size: 56.1 MB (56121622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9b578bafcccce2e437be6e08fb5fd23fccbc1e1b199d760215bb43ba22891e`  
		Last Modified: Wed, 22 Jul 2020 02:07:53 GMT  
		Size: 180.8 MB (180799405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:d9d27d51324f853ff613e44477b65d3df65a9a9902836b41d0b631282a25b8b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.4 MB (291380052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76891135e55d111ff78fc3b6835100cb62ab26b5c52ff6606be2ef3e207eb009`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:27:52 GMT
ADD file:3ab6a11382a4a9f69a874d734a83342969068fe2d2a62b325658fb5ac421f650 in / 
# Wed, 22 Jul 2020 01:27:59 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:44:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:44:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 05:46:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:48:45 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04602b0eaf483684b8d51ffeb79a3e05e2f29421e1090b3050c1b163ef02f10e`  
		Last Modified: Wed, 22 Jul 2020 01:42:51 GMT  
		Size: 48.0 MB (48046591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:663484832f716cffa80a12254c44159fcadc5117183e18db5726002b9044e907`  
		Last Modified: Wed, 22 Jul 2020 06:04:56 GMT  
		Size: 7.2 MB (7243496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3453c2f59de86c76b43dd0cf5ffaad07ce27d7ec246c4d7a72032197a5210d`  
		Last Modified: Wed, 22 Jul 2020 06:04:59 GMT  
		Size: 9.9 MB (9916091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27e96fca1be9fc01ca387bfd823078b2234cad7382c77e59910730c2ba80727`  
		Last Modified: Wed, 22 Jul 2020 06:05:26 GMT  
		Size: 53.7 MB (53716367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfcc639e2c7932f7e0816b437f1cda99394e1d84f690694ee40b908d013ec5b`  
		Last Modified: Wed, 22 Jul 2020 06:06:23 GMT  
		Size: 172.5 MB (172457507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:8052d1e5e55a9de04a3aa9f7e2e1061d9964e75ecfeb78d2dee986d518a308cd
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.5 MB (317477950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91d8b5b4b03fe86a499c628712fd5be59b40b8746dc7673f2f1c23ac9573919`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 00:42:14 GMT
ADD file:0f4a1ab6b889d98f711b241dde31787e633494e233067fe98dce73de73c2d7f3 in / 
# Wed, 22 Jul 2020 00:42:17 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 01:21:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:22:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 01:23:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 01:26:24 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:3af651ddf153ddf8519b20c192d158afb60045252366ddc81e15c938b792982e`  
		Last Modified: Wed, 22 Jul 2020 00:48:41 GMT  
		Size: 50.7 MB (50699554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18cbb2a684c92e31711be180ca45ac19643d88c12a51b2ffb58b6f120bc5ded2`  
		Last Modified: Wed, 22 Jul 2020 01:37:00 GMT  
		Size: 7.8 MB (7796374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bdf66380a30dc7828150f57df61c812d1fd653b195e8f5d57dcfb885adedbf`  
		Last Modified: Wed, 22 Jul 2020 01:37:01 GMT  
		Size: 10.6 MB (10588039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74e3c1552e3888e748a1827b0e10da06ab4a4d5d05b69a591c812b9a0a1dcee`  
		Last Modified: Wed, 22 Jul 2020 01:37:26 GMT  
		Size: 58.9 MB (58932485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea05116ddc0e3afba7bbe86ffe492c7bafbe738aef96dfeacf333a8bd487821`  
		Last Modified: Wed, 22 Jul 2020 01:38:34 GMT  
		Size: 189.5 MB (189461498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:b18132b6e78c700f173457febf5b324fa4f32af85c5a6cfd6d547058d9ad9fd0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.6 MB (336637619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f6a10c10b91e220f8b29b2ab0327edc86fc964b8008ab9206086104d7154939`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:11:12 GMT
ADD file:1c3529ea5c695a0705497b4510edaf2034b3d29a608dea3db741a4298a117d33 in / 
# Wed, 22 Jul 2020 02:11:13 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 03:32:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:32:31 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 03:32:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 03:34:07 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:32126ce0c55cb16ee9848f6d067e47a287f981a106ba123e3f2590544677f0e6`  
		Last Modified: Wed, 22 Jul 2020 02:18:12 GMT  
		Size: 53.4 MB (53433577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19d9e403cd592ae856cb4192dbfde1073d62172846377a957e99aa1612f15c17`  
		Last Modified: Wed, 22 Jul 2020 03:43:32 GMT  
		Size: 8.1 MB (8099028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23d35b0ead0819c716d1b9d778e65755014b69dde5807f1cf3a6c95a4a73dbe`  
		Last Modified: Wed, 22 Jul 2020 03:43:32 GMT  
		Size: 11.0 MB (10960296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a4001839767608296f1e2286d481abeca1f071afedceb18874a8f61061f2c5`  
		Last Modified: Wed, 22 Jul 2020 03:44:02 GMT  
		Size: 60.7 MB (60696001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c39de924b6414552462eeb23dbc5fc3be62fb6516a912af78e2a3aec7b23154`  
		Last Modified: Wed, 22 Jul 2020 03:45:22 GMT  
		Size: 203.4 MB (203448717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:333e3afb942c6adb32e2369e4f8cd6d4e6b085f40bb4bc4aaa2c8d086ad7522e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.1 MB (322083915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef5061935063627f85168c5ccd9956dc71e4c87012930ce3302dec430f7469d5`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 01:10:23 GMT
ADD file:ba027e751512c2bd75301e89e6e4ff2f37ba0d5a4dc18785ef0805c0c44217bc in / 
# Wed, 22 Jul 2020 01:10:24 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 10:38:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:39:14 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 10:40:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 10:42:33 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c1d6004a331270728a8745881ac080835166c19dd8097eeccdb751f6118875fd`  
		Last Modified: Wed, 22 Jul 2020 01:17:34 GMT  
		Size: 51.1 MB (51078870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fc8ab221636edeabd2df88a6e60355b1cd646986a8adb8b6e026bdb27a37a6`  
		Last Modified: Wed, 22 Jul 2020 10:50:36 GMT  
		Size: 7.5 MB (7450064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab2cfa46cbc90566aaca1e1931fc9c28d4dacc60e71e68bc28c5e245dc5a178`  
		Last Modified: Wed, 22 Jul 2020 10:50:37 GMT  
		Size: 10.6 MB (10598947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2dec4880e8fef552766207810870fe577d2c2340629a099ca64ee775cdbdc3`  
		Last Modified: Wed, 22 Jul 2020 10:51:31 GMT  
		Size: 56.1 MB (56101678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34cfcaace8f3082fd0cccc39efad851b7822f8366499c30306dc7fe8b42c1ba4`  
		Last Modified: Wed, 22 Jul 2020 10:54:02 GMT  
		Size: 196.9 MB (196854356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cce2d8cf5689aaf64c044fc993f6461904cdc2725ffa9a66b0b5f70721e68394
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342642397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3ccb3190284d81af55ee514fe95755b4a02bd00653d4b09d19aba8ab8a2d299`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 22 Jul 2020 02:16:35 GMT
ADD file:ca372c2f3271854631f36130adcf0999ef2bedda1861c3d9eca094bcbf3309d6 in / 
# Wed, 22 Jul 2020 02:16:42 GMT
CMD ["bash"]
# Wed, 22 Jul 2020 05:36:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:36:54 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 22 Jul 2020 05:39:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 22 Jul 2020 05:50:14 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:704e914d9d9038374759febe1260b7ddd11c6c32ee44b3d5a2acd6fca2eb8377`  
		Last Modified: Wed, 22 Jul 2020 02:27:16 GMT  
		Size: 56.1 MB (56108021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa1455254108cfbd56db733b944bb701f12d142214c65f55c6c8d9c19ac114c4`  
		Last Modified: Wed, 22 Jul 2020 05:58:28 GMT  
		Size: 8.3 MB (8347440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7df66bc0a63fb5a64c2f200a7fee03eb1d69456d7e592a131c33815d824035`  
		Last Modified: Wed, 22 Jul 2020 05:58:29 GMT  
		Size: 11.3 MB (11326980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924fc7758e94e614e9b4e8231caccc468bcd140ef85d8dd4c95997f395780fb9`  
		Last Modified: Wed, 22 Jul 2020 05:58:54 GMT  
		Size: 64.6 MB (64567829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d97b12150211a8c66f5a85fadce4b48a5b0add120855c9e88ba46ef8bc36830`  
		Last Modified: Wed, 22 Jul 2020 05:59:42 GMT  
		Size: 202.3 MB (202292127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:3b34c057b7f9828f7f97efdf7f2504a1d3761a155074fda0487d1e150c1f5edf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.3 MB (305347526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59ad895920dc5ec096ab32738427246de24450c765a8c9dcefdd47f74fc78e9a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:26 GMT
ADD file:a96b6121a19d104791604cd0cd10ee066e9d0f56abcc8f3f9cc1cfa691f2c4eb in / 
# Tue, 04 Aug 2020 01:17:28 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 02:24:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:24:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 04 Aug 2020 02:24:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 02:25:36 GMT
RUN set -ex; 	apt-get update; 	DEBIAN_FRONTEND=noninteractive 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1776f15db22f5bcf0f222cdcea18411e8904b4ebbb37ce537b90d8cea466e2cf`  
		Last Modified: Tue, 04 Aug 2020 01:20:17 GMT  
		Size: 51.0 MB (50989676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f212bdfa67a70fdb2386f3fb1144782ba98880a13323180bd4a44055bb72ad5`  
		Last Modified: Tue, 04 Aug 2020 02:29:04 GMT  
		Size: 7.6 MB (7590154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376f4dbf2b7c1eaaff8920fcd760496fead3e0e754c6b5a9d4122863158fba63`  
		Last Modified: Tue, 04 Aug 2020 02:29:04 GMT  
		Size: 10.5 MB (10456390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97873f50a31c377671799e4bea24e8ea9d922f2c499e800e0808c1f3edceaf9`  
		Last Modified: Tue, 04 Aug 2020 02:29:22 GMT  
		Size: 58.1 MB (58126605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9c73ff7dd05bf7b8ce9b2e5e31069074ed9699d3206b9a352f04185ca5531f`  
		Last Modified: Tue, 04 Aug 2020 02:29:48 GMT  
		Size: 178.2 MB (178184701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
