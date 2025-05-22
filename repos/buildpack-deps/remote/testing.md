## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:10f06ac9033f0655d3b070a6f2b68dc2979d50b7c91820fc6ed765153ee08468
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `buildpack-deps:testing` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:a60d63d456d4a37cd7c583875120f83c8d9865b9e1fd9a07bdf913fe0fea59ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.1 MB (378144406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d06640b2398cceb5499da6e689b2d90d3ca992dcaa49286c473ebdd4ddc79ac`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:b8364400c35b20e530ea76455b7a73bf615b17d9d6734e0c2539034d9fe0bed1`  
		Last Modified: Wed, 21 May 2025 22:28:00 GMT  
		Size: 49.2 MB (49246908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:073c3e094f775042a2296ed99ca159904c7ae19127cddd6dc0e02dfeff3ac66b`  
		Last Modified: Wed, 21 May 2025 23:20:52 GMT  
		Size: 25.6 MB (25583751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:796d3fae0f8d1c689d461da616de1a85e5ade1f7c61c5496c0c3b6b1bf6e722d`  
		Last Modified: Wed, 21 May 2025 23:38:03 GMT  
		Size: 67.6 MB (67637573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c62c053c3fe409c6202007ee9fe27860b42e831015c1fa52afc3a49e5110c1c`  
		Last Modified: Thu, 22 May 2025 00:13:05 GMT  
		Size: 235.7 MB (235676174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:216742157fff3aa4b4fed0aee18a72806f6b0e7be312c33840482c7f21ababbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16925615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74914abd44a5b9fbccafe6c6046b4504c53c7215caafefd55e6ac400a9a6d32`

```dockerfile
```

-	Layers:
	-	`sha256:d9e74b77f930f3277ffe9ddd8fd1304238528c723b8ee3ff1b7dbdda98bf029e`  
		Last Modified: Thu, 22 May 2025 00:13:00 GMT  
		Size: 16.9 MB (16915422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6762793613d242035ac02a2fa94e1858932d8357ab659647dd883dcabe9582c8`  
		Last Modified: Thu, 22 May 2025 00:12:59 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:e1af8d0f2be9426a0efc9d89bb1b3d0718c8082e5da6a0a6b200a25838aade62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342412589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad8539e092af8ac5a336aa112210c03f0142cedf9803246333455b8051f48cc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:15a0811b2608aa97b4e0811060ffea557de20e605122f0c38825f47469947704`  
		Last Modified: Mon, 28 Apr 2025 21:10:19 GMT  
		Size: 47.4 MB (47428611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b453de73db44edcda29182f13881db794c74b0f335096c735f5f88ffb61b994b`  
		Last Modified: Tue, 29 Apr 2025 06:01:51 GMT  
		Size: 24.5 MB (24474447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e19d072d3ad687af2af376c719bde109abef8c58cb05b32faf7ed3c425f5c84`  
		Last Modified: Tue, 29 Apr 2025 06:25:46 GMT  
		Size: 65.0 MB (64956846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72658d0155477ee6c66076c216b2d65e09afe1dbd6b141146037067d358bae5f`  
		Last Modified: Tue, 29 Apr 2025 07:12:40 GMT  
		Size: 205.6 MB (205552685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:185727ddb28f05a87aeafe67e90938ebc153545b3d3f67122d00682233c66fa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16626029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1baaabc9096bab365d03cb960a7cb0866d546d92fd9e506ad0c44ee5256c5fa`

```dockerfile
```

-	Layers:
	-	`sha256:e7d08eef8fd2e33c028ec2988b485b80cde9e1e40e2d24a93bbd6ad6fb9c3d4d`  
		Last Modified: Tue, 29 Apr 2025 07:12:35 GMT  
		Size: 16.6 MB (16615776 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca43c275badfc699ab31134ef4e55915d96f3d3f972f31f94cd7bd5ee823f1a`  
		Last Modified: Tue, 29 Apr 2025 07:12:35 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:c23a2bb31a269dbe24d20dc6935b0355f8e847c9c6b95c5f6df43189bbbdb01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.0 MB (325028871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ce8000046eb809f65b4b5ea2c9af80fbd5a5b312fd04688c453e650b8ab934`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:d877c043ab6ec52d6d4eaeab7dea355ef83893e584af00854b55ca611a3bcd99`  
		Last Modified: Mon, 28 Apr 2025 21:19:08 GMT  
		Size: 45.7 MB (45683821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:785865296d03ccb31a01d56e5adab53e0c986bcfdc0c9920d48d9b1d2d93eda8`  
		Last Modified: Tue, 29 Apr 2025 03:39:17 GMT  
		Size: 23.7 MB (23738374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e434d6c9a7d808d76e24daf0efac32e9c61b3a7b5f489a41bb49c2842179975`  
		Last Modified: Tue, 29 Apr 2025 13:26:13 GMT  
		Size: 62.5 MB (62483288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a229b5dea998e582bd4346f3fc6ead844822af286c47eafa21b06a96a2790571`  
		Last Modified: Tue, 29 Apr 2025 16:50:57 GMT  
		Size: 193.1 MB (193123388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9602df1b217f8707699dc936056567d4ce4aac38dfb30e15a6ef5cdcf890c811
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16625600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0498ae60a98de9b8c76c32b27b9fb83efacf5b97230f66ccf576161dffddfb68`

```dockerfile
```

-	Layers:
	-	`sha256:912d8ff70f0a44932fa6873db4e7e73f796fb5f943c772a04dd6179f4f77c531`  
		Last Modified: Tue, 29 Apr 2025 16:50:53 GMT  
		Size: 16.6 MB (16615347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bcf0a2a0e0a18d6edb823bdf1fafa18791746dbe4d32d7090f6693d16817127`  
		Last Modified: Tue, 29 Apr 2025 16:50:52 GMT  
		Size: 10.3 KB (10253 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:e5418820cfc1f9f47263e6ed5c3252583405c11b8f492d282861cec8c2f13dcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.4 MB (368370200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3e52f77d5f2aaf90905b296505611235700b2e9f6590b62afb2c361b08f1bc`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:288a1cecb0ea762427d39b072c1ca965d193e927e04da652f7b21eb12e9b2acd`  
		Last Modified: Mon, 28 Apr 2025 21:23:23 GMT  
		Size: 49.6 MB (49624118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6faa4d9377738e3cc52e5d3cadb55bd77d367fb6439d9d14741079130dc9e4e`  
		Last Modified: Tue, 29 Apr 2025 01:48:13 GMT  
		Size: 25.1 MB (25116968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d10b7fbeb9c563c295c91ba384fe4305118a0d8b88117bbf9e5d4d3c3f9787`  
		Last Modified: Tue, 29 Apr 2025 18:39:19 GMT  
		Size: 67.3 MB (67265970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ca0e913b250f409d6a54f6914fd0c93b11ed99929e3646882fc10ecfb26a986`  
		Last Modified: Wed, 30 Apr 2025 02:22:28 GMT  
		Size: 226.4 MB (226363144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:032c3efe83b65d3a8ad46f6157cbfa3d4ea47b4008582c63b5174bb12e586730
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16940230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:def78b23b250803645119bd3baeda9488bc9c02cd9f20a0915434fa2f61297a6`

```dockerfile
```

-	Layers:
	-	`sha256:81ab09460aefcba9bc5ef34b79095b7da06c335a69aab2815b01f34c857bb77e`  
		Last Modified: Wed, 30 Apr 2025 02:22:23 GMT  
		Size: 16.9 MB (16929957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4dd988308c21386b5230dc6a720c2596011fe0e032c89ab2f88e608aee50117b`  
		Last Modified: Wed, 30 Apr 2025 02:22:22 GMT  
		Size: 10.3 KB (10273 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:81ac221c0018e9238ccc7dd0053c5bfa0b810ba6b31430a0c28c3d2d6d0f0872
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.9 MB (386945503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b0b1273ff285e91764a99f0768eb52cce21267283a7d102d493cc48da7ab8a`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1747699200'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:7e1acd19dab9f7ab62b7570b85e71035e78cd9d9b9bff975df4b0a635578c7be`  
		Last Modified: Wed, 21 May 2025 22:28:11 GMT  
		Size: 50.8 MB (50761280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24ada90c6b3f67e8ac11f8d9700e1fbeb5f64ed848c2ef5d89e89c3d1161d7e`  
		Last Modified: Wed, 21 May 2025 23:19:58 GMT  
		Size: 26.7 MB (26745816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53475a03e00d0d9a396cb70f6edb89c6daaba7c95e28d935ced8a0100b7b7bc9`  
		Last Modified: Wed, 21 May 2025 23:38:03 GMT  
		Size: 69.7 MB (69655812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35dd214bed674db855a1bb7bd96a9a5f465ab885f73c5b07af7d81223142c462`  
		Last Modified: Thu, 22 May 2025 00:13:25 GMT  
		Size: 239.8 MB (239782595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c63bb64e4cb115b6c93c841f6f1a835e5d506e96e81f03f9ecd17c1711d164ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.9 MB (16895208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45019c9c9fa7ddf7c74e5e147c643464a872778e09a3b28c1c6ae7476ae5ba73`

```dockerfile
```

-	Layers:
	-	`sha256:14698a6f978b4bcb513060673fef5af05c56c3ebd430451f51cba68f47e98f49`  
		Last Modified: Thu, 22 May 2025 00:13:20 GMT  
		Size: 16.9 MB (16885037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22ae96c519f9eb947e3ae21c04dd12295f80d2daeafc1441676cdb266f98fbbd`  
		Last Modified: Thu, 22 May 2025 00:13:19 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eac77c9892db54b705c1ce2fddeee6779ac0ba9b58448167745361bd9f6a1eee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384205034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6669d9b184ce01a46125c23073e51f89500c0088641c1d7eb64156ffbb19b566`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:03ebb30bb37cd398ea8ab1a268c301664089cf5a54d23466e4338782afb5f9cf`  
		Last Modified: Mon, 28 Apr 2025 21:25:28 GMT  
		Size: 53.1 MB (53072552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed88abda34c2c7766794d61fd8b43cac1ab4eeadc9f85398417820583a09e36d`  
		Last Modified: Tue, 29 Apr 2025 07:48:18 GMT  
		Size: 27.1 MB (27143577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fa77ab766e4eed4e829b6e08390c6a1dc6b2350ee6134f9e56b8061b308247`  
		Last Modified: Tue, 29 Apr 2025 08:30:35 GMT  
		Size: 72.5 MB (72536214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548d300d0e0a443859c9d7b03f2fb73f0f13dd6195fcec9f5c4253b86e2389e2`  
		Last Modified: Tue, 29 Apr 2025 09:14:32 GMT  
		Size: 231.5 MB (231452691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f7088f0c414e7d2616fcc5fd03fd38b946c914c5505c8f62aead72caa3de4a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.8 MB (16847298 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4559f7375b27f62fa96225a7f9387a170b3cec1dc7a15388578a62f7083f1bd3`

```dockerfile
```

-	Layers:
	-	`sha256:9cf7611c957561a1a046c1473cade9fdac913e91ad743ae01a90dd9e8057ee9b`  
		Last Modified: Tue, 29 Apr 2025 09:14:23 GMT  
		Size: 16.8 MB (16837073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c6275dee09a0f14bd56a0acdb4b5fcd784cc55090c50bcd9c0ec95c658872db`  
		Last Modified: Tue, 29 Apr 2025 09:14:22 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:58e4e101049bc6378d22097d6534c57212e59860d68e42cdd2e636a12a70e040
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **463.6 MB (463557754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f265e671e3ab912bc7bb2abc58c83da024ea52e3e8b5eb8422e5df4a451069d4`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:3e87a3ef7201dacec1e06fe511cdfaa924c5bf89f4f022c082b59ff14eb11b6f`  
		Last Modified: Mon, 28 Apr 2025 21:16:24 GMT  
		Size: 47.7 MB (47740349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b410971d43e4d351db365aaa47795c79f72faf119ac6c217623f17c39d9714c9`  
		Last Modified: Mon, 28 Apr 2025 21:56:29 GMT  
		Size: 25.1 MB (25062721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c741c2f68d1e90ffcc6854d741c8a67c48cfcbc304e660bf2ebfbaa12e1eb21`  
		Last Modified: Tue, 20 May 2025 21:41:48 GMT  
		Size: 66.0 MB (66046518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81214ad5a528ca7e8e97354f90a67c7b67e6d5f2e249b3028ac62b632757bba5`  
		Last Modified: Tue, 20 May 2025 22:30:19 GMT  
		Size: 324.7 MB (324708166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2f260c4c25580acc3b81ff92b4b8a1205bbc2bbda83356635b0378b5bdb9e0a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.0 MB (16982009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27f281870ac5857eb54446e21655ace1853d55ad5b462d90c22ffe100238b958`

```dockerfile
```

-	Layers:
	-	`sha256:56fae0efdd453258a19a8fe9a835e376a82159a4dd3e8cab3619d2912092cf2b`  
		Last Modified: Tue, 20 May 2025 22:29:37 GMT  
		Size: 17.0 MB (16971784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49f40f7430d114d95b40e2a2e05bf9b01e49bfd247d4d2c0f278847cb59bdcd4`  
		Last Modified: Tue, 20 May 2025 22:29:35 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:f6854d82d77e914b12de74676853f6277183f304acd645ea0081230f6cc46e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351239514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8994ed8a97ada24df9dc0e0d58ba50a5af2a8b618484e74912d69d385db68016`
-	Default Command: `["bash"]`

```dockerfile
# Wed, 31 Jan 2024 23:01:46 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1745798400'
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Wed, 31 Jan 2024 23:01:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e1ec3b1570f7d822c5a6aa013529484429ad99bde8495d827b56c3603992fd3c`  
		Last Modified: Mon, 28 Apr 2025 21:11:06 GMT  
		Size: 49.3 MB (49316646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc2dfe09dce90ef60478379ac93bf4db4640c14411109c4ddd5060ffa49cdfa1`  
		Last Modified: Tue, 29 Apr 2025 00:02:32 GMT  
		Size: 26.9 MB (26932582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683df7242435f0ea9a0034ffcad35c09ebe0ed400dc39d5de0e749bf3bf141b1`  
		Last Modified: Tue, 29 Apr 2025 03:00:34 GMT  
		Size: 68.3 MB (68302009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:195e7c0cdf1713513bf973e01f68c8257ca3e8331172aebc82594e488fa6c4f4`  
		Last Modified: Tue, 29 Apr 2025 05:37:42 GMT  
		Size: 206.7 MB (206688277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:98b0859ce3f551b889c4078ac3e5e24428f5bb60edfa192c866f5063a84e8301
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16641018 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7851ee9beefc063fbd046683349a8276da0dbdf84c1c8249095f7f9be56733cb`

```dockerfile
```

-	Layers:
	-	`sha256:c9d77e9d8706a2a507f5eb0b3501dd4c4646c58c31b661b14fec7e02afb37610`  
		Last Modified: Tue, 29 Apr 2025 05:37:39 GMT  
		Size: 16.6 MB (16630825 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23cdf14adabd0769365b999a4997a4ccd829c0c98f97de700b04f1d8713a835f`  
		Last Modified: Tue, 29 Apr 2025 05:37:38 GMT  
		Size: 10.2 KB (10193 bytes)  
		MIME: application/vnd.in-toto+json
