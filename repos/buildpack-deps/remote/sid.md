## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:9f9e70bda3355f95ae3c68c71f6cec8fbdc0b8eb711bec7eb3b4b8dfec5a3c65
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:2d724e84c047618a2b975715300185363777d290cb73e3c4b11aed8e9f010e31
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.3 MB (328251063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cf0ceffc63f4897c4cb3550aee9bfdfa28055b3596698ab36dadf2378b8ea7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:22 GMT
ADD file:9463b73933c9a0f2df3bbfaa2805027794a0e3a0cca69453b066ebc4644b6f06 in / 
# Tue, 13 Oct 2020 01:42:22 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:22:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:23:05 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:23:27 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:24:20 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ead5025e4e59e53184c941889a91b90e4e7af750b6f2e005952c8484512851fe`  
		Last Modified: Tue, 13 Oct 2020 01:49:57 GMT  
		Size: 52.6 MB (52587404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50bcb11b150787afba1f3af7ebbb7af8259b2b8b14121b74a6d0b01551ad97c`  
		Last Modified: Tue, 13 Oct 2020 02:30:25 GMT  
		Size: 7.9 MB (7879844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:455355c490cedd80caaa467646ef3389e55170d8520f80248b97232c03d34b5f`  
		Last Modified: Tue, 13 Oct 2020 02:30:25 GMT  
		Size: 10.6 MB (10628194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0e82f26a95e6e817a52816fabb1c5164fea5eb51bdf5a55955277dc5d11381`  
		Last Modified: Tue, 13 Oct 2020 02:30:42 GMT  
		Size: 59.0 MB (59047155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5970279c8233874ea12393d6fc1a98b3a21b62d2e43c2f6ccc4c9235341460`  
		Last Modified: Tue, 13 Oct 2020 02:31:18 GMT  
		Size: 198.1 MB (198108466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:cec8c943d9846c37bc32340e9ae6cb41d22f1d5972cc2b5e49e5be485dc120d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **532.9 MB (532935099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b723d756c3cbb20d4017f0b7a0c2d40023033cf399166b42f07ae943d34cc4a`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:55:34 GMT
ADD file:58fae6653444e7013acac8c8b5dfaf08005d4d143891d739c3d3054778fef031 in / 
# Tue, 13 Oct 2020 01:55:37 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 03:54:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:54:36 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 03:55:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 03:58:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1f0f5ab7eed797403be4921ebb3d1c13327fe3d6d4a586c0bb2f4661bf647503`  
		Last Modified: Tue, 13 Oct 2020 02:03:52 GMT  
		Size: 50.5 MB (50504754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df38c36ffcf1ed5e05b47278687eb424e5f086d52c07d18e347f65db5cc3f69c`  
		Last Modified: Tue, 13 Oct 2020 04:10:06 GMT  
		Size: 7.4 MB (7438960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:362f9d379e753d7558113cff6099afe40e5d24024073d4516e5d92be7fd2a982`  
		Last Modified: Tue, 13 Oct 2020 04:10:06 GMT  
		Size: 10.3 MB (10316002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0102362b274a4e9e6bfd5756e0eb1af7b07e5deb73c4a0cce590073ed342e25e`  
		Last Modified: Tue, 13 Oct 2020 04:10:32 GMT  
		Size: 56.4 MB (56413373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c12ec99eb2a834aaf6f77aff37e328285ccf977fa7a9d397250396813c8ef5`  
		Last Modified: Tue, 13 Oct 2020 04:12:48 GMT  
		Size: 408.3 MB (408262010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a3a2b619d23b26f422442bf6a49a440523164f41b8cc3da53fd4d33a1a1ae24f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291521971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d09151c03ed6f6032ed7be799c0b1c87bf885f234dc1ad28f34090af4caedf`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:02:25 GMT
ADD file:6b1218c9574b91ad91309c12b66b8a83d37f3a3ead47d7fc3a16e3c498e6e102 in / 
# Tue, 13 Oct 2020 01:02:27 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 01:43:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:44:17 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 01:45:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 01:47:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:107486c9309dafb8e1d046960e1dca3c02d5aae566c72f8113cbb0f1ed15f9ab`  
		Last Modified: Tue, 13 Oct 2020 01:11:07 GMT  
		Size: 48.3 MB (48255653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb01673e64e8a48d10056720613123aae28172bfeb11020a3aba43cbbac68876`  
		Last Modified: Tue, 13 Oct 2020 01:59:15 GMT  
		Size: 7.2 MB (7183442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3439ff31f32aefcdeeaf2b053e0f8857776f05392e92baaa254c5446d40fc`  
		Last Modified: Tue, 13 Oct 2020 01:59:15 GMT  
		Size: 10.0 MB (9959277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ce14a99f926f046b0d2295b27dd91ff454c774130961e9dfc7dfe01ee57ad6`  
		Last Modified: Tue, 13 Oct 2020 01:59:39 GMT  
		Size: 53.9 MB (53945863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d651fa76c78bf7bce3706e39153ffdd5b2a10ce5c4471eac32c389f5c7dabe0c`  
		Last Modified: Tue, 13 Oct 2020 02:00:29 GMT  
		Size: 172.2 MB (172177736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:61b7868a6af81aa0172e00be8fd81543a39e4e22224c37761dff50735833c383
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.8 MB (318849462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2412dfc16b9af04345d852920305abbb019a8dfbe1645a95750e8896d6b71867`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:15 GMT
ADD file:af62f3e6ea7fec61b2823188f91b0f3419596dad24e9f9303c3305a3747d4350 in / 
# Tue, 13 Oct 2020 01:42:19 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:36:32 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:36:45 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:37:20 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:39:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:77774dc39e62096b335ade088d1f9f15b9cfba84ef4b0106507ec53b4bd6290e`  
		Last Modified: Tue, 13 Oct 2020 01:49:29 GMT  
		Size: 51.5 MB (51483868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7d9ffc760782b4e9e54ad713a8d51c982bb91d4571cbcdaddfd15199b58c4f`  
		Last Modified: Tue, 13 Oct 2020 02:49:10 GMT  
		Size: 7.7 MB (7745936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3602bebd6bd88919236d9b8aaed761e14585cf0d0129ae39141683ca7678c032`  
		Last Modified: Tue, 13 Oct 2020 02:49:10 GMT  
		Size: 10.6 MB (10636757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac51bff55f8abd95fb04d6b1b6c83ce20aa95d629d93a8dfe0528a765db3cda`  
		Last Modified: Tue, 13 Oct 2020 02:49:37 GMT  
		Size: 59.3 MB (59292524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9155654167f28f15e5cfcc4f6bdf85b33934da0fc4e4e40444345bc624da6da4`  
		Last Modified: Tue, 13 Oct 2020 02:50:39 GMT  
		Size: 189.7 MB (189690377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:ace4d667bf4568ac6922fc270de099e110c23ba990571a0268cf0ac78c1fa390
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.5 MB (337538590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fb8cd2c861fe4d82db04eb51d280bafcd9195869bab05a41bc2226877b0991`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:43:42 GMT
ADD file:71e92b8b05766d1d5d02c013ee4e6bfd49cfe21c2bd5ab2182af02e5e2493796 in / 
# Tue, 13 Oct 2020 01:43:42 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:31:40 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:31:48 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:32:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:33:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04671281ee1c9a57e6e56404219f6ae19ebe375e509c240cbdce889f052d441b`  
		Last Modified: Tue, 13 Oct 2020 01:50:52 GMT  
		Size: 53.6 MB (53624141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47de0273945f6e2c47e2f3f03a477c27bd73945f6ad62e80267ca45b1bd029e0`  
		Last Modified: Tue, 13 Oct 2020 02:41:40 GMT  
		Size: 8.1 MB (8053959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1b0b6fad1e883cd355dcce25d38d601d02eefec153ce528a98d0b38d4a84f4a`  
		Last Modified: Tue, 13 Oct 2020 02:41:40 GMT  
		Size: 11.0 MB (11015595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd96c2e2dd5b064c3f2b4644f9c8fdf61eb3eb5e96cf1c4f144aa8bde2b402e1`  
		Last Modified: Tue, 13 Oct 2020 02:42:09 GMT  
		Size: 61.0 MB (60978237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e8125c209799681e45e53b073315d1047175119a1376a28125aea9dc738399`  
		Last Modified: Tue, 13 Oct 2020 02:43:31 GMT  
		Size: 203.9 MB (203866658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:5551fda0e7d7065875b1f0efca7abc92194b8869f13bc44eedc64d6b787379a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.7 MB (315657349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42b10dc98affb641616d6c446f74075a7277d2ebd45e0734f92b838cbcf3eb93`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:10:19 GMT
ADD file:ec8eebd9c015be5ae41233496690d158f5f7d31b3dbece81b6474018168d339d in / 
# Tue, 13 Oct 2020 01:10:20 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:15:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:16:08 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:17:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:19:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:acfd16a511fbf47ee6caac9e14f0361f1b2a477e4e410835a21a56951f404ee0`  
		Last Modified: Tue, 13 Oct 2020 01:17:27 GMT  
		Size: 51.3 MB (51292191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c8c36fecc594af5a0fcd22383157160ab20328027a9a7aafcc7876e036c074`  
		Last Modified: Tue, 13 Oct 2020 02:26:36 GMT  
		Size: 7.4 MB (7400523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07514ca8c30d4614bc9d748c8ca9dec4b2481d32639fe54cfc45cc2d68aee7a`  
		Last Modified: Tue, 13 Oct 2020 02:26:37 GMT  
		Size: 10.6 MB (10639538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ed89d809ac68ebf4610853e2f5f0dc9ef101c69abe8a4dc2fdb558e07ad9c2`  
		Last Modified: Tue, 13 Oct 2020 02:27:30 GMT  
		Size: 57.9 MB (57902889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11809af01c8b66491de92524dc13a9d9ad56989f28c356d3f2c7c7a40638b1a6`  
		Last Modified: Tue, 13 Oct 2020 02:29:43 GMT  
		Size: 188.4 MB (188422208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:c790cac0e67af756b066d8db3d2e787dccebec0d490b91a4c0c51d7c7b050c6b
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.7 MB (343692905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:864e1b70bf49af43c11b8612d98af166b3873d1d8df3f9f9c5044f14d5923e0c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:24 GMT
ADD file:7998a5d3f49a86501eb252e7dc54464d086e8239a5f918b15cd85dd11e7341bb in / 
# Tue, 13 Oct 2020 01:39:30 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 09:10:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 09:11:13 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 09:12:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 09:27:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:ab405c79eb283d457b4f978511bbef215699b366c926b3450f2a7cbc6a56e33b`  
		Last Modified: Tue, 13 Oct 2020 01:51:11 GMT  
		Size: 56.5 MB (56495338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38962ab4f4d37e5644006dc2c9a5a9b270448a5ea5ea29a387f4c7955497875d`  
		Last Modified: Tue, 13 Oct 2020 09:38:29 GMT  
		Size: 8.3 MB (8329668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8ecae68ecea0d3add456e8b38f9eef46b95731e6dfca00f430a45a774f2a19`  
		Last Modified: Tue, 13 Oct 2020 09:38:30 GMT  
		Size: 11.4 MB (11392727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfde9fce3dd7addbd894e0669be922a792dc5fa95b3ee33ffbaad4ac26cb393`  
		Last Modified: Tue, 13 Oct 2020 09:39:33 GMT  
		Size: 64.7 MB (64729412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d46a45659245d475e634ade7dc1cd46dae49e65a557b9b0552bff519712e46`  
		Last Modified: Tue, 13 Oct 2020 09:42:27 GMT  
		Size: 202.7 MB (202745760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7e68453efaca7d33d1d9a67c24e2d6024e99e199df9e6fac9afddc621c4bd69c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.2 MB (306227689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d33bce6d63064ce107e8cc171ba5f3e0898878f2ff0a39def169d2fb049580`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Oct 2020 01:42:39 GMT
ADD file:8ae741412fc2632b17f3119be3f00db5ac9da9165ec6ba803cecb706cca2e10a in / 
# Tue, 13 Oct 2020 01:42:41 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 02:07:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:07:57 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Tue, 13 Oct 2020 02:08:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 02:09:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:2f8a9ab7d8c65b5068769e112907fa3def6a9a81b79ba5632dcc28f6bc45c59d`  
		Last Modified: Tue, 13 Oct 2020 01:46:00 GMT  
		Size: 51.1 MB (51120285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c6c2e1d37a743e5cb89bea0fbf288f3c97c58bd5e1e111a310a1968a8fa789`  
		Last Modified: Tue, 13 Oct 2020 02:12:16 GMT  
		Size: 7.6 MB (7552593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d9d2e85355b3a65546bae45dcf206bd44a3e26e29009a1fcaaccec7cbdc9062`  
		Last Modified: Tue, 13 Oct 2020 02:12:16 GMT  
		Size: 10.5 MB (10505631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450cd2a37bc042631c0485843fea47b52793d6012a3c58241d6cbdca704d0c23`  
		Last Modified: Tue, 13 Oct 2020 02:12:31 GMT  
		Size: 58.2 MB (58217046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c76bfc5429411e41578fb3113ed993049668215d172d9c2d8f386b43083916`  
		Last Modified: Tue, 13 Oct 2020 02:12:58 GMT  
		Size: 178.8 MB (178832134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
