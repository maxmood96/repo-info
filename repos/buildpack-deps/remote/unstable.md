## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:34590b12646f7f5c72fdf067907b1b36c606a8a37e7e1131baa2138a5efd8cfd
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
$ docker pull buildpack-deps@sha256:34d17f62f167127906dbf16ab20e8066d4499cb25ffd9092ca36354eb2137ffa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.5 MB (333469815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab6ac910bceae2addcab7681cef83d1216406cbb5ab8fe827ecc0cfd88657b1f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:23:26 GMT
ADD file:10087b555ac457b6a577fbbc8206355ac696e76dd49ff2a4eeeb27ac8b9f4cec in / 
# Tue, 29 Mar 2022 00:23:27 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:32:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:32:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 17:33:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:33:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:48f4b65c158eb45a0eb2daaee21a00efa6f1ed6e8943806281db050162c30174`  
		Last Modified: Tue, 29 Mar 2022 00:29:32 GMT  
		Size: 55.8 MB (55804401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946c2e447bb7ab1f67caa661b736f358b21370caba6f7c21d7093309266655c9`  
		Last Modified: Tue, 29 Mar 2022 17:40:25 GMT  
		Size: 5.3 MB (5269081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edad27b0c9c2e208a688817fa78f09e8d4f79e064a058415035ecdc886a7e1c4`  
		Last Modified: Tue, 29 Mar 2022 17:40:26 GMT  
		Size: 10.9 MB (10924339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adf21f150ff42a12da611d2d8abc786d9d5e6025c4274194eb2f048a06d044b`  
		Last Modified: Tue, 29 Mar 2022 17:40:44 GMT  
		Size: 57.5 MB (57460981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d742ccdefba7abd96ef7c732dcf30936fab48f8c0ae7f4070e6afaccd706a7c`  
		Last Modified: Tue, 29 Mar 2022 17:41:18 GMT  
		Size: 204.0 MB (204011013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:3840fdb969ba659fae3bab9864cf0077d44f9a4e47713762aa318ed56fe1a3f4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **304.3 MB (304337073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb103a87152d0db2c13382a63d583dee0cb3e0041bc187dadff1b6bab40fabf3`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:53:53 GMT
ADD file:8fcd736cc488ae6bc3f8a0a57f5454dbd34b0c05fd62d2bf748eeb34723c2a85 in / 
# Tue, 29 Mar 2022 00:53:53 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 07:51:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 07:52:06 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 07:53:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 07:55:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:07dd120b73b0ec25351ce0c0743306437c1d81e0ee7e06f053f28a0e58bfa81f`  
		Last Modified: Tue, 29 Mar 2022 01:09:52 GMT  
		Size: 53.2 MB (53206463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182e180f96ffc4d0dea65f46ebf08c1601dba09f8a2bb20ff2f15148ff227cfc`  
		Last Modified: Tue, 29 Mar 2022 08:11:41 GMT  
		Size: 5.2 MB (5164114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3369a2a9d3d9efecc9720a25d251260ac8afb4a7a974b188960c5a1759c27c2a`  
		Last Modified: Tue, 29 Mar 2022 08:11:43 GMT  
		Size: 10.6 MB (10597701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc501bba1675670306129a4d527e61027cd5077d145db1dbda301297e9f32004`  
		Last Modified: Tue, 29 Mar 2022 08:12:34 GMT  
		Size: 55.1 MB (55076642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4546533e2959c2ce0c1816df5458d2432baf3263de84565527da8f6f5e819313`  
		Last Modified: Tue, 29 Mar 2022 08:14:07 GMT  
		Size: 180.3 MB (180292153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:5d126e3e1621d581fe49bea7f6611fcf991fa6f89c76bde7d97ced1e00c8c35f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.0 MB (292995514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6ff4229230bad5268276e82a4983543d6913f1713db0ebdad884b99b1ab5ed7`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 09:34:34 GMT
ADD file:9aa47fa903f49c3cddd2c04ea6dfc8adc7cb3e1b8f49392eb4ef30199e306b55 in / 
# Thu, 17 Mar 2022 09:34:36 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 02:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 02:59:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 03:00:39 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 03:02:30 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d5abaa3393d9da88a4f8667cc7ed186e0fcf756926f31ba33f3b531a2db42031`  
		Last Modified: Thu, 17 Mar 2022 09:51:00 GMT  
		Size: 51.0 MB (51008095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a92e937e95ec8c4708c51bf5b42788af6dc7933017024adfe3755af9a222a4`  
		Last Modified: Sat, 19 Mar 2022 03:34:48 GMT  
		Size: 5.0 MB (5023856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f9c704ba15933d332549e911b8ecf5197b7956ef44f600fb06943964d50581`  
		Last Modified: Sat, 19 Mar 2022 03:34:50 GMT  
		Size: 10.2 MB (10244633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b84168887f66171a81e384a0ec065ccce1eed8938b60a25c845862b96da581`  
		Last Modified: Sat, 19 Mar 2022 03:35:37 GMT  
		Size: 52.8 MB (52834495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a49bc4f8ca4cbddbb3456d9c8e52b57be4cbdf7a555fd7b4179fb2a0da4dc2`  
		Last Modified: Sat, 19 Mar 2022 03:37:25 GMT  
		Size: 173.9 MB (173884435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:501e2e6c372423ec8ebb552a77ff38ab0803f239dec3836ebee358401d74a460
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.1 MB (326094379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d35215c91b2486c0b04b8f62325f9311723a124fc0fe568ed6879260f33804d4`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:44:39 GMT
ADD file:8299f759b242f8c95152a99fbc389eea6ad6b8b19eea94a657be56f01d578df6 in / 
# Tue, 29 Mar 2022 00:44:40 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:16:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:16:42 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 02:17:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:17:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:463f3634d113f916cceb251bf5bf6b13c658f1a17397f89d844d16b67f3015f5`  
		Last Modified: Tue, 29 Mar 2022 00:52:40 GMT  
		Size: 54.7 MB (54722054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c688c27b79d184159b856a3f01a1e54e1708c1934ad79a24b955d73839df742`  
		Last Modified: Wed, 30 Mar 2022 02:26:42 GMT  
		Size: 5.3 MB (5267182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c486a902e5d3841d1a069e3d537ae4f5d5fc8637861108f85a52f97a34b293c7`  
		Last Modified: Wed, 30 Mar 2022 02:26:42 GMT  
		Size: 10.7 MB (10691763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eedf871730e4574bab5587132479a1b5498891a84469745d8916f8a28fd2273`  
		Last Modified: Wed, 30 Mar 2022 02:27:02 GMT  
		Size: 57.5 MB (57488173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12547aa21775da7eb5514f967169612e9c66858849c23a04d7b374a36b2894b6`  
		Last Modified: Wed, 30 Mar 2022 02:27:39 GMT  
		Size: 197.9 MB (197925207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:8032cf6e93d99e4bc4281272cc14fc7613b880fd2d8a7fa21370a4288c41fa3f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **336.5 MB (336535254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a88e32f611eb58fb249f7448433e44000800a2b18aff1acc2b59b91675f9f68`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:43:25 GMT
ADD file:a09b15a232ef12356f8a381e48ebbc75da16b46600e0cc9849189196595b48b3 in / 
# Tue, 29 Mar 2022 00:43:26 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:00:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 18:00:22 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 18:00:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 18:01:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0847c00642d4fc3cd086952d88bb1c62b35fc1592abb8bb98b5f2580cbdf5cc5`  
		Last Modified: Tue, 29 Mar 2022 00:51:53 GMT  
		Size: 56.8 MB (56838514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b358597cf26cb0d69578f67ae8478edc056e17062702b8e9b5223d5ef224bce7`  
		Last Modified: Tue, 29 Mar 2022 18:17:32 GMT  
		Size: 5.4 MB (5399988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229c59efca77e15f2eebc343a63ccaff506b30dec30f8514f410554d9016a9db`  
		Last Modified: Tue, 29 Mar 2022 18:17:33 GMT  
		Size: 11.1 MB (11104016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33c14fb78209a987db23cdb8ca3da7ea675992fd648530b5b3cf73a82bc0598e`  
		Last Modified: Tue, 29 Mar 2022 18:17:53 GMT  
		Size: 58.9 MB (58873710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d4fd10171e3b0790d15012da0c252098c97efc803d5e1391555a963fac102e`  
		Last Modified: Tue, 29 Mar 2022 18:18:27 GMT  
		Size: 204.3 MB (204319026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:37e38d5015949e03668a65e7362e7c98e8cb1f1ee31e1049d3cbdff2e95610fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.8 MB (313772151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0d37a3af4023a855af820d639472145413a2456d8582a67c9f5a19dd01eaa9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 07:45:15 GMT
ADD file:8f554d1fa0414c8c5592687851c7ff4646547038f7d464423b75f57ecade0e16 in / 
# Tue, 29 Mar 2022 07:45:20 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 08:45:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 08:46:23 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 29 Mar 2022 08:48:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 08:53:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:024c5d1fff33205caaf39b2903eafbff594af3ca19d825c46db9f726a37cdcd1`  
		Last Modified: Tue, 29 Mar 2022 07:56:21 GMT  
		Size: 54.5 MB (54453471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1267a248cdd21e2291d70a49d2f9b0a81d371a99832c18a5c27c5cdfcd4ec4`  
		Last Modified: Tue, 29 Mar 2022 09:41:08 GMT  
		Size: 5.2 MB (5222051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:240eba6da1031777a8269c912451066c83703897876489a9be1d5150c27d785b`  
		Last Modified: Tue, 29 Mar 2022 09:41:10 GMT  
		Size: 10.7 MB (10672619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b9f55cdc16bc7b9ebb3d30b72adac432c7463267759bd2df4d8aef6337988df`  
		Last Modified: Tue, 29 Mar 2022 09:41:58 GMT  
		Size: 56.2 MB (56209506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3afedd46a003bdce17969c8f9f181ab2e675877e74792702500724ad14e46506`  
		Last Modified: Tue, 29 Mar 2022 09:44:05 GMT  
		Size: 187.2 MB (187214504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:d9ba1b8cde069181d8569cba60eb2549ed5485e6510f0d5fe41501c46c312af7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.6 MB (345624007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f587dac2210ffbe656137c9dab26ad24804802bf26a06f686f42fbe35f18265`
-	Default Command: `["bash"]`

```dockerfile
# Thu, 17 Mar 2022 11:20:22 GMT
ADD file:52ac257bb3e9b43a436c32541c15e9c3a00323e3e1d0b20273b81a572fb8d66f in / 
# Thu, 17 Mar 2022 11:20:27 GMT
CMD ["bash"]
# Sat, 19 Mar 2022 05:59:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 05:59:44 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 19 Mar 2022 06:01:29 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 19 Mar 2022 06:08:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d022277e505c1e9a57478a80b1b82e11b58551ebc0afcb5e723535b6ee105cc8`  
		Last Modified: Thu, 17 Mar 2022 11:30:38 GMT  
		Size: 60.4 MB (60406211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5191baf63a49f74aafee330281325a08a8d65451cc0ac632e8aa56129d9dca63`  
		Last Modified: Sat, 19 Mar 2022 06:45:43 GMT  
		Size: 5.5 MB (5543862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471dd71263fc10a8a1efc9a8fc7652bc8d0e227dafa1f6f9493a5a9779600d7a`  
		Last Modified: Sat, 19 Mar 2022 06:45:43 GMT  
		Size: 11.7 MB (11702261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b11bc794149909ceb1decbb8091901df40d21ad217894f0b435df98f07d5ec`  
		Last Modified: Sat, 19 Mar 2022 06:46:35 GMT  
		Size: 61.9 MB (61922448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee3ae284d96f0fad1536b463086fcf157b6739852e7262f87b4fa0c60d4a6415`  
		Last Modified: Sat, 19 Mar 2022 06:48:47 GMT  
		Size: 206.0 MB (206049225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:8eba6bd76e364d31f470138d12d10a3c1604ee5a3cef225f1a3f478f5abfc74c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.7 MB (342740508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a6357ff1e99d258d501d195f32663948044cc626d7fe2fa1ec67b1a910baae`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 21 Dec 2021 02:14:08 GMT
ADD file:1dc8a81ea9c954e594eb32623a82cdfb528586b569a915ba8f70a49f68a6f7fd in / 
# Tue, 21 Dec 2021 02:14:10 GMT
CMD ["bash"]
# Tue, 21 Dec 2021 02:56:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 02:57:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 21 Dec 2021 03:02:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 21 Dec 2021 03:10:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:f6b741955e06623f1924320507da1630323c4cf1d6489febc99917464e765860`  
		Last Modified: Tue, 21 Dec 2021 02:30:31 GMT  
		Size: 51.5 MB (51541457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91689f9aadadd96fe4e4ad4ed92ff1cb6a48034aedc9f41e14d54cf85bcdd039`  
		Last Modified: Tue, 21 Dec 2021 03:34:04 GMT  
		Size: 5.1 MB (5089016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a290be0dbc2a1d1f5f12db96d9dc0949f33b55d33712a23f37c71cb89606a3`  
		Last Modified: Tue, 21 Dec 2021 03:34:07 GMT  
		Size: 10.3 MB (10320854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44222df82131b4d925c2f594e50c018b1fb6d67154b22de79d99eb4cd4a356c9`  
		Last Modified: Tue, 21 Dec 2021 03:36:17 GMT  
		Size: 52.8 MB (52817006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f71e08edf3534b3a52b84e74759377bd253863a9cf43fa9dde36a31debd1990a`  
		Last Modified: Tue, 21 Dec 2021 03:42:27 GMT  
		Size: 223.0 MB (222972175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f4fe6a3a5612f747728cde012f9a984fa3309b2ea03fec79c91559bdbfe06dd1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.6 MB (305562398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e46d073d4453614f1a5afdd997a96836235fc7878ee5456178c6d7ea99b4f1c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 29 Mar 2022 00:53:06 GMT
ADD file:5143c5815a4282433726df7dd89926b3676994be1b8575d259b8fb48d6a6a4de in / 
# Tue, 29 Mar 2022 00:53:09 GMT
CMD ["bash"]
# Wed, 30 Mar 2022 02:28:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:28:18 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 30 Mar 2022 02:28:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 30 Mar 2022 02:29:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:c86b61bc0bc235576e3d7696ce7a1c21762146f539dc6eda8173ad30b9a4ad20`  
		Last Modified: Tue, 29 Mar 2022 01:16:39 GMT  
		Size: 54.1 MB (54056452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcff4b07483f3bf89081280922e0b152bf4d0bd3c9886eca04d4701cdfdc8bd1`  
		Last Modified: Wed, 30 Mar 2022 02:35:19 GMT  
		Size: 5.3 MB (5255620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34095a4004eb76305dc89b1fe0dd2923e12bd88528d9b779fd1ba62c9ccf1ed7`  
		Last Modified: Wed, 30 Mar 2022 02:35:19 GMT  
		Size: 10.8 MB (10818241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1369c129afe9ff16634f66b8ce0ef29c35ecd9d7bd06e6096ad4ad323968e9f3`  
		Last Modified: Wed, 30 Mar 2022 02:35:33 GMT  
		Size: 56.8 MB (56791466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b38c20a18278a21badc0a20b1e0b409f4b5924a508c6bfa5d0df6768db86fc5`  
		Last Modified: Wed, 30 Mar 2022 02:35:58 GMT  
		Size: 178.6 MB (178640619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
