## `buildpack-deps:sid`

```console
$ docker pull buildpack-deps@sha256:ee7e31c00732ac7fb067005d8f8874582d7b34e98b4fcdb5a3c680dfd7a31ecb
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

### `buildpack-deps:sid` - linux; amd64

```console
$ docker pull buildpack-deps@sha256:deed56587c0bb0352efb927083858c19e40177a5aa1fc5dae50f6dc0d11ee793
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.1 MB (349060495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c155fb40fab38ba5d51ef93a080913d765d592dbd302cb82fe895ce79712bb`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:21:12 GMT
ADD file:3b942ada2dbba1c073e568411a383d6ab987c117af5bbb011afd46549d64c4dc in / 
# Tue, 23 May 2023 01:21:12 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:52:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:53:16 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:54:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:8285c3e1284db51d7096ff9c9434e138a00153495c655a040787b10e562b7515`  
		Last Modified: Tue, 23 May 2023 01:25:36 GMT  
		Size: 49.3 MB (49289184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20c93962a936c4e623abcd5c132acd83a550b41b475220f5ba03708dd030b1c0`  
		Last Modified: Tue, 23 May 2023 01:58:03 GMT  
		Size: 24.3 MB (24276999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f584564987f0be0d812aecff1df91b59183f5667eadff38eabade6484098b`  
		Last Modified: Tue, 23 May 2023 01:58:20 GMT  
		Size: 64.5 MB (64516175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7127f99bf6a25565afbcdcb00c7bd92c950f01c3c2fa4b2358fcfc5932476c57`  
		Last Modified: Tue, 23 May 2023 01:58:53 GMT  
		Size: 211.0 MB (210978137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v5

```console
$ docker pull buildpack-deps@sha256:d5ef570688e4f0c744103ca53619ec64eee27efd1f62001d9f82e4789453c575
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.5 MB (316547689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cc039e7d985e709264f02129c6b6bb1ba748f7a391ae26c6da11f79e7f75d34`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:48:49 GMT
ADD file:bbdd13db0e090d7d928a2beba57e3c1340342d05e5c15f7b7377c9791a5cb4ba in / 
# Tue, 23 May 2023 00:48:50 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:18:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:19:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:20:11 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d14a321d144fc48aa438b2364b0f1a5667979322ef9cada9309bca48584a11a1`  
		Last Modified: Tue, 23 May 2023 00:51:36 GMT  
		Size: 47.2 MB (47154613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af911895fe3f6120ef979a3b5dbd9bac4de6b4d900e6ad8ddd6b28ccb19a7746`  
		Last Modified: Tue, 23 May 2023 01:22:48 GMT  
		Size: 23.0 MB (22951581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc480ad84aad81f48b8427943b9e4cb119ca2f0562152d578d98f45ff47a69b`  
		Last Modified: Tue, 23 May 2023 01:23:06 GMT  
		Size: 62.1 MB (62144202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c909aa5b0b4faab46fd295d7d46adae7941a4443bd61771ee5a16f726e7e542d`  
		Last Modified: Tue, 23 May 2023 01:23:41 GMT  
		Size: 184.3 MB (184297293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:54e96cc0b444702a2e08116f00f2c5b58d704f39d7d063ba949966d99c3e53ad
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **302.9 MB (302905039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c4d82fce231bab872e199f0c47c7398de32aac9c7bf10625868625572586fe2`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 02 May 2023 23:48:42 GMT
ADD file:17739fc730ad8febc64f53eec61cbf10f8d2c5184cfda5466e89ab423a88f9d6 in / 
# Tue, 02 May 2023 23:48:42 GMT
CMD ["bash"]
# Wed, 17 May 2023 00:02:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:02:37 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 17 May 2023 00:03:24 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:b0b827c534260a55126ac3b18c14ea9160a3a3a03448b5c2b4462f9f3f4cf0ab`  
		Last Modified: Tue, 02 May 2023 23:53:05 GMT  
		Size: 45.0 MB (44988077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858686fb647755cfaf9d97846212a8b1056f291d77f962bb8bf7be5d16a5ff60`  
		Last Modified: Wed, 17 May 2023 00:24:35 GMT  
		Size: 23.2 MB (23219225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16fdb017446b11706119bca2906a6b8fa79ccf636d08457981e54be450413bf`  
		Last Modified: Wed, 17 May 2023 00:24:55 GMT  
		Size: 59.8 MB (59773847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05930ecf1b48b63067b8734906c94169606839e7d6c40620dd661cdf4f03308a`  
		Last Modified: Wed, 17 May 2023 00:25:28 GMT  
		Size: 174.9 MB (174923890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:b31b6997b3b48d8c20a60d3d9f2869b42b603c3a547aabe99f85c68278038f4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.0 MB (340030095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf6168ba9d8d3738c05b23189ec0695edf6c133e5ff69b1aa435355584df0656`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:48 GMT
ADD file:4608b82b211b6814e5bf372be706a6c01bd7a2a4841b59ac5430ec3a3f94468d in / 
# Tue, 23 May 2023 00:43:49 GMT
CMD ["bash"]
# Tue, 23 May 2023 05:59:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 05:59:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 06:00:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:5842d200e3f7df637a96b64f14e82ccb2c66e201137165f2d91447fbd3248a8c`  
		Last Modified: Tue, 23 May 2023 00:47:31 GMT  
		Size: 49.3 MB (49336298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f8c760dbeccae06cc6b46a82bd8c7d79890fb31a8237d0ba2b23c16b2b47fba`  
		Last Modified: Tue, 23 May 2023 06:04:42 GMT  
		Size: 23.8 MB (23813069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6085f2f6a378ccf03bc2e19864b5cb626f6bb97c0548e81dfe6c75f730b24245`  
		Last Modified: Tue, 23 May 2023 06:04:58 GMT  
		Size: 64.5 MB (64499310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ff2b84fcbd84d3469d2b8d95b1e565307b917710bdaffafc55a1a6c9aa9b02`  
		Last Modified: Tue, 23 May 2023 06:05:25 GMT  
		Size: 202.4 MB (202381418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; 386

```console
$ docker pull buildpack-deps@sha256:bfb948a2cd1a85ea856704fa7e2f65860cc55c0c987de9c33f3b48af815250c0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.7 MB (351665710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d8e87a5cf2c9eaf7e804ebe93e6d03f016c49025cadcdd134a231d6df17700`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:40:47 GMT
ADD file:33dd3eb2725f92170606ce015e99cc9496d244630b3f4844cb8f3f61b16e2eb0 in / 
# Tue, 23 May 2023 00:40:48 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:01:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:02:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:03:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:1034171b4bde64cf8e4ff854704a3bf68000eddcceb63b481197082dced785ba`  
		Last Modified: Tue, 23 May 2023 00:46:09 GMT  
		Size: 50.3 MB (50311497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0773461f28d3828f3df4474bf07fd4bc2d3cdec7f41c65f1253678f4a5f861b9`  
		Last Modified: Tue, 23 May 2023 02:07:38 GMT  
		Size: 25.1 MB (25112113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f3b130ddfdd33ce29355bf1322b63f47960cc73b9e64789abc64c7954273d2`  
		Last Modified: Tue, 23 May 2023 02:07:59 GMT  
		Size: 66.3 MB (66343136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebea0fc9963d0bf015c9ee164b3055359aa0813a89a3573a104341b78c83243`  
		Last Modified: Tue, 23 May 2023 02:08:44 GMT  
		Size: 209.9 MB (209898964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; mips64le

```console
$ docker pull buildpack-deps@sha256:48ef83aa4d45da44977b10e195787c496431410357a9dc4bd4e14de3423548e1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **326.2 MB (326151829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0343c299015129f953d61681b6cf9b0d7cc1d4df0732f160be809403e42715`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:11:03 GMT
ADD file:4747b72418fe8be7c83a33927d22b74c9169c9f02959e41f61d71d739fd30ff8 in / 
# Tue, 23 May 2023 01:11:08 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:58:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:00:31 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:06:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:0f1da758a33cea391a9b76cbdcea2cd41c87b5a2c179c4c1f3d65a456c65d8e1`  
		Last Modified: Tue, 23 May 2023 01:20:05 GMT  
		Size: 49.3 MB (49293333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ebbc59228088cdeea0edefdf4596c78cc8f25b00177cd12202cf4a879b33945`  
		Last Modified: Tue, 23 May 2023 02:13:15 GMT  
		Size: 23.9 MB (23868941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2051f379a7704fbd90dac1820d91a3165e19ecd15d8720c7e0af0762d9ecd78`  
		Last Modified: Tue, 23 May 2023 02:14:04 GMT  
		Size: 63.4 MB (63426661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7be9d0fbbb8bb1d9c8f1ea42ef13479c785cc3da542fb3253a52d9dfeef23d`  
		Last Modified: Tue, 23 May 2023 02:16:06 GMT  
		Size: 189.6 MB (189562894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:4180f83bee8862f62e34b242a6c4676f055a0f07f919efc59b95ea783f28b947
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.2 MB (363209518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc7746abe0792125c6d07981a17bf7eddf421fc2d3b4d85176177bb5470447ee`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:17:52 GMT
ADD file:cffada1d28fb1dc246127e193bd218b3c76450667fe4cd380f04a5caf5571be9 in / 
# Tue, 23 May 2023 01:17:55 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:55:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:55:46 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:57:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:d914d1b8acfde6dc74b2fb48f95f7aedafbe4e4ad3b6ea21aa9db007eee47739`  
		Last Modified: Tue, 23 May 2023 01:22:29 GMT  
		Size: 53.3 MB (53302061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfd02567bd019328b094640438b56aa8ec096d625eb4dd7646bad29dc33d703`  
		Last Modified: Tue, 23 May 2023 02:02:41 GMT  
		Size: 25.9 MB (25928691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37bffe3818ac84f2da95782d45c9d0ec1ac2686d474eef4dd224cd8a76dca7a`  
		Last Modified: Tue, 23 May 2023 02:03:23 GMT  
		Size: 70.0 MB (69960094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50fadd7c17d6fa307406898325a872ede82ab292ef5fa12394c40c221c7eb9c3`  
		Last Modified: Tue, 23 May 2023 02:04:21 GMT  
		Size: 214.0 MB (214018672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:564fd56a3df6adb28650896f1b9681ef21ccfe79d1a815ab438385e8cd0739f3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **362.6 MB (362620482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:269a03d1956ba95d3d2886739592023ec4964e52e95e5d0434cc4afdaa1746f9`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 01:09:11 GMT
ADD file:20221b6f94aa48c9890226bf3be037d4b2c2cb20a076225236ca9d2c09efcbd4 in / 
# Tue, 23 May 2023 01:09:13 GMT
CMD ["bash"]
# Tue, 23 May 2023 01:31:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:34:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 01:41:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:04b827a08c39becba5f6c479b23a265f1f501c5d3aef76e037fa30157864daaf`  
		Last Modified: Tue, 23 May 2023 01:12:26 GMT  
		Size: 45.5 MB (45503414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7efef68c40b0d23d116a73ed6b2156ae42fb93e63547bebff3d6febc2bbbea30`  
		Last Modified: Tue, 23 May 2023 01:42:27 GMT  
		Size: 22.5 MB (22487151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b058e1f937b69e6050ad30d3ef4e1094300d70d5175e07c16d50c7efd62c36c8`  
		Last Modified: Tue, 23 May 2023 01:43:46 GMT  
		Size: 60.0 MB (59962968 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9518b6188b1fbe610cedf16e43133a38704a9dea99007ed94481fa7723f6ff0e`  
		Last Modified: Tue, 23 May 2023 01:49:21 GMT  
		Size: 234.7 MB (234666949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `buildpack-deps:sid` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:1bbafd5378397c3d7f47f2e041f2819246b08b6702b86811c4784aa230ad45ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.6 MB (318590113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83de6025398ecbe1b08015f53e1a1c50da9f422fb2d44a672de0159a898f550f`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 23 May 2023 00:43:02 GMT
ADD file:7a71212c59dd3640d3ec2c6d4fd4df4a864f77e634571c1e200a6f7877a02cb2 in / 
# Tue, 23 May 2023 00:43:06 GMT
CMD ["bash"]
# Tue, 23 May 2023 02:34:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:35:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 02:35:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
```

-	Layers:
	-	`sha256:021a3707435b37ce556f1886fb9417a47cbfa836555f680d70cffb85f96a6eec`  
		Last Modified: Tue, 23 May 2023 00:45:58 GMT  
		Size: 47.7 MB (47664615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6242508e16648c81ff21ed8251d1dfbddaed438084bbcd6c7baf639349cf592b`  
		Last Modified: Tue, 23 May 2023 02:39:32 GMT  
		Size: 24.3 MB (24275724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:081327490bfb5677aff76324903d283fb120712a9f911ed52f6d4be91df47e0d`  
		Last Modified: Tue, 23 May 2023 02:39:46 GMT  
		Size: 63.6 MB (63609047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46eacf0032042bf63c931197525f86388a95920b01b4b1a56fb4cf0331d60ba`  
		Last Modified: Tue, 23 May 2023 02:40:13 GMT  
		Size: 183.0 MB (183040727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
