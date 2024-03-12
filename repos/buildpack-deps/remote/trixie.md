## `buildpack-deps:trixie`

```console
$ docker pull buildpack-deps@sha256:6317e33e9a8c5c5234126cf91cb8152456b59fdd1be966d25c410e86d8999f14
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

### `buildpack-deps:trixie` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:8d5e5912bc9fdc287f89b87e7b97a615110842f6c6f3ed380dccef85a75ef6cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.2 MB (407168618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fe9616e1e3f166a5d266b413e8cf782bc58e4b587c8f350e61a2b2f143c71d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:23:42 GMT
ADD file:93e647bfd891e82156d7a13e0f0b194003855008967ec51e962ea0d70fc59ff6 in / 
# Tue, 12 Mar 2024 01:23:43 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 05:59:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 06:00:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 06:01:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:6fbaa46799c378c8b00a06cb5a2319bdd5ab7abe194cd97bbc9aec2daf476e9c`  
		Last Modified: Tue, 12 Mar 2024 01:29:57 GMT  
		Size: 52.4 MB (52360823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1767d006c9347102620ba4282bc383135a85f2d494cc82af4568dbaa79a48972`  
		Last Modified: Tue, 12 Mar 2024 06:08:15 GMT  
		Size: 24.2 MB (24160710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2af29457b55c7e48f1d7a6c2a6a8953b155a7d1f248122f397d12e999c14db9a`  
		Last Modified: Tue, 12 Mar 2024 06:08:33 GMT  
		Size: 66.5 MB (66471388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9abe1738f63ec1b49d32f4238b27705dd3aa9ac9f41a0c61042a977b1d590b21`  
		Last Modified: Tue, 12 Mar 2024 06:09:13 GMT  
		Size: 264.2 MB (264175697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:0b5b1728e14dc719b7e05ae6f2995481627cbc1252401ba7d203f9ff84b33448
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370321603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20d9d457deb3213140e7db5fa8f4cb6f0737fdde79fef188bacc9c37a387d70d`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:49:56 GMT
ADD file:3e60918b2fc6eb291458158f2b94b782320f758effe373fd6d0a5c58dd3e2319 in / 
# Tue, 12 Mar 2024 00:49:56 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:39:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:39:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:42:45 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:5d768e5bf180c947f8692477b575df3498b64f65e904bac933d0260cd957c8aa`  
		Last Modified: Tue, 12 Mar 2024 00:55:26 GMT  
		Size: 49.4 MB (49418029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deb2336dddcb338dd0f592faca75df5ec1dcd20bf4a99dac4ce09223036087fc`  
		Last Modified: Tue, 12 Mar 2024 01:45:26 GMT  
		Size: 23.0 MB (23040791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4717627ab561eb4522e931062c30f6a46c82295340d11e5dc75d76edc1d9ab28`  
		Last Modified: Tue, 12 Mar 2024 01:45:46 GMT  
		Size: 64.1 MB (64110351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bf88f764fa1a06579496041deb844ece94b3e50122989d7c5923264915c294`  
		Last Modified: Tue, 12 Mar 2024 01:46:32 GMT  
		Size: 233.8 MB (233752432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:14730d1c15aed4c1dc658391f0401e440e66b6150c7ca275563a4d856980c91d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348765010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5ee40bafaa86f16808cb6f0a87d05c6b9025f53ba9ac76034f4e1e123f29a0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:01:42 GMT
ADD file:653b30d78a37c262fc23750e2a51b4c22f86c5a03a005268cedcb42011759039 in / 
# Tue, 12 Mar 2024 01:01:45 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:15:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:16:18 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:18:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:84940e63db1cf18d5cf1aa5d0b2d913f1cfeaf6d1392975ee4542b2b21627246`  
		Last Modified: Tue, 12 Mar 2024 01:08:19 GMT  
		Size: 46.9 MB (46919137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f950b5c77433bb7df3cf43f999646d938e0afeca45ad4123d681d5aa08f1576`  
		Last Modified: Tue, 12 Mar 2024 02:23:27 GMT  
		Size: 22.4 MB (22354857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdfb6eab2ddb5d810e5dba3e205db88b240377b7edec7f49cd3ed75f824b230`  
		Last Modified: Tue, 12 Mar 2024 02:23:44 GMT  
		Size: 61.5 MB (61464848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af978e6eab93d4f4002c75853b2fbe20957974791a4b908c0dbc688f4d8c9982`  
		Last Modified: Tue, 12 Mar 2024 02:24:21 GMT  
		Size: 218.0 MB (218026168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:4b67cb90eaa2015aaa744912499f4c52e3dbaac67c67d8513db2d037624bcca0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.0 MB (395039157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e9ace6284613e137d577642b01f432e831f4077181bb1a3f2af947f0e1b7bd`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:47:23 GMT
ADD file:822f8ebf81dcb8d0c3abe6092460eb4cd185e7a4b5b794a9ebc4221cc30518c9 in / 
# Tue, 12 Mar 2024 00:47:24 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:31:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:32:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:33:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:abb8ff6184544bf5d189fbbab4286e594f2b7adc7d1feb51af49c007cff0e2c6`  
		Last Modified: Tue, 12 Mar 2024 00:53:00 GMT  
		Size: 52.2 MB (52191351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f6a2f77ef2eb04a7b071796c5ec48f48d3cc5f0577048728b1f064cfc42453`  
		Last Modified: Tue, 12 Mar 2024 01:38:42 GMT  
		Size: 23.9 MB (23878999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48cbf246385c09e5150a227c27b3c398dc21e65ecb2d6e2cffb90763484c5e89`  
		Last Modified: Tue, 12 Mar 2024 01:38:58 GMT  
		Size: 66.6 MB (66571239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130f968e94acf62d7846961e8741c83cd276a2e4493be157ca427fdff92bac01`  
		Last Modified: Tue, 12 Mar 2024 01:39:30 GMT  
		Size: 252.4 MB (252397568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; 386

```console
$ docker pull buildpack-deps@sha256:85ecd9118c07fbbee4b318cc8df727a0b4b985fe612fbd85a4b362cdf1a00f5f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403591654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa617fbb1162f878932a8279d6a8c3b118abf7e90143f99366527bd621328014`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:00:45 GMT
ADD file:37f9337bf11dc9e80356b325a83e455996065eb5a0bb7e34196dd3ab715908c3 in / 
# Tue, 12 Mar 2024 01:00:46 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 07:50:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 07:50:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 07:52:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:d38fd1f357db42e901e77bda285b7bc07b7f9c002000df3fbd114813ff6b7831`  
		Last Modified: Tue, 12 Mar 2024 01:07:51 GMT  
		Size: 53.2 MB (53172667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b95670c35235fad2d1e368da26e5ba78fff048eab444dc410d559b74309288`  
		Last Modified: Tue, 12 Mar 2024 07:58:54 GMT  
		Size: 25.3 MB (25279222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee00c582fb3599daec934a23e6b97ddc0777774e503ce6f678e758d6e93c1ca2`  
		Last Modified: Tue, 12 Mar 2024 07:59:17 GMT  
		Size: 68.2 MB (68248894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e817596709b154de561bd7bf62a8b1fd6dfd9e519ef22218e1193b6a268d89e7`  
		Last Modified: Tue, 12 Mar 2024 08:00:16 GMT  
		Size: 256.9 MB (256890871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:f997feb50e49f207dda1557846ccd22157a36b2564137e64c3e6dc8fe6e35afc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.0 MB (373973171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90cc589f0282ffb8bd194871990ffa0ef938ae6002bd9d5d09fc801f9f95f08f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:54 GMT
ADD file:b1a1fd9e7f874d3dc6cae10f09e49e08335ad86924ba543f9ff6c777d93c7314 in / 
# Tue, 12 Mar 2024 01:12:59 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:34:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:40:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9b0712382998885f6ab26afd04e80c46f04069a2491aab0d33d167a8539090c2`  
		Last Modified: Tue, 12 Mar 2024 01:25:01 GMT  
		Size: 51.4 MB (51407725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9f9dba4bf2ad9240436865bb873640b08db96046b128861417790bef43c9163`  
		Last Modified: Tue, 12 Mar 2024 02:52:06 GMT  
		Size: 24.6 MB (24624765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:add9f4278749b45fe2f852673b16441b5b51bcb148434e457ef125712328347d`  
		Last Modified: Tue, 12 Mar 2024 02:52:58 GMT  
		Size: 65.3 MB (65266884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff644ca173a256bdfb2ced66f9bd9b161ca1dc9bfea0f3d13d8174039fb375cb`  
		Last Modified: Tue, 12 Mar 2024 02:55:30 GMT  
		Size: 232.7 MB (232673797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:69ed7e753f15f4007de026a9bd8a1b700d840ae1327f241020c4f8070a237b19
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.9 MB (417852483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:464fb556ead85d31f149959c49da8af5d5718cd704e4fef21a09a63988f064bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:34:27 GMT
ADD file:ee3f9725c5da5d09634af5073dc8d63c0cf10c6ece6c7b0084a82d44eeaa487e in / 
# Tue, 12 Mar 2024 00:34:33 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:06:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:08:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:18:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:df0d8d793e684337100029abc1076242a4e60e57c67bb9ee5002155393dd3737`  
		Last Modified: Tue, 12 Mar 2024 00:41:55 GMT  
		Size: 56.2 MB (56240791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0231f2ef2e18927b6d6939bd530fca98be4ea26cbda154232692c64973723b7c`  
		Last Modified: Tue, 12 Mar 2024 02:23:59 GMT  
		Size: 26.3 MB (26256378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78176af6a8d257c809c4e8791b9ef8922786ed93b43b0d048108141528b3f6cf`  
		Last Modified: Tue, 12 Mar 2024 02:24:21 GMT  
		Size: 72.0 MB (71955605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc03bd8f369248b128d8c66e62902d61b2575348b75dc2e680c8c9d3ec33bd93`  
		Last Modified: Tue, 12 Mar 2024 02:25:10 GMT  
		Size: 263.4 MB (263399709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:trixie` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:abb8dfbb40f9eced783c56facec88675bd10de7c28f0951e71c203c8e64afa66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 MB (385271152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1391c0deeb431ae8cc777430e145c0ffd387ec5397a96ac6cbfe91859fa30be5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:12:17 GMT
ADD file:a763a87b7a749afb8ffcbc72555a671734dd9d842834384eebb8dd784135bfc9 in / 
# Tue, 12 Mar 2024 01:12:19 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 02:26:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:28:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 02:30:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:2f13ce6fc956957d2abf0abd272bd88a159c9cdf4a731647c572eb2581973c57`  
		Last Modified: Tue, 12 Mar 2024 01:23:47 GMT  
		Size: 51.7 MB (51738519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4953941dae1a90e29387e6e32120bb7c2ebca24adab5d68977c75cbd85a709bf`  
		Last Modified: Tue, 12 Mar 2024 02:50:10 GMT  
		Size: 25.3 MB (25296799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6744696380aedee2755d9dc38f57a9a70817812b1b1a78dccc3f68e5fe21f170`  
		Last Modified: Tue, 12 Mar 2024 02:50:27 GMT  
		Size: 67.5 MB (67548163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fd7821e4eb2a6c048664a350dbacd53cceeca5cc115da2101671bbdbfde45ae`  
		Last Modified: Tue, 12 Mar 2024 02:51:03 GMT  
		Size: 240.7 MB (240687671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
