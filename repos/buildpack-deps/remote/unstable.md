## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:4b15ee65c787bf0d796a50f34b93a7ab6159d299b8baea2836b1777036c2b972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `buildpack-deps:unstable` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:1a03aa0d012064939b130972b0af8b8c92e56d8a348c5ac1312bdf1a4963a94b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.1 MB (321085419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26298bed7bb062bddc23ae8e3af026621813aeca9503e6f992be7eef3f3dd42`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:22:47 GMT
ADD file:68b1541306250f957e5f1035d80f5683c1ed22e73cf2f2b563adc52424897a09 in / 
# Sat, 28 Dec 2019 04:22:47 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 04:56:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:57:03 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 04:57:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 04:58:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d0b468739e287d7cd8fa8bcb34afb10216f12567d28caab345db8873c4246896`  
		Last Modified: Sat, 28 Dec 2019 04:27:19 GMT  
		Size: 51.5 MB (51479608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44261d6f427d89f764fcd9898d2845c7327812575dcc485436bb888b2ee1d0c7`  
		Last Modified: Sat, 28 Dec 2019 05:03:30 GMT  
		Size: 7.9 MB (7919965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd42132ce8afeea96ec992f4170f1b4fe9fa1a621a93dc2d236088351e29685`  
		Last Modified: Sat, 28 Dec 2019 05:03:30 GMT  
		Size: 10.2 MB (10183322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c16ba6f425320c83bd55536bb502f6e0b7064468bed05a5dcdbf0a13e9d892`  
		Last Modified: Sat, 28 Dec 2019 05:03:45 GMT  
		Size: 54.7 MB (54742028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a25030e962fd2e6934c589d89d5843df2d92e6833602ec2e97f45f5da0db86`  
		Last Modified: Sat, 28 Dec 2019 05:04:23 GMT  
		Size: 196.8 MB (196760496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:5e14a420d9ab5527e7c93b8f0bcbe3877cbc728ad7be11bf8fe27c25d4605ae0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.6 MB (293605287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41fc4950d0538d13c18bb815c8b5fcb077395065f8a547b3e35401cccbcc2d36`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:52:33 GMT
ADD file:e863dd2efdd5f4a6e29a4da391218d83cf13d07b263a55c438361d48079dd528 in / 
# Sat, 01 Feb 2020 16:52:35 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:34:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:35:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:35:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:38:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:25551be68c42d4da1cad9359e21cdc842a69363b035a77721ddf9ad7db276105`  
		Last Modified: Sat, 01 Feb 2020 16:59:21 GMT  
		Size: 49.5 MB (49540705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718af626bdc2f1b7d5facec6b5ba8016afa8bb5d691f4ead7274c55588a7bf48`  
		Last Modified: Sat, 01 Feb 2020 17:47:57 GMT  
		Size: 7.5 MB (7494164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19493feb9c608ccc1c197cb34c49c8902d9e560ef999db9500a91a6244e10e0d`  
		Last Modified: Sat, 01 Feb 2020 17:47:57 GMT  
		Size: 10.0 MB (9974015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9e0dd91a0c5d9c8d98b8511ad3af8cf0d03337280a36a0032e81abf0aaedfc`  
		Last Modified: Sat, 01 Feb 2020 17:48:25 GMT  
		Size: 52.6 MB (52595530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82ca5cef28f6f3687ed090119e19e308504d0b5832bebcd8ca8c8087dfb28e5`  
		Last Modified: Sat, 01 Feb 2020 17:49:17 GMT  
		Size: 174.0 MB (174000873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:b9ba272b7640e3c65dd6564cd702fdd42f2a5f2868eed3bdc6bf56beb380c05b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.9 MB (286857569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954ff2810c81634d11e0f31ac9d18d80872e83a8dfadfef127c1ebf533ee5382`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 05:01:32 GMT
ADD file:b5c7da33763f5d6cace9605e53bf483375c1f792de0982f47885c85b47304392 in / 
# Sat, 28 Dec 2019 05:01:36 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 06:55:57 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:56:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 06:56:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 06:59:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:9d5856d0eb425d736e9f4c60a79333c1933bada38a126c109eff8f1eb43a9c21`  
		Last Modified: Sat, 28 Dec 2019 05:09:48 GMT  
		Size: 47.2 MB (47210722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c3768cabb2504bdc0d3bf15c2e022ab2e94f61e198eb24b077cb6c5e620d5ac`  
		Last Modified: Sat, 28 Dec 2019 07:09:45 GMT  
		Size: 7.2 MB (7234041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfad613eea011450300250c8f76f687229e6483a59e575849962e519e171c0b5`  
		Last Modified: Sat, 28 Dec 2019 07:09:45 GMT  
		Size: 9.5 MB (9529582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbdba93dc41685dd6b3cc9be45d32c5995478ce980c4972401e0c1b17f7c5c70`  
		Last Modified: Sat, 28 Dec 2019 07:10:09 GMT  
		Size: 50.2 MB (50193053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d048b5d0f9a0634b69822f8bf5830246aa1a01da6bf253b54f91502476b43fd`  
		Last Modified: Sat, 28 Dec 2019 07:10:55 GMT  
		Size: 172.7 MB (172690171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:aed2c4a3e4e43421c93b83ed729b337d3c6280baa2137a00e5e7caa76e5b33f3
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.1 MB (314142528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f8e27a9c77624731a20a727defa10292ca4c55afdb91f744c94f5c4c132821`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:58 GMT
ADD file:636edb6845120aa418f3291c0858ab38c7d658cb2790c08b113e8068fe152a32 in / 
# Sat, 01 Feb 2020 16:42:00 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:26:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:26:32 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:27:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:29:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a3f06cbd9a524c44b9b8c92922dc9c06d87668d76af414bd34aeb7238502e475`  
		Last Modified: Sat, 01 Feb 2020 16:47:18 GMT  
		Size: 50.5 MB (50505966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66da598f357ac8ab4c813dc7a16cf57b1d0fdc7579b59a9a2cee24efb09f057d`  
		Last Modified: Sat, 01 Feb 2020 17:37:33 GMT  
		Size: 7.8 MB (7793001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a8f172b9e64796699f56dc5a838982165c0591f68740791b1d1e8971e09602`  
		Last Modified: Sat, 01 Feb 2020 17:37:50 GMT  
		Size: 10.3 MB (10252714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b48a71f1808040c4e34e7856e42f28683335784039b75aa3cc9c48c178a2bced`  
		Last Modified: Sat, 01 Feb 2020 17:38:15 GMT  
		Size: 55.1 MB (55123874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b205c9cca73b1948b444baccd361ff7c04660738b8cea8311d4025df8021c8`  
		Last Modified: Sat, 01 Feb 2020 17:39:11 GMT  
		Size: 190.5 MB (190466973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:68e487d8ce78d5563bfa2b21daa2125a85ab718f68ef1642777d27c5ef08b2ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.0 MB (331975869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be20678636c6b0e18bfbddcaac34a0a39e33e4572e4a5eb980327560862636a`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 01 Feb 2020 16:41:00 GMT
ADD file:941e54a7461d61d84748dacc44e888cce50acfb10e34f38a7e4083e19f23b7ce in / 
# Sat, 01 Feb 2020 16:41:01 GMT
CMD ["bash"]
# Sat, 01 Feb 2020 17:36:44 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:36:51 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 01 Feb 2020 17:37:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 01 Feb 2020 17:38:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8901e4e25f1677947cce32c9111e1a14e167a08c1c9b0f38aa3b62ad8dfa24aa`  
		Last Modified: Sat, 01 Feb 2020 16:46:18 GMT  
		Size: 52.7 MB (52679793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a37f13c8736e8d302836bf7f36d02b6d21c78ea34eaa0d441bfac8ab1e8c15`  
		Last Modified: Sat, 01 Feb 2020 17:44:29 GMT  
		Size: 8.1 MB (8093419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf161fe0fa72e46e5ea25da7008f0141c7c33bd269c543c8f95df1e56c25b90a`  
		Last Modified: Sat, 01 Feb 2020 17:44:29 GMT  
		Size: 10.6 MB (10622239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3013dd71e2203e20bbe8863f8023cad80c4bcc8e6c089ef172e39590a4d889ee`  
		Last Modified: Sat, 01 Feb 2020 17:44:48 GMT  
		Size: 56.8 MB (56759452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95d1ab430d64d5c26ff6a13037123e9961d6863d6762ab2dbb23f781d7130af`  
		Last Modified: Sat, 01 Feb 2020 17:45:39 GMT  
		Size: 203.8 MB (203820966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:aedf50c27b844a2ea8f3929c62edf13328290b6cee67c99e2b1e0e1dcc22379f
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.4 MB (340431991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18ce59a61bd1a93d3993f1426ee5ad8a87ea08ede9aa4696a3aada493ef1f001`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:21:44 GMT
ADD file:d7ba1f92f51134645d0c28cccf74dc6cc9cff62c18d1e7ea24e9306b603cc4c6 in / 
# Sat, 28 Dec 2019 04:21:49 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 07:04:17 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:04:43 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 07:05:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 07:11:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:a19f8e61b2d8b008c7115d66fcae892bce80e022931657219cecb2a15110c398`  
		Last Modified: Sat, 28 Dec 2019 04:29:56 GMT  
		Size: 55.3 MB (55284979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814b37b063181f0e69d2ffc211b88d130aa8935273a93f9155d2df7a1bf9c150`  
		Last Modified: Sat, 28 Dec 2019 07:23:51 GMT  
		Size: 8.4 MB (8352650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1122a79a4397f123afc0998256257fa3fcdfa99567d9a6e43d19cdaac02f9ee`  
		Last Modified: Sat, 28 Dec 2019 07:23:51 GMT  
		Size: 10.9 MB (10946018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5501c344b50ae868e0144d013d546e02a4c4033ebe9c8fc067ee90f568efc396`  
		Last Modified: Sat, 28 Dec 2019 07:24:22 GMT  
		Size: 60.0 MB (60040117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151bc72873e77d179d29fec41a6f95ed3cb89c5ec6bfc485bacb0f68449e78cb`  
		Last Modified: Sat, 28 Dec 2019 07:25:28 GMT  
		Size: 205.8 MB (205808227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:67b7ca4228dbb3ade38b603be9d7f2d7563da4caf763fd0744bc1e78230c5233
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301606262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4471198076e021f2e502bce9c0f612e463624f33bbdbd0dbc58bd19623f43dde`
-	Default Command: `["bash"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:32 GMT
ADD file:ebe1df568622bb8e8e8e3b2318d11550389d84f3196d3ade9aaa9ecfdecd1028 in / 
# Sat, 28 Dec 2019 04:42:32 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:47:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:47:56 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Sat, 28 Dec 2019 05:48:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 05:49:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:7d0208a582df93acf7a81d059abd969865a1e647765a53c87e2123fb6b283a34`  
		Last Modified: Sat, 28 Dec 2019 04:45:42 GMT  
		Size: 50.1 MB (50131585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46a42bc5c7805eb22e48c27565c0a108b60dd3c74386aea7cb2a2b367d00d07`  
		Last Modified: Sat, 28 Dec 2019 05:54:12 GMT  
		Size: 7.6 MB (7591630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77c311db77933f5cbc7d2dc6e649e1d95c34ce4c806932601722b88f9b28a61`  
		Last Modified: Sat, 28 Dec 2019 05:54:12 GMT  
		Size: 10.1 MB (10069342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc903c6290ae481b2ee639d7b0ce90ef144f5db8cf1c9f396e521df9b32214c8`  
		Last Modified: Sat, 28 Dec 2019 05:54:25 GMT  
		Size: 54.0 MB (53985858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe289d8445f03ea8910f2c2b83a54b83e51e04c3acb6514534b860fda702aee`  
		Last Modified: Sat, 28 Dec 2019 05:54:50 GMT  
		Size: 179.8 MB (179827847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
