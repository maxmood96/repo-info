## `buildpack-deps:testing`

```console
$ docker pull buildpack-deps@sha256:3e77c77b5a519d06a4e676f959966803d56409d553c94c86a265f53409cbec48
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
		Last Modified: Tue, 04 Nov 2025 07:43:25 GMT  
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
		Last Modified: Tue, 04 Nov 2025 03:22:36 GMT  
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
		Last Modified: Tue, 04 Nov 2025 03:16:00 GMT  
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
		Last Modified: Tue, 04 Nov 2025 03:15:55 GMT  
		Size: 16.3 MB (16327387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66784ed358ab9a147898a702f4e9a755972fb2ff6f7ec024a89e1dafbd142a94`  
		Last Modified: Tue, 04 Nov 2025 03:15:54 GMT  
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
		Last Modified: Tue, 04 Nov 2025 03:16:19 GMT  
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
		Last Modified: Tue, 04 Nov 2025 03:16:15 GMT  
		Size: 16.2 MB (16222617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:319d0e46220464849997d05f8089917ec91868346122271e7f3ab4bf083ae614`  
		Last Modified: Tue, 04 Nov 2025 03:16:14 GMT  
		Size: 10.1 KB (10123 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; ppc64le

```console
$ docker pull buildpack-deps@sha256:eeb80dfa570df5103bc2a7b85f9a690ad4b6c744dc30b02ce29ef590273d0070
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **695.3 MB (695251351 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22bf5991df99734dd2aa0275806d8f2b7ebf4d0b5c4376f42a9519bcc71286d5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:e7d4356e03351899ba9f4be32ba46e679bea4702bcfe72d9b6fe6e31094e1e6b`  
		Last Modified: Tue, 21 Oct 2025 00:20:47 GMT  
		Size: 54.9 MB (54875797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5bcc30631d4ebf74056ea48897550384c1481cf43eaade92e3921cc0643a2bf`  
		Last Modified: Tue, 21 Oct 2025 07:44:17 GMT  
		Size: 27.5 MB (27478769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d87a04ce21422586329cf59f62b4efbec13228e3bd60b2f1a900885826778f60`  
		Last Modified: Tue, 21 Oct 2025 17:32:33 GMT  
		Size: 73.7 MB (73699578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d13b1c6fe96ded03ba62f142f974448ef1505ea0e5587fd6b8f1fa54f975800a`  
		Last Modified: Wed, 22 Oct 2025 05:33:52 GMT  
		Size: 539.2 MB (539197207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:141f814470e48d31e9249a52c07b1bf1caa3e7bebcb4cbc6835c9e3fc5e35875
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.3 MB (16286458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bfb5c9761228f7c1801c3b0ead80a4ef0c82ec5afff4b682dd33c0ad35a8cf`

```dockerfile
```

-	Layers:
	-	`sha256:0d8be0934b536e4fec97e376c6f1ec8c6e7eb2f30ae3a15af5329ad32160f62c`  
		Last Modified: Wed, 22 Oct 2025 01:20:37 GMT  
		Size: 16.3 MB (16276238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c70e2f0e166b68604dcb0242bf8b8d2122923e7128a9dd63a033ef3cd02eeb5`  
		Last Modified: Wed, 22 Oct 2025 01:20:38 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; riscv64

```console
$ docker pull buildpack-deps@sha256:881bd26a38de150a5f93cc4f04d5fa860656993bd526845a3153b9abac2729ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 GB (1075336072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a6c85816df80e69b4df12979be107f3483b44a956ed93a4c28271a3d1321e5`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 'riscv64' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:900b76287341e8d31ab6f7e93e1704f0b3f8f921cc26e9b52c61d9ca744682fb`  
		Last Modified: Tue, 21 Oct 2025 00:21:40 GMT  
		Size: 48.0 MB (48011809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b707e625b2b66ed8212d08094e38d3d8ad6190ee6fb155233b24c4272dcc4f`  
		Last Modified: Wed, 22 Oct 2025 18:02:35 GMT  
		Size: 25.4 MB (25350235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f289a49d4334af2a7114772c1c1dd72325f16c273184dbfad686587605e372ef`  
		Last Modified: Fri, 24 Oct 2025 21:19:28 GMT  
		Size: 67.2 MB (67210026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82ca0b0305876a7f03a9d7ed90e068976b7df67da5099d5ef60772e031aff991`  
		Last Modified: Sun, 26 Oct 2025 13:45:42 GMT  
		Size: 934.8 MB (934764002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:bc5582737b758a7ca027b23d73b91d6b8085aa1aa930b1bc5055711e6d1b9dca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.4 MB (16359069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f78d8bfea2b3b24547501faa400fe1e02855ac7b08cf4892e11caea83d772fe0`

```dockerfile
```

-	Layers:
	-	`sha256:c205615429681f7dc6a8fc0dfd286e2972fe9ac84766242db2da18d4ffe171a0`  
		Last Modified: Sun, 26 Oct 2025 13:20:42 GMT  
		Size: 16.3 MB (16348849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:840791d14c4b53ca708f9343f83b23aedcd8b91d640a47a003866552b0514d5e`  
		Last Modified: Sun, 26 Oct 2025 13:20:43 GMT  
		Size: 10.2 KB (10220 bytes)  
		MIME: application/vnd.in-toto+json

### `buildpack-deps:testing` - linux; s390x

```console
$ docker pull buildpack-deps@sha256:a5f4ac1e99941781e12e150565494b91910b625af3b3d46f9242963ccba20528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **648.3 MB (648325650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e1b37e122033c6adbffe3c4778b8f47117d2e5b534cf4fe0c8d6daeecb530e8`
-	Default Command: `["bash"]`

```dockerfile
# Tue, 12 Aug 2025 22:12:51 GMT
RUN # debian.sh --arch 's390x' out/ 'forky' '@1760918400'
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
# Tue, 12 Aug 2025 22:12:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:4c17c2477a00887cc596493d4aa463fcafb677435d66760d41166feb0acd2773`  
		Last Modified: Tue, 21 Oct 2025 00:22:26 GMT  
		Size: 49.6 MB (49620788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e3fe8a7e87d33de6f27420b538e4d4def300139279c514e15386689dae092d6`  
		Last Modified: Tue, 21 Oct 2025 12:37:54 GMT  
		Size: 27.2 MB (27216829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2021b48125f7f538d074d5cee67536afd71a173bb0f5407bc24672bc22a16e47`  
		Last Modified: Tue, 21 Oct 2025 23:22:56 GMT  
		Size: 69.2 MB (69196789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac8a26c0835e294ae417ca3df33e1fb25eadafddd60be660cdd26ceb285160fb`  
		Last Modified: Wed, 22 Oct 2025 08:26:50 GMT  
		Size: 502.3 MB (502291244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:testing` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:29eba0ccbc970c3cef69153ab79c7b70ae03678005c544e3bea21502b56824d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.1 MB (16078924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8c1d95a38adeb2e5a54304f0b49aadf1afafcaf1f9e7f5216e959a58a8a470`

```dockerfile
```

-	Layers:
	-	`sha256:245f5cc3e8309757c34f15bb5aff14e256f626bfe94b881bb089cb7265b4e7ce`  
		Last Modified: Wed, 22 Oct 2025 07:20:50 GMT  
		Size: 16.1 MB (16068736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:57e655ecf7fa57153ca4f07c971ac0d1bf7c10b84b2dcbebc450e8137b7cf259`  
		Last Modified: Wed, 22 Oct 2025 07:20:51 GMT  
		Size: 10.2 KB (10188 bytes)  
		MIME: application/vnd.in-toto+json
