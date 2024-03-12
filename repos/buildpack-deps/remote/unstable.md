## `buildpack-deps:unstable`

```console
$ docker pull buildpack-deps@sha256:1f2a209ff6724129807c9a7722bea5bf4d5523d5c9070054b5869cd0b7596cd7
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
$ docker pull buildpack-deps@sha256:c5f624e22f63eab74ad44c949c411907e08323fd94f954dc217eabeb8a1086b3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **407.1 MB (407116189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7d209584b062cf0549b2080529ebf79610669da99af4644b934a2841095e3e7`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:39:01 GMT
ADD file:d669b75a7533bca38f2c301c256ebdfa35812b13652db86b8742a30e6856fd74 in / 
# Tue, 13 Feb 2024 00:39:01 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:27:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:b49777280093cb58e1e93044ad56b006d1fb67107f14896ae3fd237faac8d485`  
		Last Modified: Tue, 13 Feb 2024 00:44:56 GMT  
		Size: 52.3 MB (52336486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0416ce76c708a01d23d622188ae0a4c0552e5a29d07378826ce051a51a2fc61d`  
		Last Modified: Tue, 13 Feb 2024 01:33:47 GMT  
		Size: 24.2 MB (24170886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab94778b4f8d542570a58f18b952aac258e2970cab96fd361b214bfa16118b00`  
		Last Modified: Tue, 13 Feb 2024 01:34:04 GMT  
		Size: 66.5 MB (66468254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80def60bd73e3a9a5705eaecdbe842048e3d84a1c605e6fae357e8be7cf6e617`  
		Last Modified: Tue, 13 Feb 2024 01:34:45 GMT  
		Size: 264.1 MB (264140563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:bcf7327d7f12ffc8a2a41a1f361e1cf6533d82877429896f0da0f01ae3fdc5bd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.3 MB (370331989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41519ced967b01b112d200b16c18a1a11bc1f34d907ed1811981430e1eb64146`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:09:36 GMT
ADD file:624f450cf1c3fdf8774bf8313557baecef902871c3ad8dff4410f14122f8c507 in / 
# Tue, 13 Feb 2024 01:09:37 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:46:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:47:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:50:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:24aea175239943bb2adfa7be646a8e0c040383dec937faf220aee85a3f296298`  
		Last Modified: Tue, 13 Feb 2024 01:15:26 GMT  
		Size: 49.4 MB (49423639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c530646f760ee121e031a3cfc99e5f7b580df8596f51a1f5e30e10af689119c`  
		Last Modified: Tue, 13 Feb 2024 01:56:34 GMT  
		Size: 23.1 MB (23051918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3a1cdabe4cc17ce6f55149b66ca7c16793fb014ff72d99cb1da643581eed76`  
		Last Modified: Tue, 13 Feb 2024 01:56:59 GMT  
		Size: 64.1 MB (64108591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de7541155b76422a64edf910ec2131b609a880f2b83ac01ac06abd5cb73d5ee`  
		Last Modified: Tue, 13 Feb 2024 01:57:51 GMT  
		Size: 233.7 MB (233747841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:a8a188b1ac61aeeaf35024c340f52f63a0132ba4657889d2e9437aca5527433b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348778060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3ad35eb2f1a3a5e5732ca672c9f3ce8c926a53741aa176c8e2fd0870378fe2c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:22:33 GMT
ADD file:fd66e10084783208c7cc3adad23d5c975d8f5be56c462c5a37d7a50fffacb677 in / 
# Tue, 13 Feb 2024 01:22:34 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:20:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:20:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:22:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:a9ce49138215d345df26ba8499250bd7c71ec90f1afb15a8ac29dcd7248b188d`  
		Last Modified: Tue, 13 Feb 2024 01:29:59 GMT  
		Size: 46.9 MB (46928854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bed3d75f3913415a967fa0e909adbaf536b4d7ca377cf97730e2135c92b5c0f`  
		Last Modified: Tue, 13 Feb 2024 04:30:48 GMT  
		Size: 22.4 MB (22360614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78cb86ad182c3cf9cfed5742a1bbd6365a9bcb95a5f378a558088dbcfe7364a`  
		Last Modified: Tue, 13 Feb 2024 04:31:10 GMT  
		Size: 61.5 MB (61467747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1496516de4f431d258aba363886cad002ce4f57baeffcdf4e252ed7edd24c0f9`  
		Last Modified: Tue, 13 Feb 2024 04:31:58 GMT  
		Size: 218.0 MB (218020845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ef6f4e52aedd829ce0de3122b8bfe1e5183b239ce9800e3afcf4907cf1d197ca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.9 MB (396879453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c044fcdcdaf492bfea47c5177557c1bf675e3cd2e85cc79f253d540155bdc1bc`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 00:46:41 GMT
ADD file:1202a56d8723ce5bee3f68e3d9488cef88889fe8b2bb138cde766ff787577a7b in / 
# Tue, 12 Mar 2024 00:46:42 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:29:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:29:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:31:28 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:8e7b106821c007c3c67e9a4d248bd2f87194491ad746f2aa752c5b0ba2fca099`  
		Last Modified: Tue, 12 Mar 2024 00:51:35 GMT  
		Size: 51.4 MB (51353263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa13c84a803d4b150b717babd5d0b89e39ce55a7c4c07cfbc3d34a5e4ce85a3`  
		Last Modified: Tue, 12 Mar 2024 01:37:43 GMT  
		Size: 25.4 MB (25434519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde6d0bb19e702e70dc6d3b44c7538729b197d5c5c229f8df55709b3de11f031`  
		Last Modified: Tue, 12 Mar 2024 01:37:59 GMT  
		Size: 66.5 MB (66509574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723b9d30029b8a3ce50c4cc475df5ca33be0f8c86a353160538d9108af4cbb3e`  
		Last Modified: Tue, 12 Mar 2024 01:38:31 GMT  
		Size: 253.6 MB (253582097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; 386

```console
$ docker pull buildpack-deps@sha256:251fddb93de647e92e5db9520b50e234245592088d0ea64935cc2fc9cc92550f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.6 MB (403617689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8e0fb16df1b72057c3fe1def6cc1a9b8c83fe2c54bd9320847a6a63ffc2d62`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:38 GMT
ADD file:4189b090bbf8678fcabd8dabb56450346892e68ce7343823f5a1de966a7cfba7 in / 
# Tue, 13 Feb 2024 00:40:38 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 01:24:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:24:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 01:26:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:986c70cdc0585f2b2041c18972cf24b00e1384bf0ae25efa4ed418df60c27f39`  
		Last Modified: Tue, 13 Feb 2024 00:47:09 GMT  
		Size: 53.2 MB (53166067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5992ae92ecc708d9f7dbc50c93a7a44033fbb23286817ad552428376a53b6b21`  
		Last Modified: Tue, 13 Feb 2024 01:33:35 GMT  
		Size: 25.3 MB (25291521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b34fbe23d33273890d47ce232e0ea3ecafabe7cd6f1eacdaed0132a34c12c8`  
		Last Modified: Tue, 13 Feb 2024 01:34:03 GMT  
		Size: 68.2 MB (68249193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef40ea4fb0aaa505ca0fc627a4b7f559f54d7f3a06a621779b84c00fb13dc3d`  
		Last Modified: Tue, 13 Feb 2024 01:35:03 GMT  
		Size: 256.9 MB (256910908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:b492a050d8bee6734d4e7fddf2b7dfc78e633a132a169b1e1700ee0a9229feb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.0 MB (374000250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35abde10cd1ddc508f26b152e3ed074e3faab5ae5a9689f6d148e8967c4806b0`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 02:07:17 GMT
ADD file:46b0dcd0e81e4f61221659b1260cc43869ec44a23c045f293f694b50a4ce89a8 in / 
# Tue, 13 Feb 2024 02:07:22 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 04:01:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:03:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 04:10:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:ba59fa1171a061c2b49e9de14015f71d0e00ec2a17b49ddcdd453a663a922bf7`  
		Last Modified: Tue, 13 Feb 2024 02:18:44 GMT  
		Size: 51.4 MB (51411523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11595e21bfcc750f6639cddb481d3bae82b987766fc917da9fdbb55241005776`  
		Last Modified: Tue, 13 Feb 2024 04:27:08 GMT  
		Size: 24.6 MB (24627275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6328e06fb256ea30715aa4016628a9149817a5fd5af519caa1fc97eed490e251`  
		Last Modified: Tue, 13 Feb 2024 04:28:01 GMT  
		Size: 65.3 MB (65264661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0279072739c3e1a41c7935740d8cbb0cebb904baa4052f248b0c7367bbdcc76`  
		Last Modified: Tue, 13 Feb 2024 04:30:38 GMT  
		Size: 232.7 MB (232696791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:cb959a6bb47eee2998308c197d3c0ca38ecc6b48e80abec53dd7ecb715a5c226
```

-	Docker Version: 20.10.26
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.9 MB (417863444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fdbe3e9b6748ebc3010b3c56484c4abd26ff4e2995d92e0c772c765eda4038c`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 00:40:17 GMT
ADD file:d19bcd45d866b0d48dac33521c067bfbc08e3a101f90daebd092f75f282f6aff in / 
# Tue, 13 Feb 2024 00:40:21 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 07:27:22 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:28:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 07:31:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:947f8d1be7548afd5382ff5b1b5c220ae7893fa7f2c8f135cf8967ae1d5d8b04`  
		Last Modified: Tue, 13 Feb 2024 00:45:58 GMT  
		Size: 56.2 MB (56237347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81019b4261c2b7655008e5d128bbae18fd5c794c1676de082ef06c6e9d52b2f8`  
		Last Modified: Tue, 13 Feb 2024 07:38:36 GMT  
		Size: 26.3 MB (26259832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a5c8875e799e5e279fbdd05c6f1210fc9492749ce7709449def06189f5a739`  
		Last Modified: Tue, 13 Feb 2024 07:38:56 GMT  
		Size: 72.0 MB (71962170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bfa143fea443b5fbf9767fb081bf4a51c014002c74db280206fed9c76c7a2e6`  
		Last Modified: Tue, 13 Feb 2024 07:39:45 GMT  
		Size: 263.4 MB (263404095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:6c3d3c28d0798409f79e2c12e7c382fbe02438e2d872122f26d81e0408c6928f
```

-	Docker Version: 20.10.27
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **439.7 MB (439705173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8c08ee24ef8e58044f17bd2ec9d1260ab56f2bf9a2bd429dc2c0c8b417ed3f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Mar 2024 01:08:51 GMT
ADD file:ad62fb7e744226b84b9b87b22c6b1e797cb2a179f4f2c7295e0db14b95dcd84a in / 
# Tue, 12 Mar 2024 01:08:54 GMT
CMD ["bash"]
# Tue, 12 Mar 2024 01:30:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:32:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 12 Mar 2024 01:40:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:9c2efbfef38bc6f28418aabddc7ba24be7bed3ebbd2673ebc8db7533e9ae8c47`  
		Last Modified: Tue, 12 Mar 2024 01:11:24 GMT  
		Size: 49.7 MB (49682014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ab338dc4eeec296303efc67a955dedb7028ccf69f05896a788076dbc0a4108`  
		Last Modified: Tue, 12 Mar 2024 01:41:00 GMT  
		Size: 24.7 MB (24700091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca4553b75aacf6fefe0df7808ade0293c53b5a2b5926e00353a53712d08926`  
		Last Modified: Tue, 12 Mar 2024 01:42:04 GMT  
		Size: 66.6 MB (66645885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b421251d69b0b51ecca7046816c9f4249e4ac2e888c4d98bd3392fac2df2f8`  
		Last Modified: Tue, 12 Mar 2024 01:47:28 GMT  
		Size: 298.7 MB (298677183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:unstable` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:cbcf2b8c203819dcee64abf3e7c40fe72103115355dc0546c993a533fc14fe44
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.3 MB (385275888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91997c3e812b362628e372aa2d09a9a6cf7ff77aa137b4fcba2a62a8754bf29f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 13 Feb 2024 01:11:12 GMT
ADD file:4bc7c850cbec49616034f8ea4f54dd700feae8731e30f527142a4ae20f2089d9 in / 
# Tue, 13 Feb 2024 01:11:15 GMT
CMD ["bash"]
# Tue, 13 Feb 2024 02:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:33:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean
# Tue, 13 Feb 2024 02:35:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean
```

-	Layers:
	-	`sha256:463755eaddfb5b742f8a2a82a7c2ebcfcdcdbcfcad5bc7a79a96f0c7ea3c590a`  
		Last Modified: Tue, 13 Feb 2024 01:31:31 GMT  
		Size: 51.7 MB (51742366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83cc53fd314acb7fb481a8eae3a329f16695193f59a9f56c9e4806de6b5cf329`  
		Last Modified: Tue, 13 Feb 2024 02:59:42 GMT  
		Size: 25.3 MB (25307440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607d71e89930040fcd5c9bab43bc590b577afe0564c16033af772417a01da471`  
		Last Modified: Tue, 13 Feb 2024 02:59:57 GMT  
		Size: 67.6 MB (67555116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e4950bfd2260fcacae5cb79b071be191ad22b275987a43ed9ab875aea6929a3`  
		Last Modified: Tue, 13 Feb 2024 03:00:36 GMT  
		Size: 240.7 MB (240670966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
