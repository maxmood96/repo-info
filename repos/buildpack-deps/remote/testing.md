## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:d6a28c6065b345375effa26f1f20c545213d8f51c56d04e8bf0530ea817fed09
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
$ docker pull buildpack-deps@sha256:6b72bccedf4b5cf04ac8d926374b2c2861aebfbccd3e15664daae38832153f51
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.7 MB (416681821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17abef862ac079c96eddac76a9220d17fef1a06a6c36649daa04412066657107`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:30:44 GMT
ADD file:9465a54824a47fac7a8656f1a1d95dc38be8c06ce3809b905d67ff7ce345ce64 in / 
# Wed, 24 Apr 2024 03:30:45 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:18:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:19:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:0e07e2723f97d31d3cc6945b2518b9912a7301e652e09eaac68f1eec11330efa`  
		Last Modified: Wed, 24 Apr 2024 03:36:47 GMT  
		Size: 52.3 MB (52338632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d95ad0980b95c8ae82ca2a8d74a4757e86cf14913e53a8be04dbf6519d8fcdc3`  
		Last Modified: Wed, 24 Apr 2024 04:25:04 GMT  
		Size: 24.2 MB (24160698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7f4651e17e14aecbd72058c76b8f5915f16370760bf5b7f31b11a45b7b29e6`  
		Last Modified: Wed, 24 Apr 2024 04:25:24 GMT  
		Size: 66.5 MB (66510163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd558b06ca5667c4bd4c52006bb07d433fe6e22a4c110b3db65b8fcf8013eae6`  
		Last Modified: Wed, 24 Apr 2024 04:26:06 GMT  
		Size: 273.7 MB (273672328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e6a0071de199725ac708415e5b9bcc60b7b2726f82c6a3b92f826b0a6eb348c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.5 MB (378539654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52b20d7bfea576b7fb275dee9e98412fd64115b08cc0ab1e9a91750c838878f1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:54:47 GMT
ADD file:cc1e9468e81e521d409dd8b88fafcaaa5f105f627b1eaef62c896e916213ebc7 in / 
# Wed, 24 Apr 2024 03:54:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:25:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:25:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:27:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:65330d4a78bd6d548d7f0dc559b639551ef46dee6b7d5b6d0366a8e6d22f8ac4`  
		Last Modified: Wed, 24 Apr 2024 03:59:41 GMT  
		Size: 49.4 MB (49434297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcaaad035748a99175cae78a5b89744fde3b0a273b1aaa1a736ed21b63fea6e8`  
		Last Modified: Wed, 24 Apr 2024 04:31:48 GMT  
		Size: 23.0 MB (23040802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e41db2ec6222226bff823394d26463c48212fd9c5a9fbcc8944ff87735f08014`  
		Last Modified: Wed, 24 Apr 2024 04:32:08 GMT  
		Size: 64.2 MB (64153991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e463bbe05fde2c5e86389ac7b3ec3335a1a8c57241a5b96277b0af8295674f7d`  
		Last Modified: Wed, 24 Apr 2024 04:32:51 GMT  
		Size: 241.9 MB (241910564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:3b18288f21df3d40ece511291387ae9b93d1f58a3630f07f1d62a56e48c74c32
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.6 MB (356557171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd4b058730b2df6b077e05527d0d9112bb614489e311fe29e37490ef0d692ca`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:09:21 GMT
ADD file:68fc8102f9cd1f1d24d4c270a545146ee6a7ba7fb9d8b6f00d511cc30cae87d3 in / 
# Wed, 24 Apr 2024 04:09:21 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:59:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 05:01:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:c2f00d681f2c70b358e621ba07e5f58c2068fd56d05bd0f1fac5a67972fc1624`  
		Last Modified: Wed, 24 Apr 2024 04:15:19 GMT  
		Size: 46.9 MB (46930352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9505d03d248caf9d52b35ec3ac69ec1aa253a9f5ad5518bad0ae8fd609e08b`  
		Last Modified: Wed, 24 Apr 2024 05:07:26 GMT  
		Size: 22.4 MB (22355377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3232da5efc12f2d7cabc485881605838030d4d7e9d541756495a9373f151f95c`  
		Last Modified: Wed, 24 Apr 2024 05:07:44 GMT  
		Size: 61.5 MB (61511282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24f55b596c68faafe0c85866bd22e31c8eb20d9f2f7cee570eed5844e858aaed`  
		Last Modified: Wed, 24 Apr 2024 05:08:27 GMT  
		Size: 225.8 MB (225760160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:77e8b175fcd09ab4921f8ac5c42e0b10e2efa95760e10dc98b213bc799a8c0ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **404.7 MB (404666549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c51592755949052f0ef44195ea8358f1fbea1f77a0eff888fc2826e94d85cad1`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 04:12:22 GMT
ADD file:0611fcedfd3f34de99368066f2193d5e912fee03e8d663d92f515f68718218ea in / 
# Wed, 24 Apr 2024 04:12:23 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 08:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 08:39:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 08:40:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:96ea578e4fb99ec8b7369413659385f232783b73beb1fc1170a2a4bc40edef55`  
		Last Modified: Wed, 24 Apr 2024 04:18:04 GMT  
		Size: 52.2 MB (52199455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d800f2346117fe086ce6de506f15dc0c1c7d1b93d2e5f8d98fb752ae9c451963`  
		Last Modified: Wed, 24 Apr 2024 08:45:04 GMT  
		Size: 23.9 MB (23879131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8423a6b70030798688895ac141ff54481960263df825e749c0e4b82b267624c`  
		Last Modified: Wed, 24 Apr 2024 08:45:20 GMT  
		Size: 66.6 MB (66622297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99923b18efa401582ac6b46c812458306bcca3c33eaead5393b8f8ff63c46e0a`  
		Last Modified: Wed, 24 Apr 2024 08:45:53 GMT  
		Size: 262.0 MB (261965666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:399484dd9f6f5f163b02ca5be937723ea6477621f41ac79ff14c685303d7b0bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.9 MB (412862642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9786692b49a9192cb781337ab0c859408434f83b06cf6f942564545b9352b9`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:41:36 GMT
ADD file:ed473d3b605a6b0948955f74f5dca4dccb14a7d6cf9d219891c6110ba6572f94 in / 
# Wed, 24 Apr 2024 03:41:37 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:38:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:38:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:40:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d51399cd19ce178fe1bb087a7ed5b07667b07b1dd98716723177809157778ffd`  
		Last Modified: Wed, 24 Apr 2024 03:48:34 GMT  
		Size: 53.2 MB (53187646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e9cbfbb03c89e50483bc6f14d5feeea6ad8da1d06153c1bb027ef0f401de94d`  
		Last Modified: Wed, 24 Apr 2024 04:46:54 GMT  
		Size: 25.3 MB (25279252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd74f5811c9b909697371e2951aac6db5673f860ba43dd4abc538cc436c4947`  
		Last Modified: Wed, 24 Apr 2024 04:47:19 GMT  
		Size: 68.3 MB (68291957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c585e600b978ff1c55e00e2b7a75dcb3ef126aad90d0443205cda3349369f08`  
		Last Modified: Wed, 24 Apr 2024 04:48:20 GMT  
		Size: 266.1 MB (266103787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:51b617da853cfc54bff583e1fb14e5e4562d23861da2d76bd6c721ce9b3d4a60
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.5 MB (383501163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c35dd94881c561d21af0bb0c49378fa1cbb4ce99b9eb666524a2609b7bf385`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:21:02 GMT
ADD file:3528147ed2ff17c452628f4992045437579a2eb00d2eac617b8542d7706b58f9 in / 
# Wed, 24 Apr 2024 03:21:07 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:21:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:29:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3d9ec6cbd0472de02f68ab46797d6a2b9840ccc575c40d8562ede5007cd7622b`  
		Last Modified: Wed, 24 Apr 2024 03:32:27 GMT  
		Size: 51.4 MB (51411293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a78282402894106b7f446ef7995bf01264e8c063d4dc3f3d1cae34bb31b7f5`  
		Last Modified: Wed, 24 Apr 2024 04:40:34 GMT  
		Size: 24.6 MB (24624106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3a8c05e8087139d064ba2562c9f539168b11a8e1e618c0c8dd990ffddf0aa5`  
		Last Modified: Wed, 24 Apr 2024 04:41:26 GMT  
		Size: 65.3 MB (65301544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeade64008030ac5c43c0000a932fd2d0d43070bcbdc1a1b506b48403b69c2f1`  
		Last Modified: Wed, 24 Apr 2024 04:44:08 GMT  
		Size: 242.2 MB (242164220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aa5f3cdf5dc419b19e3eb4c5cbf6d07b7c0dbf29c3323c0d525b910744998aa4
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **428.5 MB (428508103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00d50bf0de767b5f3c4af32a2c56baed9a46ce4899d26d2677cdbb2bdac4d009`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:23:55 GMT
ADD file:49f2825f9c5b50843535acfc958249a70e087e06e06eb89df8fcaddcbf45564c in / 
# Wed, 24 Apr 2024 03:24:01 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:15:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:16:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:21:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:e5bb82112ecd21be1be5a4a97a1beabfa110a5d5eb34d4561d4a17294d7f44c6`  
		Last Modified: Wed, 24 Apr 2024 03:30:40 GMT  
		Size: 56.3 MB (56253273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1d091ba74dd77c332622f47e69c38784baad91176e28aa55e464ca78ff6b4b3`  
		Last Modified: Wed, 24 Apr 2024 04:26:37 GMT  
		Size: 26.3 MB (26256543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edbdc1bc67e9aaa4ea2e9acc9960c0bdca8a28b392ecaa8f1767e62f424e2f12`  
		Last Modified: Wed, 24 Apr 2024 04:26:57 GMT  
		Size: 72.0 MB (72007256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69550a4f2343629a469443c1d501764590f6d2e12838bd7de8108c05b40ac1c9`  
		Last Modified: Wed, 24 Apr 2024 04:27:46 GMT  
		Size: 274.0 MB (273991031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cf7285bfc24b69dc56c05777df4e548f77ca6c1d2feeb3e674ec6804eddea8d0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **394.0 MB (394012821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f426190e40ffbe660e5e0c7cf33524be40d61ce4ef6eb3c7b0d8d0f1e6e1e049`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 24 Apr 2024 03:46:49 GMT
ADD file:13427baa96123e72c30f8ac6ca708a7f7d3be7f0ac0833390d7414c8d1e438e2 in / 
# Wed, 24 Apr 2024 03:46:55 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:18:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:18:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Wed, 24 Apr 2024 04:20:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:3f21e8a280ca933b265ed896c2cfa5317f05fac17b7b290b87455ee5b3f92921`  
		Last Modified: Wed, 24 Apr 2024 03:51:44 GMT  
		Size: 51.8 MB (51766843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21cd83a1cb8c7c3071ddfefcd98acfb1745aa44bd51fc629f0c9a3a31f182565`  
		Last Modified: Wed, 24 Apr 2024 04:25:56 GMT  
		Size: 25.3 MB (25294940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d8c2beefb38b0b74b231a920769281b4b909f949acae01f0aefd2b33aefaea`  
		Last Modified: Wed, 24 Apr 2024 04:26:12 GMT  
		Size: 67.6 MB (67593897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9e51d20a6c24eb05deb78deadedbe4ef5240f39bdea73d117940a69e457ccb`  
		Last Modified: Wed, 24 Apr 2024 04:26:48 GMT  
		Size: 249.4 MB (249357141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
