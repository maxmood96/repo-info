## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:909daf2a4e35271d8ed1422500abe094af6627f4cd0ea1af6411b9c88febeed4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
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
$ docker pull buildpack-deps@sha256:9b5784205a1c8fac24de4789208a7bbe33da50ca974dd15e9c6fad0aacb4a7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.6 MB (343627095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709160774b3793ca293855123892313f45342efdbeb707ec1ac3b023e1beb3e9`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:28:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 07:42:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:186ca733686ffcaca03fdc512b51c9498f39b93235775cf08154b1ff0b143901`  
		Last Modified: Tue, 04 Nov 2025 00:12:56 GMT  
		Size: 48.5 MB (48481364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a5d3d8f7f036c72a68099d4e5f2152d5ebac52f060fec3d2009131f12e2ee6`  
		Last Modified: Tue, 04 Nov 2025 00:28:30 GMT  
		Size: 27.2 MB (27194469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5fa7289d9c2385034e2bef8c2d8440132ab102f8472020015b0d26d75a15788`  
		Last Modified: Tue, 04 Nov 2025 04:14:50 GMT  
		Size: 68.4 MB (68443347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:762ed0b206dcf709064acc85efd51762b342b9c08ca8b60ffa9148900c21a4e6`  
		Last Modified: Tue, 04 Nov 2025 14:29:12 GMT  
		Size: 199.5 MB (199507915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:c53c1e86bbcc881e6c77f5dc4dc943fc8bfcca5b52224df5953f809ee7f00919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16262983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c62d7fa1601a05b4cb41f8472b97382a8cdf4793aa84be4cf034b1e6e84a20`

```dockerfile
```

-	Layers:
	-	`sha256:6959321bff2b1485f8fed332cfb657c928e35d334050ffdfe89f88608d1f386a`  
		Last Modified: Tue, 04 Nov 2025 11:21:16 GMT  
		Size: 16.3 MB (16252838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f81106108e1a1b4cfdbe2fe0181b4178c8e0584d0727847298b9e86bf757409`  
		Last Modified: Tue, 04 Nov 2025 11:21:17 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:383590cf22929c20963321f9ab3e1bd8a867022dd3805f74bb7a1540ea98bf0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291503896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8234a82c96fafc1e7cc486e2945e430e4a9ff0b3eca0af7256e55bced457c16a`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 00:39:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:18:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:22:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:1a3f9ca9ddd6f8d1ee0ddc59ad7ed9255992d14a1e28dcd6f3a00557f6d1c188`  
		Last Modified: Tue, 04 Nov 2025 00:12:42 GMT  
		Size: 45.0 MB (44987650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09e3d8e8af8f367c36a3d87550dc3267b3259f0235ff915d84427b289652d3b6`  
		Last Modified: Tue, 04 Nov 2025 00:40:06 GMT  
		Size: 24.9 MB (24928009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:599c4ef410d822d8ddb9cf8db762dfae87e2a2463c48ad3be3776aa8c3a8f9b9`  
		Last Modified: Tue, 04 Nov 2025 02:19:03 GMT  
		Size: 63.3 MB (63303162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b45bc0dc9ac268b82d76002c7a41addd9876759082bf5b58be54659c6b2439`  
		Last Modified: Tue, 04 Nov 2025 14:29:03 GMT  
		Size: 158.3 MB (158285075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:9f5fa42729d0fb8048f78e9f8d0ec1367a0572c2b896d4bf42aced843f7e6e27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16019995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e426f907611760e7276295445702dc4830ee6d0ba6db5568d1306e615a34bf1d`

```dockerfile
```

-	Layers:
	-	`sha256:8e4ee2a33dc1a8fa1cee7a2a76d621ab8a1ea6ddc46337ccd2b9c1be0797f2ad`  
		Last Modified: Tue, 04 Nov 2025 11:21:33 GMT  
		Size: 16.0 MB (16009786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df3d1e1ef6b0700a11c6fe7e706fd75e0fad122e08c166b0970b767d18477eb2`  
		Last Modified: Tue, 04 Nov 2025 11:21:34 GMT  
		Size: 10.2 KB (10209 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; arm64 variant v8

```console
$ docker pull buildpack-deps@sha256:ed0e5d0bedc4240c4d7f45ee93fcb248b27eb4a7b0ed51b5b95279330adf0cbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **332.5 MB (332500956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ec02540565dd8b2f2751d144dd582d72f3a730db04fcfb6030cf1b683c8b465`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:29:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:20:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:15:18 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:52d2706ca00f3431b3c37b306b3eb6cc4989781e31180bfdf93c4dd4108e1e3c`  
		Last Modified: Tue, 04 Nov 2025 00:13:40 GMT  
		Size: 48.6 MB (48583638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34b1dc65111912cace804df53935fa607cbdf8cea0c2d3c79b97f575ff17a44e`  
		Last Modified: Tue, 04 Nov 2025 01:29:59 GMT  
		Size: 26.5 MB (26459050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6ac97762f880e49106968b7b0e7e59e47c19263e8ccb0c88ea1fb872b49fafa`  
		Last Modified: Tue, 04 Nov 2025 02:20:53 GMT  
		Size: 68.1 MB (68111513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f16742389ff3e8eaf21b775052c6ba3efede0928c772e8693fab6fc0e4b83b1c`  
		Last Modified: Tue, 04 Nov 2025 14:28:54 GMT  
		Size: 189.3 MB (189346755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2f335e1addf4c6a0d6e7a3cf129ec1d7e664e385d1016041359e55944298c858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16337612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0a13a829a59ae0e856ddbb070031799badf50904dbef78e17d49a35bf76d711`

```dockerfile
```

-	Layers:
	-	`sha256:9b13edf34e1291f0cde5548225af276179d47c9448e7c3d64e162dad7dc0f5fb`  
		Last Modified: Tue, 04 Nov 2025 14:28:39 GMT  
		Size: 16.3 MB (16327387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66784ed358ab9a147898a702f4e9a755972fb2ff6f7ec024a89e1dafbd142a94`  
		Last Modified: Tue, 04 Nov 2025 14:28:37 GMT  
		Size: 10.2 KB (10225 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; 386

```console
$ docker pull buildpack-deps@sha256:478f4a6d6b668953892dd422e4fda2ba43237a621a981ce5826b30a2efd0855d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.1 MB (351124932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7452d9fcdd4b28745263c807e960ec12f5165805b8cd05d0e4949c1853096815`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 01:31:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:19:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 03:15:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:bd86ecb6d3ac97cad4df6e0aeedefdf1790afb18f99112bd09ea68844e318978`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 49.8 MB (49809500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e56f22c9a3cedb803ef4ecfe9678d058c62ff4867aa23b90c8aad3b86d75d98e`  
		Last Modified: Tue, 04 Nov 2025 01:31:56 GMT  
		Size: 28.4 MB (28432712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2426e6c2ac9755238716e16600b3257ad387583b1571f9758b22265e968a3cc9`  
		Last Modified: Tue, 04 Nov 2025 02:20:23 GMT  
		Size: 70.4 MB (70355653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7639643a328ac2fd107b8d3f9c31617749b8fa0f168ddc69d465486233d2eb6`  
		Last Modified: Tue, 04 Nov 2025 14:28:58 GMT  
		Size: 202.5 MB (202527067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:db33ce7861ece2457186270f322a360570f83b1255155154adcc3e4a16c69c11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16232740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ab61f606397e3e787e20815492bfccadb8d900ac0a4e1ed89046a9013c75e6e`

```dockerfile
```

-	Layers:
	-	`sha256:c8cfc7574c5832ccfa6f9a6b935a2d4397680244b6bdf0df5bdef4fecd1bed33`  
		Last Modified: Tue, 04 Nov 2025 14:28:36 GMT  
		Size: 16.2 MB (16222617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:319d0e46220464849997d05f8089917ec91868346122271e7f3ab4bf083ae614`  
		Last Modified: Tue, 04 Nov 2025 14:28:32 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:195e6d1c52ddfa3b13130d9b6655c3edbd51b567640951f4954badf0c26a7717
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.9 MB (347858796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60de0eee8f87d0ba6a9368bb9864c8968d959e902bf47f582350d4bf92a57224`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 06:26:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 15:58:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 20:43:17 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:9422d47ff8508a211c5181db20a5b72bab47758f9bcd0687b05752ead1b35a5a`  
		Last Modified: Tue, 04 Nov 2025 00:14:32 GMT  
		Size: 53.3 MB (53315240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11aed674c331384a39236b4b411559b275037202a43d78e434b1d5c25b1e6d72`  
		Last Modified: Tue, 04 Nov 2025 06:26:53 GMT  
		Size: 28.8 MB (28798376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb8defd21903bd4a9c5ce27e534598f52e2a1e6029872b40ca09576c2e165d5`  
		Last Modified: Tue, 04 Nov 2025 15:59:56 GMT  
		Size: 73.9 MB (73865276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea108f0bf025de0b233e391946942f6903fc348d3db37123cb910d4b293d8a17`  
		Last Modified: Wed, 05 Nov 2025 03:18:47 GMT  
		Size: 191.9 MB (191879904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:adb09955a03e564a8d2797f08f46c172be1412c68e4ff248ab90cc97b299cdf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.2 MB (16237163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff8c08a3ddaac7dcd06d41423a8264124e1136ee3e4c0c5784054040ff3ff72`

```dockerfile
```

-	Layers:
	-	`sha256:00561d131e31e53216d4d3a2b12bf5a329593b7e1bac25f754d7002a0e2bbe87`  
		Last Modified: Tue, 04 Nov 2025 23:20:30 GMT  
		Size: 16.2 MB (16226986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d2d81cb603218b2af0a65d269196520be8fab9cd42d9fa19dc9335e9f72d02e`  
		Last Modified: Tue, 04 Nov 2025 23:20:31 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:4115c41d34e472c2b5e6584f671b28e1607cba56fbe6738a7c77143499a698e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **445.5 MB (445494123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f82a7ad3d60a866c4af1bcda7ffa05ab82235ac312da790bc5c74f14969437b7`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1762202650'
# Wed, 05 Nov 2025 11:56:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Thu, 06 Nov 2025 07:24:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Sat, 08 Nov 2025 03:30:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:81afe9ed9d72ebbd06999820f64e36aa62bc978725062b4cc32efc39c6a99213`  
		Last Modified: Tue, 04 Nov 2025 00:13:41 GMT  
		Size: 46.8 MB (46791125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de80c58c6e8800ea08ee90fdc845007e21de17aea53e05a410b042fb2c91d58`  
		Last Modified: Wed, 05 Nov 2025 11:57:49 GMT  
		Size: 26.4 MB (26387683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba38582987e4915b52f0e092e29ae54ca12e102a825bf157a95190c5f836e50`  
		Last Modified: Thu, 06 Nov 2025 07:28:26 GMT  
		Size: 67.2 MB (67202784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4bbaa85d1c7d501fec9d34d9b54416c39b19c67fb840d9f8a1abf22dfb13438`  
		Last Modified: Sat, 08 Nov 2025 03:45:18 GMT  
		Size: 305.1 MB (305112531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:2f0ab91ac55a141f05a809e81d7b28ed95c221e1877c7c2c00e1aa55342362a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16310868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:284a6ae5a10b8073d887c3895583671ca3ee6046414c10fb34f42add1e49cf66`

```dockerfile
```

-	Layers:
	-	`sha256:ee294e4cca1bc64fce75deb66d4df267004d251a94155ab7a82d64171dacca67`  
		Last Modified: Sat, 08 Nov 2025 05:20:49 GMT  
		Size: 16.3 MB (16300691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e22948fdf17087865265a2f446a5a9e7989edff5ff22f778355c7da8d9ded1b4`  
		Last Modified: Sat, 08 Nov 2025 05:20:50 GMT  
		Size: 10.2 KB (10177 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:7f2ba0599577a7aed705697ad2436b5fa8a23dc5d03157963dcaf05338c56bc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.5 MB (311460125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27ed8dc529089f96f69eafc4b46af6004720130fc4aeef130700c981cd4104fc`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1762202650'
# Tue, 04 Nov 2025 10:00:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 14:50:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 17:26:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:aa89048d1c3c931b297cf2d408ea7138528530c43e452af625223e71f97282b3`  
		Last Modified: Tue, 04 Nov 2025 00:14:09 GMT  
		Size: 48.3 MB (48343062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5fd290c851a8e221175041f9832e015aa1560214f438629f7d489ba726030d3`  
		Last Modified: Tue, 04 Nov 2025 10:01:24 GMT  
		Size: 28.3 MB (28319729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dc578ee5dbdb569a00fdc4f0f6cf56b364e8c2a978570ac8bfe2654c08bf3c0`  
		Last Modified: Tue, 04 Nov 2025 14:51:10 GMT  
		Size: 69.2 MB (69186605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d256c6f7a44165be274215925862c2576bc84ca02e76724dbdf34b36c488dced`  
		Last Modified: Wed, 05 Nov 2025 03:18:29 GMT  
		Size: 165.6 MB (165610729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:1917bc6a3e7c4a7a50f27bd35297d3ae59b592404b0f0ff6a2846a51c92a7799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.0 MB (16029647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df78cc2b72a24ab7c164e2d833642aff5695fcda780864d00ad17368a8c2878e`

```dockerfile
```

-	Layers:
	-	`sha256:da9938cb0940cb6fae326cf244c4224627eb78840399ecc2046ea07b2b01857a`  
		Last Modified: Tue, 04 Nov 2025 20:21:19 GMT  
		Size: 16.0 MB (16019502 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ff107daa3500a3397ac4155894aed0084c54eb176f45d91ece7f3d84b29e09f`  
		Last Modified: Tue, 04 Nov 2025 20:21:21 GMT  
		Size: 10.1 KB (10145 bytes)  
		MIME: application/vnd.in-toto+json
