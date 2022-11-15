## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:f3490fdae8f24607bedb5271d698999a92b40fddfbfceb1d3a62775b89461511
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

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:af1ce09a656dac88462672b2a18e58265751c2891129ac1c69b1da7ad01ab183
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.5 MB (341515849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf03db45463518898a5d2b3f34a0ac5808043201ff2b51ca07a25e6db41ef64c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:44:41 GMT
ADD file:635f36e1a46e6c28b2a6ab0637cca9e47837c3547b17916d1dbb2595fbeb0821 in / 
# Tue, 25 Oct 2022 01:44:41 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:26:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:26:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:27:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:28:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d90f8b044e56f2589b41d1fe9b249b85bde027855731c6f512f0f9401c99e68d`  
		Last Modified: Tue, 25 Oct 2022 01:49:42 GMT  
		Size: 50.6 MB (50641226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e6bcc62372cb6ad18c098f8dda6e9c5b3707abc6e74f2dae7f8032bf929e4d`  
		Last Modified: Tue, 25 Oct 2022 09:49:51 GMT  
		Size: 9.1 MB (9101445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d43887f8917a514e50f8816ba51125c208418ba87167de7d84979146bf6e06e`  
		Last Modified: Tue, 25 Oct 2022 09:49:51 GMT  
		Size: 11.2 MB (11180674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8959e14a7057e4471c7c2de00c4d7048aa8bcc79de9966ac8d3b137fb3cd114d`  
		Last Modified: Tue, 25 Oct 2022 09:50:09 GMT  
		Size: 57.8 MB (57842369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70592bbfea369bf093c07859ff56c840eef7e0bb191ea328a4e2beba61301efa`  
		Last Modified: Tue, 25 Oct 2022 09:50:46 GMT  
		Size: 212.8 MB (212750135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:7cd82ecc7e836463d8b3af97f8b641f01e0d12245d06dad3e5432fef84533c46
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312622143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7305d20ed1ef9601e68cb8ca9656b28caad165c6b35c17173ecfecee222e490`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:49:31 GMT
ADD file:08f8312faaa666d9d1d3cdf1e0ac577979317e8784c264b29b4d3399045d2adb in / 
# Tue, 15 Nov 2022 01:49:32 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:44:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:44:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 05:44:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:45:50 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:351340891f63641ac5516af46a2dfb6b370ea5971d604352dfe16a498646eb52`  
		Last Modified: Tue, 15 Nov 2022 01:54:51 GMT  
		Size: 49.3 MB (49284160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989d5b3af22bb23168efd5d127277e94392a88454e93916c8136bdbbbfdb6c07`  
		Last Modified: Tue, 15 Nov 2022 05:49:45 GMT  
		Size: 8.5 MB (8471398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ae7d5b628dfd536fe95d650285c66873a6d0e49fe2d657c2e7317203d6f01c9`  
		Last Modified: Tue, 15 Nov 2022 05:49:45 GMT  
		Size: 11.0 MB (11015001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88f1eeef7589c4ac448515182c2e3e5f648683d400190ea8e24edc498dfb4565`  
		Last Modified: Tue, 15 Nov 2022 05:50:07 GMT  
		Size: 58.1 MB (58119787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18b423886ff674e779806b6c3ff6744142783e50868dfe6a20a8adbadb844f2`  
		Last Modified: Tue, 15 Nov 2022 05:50:48 GMT  
		Size: 185.7 MB (185731797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:88b8e41554e7829c186a732b567c1846debffa7b2ea42f3ebd20269eb2ad389b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **300.4 MB (300434841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77c7511837c414255b12e0ae48fbcd47b5c8e9c00b0c07de574acc251cf292b`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:15:36 GMT
ADD file:072a31b7cfe6ee4e4a8e0832259c68a602abda7e1a6682cdcb28eba7f0705383 in / 
# Tue, 25 Oct 2022 03:15:36 GMT
CMD ["bash"]
# Wed, 26 Oct 2022 04:39:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:39:28 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Oct 2022 04:39:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Oct 2022 04:41:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c9040ceaeef63642a4aa2653b1350e028be0db975aa9a23c7e441aaa7dc5a11a`  
		Last Modified: Tue, 25 Oct 2022 03:23:25 GMT  
		Size: 47.4 MB (47411564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d13b466f981f25c2e1938044e245a8dca528315fa39d2e8a80709f09075fa43e`  
		Last Modified: Wed, 26 Oct 2022 05:13:18 GMT  
		Size: 8.2 MB (8204920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c85fa3e21298caffbfd811747b3acc6991bda175e560e8f8d9c2a8152d1eef`  
		Last Modified: Wed, 26 Oct 2022 05:13:19 GMT  
		Size: 10.5 MB (10458411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab70124f63ca402b0decd346eb68aadc1e78a44dca244108cb94bfbf22164a7`  
		Last Modified: Wed, 26 Oct 2022 05:13:41 GMT  
		Size: 53.4 MB (53361135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e9dc52ad49270c8841763f0dee2341c8fb0c8a364f096d8e9b18ad823f877d`  
		Last Modified: Wed, 26 Oct 2022 05:14:21 GMT  
		Size: 181.0 MB (180998811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4b73d2ba4f559d6cc52950ea729f7e77f2faf4dd801d975173ce1e40bf2684b0
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **334.5 MB (334512228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca95be34666851c488ef97bfc68fea2849b8b5a96ff2fedfd46c9c0afbd49c7e`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 15 Nov 2022 01:41:54 GMT
ADD file:ba227e9990636bcf4ac74991aee2f89f076de2adf7a651c75b55b2dc145b5340 in / 
# Tue, 15 Nov 2022 01:41:54 GMT
CMD ["bash"]
# Tue, 15 Nov 2022 05:39:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:39:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 15 Nov 2022 05:39:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 15 Nov 2022 05:40:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a4831e9d6ed52920992a4dda63cbeb8f430d77a27377294be499a02b93fb1e3b`  
		Last Modified: Tue, 15 Nov 2022 01:46:00 GMT  
		Size: 50.4 MB (50371180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28af2f647d544013c2979fcc9bb3234c113dc9496fa976cc4a2fdf6d0622b2d5`  
		Last Modified: Tue, 15 Nov 2022 05:44:45 GMT  
		Size: 8.8 MB (8849884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a70069958d3a3ba34e8ab2a47caf5d5f7b8a3be5ff9bb2a50385ea0deceeff91`  
		Last Modified: Tue, 15 Nov 2022 05:44:45 GMT  
		Size: 11.3 MB (11332918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ba53036e16acaf6e7813d2d4bee2d4d96501cdc5886dc90f6eeb8d38e8586b`  
		Last Modified: Tue, 15 Nov 2022 05:45:01 GMT  
		Size: 60.5 MB (60450848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d8c189be234de40926ab6fe25132ee8f35f15b424c57d057ab30160387c993`  
		Last Modified: Tue, 15 Nov 2022 05:45:30 GMT  
		Size: 203.5 MB (203507398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:5bd7bb5803c4f0ad919619492abe354c5ff051233d1fd15ab0b702dcd2fc099e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.9 MB (343886877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881b4643c019f8a58e6490838d5a8ad00df910743f87b1a3e581433aa83888b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 02:23:38 GMT
ADD file:80dabb60a37b1d88f3750adb85c9e159d00b55293f70ad93512f94bd3cfd99bc in / 
# Tue, 25 Oct 2022 02:23:39 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 05:18:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:18:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 05:19:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 05:20:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:367799113badd94b9683087d6086436649a1fb7127698c42b0d730f5bbedcf86`  
		Last Modified: Tue, 25 Oct 2022 02:30:22 GMT  
		Size: 51.6 MB (51625321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:564d2fccc59969c0b37e3bb8384bc6545a4cce125daa11c7e8b599ec0acac788`  
		Last Modified: Tue, 25 Oct 2022 05:30:00 GMT  
		Size: 9.3 MB (9282393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09be9213196e288bdcccf553107591d6fe4f04fccea4da55faea35dd79cfff15`  
		Last Modified: Tue, 25 Oct 2022 05:30:00 GMT  
		Size: 11.4 MB (11379737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7cf8ff2ca1128a94c435416195c01bd46e7b32191a4a225527692f374d4e31e`  
		Last Modified: Tue, 25 Oct 2022 05:30:21 GMT  
		Size: 59.5 MB (59473844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d348a2548fad4997feadc2b7be7e32cc9412c27e3208c57b624b3263c3c096c3`  
		Last Modified: Tue, 25 Oct 2022 05:30:57 GMT  
		Size: 212.1 MB (212125582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:d67dac23e695cb618d3f33fd540a8f175692e25a535297bae57c2780cab3b3a4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.0 MB (317034689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1042dbb74561c0b4f139076dbd57ce1a0626daca54852a9eb4f829521e41eccb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 04:39:58 GMT
ADD file:da7998228f2661dd3490a7bee754b7aaed5cf07ebe582e97b32c3985ad0d283c in / 
# Tue, 25 Oct 2022 04:40:04 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 09:39:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:40:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 09:42:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 09:48:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c2275c195d2a35a07739822efcd752aad4e9580392e4129bbac1f6cfe608ee1b`  
		Last Modified: Tue, 25 Oct 2022 04:48:12 GMT  
		Size: 50.9 MB (50901534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45280c218956111f5980d1b17036f589a29dca56a64f196bd8f0bfabf7b2966a`  
		Last Modified: Tue, 25 Oct 2022 09:55:12 GMT  
		Size: 8.5 MB (8465620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cd0404c18893ceb6c37012f16133ba8b3c876fa90176ae85b3f9d94f25dafd`  
		Last Modified: Tue, 25 Oct 2022 09:55:12 GMT  
		Size: 10.9 MB (10933561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d962f72168bd74a6b23bbb9da6e07f630f0cb6fa527486ce2dd2d42508351ac`  
		Last Modified: Tue, 25 Oct 2022 09:56:01 GMT  
		Size: 56.7 MB (56660389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd44cdb622809ff58a1a859aaac107e396cdfd275ca5cfe8197b16e09c112417`  
		Last Modified: Tue, 25 Oct 2022 09:58:11 GMT  
		Size: 190.1 MB (190073585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4a3598d62e23e3003db6e423ae264e43db2ff5657ec189e6f6d00f5c69e85a4b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.0 MB (352964297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992be19844bb6ce728b69d6af195e74bad155d8b12433dacfa7ba1c518fffaa8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 03:14:07 GMT
ADD file:6e9efd6bb77c835520332c88cb412f38f0d8573ec3347b090b77965e17131780 in / 
# Tue, 25 Oct 2022 03:14:10 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 06:17:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:17:20 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 06:17:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 06:19:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7a3962f6ac5b86fa159789ea1e9241ecbb956b3223e8312f7d92d7fbb8bf5485`  
		Last Modified: Tue, 25 Oct 2022 03:20:03 GMT  
		Size: 54.7 MB (54704717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c5225e6c97e35e08afc065bed0fb4156a1727da9a3e12b4a611189682c919a`  
		Last Modified: Tue, 25 Oct 2022 06:50:49 GMT  
		Size: 9.7 MB (9684744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39fe7c3b495d9320ca99478bfddf7a3fa0412a37c56ca95a4cc891ceb738e62`  
		Last Modified: Tue, 25 Oct 2022 06:50:49 GMT  
		Size: 11.9 MB (11937807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab9270b45cd7087efea37438ff9651d0078e51c8b476b199cfc26770079313e3`  
		Last Modified: Tue, 25 Oct 2022 06:51:17 GMT  
		Size: 62.7 MB (62679073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652adf8e207d919d0f1ddc84ad9fa208e1ec7d27d5573d5c3348e681a13f65b5`  
		Last Modified: Tue, 25 Oct 2022 06:52:18 GMT  
		Size: 214.0 MB (213957956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:3a887968fe43226ca614e3bdfba591197b3593e08bde65a9a38a179bf5715812
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.9 MB (359929860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0617997a465ac3f99d967a05d654c18e959edee32e325b2b1dc07db26768495`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 05 Oct 2022 00:39:40 GMT
ADD file:cff1e1a432929527e9bb64bde53e2b614c941bd4631b7bd3634fdda8a7240455 in / 
# Wed, 05 Oct 2022 00:39:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 02:26:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 05 Oct 2022 02:31:38 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 05 Oct 2022 02:40:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9cc6da93595cf4d9d589de999765cc4f1efa5e0d8e23ca6dd8b73b18afdc8189`  
		Last Modified: Wed, 05 Oct 2022 00:57:59 GMT  
		Size: 48.9 MB (48857821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554ce58712f86101a4716baede25ee43c9c1fc550b39fb4b3e5fa1622fd3b00b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 8.4 MB (8388012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd132871253f925889ef836099addcf830644843a64a1529bddc510390846a9b`  
		Last Modified: Wed, 05 Oct 2022 03:30:22 GMT  
		Size: 10.8 MB (10750715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73bfc76b3f6f1ba447e697e6e2190cf70e757458cce81446b79426ae4cccdb03`  
		Last Modified: Wed, 05 Oct 2022 03:33:00 GMT  
		Size: 54.0 MB (54018661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e7099a4ad88bc20a780df4c500b9445dc2cb39e8ac84d70a11e8903e5b6448`  
		Last Modified: Wed, 05 Oct 2022 03:40:39 GMT  
		Size: 237.9 MB (237914651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f3a95238e9fb25bdb30cf9bac9a31017e573719ecc1390cb196795031f399a69
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.9 MB (308907690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b76b4efc93df24f2f1e78a196a448ee70d9bf65a4f671e9a7d61ee0a29bad85`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 25 Oct 2022 01:14:54 GMT
ADD file:7dba2ae439c9f5da3fe962e867cee94eafc0b12a74939e13fdf987965ef8191c in / 
# Tue, 25 Oct 2022 01:14:57 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:32:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 25 Oct 2022 02:33:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 25 Oct 2022 02:33:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1430653806baea9ab2928a0d226c10ba8e7bf4b9b93398f9082ba16edfb2d4b8`  
		Last Modified: Tue, 25 Oct 2022 01:19:17 GMT  
		Size: 49.0 MB (49012977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa67452e329e71787509a1583923b8e1e83b22a2fb76e48111393a03205d4c20`  
		Last Modified: Tue, 25 Oct 2022 02:50:30 GMT  
		Size: 8.7 MB (8738304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7be163526b121ed701b3595b33b6d8755aba04a12b0fd801f9c899cbd3ebd0`  
		Last Modified: Tue, 25 Oct 2022 02:50:30 GMT  
		Size: 11.0 MB (11041665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04ea6534b4c7c78beb071314cf02af39dc48f27dffa56b6182c538fc47d868d4`  
		Last Modified: Tue, 25 Oct 2022 02:50:45 GMT  
		Size: 56.9 MB (56939890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e73095f949aa471b5db609eab93348cee45f8092aba617f080c27c32b8c06c`  
		Last Modified: Tue, 25 Oct 2022 02:51:14 GMT  
		Size: 183.2 MB (183174854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
